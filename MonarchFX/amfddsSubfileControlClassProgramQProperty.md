---
title: DdsSubfileControl.ProgramQ Property

Id: amfddsSubfileControlClassProgramQProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 60

keywords: ProgramQ property
keywords: DdsSubfileControl.ProgramQ property
keywords: program queues, field name
keywords: how to, set program queue field name
keywords: how to, get program queue field name
keywords: subfiles, setting program queue field name
keywords: subfiles, getting program queue field name
keywords: subfile records, setting program queue field name
keywords: subfile records, getting program queue field name
keywords: _Star_PGM
keywords: SFLPGMQ

---

Gets or sets the name of the field containing the name of the program queue used to build a message subfile (SFLPGMQ).

#### Syntax
<pre class="prettyprint"> **BegProp ProgramQ Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. The name of the field containing the name of the program queue used to build a message subfile.

#### Remarks
The **ProgramQ** property works similar to the **SFLPGMQ** keyword to specify the name of the field containing the name of the program queue used to build a message subfile.

You can specify either the name of the field that contains the message subfile queue, or the special value ***PGM** , which specifies to use the message queue of the program issuing the output operation.

The first field in the subfile record format is used for the Message subfile. This field contains the name of the program message queue used by the program to build a message subfile. In addition, ProgramQ can be specified on the record format when the [ InitializeRecords](amfddsSubfileControlClassInitializeRecordsProperty.html) property is enabled.

The length of this field is specified by the [ ProgramQLen](amfddsSubfileControlClassProgramQLenProperty.html) property, which has a default length of 10 generating a 10-byte character field. See **ProgramQLen** property for more information.

When you specify a field name in the **ProgramQ** property, and also enable the **InitializeRecords** property, the Message Subfile is initialized with all the messages that are in the program message queue for the name or current program (*PGM) specified in the **ProgramQ** property.

The **ProgramQ** field can also contain the special value ***PGM** instead of a program message queue name. ***PGM** indicates to use the message queue of the program issuing the output operation.

To set this property at design-time, click on the right of the **ProgramQ** property and enter the indicator expression.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ InitializeRecords Property](amfddsSubfileControlClassInitializeRecordsProperty.html) <br /> [ ProgramQLen Property](amfddsSubfileControlClassProgramQLenProperty.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
