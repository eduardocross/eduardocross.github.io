---
title: FileAdapter(AdgConnection)

Id: dcsFileAdapterClassFileAdapterMethod2
TocParent: dcsFileAdapterClassFileAdapterMethodMain
TocOrder: 1

---

Constructs an instance of the [FileAdapter](dcsFileAdapterClass.html) object using the given [AdgConnection](dcsAdgConnectionClass.html) object.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public FileAdapter(
   AdgConnection cn
);** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Sub New( _
   ByVal cn As AdgConnection _
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegConstructor Access(*Public)
   DclSrParm cn Type(AdgConnection)** 
      </pre>

Parameters

<dl>
        <dt>
 *cn* 
        </dt>
        <dd>An instance of **AdgConnection**  used to initialize the [
			Connection](dcsFileAdapterClassConnectionProperty.html) property.
					</dd>
</dl>

Remarks

This constructor creates an instance of **FileAdapter** with the given database connection but without a file path or member name. The [Open](dcsFileAdapterClassOpenMethod.html) method of such an instance cannot be used until its [ FileName](dcsFileAdapterClassFileNameProperty.html) property is set (the constructor initializes its value to null). The [MemberName](dcsFileAdapterClassMemberNameProperty.html) property is initialized to null. If **MemberName** is not explicitly set prior to a call to the **Open** method, DCS assigns the value "*FIRST" to this property.

The [AccessMode](dcsFileAdapterClassAccessModeProperty.html) property is initialized with the value [Read](dcsAccessModeEnumeration.html).
Examples

<pre>        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection dataBase = new AdgConnection("*Public/DG NET IBM i");
  FileAdapter dbFile = new FileAdapter(dataBase);
  dbFile.FileName = "*Libl/CMASTNEWL1";
  dbFile.MemberName = "CMMASTERL1";</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim dataBase As New AdgConnection("*Public/DG NET IBM i")
  Dim dbFile As New FileAdapter(dataBase)
  dbFile.FileName = "*Libl/CMASTNEWL1"
  dbFile.MemberName = "CMMASTERL1"</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  DclFld dataBase Type(AdgConnection) New("*Public/DG NET IBM i")
  DclFld dbFile Type(FileAdapter)
  dbFile = *New FileAdapter(dataBase)
  dbFile.FileName = "*Libl/CMASTNEWL1"
  dbFile.MemberName = "CMMASTERL1"</pre>

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

