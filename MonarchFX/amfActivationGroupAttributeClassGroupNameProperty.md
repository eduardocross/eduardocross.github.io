---
title: ActivationGroupAttribute.GroupName Property

Id: amfActivationGroupAttributeClassGroupNameProperty
TocParent: amfActivationGroupAttributeClassProperties
TocOrder: 10

keywords: GroupName property
keywords: ActivationGroupAttribute.GroupName property
keywords: activation group name
keywords: activation group attributes, group name
keywords: activation group attributes, getting group name

---

Gets a string value containing the name of the activation group to use for the program.

#### Syntax
<pre class="syntax"> **BegProp GroupName Access(*Public) Type(*String)
   BegGet;** </pre>

#### Property Values
String. The name for the activation group to use for the program.

#### Remarks
When a **GroupName** is used, the [ IsDefault](amfActivationGroupAttributeClassIsDefaultProperty.html), [ IsNew](amfActivationGroupAttributeClassIsNewProperty.html), and [ IsCaller](amfActivationGroupAttributeClassIsCallerProperty.html) properties will all be **False** .
<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[ ActivationGroupAttribute Class](amfActivationGroupAttributeClass.html) <br clear="none" /> [ ActivationGroupAttribute Members](amfActivationGroupAttributeClassMembers.html) <br clear="none" /> [ CallerActivationGroupAttribute Class](amfCallerActivationGroupAttributeClass.html) <br clear="none" /> [ NewActivationGroupAttribute Class](amfNewActivationGroupAttributeClass.html) <br clear="none" />[ASNA.Monarch Namespace](amfMonarchNamespace.html)
