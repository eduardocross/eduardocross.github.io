---
title: CLProgram.AddPFM Method

Id: amfCLProgramClassAddPFMMethod
TocParent: amfCLProgramClassMethods
TocOrder: 20

keywords: AddPFM method
keywords: CLProgram.AddPFM method
keywords: how to, add physical file member
keywords: physical files, adding members

---

This method add the specified member of a physical file.

#### Syntax
<pre class="syntax"> **BegSr AddPFM Access(*Protected) Type(Void)
   DclSrParm *File*  Type(*String)
   DclSrParm *Mbr*  Type(*String)
   DclSrParm *Text*  Type(*String)**       </pre>

#### Parameters
<dl>
        <dt>
          <code> *File* </code>
        </dt>
        <dd>

String. The qualified name of the physical file containing the member to add. The name of the physical file can be qualified by one of the following library values:

- <code><u>*LIBL</u></code>: All libraries in the job's library
            list are searched until the first match is found. This
            is the default.
- <code>*CURLIB</code>: The current library for the
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

String. The optional name of the physical file member within the *File* to add. The name of the member can be:

- <code><u>*FIRST</u></code>: The first member in the database file is
            used. This is the default.
- <code>*LAST</code>: The last member of the
            database file is used.
- <code> *physical-file-member* </code>: Specify the name of the
            physical file member.

</dd>
        <dt>
          <code> *Text* </code>
        </dt>
        <dd>

String. The text associated with the file.
</dd>
</dl>

#### Remarks
The following restrictions apply:

- The user must have object operational, object
        management or alter, and delete authority for the physical
        file that contains the member and execute authority to the
        library.
- If any of the access paths to the member are in use
        when this command is entered, or if the physical file
        member is in use, the command is not run.
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
[CLProgram Class](amfCLProgramClass.html) <br clear="none" /> [ CLProgram Class Members](amfCLProgramClassMembers.html) <br clear="none" /> [ InitializePFM Methods](amfCLProgramClassInitializePFMMethods.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
