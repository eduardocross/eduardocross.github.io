---
title: DdsSubfile.GetConditionedValue Method

Id: amfDdsSubfileClassGetConditionedValueMethod
TocParent: amfDdsSubfileClassMethods
TocOrder: 20

keywords: DdsSubfile.GetConditionedValue method
keywords: GetConditionedValue method
keywords: how to, get conditional value for subfile
keywords: conditioning expressions, subfile fields
keywords: subfiles, conditional field expressions
keywords: subfile fields, controlling data displayed
keywords: subfile records, controlling fields displayed
keywords: web controls, controlling fields displayed
keywords: subfile usage, controlling fields displayed
keywords: subfile usage, controlling data rendering

---

This method returns a string containing the conditional values for a specific field.

#### Syntax
<pre class="prettyprint"> **BegFunc GetConditionedValue Access(*Public) Type(*String) Modifier(*Overrides)
   DclSrParm *fieldID*  Type(*string)
   DclSrParm *possibleValues*  Type(ASNA.Monarch.WebDspF.ConditionalValue) Rank(1)** </pre>

#### Parameters
<dl>
        <dt>
 *fieldID* 
        </dt>
        <dd>String containing the ID for the field to get the
        conditional values for.</dd>
        <dt>
 *possibleValues* 
        </dt>
        <dd>An array of 
        [
        ASNA.Monarch.WebDspF.ConditionalValue](amfConditionalValueClass.html) objects that
        represent the condition values for the field.</dd>
</dl>

#### Returns
String containing the conditional indicator expressions for the specific field. The composition of a conditional indicator expression is ** *value* : *condition* ** . An example using conditional indicators might be Red:03 &amp; !99, where ***value*** is "Red", and the ***condition*** is "03 &amp; !99". The actual conditional values array contents will depend upon the conditional values set for the field ID within the record. An example using conditional indicators might be "Red:03 &amp; !99", where ***value*** is "Red", and the ***condition*** is "03 &amp; !99". See [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) for more information.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsSubfile Class](amfDdsSubfileClass.html) <br /> [ DdsSubfile Class Members](amfDdsSubfileClassMembers.html) <br /> [ ConditionalValue Class](amfConditionalValueClass.html) <br /> [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
