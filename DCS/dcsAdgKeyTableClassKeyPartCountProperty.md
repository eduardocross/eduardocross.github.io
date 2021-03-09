---
title: AdgKeyTable.KeyPartCount Property

Id: dcsAdgKeyTableClassKeyPartCountProperty
TocParent: dcsAdgKeyTableProperties
TocOrder: 1

keywords: AdgKeyTable.KeyPartCount property
keywords: KeyPartCount property
keywords: fields, getting the number composing the key
keywords: number of, fields composing the key

---

Gets or sets the number of key fields composing the key value.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public integer KeyPartCount { get:  set  }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Property KeyPartCount As Integer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp KeyPartCount Access(*Public) Type(*Integer)
   BegGet    BegSet** 
      </pre>

Property Value

**Integer** . Gets or sets the number of key parts of the key.
Remarks

In DataGate, a database file key is composed of an ordered set of fields ("key fields") much like record formats. Each key field corresponds to one field in a record format. A "key value" is defined as the concatenation of the values of some subset of the key fields. Fields in the subset, or "key parts", are the successive fields of the key fields set, beginning with the first.

This property specifies the number of key parts for the key represented by an **AdgKeyTable** instance. **KeyPartCount** and [Row](dcsAdgKeyTableClassRowProperty.html) together fully specify a key value for use with the keyed-access methods of [ FileAdapter](dcsFileAdapterClass.html) such as [ReadRandomKey](dcsFileAdapterClassReadRandomKeyMethod.html).

Upon construction of the **AdgKeyTable,** **KeyPartCount** is set to the number of key fields defined for the file.

Note that setting this property to a value less than zero or greater than the number of key fields will result in dgException being thrown with the Error property set to dgEINVARG. 
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AdgKeyTable Class](dcsAdgKeyTableClass.html)
      <br />
      [AdgKeyTable Class Members](dcsAdgKeyTableMembers.html)
      <br />
      [Row Property](dcsAdgKeyTableClassRowProperty.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [ReadRandomKey Method](dcsFileAdapterClassReadRandomKeyMethod.html)  <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)<br />
      [Efficient File Access](dcsEfficientFileAccess.html)

