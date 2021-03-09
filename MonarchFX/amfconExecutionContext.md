---
title: Execution Context Overview

Id: amfconExecutionContext
TocParent: amfASNAMonarchFrameworkConceptsMain
TocOrder: 40

keywords: ASNA Monarch concepts, execution context
keywords: ASNA Monarch concepts, program execution management
keywords: ASNA Monarch concepts, ILE Model
keywords: ASNA Monarch concepts, AVR support
keywords: ASNA Monarch concepts, AVR CALL/CALLB/CALLD/RETURN constructs
keywords: concepts, ASNA.Monarch execution context
keywords: concepts, ASNA.Monarch.Program execution management
keywords: concepts, ASNA.Monarch ILE model
keywords: concepts, ASNA.Monarch AVR support of program execution management
keywords: concepts, ASNA.Monarch AVR CALL/CALLB/CALLD/RETURN constructs
keywords: program execution management, program activation
keywords: program activation in Monarch Framework
keywords: program execution management, program invocation
keywords: program state in Monarch Framework
keywords: execution context, ASNA Monarch
keywords: OS400 concepts, local program call
keywords: OS400 concepts, activate a program
keywords: OS400 concepts, invoke a program
keywords: OS400 concepts, modify storage allocation
keywords: OS400 concepts, deactivate a program
keywords: OS400 concepts, destroy a program invocation

---

To understand the Execution Context provided by the Monarch Framework better, it is useful to first review some IBM i&#174; concepts.
<!-- -->

#### Program Execution Management on the IBM i
The basic functions performed by the PEM on the IBM i are:

- Activates a program: Puts a program into a
        ready-to-execute state.
- Invokes a program: Causes the program to execute.
- Modifies storage allocation: Extends or truncates the
        allocated process automatic storage area, and extends the
        allocated process static storage area.
- Deactivates a program: Removes the program from an
        executable state.
- Destroys a program invocation: Terminates the execution
        of a program.

### Program Activation
All programs executing in the system operate under the control of a Job. The process under which a program is to execute must be established before it can be activated and executed. The primary objective of the activation is to initialize the process's static storage area and initially allocate the areas used. Once a process has been established, PEM can activate a program.

### Program Invocation
The invocation function of PEM controls the synchronous execution of programs within a process. It also allows control to be passed from one program instruction stream to another and allows for a subsequent return of control when a function is complete. The high-level language command to accomplish invocations is <code>CALL</code>.

### Invocation Destruction
When an invoked program relinquishes control, the associated invocation is deallocated and control passes to the calling program. Note too that the program remains active until an explicit deactivation occurs. When the <code>*INLR</code> indicator is <code>*ON</code> in an RPG program whose invocation is to be deallocated, the program's activation entry is also destroyed. The high-level language command used to relinquish control is <code> **RETURN** </code>.

### Call Instruction
The instruction preserves the calling invocation and passes control to the external entry point of the program specified. It also ensures the program is properly activated before the invocation occurs. In a sequence of program calls, while the programs are called, they are both active and invoked. The value of a program's variables, the location of the cursor in each of the files it has opened, and the following instruction to execute is: the **program state** . When a program returns with <code>*INLR</code> set <code>*OFF</code>, the program is considered active but not invoked. Note that should this program be called again, any variables will retain their current value.
<!-- -->

#### ILE Model
With the advent of ILE, RPG introduced new constructs to take advantage of the facilities available in the new (IL) Environment. The most significant from the PEM point of view were activation groups and procedures.

Activation groups enable a programmer to explicitly differentiate the areas where program activations are to be allocated and allow programs to be recursively called. There are 3 basic types of activation groups: explicitly named by the user, statically created by the system (like <code>*DFTACTGRP</code>) and dynamically created by the system to support those programs marked with an activation group of <code> ****NEW*** </code>.

A procedure allows better control over the main entry point of a program while sub-procedures provide a modern alternative to subroutines. One of the main advantages of procedures and sub-procedures is the finer control of the parameters being passed, particularly the ability to omit parameters via <code>*OMIT</code> and to not pass them at all.

