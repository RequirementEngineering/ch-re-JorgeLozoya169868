# Introduction
## Purpose

Although this project has an academic focus, the chosen theme will help to understand the CRUD system (Create, Read, Update and Delete) and its requirements in a simpler way. In this document the role of the users and their interactions, requirements of the problem and its description will be detailed. A user interface will also be proposed and its limitations will be planed.

## Scope

"Electronics Store Management System " (ESMS) will be an application designed to be developed in Java with a database connection, where you can create, read, update and delete products from a store. It will have as data the name of the product, an ID and its price. Where the user will be able to consult said information

There are different users with different authority in the system, to which, not all users can access the data in the same way.

Although the project can be managed and designed to be commercialized, it will be more focused on an academic purpose.

## Definitions, acronyms, and abbreviations

## References

# Overall Description
## Product Perspective

The system consists of an application for consultation and modification of data, therefore it is divided into two parts.
The application needs a constant communication with the database to retrieve the information in real time and thus show the current status of each product and be able to modify this state.


## Product functions

The main function of the system is to provide information to the user and the complete management of the system to the administrator. Thus making an application for the management of a electronics store.

| Class of use cases|Use cases| Description of uses cases|
| ------------- |-------------| -----|
|**Use case related to Installation**   |Installation   |Software pre-installed on a tablet |
|**Use cases related to product database**|Login to the product database| Login into to system |
|| Change IDs| Can change Product's ID|
|| Update inventory | Update purchased and received products |
|| Rename Products | Be able to modify the name of the products|
|**Use cases related to purchases**| Display the price|Show the price of any product|
||Enable purchases in only available products | The client only can buy the available products|
||Do not allow the purchase of stockouts| The client may see the product but can't buy it|
|**Use cases related to securities**|Generate tickets|A ticket is generated to pay at the cashier|
||No purchases allowed from the application |The application will not accept any payment method|
|**Use cases related to alert**|Generate empty inventory alert|When a product is not available, an alert will be sent|
||Show alerts|Show all the pending alerts|

## Principal Actors
The two principal actors in ESMS are "user" and "system".

## User characteristics

There are four types of users: the end user, the administrator, employer and the owner of the electronics store. Each of them has different use cases and therefore each one has different characteristics in the requirements.

| User| Description|
| ------------- |:-------------:| 
| End user | Can only use the application to find stocks of the product. This means that the user can only interact with and search the search interface. It is important that the product that is searched matches the data.      |
| Owner| does not have to navigate in the application, its function will be to modify and update the products but will not have access to the change of ID unless it is a new product. | 
| Administrador | will have access to the data, being able to modify it and confirm that the information is valid. |
| Employers |They can make product delete and update the data|

## Constraints
The different interfaces that are needed can become a restriction due to the difficulty of adapting. Since it opens a difference of navigation depending on the type of user.

The hardware can be an impediment due to the high cost it can generate for a electronics store.

If you want the end user to search for the product, you need a more functional interface that is face-to-face / physical.

## Assumptions and dependencies
| AS (Assumption) DE(Dependencies)| Description |
| ------------- |:-------------:| 
| AS-1:| Only one end user at a time  |
| AS-2:| The final interface will be a tablet application.| 
| DE-1:| Internet Connection |
| DE-2:| Electricity for final device|
## Apportioning of requirements

# Specific requirements

## External interface Requirements

Here you will see all the details about the inputs and outputs that have been planned for the system. There will also be a description of hardware, software and its communication between interfaces and a basic prototype of the user interface is also provided.

## User Interface
## Hardware Interface
## Communications interfaces

# Functional requirements
We describe the funtional requirements by giving various use cases.

 *Use case related to installation:*

 **Use Case 1:** Installation

 *Primary Actor*: Owner

 *Pre Condition*: Have a tablet with ESMS, Pre-made database

 *Main Scenario:*
 1. The store owner turns on the system.
 2. System asks for the dicrectoy of the database.
 3. The owner specifies where is the directory and access.
 4. The system shows a success message
 *Alternate Scenario:*
 3(a). Don't find the directory
 
  *Use case related to product database:*

 **Use Case 2:** Login to the product database

 *Primary Actor*: Administrador

 *Pre Condition*: Have the password, database already installed

 *Main Scenario:*
 1. The administrator logs into the database
 2. Makes the necessary changes
 
 
