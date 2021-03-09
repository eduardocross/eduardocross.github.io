---
title: CallerActivationGroupAttribute Class

Id: amfCallerActivationGroupAttributeClass
TocParent: amfMonarchNamespaceClasses
TocOrder: 20

keywords: CallerActivationGroupAttribute class, about CallerActivationGroupAttribute class
keywords: classes [ASNA.Monarch], CallerActivationGroupAttribute class
keywords: activation manager, CallerActivationGroupAttribute

---

The <code> **CallerActivationGroupAttribute** </code> is provided to support the job activation manager when a program is to be allocated in the same activation group as the program by which it is called.

For a list of all members of this class, see [Class Members](amfCallerActivationGroupAttributeClassMembers.html).

#### Inheritance Hierarchy
<pre>[ASNA.Monarch](amfMonarchNamespace.html)
 **ASNA.Monarch.CallerActivationGroupAttribute**   </pre>

#### Syntax
<pre class="syntax"> **Public class CallerActivationGroupAttribute Inherits System.Attribute** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
The **Job** maintains an ***activation manager*** responsible for handling the activations of programs according to the ActivationGroup custom attribute defined in the <code> **BegClass** </code> of the program. The following code examples shows a program (<code>Custcalc</code>) that is to be allocated in the same activation group as the program calling this program.
<pre class="example"> BegClass Custcalc Extends (ASNA.Monarch.Program Access ( *Public ) +
 Attributes ( CallerActivationGroup ())</pre>

<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
<dl><dt>
        [ASNA.Monarch
      Namespace](amfMonarchNamespace.html)</dt><dt>
        [
      CallerActivationGroupAttribute Class Members](amfCallerActivationGroupAttributeClassMembers.html) 
     </dt><dt>[
      ActivationGroupAttribute Class](amfActivationGroupAttributeClass.html)</dt><dt>[
      NewActivationGroupAttribute Class](amfNewActivationGroupAttributeClass.html)</dt></dl>

