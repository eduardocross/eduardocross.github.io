---
title: CLProgram.OverrideFile Methods

Id: amfCLProgramClassOverrideFileMethods
TocParent: amfCLProgramClassMethods
TocOrder: 140

keywords: OverrideFile methods
keywords: CLProgram.OverrideFile methods
keywords: setting CL program overrides
keywords: setting procedure overrides
keywords: setting job overrides
keywords: setting database file overrides
keywords: setting workstation file overrides
keywords: setting print file overrides
keywords: how to, set CL program overrides
keywords: how to, set procedure overrides
keywords: how to, set job overrides
keywords: how to, set database file overrides
keywords: how to, set print file overrides
keywords: how to, set workstation file overrides
keywords: procedure overrides, setting
keywords: CL program overrides, setting
keywords: job overrides, setting
keywords: database files, setting overrides
keywords: workstation files, setting overrides
keywords: print files, setting overrides
keywords: overrides, setting for CL programs
keywords: overrides, setting for procedures
keywords: overrides, setting for jobs

---

This overloaded method provides CLProgram file override options. 

You can use an override command to replace the database file named in a CL procedure or program or to change certain parameters of the existing database file. These overrides can be applied to DBFile, PrintFile, or a WorkStnFile file. This may be especially useful for files that have been renamed or moved since the procedure or program was created. It can also be used to access a file member other than the first member. 

When you override to a different file(ToFile), the overriding file must have only one record format. A logical file, which has multiple record formats defined in DDS, may be used if it is defined over only one physical file member. A logical file, which has only one record format defined in the DDS, may be defined over more than one physical file member. The name of the format does not have to be the same as the format name referred to when the program was created. 

You should ensure that the format of the data in the overriding file is the same as in the original file, otherwise you may get unexpected results.

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
            <td>           <code>[
              OverrideFile (
 *string, OverrideOptions, object* )](amfCLProgramClassOverrideFileMethod1.html)</code>
            </td>
            <td>Overrides a 
 *CL procedure, program,
            or file*  for the 
 *option*  specified with a 
 *new value*  that is provided.</td>
          </tr>
          <tr>
            <td>              <code>[
              OverrideFile (
 *string, OverrideOptions, object,
              OverrideScope* )](amfCLProgramClassOverrideFileMethod2.html)</code>
            </td>
            <td>Overrides a 
 *CL procedure, program,
            or file*  for the 
 *option*  specified with a 
 *new value*  that is provided for the 
 *scope*  indicated (call level or job level).</td>
          </tr>
</table>

<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->      

#### See Also
[CLProgram Class](amfCLProgramClass.html) <br clear="none" /> [ CLProgram Members](amfCLProgramClassMembers.html) <br clear="none" /> [ ASNA.Monarch.OverrideOptions](amfOverrideOptionsEnumeration.html) <br clear="none" /> [ ASNA.Monarch.OverrideScope](amfOverrideScopeEnumeration.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
