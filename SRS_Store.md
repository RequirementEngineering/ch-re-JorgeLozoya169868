  <h1 align="center"> Universidad Autonoma de Ciudad Juarez</h3>
  <h2 align="center"> División Multidisciplinaria de Ciudad Universitaria </h3>
  <p align="center"><img src="fig/uacj_logo.png" height="458" width="350"></img></p>
  <h2>SRS Document: Process of Electronic Store</h3>
  <h3 align="center">By:Jorge Lozoya Acosta</h3>
  <h3 align="center">169868</h3>
  
# Table of contents
* [Introduction](#Introduction)
    - [Purpose](#Purpose)
    - [Scope](#Scope)
    - [Definitions, acronyms, and abbreviations](#Definitions-acronyms-and-abbreviations)
    - [References](#References)

* [Overrall description](#Overall-description)
    - [Business Managment Process](#Business-Managment-Process)
    - [Product perspective](#Product-perspective)
    - [Product Functions](#Product-functions) 
    - [Principal Actors](#Principal-Actors)
    - [User characteristics](#User-characteristics)
    - [Constrains](#Constrains)
    - [Assumptions and dependencies](#Assumptions-and-dependencies)
* [Specific requirements](#Specific-requirements) 
    - [User Interface](#User-Interface)
    - [Requirements](#requirements)
       - [Functional Requirements](#Functional-Requirements)
       - [Non functional Requirements](#Non-functional-Requirements) 
       - [System Requirements](#System-Requirements)
       - [User Requirements](#User-Requirements)
* [Appendices](#Appendices) 
   - [Elicitation process](#Elicitation-process)
    

# Introduction
## Purpose

Although this project has an academic focus, the chosen theme will help to understand the CRUD system (Create, Read, Update and Delete) and its requirements in a simpler way. In this document the role of the users and their interactions, requirements of the problem and its description will be detailed. A user interface will also be proposed and its limitations will be planed.

## Scope

"Electronics Store Management " (ESM) is an application that simulates the processes carried out in a specialized store, where you can create, read, update and delete products from a store. It will have as data the name of the product, an ID and its price.

Different users interact in different ways, each one has activities that influence the flow of the process.

Although the project can be managed and designed to be commercialized, it will be more focused on an academic purpose.

## Definitions, acronyms, and abbreviations
- ESM Electronics Store Managment
- .vpp File of Visual Paradigm Proyect
- BMP Business Managment Process
- CRUD Create, Read, Update and Delete
- AS Assumptions
- DE Dependencies

## References
Weinzimer, P. (2014, 14 August). 7 Steps to Excellent Service Delivery. Recovered 12 May, 2019, from https://www.cio.com/article/2462369/7-steps-to-excellent-service-delivery.html
# Overall Description
## Business Managment Process
For the bussiness Managment Pocess, it will be planned as shown in the following figure, where it was designed from the [elicitation process](#Elicitation-process)
 ### Main BMP Diagram
 ![MainProcess_BPM](fig/ElectronicStore_MainProcess.jpg)
 
 * Here you can see how the process of an electronic store is deployed with the main process of buying and selling products.
 * You can also see the interaction between the internal and external users of the process, with the main external suppliers.

* ![Make Order Process](fig/MakeOrderProcess.jpg)

Throughout this process (Make orders) you can see the path a product takes to be received in the store. All procedures that are carried out to confirm purchases and orders.

In case you want to review more thoroughly you can download the .vpp file by clicking on the following link [File .vpp](https://github.com/RequirementEngineering/ch-re-JorgeLozoya169868/blob/master/fig/ElectronicStore.vpp).

## Product Perspective

The system consists of a query application, therefore, show the current status of each product and generate a bar code so that the product can be purchased directly. The client will be able to see all his products seeing the inventory that the electronics store has, so he will only have to pay for them. 

## Product functions
* Update the product
* To be able to make requests to suppliers.
* To be able to add new products
* Send a message to the sales manager in case the chosen product is not in the store.
* Generate tickets

## User characteristics

There are five types of users: the customers, departement of sales and department risks, employee of sales and the suppliers of the electronics store. Each of them has different use cases and therefore each one has different characteristics in the requirements.

| User| Description|
| ------------- |:-------------:| 
| Customers | Has waiting times when making the purchase and interacts with the selling employees      |
| Risk Department| It is the intermediary between the management of resources and suppliers | 
| Sale Manager | He is in charge of reviewing the inventory and buying from suppliers |
| Sale Employers |They can make product update|
| Suppliers | Sell products to the store|

## Constraints

It is necessary to know better the process for an optimal process and to improve the waiting time.

## Assumptions and dependencies
| AS (Assumption) DE(Dependencies)| Description |
| ------------- |:-------------:| 
| AS-1:| Maybe a product is not available.  |
| AS-2:| The customer waits in the line at least half an hour.|  
| DE-1:| Internet Connection |
| DE-2:| There are always available providers.|

# Specific requirements

## User Interface
There will be a screen where the scanned product will be displayed. The sales manager will be shown the status update of the purchased product. This will happen when the customer buys a product.

Other features and extra features are:
* Add products
* Delete products
* Changes products
* Send messages between departments and users
* Generate ticket

## Requirements

### Functional Requirements
**A general use case**

![General_UseCase](fig/General_UseCase.jpg)

User  | Description
 ----- | -------------
 Name | Electronic Store
 Author | Jorge Lozoya
 Date | 08/05/2019
 Brief Description |The main function of the system is to register the sale of a product in order to update the information in the inventory and thus notify it to the sales manager to make decisions regarding the orders of new or more products.
 Actors | Sale Department
 Pre-conditions | Have sales
 Normal flow | Client: Buy a product. Sale Employer: Check the payment process of the customer's product. The information of the products is updated.
 Alternative flow | Something is wrong with the inventory system. The product can not be sold.
 Post-conditions | Generate a ticket.
 
 - **Specific requirement: Sell Product**
 
 ![UseCase1_SellProduct](fig/UseCase1_SelProduct.jpg)

User  | Description
 ----- | -------------
 Name | Sell product
 Author | Jorge Lozoya
 Date | 08/05/2019
 Brief Description |The client wants to pay for a product so he interacts with the sales employee, the employee performs the payment process and generates a ticket for the client.
 Actors | Customer and sale employer
 Pre-conditions | Buy at least one product
 Normal flow | Client: Buy a product. Sale Employer: Check the payment process of the customer's product. Generate a sale's ticket
 Alternative flow | Something is wrong with the inventory system. The product can not be sold.
 Post-conditions | Generate a ticket.
 
  - **Specific requirement: Check Inventory**
  
 ![UseCase2_CheckInventory](fig/UseCase2_CheckInventory.jpg)
 
 User  | Description
 ----- | -------------
 Name | Check Inventory
 Author | Jorge Lozoya
 Date | 08/05/2019
 Brief Description | When a sales ticket is generated, the inventory is updated on its own. Then the manager has to review it so they do not run out.
 Actors | Sale manager and Risk department
 Pre-conditions | A product below 3 units
 Normal flow | The sales manager, after checking the inventory, makes a request to the risk department to have more products.
 Alternative flow | Nothing.
Post-conditions | Nothing.

 - **Specific requirement: Request Products**
 
![UseCase3_RequestProducts](fig/UseCase3_RequestProducts.jpg)
 
 User  | Description
 ----- | -------------
 Name | Request Products
 Author | Jorge Lozoya
 Date | 11/05/2019
 Brief Description |The manager sends an order to the risk department, then the finance department is in charge of contacting the supplier and receiving the product.
 Pre-conditions | A product below 3 units
 Normal flow | A specific product is requested, this request is sent to finance and then finance is in charge of finding the supplier and making the purchase of the product. It also ensures that the product arrives at the store.
 Alternative flow | It may take longer than expected.
 Post-conditions | The product arrive.
 
  - **Specific requirement: Receive Product**
  
![UseCase4_ReceiveProducts](fig/UseCase4_ReceiveProducts.jpg)
 
 User  | Description
 ----- | -------------
 Name | Request Products
 Author | Jorge Lozoya
 Date | 11/05/2019
 Brief Description |The manager receives a product and updates the status.
 Pre-conditions |Arrival of a new product
 Normal flow | The manager receives a product and updates the status.
 Alternative flow | The product has not arrived. Then send another request to the risk department
 Post-conditions | The product has been updated.
 
### Non-Functional Requirements
* The approach of security in the purchase and sale of products must be maximum
* Usability must satisfy the client being comfortable for them.
* The fast delivery of products does not have to take more than 2 months
* Messages and requests must be made at the moment they are sent.
* Always try to have product availability
* With the help of tickets and various vouchers you will have an organized system of products.
### System Requirements
* Send low product alerts in the inventory
* Export data in a PDF file
* Generate sales graphs
* Availability of supplier products.
* Be able to generate reports
* Generate requests to purchase products from suppliers
### User Requirements
* Show the price of the product sold to the customer
* Generate product status
* Allow verification of product availability
* Update the purchase number to be assigned to each customer
* Being able to print the data

# Appendices
## Elicitation Process

*Interview: First day*

**Interviewer:** What kind of processes exist here?

**John Smith(owner):** Well, first of all, the products come from different suppliers.

**Interviewer:** Who is the person in charge of the inventory?

**Owner:** We have a manager. He is in charge of inventory and employees.

**Interviewer:** Who else has access to the inventory?

**Owner:** Oh, the system allows employees to remove a product from inventory by selling it


*Inverview: Second day*

**Interviewer:** Well, how long do customers usually wait in their lines?

**Owner:** About half an hour, although normally we do not have that problem

**Interviewer:** So what is the problem?
 
**Owner:** When a customer buys a product, there is the possibility of not having it in stock.Then we see if the product is in the cellar.

**Interviewer:** What happens if you do not have it in the cellar?

**Owner:** Oh, we notify you that the product asks the customer does not have it and we send a request to the risk department

*Conversation: Fifth day*

**Sales employee:** When a customer buys a product, a payment process is initiated, where I capture the payment either in cash or with a card and in the end the customer receives the ticket for his purchase.

**Sales Manager:** Yes, every time a ticket is generated, the system updates the product data, that is, when we have available products in the store and in the inventory. Then, I have to verify that the inventory does not have any risk of being empty, in case there are only three units left I send an order to the risk department so they know about the inventory problem.

*Conversation: Sixth day*

**Risk department:** From time to time we receive orders from the sales manager, what we do is identify the most trusted supplier and contact him. Next, we call the finance department to authorize payment.

**Finance:** We review all the requests and, depending on the price and our funds, we authorize the purchase to the supplier. The supplier sends his product once the purchase is made and the product reaches the sales department.

*Conversation: last day:*

**Sale Manager:** When I receive a product that I could, update the data in the system and arrange it in the store. When I receive a product that I could, update the data in the system and arrange it in the store. The voucher of the purchase is also kept with the supplier.

**Finance:** The normal process of the providers is:
- They receive the product order
- They wait for the payment order and its confirmation
- In case the payment does not arrive, the order is canceled
- If we do not take more than one month making the payment process the order
- In case of not having the product, production begins
- We are notified of your delivery
- We receive the delivery and send it to the sales department.
