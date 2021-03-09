---
title: CLProgram.FileExists Method

Id: amfCLProgramClassFileExistsMethod
TocParent: amfCLProgramClassMethods
TocOrder: 120

keywords: FileExists method
keywords: CLProgram.FileExists method
keywords: how to, determine if file exists
keywords: files, existing
keywords: existing files

---

Returns **True** if a file exists, otherwise it returns **False** .

#### Syntax
<pre class="syntax"> **BegFunc FileExists Access(*Protected) Type(*Boolean)
   DclSrParm *FilePath*  Type (*String)**       </pre>

#### Parameters
<dl>
        <dt>
          <code> *FilePath* </code>
        </dt>
        <dd>

String. The library and file name of the file to be checked.
</dd>
</dl>

#### Return Value
Boolean. **True** if the file exists, otherwise **False** .
<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->     

#### See Also
[CLProgram Class](amfCLProgramClass.html) <br clear="none" /> [ CLProgram Class Members](amfCLProgramClassMembers.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
