---
title: DdsFile.AddValidationMessage Method

Id: amfDdsFileClassAddValidationMessageMethod
TocParent: amfDdsFileClassMethods
TocOrder: 20

keywords: AddValidationMessage method
keywords: DdsFile.AddValidationMessage method
keywords: attention keys, adding validation message
keywords: function keys, adding validation message
keywords: validation messages, adding
keywords: web controls, adding validation messages
keywords: display files, adding validation messages

---

This method adds a validation message to the control.

#### Syntax
<pre class="prettyprint"> **BegSr AddValidationMessage Access(*Public) Type(Void)
    DclSrParm *message*  Type(ASNA.Monarch.WebDspF.ErrorMessageInfo)
    DclSrParm *messageSource*  Type(*String)** </pre>

#### Parameters
<dl>
        <dt>
 *message* 
        </dt>
        <dd>
 **ASNA.Monarch.WebDspF.ErrorMessageInfo**  object to be
        added. This contains text of the message and information
        about replacement variables and can include variable data
        that is being provided by the message sender.</dd>
        <dt>
 *messageSource* 
        </dt>
        <dd>
 **String**  containing identification of the
        source of the message.</dd>
</dl>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsFile Class](amfDdsFileClass.html) <br clear="none" /> [DdsFile Class Members](amfDdsFileClassMembers.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
