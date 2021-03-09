---
title: NewActivationGroupAttribute.NewActivationGroupAttribute Constructor()

Id: amfNewActivationGroupAttributeClassConstructors
TocParent: amfNewActivationGroupAttributeClass
TocOrder: 10

keywords: NewActivationGroupAttribute class, constructors
keywords: NewActivationGroupAttribute.NewActivationGroupAttribute constructors
keywords: constructors [ASNA.Monarch], NewActivationGroupAttribute class
keywords: activation group, _Star_new
keywords: activation group, creating _Star_new instance
keywords: activation group attributes, _Star_new
keywords: activation manager, new activation group

---

This method constructs a new instance of a **NewActivationGroupAttribute** object.
<pre class="prettyprint"> **BegConstructor NewActivationGroupAttribute() Access(*Public)**       </pre>

#### Remarks
Using **NewActivationGroupAttribute** defines an instance when the activation group for the program is to be run in a new activation group. Monarch will create a new unique name for the group. An example of the BegClass follows.
<pre class="example"> BegClass Custcalc Extends (ASNA.Monarch.Program Access ( *Public ) +
 Attributes ( NewActivationGroup ())</pre>

Refer to [ ActivationGroupAttribute Class](amfActivationGroupAttributeClass.html) and [ CallerActivationGroupAttribute Class](amfCallerActivationGroupAttributeClass.html) for more information.
<!-- start -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td>[ASNA.Monarch](amfMonarchNamespace.html)</td>
          </tr>
          <tr>
            <td>Assembly:</td>
            <td>ASNA.VisualRPG.Runtime.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ NewActivationGroupAttribute Class](amfNewActivationGroupAttributeClass.html)<br />[ NewActivationGroupAttribute Class Members](amfNewActivationGroupAttributeClassMembers.html)<br />[ASNA.Monarch Namespace](amfMonarchNamespace.html)
