Force.com, allows admins and developers to create websites and applications into the main Salesforce.com application.
AppExchange is an online application marketplace for third-party applications that run on the Force.com platform.
Heroku Enterprise gives developers the flexibility to create apps using their preferred languages and tools.
Salesforce Thunder is big data and rules processing engine designed to analyze events and take personalized actions.
Salesforce Sandbox allows developers to test ideas in a safe and isolated development environment.






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
 
 **Apex** is a programming language that uses Java-like syntax and acts like database stored procedures. Apex enables developers to add business logic to system events, such as button clicks, updates of related records, and Visualforce pages.
 
 
 Because Apex is a data-focused language and is saved on the Lightning Platform, it has direct access to your data in Salesforce.
 
 **DML Statements**
The following DML statements are available.

1)insert
2)update
3)upsert
delete
4)undelete
5)merge

The *upsert* DML operation creates new records and updates sObject records within a single statement, using a specified field to determine the presence of existing objects, or the ID field if no field is specified.

The *merge* statement merges up to three records of the same sObject type into one of the records, deleting the others, and re-parenting any related records.



You can retrieve a record from the database to obtain its fields, including the ID field, but this can’t be done with DML. You’ll need to write a query by using SOQL. You’ll learn about SOQL in another unit.


You can perform DML operations either on a single sObject, or in bulk on a list of sObjects.


You can delete persisted records using the delete statement. Deleted records aren’t deleted permanently from Lightning Platform, but they’re placed in the Recycle Bin for 15 days from where they can be restored.


**Should You Use DML Statements or Database Methods?**
Use DML statements if you want any error that occurs during bulk DML processing to be thrown as an Apex exception that immediately interrupts control flow (by using try. . .catch blocks). This behavior is similar to the way exceptions are handled in most database procedural languages.
Use Database class methods if you want to allow partial success of a bulk DML operation—if a record fails, the remainder of the DML operation can still succeed. Your application can then inspect the rejected records and possibly retry the operation. When using this form, you can write code that never throws DML exception errors. Instead, your code can use the appropriate results array to judge success or failure. Note that Database methods also include a syntax that supports thrown exceptions, similar to DML statements.
Working with Related Records


When SOQL is embedded in Apex, it is referred to as inline SOQL.

*TRIGERS*
Apex triggers enable you to perform custom actions before or after events to records in Salesforce, such as insertions, updates, or deletions. Just like database systems support triggers, Apex provides trigger support for managing records.

There are two types of triggers.

*Before triggers* are used to update or validate record values before they’re saved to the database.
*After triggers* are used to access field values that are set by the system (such as a record's Id or LastModifiedDate field), and to affect changes in other records. The records that fire the after trigger are read-only.

**USER:**
A user is anyone who logs in to Salesforce. Users are employees at your company, such as sales reps, managers, and IT specialists, who need access to the company's records.

Every user in Salesforce has a user account. The user account identifies the user, and the user account settings determine what features and records the user can access. Each user account contains at least the following:

**Profiles:**
Profiles determine what users can do in Salesforce. They come with a set of permissions which grant access to particular objects, fields, tabs, and records. Each user can have only one profile. Select profiles based on a user’s job function (the Standard User profile is the best choice for most users). Don’t give a user a profile with more access than the user needs to do their job. You can grant access to more items the user needs with a permission set.

**Roles**
Roles determine what users can see in Salesforce based on where they are located in the role hierarchy. Users at the top of the hierarchy can see all the data owned by users below them. Users at lower levels can't see data owned by users above them, or in other branches, unless sharing rules grant them access. Roles are optional but each user can have only one.
If you have an org with many users, you may find it easier to assign roles when adding users. However, you can set up a role hierarchy and assign roles to users at any time. Roles are only available in Professional, Enterprise, Unlimited, Performance, and Developer editions of Salesforce.

**the Lightning App Builder**

The Lightning App Builder is a point-and-click tool that makes it easy to create custom pages for the Salesforce mobile app and Lightning Experience, giving your users what they need all in one place.

But that’s not all. When you edit a Lightning app from the App Manager in Setup, you’re brought into the Lightning App Builder to manage the app’s settings. You can update the app’s branding, navigation, options, and manage the Lightning pages assigned to that app all in the Lightning App Builder.

**Lightning Components**
A Lightning component is a compact, configurable, and reusable element that you can add to a Lightning page in the Lightning App Builder.



