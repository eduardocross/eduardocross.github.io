---
title: CLProgram.CreateDuplicateFile Method

Id: amfCLProgramClassCreateDuplicateFileMethod
TocParent: amfCLProgramClassMethods
TocOrder: 80

keywords: CreateDuplicateFile method
keywords: CLProgram.CreateDuplicateFile method
keywords: how to, create duplicate file
keywords: how to, create duplicate file definition only
keywords: files, creating duplicate
keywords: files, creating definition only
keywords: physical files, creating duplicate
keywords: physical files, creating definition only

---

Creates a duplicate file.

#### Syntax
<pre class="syntax"> **BegSr CreateDuplicateFile Access(*Protected) Type(Void)
   DclSrParm *FromLibrary*  Type (*String)
   DclSrParm *FileName*     Type (*String)
   DclSrParm *ToLibrary*    Type (*String)
   DclSrParm *NewName*      Type (*String)
   DclSrParm *CopyData*     Type (*Boolean)**       </pre>

#### Parameters
<dl>
        <dt>
          <code> *FromLibrary* </code>
        </dt>
        <dd>

String. The library from which the file will be copied. (May be specified as *LIBL)
</dd>
        <dt>
          <code> *FileName* </code>
        </dt>
        <dd>

String. The file name of the file to be copied.
</dd>
        <dt>
          <code> *ToLibrary* </code>
        </dt>
        <dd>

String. The library to which the file will be copied.
</dd>
        <dt>
          <code> *NewName* </code>
        </dt>
        <dd>

String. The new file name to give to the file being copied.
</dd>
        <dt>
          <code> *CopyData* </code>
        </dt>
        <dd>

Boolean. **True** if the data is to be copied, otherwise **False** to indicate just the file definition is copied.
</dd>
</dl>

<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
<dl><dt>
        [CLProgram
        Class](amfCLProgramClass.html)
        <br clear="none" />
        [
        CLProgram Class Members](amfCLProgramClassMembers.html)
        <br clear="none" />
        [ASNA.Monarch
        Namespace](amfMonarchNamespace.html)
      </dt></dl>

