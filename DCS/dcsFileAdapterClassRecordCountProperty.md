---
title: FileAdapter.RecordCount Property

Id: dcsFileAdapterClassRecordCountProperty
TocParent: dcsFileAdapterProperties
TocOrder: 10

keywords: FileAdapter.RecordCount property
keywords: RecordCount property
keywords: how to, determine the number of non-deleted records in database file
keywords: records, number of non-deleted in database file
keywords: number of, non-deleted records in database file
keywords: database files, number of non-deleted records in

---

<span>The number of non-deleted records in the open database file. </span> 
<pre>        <span class="lang">[C#]</span>
 **Public long RecordCount { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property RecordCount As Long** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp RecordCount Type(*Integer) Len(8) Access(*Public)
   BegGet** 
      </pre>

Property Value

Integer. Read-only. Returns a long integer containing the count of records in a member.
Remarks

Use the <span> **RecordCount** </span> property to examine the total number of records contained in the member. 
Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;

  int refreshInterval = 10; //Used so we don't slow down refreshing too much...
  dbFile.OpenAttributes.BlockingFactor = refreshInterval;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* Here, we read every record until end of file is reached.
   * Because this is an fairly long process, we set up a progress bar
   * to keep the user from being discouraged. We set its Maximum
   * value to the number of records in the file, which is found
   * using FileAdapter's RecordCount propert, divided by
   * our refreshInterval. */
  int recordsReadSinceLastRefresh = 0;
  prgBar.Minimum = 0;
  prgBar.Maximum = Convert.ToInt32(dbFile.RecordCount) / refreshInterval;

  bool EOF = false;
  while(!EOF)
  {
      try
      {
          /* Though it seems like we have to read each record one at a time,
           * in reality DCS stores the first 10 records the first time we read
           * and then afterwards we simply read from the cache. When those run out, 
           * DCS will automatically grab another ten records from the database.
           * Note that 10 is our refresh interval, meaning that this I/O operation
           * occurs at the same time that we update our progress bar. If the blocking
           * factor was higher than our refresh interval, not only would we have to 
           * wait longer to read the first record but the progress bar would go longer
           * without being updated. */
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait);
          /* Perform some action on each record here... */
          recordsReadSinceLastRefresh ++;
          if (recordsReadSinceLastRefresh == refreshInterval)
          {
              recordsReadSinceLastRefresh = 0;
              prgBar.PerformStep();
              this.Refresh(); //Refreshes the form.
          }
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
          {
              //Exit procedure or end application here.
          }
      }
  }
  dbFile.Close();
  db.Close();</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.Read
  Dim myDS As AdgDataSet = Nothing

  'Used so we don't slow down reshing too much...
  Dim reshInterval As Integer = 10
  dbFile.OpenAttributes.BlockingFactor = reshInterval
  dbFile.OpenNewAdgDataSet(myDS)

  ' Here, we read every record until end of file is reached.
  ' Because this is an fairly long process, we set up a progress bar
  ' to keep the user from being discouraged. We set its Maximum
  ' value to the number of records in the file, which is found
  ' using FileAdapter's RecordCount property, divided by
  ' our reshInterval. 
  Dim recordsReadSinceLastresh As Integer = 0
  prgBar.Minimum = 0
  prgBar.Maximum = Convert.ToInt32(dbFile.RecordCount) / reshInterval

  Dim EOF As Boolean = False
  While Not EOF
      Try
          ' Though it seems like we have to read each record one at a time,
          ' in reality DCS stores the first 10 records the first time we read
          ' and then afterwards we simply read from the cache. When those run out, 
          ' DCS will automatically grab another ten records from the database.
          ' Note that 10 is our resh interval, meaning that this I/O operation
          ' occurs at the same time that we update our progress bar. If the blocking
          ' factor was higher than our resh interval, not only would we have to 
          ' wait longer to read the first record but the progress bar would go longer
          ' withbeing updated. 
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait)
          ' Perform some action on each record here... 
          recordsReadSinceLastresh = recordsReadSinceLastresh + 1
          If recordsReadSinceLastresh = reshInterval Then
              recordsReadSinceLastresh = 0
              prgBar.PerformStep()
              Me.Refresh() 'reshes the form.
          End If
      Catch dgEx As dgException
          If dgEx.Error = dgErrorNumber.dgEaEOF Then
              EOF = True
          Else
              'Exit procedure or end application here.
          End If
      End Try
  End While
  dbFile.Close()
  db.Close()</pre>

Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Members](dcsFileAdapterMembers.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)  

