---
title: PrintDevAttr.WriteXml Method

Id: dcsPrintDevAttrClassWriteXmlMethod
TocParent: dcsPrintDevAttrMethods
TocOrder: 1

keywords: WriteXml method
keywords: PrintDevAttr.WriteXml method

---

This is preliminary and subject to change. 

This **WriteXml** method creates XML representing the **PrintDevAttr** object, using writer as its output channel.
<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span> **public void WriteXml(
   System.Xml.Xmlwriter writer
);** 
      </pre>

      <pre class="prettyprint">
          <span class="lang">[Visual Basic] </span>
 **Public Sub WriteXml(_
   ByVal writer As System.Xml.Xmlwriter<br /> ) As PrintDevAttr** 
      </pre>

      <pre class="prettyprint">
 **<span class="lang">[Visual RPG]</span>
  BegSr WriteXml Access(*Public) Type(PrintDevAttr)<br />   DclSrParm writer Type(System.Xml.Xmlwriter)** 
      </pre>

Parameters

*writer* 
<dl>
        <dd>

An instance of **System.Xml.XmlWriter.** 
</dd>
</dl>

Returns

Xml representing the **PrintDevAttr** class.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span>
See Also

<dl />
      [PrintDevAttr Class](dcsPrintDevAttrClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

