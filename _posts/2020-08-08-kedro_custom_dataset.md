---
published: true
title: How to create a custom Kedro DataSet
collection: cv
layout: single
author_profile: true
read_time: true
categories: [projects]
header :
    teaser : /assets/images/kedro_banner.png
comments : true
toc: true
toc_sticky: true
sidebar:
    nav: sidebar-sample
---

In the following article, i will show how to create a custom dataset for  [Kedro](https://github.com/quantumblacklabs/kedro), an open source Python library for Production-Ready Machine Learning Code. 


The custom dataset will be used to read
DICOM files and produce image and CSV datasets which are native Kedro datasets.

This article is linked to  my article on [how to create a kedro project](https://tdenimal.github.io/projects/kedro/) and my project on [pneumothorax classifier](https://tdenimal.github.io/projects/xray-classif_EDA/), you will find more informations on the DICOM dataset there.


To be able to read and extract data from DICOM files, we will use the [pydicom](https://github.com/pydicom/pydicom) library.



# DICOMDataSet class

```python
from typing import Any, Dict, List

import numpy as np

from kedro.io import AbstractDataSet


class DICOMDataSet(AbstractDataSet):
    """``DICOMDataSet`` loads / save DICOM file from a given filepath as Image DataSet and CSV DataSet using pydicom library.

    Example:
    ::

        >>> DICOMDataSet(filepath='/img/file/path.dcm')
    """

    def __init__(self, filepath: str):
        """Creates a new instance of DICOMDataSet to load / save DICOM file at the given filepath.

        Args:
            filepath: The location of the DICOM file to load / save data.
        """
        self._filepath = filepath

    def _load(self) -> np.ndarray:
        """Loads data from the image file.

        Returns:
            Data from the image file as a numpy array.
        """
        ...

    def _save(self, data: np.ndarray) -> None:
        """Saves image data to the specified filepath"""
        ...

    def _describe(self) -> Dict[str, Any]:
        """Returns a dict that describes the attributes of the dataset"""
        ...
```

First create a new  conda virtual environment :
kedro is compatible with python 3.6, 3.7 and 3.8 versions. Here i choosed 3.7.
```bash
conda create -n kedro_project python=3.7
```

Then activate it
```bash
conda activate kedro_project
```

Install kedro from conda-forge repository:


```bash
conda install -c conda-forge kedro
```

Install also kedro-viz plugin, very usefull to display your data pipelines:

## Install kedro-viz plugin

```bash
pip install kedro-viz
```

Verify the installation:

```bash
kedro info

 _            _
| | _____  __| |_ __ ___
| |/ / _ \/ _` | '__/ _ \
|   <  __/ (_| | | | (_) |
|_|\_\___|\__,_|_|  \___/
v0.16.2

kedro allows teams to create analytics
projects. It is developed as part of
the Kedro initiative at QuantumBlack.

Installed plugins:
kedro_viz: 3.4.0 (hooks:global,line_magic)

```

# Create your Data Science project

We are going to create our datascience project directory using Kedro. It will initialize all the needed directories using a [cookiecutter](https://cookiecutter.readthedocs.io/) template.

First go to the directory where you're used to create your projects repos ( mine is /home/tdenimal/Dev )

```bash
cd /home/tdenimal/Dev
```

Then create project and choose the project name,  leave the other choices at their default value.
I choosed pneumothorax, to create the project directory for the [following work](https://tdenimal.github.io/projects/xray-classif_EDA/).

```bash

kedro new
Project Name:
=============
Please enter a human readable name for your new project.
Spaces and punctuation are allowed.
 [New Kedro Project]: pneumothorax

Repository Name:
================
Please enter a directory name for your new project repository.
Alphanumeric characters, hyphens and underscores are allowed.
Lowercase is recommended.
 [pneumothorax]: 

Python Package Name:
====================
Please enter a valid Python package name for your project package.
Alphanumeric characters and underscores are allowed.
Lowercase is recommended. Package name must start with a letter or underscore.
 [pneumothorax]: 

Generate Example Pipeline:
==========================
Do you want to generate an example pipeline in your project?
Good for first-time users. (default=N)
 [y/N]: 

Change directory to the project generated in /home/tdenimal/Dev/pneumothorax

A best-practice setup includes initialising git and creating a virtual environment before running `kedro install` to install project-specific dependencies. Refer to the Kedro documentation: https://kedro.readthedocs.io/


```

