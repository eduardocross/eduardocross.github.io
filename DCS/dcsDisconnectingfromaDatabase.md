---
title: Disconnecting From a Database

Id: dcsDisconnectingfromaDatabase
TocParent: dcsConnectingtoaDatabaseMain
TocOrder: 1

keywords: disconnecting from a database
keywords: databases, disconnecting from

---

After database connection and access are complete, applications *must* disconnect from the database to properly release unmanaged resources. These unmanaged resources are provided to DCS by the <span>Common Language Runtime (CLR)</span> for network access. In general, DCS and the CLR will not release these unmanaged resources for you, and if not released, unexpected results, including loss of data, can occur. You must explicitly release unmanaged resources associated with **AdgConnection** objects using the [ AdgConnection.Close](dcsAdgConnectionClassCloseMethod.html) or [AdgConnection.Dispose](dcsAdgConnectionClassDisposeMethod.html) methods. You should call one of these methods before the **AdgConnection** variable loses scope or is reassigned.
<pre><span class="lang">[C#]</span>
  Cx.Close();
  Cx = null;</pre>
      <pre><span class="lang">[Visual Basic]</span>
  Cx.Close()
  Cx = Nothing</pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
  Cx.Close()
  Cx = *Nothing</pre>

Whether you use <span> **AdgConnection.Close** </span> or <span> **AdgConnection.Dispose** </span> is a matter of preference since they perform the same task of disconnecting the database and releasing unmanaged resources. Note that <span> **AdgConnection.Dispose** </span> implements the conventional <span> **System.IDisposable** </span> interface for **AdgConnection** . 
See Also
<dl />
      <span>
        [AdgConnection Class](dcsAdgConnectionClass.html)
      </span>
      <br />
      [AdgConnection.Close Method](dcsAdgConnectionClassCloseMethod.html)
      <br />
      [AdgConnection.Dispose Method](dcsAdgConnectionClassDisposeMethod.html)
      <br />
      [Connecting to a Database](dcsConnectingtoaDatabase.html)
      <br />

