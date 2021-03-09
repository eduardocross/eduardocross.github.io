---
title: SourceProfile()

Id: dcsSourceProfileClassSourceProfileConstructor1
TocParent: dcsSourceProfileConstructorsMain
TocOrder: 0

---

Constructs an anonymous instance of [ SourceProfile](dcsSourceProfileClass.html) with default values.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public SourceProfile();** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub New()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegConstructor Access(*Public)** 
      </pre>

Parameters

None.
Exceptions

None.
Remarks

The [DatabaseName](dcsSourceProfileClassDatabaseNameProperty.html) property of the **SourceProfile** created with this constructor is set to the empty string (""). Thus, the registry-related instance methods of **SourceProfile** ([Register](dcsSourceProfileClassRegisterMethod.html) and [Unregister](dcsSourceProfileClassUnregisterMethod.html)) are not available with such an object. 

This constructor is useful when the application should control all parameters of a database connection and should not be reliant on the Windows registry. It may also be useful for constructing a template object to be passed to the copy constructors of **SourceProfile** .

This constructor sets **SourceProfile** properties to default values as follows: 
<br />

<table class="dtTABLE" id="Table5" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 80%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Property
						</th>
            <th colspan="1" rowspan="1">
							Value
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[ DatabaseName](dcsSourceProfileClassDatabaseNameProperty.html) 
</td>
            <td colspan="1" rowspan="1">

""
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[Server](dcsSourceProfileClassServerProperty.html) 
</td>
            <td colspan="1" rowspan="1">

""
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[Label](dcsSourceProfileClassLabelProperty.html) 
</td>
            <td colspan="1" rowspan="1">

""
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[User](dcsSourceProfileClassUserProperty.html) 
</td>
            <td colspan="1" rowspan="1">

""
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[Password](dcsSourceProfileClassPasswordProperty.html) 
</td>
            <td colspan="1" rowspan="1">

""
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[PasswordType](dcsSourceProfileClassPasswordTypeProperty.html) 
</td>
            <td colspan="1" rowspan="1">

**PasswordType.SecurePassphrase** 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[PlatformAttribute](dcsSourceProfileClassPlatformAttributeProperty.html) 
</td>
            <td colspan="1" rowspan="1">

""
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[InitialLibl](dcsSourceProfileClassInitialLiblProperty.html) 
</td>
            <td colspan="1" rowspan="1">

**String** array of one element, with value ""
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[Text](dcsSourceProfileClassTextProperty.html) 
</td>
            <td colspan="1" rowspan="1">

""
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[Port](dcsSourceProfileClassPortProperty.html) 
</td>
            <td colspan="1" rowspan="1">

0
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[Qualifier](dcsSourceProfileClassQualifierProperty.html) 
</td>
            <td colspan="1" rowspan="1">

0
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[PoolingTimeout](dcsSourceProfileClassPoolingTimeoutProperty.html) 
</td>
            <td colspan="1" rowspan="1">

0
</td>
          </tr>
</table>

<br />

Requirements

<span> **Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span> 
See 
Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html) <br />[SourceProfile Class Members](dcsSourceProfileMembers.html)<br />[AdgConnection Class](dcsAdgConnectionClass.html)<br />[ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

