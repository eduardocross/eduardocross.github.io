---
title: Command Class

Id: amfCommandClass
TocParent: amfWebDspFASNAMonarchClasses
TocOrder: 10

keywords: Command class, about Command class
keywords: classes [ASNA.Monarch], Command class
keywords: aspx.vr, non-display file, commands
keywords: non-display file aspx.vr, command class
keywords: Web server controls, non-display file aspx.vr commands
keywords: Web server controls [ASNA.Monarch], non-display file aspx.vr command
keywords: MONARCH_CMDPARM

---

The <code> **Command** </code> class is provided to allow code in a non-display file aspx page to invoke functions within a job. Particularly it enables program calls and the return of a job to procedural processing.

For a list of all members of this type, see [Command Members](amfCommandClassMembers.html).
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch Namespace](amfWebDspFASNAMonarchNamespace.html)(ASNA.Monarch.WebDspF.DLL)</pre>

#### Syntax
<pre class="syntax"> **public class Command** </pre>

<!--mine -->

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe. 
<!--mine -->

#### Remarks
The <code>[Call](amfCommandClassCallMethods.html)</code> methods can invoke an interactive or process program. Programs called receive parameters by reference, i.e.: the ASPX code can send and receive data to/from the called program. These parameters are stored in an array of strings. The called program can define its parameters list using fields of type character and decimal (zoned, packed, binary, and decimal).

Interactive calls also require an ASPX page reference where control will be relinquished once the called program finishes execution. Calling interactive programs effectively means a transfer of control, first to the interactive program being called and then to the <code>Callback</code> page reference. Calls that invoke interactive programs can send data into the program via parameters but the output parameter list will be sent to the Callback page by storing the array in the Session under the ["<code>MONARCH_CMDPARM</code>"] key.

[ SetLdaField](amfCommandClassSetLdaFieldMethod.html) and [ GetLdaField](amfCommandClassGetLdaFieldMethod.html) methods are provided to set and return a value portion of the jobs' LDA while the [SetLdcObject](amfCommandClassSetLdcObjectMethod.html), [ GetLdcObject](amfCommandClassGetLdcObjectMethod.html), and [ RemoveLdcObject](amfCommandClassRemoveLdcObjectMethod.html) methods are provided to set, return, or remove an entry from the jobs' LDC. 

The [ RequestShutdown](amfCommandClassRequestShutdownMethod.html) method is used to request a shutdown of the job terminating all active programs in the job. The [ Return](amfCommandClassReturnMethod.html) method returns the job to procedural processing.

The [InvokeQCmdExc](amfCommandClassInvokeQCmdExcMethod.html) method (introduced in 8.0) executes a command on the IBM i's Job associated with the database connection by calling IBM's <code>QCMDEXC</code>.

See [Enhancing Applications using Non-Display File ASPX Pages](amfconEnhancingWithNonDisplayFileASPX.html) topic for more information and examples.
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

<!--mine -->

#### See Also
<dl>
        <dd>[ASNA.Monarch
      Namespace](amfWebDspFASNAMonarchNamespace.html) 
      </dd><dd>[Command
      Class Members](amfCommandClassMembers.html)</dd><dd>[Enhancing
      Applications using Non-Display File ASPX Pages](amfconEnhancingWithNonDisplayFileASPX.html)</dd></dl>

