---
title: dgException.ErrorClass Field

Id: dcsdgExceptionClassErrorClassField
TocParent: dcsdgExceptionClassFieldsMain
TocOrder: 1

keywords: ErrorClass field
keywords: dgException.ErrorClass field
keywords: dgErrorClass enumeration, used by
keywords: enumerations [DCS 16.0 dgErrorClass, used by
keywords: dgException, category
keywords: how to, determine dgException category

---

A category of the condition raising the exception.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public dgErrorClass ErrorClass { get; set }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Property ErrorClass As dgErrorClass** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp ErrorClass As dgErrorClass<br /> BegGet, BegSet** 
      </pre>

Field Value

[ASNA.DataGate.Common.dgErrorClass](dcsdgErrorClassEnumeration.html). The category of the condition raising the exception. 
Remarks

The condition raising the <span>dgException</span> belongs to a particular category of conditions identified by DCS. The <span> **ErrorClass** </span> field contains this category value.
Examples 

<pre class="prettyprint">        <span class="lang">
 **[C#]** 
        </span>
  /* This code attempts to open a file exclusively. 
   * If it fails, we print out the IBM i exception responsible.
   * "dbFile" is of type FileAdapter. */ 
  dbFile.AccessMode = AccessMode.Write;
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive;

  AdgDataSet dataSet = null;
  try
  {
      dbFile.Open(dataSet);
  }
  catch(dgException dgEx)
  {
      string msg;
      switch(dgEx.ErrorClass)
      {
          case dgErrorClass.dgEC_AS400CPF:
              msg = "CPF";
              break;
          case dgErrorClass.dgEC_AS400CPI:
              msg = "CPI";
              break;
          case dgErrorClass.dgEC_AS400DG8:
              msg = "DG8";
              break;
          case dgErrorClass.dgEC_AS400MCH:
              msg = "MCH";
              break;
          default:
              throw dgEx; /* Throw exception otherwise. */
      }
      /* Append the hexadecimal value of the SystemError to
       * form the classic name of the IBM i exception. */
      msg = msg + dgEx.SystemError.ToString("X");
      MessageBox.Show("iSeries threw exception " + msg + 
          " while opening file.", "iSeries exception.");
      /* Throw exception otherwise. */
      throw dgEx;
  }</pre>
      <pre class="prettyprint">        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' This code attempts to open a file exclusively. 
  ' If it fails, we print out the IBM i exception responsible.
  ' "dbFile" is of type FileAdapter. 
  dbFile.AccessMode = AccessMode.Write
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive

  Dim dataSet As AdgDataSet = Nothing
  Try
      dbFile.Open(DataSet)
  Catch dgEx As dgException
      Dim msg As String
      Select Case dgEx.ErrorClass
          Case dgErrorClass.dgEC_AS400CPF
              msg = "CPF"
          Case dgErrorClass.dgEC_AS400CPI
              msg = "CPI"
          Case dgErrorClass.dgEC_AS400DG8
              msg = "DG8"
          Case dgErrorClass.dgEC_AS400MCH
              msg = "MCH"
          Case Else
              Throw dgEx ' Throw exception otherwise. 
      End Select
      ' Append the hexaDecimal value of the SystemError to
      ' Form the classic name of the IBM i exception. 
      msg = msg + dgEx.SystemError.ToString("X")
      MsgBox("iSeries threw exception " &amp; msg &amp; _
          " While opening file.", MsgBoxStyle.Critical, "iSeries exception.")
      ' Throw exception otherwise. 
      Throw dgEx
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
      [dgErrorClass Enumeration](dcsdgErrorClassEnumeration.html) <br />[ASNA DataGate Common Namespace](dcsDataGateCommonNamespace.html)  

