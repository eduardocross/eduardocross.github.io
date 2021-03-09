---
title: New / Changed Methods and Properties

Id: dcsWhatsNewMethodsandProperties

keywords: whats new [DCS 16.0 methods and properties
keywords: new [DCS 16.0 methods and properties
keywords: new methods and properties [DCS 16.0]

---

### Introduction
This document contains a list and brief description of the new methods and properties added to existing classes or changes to existing methods or properties.

###  Client Namespace 
[AdgConnection Class](dcsAdgConnectionClass.html) 

- The new [BeginTransaction(ASNA.DataGate.Common.TransactionLevel, 
							string, string)](dcsAdgConnectionClassBeginTransactionMethod4.html)  method begins manual transaction.  This new 
						overloaded method has parameters to establish the lock level, name, and 
						options for the transaction.  The existing [
							BeginTransaction methods](dcsAdgConnectionClassBeginTransactionMethodMain.html) have also been updated with additional 
						information.

<br />

[AdgDataSet Class](dcsAdgDataSetClass.html) 

- The new [AddRow(string)](dcsAdgDataSetClassAddRowMethod2.html) method 
						adds a prepared row to the table for a particular format.  This new 
						overloaded method has a string parameter containing the name of the format 
						corresponding to the table to which the prepared row will be added.
- The new [InsertRow](dcsAdgDataSetClassInsertRowMethods.html) method 
						inserts a record in the DataSet table for a particular format and relative 
						record position.  Depending upon the overloaded method used, you can 
						either use the integer zero-relative index of the format, or the string name of 
						the format, AND a positive integer value reflecting the position 
						of the record after insertion into the table.
- The new [NewKeyTable(integer)](dcsAdgDataSetClassInsertRowMethods.html) method 
						creates a key buffer for keyed access operations.  This new 
						overloaded method has a positive integer value containing the 
						zero-relative index of the format in the AdgDataSet.
- The new [SetActive(string, 
							integer)](dcsAdgDataSetClassSetActiveMethod2.html) method establishes the specified row as the active 
						row.  This new overloaded method has a string parameter to identify the 
						format corresponding to the DataTable in which the DataRow resides and a 
						positive integer value referring to the DataRow objects position within the row 
						collection of the DataTable.

<br />

[FileAdapter Class](dcsFileAdapterClass.html) 

- The new [ FormatRequested](dcsFileAdapterClassFormatRequestedProperty.html) property is used to determine the relationship between this dependent and its base (see [ DependentTypes](dcsDependentTypesEnumeration.html) enumeration).
- [ResetDevAttr](dcsFileAdapterClassResetDevAttrMethod.html) method has been flagged as obsolete, replaced by ResetPrintAttr.

<br />

###  [Providers Namespace](dcsDataGateProvidersNamespace.html) 
[SourceProfile Class](dcsSourceProfileClass.html) 

- The new [PasswordType](dcsSourceProfileClassPasswordTypeProperty.html) property is used to specify the authentication method for initiating database sessions with the [Password](dcsSourceProfileClassPasswordProperty.html) property.
- The [Register](dcsSourceProfileClassRegisterMethod.html) method has a new exception added.
- The SourceProfile constructors with string parameters have a new exception added:

1. [SourceProfile (string)](dcsSourceProfileClassSourceProfileConstructor2.html)
2. [SourceProfile (string, ASNA.DataGate.ProvidersSourceProfile)](dcsSourceProfileClassSourceProfileConstructor5.html)
3. [SourceProfile (string, bool)](dcsSourceProfileClassSourceProfileConstructor3.html)

<br />

See Also

<dl />
      [Client Namespace](dcsDataGateClientNamespace.html) <br />
      [Common Namespace](dcsDataGateCommonNamespace.html) <br />
      [What's New](dcsWhatsNewMain.html)<br />
      [New Classes](dcsWhatsNewClasses.html)<br />
      [New Delegates](dcsWhatsNewDelegates.html)<br />
      [New Enumerations](dcsWhatsNewEnumerations.html)

