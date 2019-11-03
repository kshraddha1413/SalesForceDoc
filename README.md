*Introduction to Data Import*
=======
Salesforce offers two main methods for importing data.
1)Data Import Wizard
2)Data Loader

**Use the Data Import Wizard When:**

You need to load less than 50,000 records.
The objects you need to import are supported by the wizard.
You don’t need the import process to be automated.

**Use Data Loader When:**

You need to load 50,000 to five million records. If you need to load more than 5 million records, we recommend you work with a Salesforce partner or visit the AppExchange for a suitable partner product.
You need to load into an object that is not supported by the Data Import Wizard.
You want to schedule regular data loads, such as nightly imports.

A *profile* is a collection of settings and permissions. Profile settings determine which data the user can see, and permissions determine what the user can do with that data.


**Standard Profiles**
The platform includes a set of standard profiles. Some examples are:

Read Only
Standard User
Marketing User
Contract Manager
System Administrator

The System Administrator profile also includes two special permissions:
View All Data
Modify All Data

** four ways to control access to records**

1)Org-wide defaults specify the default level of access users have to each other’s records.
2)Role hierarchies ensure managers have access to the same records as their subordinates. Each role in the hierarchy represents a level of data access that a user or group of users needs.
3)Sharing rules are automatic exceptions to org-wide defaults for particular groups of users, to give them access to records they don’t own or can’t normally see.
4)Manual sharing lets record owners give read and edit permissions to users who might not have access to the record any other way.


*Sharing rules*
Each sharing rule has three components.
1)Share which records?
2)With which users?
3)What kind of access?

*Define a Public Group*
Before creating a sharing rule, it’s important to set up the appropriate public group. A public group is a collection of individual users, other groups, individual roles or territories, and/or roles or territories with their subordinates that all have a function in common.

**Formula Field**
The formula editor comes in two flavors: Simple and Advanced. 

**Introduction to Roll-Up Summary Fields**
While formula fields calculate values using fields within a single record, roll-up summary fields calculate values from a set of related records, such as those in a related list. 

**Defining a Roll-Up Summary Field**
Since roll-up summary fields are based on master-detail relationships, it’s useful to review object relationships before creating a roll-up summary field.

**Lighting Flow**
Lightning Flow is the name of the product.
Process Builder and Flow Builder are the names of the tools.
Use Process Builder to make processes; use Flow Builder to make flows.

**Prcocess builder**
Process Builder is a point-and-click tool that lets you easily automate if/then business processes and see a graphical representation of your process as you build.
**The Components of a Process**
**Trigger**: Identify When the Process Should Run
**Criteria**: Determine Whether or Not to Execute Actions
**Actions**: What the Process Should Do


**Lightning Flow**—the product that encompasses building, managing, and running flows and processes.
**Flow Builder**—a point-and-click tool for building flows.
**Flow**—an application that automates a business process by collecting data and doing something in your Salesforce org or an external system.
In short, the Lightning Flow product includes a couple of tools. One of them, Flow Builder, lets you create flows.


**Flow Building Blocks**
Every flow is made up of three building blocks.

Elements (1) appear on the canvas. To add an element to the canvas, click it or drag it there from the toolbox.
Connectors (2) define the path that the flow takes at runtime. They tell the flow which element to execute next.
Resources (3) are containers that represent a given value, such as field values or formulas. You can reference resources throughout your flow. For example, look up an account’s ID, store that ID in a variable, and later reference that ID to update the account.

**Mobile App Customization**
 There are two types of actions:
 1)global and 
 2)object-specific.
 
 But be aware that global actions can’t update a record. Only object-specific actions can do that.
 
 
 
 Action layouts...global publisher layouts...page layouts…compact layouts.
 
 
  two main options you have for customizing your users’ navigation experience, the Mobile Only app and Lightning apps.
 
 Well, we need visual cues to find our way in apps, too. And that’s what the mobile navigation menu is: a signpost. Your users rely on it to get from place to place in the Salesforce mobile app as efficiently as possible.
 
 
 

