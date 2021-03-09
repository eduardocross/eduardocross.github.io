---
title: DdsSubfileControl.SubfileStyle Property

Id: amfddsSubfileControlClassSubfileStyleProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 250

keywords: SubfileStyle property
keywords: DdsSubfileControl.SubfileStyle property

keywords: subfile style, classic
keywords: subfile style, dropdown box
keywords: subfile style, checkboxes
keywords: subfile style, radio buttons
keywords: classic, subfile style
keywords: dropdown box, subfile styles
keywords: checkbox, subfile style
keywords: listbox, subfile style
keywords: radio button, subfile style
keywords: enumerations [ASNA.Monarch.WebDspF], SubfileStyles, used by
keywords: SubfileStyles enumeration, used by
keywords: how to, set subfile style
keywords: how to, get subfile style
keywords: subfiles, setting style
keywords: subfiles, getting style
keywords: subfile records, setting subfile style
keywords: subfile records, getting subfile style
keywords: subfile controls, setting subfile style
keywords: subfile controls, getting subfile style
keywords: web controls, subfile styles
keywords: display files, subfile styles

---

Gets or sets the style of the Subfile from a member of the [ SubfileStyles](amfSubfileStylesEnumeration.html) enumeration that specifies the HTML element used for the subfile data; Classic, Checkboxes, DropDown, ListBox, and RadioButtons.

#### Syntax
<pre class="prettyprint"> **BegProp SubfileStyle Access(*Public) Type([SubfileStyles](amfSubfileStylesEnumeration.html))
   BegGet;  BegSet** </pre>

#### Property Values
**SubfileStyles** that specifies the HTML element used for the subfile data; Classic, Checkboxes, DropDown, ListBox, and RadioButtons.

#### Remarks
The default subfile style is **Classic** , which functions the same as subfiles in AVR Classic.

To set this property at design-time, click on the arrow to the right of the **SubfileStyle** property and select one of the options from the drop-down box.

A subfile is typically rendered in a classic tabular format with each record in the subfile providing the data for a row and field shown as a column. However, it is possible to render a subfile records as a sequence of checkboxes, radio buttons, in a drop-down box, or a list box. This property determines the widget(s) to use for rendering the subfile. If a style other than **Classic** is selected, the subfile record must have at least three fields where the first three fields must have the following format:
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col style="FONT-WEIGHT: bold" width="10%" />
            <col width="10%" />
            <col width="75%" />
          </colgroup>
          <tr>
            <th>Field</th>
            <th>Type</th>
            <th>Notes</th>
          </tr>

          <tr>
            <td>Control</td>
            <td>Numeric</td>
            <td>Determines which button is
            selected. 0 = not selected, 1 = selected.</td>
          </tr>
          <tr>
            <td>Value</td>
            <td>Any</td>
            <td>Used to help the 
 **program**  distinguish this record from
            other records.</td>
          </tr>
          <tr>
            <td>Text</td>
            <td>Any</td>
            <td>Displayed in the browser.
            Used to help the 
 **user**  distinguish this record from other
            records.</td>
          </tr>
</table>

The order of the three fields is significant and is determined by the sequence in how they are ordered in the markup file and not in the screen (top, left) position. The name of the fields is not important; neither are the details of their types, as long as the *Control* field is of numeric type.

Besides the classic style, the SubfileStyle permits selecting one of the following styles: CheckBoxes, Dropdown, Listbox, RadioButtons

**Checkboxes** 

The Dropdown style displays each record on the subfile as a checkbox with the ** *Text* ** as the checkbox's text. Multiple checkboxes can be selected. If a record's ** *Control* ** field is set to 1, then it is considered selected, otherwise it is not. The user can modify the selected state of each record and the ** *Control* ** field will be updated accordingly; READC will return all records modified.

**Listbox** 

A style of Listbox displays every record of the subfile as an element of a listbox. Only one element can be selected, the first one found to have its *Control* field set to 1. The user can change the selection, in this case READC will return the new record selected and the old record that was de-selected.

**Radio Buttons** 

The RadioButtons style is similar to the Checkboxes style, the difference between the two styles lies in that RadioButtons permit the user to only select one of the records of the subfile.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ SubfileStyles Enumeration](amfSubfileStylesEnumeration.html) 
