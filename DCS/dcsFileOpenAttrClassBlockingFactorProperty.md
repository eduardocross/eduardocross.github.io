---
title: FileOpenAttr.BlockingFactor Property

Id: dcsFileOpenAttrClassBlockingFactorProperty
TocParent: dcsFileOpenAttrProperties
TocOrder: 0

keywords: BlockingFactor property
keywords: FileOpenAttr.BlockingFactor property
keywords: network blocking factor
keywords: network blocking factor, number of records specified
keywords: how to, network blocking factor established
keywords: database files, network blocking factor specified
keywords: files, network blocking factor specified

---

Specify network blocking feature in the open file.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **Public int BlockingFactor { get; set; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Property BlockingFactor As Integer**  </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp BlockingFactor Type(*Integer) Len(4) Access(*Public)
   BegGet, BegSet** 
      </pre>

Property Value

Integer. A number (greater than zero) of records to block, or the special value, [OptimalBlockingFactor](dcsFileOpenAttrClassOptimalBlockingFactorField.html).
Remarks

Set this property to a number of records (greater than zero) to engage "network blocking" features of DataGate. Network blocking dramatically improves the performance of access operations by caching sets of records on the client side of DataGate’s client/server link. With network blocking, DataGate is able to compress certain operations, such as reading a large set of sequential records, into just a few client/server calls.

This property may be set to any positive number of records. When used this way, DataGate will create an in-memory record buffer to contain exactly the number of records specified.

Two special values are recognized for the **BlockingFactor** property. **OptimalBlockingFactor** tells DataGate to calculate the best-fit size of the record buffer, using factors such as record length and network packet size. In most cases, **OptimalBlockingFactor** will yield the best network blocking performance. [ OmitBlocking](dcsFileOpenAttrClassOmitBlockingField.html) is the default value of **BlockingFactor** , signifying that all record blocking features will be omitted.
Examples

<pre>        <span class="lang">
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
    * using FileAdapter's RecordCount property, divided by
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
  db.Close()</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.Read
  Dim myDS As AdgDataSet = Nothing

  Dim refreshInterval As Integer = 10 'Used so we don't slow down refreshing too much...
  dbFile.OpenAttributes.BlockingFactor = refreshInterval
  dbFile.OpenNewAdgDataSet(myDS)

  ' Here, we read every record until end of file is reached.
  ' Because this is an fairly long process, we set up a progress bar
  ' to keep the user from being discouraged. We set its Maximum
  ' value to the number of records in the file, which is found
  ' using FileAdapter's RecordCount property, divided by
  ' our refreshInterval. 
  Dim recordsReadSinceLastRefresh As Integer = 0
  prgBar.Minimum = 0
  prgBar.Maximum = Convert.ToInt32(dbFile.RecordCount) / refreshInterval

  Dim EOF As Boolean = False
  While Not EOF
      Try
          ' Though it seems like we have to read each record one at a time,
          ' in reality DCS stores the first 10 records the first time we read
          ' and then afterwards we simply read from the cache. When those run out, 
          ' DCS will automatically grab another ten records from the database.
          ' Note that 10 is our refresh interval, meaning that this I/O operation
          ' occurs at the same time that we update our progress bar. If the blocking
          ' factor was higher than our refresh interval, not only would we have to 
          ' wait longer to read the first record but the progress bar would go longer
          ' without being updated. 
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait)
          ' PerForm some action on each record here... 
          recordsReadSinceLastRefresh = recordsReadSinceLastRefresh + 1
          If recordsReadSinceLastRefresh = refreshInterval Then
              recordsReadSinceLastRefresh = 0
              prgBar.PerFormStep()
              Me.Refresh() 'Refreshes the Form.
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
  db.Close()Requirements</pre>

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileOpenAttr Class](dcsFileOpenAttrClass.html)
      <br />
      [FileOpenAttr Class Members](dcsFileOpenAttrClassMembers.html)
      <br />
      [OmitBlocking Field](dcsFileOpenAttrClassOmitBlockingField.html)
      <br />
      [OptimalBlockingFactor 
					Field](dcsFileOpenAttrClassOptimalBlockingFactorField.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

