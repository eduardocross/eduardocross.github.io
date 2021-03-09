---
title: Public and Private Database Names

Id: dgPublicandPrivateDatabaseNames
TocParent: dgWorkingwithDatabaseNamesMain
TocOrder: 33

keywords: database names, public
keywords: database names, private
keywords: database names, public vs private

---

The currently-registered database names of the local computer are shown under Local Database Names in DataGate Explorer.

The database name information is maintained in the Local Settings for the Current_User. If another user logs on to the same Windows computer, the Database Name would be unknown to the new user (it is " **private** " to the first user). This can be circumvented by defining the database name as a " **public** " database.

You make a database name public by selecting the "*Public database name" checkbox in the database name dialog. A public database name can be referred to explicitly by prepending the string " ***Public/** ", as in "*public/my database name". Note however that a public database name is known implicitly to your applications as "my database name" without regard to the current user.

Since a public database name has no connection to the current user, a public database name is maintained in the Local Settings of the " **All Users** " area of the local computer.

Public database names are often used for web applications, or in other middle-tier applications where the user may be anonymous, have restricted capabilities, or is simply unknown to the application.

The database names that have been defined as public will display in DataGate Explorer as nodes with a special symbol (an uppercase "P") on their icon .

#### Section summary:

- <a href="dgWorkingwithDatabaseNamesMain.htm" target="Main">Working with Database Names</a>
- <a href="dgCreatingDatabaseNames.htm" target="Main">Creating Database Names</a>
- <a href="dgModifyingDatabaseNames.htm" target="Main">Modifying Database Names</a>
- <a href="dgPublicandPrivateDatabaseNames.htm" target="Main">Public and Private Database Names</a>
- <a href="dgChangingDatabaseNames.htm" target="Main">Renaming Database Name Indentifiers</a>
- <a href="dgDatabaseNameParameters.htm" target="Main">Database Name Parameters</a>
- <a href="dgAdvancedConnectionProperties.htm" target="Main">Advanced Connection Properties</a>

