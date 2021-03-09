---
title: PrintDevAttr.ReadXml Method

Id: dcsPrintDevAttrClassReadXmlMethod
TocParent: dcsPrintDevAttrMethods
TocOrder: 0

keywords: ReadXml method
keywords: PrintDevAttr.ReadXml method

---

This is preliminary documentation and subject to change. 

This **ReadXml** method creates an instance of a **PrintDevAttr** XML object.
<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span> **public void ReadXml(
   System.Xml.XmlReader reader
);**      </pre>
      <pre class="prettyprint">
 **<span class="lang">[Visual Basic] </span>
 Public Sub ReadXml(_
   ByVal reader As System.Xml.XmlReader<br /> ) As PrintDevAttr**      </pre>
      <pre class="prettyprint">
 **<span class="lang">[Visual RPG]</span>
 BegSr ReadXml Access(*Public) Type(PrintDevAttr)<br />   DclSrParm reader Type(System.Xml.XmlReader)**      </pre>

Parameters

<dl>
        <dt />
</dl>

*reader* 
<dl>
        <dd>

**System.Xml.XmlReader** . The input stream used by **System.Xml.XmlReader** .
</dd>
</dl>

Returns

A new instance of a **PrintDevAttr** object.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span> 
See Also

<dl />
      [PrintDevAttr Class](dcsPrintDevAttrClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

