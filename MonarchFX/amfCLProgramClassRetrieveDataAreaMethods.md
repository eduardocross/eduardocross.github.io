---
title: CLProgram.RetrieveDataArea Methods

Id: amfCLProgramClassRetrieveDataAreaMethods
TocParent: amfCLProgramClassMethods
TocOrder: 110

keywords: CLProgram.RetrieveDataArea methods
keywords: RetrieveDataArea methods
keywords: how to, retrieve local data area
keywords: how to, retrieve part of local data area
keywords: local data areas, retrieving
keywords: lda, retrieving
keywords: LDA, retrieving

---

A local data area is created for each job in the system. The system creates a local data area, which is initially filled with blanks, with a length of 1024 and type <code>*CHAR</code>. When you submit a job, the value of the submitting job's local data area is copied into the submitted job's local data area. You can use this local data area to pass information to a procedure or program without the use of a parameter list. <code> **RetrieveDataArea** </code> allows for the retrieval of all or a portion of a local data area.

#### Overloaded List
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <th>Syntax</th>
            <th>Description</th>
          </tr>
          <tr>
            <td>            <code>[
              RetrieveDataArea (
 *string* )](amfCLProgramClassRetrieveDataAreaMethod1.html)</code>
            </td>
            <td>Retrieves the path to the local *data area*  named.</td>
          </tr>
          <tr>
            <td>             <code>[
              RetrieveDataArea (
 *string, integer, integer* )](amfCLProgramClassRetrieveDataAreaMethod2.html)</code>
            </td>
            <td>Retrieves the path to the partial
            contents of the local 
           <code> *dataArea* </code> at the 
            <code> *start* </code> position and for the 
            <code> *length* </code> specified.</td>
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
