---
title: ValuesStyle Enumeration

Id: amfValuesStyleEnumeration
TocParent: amfWebDspFEnumerations
TocOrder: 140

keywords: enumerations [ASNA.Monarch.WebDspF], ValuesStyle
keywords: ValuesStyle enumeration

keywords: DropDownValues enumeration member
keywords: DropDownText enumeration member
keywords: DropDownBoth enumeration member
keywords: Textbox enumeration member

---

The **ValuesStyle** enumerated constant defines the control style used to enable users to select from a single selection down-down ListBox, or textbox. This impacts the drop-down style for the **Values** , **ValuesText** , and the **Text** properties.

#### Syntax
<pre class="prettyprint"> **BegEnum ValuesStyle Access(*Public)** </pre>

#### Remarks
A drop-down control shows a drop-down button displaying the associated items, depending upon the **ValuesStyle** type and entries in **Values** and/or **ValuesText** .

#### Members
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="15%" /><col width="80%" /><col width="5%" align="center"/>
          </colgroup>
          <tr><th>Member</th>
  <th>Description</th>
  <th>Value</th>
          </tr>
          <tr>
            <td>Textbox</td>
            <td>(Default). The field displays
          as a text box.</td>
            <td>0</td>
          </tr>
          <tr>
            <td>DropDownBoth</td>
            <td>The field displays as a
          drop-down box containing the entries in the 
 **Values**  and 
 **ValuesText**  properties.</td>
            <td>1</td>
          </tr>
          <tr>
            <td>DropDownText</td>
            <td>The field displays as a
          drop-down box containing the entries in the 
 **ValuesText**  property.</td>
            <td>2</td>
          </tr>
          <tr>
            <td>DropDownValues</td>
            <td>The field displays as a
          drop-down box containing the entries in the 
 **Values**  property.</td>
            <td>3</td>
          </tr>
</table>

<!-- -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup><col width="15%" style="font-weight:bold" /><col width="85%" />
          </colgroup>
          <tr><td>Namespace:</td>
 <td>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)</td>
          </tr>
          <tr><td>Assembly:</td>
          <td>ASNA.Monarch.WebDspF.DLL</td>
          </tr>
         <tr><td>Platforms:</td>
 <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

#### See Also
<dl>
   <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
   <dd>[ValuesText Property](amfDdsDataFieldClassValuesTextProperty.html)</dd>
   <dd>[Values Property](amfDdsDataFieldClassValuesProperty.html)</dd>
</dl>

