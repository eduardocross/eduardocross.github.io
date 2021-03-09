---
title: SourceProfile.Password Property

Id: dcsSourceProfileClassPasswordProperty
TocParent: dcsSourceProfilePropertiesMain
TocOrder: 3

keywords: Password property
keywords: SourceProfile.Password property
keywords: password to connect to a database
keywords: password, user profile
keywords: how to, specify password to connect to a database
keywords: how to, specify password for user profile

---

The password to be used in conjunction with [ User](dcsSourceProfileClassUserProperty.html) for connection authentication.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public string Password { set; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public ReadOnly Property Password As String** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Password Type(*String) Access(*Public)<br />   BegSet** 
      </pre>

Property
 Value

String. Write-only. Sets a string specifying the password for the user profile indicated by the **User** property.
Remarks

Authentication is the process of verifying that a user with a unique name is the actual user that the name implies. This verification process is also applied to applications running in the security context of a user. Typically, authentication is implemented by giving the user a password.

This property should only be set if the user profile has an associated password, and only after setting the <span> **User** </span> property. 
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
  AdgConnection database = new AdgConnection(sp);</pre>
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
  Dim database As New AdgConnection(sp)</pre>

Requirements

**Namespace:** [ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html)

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 </span> 
See Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [SourceProfile Class Members](dcsSourceProfileMembers.html)
      <br />
      [User Property](dcsSourceProfileClassUserProperty.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

