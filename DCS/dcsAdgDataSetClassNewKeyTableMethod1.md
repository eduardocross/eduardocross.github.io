---
title: AdgDataSet.NewKeyTable(string)

Id: dcsAdgDataSetClassNewKeyTableMethod1
TocParent: dcsAdgDataSetClassNewKeyTableMethods
TocOrder: 0

---

Create a key buffer for keyed access operations for the specified format string.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public [AdgKeyTable](dcsAdgKeyTableClass.html) NewKeyTable(
   string strFormat
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function NewKeyTable(
   ByVal strFormat As String
) As [AdgKeyTable](dcsAdgKeyTableClass.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc NewKeyTable Access(*Public) Type([AdgKeyTable](dcsAdgKeyTableClass.html))
   DclSrParm strFormat Type(*String)** 
      </pre>

Parameters

<dl>
        <dt>
 *strFormat* 
        </dt>
        <dd>A string naming a format in the **AdgDataSet** .</dd>
</dl>

Exceptions

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <th colspan="1" rowspan="1">
							Value of dgException.Error
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NullReferenceException
</td>
            <td colspan="1" rowspan="1">

Can occur if *strFormat* specifies an invalid format name.
</td>
          </tr>
</table>

Remarks

[FileAdapter](dcsFileAdapterClass.html) provides methods for accessing a file by key value using [AdgKeyTable](dcsAdgKeyTableClass.html). **AdgKeyTable** is a class for manipulating a DataTable which represents a DataGate file key. **NewKeyTable** generates an instance of **AdgKeyTable** corresponding to a key in a particular file format. Generally, this is the way application programs create key buffers for use in **FileAdapter** keyed access methods.
Examples

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span></pre>
      <pre class="prettyprint">  /* This example will open a file and find the record for
     the customer "Thilmany of Bread Co Resources".
     It omits error trapping for clearity's sake. */

  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  db.Open();
  FileAdapter file = new FileAdapter(db);
  file.FileName = "Examples//CMastNewL2";
  AdgDataSet dataSet;
  file.OpenNewAdgDataSet( out dataSet );

  //This next line creates a key based on record format RCMMastL2
  AdgKeyTable key = dataSet.NewKeyTable("RCMMastL2");

  //We specifiy KeyPartCount to avoid specifiying the second
  //key field.
  //We then set the keyfield "CMName" to our search argument.
  key.KeyPartCount = 1;
  key.Row["CMName"] = "Thilmany Of Bread Co Resources";

  //The following read will find the record associated with the 
  //customer name "Thilmany Of Bread Co Resources" and store it
  //in dataSet.
  file.ReadRandomKey(dataSet, ReadRandomMode.Equal, LockRequest.Default, key);</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
</pre>
      <pre class="prettyprint">  ' This example will open a file and find the record for
  ' the customer "Thilmany of Bread Co Resources".
  ' It omits error trapping for clearity's sake.
  Dim db As New AdgConnection("*Public/DG NET Local")
  db.Open()
  Dim file As New FileAdapter(db)
  file.FileName = "Examples//CMastNewL2"
  Dim dataSet As AdgDataSet
  file.OpenNewAdgDataSet(dataSet)

  ' This next line creates a key based on record format RCMMastL2
  Dim key As AdgKeyTable
  key = dataSet.NewKeyTable("RCMMastL2")

  ' We specifiy KeyPartCount to avoid specifiying the second
  ' key field.
  ' We then set the keyfield "CMName" to our search argument.
  key.KeyPartCount = 1
  key.Row("CMName") = "Thilmany Of Bread Co Resources"

  ' The following read will find the record associated with the 
  ' customer name "Thilmany Of Bread Co Resources" and store it
  ' in dataSet.
  file.ReadRandomKey(dataSet, ReadRandomMode.Equal, LockRequest.Default, key)
 </pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  /* This example will open a file and find the record for
     the customer "Thilmany of Bread Co Resources".
     It omits error trapping for clearity's sake. */
  DclFld db Type(AdgConnection) New("*Public/DG NET Local")
  db.Open()
  DclFld file Type(FileAdapter) New(db)
  file.FileName = "Examples//CMastNewL2"
  DclFld dataSet Type(AdgDataSet)
  file.OpenNewAdgDataSet(*ByRef dataSet)

  // This next line creates a key based on record format RCMMastL2

  DclFld key Type(AdgKeyTable) 
  key = dataSet.NewKeyTable("RCMMastL2") 

  /* We specifiy KeyPartCount to avoid specifiying the second
     key field. We then set the keyfield "CMName" to our search argument.*/

  key.KeyPartCount = 1 
  key.Row["CMName"] = "Thilmany Of Bread Co Resources" 

  /* The following read will find the record associated with 
     the customer name "Thilmany Of Bread Co Resources" and store
     it in dataSet.*/

  file.ReadRandomKey(dataSet, ReadRandomMode.Equal, LockRequest.Default, key)</pre>

Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [AdgDataSet Class Members](dcsAdgDataSetMembers.html)
      <br />
      [AdgKeyTable Class](dcsAdgKeyTableClass.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

