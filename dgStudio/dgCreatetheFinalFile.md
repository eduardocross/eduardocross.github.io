---
title: Creating the Finished File

Id: dgCreatetheFinalFile
TocParent: dgCreatingaFileMain
TocOrder: 27

keywords: creating a file
keywords: Final database file
keywords: creating new database file

---

** *Before you create a file, ensure that the database file definition, record format, fields, keys, and Select/Omit Rules are exactly as you want them. Use the Database File Definition Designer, Print File Definition Designer, or XML editor to create the file definition. Once a file is created, you cannot make any changes to its definitions.* ** 

#### To Create a File

1. **Open**  or create the DataGate project in Solution Explorer containing the file
			definition source file from which you will create the database or print file.
2. After editing the file definition in Database File Definition Designer, Print File
			Definition Designer, or the XML editor, **save**  your changes.
3. Select the **file definition source file**  from the DataGate project in Solution
			Explorer.
4. **Right-click**  on the file node, and select **Create File**  from the context menu. The
			Create DataGate File dialog will display.
5. On the **Location**  tab, as shown above, enter the name of the new file, the library it
			should reside in, the database connection to use, and text comments to associate
			with the created file.
6. The following attributes can be set on the Location tab.

#### File Name:
The name of the selected database file definition source file node will display by default. You can however, change the name of the file to create. Note that some databases, notably the iSeries, restrict file name LeftPad.

#### Text:
By default, no text comments are displayed. If you want to associate a comment with the created file object, you can enter it at this time.
7. On the **Member**  tab, you may specify a member name. If a
			member name is specified, a member object will be added to the file with that name,
			upon successful creation of the file. You may also indicate text comments to
			associate with the member, and, for logical members, the base member(s) of the
			logical member.

#### Name:
*FILE will display as the default member. *FILE is a keyword indicating that the member name should be the same as the file name. You can change the default member name, or leave the Name field blank to indicate that no member should be added to the created file. A file must contain at least one member to be used in a program.

#### Base Members:
If the file definition defines a logical file, and the base file in the format is verified on the target database, you may select one or more of the members of the base file as base members for the logical member. Place a check next to each member which is to be a base member for the logical member added.

#### Text:
Enter a text description of the contents the member will contain.
8. Click **OK**  to begin creating the file, or **Cancel**  to close the dialog without creating a
			file. Observe progress and any errors produced by the command in the DataGate
			Studio Output and Error List windows.

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

