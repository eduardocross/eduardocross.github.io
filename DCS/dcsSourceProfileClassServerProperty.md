---
title: SourceProfile.Server Property

Id: dcsSourceProfileClassServerProperty
TocParent: dcsSourceProfilePropertiesMain
TocOrder: 9

keywords: Server property
keywords: SourceProfile.Server property
keywords: database servers, DNS host machine name set/return
keywords: database servers, TCP/IP address set/return
keywords: DNS host machine name for database server
keywords: how to, establish DNS host machine name for database server
keywords: TCP/IP address of a database server
keywords: how to, establish TCP/IP address of a database server

---

The database server host machine name or address.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public string Server { get; set; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Property Server As String** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Server Type(*String) Access(*Public)** 
      </pre>

Property Value

String. Returns or sets a string containing either a DNS host name or, a TCP/IP address in "dotted decimal" notation.
Remarks

The <span> **Server** </span> property may either be: 1) a Domain Name System (DNS) host name or 2) a TCP/IP address in "dotted decimal" notation (such as 127.0.0.1). 
Examples

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  /* The code below updates a database profile to use a different IP address. */
  SourceProfile sp = new SourceProfile("CustomerDB");
  sp.Server = "555.93.279.303";
  sp.Register(); /* Save changes. */
</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' The code below updates a database profile to use a different IP address. 
  Dim sp As New SourceProfile("CustomerDB")
  sp.Server = "555.93.279.303"
  sp.Register() ' Save changes. </pre>

Requirements

<strong class="hcp2">Namespace:</strong> [ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html)

<span><strong class="hcp2">Assembly:</strong> ASNA DataGate Client</span> 

<span><strong class="hcp2">Platforms:</strong> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span>
See Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [SourceProfile Class Members](dcsSourceProfileMembers.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

