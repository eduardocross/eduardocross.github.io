---
title: Job Class

Id: amfJobClass
TocParent: amfMonarchNamespaceClasses
TocOrder: 60

keywords: ActivationGroupCallException
keywords: ActivationGroupCreateException
keywords: ActivationGroupDisposeException
keywords: RecursiveCallException
keywords: Job class, about Job class
keywords: classes [ASNA.Monarch], Job class
keywords: ASNA.Monarch.Job class
keywords: jobs, about

---

The **Job** class provides an environment to submit, control, and keep track of program activations.

For a list of all members of this type, see [Job Members](amfJobMembers.html).
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch](amfMonarchNamespace.html)
 **ASNA.Monarch.Job** </pre>

<!--mine -->

#### Syntax
<pre class="prettyprint"> **Public class Job** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
There is a Monarch Job associated with each user in an ASP.Net application. Actually, there is a job with each session kept by ASP.Net. As part of the session startup, a new job is created, a thread is allocated, and the Job is started in this thread.

**Invocations / Activations** 

- The 
        [
        EndPrograms](amfJobClassEndProgramsMethod.html) method de-activates any program that is
        still active and then the 
        [
        Dispose](amfJobClassDisposeMethod.html) method is used to release resource. The 
        [
        ShutDown](amfJobClassShutDownMethod.html) method terminates the entire session.  The

 **Job**  also maintains an 
 ***activation manager***  responsible for handling the activations of programs
        according to the 
        [
        ActivationGroup](amfActivationGroupAttributeClass.html) custom attribute define in the 
 **BegClass**  of the program.

**Database Files, File Overrides, and Message Queues** 

- The 
        [
        getDatabase](amfJobClassgetDatabaseMethod.html) method establishes the database connection.
        The 
        [
        Database](amfJobClassDatabaseProperty.html) property is used to get the database associated
        with the job.
- You can use an override command to replace the database
        file named in a program or to change certain parameters of
        the existing database files. These overrides can be applied
        to DBFile, PrintFile, or a WorkStnFile object. When you
        override to a different file (ToFile), the overriding file
        must have only one record format. A logical file, which has
        multiple record formats defined in DDS, may be used if it
        is defined over only one physical file member. A logical
        file, which has only one record format defined in the DDS
        may be defined over more than one physical file member. The
        name of the format does not have to be the same as the
        format name referred to when the program was created. You
        should ensure that the format of the data in the overriding
        file is the same as in the original file; otherwise, you
        may get unexpected results. 
        [
        OverrideFile](amfJobClassOverrideFileMethods.html) is an overloaded method that provides file
        overrides with several parameters options. The 
        [
        DeleteOverride](amfJobClassDeleteOverrideMethods.html) overloaded method is used to remove
        database file overrides previously applied.
- A message is a communication sent from one user,
        program, or procedure to another. There are two types of
        messages; Immediate and Predefined. Immediate messages are
        created by the program or system user when they are sent
        and are not permanently stored in the system. Predefined
        messages are created before they are used. These messages
        are placed in a 
 **message file** (
        [
        MesssageFileFolder](amfJobClassMessageFileFolderProperty.html)) when they are created, and
        retrieved from that file when they are used. Messages are
        sent to and received from 
 **message queues** , which are separate objects
        on the system. When a message is sent to a procedure, a
        program, or a system user, it is placed on a message queue
        associated with that procedure, program, or user. The
        procedure, program, or user sees the message by receiving
        it from the queue. A message sent to a queue can remain on
        the queue until it is explicitly received by a program or
        workstation user. Additional fields in support of message
        files and message queue are 
        [
        ExternalQueue](amfJobClassExternalQueueField.html) and 
        [
        messageFileFolder](amfJobClassmessageFileFolderField.html).

**Job / Program Status** 

- The 
        [
        CurrentJob](amfJobClassCurrentJobProperty.html) property returns the name of the current
        active job and the 
        [
        StartupMoment](amfJobClassStartupMomentProperty.html) property returns the 
 **System.DateTime**  the job was started.
- A program status data structure (PSDS) can be defined
        to make program exception/error information available to a
        program. There is only one PSDS per module. 
        [
        PsdsJobName](amfJobClassPsdsJobNameField.html), 
        [
        PsdsJobNumber](amfJobClassPsdsJobNumberField.html), and 
        [
        PsdsJobUser](amfJobClassPsdsJobUserField.html) fields set or return the job name, job
        number, or user name, respectively.

**Job Attributes and Variables** 

- Associated with each job on the IBM i there is a set
        of properties or attributes. These attributes can be
        programmatically accessed in CL via the RTVJOBA commands.
        One of these attributes is a series of 8 switches that can
        be 'on' or 'off'. RPG programs also have access to these
        switches via the *INUx indicators. In order to support
        applications using these switches, this class provides a
        set of methods to access the 8 values. These are 
        [
        GetSwitch](amfJobClassGetSwitchMethod.html), 
        [
        GetSwitches](amfJobClassGetSwitchesMethod.html), and 
        [
        SetSwitch](amfJobClassSetSwitchMethod.html).

#### Exceptions
The following exceptions may be encountered by the *activation manager* .
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
              <colgroup>
                <col width="50%" />
                <col width="50%" />
              </colgroup>
              <tr>
                <th>Value</th>
                <th>Condition</th>
              </tr>
              <tr>
                <td>ActivationGroupCallException</td>
                <td>Attempted to call a program
            with *CALLER activation group from a class.</td>
              </tr>
              <tr>
                <td>ActivationGroupCreateException</td>
                <td>Could not create activation
            group.</td>
              </tr>
              <tr>
                <td>ActivationGroupDisposeException</td>
                <td>Could not dispose of
            activation group.</td>
              </tr>
              <tr>
                <td>RecursiveCallException</td>
                <td>A recursive call in an
            activation group has been attempted.</td>
              </tr>
</table>

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
              <colgroup>
                <col width="15%" style="font-weight:bold" />
                <col width="85%" />
              </colgroup>
              <tr>
                <td>Namespace:</td>
                <td>
                  [ASNA.Monarch](amfMonarchNamespace.html)
                </td>
              </tr>
              <tr>
                <td>Assembly:</td>
                <td>ASNA.VisualRPG.Runtime.</td>
              </tr>
              <tr>
                <td>Platforms:</td>
                <td>Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
              </tr>
</table>

#### See Also
<dl>
            <dd>
              <a shape="rect" href="amfJobMembers.htm">Job Members</a>
            </dd>
            <dd>
              <a shape="rect" href="amfWebJobClass.htm">WebJob Class</a>
            </dd>
            <dd>
              <a shape="rect" href="amfMonarchNamespace.htm">ASNA.Monarch
        Namespace</a>
            </dd>
</dl>

