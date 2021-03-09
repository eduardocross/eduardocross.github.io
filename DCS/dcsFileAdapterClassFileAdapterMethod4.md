---
title: FileAdapter(AdgConnection, string, string)

Id: dcsFileAdapterClassFileAdapterMethod4
TocParent: dcsFileAdapterClassFileAdapterMethodMain
TocOrder: 3

---

Constructs an instance of the [ FileAdapter](dcsFileAdapterClass.html) object with an [AdgConnection](dcsAdgConnectionClass.html) object, file path name, and member name.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public FileAdapter(
   AdgConnection cn,
   string FileName,
   string MemberName
);** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Sub New( _
   ByVal cn As AdgConnection _
   ByVal FileName As String _
   ByVal MemberName As String
)** 
      </pre>
      <pre class="prettyprint"><code class="avr">        <span class="lang">[Visual RPG]</span>
 **BegConstructor Access(*Public)
   DclSrParm cn Type(AdgConnection)
   DclSrParm FileName Type(*String)
   DclSrParm MemberName Type(*String)** 
     </code> </pre>

Parameters

<dl>
        <dt>
 *cn* 
        </dt>
        <dd>An instance of **AdgConnection**  used to initialize the [
							Connection](dcsFileAdapterClassConnectionProperty.html) property. </dd>
        <dt>
 *FileName* 
        </dt>
        <dd>A string used to initialize the [FileName](dcsFileAdapterClassFileNameProperty.html)
								property. </dd>
        <dt>
 *MemberName* 
        </dt>
        <dd>A string used to initialize the [
											MemberName](dcsFileAdapterClassMemberNameProperty.html) property.
									</dd>
</dl>

Remarks

This constructor creates an instance of **FileAdapter** with the given database connection, file path, and member name (which are used to initialize the **Connection** , **FileName** , and **MemberName** properties respectively). If the value of the given member name is null or an empty string, and the **MemberName** property is not otherwise set prior to a call to the [ Open](dcsFileAdapterClassOpenMethod.html) method, DCS assigns this property the value "*FIRST".

The [AccessMode](dcsFileAdapterClassAccessModeProperty.html) property is initialized with the value Read.
Examples

<pre>        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection dataBase = new AdgConnection("*Public/DG NET IBM i");
  FileAdapter dbFile = new FileAdapter(dataBase, "*Libl/CMASTNEWL1", "CMMASTERL1");</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim dataBase As New AdgConnection("*Public/DG NET IBM i")
  Dim dbFile As New FileAdapter(dataBase, "*Libl/CMASTNEWL1", "CMMASTERL1");</pre>
      <pre class="prettyprint">        <span class="lang">
 **[Visual RPG]** 
        </span>
  DclFld dataBase Type(AdgConnection) New("*Public/DG NET IBM i")
  DclFld dbFile Type(FileAdapter)
  dbFile = *New FileAdapter(dataBase, "*Libl/CMASTNEWL1", "CMMASTERL1");</pre>

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
      [AccessMode Property](dcsFileAdapterClassAccessModeProperty.html)
      <br />
      [Connection Property](dcsFileAdapterClassConnectionProperty.html)
      <br />
      [FileName Property](dcsFileAdapterClassFileNameProperty.html)
      <br />
      [MemberName Property](dcsFileAdapterClassMemberNameProperty.html)
      <br />
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [AccessMode Enumeration](dcsAccessModeEnumeration.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

