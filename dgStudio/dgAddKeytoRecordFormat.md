---
title: Adding Keys to Record Formats

Id: dgAddKeytoRecordFormat
TocParent: dgCreatingaFileMain
TocOrder: 25

keywords: Adding a Key
keywords: Record Format, adding a key
keywords: Record formats
keywords: Keys

---

A key determines the order in which records will be retrieved from the file.

#### To Add a Key to a Record Format

1. Open the physical file definition source file in the Database File Definition Designer.
2. In the details tree view of the designer, select the record format node as shown
				below with the RCMMASTER record format.
3. Select the Keys tab in the lower right panel to display the keys grid as shown below.

![](../images/KeysGrid.bmp)
4. Scroll to the bottom of the keys grid, if necessary. Select the **New Row**  (the last
				row of the grid) by clicking on the leftmost column of the row.
5. Select the name of the key part to add by clicking on the drop-down box in the
				KeyName cell as shown below. Modify the remaining default column values of the
				New Row to reflect the attributes of the key part to be added to the record format.
				Note that a key part will not be added to the format until you select a field or make a
				change to the default data.
6. Click **Add**  to create the new file definition and add it to the project.

The new file definition is created in a file in the project folder. If the file definition is for a print file, the extension of the file is " **.apd** ". The extension for database file definitions is " **.dgdef** ". The file definition added to the project can now be opened for editing by double-clicking on the file in Solution Explorer.

You can change attributes of the key part by modifying the following column parameters.

#### Keyname:
Click on the arrow on the right of the key name cell and select one of the available fields to designate as a key field. A key name is required.

#### Key Order:
Click on the arrow on the right of the key order cell to select the order in which the key field will be sorted. The default is ascending order.

Ascending - Alphabetical order, from A to Z.

Descending - Alphabetical order, from Z to A.

#### Key Usage:
Select a usage by clicking the arrow on the right of key usage cell. The following are the available usage types.

- **Absolute Value –** Absolute value numeric sequence.
- **Signed –** Algebraic numeric sequence.
- **Unsigned –** Ignore the sign when sorting.
- **Digit –** The low nibble of each byte of the key field.
- **Zone –** A numeric type where there is a byte per digit, divided into a
				 	low andhigh nibble.

You can add a maximum of 32 key fields. The total LeftPad of the key can be up to 250 Bytes.

#### Inserting a New Key Part before an Existing Key Part

7. **Append**  the new key part as detailed above.
8. Select the **new key part row** , then click and drag the row to the key part row in the
					grid where you want to insert the new key part.
9. **Drop**  the new key part on top of the existing key part. The new key part is inserted
					before the existing key part.

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

