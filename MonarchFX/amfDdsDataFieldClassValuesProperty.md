---
title: DdsDataField.Values Property

Id: amfDdsDataFieldClassValuesProperty
TocParent: amfDdsDataFieldClassProperties
TocOrder: 120

keywords: Values property
keywords: DDS VALUES
keywords: DdsDataField.Values property
keywords: Web server controls [ASNA.Monarch], field values
keywords: how to, set field control values
keywords: how to, get field control values
keywords: display files, setting field control values
keywords: display files, getting field control values
keywords: web controls, setting field control values
keywords: web controls, getting field control values
keywords: field controls, values

---

Gets or sets the list of valid values for the field; separated by blanks.

#### Syntax
<pre class="prettyprint"> **BegProp Values Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String containing the list of valid values for the field; separated by blanks.

#### Remarks
The **Values** property allows you to display the valid values that the data field can accept in the application; separated by spaces. However, if the **Values** property is left blank, which is the default, the user can enter anything into the field.

For example, if the application were looking for an input value of A, B, C, or D, you would list the values **A B C D** in the **Values** property.

However, unless the user knows what those values stand for, values alone can be confusing. If using **Values** , you may want to also set the [ ValuesText](amfDdsDataFieldClassValuesTextProperty.html) property, which allows you to specify one word per value entered in the **Values** property; separated by spaces.

For the user to see these **Values** , the [ ValuesStyle](amfDdsDataFieldClassValuesStyleProperty.html) property must be set to either **DropdownValues** or **DropDownBoth** .

For example, using **A B C D** in **Values** , **Add Browse Change Delete** in **ValuesText** , and **DropDownBoth** in **ValuesStyle** , the user would see the following in the field:

<img alt="" src="../Images/DropdownBoth.jpg" border="0" /> 

Changing **ValuesStyle** to **DropdownValues** , the following will display:

<img alt="" src="../Images/Values_entries.jpg" border="0" /> 

***Note:** If there are no entries in the **Values** property, then regardless if there are entries for the **ValuesStyle** and **ValuesText** properties, they will be disregarded and the field will display as a **TextBox** .* 

Please note that the DDS VALUES string becomes the setting for the **Values** property and the default setting for the **ValuesStyle** property is *DropdownValues* . When the user drops down the list, the **Values** elements are displayed.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsDataField Class](amfDdsDataFieldClass.html) <br /> [ DdsDataField Class Members](amfDdsDataFieldClassMembers.html) <br /> [ Derived Classes](amfDdsDataFieldDerivedClasses.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)<br />[ValuesText Property](amfDdsDataFieldClassValuesTextProperty.html)<br />[ ValuesStyle Property](amfDdsDataFieldClassValuesStyleProperty.html)
