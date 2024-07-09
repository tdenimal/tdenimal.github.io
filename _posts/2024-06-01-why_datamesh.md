---
published: true
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

# Introduction to Data Mesh: A Modern Approach to Data Management

Data Mesh is a decentralized data management architecture that breaks away from the traditional centralized data architectures ( and organisations) like Enterprise Datawarehouses or datalake.

Data Mesh has gained popularity in recent years by removing bottlenecks in the data value stream [1](#Dehghani2022) due to its ability to address the challenges of traditional centralized data architectures, such as slow data delivery, siloed data, and lack of alignment between technical and business domains. It allows for greater agility and autonomy for domain teams, and promotes a culture of collaboration and shared responsibility for data.
This decentralization also allows for greater accountability, as the teams with the greatest expertise about the data are responsible for its management and maintenance.

It was first described by Zhamak Dehghani as a set of four principles that guide its implementation [2](#Dehghani2023). In this post, we will provide a quick introduction to the Data Mesh concept, describing each of its four principles.


## Four Principles of Data Mesh

Data Mesh principles are the cornerstones of its implementation. These principles help to make data operations efficient at scale and are as follows:

1. **Domain Ownership** : 
    Data Mesh encourages domain teams to take ownership of their data. This means that each domain is responsible for the quality, security, and governance of its data [3](#Dehghani2023).

    Data Mesh is built around business domains, each with its own data, services, and teams. This alignment with business domains ensures that data is understood and managed in the context of the business, aligning technology with business strategy and domain-specific experts knowledge.



2. **Domain Data as a Product**: 
    Each domain treats its data as a product, ensuring it is well-documented, high-quality, and meets the needs of its consumers [2](#Dehghani2023).

    Data should be treated as any product, with its own lifecycle, versioning, and APIs. This approach encourages the creation of reusable, discoverable, and consumable data assets.

    There is different types of data products in data mesh litterature :

    > **Source-Aligned Data Products**: These data products are created by the data providers and are based on the source systems. They are often used for internal operations, data validation, and quality checks. They can be consumed to feed **Consumer-Aligned Data Products** or **Aggregated Data Products**.

    > **Consumer-Aligned Data Products**: These data products are built with the end user in mind, focusing on the specific needs and requirements of the consumers. They are designed to provide actionable insights and are often used in real-time decision-making processes.

    > **Aggregated Data Products**: These data products combine data from multiple sources to provide a more comprehensive view. They can help in gaining insights that might not be possible with individual sources.




3. **Self-Serve Data Platform**: 
    A self-service data platform is provided to enable domain teams to access, transform, and analyze data easily, reducing the reliance on central IT teams [2](#Dehghani2023).

    The self-serve platform abstracts technical complexity, allowing users to focus on their data use cases. This platform empowers domain teams to seamlessly create, manage, and consume data products, making data-driven decisions more quickly and effectively.


4. **Federated Computational Governance**: 
    Last but not least, Data Mesh promotes a federated approach to governance, where decisions are made collaboratively among the domain teams. This means that rather than having a centralized data governance team, data governance is distributed across the domain teams, who work together to ensure data consistency and quality. [3](#Dehghani2023).



### Pros of Data Mesh

- **Increased agility**: Decentralized ownership and decision-making allow teams to respond quickly to changing business needs.
- **Improved data quality**: Domain teams are responsible for the quality of their data, leading to more accurate and consistent data across the organization.
- **Reduced dependence on central IT teams**: Self-service data platforms empower domain teams to access, transform, and analyze data without relying on central IT teams.

### Cons of Data Mesh

- **Requires cultural shift**: The shift from a centralized to a decentralized approach can be challenging and may require significant changes to organizational culture.
- **Increased complexity**: The decentralized nature of Data Mesh can lead to increased complexity, as multiple teams are managing and curating data.
- **Requires strong governance**: A strong federated governance framework is essential to ensure that data is used consistently across the organization.


## Summary


Data Mesh is a promising approach for managing large-scale data estates, but it requires careful planning and a strong commitment from the organization to be successful.

Implementing a Data Mesh architecture requires a significant cultural shift and a high level of trust and collaboration between domain teams. It also requires a robust governance framework to ensure data quality, consistency, and security across the organization. Additionally, it can be complex to implement and maintain, as it requires a significant amount of coordination and collaboration between domain teams.

In summary, Data Mesh is a powerful approach to data management that empowers domains, treats data as a product, and promotes self-service capabilities. By understanding its principles, benefits, and self-service features, organizations can unlock the full potential of their data assets and gain a competitive edge in today's data-driven world.


In next posts we will deep dive in each of the data mesh principles.

## References

- [1] Dehghani, Z. (2022). Data Mesh. [Book].
- [2] Majchrzak, J., Balnojan, S., & Siwiak, M. (2023). Data Mesh in Action. [Book].
- [3] Bellemare, A. (2023). Building an Event-Driven Data Mesh. [Book].
- [4] Schultze, M. & Wider, A. (2021). Data Mesh in Practice. [Book].
