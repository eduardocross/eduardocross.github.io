---
title: IAdgObject.WriteBases Method

Id: dcsIAdgObjectClassWriteBasesMethod
TocParent: dcsIAdgObjectMethods
TocOrder: 11

keywords: WriteBases method
keywords: IAdgObject.WriteBases method
keywords: how to, create XML document fragment for base object of single database object
keywords: XML [DCS 16.0 documents, create fragment from base objects description
keywords: XML [DCS 16.0 database objects, create fragment from base objects description
keywords: database objects, XML documents, create from base objects description

---

**WriteBases** creates an XML document fragment describing the base objects of a single database object.
<pre>        <span class="lang">
 **[C#]** 
        </span> **Public void WriteBases(
   System.Xml.XmlWriter writer
);**   </pre>
      <pre> **<span class="lang">[Visual Basic] </span>
 public Sub WriteBases(_
   ByVal writer As System.Xml.XmlWriter<br /> ) As IAdgObject**      </pre>
      <pre class="prettyprint">
 **<span class="lang">[Visual RPG]</span>
  BegSr WriteBases Access(*Public) Type(IAdgObject)<br />   DclSrParm writer Type(System.Xml.XmlWriter)**     </pre>

Parameters

<dl>
        <dt />
</dl>

*writer* 
<dl>
        <dd>
**System.Xml.XmlWriter** . A stream onto which the XML document fragment will be output.
</dd>
</dl>

Exceptions

<table class="dtTABLE" id="Table2" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="30%" style="FONT-WEIGHT: bold" />
            <col span="1" width="70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Exception Type</th>
            <th colspan="1" rowspan="1">
							Condition</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

InvalidOperationException 
</td>
            <td colspan="1" rowspan="1">

The value of the **WriteState** property of *writer* is **Closed** . 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgException 
</td>
            <td colspan="1" rowspan="1">

See table below. 
</td>
          </tr>
</table>

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="20%" style="FONT-WEIGHT: bold" />
            <col span="1" width="70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Value of dgException.Error
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOTFND 
</td>
            <td colspan="1" rowspan="1">

The database object the **IAdgObject** represents does not exist or is unavailable. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmFNOTFND 
</td>
            <td colspan="1" rowspan="1">

The database file the **IAdgObject** represents does not exist or is unavailable. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmMNOTFND 
</td>
            <td colspan="1" rowspan="1">

The database member the **IAdgObject** represents does not exist or is unavailable. 
</td>
          </tr>
</table>

Remarks

**WriteBases** is called by the [ WriteXml](dcsIAdgObjectClassWriteXmlMethods.html) method to generate the description of the base objects of an existing database file or member. This method may be used by user programs when only this portion of the object description is of interest. The description of base objects includes the path names of the base objects. The XML document fragment produced by **WriteBases** consists of exactly one element node at the current level of *writer* . Note that **WriteBases** produces a valid document fragment even when the database object does not define any base objects. 

If the base object description of **IAdgObject** has been previously set with the [ReadBases](dcsIAdgObjectClassReadBasesMethod.html) or the instance was created with [AdgFactory.ReadXml](dcsAdgFactoryClassReadXmlMethods.html), the information in the document fragment produced by **WriteBases** is equivalent to that provided to **ReadBases** or **ReadXml** . Otherwise, the description is obtained from the existing database object represented by **IAdgObject** the first time **WriteBases** is called.

On entry, the **WriteState** property of *writer* must not be **Closed** . On successful return from **WriteBases** , the value of **WriteState** will be the same as before the call.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [WriteXml Method](dcsIAdgObjectClassWriteXmlMethods.html)
      <br />
      [ReadBases Method](dcsIAdgObjectClassReadBasesMethod.html)
      <br />
      [AdgFactory Class](dcsAdgFactoryClass.html)
      <br />
      [ReadXml Method](dcsAdgFactoryClassReadXmlMethods.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

