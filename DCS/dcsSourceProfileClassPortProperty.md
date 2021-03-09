---
title: SourceProfile.Port Property

Id: dcsSourceProfileClassPortProperty
TocParent: dcsSourceProfilePropertiesMain
TocOrder: 7

keywords: Port property
keywords: SourceProfile.Port property
keywords: database servers, port number
keywords: port number, default
keywords: port number, set/return TCP port number
keywords: TCP port number, TCP/IP based transport, default
keywords: TCP port number, TCP/IP based transport
keywords: how to, TCP port number used for TCP/IP based transport

---

The TCP port number used by the database server for TCP/IP-based transport (default 5042). 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public int Port { get; set; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Property Port As Integer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Port Type(*Integer) Len(4) Access(*Public)<br />   BegGet, BegSet** 
      </pre>

Property Value

Integer. Returns or sets the TCP port number that is to be used for TCP/IP-based transport. 
Remarks

The default TCP port number is 5042. 
Examples

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  /* When we specify false with this constructor, we're
   * telling Datagate not to get information from the
   * registry. Thus we can use it to create an entirely
   * new database name. */
  SourceProfile newDbProfile = new SourceProfile("New database", false);
  newDbProfile.Server = "valid ip address";
  newDbProfile.User = "User1";
  newDbProfile.Password = "password"; /* Note- not very secure. */
  newDbProfile.Port = 5047;
  newDbProfile.PoolingTimeout = 0;
  newDbProfile.PlatformAttribute = "*DATALINK";
  newDbProfile.Text = "New database at valid ip address, on port 5047.";
  /* Register the database name. */
  newDbProfile.Register();</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' When we specIfy false with this constructor, we're
  ' telling Datagate not to get inFormation from the
  ' registry. Thus we can use it to create an entirely
  ' new database name. 
  Dim newDbProfile = New SourceProfile("New database", False)
  newDbProfile.Server = "valid ip address"
  newDbProfile.User = "User1"
  newDbProfile.Password = "password" ' ' Note- not very secure. 
  newDbProfile.Port = 5047
  newDbProfile.PoolingTimeout = 0
  newDbProfile.PlatFormAttribute = "*DATALINK"
  newDbProfile.Text = "New database at valid ip address, on port 5047."
  ' Register the database name.
  newDbProfile.Register()</pre>

Requirements

**Namespace:** [ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html)

<span> **Assembly:** ASNA DataGate Client </span> 

<span /> <span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span>
See Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [SourceProfile Class Members](dcsSourceProfileMembers.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

