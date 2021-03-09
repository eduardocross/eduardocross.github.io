---
title: DdsDataField.ParseValues Method

Id: amfDdsDataFieldClassParseValuesMethod
TocParent: amfDdsDataFieldClassMethods
TocOrder: 120

keywords: ParseValues method
keywords: DdsDataField.ParseValues method
keywords: Web server controls [ASNA.Monarch], parse dropdown values
keywords: how to, parse field control dropdown values
keywords: display files, parsing field dropdown values
keywords: web controls, parsing field dropdown values
keywords: field controls, parsing dropdown valuesg
keywords: parsing field control dropdown values

---

This method parses the values to be displayed when the field is of type dropdown.

#### Syntax
<pre class="prettyprint"> **BegFunc ParseValues Access(*Public) Type(*String) Rank(1)
   DclSrParm *valueString*  Type(*String)** </pre>

#### Parameters
<dl>
        <dt>
 *valueString* 
        </dt>
        <dd>
 **String**  that represents the values that
        needs to be parsed.</dd>
</dl>

<!--mine -->

#### Return Value
String containing an array of the dropdown values.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsDataField Class](amfDdsDataFieldClass.html) <br /> [ DdsDataField Class Members](amfDdsDataFieldClassMembers.html) <br /> [ Derived Classes](amfDdsDataFieldDerivedClasses.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
