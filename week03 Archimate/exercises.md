# Week 03 Exercises

## Exercise 01 Speedy
Speedy is a delivery company that wants to create a new reporting system for the top management. After inspecting the sales reports, the top management may also need to query the existing ERP system, based on Oracle Fusion, to get detailed sales and HR information.

To implement the reporting system, a data warehouse (DW) based on Microsoft SQL Server 2022 will be used. The DW will run three components responsible for extracting sales data from the ERP database, managing analysis data, and generating sales reports.\
The DW will run on-premise on a different node than the one running the ERP. Both nodes will share the same LAN.

ArchiMate models representing the business goals and the existing ERP system looks like the following:

**Motivation**:
![](./exercise%20files/ex01_speedy_motivation.png)

**Existing ERP System**:
![](./exercise%20files/ex01_speedy_ERP_system.png)

Starting from these models, create a complete ArchiMate model that: 
1. fully represents the business layer and links it to the application layer, 
2. extends the application and technology layers by adding the elements required for the new reporting service.


### Teachers solution

![](./exercise%20files/teachers%20solutions/speedy_complete_solution.png)


## Exercise 02 IC
IC is an insurance company which wants to offer a new insurance service for small objects (<2000$) managed completely online for reliable customers. To achieve this, a customer who wants their assets to be insured has to provide its credentials and photo of the asset and its details (serial number, purchase date) to IC. To ensure that the customer is reliable and the asset inexpensive, IC will then check the customers credentials and past history and estimate the asset’s price. If the checks succeed, a proposal will be generated. Otherwise, the request will be rejected.

To support the new service, IC needs to develop a new application with the following functionalities: proposal generation, price estimation, customer reliability check.

The new application will be implemented as a Java EE component running on Apache Tomcat. It will also rely on an operational database deployed on Oracle MySQL. Both the database and the application will reside on a dedicated server, which is connected to the corporate LAN.
To estimate an item price, an external service will be used.
To check the customer reliability, the application needs data coming from the company’s CRM, exposed by the CRM as a REST service and accessed through the corporate LAN.
The corporate LAN is separated from the public Internet by a firewall.

Model in ArchiMate the service provided by the company and its infrastructure.

### Teachers solution

![](./exercise%20files/teachers%20solutions/ic_complete_solution.png)

## Exercise 03 Tel
TEL is a telephony company interested in improving its customer experience. Currently, billing details are only accessible internally by TEL staff.
Data about telephony usage is stored on a Linux server running IBM DB2 UDB database, and it can only be accessed through SQL queries. Conversely, billing information is stored and handled by a legacy transactional CICS application running on an IBM mainframe.

To improve its customer experience, TEL wants to develop a new web portal that can provide real-time billing details to users. In particular, the new portal will provide two main functionalities: inspect billing information and inspect usage information. 
The process enabled by the new portal will be organized as follows: 
- the user logs in the portal, 
- then they can select an item to inspect from the menu,
- finally they can view the billing details in a dedicated page.

The new portal will be built for Microsoft SharePoint Online PaaS cloud service.
To access data from the existing infrastructure, a new node running Microsoft BizTalk Server 2020 middleware will also be introduced. BizTalk Server will offer a gateway service, making CICS applications and relational databases accessible through a standard REST interface.
An ArchiMate model of the existing system is enclosed in the next slide. Extend the model by adding the elements required for the new service.

### Teachers solution

![](./exercise%20files/teachers%20solutions/tel_complete_solution.png)