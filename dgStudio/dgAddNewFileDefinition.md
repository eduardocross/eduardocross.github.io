---
title: Add Database File Definitions

Id: dgAddNewFileDefinition
TocParent: dgCreatingaFileMain
TocOrder: 22

keywords: Adding a File Definition
keywords: File Definitions
keywords: File Definitions, Adding
keywords: New File Definitions
keywords: Database File Definitions

---

DataGate projects are composed of file definition source files. These may be used to design and create database and print files. To do so you must add file definition source files to your project. You may add new file definitions based on DataGate project templates, or you may add existing file definitions source files. You can also import the definitions of existing database files via **DataGate Explorer.** 

#### To Add a New File Definition

1. [Create or Open a DataGate project/solution](dgCreateOrOpenaProject.html)
2. In Solution Explorer, select the **project**  in which the new file definition will be added.

Note that if the solution is composed of only one project, Solution Explorer may only show that project node, and no solution node. If more than one project exists in the solution, the project nodes will be shown under the root solution node.
3. Select **Add New Item**  from the Project menu. The Add New Item dialog is displayed.

The **Add New Item** command is shown on the **Project** menu only when a project is selected in Solution Explorer. If you don't see the command, make sure you have a project or solution open in Solution Explorer, and that the correct project is selected.
4. Select the new **file definition template**  corresponding to the file definition type to
				be added to the project (see File Types).

DataGate items will only be shown if the **Add New Item** command is executed while a DataGate project is selected in Solution Explorer. If you don't see the DataGate category in the Add New Item dialog, Cancel the dialog and make sure you have selected a DataGate project in Solution Explorer.
5. Modify the **source file name** , if desired.

The source file name is simply the name of the source file containing the file definition. This name does not correspond to any particular database object, and will not be used as the name of the created file (unless that is desired). Use a descriptive name that will reflect the usage of the file definition in the development project.
6. Click **Add**  to create the new file definition and add it to the project.

The new file definition is created in a file in the project folder. If the file definition is for a print file, the extension of the file is " **.apd** ". The extension for database file definitions is " **.dgdef** ". The file definition added to the project can now be opened for editing by double-clicking on the file in Solution Explorer.

#### To Add an Existing File Definition

7. [Create or Open a DataGate project/solution](dgCreateOrOpenaProject.html)
8. In Solution Explorer, select the **project**  into which the 
			existing file definition will be added.

Note that if the solution is composed of only one project, Solution Explorer may only show that project node, and no solution node. If more than one project exists in the solution, the project nodes will be shown under the root solution node.
9. Select **Add Existing Item**  from the Project menu. The Add 
			Existing Item dialog is displayed.

There are two types of DataGate file definition source files. Print file definitions have the extension ". **apd** ". Database file definitions have the extension ". **dgdef** ". DataGate Studio recognizes these extensions and handles commands on these file types appropriately. You may add either type of file definition source file to your project.
10. Navigate to the **file definition source**  file to be added to the project, and select it.
11. Click **OK**  to add the file definition to the project, or **Cancel**  to close the dialog without
				adding a file.

### Importing a Database File Definition
A common task is to modify or create a new file based on the definition of an existing database file. DataGate Explorer makes it easy to import file definitions into your DataGate project using either context menus or a drag and drop techniquw

#### To Import a Database File Definition

12. [Create or Open a DataGate project/solution](dgCreateOrOpenaProject.html)
13. Open DataGate Explorer, and connect to the database containing the file to import.
				Navigate to the file in DataGate Explorer.				

You may need to first add a database name and connection to connect to the database containing the file.
14. Right-click on the file, and select **Copy Filedef Source To Project.** 

The **Copy Filedef Source To Project** command is only one way to import a file definition from a database. A "drag and drop" shortcut is described below.
15. If the solution consists of more than one DataGate project, the Project Chooser
				dialog will appear. Select the target project for the import operation, and click **OK** ,
				or click Cancel to abort the import. 

Note that if the solution contains only one DataGate project, the file definition is imported directly into that project without the Project Chooser dialog.
16. A file definition source file is added to your project with a name corresponding to the
				name of the database file it was imported from.

#### To Import a Database File Definition (Drag and Drop)

17. [Create or Open a DataGate project/solution](dgCreateOrOpenaProject.html)
18. Open DataGate Explorer, and connect to the database containing the file to import.
				Navigate to the file in DataGate Explorer.				

You may need to first add a database name and connection to connect to the database containing the file.
19. Click on the file in DataGate Explorer, and drag it to the Solution Explorer Window.
20. Drop the file onto the DataGate project node into which the file definition should be
				imported.
21. A file definition source file is added to your project with a name corresponding to the
				name of the database file it was imported from.

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

