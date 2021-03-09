---
title: CLProgram.InitializePFM Methods

Id: amfCLProgramClassInitializePFMMethods
TocParent: amfCLProgramClassMethods
TocOrder: 130

keywords: CLProgram.InitializePFM methods
keywords: InitializePFM methods
keywords: how to, initialize records in physical file
keywords: physical files, initializing records in
keywords: records, initializing in physical file
keywords: initializing records

---

Initializes records in a member of a physical file. As many records are added as is necessary to make the total record count specified.
<!-- start constructor table -->	

#### Overloaded List
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="50%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <th>Syntax</th>
            <th>Description</th>
          </tr>
<!-- end copy BUT put in extra div and end of table -->

          <tr>
            <td>              <code>[
              InitializePFM (
 *string, string, InitializePFMOptions,
              integer* )](amfCLProgramClassInitializePFMMethod1.html)</code>
            </td>
            <td>Initializes records
            in the 
 *physical file*  and 
 *member*  specified to make the total number
            of records indicated.  The 
 *initialize options*  specifies how the new
            records are initialized.</td>
          </tr>
          <tr>
            <td>              <code>[
              InitializePFM (
 *string, string, integer* )](amfCLProgramClassInitializePFMMethod2.html)</code>
            </td>
            <td>Initializes records
            in the 
 *physical file*  and 
 *member*  specified to make the total number
            of records indicated.  New records are initialized
            with default values.</td>
          </tr>
</table>

<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[CLProgram Class](amfCLProgramClass.html) <br clear="none" /> [ CLProgram Class Members](amfCLProgramClassMembers.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
