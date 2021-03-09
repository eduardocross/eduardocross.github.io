---
title: dgException.SystemError Field

Id: dcsdgExceptionClassSystemErrorField
TocParent: dcsdgExceptionClassFieldsMain
TocOrder: 2

keywords: SystemError field
keywords: dgException.SystemError field
keywords: dgException, system-level classification

---

A system-level classification of the <span>dgException</span>. 
<pre><span class="lang">[C#]</span>
 **public int SystemError** 
      </pre>
      <pre><span class="lang">[Visual Basic] </span>
 **Public Property SystemError As Integer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **DclFld Name(SystemError) Type(*Integer) Access(*Public)** 
      </pre>

Field Value

Integer. A system-level exception condition identifier.
Remarks

**SystemError** is an integer code which may be returned by DataGate providers for certain conditions. Its use is provider dependent.

If the DataGate provider is an IBM i database, <span> **SystemError** </span> will contain useful information only if the value of [ ErrorClass](dcsdgExceptionClassErrorClassField.html) is one of the following:

- dgEC_AS400CPF
- dgEC_AS400MCH
- dgEC_AS400CPI
- dgEC_AS400DG8

In these cases, <span> **SystemError** </span> will contain an integer code associated with a system error. For example, if the <span>dgException</span> was raised due to the IBM i exception identified as "CPF501C", then <span> **ErrorClass** </span> will be set to dgEC_AS400CPF and <span> **SystemError** </span> will be set to 20508 (or 501C in hexadecimal). Also in these cases, [ Error](dcsdgExceptionClassErrorField.html) will be set to dgEsAS400ERROR.
Examples

<pre class="prettyprint">        <span class="lang">
 **[C#]** 
        </span>
  /* This code attempts to open a file exclusively. 
  * If it fails, we print out the IBM i exception responsible.
  * "dbFile" is of type FileAdapter. */ 
  dbFile.AccessMode = AccessMode.Write;
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive;
  dbFile.OpenAttributes.WaitForFile = 0;

  AdgDataSet dataSet = null;
  try
  {
      dbFile.Open(dataSet);
  }
  catch(dgException dgEx)
  {
      /* Take special action if error is due to the IBM i exception
       * "CPF1002". */
      if (dgEx.ErrorClass == dgErrorClass.dgEC_AS400CPF &amp;&amp;
          dgEx.SystemError.ToString("X") == "1002")
      {
          MessageBox.Show("iSeries threw exception CPF1002.");
          // Take alternative action here.
      }
      else
      {
          /* Throw exception otherwise. */
          throw dgEx;
      }
  }</pre>
      <pre class="prettyprint">        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' This code attempts to open a file exclusively. 
  ' If it fails, we print out the IBM i exception responsible.
  ' "dbFile" is of type FileAdapter. 
  dbFile.AccessMode = AccessMode.Write
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive
  dbFile.OpenAttributes.WaitForFile = 0

  Dim dataSet As AdgDataSet = Nothing
  Try
      dbFile.Open(DataSet)
  Catch dgEx As dgException
      ' Take special action If error is due to the IBM i exception
      ' "CPF1002". 
      If (dgEx.ErrorClass = dgErrorClass.dgEC_AS400CPF And _
          dgEx.SystemError.ToString("X") = "1002") Then
          MsgBox("iSeries threw exception CPF1002.")
          ' Take alternative action here.
      Else
          ' Throw exception otherwise.
          Throw dgEx
      End If
  End Try
</pre>

Requirements

**Namespace:** [ ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [dgException Class](dcsdgExceptionClass.html)
      <br />
      [dgException Members](dcsdgExceptionClassMembers.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)
      <br />
      [Error Field](dcsdgExceptionClassErrorField.html)
      <br />
      [ErrorClass Field](dcsdgExceptionClassErrorClassField.html)

