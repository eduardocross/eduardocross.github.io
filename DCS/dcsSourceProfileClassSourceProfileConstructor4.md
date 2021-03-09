---
title: SourceProfile(SourceProfile)

Id: dcsSourceProfileClassSourceProfileConstructor4
TocParent: dcsSourceProfileConstructorsMain
TocOrder: 3

---

Constructs an instance of [SourceProfile](dcsSourceProfileClass.html) that is an exact copy of the given **SourceProfile** .
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public SourceProfile(<br />   SourceProfile sp<br />);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub New( _<br />   ByVal sp As [SourceProfile](dcsSourceProfileClass.html)<br />)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegConstructor Access(*Public)<br />   DclSrParm sp Type(SourceProfile)** 
      </pre>

Parameters

<dl>
        <dt>
 *sp* 
        </dt>
        <dd>
          [SourceProfile](dcsSourceProfileClass.html). The **SourceProfile** 
						to be copied by the constructed object.
					</dd>
</dl>

Exceptions

<table class="dtTABLE" id="table2" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">

Exception Type
</th>
            <th colspan="1" rowspan="1">

Condition
</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NullReferenceException
</td>
            <td colspan="1" rowspan="1">

*sp* is a null reference.
</td>
          </tr>
</table>

Remarks

All public properties of the constructed object have the same value as the copied **SourceProfile** , including [ DatabaseName](dcsSourceProfileClassDatabaseNameProperty.html) property such that the [ Equals](dcsSourceProfileClassEqualsMethod.html) method of the resulting object returns **True** when passed *sp* . The object constructed in this way is identical to the object returned by the [Clone](dcsSourceProfileClassCloneMethod.html) method of *sp* .
Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

[SourceProfile Class](dcsSourceProfileClass.html) <br />
        [SourceProfile Class Members](dcsSourceProfileMembers.html)<br />
		[Clone Method](dcsSourceProfileClassCloneMethod.html)<br />
		[DatabaseName Property](dcsSourceProfileClassDatabaseNameProperty.html)<br />
		[Equals Method](dcsSourceProfileClassEqualsMethod.html)<br />
		[ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

