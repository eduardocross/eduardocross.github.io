---
title: SourceProfile.User Property

Id: dcsSourceProfileClassUserProperty
TocParent: dcsSourceProfilePropertiesMain
TocOrder: 11

keywords: User property
keywords: SourceProfile.User property
keywords: host platform, authenticating user or profile name, 
keywords: profile name, authenticating host platform access
keywords: user name, authenticating host platform access
keywords: database files, authenticating user or profile name host platform access
keywords: _Star_PROMPT authentication usage
keywords: database files, _Star_PROMPT authentication usage
keywords: database files, _Star_DOMAIN authentication usage
keywords: _Star_DOMAIN authentication usage
keywords: authenticating user or profile name host platform access
keywords: authentication, user or profile name host platform access
keywords: how to, use user or profile name for host platform access
keywords: how to, prompt user for user name and password

---

A user or profile name for authenticating access to the host platform.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public string User { get; set; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Property User As String** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp User Type(*String) Access(*Public)<br />   BegGet, BegSet** 
      </pre>

Property
 Value

String. Returns or sets a string containing the user or profile name for authenticating access to the host platform.
Remarks

Authentication is the process of verifying that a user with a unique name is the actual user that the name implies. This verification process is also applied to applications running in the security context of a user. Typically, authentication is implemented by giving the user a password.

The user profile described by the **User** property is the one used to authenticate the database connection on the server platform, not the client. Typically, this user profile is given in the Acceler8DB database name or by this property.

A special value, "*PROMPT", may be used to require an interactive user to supply a user name and password (via dialog box) at the moment the database connection is initiated. Another special value, "*DOMAIN", may be used to specify that the authentication of the currently signed on client-side user profile be used to authorize access to the server, if both the client and server are members of the same Windows NT domain. 
Examples

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  /* Connect using the already established database name 
   * "*PUBLIC/DG NET iSeries" but use a different
   * username and password. */
  SourceProfile sp = new SourceProfile("*PUBLIC/DG NET iSeries");
  sp.User = "NewUser";
  sp.Password = "NewPassword";
  AdgConnection database = new AdgConnection(sp);
</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Connect using the already established database name 
  ' "*PUBLIC/DG NET iSeries" but use a dIfferent
  ' username and password. 
  Dim sp As New SourceProfile("*PUBLIC/DG NET iSeries")
  sp.User = "NewUser"
  sp.Password = "NewPassword"
  Dim database As New AdgConnection(sp)
</pre>

Requirements

**Namespace:** [ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html)

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012, Windows Server 2016, Windows 7, Windows 8.x, Windows 10</span>
See Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [SourceProfile Class Members](dcsSourceProfileMembers.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

