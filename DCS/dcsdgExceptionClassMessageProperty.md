---
title: dgException.Message Property

Id: dcsdgExceptionClassMessageProperty
TocParent: dcsdgExceptionClassPropertiesMain
TocOrder: 0

keywords: Message property
keywords: dgException.Message property
keywords: string associated with dgException
keywords: dgException, string associated with dgException

---

String associated with the dgException. 
<pre>
        <span class="lang">[C#]</span>
 **public override string Message { get; }** 
      </pre>
      <pre>
        <span class="lang">[Visual Basic] </span>
 **Public Overrides ReadOnly Property Message As String** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Message Type(*String) Access(*Public) Modifier(*Overrides)
   BegGet** 
      </pre>

Property Value

String. Read-only. A canned message associated with the value of the [ Error](dcsdgExceptionClassErrorField.html) field. 
Remarks

Most values of the <span> **Message** </span> property have a unique standard message describing the particular condition raising the exception. Only when the value of [ Error](dcsdgExceptionClassErrorField.html) is dgEsAS400ERROR will <span> **Message** </span> return a string that is not a direct mapping of the **Error** identifier. In that case **Message** returns the value of the [ Text](dcsDisconnectingfromaDatabase.html) field.

The <span> **Message** </span> property overrides the property defined by <span> **System.Exception** </span>. This allows **dgException** to participate in standard conversions, such as provided by the <span> **ToString** </span> method of <span>System.Exception</span>.
Examples

<pre class="prettyprint">        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      /* This will show a somewhat specific message as to what 
       * went wrong opening the file. */
      MessageBox.Show(dgEx.Message, "Error opening file");
      //Exit procedure here.
  }
</pre>
      <pre class="prettyprint">        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.Read

  Dim myDS As AdgDataSet = Nothing
  Try
      dbFile.OpenNewAdgDataSet(myDS)
  Catch dgEx As dgException
      ' This will show a somewhat specIfic message as to what 
      ' went wrong opening the file. 
      MsgBox(dgEx.Message, MsgBoxStyle.Critical, "Error opening file")
      'Exit procedure here.
  End Try</pre>

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
      [Text Field](dcsDisconnectingfromaDatabase.html)

