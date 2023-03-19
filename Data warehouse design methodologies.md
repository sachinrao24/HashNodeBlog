---
title: "Data warehouse design methodologies"
seoTitle: "Types of data warehouse design methodologies"
datePublished: Mon Feb 13 2023 15:14:36 GMT+0000 (Coordinated Universal Time)
cuid: cle2yhz5n000009mgdc674clo
slug: data-warehouse-design-methodologies
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1676310899411/100b85ae-1102-42e3-b9ef-70151f920789.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1676301176823/5cb73be8-511d-4d0a-9c5a-5f581c1e85f0.png
tags: analytics, data, databases, warehouse, data-engineering

---

A data warehouse can be defined as a repository used to store a massive amount of data in order to transform and analyze it to extract meaningful insights. But how do you go about designing such a warehouse?

In this article, I'm going to talk about 4 different design methodologies and in what situations they can be used for optimal results. These methodologies are-

1. ### Inmon methodology
    
    When the father of the data warehouse creates a design methodology, you know it's going to be good. Developed by Bill Inmon, the Inmon methodology holds the enterprise data warehouse as the core of the architecture. Inmon defined a data warehouse as "subject-oriented, integrated, time-variant and non-volatile".
    
    A single data warehouse acts as a central repository for all data and smaller data marts are created for each business function.
    
    For example, an organization's central warehouse can have data marts for marketing, sales, etc.
    
    The Inmon methodology is a top-down approach or a data-driven approach that uses the idea of a Corporate Information Factory (CIF) consisting of 3 layers- an external layer, an integration/transformation layer and an operational data store.
    
    • The external layer contains all the raw data collected from various sources, external applications and OLTP systems. The data can either be structured or unstructured.
    
    • The integration or transformation layer acts as a staging area where transformation operations can be performed. It focuses on integrating the data from a multitude of sources and the transformed data is loaded into Operational Data Stores and the Enterprise Data Warehouse.
    
2. ### Kimball methodology
    
    Proposed by Ralph Kimball, who defined a data warehouse as "a copy of transaction data specifically structured for querying and analysis", the Kimball methodology identifies the business requirements as its first step.
    
    It is focused on making business intelligence available to the end users as soon as possible, by creating data marts before the creation of the warehouse itself.
    
    Although this method is fast to implement since no normalization is involved, redundant data can exist during the process of updation.
    
3. ### Data vault methodology
    
    This methodology was proposed by Dan Linstedt, and is considered to be a hybrid approach as it combines both the Inmon and Kimball methodologies.
    
    Here, all the raw data is stored before using it for specific business needs.
    
    All the entity tables, referred to as hubs, are connected through a link key table. Hubs contain unique hashed business keys, which are very important since losing them can result in a loss of all information.
    
    Links refer to the relationship between the different business keys, which usually have many-to-many cardinality.
    
    These hubs are also connected to satellites, which contain metadata such as the time when the data was loaded and the data source.
    
    This is an "insert-only" methodology, in which hash keys are used instead of composite or surrogate keys. Data marts are built on top of the vault as views.
    
    The data vault methodology is especially useful for handling streaming data, and can also handle structured and unstructured data.
    
4. ### Wide table or One Big Table
    
    As the name suggests, this methodology proposes the idea of just having one big normalized table, where the need for join operations is eliminated.
    
    It offers faster query performance in comparison with the dimensional modeling approach and provides affordable storage combined with easy scalability using cloud services. This approach is also intuitive to end users, making it really easy to use.
    

If you found this helpful, consider liking and sharing it, and subscribing to my newsletter. Feel free to leave your thoughts, questions and ponderings in the comments.

You can also follow me for more data and ML-related content. I focus on demystifying technical jargon and encouraging newcomers in the field by explaining concepts as simply as possible.
 
This is Sachin being succinct :)
