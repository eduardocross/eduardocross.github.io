---
title: XmlInfoEventHandler Delegate

Id: dcsXmlInfoEventHandlerDelegate
TocParent: dcsWhatsNewDelegates
TocOrder: 2

keywords: XmlInfoEventHandler delegate
keywords: delegates [DCS 16.0 XmlInfoEventHandler
keywords: XML [DCS 16.0 event handler, about feedback
keywords: event handlers, using delegates

---

This **XmlInfoEventHandler** delegate provides a feedback channel for the [ AdgFactory.ReadXml](dcsAdgFactoryClassReadXmlMethod2.html) and [IAdgObject.WriteXml](dcsIAdgObjectClassWriteXmlMethod2.html) methods.
<pre class="prettyprint">        <span class="lang">
 **[C#]**  </span> 
 **public delegate XmlInfoEventHandler(
   Object object,<br />[XmlInfoEventArgs](dcsXmlInfoEventArgsClass.html) args
);** 
      </pre>

      <pre class="prettyprint"> **<span class="lang">[Visual Basic] </span>
 Public Delegate Sub XmlInfoEventHandler(_
   ByVal object As Object _<br />   ByVal   args As [XmlInfoEventArgs](dcsXmlInfoEventArgsClass.html)<br /> ) As Object** 
</pre>

      <pre class="prettyprint"> **<span class="lang">[Visual RPG]</span>
 BegSr XmlInfoEventHandler Access(*Public) Type(Delegate)<br />   DclSrParm object Type(Object)<br />   DclSrParm   args Type([XmlInfoEventArgs](dcsXmlInfoEventArgsClass.html))<br />** </pre>

Parameters

<dl>
        <dt />
</dl>

*object* 
<dl>
        <dd>

The **System.Object** instance invoking the delegate. This parameter is reserved for the internal use of DCS and should not be manipulated by the user.
</dd>
        <dt />
</dl>

*args* 
<dl>
        <dd>

[XmlInfoEventArgs](dcsXmlInfoEventArgsClass.html). A reference to an object describing the event being reported.
</dd>
</dl>

Exceptions

DCS will ignore any exceptions raised by the delegate. That is, a raised exception will not be handled, and will thus terminate the **ReadXml** or **WriteXml** method. The caller of these methods should be prepared to handle any exceptions raised by the delegate. 
Remarks

The **XmlInforEventHandler** delegate is defined strictly for use as an optional parameter with the **IAdgObject.WriteXml** and **AdgFactory.ReadXml** methods. If desired, the user can define an implementation for this delegate to monitor the operation of these methods. The methods will periodically call the delegate to report a milestone of a certain detail level (see **XmlInfoEventArgs** ). 
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016,Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span> 
See 
Also

<dl />
      [XmlInfoEventArgs Class](dcsXmlInfoEventArgsClass.html)
      <br />
      [AdgFactory.ReadXml Method](dcsAdgFactoryClassReadXmlMethod2.html)
      <br />
      [IAdgObject.WriteXml Method](dcsIAdgObjectClassWriteXmlMethod2.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

