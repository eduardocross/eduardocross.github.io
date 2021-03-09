---
title: Create or Open a DataGate Project

Id: dgCreateOrOpenaProject
TocParent: dgCreatingaFileMain
TocOrder: 21

keywords: DataGate Studio
keywords: Opening a Project
keywords: Creating a Project
keywords: Datagate Project
keywords: Creating a Project
keywords: New DataGate Project
keywords: Starting a Project

---

To use file definition source files to create database and print files, you must organize them into a DataGate project. The project is a list of source files and database references that should represent the file creation design and implementation portion of a particular database development task.

Projects can be opened directly, or can be opened as members of a Visual Studio solution. In the latter case, you open the solution file to access the projects of the solution.

### Creating a New Datagate Project

1. Select **Project**  from the **File - New**  menu. The New Project dialog is displayed.
2. Select **DataGate**  from the list of available Project Types.

Depending on your installation options for DataGate Studio, you may have several Project Types listed in the New Project dialog. The DataGate project types are specific to DataGate tasks.
3. Select **DataGate File Definition Project**  from the installed templates list.
The DataGate File Definition Project may contain a sample database definition source file. You may use this as a starting point to begin your tasks, or simply delete the file and add your own.
4. Modify the name, location, and solution options, if desired, of the new project.

The Name field names the project file. This name will be shown next to a project node when the project is open in Solution Explorer, and is also the name of your project file. The project file has the ". **dgproj** " extension (e.g., "MyProject.dgproj).

The location of the project may be specified as a file path on the local computer. Click the browse button to navigate to a particular folder in which to add the project file.

By default, DataGate Studio will create a solution for your new project. You may add a new DataGate project to an existing solution by first opening the solution, then creating the project. On the New Project dialog, select " **Add to Solution** " from the Solution drop-down box instead of " **Create new Solution** ".

If you have installed a Source Control provider that is compatible with DataGate Studio, you may elect to add your project to a source repository by selecting the " **Add to Source Control** " checkbox.
5. Click **OK** . After creating the project, DataGate Studio will open the project (and its solution) in
				Solution Explorer.

### Opening an Existing DataGate Project

6. Select **Project/Solution**  from the **File - Open**  menu. The Open Project 
				dialog is displayed.
7. Navigate to the folder containing the DataGate project or its solution.

The Open Project dialog is a file browser for you to navigate among the project and solution files on your computer. By default, all solution files (extension ". **sln** " and project files are filtered). To filter only the DataGate project files (extension ". **dgproj** "), select **DataGate Project Files** from the "Objects of type" drop down box.
8. Select the project or solution.
9. Select **Add to Solution**  to add the project to the currently open solution, or select
				Close Solution to close the open solution before opening the project.

By default, the Open Project dialog closes any currently open solution before opening another project. Select **Add to Solution** as a way to add a selected project file to the currently open solution.
10. Click **OK**  to open the project, or **Cancel**  to close the dialog without opening a project.

### Creating a New, Empty Solution
There are two options for creating new solution files. By default, DataGate Studio creates a new solution when you create a new DataGate project (see To Create a New DataGate Project above). However, you may also create an empty solution file to which you can add existing or new project files.

#### To Create a New, Empty Solution

11. Select **Project**  from the **File - New**  menu. The New Project dialog is displayed.
12. Expand the " **Other Project Types** " node under Project Types. Select Visual Studio
						Solutions under Other Project Types.
13. Select **Blank Solution**  under installed templates.
14. Modify the name, location, and source control options of the new solution; if desired.
15. Click **OK**  to create the solution.

The new solution will be opened in Solution Explorer. Notice that it contains no projects. To add a project, you may create a new project or open an existing project as detailed above, making sure to use the " **Add to Solution** " options when doing so.

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

