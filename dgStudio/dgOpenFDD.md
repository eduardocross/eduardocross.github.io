---
title: File Definition Designers

Id: dgOpenFDD
TocParent: dgCreatingaFileMain
TocOrder: 23

keywords: File Definition Designers
keywords: File Definitions

keywords: Database File Definition Designer
keywords: Designer Layout

---

The file definition designers in DataGate Studio allow you to quickly find, view, and edit file definition features. DataGate Studio provides two designers: the Print File Designer and the Database File Designer. Each designer operates as a standard document window in the IDE.

The "code behind" for these designers is an XML document, which you may also edit directly using the DataGate Studio XML editor. The XML schema for file definition documents is installed with DataGate Studio, so the XML editor features schema validation checking and IntelliSense® support.

### Database File Definition Designer Overview
The Database File Definition Designer is DataGate Studio's graphical user interface for simplifying the development of DataGate database files. It presents database file definitions in a set of organized property groups, allowing you to quickly drill down to focus on each of the main functional areas of the file. The Database File Definition Designer is invoked by opening a database file definition source file (extension ".dgdef") in a DataGate project.

The designer is strictly for editing file definition source files. When you make changes in the designer, you are changing a file definition source file in your DataGate project, not a DataGate database file. You cannot directly create or modify database files in the File Definition Designer. After designing a file definition, you save changes to the source file in the DataGate project, which can then be used with a separate project command to create a database file.

### Designer Layout
![" align="middle](../images/FDDlayout.bmp)		

The primary layout of the designer features a tree view on the left, and details panel on the right. The tree view displays a high-level view of the file definition. The root node represents the file type (physical, simple logical, multiformat, join, or SQL logical) and the file-level attributes of the definition. Under the root node, you will see nodes representing major functional components of the file. In the case of the physical file definition shown above, three tree nodes are displayed under the root node, representing the field reference file, record format, and file creation attributes.

The details pane on the right side of the designer displays the set of attributes associated with the tree node selected in the left pane. In the example above, the filelevel attributes of the physical file (text and duplicate key processing), are shown in an editable form. Selecting other nodes in the tree results in an update of the details pane, to show the attributes associated with the node.

### Modifying the File Definiton
To make changes to a file definition, simply click an editable control in the details pane and make selections, or enter text. After you do so, notice that the editor places an asterisk at the end of the source file name in the document window tab, at the top of the designer.

The asterisk indicates that un-saved changes have been made to the file definition. You should save your changes often using one of the DataGate Studio Save commands on the **File** menu. When you successfully save your changes, the editor removes the asterisk from the tab, indicating that all changes are saved.

The Database File Designer also supports the Undo and Redo commands. Thus if you change your mind about one or more changes, simply invoke the **Undo** command on the **Edit** menu (or Ctrl-z) for each change you wish to reverse. Note that you can Undo or Redo changes even after you save them to the source file. Thus, the un-saved changes asterisk may disappear and reappear as you invoke Undo and Redo.

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

