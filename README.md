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
