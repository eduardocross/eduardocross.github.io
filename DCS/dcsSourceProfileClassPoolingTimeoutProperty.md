---
title: SourceProfile.PoolingTimeout Property

Id: dcsSourceProfileClassPoolingTimeoutProperty
TocParent: dcsSourceProfilePropertiesMain
TocOrder: 6

keywords: PoolingTimeout property
keywords: SourceProfile.PoolingTimeout property
keywords: database connections, pooling timeout
keywords: pooling, enabling timeout for database connection
keywords: pooling, timeout database connection
keywords: how to, enable connection pooling for database connection

---

The amount of time (in minutes) in which a connection will remain idle in the pool until it is closed and removed from the pool.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public byte PoolingTimeout { get; set; )** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Property PoolingTimeout As Byte** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp PoolingTimeout Type(*Byte) Access(*Public)<br />   BegGet, BegSet** 
      </pre>

Property
 Value

Byte. The amount of time (in minutes) in which a connection will remain idle in the pool until it is closed and removed from the pool. 
Remarks

When database connection pooling is enabled, the communication to the server and to the server resources are kept in a special ‘pool’. The next time the application requires database services, one of the available connections in the ‘pool is assigned to it. Thus, enabling Pooling Connections results in faster database connections.

If connection pooling is not enabled, when a database and all its associated files are closed, the connection and server resources are ended (i.e., in the case of DataGate, the DataGate Job ends). When the same application needs the database services again, a new connection and corresponding job has to be established. This overhead wastes resources and slows down the application.
Examples

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  /* Connect using the already established database name 
   * "*PUBLIC/DG NET iSeries" but use a different idle
   * timeout time. */
  SourceProfile sp = new SourceProfile("*PUBLIC/DG NET iSeries");
  sp.PoolingTimeout = 10;
  AdgConnection database = new AdgConnection(sp);
</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Connect using the already established database name 
  ' "*PUBLIC/DG NET iSeries" but use a dIfferent idle
  ' timeout time. 
  Dim sp As New SourceProfile("*PUBLIC/DG NET iSeries")
  sp.PoolingTimeout = 10
  Dim dataBase As New AdgConnection(sp)</pre>

Requirements

**Namespace:** [ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html)

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span>
See Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html) <br />
      [SourceProfile Class Members](dcsSourceProfileMembers.html)<br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

