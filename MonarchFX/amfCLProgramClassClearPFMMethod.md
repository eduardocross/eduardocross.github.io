---
title: CLProgram.ClearPFM Method

Id: amfCLProgramClassClearPFMMethod
TocParent: amfCLProgramClassMethods
TocOrder: 60

keywords: ClearPFM method
keywords: CLProgram.ClearPFM method
keywords: how to, remove data from file member
keywords: physical files, removing data

---

This method removes all data from the specified member of a physical file.

#### Syntax
<pre class="syntax"> **BegSr ClearPFM Access(*Protected) Type(Void)
   DclSrParm *File*  Type(*String)
   DclSrParm *Mbr*  Type(*String)** </pre>

#### Parameters
<dl>
        <dt>
          <code> *File* </code>
        </dt>
        <dd>

String. The qualified name of the physical file containing the member to clear. The name of the physical file can be qualified by one of the following library values:

- <code> ***LIBL** </code>: All libraries in the job's library
            list are searched until the first match is found. This
            is the default.
- *CURLIB: The current library for the
            job is searched. If no library is specified as the
            current library for the job, the QGPL library is
            used.
- <code> *library-name* </code>: Specify the name of the library
            to be searched.
- <code> *physical-file-name* </code>: Specify the name of the
            physical file.

</dd>
        <dt>
          <code> *Mbr* </code>
        </dt>
        <dd>

String. The optional name of the physical file member within the *File* to clear. The name of the member can be:

- <code><u>*FIRST</u></code>: The first member in the database file is
            used. This is the default.
- <code>*LAST</code>: The last member of the
            database file is used.
- <code> *physical-file-member* </code>: Specify the name of the
            physical file member.

</dd>
</dl>

#### Remarks
The following restrictions apply:

- The user must have object operational and object
        management or alter and delete authority for the physical
        file that contains the member; and execute authority for the
        library.
- If any of the access paths to the member are in use
        when this command is entered, or if the physical file
        member is in use, the command is not run.
- An *EXCL lock is required on the member to clear
        it.
- In multi-threaded jobs, this command is not thread safe
        for distributed files. This command is also not thread safe
        and fails for Distributed Data Management (DDM) files of
        type *SNA.

<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
<dl><dt>
        <a shape="rect" href="amfCLProgramClass.htm">CLProgram
        Class</a>
        <br clear="none" />
        <a shape="rect" href="amfCLProgramClassMembers.htm">
        CLProgram Class Members</a>
        <br clear="none" />
        <a shape="rect" href="amfCLProgramClassInitializePFMMethods.htm">
        InitializePFM Methods</a>
        <br clear="none" />
        <a shape="rect" href="amfMonarchNamespace.htm">ASNA.Monarch
        Namespace</a></dt>
</dl>

