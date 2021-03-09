---
title: DdsSubfileControl.ShowRecordAtTop Property

Id: amfDdsSubfileControlClassShowRecordAtTopProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 110

keywords: ShowRecordAtTop property
keywords: DdsSubfileControl.ShowRecordAtTop property
keywords: how to, set first record displayed
keywords: subfiles, setting first record displayed
keywords: subfile records, setting first record displayed
keywords: subfile controls, setting first record displayed
keywords: web controls, setting first record displayed
keywords: SFLRCDNBR _Star_TOP
keywords: _Star_TOP, SFLRCDNBR

---

Gets or sets a boolean value to indicate if the record number, contained in the hidden field in the [ ShowRecordField](amfDdsSubfileControlClassShowRecordFieldProperty.html) property, is displayed as the first record on the page. This is the equivalent to the SFLRCDNBR keyword *TOP.

#### Syntax
<pre class="prettyprint">
 **BegProp ShowRecordAtTop Access(*Public) Type(*Boolean)
   BegGet;  BegSet** 
            </pre>

#### Property Values
Boolean. **True** , indicates the record is displayed as the first record on the page; otherwise, **False** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ShowRecordField Property](amfDdsSubfileControlClassShowRecordFieldProperty.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
