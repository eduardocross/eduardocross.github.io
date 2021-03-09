---
title: ActivationGroupAttribute.IsCaller Property

Id: amfActivationGroupAttributeClassIsCallerProperty
TocParent: amfActivationGroupAttributeClassProperties
TocOrder: 20

keywords: IsCaller property
keywords: ActivationGroupAttribute.IsCaller property
keywords: activation group, _Star_caller
keywords: activation group attributes, _Star_caller

---

Gets a boolean value indicating whether the program will be allocated in the same activation group as the program calling this program. The default is **False** .

#### Syntax
<pre class="syntax"> **BegProp IsCaller Access(*Public) Type(*Boolean)
  BegGet;** </pre>

#### Property Values
Boolean. **True** indicates the program will be allocated in the same activation group as the program calling this program; otherwise **False** .

#### Remarks
Refer to [ GroupName](amfActivationGroupAttributeClassGroupNameProperty.html), [ IsDefault](amfActivationGroupAttributeClassIsDefaultProperty.html), and [ IsNew](amfActivationGroupAttributeClassIsNewProperty.html) properties for additional information.
<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[ ActivationGroupAttribute Class](amfActivationGroupAttributeClass.html) <br clear="none" /> [ ActivationGroupAttribute Members](amfActivationGroupAttributeClassMembers.html) <br clear="none" /> [ CallerActivationGroupAttribute Class](amfCallerActivationGroupAttributeClass.html) <br clear="none" /> [ NewActivationGroupAttribute Class](amfNewActivationGroupAttributeClass.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
