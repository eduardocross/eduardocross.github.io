<keyword name="Microsoft.Help.Keywords" content="whats new [DCS 16.0 delegates">---
title: New / Changed Enumerations

Id: dcsWhatsNewEnumerations

keywords: whats new [DCS 16.0 enumerations
keywords: new [DCS 16.0 enumerations
keywords: new enumerations [DCS 16.0]

---

### Introduction
This document contains a list and brief description of the **new and updated** enumerations. 
<br />

### CLIENT NAMESPACE
<br />

<table class="dtTABLE" id="table2" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
            <colgroup span="1">
              <col span="1" style="WIDTH: 20%" />
              <col span="1" style="WIDTH: 70%" />
            </colgroup>
            <tr>
              <td colspan="1" rowspan="1">

[InitMemberOptions](dcsInitMemberOptionsEnumeration.html) 
</td>
              <td colspan="1" rowspan="1">

Enumerated constant indicating how a member of a database will be initialized.
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

[LiblPosition](dcsLiblPositionEnumeration.html) 
</td>
              <td colspan="1" rowspan="1">

Enumerated constant indicating the values used by [ ILibraryList.AddEntry](dcsILibraryListClassAddEntryMethod.html) to specify the location in the library list to add the new entry.
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

[XmlInfoEventType](dcsXmlInfoEventTypeEnumeration.html) 
</td>
              <td colspan="1" rowspan="1">

Enumerated constant indicating the level of information to be provided when reading and writing XML files with events.
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1" style="height: 47px">

[XmlOptions](dcsXmlOptionsEnumeration.html) 
</td>
              <td colspan="1" rowspan="1" style="height: 47px">

Enumerated constant indicating the options when reading and writing Xml database objects.
</td>
            </tr>
</table>

<br />

### COMMON NAMESPACE
<br />

<table class="dtTABLE" id="Table3" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
            <colgroup span="1">
              <col span="1" style="WIDTH: 20%" />
              <col span="1" style="WIDTH: 70%" />
            </colgroup>
            <tr>
              <td colspan="1" rowspan="1">
                [AdgObjectTypes](dcsAdgObjectTypesEnumeration.html)
              </td>
              <td colspan="1" rowspan="1">
							Defines values for the [AdgObjectType](dcsIAdgObjectClassAdgObjectTypeProperty.html)
							property of an object.
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1" style="height: 23px">
                [AdgSubTypes](dcsAdgSubTypesEnumeration.html)
              </td>
              <td colspan="1" rowspan="1" style="height: 23px">
							Defines values for the [AdgSubType](dcsIAdgObjectClassAdgSubTypeProperty.html)
							property of an object. 
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">
                [AuthorityTypes](dcsDbcsFormatEnumeration.html)
              </td>
              <td colspan="1" rowspan="1">
							Defines values that specify the types of authority a user has a right to when 
							working on objects.
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">
                [DependentTypes](dcsDependentTypesEnumeration.html)
              </td>
              <td colspan="1" rowspan="1">
							Defines values that indicate the relationship between two objects.
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">
                [DuplicateOptions](dcsDuplicateOptionsEnumeration.html)
              </td>
              <td colspan="1" rowspan="1">
							Defines values on how a database file will be duplicated.
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">
                [InspectFileOutput](dcsInspectFileOutputEnumeration.html)
              </td>
              <td colspan="1" rowspan="1">
							Defines values that are used to indicate the parts of a output file 
							that will be inspected.
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">
                [InspectFileParts](dcsInspectFilePartsEnumeration.html)
              </td>
              <td colspan="1" rowspan="1">
							Defines values that are used to indicate the parts of a file 
							that will be inspected.
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

[KeyUsages](dcsKeyUsagesEnumeration.html) 
</td>
              <td colspan="1" rowspan="1">

Defines key definition properties which apply to a key field.
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">
                [PaperOrientation](dcsPaperOrientationEnumeration.html)
              </td>
              <td colspan="1" rowspan="1">
							Defines values on the orientation of the paper.
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">PaperSize
						</td>
              <td colspan="1" rowspan="1">
							Replaced with
							System.Drawing.Printing.PaperKind 
      Enumeration
							to define values for the type of the paper. 
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">PaperSource
						</td>
              <td colspan="1" rowspan="1">Replaced with
							System.Drawing.Printing.PaperSourceKind 
Enumeration
							to define values on the printer tray that will be used.
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">
                [PasswordType](dcsPasswordTypeEnumeration.html)
              </td>
              <td colspan="1" rowspan="1">
							Defines values for the type of password for the user.
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">PrintDuplex
						</td>
              <td colspan="1" rowspan="1">
							Replaced with 
							System.Drawing.Printing.Duplex 
      Enumeration
							to define values for duplex (double-sided) printing.
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">PrintQuality
						</td>
              <td colspan="1" rowspan="1">
							Replaced with 
							System.Drawing.Printing.PrinterResolutionKind 
      Enumeration to define values for the print quality.
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">
                [PrintTrueType](dcsPrintTrueTypeEnumeration.html)
              </td>
              <td colspan="1" rowspan="1">
							Defines values whether the True Type font will be used.
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">
                [RepairOptions](dcsRepairOptionsEnumeration.html)
              </td>
              <td colspan="1" rowspan="1">
							Defines values that indicate how data will be repaired.
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">
                [ShareTypes](dcsShareTypesEnumeration.html) Updated </td>
              <td colspan="1" rowspan="1">
							Defines modes on how a file will be shared.
						</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">
                [TransactionLevel](dcsTransactionLevelEnumeration.html) Updated </td>
              <td colspan="1" rowspan="1">Defines values for the [TransactionLevel
							](dcsIAdgTransactionClassTransactionLevelProperty.html)property of [IAdgTransaction](dcsIAdgTransactionClass.html).</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">
                [WaitOptions](dcsWaitOptionsEnumeration.html) Updated </td>
              <td colspan="1" rowspan="1">
							Defines modes describing the behavior of the Lock method when the requested 
							lock is not immediately available.
						</td>
            </tr>
</table>

See Also

<dl />
        [Client Enumerations](dcsDataGateClientEnumerations.html)
        <br />
        [Common Enumerations](dcsDataGateCommonEnumerations.html)
        <br />
        [AdgObjectType Property](dcsIAdgObjectClassAdgObjectTypeProperty.html)
        <br />
        [AdgSubType Property](dcsIAdgObjectClassAdgSubTypeProperty.html)
        <br />
        [IAdgTransaction Class](dcsIAdgTransactionClass.html)
        <br />
        [TransactionLevel 
					Property](dcsIAdgTransactionClassTransactionLevelProperty.html)
        <br />
        [ILibraryList.AddEntry](dcsILibraryListClassAddEntryMethod.html)

</keyword>
