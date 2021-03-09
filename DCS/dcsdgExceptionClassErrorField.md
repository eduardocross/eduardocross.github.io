---
title: dgException.Error Field

Id: dcsdgExceptionClassErrorField
TocParent: dcsdgExceptionClassFieldsMain
TocOrder: 0

keywords: Error field
keywords: dgException.Error field
keywords: dgErrorNumber enumeration, used by
keywords: enumerations [DCS 16.0 dgErrorNumber, used by
keywords: dgException, error field
keywords: how to, determine dgException error

---

The condition identifier for this dgException.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public dgErrorNumber Error}** 
      </pre>
		  <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Property Error As dgErrorNumber** 
      </pre>
		  <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **DclFld Name(Error) Type(dgErrorNumber)** 
      </pre>

				  Field Value

[ASNA.DataGate.Common.dgErrorNumber](dcsdgErrorNumberEnumeration.html). The condition identifier for the exception.
Remarks

DCS sets the **Error** field to identify the condition giving rise to the dgException. The **Error** field uniquely identifies the condition, as detected by DCS and the DataGate provider. However, further details of the exception may be gleaned from other fields, such as [SystemError](dcsdgExceptionClassSystemErrorField.html) and [Text](dcsDisconnectingfromaDatabase.html), dependent upon provider support.
Examples

<pre class="prettyprint">        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMMASTERL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      /* There are many reasons why opening a file can fail. Here, we
       * catch some of the more general ones. */
      if (dgEx.Error == dgErrorNumber.dgEmMNOTFND)
          MessageBox.Show("Member " + dbFile.MemberName + " not found!", "Error opening file");
      else if (dgEx.Error == dgErrorNumber.dgEmFNOTFND)
          MessageBox.Show("File " + dbFile.FileName + " not found!", "Error opening file");
      else
          MessageBox.Show(dgEx.Message, "Error opening file");
          //Exit procedure here.
  }

  /* Do some action here. */

  dbFile.Close();
  db.Close();</pre>
					  <pre class="prettyprint">        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMMASTERL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.Read

  Dim myDS As AdgDataSet = Nothing
  Try
      dbFile.OpenNewAdgDataSet(myDS)
  Catch dgEx As dgException
      ' There are many reasons why opening a file can fail. Here, we
      ' catch some of the more general ones. 
      If (dgEx.Error = dgErrorNumber.dgEmMNOTFND) Then
         MsgBox("Member " &amp; dbFile.MemberName &amp; " not found.", MsgBoxStyle.Critical, "Error opening file")
      ElseIf (dgEx.Error = dgErrorNumber.dgEmFNOTFND) Then
         MsgBox("File " &amp; dbFile.FileName &amp; " not found.", MsgBoxStyle.Critical, "Error opening file")
      Else
         MsgBox(dgEx.Message, MsgBoxStyle.Critical, "Error opening file")
         'Exit procedure here.
      End If
  End Try
  ' Do some action here. 

  dbFile.Close()
  db.Close()
</pre>

							  Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
								  [dgException Class](dcsdgExceptionClass.html)
								  <br />
								  [dgException Members](dcsdgExceptionClassMembers.html)
								  <br />
								  [dgErrorNumber Enumeration](dcsdgErrorNumberEnumeration.html)
								  <br />
								  [ASNA DataGate Common Namespace](dcsDataGateCommonNamespace.html)

