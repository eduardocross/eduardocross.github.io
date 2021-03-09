---
title: Multimember File Migration

Id: amfConMultimemberSupport
TocParent: amfconSQLStatementExamples
TocOrder: 200

keywords: Members
keywords: Multimember files
keywords: Single member files
keywords: Multimember physical files
keywords: Single member physial files
keywords: Multimember logical files
keywords: Single member logical files

---

### Multimember Files in Monarch
Prior to 8.0, Monarch only supported the migration of Physical and logical files with zero to one member into SQL; with 8.0 Monarch gained the ability to migrate Physical and logical files with any number of members. Monarch handles these two file types differently, although with similar ease.

#### Single Member Physical Files
Single member files include those with a maximum member value of zeroe or one; both are handled the same way:

Monarch migrates the file to a table that shares the name of the file. The member, if present, will already have the same name as the file.

The member of a single member file cannot be renamed or deleted without doing the same to the file, and no new members can be added to the file.

This applies to both migrated files and files created through DataGate.

#### Multimember Physical Files
Multimember files (any file with a maximum member value greater than one) are handled by creating a table that represents the file, and which shares the name of the file. <br /> An additional table is created for each member using the naming convention <code> *FileName* # *MemberName* </code>. Each table contains the data from one member.

Changing the name of the File-table will change the *FileName* portion of the names of eaxh associated Member-table. Members can be freely added, deleted, and renamed (so long as they retain the *FileName* suffix.

This applies to both migrated files and files created through DataGate.

#### Single Member Logical Files
Single member files include those with a maximum member value of zeroe or one; both are handled the same way:

Monarch migrates the file to a table that shares the name of the file. The member, if present, will already have the same name as the file.

The member of a single member file cannot be renamed or deleted without doing the same to the file, and no new members can be added to the file.

This applies to both migrated files and files created through DataGate.

#### Multimember Logical Files
Multimember files (any file with a maximum member value greater than one) are handled by creating a view that represents the file, and which shares the name of the file. <br /> An additional view is created for each member using the naming convention <code> *FileName* # *MemberName* </code>. Each view contains the data from one member.

Changing the name of the File-view will change the *FileName* portion of the names of eaxh associated Member-view. Members can be freely added, deleted, and renamed (so long as they retain the *FileName* suffix.

This applies to both migrated files and files created through DataGate.

#### See Also
<dl>
       <dd>[Reference
        Library](amfReferenceMain.html)</dd>
       <dd>[WebDspf.Page Class](amfPageClass.html)</dd>
       <dd>[Page Class Methods](amfPageClassMethodsMain.html)</dd>
</dl>

