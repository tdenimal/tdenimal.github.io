---
published: false
title: Why data mesh ?
collection: data_architecture
layout: single
author_profile: true
read_time: true
categories: [projects]
header :
    teaser : /assets/images/what-is-data-mesh-architecture.jpg
comments : true
toc: true
toc_sticky: true
sidebar:
    nav: sidebar-sample
---


What is data mesh ? 
The data mesh is a decentralization paradigm opposed to old school centralized data architectures ( and organisations) like Enterprise Datawarehouses or datalake.

Data Mesh has gained popularity in recent years due to its ability to address the challenges of traditional centralized data architectures, such as slow data delivery, siloed data, and lack of alignment between technical and business domains. It allows for greater agility and autonomy for domain teams, and promotes a culture of collaboration and shared responsibility for data.

However, Data Mesh also has its drawbacks. Implementing a Data Mesh architecture requires a significant cultural shift and a high level of trust and collaboration between domain teams. It also requires a robust governance framework to ensure data quality, consistency, and security across the organization. Additionally, it can be complex to implement and maintain, as it requires a significant amount of coordination and collaboration between domain teams.

Data Mesh is a promising approach for managing large-scale data estates, but it requires careful planning and a strong commitment from the organization to be successful.

Datamesh is more than architecture; look at the 4 pilliars (i will go in more details for each pilliar in a specific post):

- Domain ownership

Following decentralization paradigm, the domain ownership principle requires domain teams to take responsibility for their data. Data Mesh is built around business domains, each with its own data, services, and teams. This alignment with business domains ensures that data is understood and managed in the context of the business, aligning technology with business strategy.

Data Mesh encourages the creation of autonomous domains, where each domain is responsible for its data. These domains are typically aligned with business units or functional areas. Each domain should have domain-specific experts who understand the data and the business context.

- Data-as-a-product

In Data Mesh, data is owned, managed, and curated by the teams that produce it. This decentralization empowers teams to make decisions about their data and encourages them to be more accountable for its quality and usage.

Data should be treated as a product, with its own lifecycle, versioning, and APIs. This approach encourages the creation of reusable, discoverable, and consumable data assets.

There is different types of data products in data mesh litterature :

1. **Consumer-Aligned Data Products**: These data products are built with the end user in mind, focusing on the specific needs and requirements of the consumers. They are designed to provide actionable insights and are often used in real-time decision-making processes.

2. **Source-Aligned Data Products**: These data products are created by the data providers and are based on the source systems. They are often used for internal operations, data validation, and quality checks.

3. **Aggregated Data Products**: These data products combine data from multiple sources to provide a more comprehensive view. They can help in gaining insights that might not be possible with individual sources.

4. **Virtual Data Products**: These data products are not physical entities but represent a composition of other data products. They can be used to create complex analytics, dashboards, or reports.


- Self-serve infrastructure

Data Mesh enables self-service data access, allowing data consumers to find, access, and use data on their own, without relying on a centralized data team. This empowers business users to make data-driven decisions more quickly and effectively.

A data mesh requires a self-service platform that enables domain teams to publish, discover, and consume data products easily and efficiently. This self-service platform should provide open and standard interfaces for data processing, quality, and monitoring.

The Data Mesh provides a self-serve platform that abstracts technical complexity, allowing users to focus on their data use cases. This platform enables domain teams to create, manage, and consume data products easily.

- Federated governance

Federated governance is the shared responsibility of governing data across the organization. This means that rather than having a centralized data governance team, data governance is distributed across the domain teams, who work together to ensure data consistency and quality.


Pros of Data Mesh vs Traditional Centralized Data Warehousing:

1. **Flexibility:** Data Mesh allows for more flexibility in how data is managed and used, as it is decentralized and product-oriented.

2. **Efficiency:** By enabling self-service data access, Data Mesh reduces the burden on centralized data teams and allows business users to access data more quickly.

3. **Responsiveness:** As data is owned and managed by the teams that produce it, Data Mesh allows for faster response times to changing business needs.

Cons of Data Mesh:

1. **Complexity:** The decentralized nature of Data Mesh can lead to increased complexity, as multiple teams are managing and curating data.

2. **Quality:** Ensuring data quality can be challenging in a decentralized environment, as there may be inconsistencies and duplications across different domains.

3. **Governance:** Establishing and maintaining data governance can be difficult in a self-serving environment, as there may be less oversight and control.

Let's deep dive on each principle in next posts.


