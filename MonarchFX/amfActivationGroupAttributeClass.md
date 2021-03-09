---
title: ActivationGroupAttribute Class

Id: amfActivationGroupAttributeClass
TocParent: amfMonarchNamespaceClasses
TocOrder: 10

keywords: ActivationGroupAttribute class, about ActivationGroupAttribute class
keywords: classes [ASNA.Monarch], ActivationGroupAttribute class
keywords: activation manager, ActivationGroupAttribute
keywords: CALLER constant
keywords: DEFAULT constant
keywords: NEW constant

---

The **ActivationGroupAttribute** is provided to support the job activation manager to set an activation group attribute.

For a list of all members of this class, see [ ActivationGroupAttribute Class Members](amfActivationGroupAttributeClassMembers.html).

#### Inheritance Hierarchy
<pre>[ASNA.Monarch](amfMonarchNamespace.html)
 **ASNA.Monarch.ActivationGroupAttribute** </pre>

#### Syntax
<pre class="syntax"> **Public class ActivationGroupAttribute Inherits System.Attribute**       </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
The **Job** maintains an ***activation manager*** responsible for handling the activations of programs according to the ActivationGroup custom attribute defined in the <code> **BegClass** </code> of the program. The **ActivationGroup** attribute takes a string as a parameter that can be one of the following:

- *Name* - A user provided name identifying the
        activation group to use for the program. The 
        [
        GroupName](amfActivationGroupAttributeClassGroupNameProperty.html) property will contain this activation
        group name.
- '*Default' - A predefined activation
        group called "*Default". Programs not marked
        with an ActivationGroup attribute are allocated in this
        group. The 
        [
        IsDefault](amfActivationGroupAttributeClassIsDefaultProperty.html) property will be 
 **True** .
- '*New' - This special value indicates
        that the program is to be run in a new activation group.
        Monarch will create a new unique name for the group. The 
        [
        IsNew](amfActivationGroupAttributeClassIsNewProperty.html) property will be 
 **True** .
- '*Caller' - This special value states that
        the program will be allocated in the same activation group
        as the program calling this program. The 
        [
        IsCaller](amfActivationGroupAttributeClassIsCallerProperty.html) property will be 
 **True** .

Instead of using hard-coded string literals for the special values, the **ActivationGroupAttribute** class provides the following three constants:

- ActivationGroupAttribute.Caller (value *Caller)
- ActivationGroupAttribute.Default (value *Default)
- ActivationGroupAttribute.New (value *New)

An example using each of these is shown below:
<pre class="example"> BegClass Custcalc Extends (ASNA.Monarch.Program Access ( *Public ) +
 Attributes (ActivationGroup( ActivationGroupAttribute.Default ))
</pre>
<pre class="example"> BegClass Custcalc Extends (ASNA.Monarch.Program Access ( *Public ) +
 Attributes (ActivationGroup( ActivationGroupAttribute.New ))
</pre>
<pre class="example"> BegClass Custcalc Extends (ASNA.Monarch.Program Access ( *Public ) +
 Attributes (ActivationGroup( ActivationGroupAttribute.Caller ))  
</pre>

Monarch also defines a couple of additional classes for use in the cases of *New and *Caller, these are: [ NewActivationGroupAttribute](amfNewActivationGroupAttributeClass.html) and [ CallerActivationGroupAttribute](amfCallerActivationGroupAttributeClass.html) respectively. 

**Note:** By convention, attribute names end up with the word "Attribute", as in ActivationGroup **Attribute** or CallerActivationGroup **Attribute** . When the attribute class is being referenced in the Attributes keyword, the **Attribute** suffix can be omitted from the name of the attribute. Therefore, the following pairs are equivalent.
<pre class="example"> BegClass Custcalc Attributes (ActivationGroup( "myGroupName" ))
 BegClass Custcalc Attributes (ActivationGroup **Attribute** ( "myGroupName" ))
</pre>
<pre class="example"> BegClass Custcalc Attributes (ActivationGroup( NewActivationGroup ))
 BegClass Custcalc Attributes (ActivationGroup( NewActivationGroup **Attribute** )  
</pre>

The full name must be used when the attribute class is being used in any other context, for instance when referring to one of its properties like **ActivationGroupAttribute.New** .

See [ Monarch Job and Program Concepts](amfconMonarchJobandProgramClasses.html) topic for more information on the relationship and usage of these three classes.
<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
<dl><dt>
        [ASNA.Monarch
      Namespace](amfMonarchNamespace.html)</dt>
        <dt>
        [
      ActivationGroupAttribute Class Members](amfActivationGroupAttributeClassMembers.html) </dt>
		  <dt>[
      Monarch Job and Program Concepts](amfconMonarchJobandProgramClasses.html)</dt>
     <dt>[
      NewActivationGroupAttribute Class](amfNewActivationGroupAttributeClass.html)<br clear="none" />[
      CallerActivationGroupAttribute Class](amfCallerActivationGroupAttributeClass.html)</dt></dl>

