---
title: Program.SqlCursor.ScrollTypes Enumeration

Id: amfProgramSqlCursorScrollTypesEnumeration
TocParent: amfMonarchNamespaceEnumerations
TocOrder: 70

keywords: enumerations [ASNA.Monarch], Program.SqlCursor.ScrollTypes
keywords: Program.SqlCursor.ScrollTypes enumeration
keywords: Dynamic enumeration member
keywords: NonScrollable enumeration member
keywords: Scrollable enumeration member
keywords: SQL, cursor scroll type
keywords: SQL cursor, scroll type

---

The **ScrollTypes** enumerated constant defines values for the type of scrolling allowed for [ SqlCursor](amfProgramSqlCursorClass.html).

#### Syntax
<pre class="syntax"> **BegEnum ScrollTypes Access(*Public)**       </pre>

#### Remarks
**ScrollTypes** denote values that define the type of scrolling for SQL cursor.
<!--mine -->

#### Enumerators
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="15%" />
            <col width="80%" />
            <col width="5%" align="center"/>
          </colgroup>
          <tr>
            <th>Member</th>
            <th>Description</th>
            <th>Value</th>
          </tr>
          <tr>
            <td>NonScrollable</td>
            <td>NonScrollable cursor in that
          only the 'next' fetch operation is allowed.</td>
            <td>0</td>
          </tr>
          <tr>
            <td>Scrollable</td>
            <td>Rows can be randomly fetched
          from anywhere in the cursor.</td>
            <td>1</td>
          </tr>
          <tr>
            <td>Dynamic</td>
            <td>Dynamic cursor movement is
          allowed.</td>
            <td>2</td>
          </tr>
</table>

<!-- -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td>[ASNA.Monarch](amfMonarchNamespace.html)</td>
          </tr>
          <tr>
            <td>Assembly:</td>
            <td>ASNA.VisualRPG.Runtime.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
<dl><dd>[
    Program.SqlCursor Class](amfProgramSqlCursorClass.html)</dd><dd>[ASNA.Monarch
    Namespace](amfMonarchNamespace.html)</dd></dl>

