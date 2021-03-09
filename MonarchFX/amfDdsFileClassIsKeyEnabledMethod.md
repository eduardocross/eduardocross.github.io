---
title: DdsFile.IsKeyEnabled Method

Id: amfDdsFileClassIsKeyEnabledMethod
TocParent: amfDdsFileClassMethods
TocOrder: 40

keywords: IsKeyEnabled method
keywords: DdsFile.IsKeyEnabled method
keywords: aidkeys, determine if enabled
keywords: attention keys, determine if enabled
keywords: function keys, determine if enabled
keywords: how to, determine aidkey enabled
keywords: web controls, determine aidkey enabled
keywords: display files, determine aidkey enabled

---

This method returns True if the aidkey indicated is enabled; otherwise False.

#### Syntax
<pre class="prettyprint"> **BegFunc IsKeyEnabled Access(*Public) Type(*Boolean)
    DclSrParm aidKey Type(ASNA.Monarch.WebDspF.AidKey)** </pre>

#### Parameters
<dl>
        <dt>
 *aidKey* 
        </dt>
        <dd>
 **ASNA.Monarch.WebDspF.AidKey**  enumeration
        value containing the key to be checked.</dd>
</dl>

<!--mine -->

#### Return Value
Boolean **True** if the *aidKey* is enabled; otherwise **False** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsFile Class](amfDdsFileClass.html) <br clear="none" /> [DdsFile Class Members](amfDdsFileClassMembers.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
