---
title: Creating a Database File

Id: dgCreatingaFileMain
TocParent: Welcome
TocOrder: 20

keywords: creating a database file
keywords: file, creating database
keywords: database files
keywords: making new database files
keywords: new database files

---

Creating a database file requires a series of steps, outlined below and expanded on in the individual pages each step links to.

1. [Create or Open a DataGate Project](dgCreateOrOpenaProject.html)

DataGate file definitions are contained in DataGate projects. You may *create* a new project, or *open* a new project, using the DataGate Studio **File** menu. When you open or create a project, Solution Explorer displays the solution in the IDE, showing a DataGate project, or a collection of projects. Source files in DataGate projects are used to create database and print files.
2. [Add New Database File Definition](dgAddNewFileDefinition.html)

Creates a Database File Definition for a Physical, Simple, Join, Multiformat or Print file that contains the collection of information regarding the type of file being created, and how data in the file will be accessed and stored. The record format will also be created, along with a field key, Join definition and **Select/Omit** node (for Join and Multiformat files only).
3. [Open the Database File Definition Designer](dgOpenFDD.html)

The database file definition designers show editable file definition parameters in several easy to use display panels. Or if you prefer, you may edit file definition XML code in the XML editor.
4. [Add Field(s) to the Record Format](dgAddFieldtoRecordFormat.html)

Adds fields that make up a record format.
5. [Add Key(s) to the Record Format](dgAddKeytoRecordFormat.html)

Adds keys to the selected record format to determine the order and usage of how records will be retrieved from the file.
6. [Add Select/Omit Rule](dgAddSelectOmitRule.html)

For logical files only, adds Select/Omit Rules to define which records to Select and Omit.
7. [Create the Final File](dgCreatetheFinalFile.html)

Creates a new file and a member by using a database file definition in the DataGate project and creating the described file in the selected library in the desired database.
8. Add Member(s)

Adds members to a file in the database to store data in the format given by the database file definition. At least one member *must* be specified before a file can be used in a program.

#### Section summary:

- [Create or Open a DataGate Project](dgCreateOrOpenaProject.html)
- [Add New Database File Definition](dgAddNewFileDefinition.html)
- [Open the Database File Definition Designer](dgOpenFDD.html)
- [Add Field(s) to the Record Format](dgAddFieldtoRecordFormat.html)
- [Add Key(s) to the Record Format](dgAddKeytoRecordFormat.html)
- [Add Select/Omit Rule](dgAddSelectOmitRule.html)
- [Create the Final File](dgCreatetheFinalFile.html)
- [File Types, Data Type Keywords and Parameters](dgFileTypesandDataTypes.html)
- [The File Definition Document Editor](dgFileDefinitionDocumentEditor.html)