The op-code <code> **CALLB** (CALL BOUND)</code> was introduced to support procedures. <code>CALLB</code> resolves the procedure to be called at program creation time, whereas <code> **CALL** </code> resolves the program at runtime.

### ASNA Visual RPG support of PEM
AVR draws its heritage from the implementations of RPG under IBM i but also strives to participate within the .NET framework. In IBM i, the <code> **CALL/RETURN** </code> instructions were supported by all major programming languages and it was the preferred mechanism by which most applications were segmented into manageable / reusable portions. Most applications depend upon two programming languages, CL and COBOL or CL and RPG. However, few utilize more than two languages.

The .NET framework does not directly support the concept of a *program* (as understood in the IBM i world), therefore there is no direct support in .NET for the semantics required to implement <code>CALL/RETURN</code>.

In .NET, applications are partitioned using the concept of a Class. A class defines the operations an object can perform (methods, events, or properties) and defines a value that holds the state of the object (fields). An instance of a class is an object. You access an object's functionality by calling its methods and accessing its properties, events, and fields. There are certain kinds of methods and fields that are shared across all object instances of a class. These fields and methods are "shared" (or "static" in languages like C++ and C#). To access shared methods, all that is needed is the name of the class and not an actual instance of it.

### AVR Procedures
AVR 8.0 introduced procedures into the language to facilitate the migration of RPG applications via Monarch. AVR Procedures are similar to AVR functions but have the following differences:

- Are invoked via or in an expression.
- Can have absent and omitted parameters.
- May cause a new activation of the containing class
        (program).

A class may contain a special procedure named <code>* **ENTRY** </code>. This procedure acts as the default entry point of a class when the class name is used as the target of a <code> **CALLB** </code>. The parameters of <code>*ENTRY</code> are also different. They are just references to global fields defined at the class (program) level and as such, the <code> **DclSrParm** </code> commands may not have type keywords. When a <code>* **ENTRY** </code> procedure is invoked, the parameters passed to it are copied to (or referred by) the global fields.

The implementation of Procedures by AVR has no direct implementation of activations. Instead, AVR relies on the user providing an activation manager via a static member of the runtime support. Monarch sets up this manager, as we will see later.

As part of the preamble generated by the compiler when expanding the code for a procedure, AVR invokes the activation manager to obtain the proper activation for the program and sets up exception handling routines to trap the **ASNA.VisualRPG.Runtime.Return** exception (see below).

### Visual RPG <code>CALL/CALLB/CALLD/RETURN</code> Constructs
Because .NET does not provide the support for jobs, programs, and activation groups, and because AVR must remain nimble to play well with the rest of the .NET framework and languages, its implementations of <code> **CALL** , **CALLB** , **CALLD** </code>, and <code> **RETURN** </code> are very simple, leaving the burden of providing the same semantics as IBM i to the user. In the case of Monarch applications, the Monarch Framework assumes you will take this responsibility. Let us examine what tools AVR provides.

AVR implementation of allows the calling of a remote program. The <code> **CALLB** </code> opcode can be used to call a procedure defined in the same class or a *public* procedure in a different class.

<code> **CALLD** </code> on the other hand, supports a call to a local Monarch Program on the same assembly, on a different assembly, or even if the assembly does not yet exist. This conveniently allows compilation of programs that reference other programs that are not compiled yet. This feature is invaluable when migrating large applications where local program calls in separate assemblies can be compiled successfully, even before the application is fully tested. This replicates the development cycle on the IBM i and makes AVR a unique language in that no other languages available for .NET allow dynamic referencing of assemblies without adding advanced reflection support by the user.

The implementation that AVR provides for the <code> **RETURN** </code> op-code is also very primitive. It simply throws the exception **ASNA.VisualRPG.Runtime.Return** .

#### Next: [Control Execution Lifecycle](amfconControlExecutionLifecycle.html)

#### Previous: [Introduction](amfconIntroductionMain.html)

#### See Also
<dl><dd>[What's New](amfWhatsNewin72.html)</dd>
        <dd>[Reference
        Library](amfReferenceMain.html)</dd>
</dl>

