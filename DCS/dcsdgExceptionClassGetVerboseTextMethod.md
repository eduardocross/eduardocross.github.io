---
title: dgException.GetVerboseText Method

Id: dcsdgExceptionClassGetVerboseTextMethod
TocParent: dcsdgExceptionClassMethodsMain
TocOrder: 0

keywords: GetVerboseText method
keywords: dgException.GetVerboseText method
keywords: dgException, return a multi-line description of
keywords: how to, return a multi-line description of dgException

---

Returns a multi-line description of the <span>dgException</span>.
<pre>
        <span class="lang">[C#]</span>
 **public virtual new String GetVerboseText();** 
      </pre>
      <pre>
        <span class="lang">[Visual Basic] </span>
 **Public Overridable NotOveriddable Function GetVerboseText() As String** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc GetVerboseText Type(*String) Access(*Public) Modifier(*NotOverridable)** 
      </pre>

Remarks

For development and debugging purposes, <span> **GetVerboseText** </span> is an easy method to use to "dump" most of the available information associated with the <span>dgException</span>.
Examples

<pre class="prettyprint">        <span class="lang">
 **[C#]** 
        </span>
  /* Verbose text generates a large string which is a concatanation 
   * of several of dgException's properties and also shows the
   * stack trace. While not very user friendly, it can come in handy
   * developing a program. */
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read ;

  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* We retrieve the record for customer number 7800. */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");
  keyTbl.Row["CMCUSTNO"] = 7800;
  try
  {
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Write, keyTbl);
      myDS.ActiveRow["CMCUSTNO"] = 300;
      dbFile.ChangeCurrent(myDS);
  }
  catch(dgException dgEx)
  { /* Print out Verbose text to figure out why ReadRandomKey is
     * throwing an exception. */
      MessageBox.Show(dgEx.GetVerboseText(), "Datagate Exception");
  }

  dbFile.Close();
  db.Close();</pre>
      <pre class="prettyprint">        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Verbose text generates a large String which is a concatanation 
  ' of several of dgException's properties and also shows the
  ' stack trace. While not very user friendly, it can come in handy
  ' developing a program. 
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.Read Or AccessMode.Delete

  Dim myDS As AdgDataSet = Nothing
  dbFile.OpenNewAdgDataSet(myDS)

  ' We retrieve the record For customer number 7800. 
  Dim keyTbl As AdgKeyTable = myDS.NewKeyTable("RCMMASTL1")
  keyTbl.Row.Item("CMCUSTNO") = 7800
  Try
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Default, keyTbl)
      myDS.ActiveRow.Item("CMCUSTNO") = 300
      dbFile.ChangeCurrent(myDS)
  Catch dgEx As dgException
      ' Print out Verbose text to figure out why ReadRandomKey is
      ' throwing an exception. 
      MsgBox(dgEx.GetVerboseText(), MsgBoxStyle.Critical, "Datagate Exception")
  End Try

  dbFile.Close()
  db.Close()</pre>

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

