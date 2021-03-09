---
title: DdsSubfileControl.ProgramQLen Property

Id: amfddsSubfileControlClassProgramQLenProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 70

keywords: ProgramQLen property
keywords: DdsSubfileControl.ProgramQLen property
keywords: program queues, property length
keywords: how to, set program queue property length
keywords: how to, get program queue property length
keywords: subfiles, setting program queue property length
keywords: subfiles, getting program queue property length
keywords: subfile records, setting program queue property length
keywords: subfile records, getting program queue property length

---

Gets or sets the length of the [ ProgramQ](amfddsSubfileControlClassProgramQProperty.html) property field.

#### Syntax
<pre class="prettyprint">
 **BegProp ProgramQLen Access(*Public) Type(*Integer)
   BegGet;  BegSet** 
            </pre>

#### Property Values
Integer. The length of the field specified by the **ProgramQ** property.

#### Remarks
The values you can use for ProgramQLen are:

- **10 (Default)** - Generates a 10-byte
        character field - *Char(10).
- 276 - Generates a 276-byte character field -
        *Char(276).
- 0 - Use for String fields - *String.

To set this property at design-time, click on the right of the **ProgramQLen** property and the length.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ProgramQ Property](amfddsSubfileControlClassProgramQProperty.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
