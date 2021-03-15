---
title: IFileObject Methods

Id: dcsIFileObjectMethods
TocParent: dcsIFileObjectClass
TocOrder: 1

keywords: methods [DCS 16.0 IFileObject class
keywords: IFileObject class, methods

---

Public Methods

<br />

<table class="dtTABLE" id="table3" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [Copy](dcsIFileObjectClassCopyMethod.html)
</td>
            <td colspan="1" rowspan="1">

**Copy** creates a copy of the database file represented by **IFileObject** with the name and location specified.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [GetAdgDataSet](dcsIFileObjectClassGetAdgDataSetMethod.html)
</td>
            <td colspan="1" rowspan="1">

**GetAdgDataSet** method returns an instance of [ AdgDataSet](dcsAdgDataSetClass.html) modeling the formats of the database file represented by **IFileObject** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ReadCreationAttributes](dcsIFileObjectClassReadCreationAttributesMethod.html)
</td>
            <td colspan="1" rowspan="1">

**ReadCreationAttributes** reads and validates an XML document fragment describing a database file's creation-time attributes.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ReadDefinition](dcsIFileObjectClassReadDefinitionMethod.html)
</td>
            <td colspan="1" rowspan="1">

**ReadDefinition** reads and validates an XML document fragment describing a database file's definition.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [RepairFile](dcsIFileObjectClassRepairFileMethod.html)
</td>
            <td colspan="1" rowspan="1">

**RepairFile** repairs the database file represented by **IFileObject** , as specified by [RepairOptions](dcsRepairOptionsEnumeration.html).
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [WriteCreationAttributes](dcsIFileObjectClassWriteCreationAttributesMethod.html)
</td>
            <td colspan="1" rowspan="1">

**WriteCreationAttributes** dumps a database file's creation-time attributes to an XML content node.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [WriteDefinition](dcsIFileObjectClassWriteDefinitionMethod.html)
</td>
            <td colspan="1" rowspan="1">

**WriteDefinition** dumps a database file's definition to an XML content node.
</td>
          </tr>
</table>

See Also

<dl />
      [IFileObject Class](dcsIFileObjectClass.html)
      <br />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [RepairOptions Enumeration](dcsRepairOptionsEnumeration.html)

