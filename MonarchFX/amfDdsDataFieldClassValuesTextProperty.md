---
title: DdsDataField.ValuesText Property

Id: amfDdsDataFieldClassValuesTextProperty
TocParent: amfDdsDataFieldClassProperties
TocOrder: 140

keywords: ValuesText property
keywords: DdsDataField.ValuesText property
keywords: Web server controls [ASNA.Monarch], field values text
keywords: how to, set field control values text
keywords: how to, get field control values text
keywords: display files, setting field control values text
keywords: display files, getting field control values text
keywords: web controls, setting field control values text
keywords: web controls, getting field control values text
keywords: field controls, values text

---

Gets or sets the list of text to be shown when using the [ ValuesStyle](amfDdsDataFieldClassValuesStyleProperty.html) property is set to **DropdownText** or **DropdownBoth** for the field.

#### Syntax
<pre class="prettyprint"> **BegProp ValuesText Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String containing a list of valid values for the field; separated by blanks.

#### Remarks
The **ValuesText** property allows you to display for the user valid values that the input field can accept in the application; separated by spaces. However, if the [ Values](amfDdsDataFieldClassValuesProperty.html) property is left blank, which is the default, the user can enter anything into the field.

If using **Values** , you may want to also set the **ValuesText** property, which allows you to specify a corresponding word or phrase for each values entered in the **Values** property; separated by spaces. Use apostrophes to encapsulate the words in a phrase or to describe a blank entry e.g. **' ' 'Per Each' Dozen Gross 'Very Many'** corresponds to five values that would appear as: &lt;space&gt;, Per Each, Dozen, Gross, Very Many. The quote character (") has no tokenizing significance and is treated as a normal character.

For example, using **A B C D** in the **Values** property, you could enter the text **Add Browse Change Delete** in the **ValuesText** property.

For the user to see the entries in the **ValuesText** property, the **ValuesStyle** property must be set to either **DropdownText** or **DropdownBoth** .

With **ValuesStyle** set to **DropdownBoth** , **Values** set to **A B C D** , and **ValuesText** set to **Add Browse Change Delete** , the following will display for the user:
<blockquote dir="ltr">

<img alt="" src="../Images/DropdownBoth.jpg" border="0" /> 
</blockquote>

With **ValuesStyle** set to **DropdownText** and **ValuesText** set to **Add Browse Change Delete** , the following will display for the user:
<blockquote dir="ltr">

<img alt="" src="../Images/ValuesText_entries.jpg" border="0" /> 
</blockquote>

***Note:** If there are no entries in the **Values** property, then regardless if there are entries for the **ValuesStyle** and **ValuesText** properties, they will be disregarded and the field will display as a **TextBox** .* 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsDataField Class](amfDdsDataFieldClass.html) <br /> [ DdsDataField Class Members](amfDdsDataFieldClassMembers.html) <br /> [ Derived Classes](amfDdsDataFieldDerivedClasses.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)<br />[ ValuesStyle Property](amfDdsDataFieldClassValuesStyleProperty.html)<br />[Values Property](amfDdsDataFieldClassValuesProperty.html)
