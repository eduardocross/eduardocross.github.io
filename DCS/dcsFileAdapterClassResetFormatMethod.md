---
title: FileAdapter.ResetFormat Method

Id: dcsFileAdapterClassResetFormatMethod
TocParent: dcsFileAdapterMethods
TocOrder: 23

keywords: ResetFormat method
keywords: FileAdapter.ResetFormat method

keywords: records, reset format restrictions
keywords: formats, reset record restrictions
keywords: how to, reset record format restrictions
keywords: multiformat files, reset record format restrictions
keywords: reset record format restrictions on multiformat files

---

For multi-format file access, reset the file to access a record of any format in subsequent operations (see [SetFormat](dcsFileAdapterClassSetFormatMethod.html)).
<pre>[C#]
 **public void ResetFormat();** </pre>
      <pre>[Visual Basic]
 **Public Sub ResetFormat()** </pre>
      <pre class="prettyprint">[Visual RPG]
 **BegSr ResetFormat Access(*Public)** </pre>
      <br />

Exceptions

None.
Remarks

By default, when accessing multi-format files, records of all formats are accessible. The **SetFormat** method of **FileAdapter** can be used to restrict access to only records of a certain format. The **ResetFormat** method is used to return the access mode to the default, non-format specific behavior.
Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
AdgConnection db = new AdgConnection("*Public/DG NET Local");
FileAdapter dbFile = new FileAdapter(db, "Examples/SalesMem", "SalesMem");
dbFile.AccessMode = AccessMode.Read;
AdgDataSet myDS = null;
dbFile.OpenNewAdgDataSet(out myDS);

/* Here we find the name of the customer whose sales (not counting returns) were
 * the best on average in January from 1998 to 2004. This example assumes
 * there are no customer numbers in the second format which are not found in the
 * first format, and that there are no years on record past 1998 to 2004.
 * We use the ResetFormat method to read from both formats, and
 * this gives us the ability to easy see the next customer's name before we
 * read their records. */

decimal total = 0;
decimal currentAverage = 0;
string currentName = "";
decimal maxAverage = -1;
string maxName = "";

dbFile.ResetFormat(); /* Read from both formats automatically. */
/* Make sure we start off on format 0. */
do{
    dbFile.ReadSequential(myDS,ReadSequentialMode.Next, LockRequest.Read);
  }while(dbFile.CurrentFormatIndex != 0);
try /* Read until end of file. Throw exception again if it was not due to EOF. */
    {
    while(true) /* Hitting end of file will throw an exception and let us leave. */
    {
/* Remember, the ActiveRow changes depending on the current format. */
        currentName = myDS.ActiveRow["CMName"].ToString();
        total = 0;
        dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);
        while (dbFile.CurrentFormatIndex == 1)
        {
            total += Convert.ToDecimal(myDS.ActiveRow["CSSales01"]);
            dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);
        }
/* there could be as many as seven records from 1998 - 2004. */
        currentAverage = total / 7;
        if (currentAverage &gt; maxAverage)
        {
            maxName = currentName;
            maxAverage = currentAverage;
        }
    }
}
catch(dgException dgEx)
{
    if (dgEx.Error != dgErrorNumber.dgEaEOF)
        throw dgEx;
}
string decimalResult = maxAverage.ToString();
decimalResult = decimalResult.Substring(0, decimalResult.IndexOf('.') + 3);
MessageBox.Show("The cusomter with the highest average sales in " +
    "January from 1998 - 2004 is \"" + maxName +
     "\", with an average of " + decimalResult + ".",
     "Result");
dbFile.Close();
db.Close();</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
Dim db As New AdgConnection("*Public/DG NET Local")
Dim dbFile As New FileAdapter(db, "Examples/SalesMem", "SalesMem")
dbFile.AccessMode = AccessMode.Read
Dim myDS As AdgDataSet = Nothing
dbFile.OpenNewAdgDataSet(myDS)

' Here we find the name of the customer whose sales (not counting returns) were
' the best on average in January from 1998 to 2004. This example assumes
' there are no customer numbers in the second format which are not found in the
' first format, and that there are no years on record past 1998 to 2004.
' We use the ResetFormat method to read from both formats, and
' this gives us the ability to easy see the next customer's name before we
' read their records.

Dim total As Decimal = 0
Dim currentAverage As Decimal = 0
Dim currentName As String = ""
Dim maxAverage As Decimal = -1
Dim maxName As String = ""
dbFile.ResetFormat() ' Read from both formats automatically.
' Make sure we start off on format 0.
Do
    dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read)
Loop While (dbFile.CurrentFormatIndex &lt;&gt; 0)

Try ' Read until end of file. Throw exception again If it was not due to EOF.
    While (True) ' Hitting end of file will throw an exception and let us leave.
        ' Remember, the ActiveRow changes depending on the current format.
        currentName = myDS.ActiveRow.Item("CMName").ToString()
        total = 0
        dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read)
        While (dbFile.CurrentFormatIndex = 1)
            total += Convert.ToDecimal(myDS.ActiveRow.Item("CSSales01"))
            dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read)
        End While
        ' there could be as many as seven records from 1998 - 2004.
        currentAverage = total / 7
        If (currentAverage &gt; maxAverage) Then
            maxName = currentName
            maxAverage = currentAverage
        End If
    End While
Catch dgEx As dgException
    If (dgEx.Error &lt;&gt; dgErrorNumber.dgEaEOF) Then
        Throw dgEx
    End If
End Try

Dim DecimalResult As String = maxAverage.ToString()
DecimalResult = DecimalResult.Substring(0, DecimalResult.IndexOf(".") + 3)

MsgBox("The cusomter with the highest average sales in " &amp; _
     "January from 1998 - 2004 is """ &amp; maxName &amp; _
     """, with an average of " &amp; DecimalResult &amp; ".", 
MsgBoxStyle.OKOnly, "Error")
dbFile.Close()
db.Close()
</pre>

Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Class Members](dcsFileAdapterMembers.html)
      <br />
      [SetFormat Method](dcsFileAdapterClassSetFormatMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

