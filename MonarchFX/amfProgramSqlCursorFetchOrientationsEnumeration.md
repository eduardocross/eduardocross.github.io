---
title: Program.SqlCursor.FetchOrientations Enumeration

Id: amfProgramSqlCursorFetchOrientationsEnumeration
TocParent: amfMonarchNamespaceEnumerations
TocOrder: 60

keywords: enumerations [ASNA.Monarch], Program.SqlCursor.FetchOrientations
keywords: Program.SqlCursor.FetchOrientations enumeration
keywords: After enumeration member
keywords: Before enumeration member
keywords: Current enumeration member
keywords: First enumeration member
keywords: Last enumeration member
keywords: Next enumeration member
keywords: Prior enumeration member
keywords: Relative enumeration member
keywords: SQL cursor, fetch orientation
keywords: SQL, cursor fetch orientation

keywords: First
keywords: Last
keywords: Next
keywords: Prior
keywords: Relative

keywords: FetchOrientations.First
keywords: FetchOrientations.Last
keywords: FetchOrientations.Next
keywords: FetchOrientations.Prior
keywords: FetchOrientations.Relative

keywords: SqlCursor.FetchOrientations.First
keywords: SqlCursor.FetchOrientations.Last
keywords: SqlCursor.FetchOrientations.Next
keywords: SqlCursor.FetchOrientations.Prior
keywords: SqlCursor.FetchOrientations.Relative

keywords: Program.SqlCursor.FetchOrientations.First
keywords: Program.SqlCursor.FetchOrientations.Last
keywords: Program.SqlCursor.FetchOrientations.Next
keywords: Program.SqlCursor.FetchOrientations.Prior
keywords: Program.SqlCursor.FetchOrientations.Relative

keywords: ASNA.Monarch.Program.SqlCursor.FetchOrientations.First
keywords: ASNA.Monarch.Program.SqlCursor.FetchOrientations.Last
keywords: ASNA.Monarch.Program.SqlCursor.FetchOrientations.Next
keywords: ASNA.Monarch.Program.SqlCursor.FetchOrientations.Prior
keywords: ASNA.Monarch.Program.SqlCursor.FetchOrientations.Relative

---

The **FetchOrientations** enumerated constant defines values for the fetch orientation of [ SqlCursor](amfProgramSqlCursorClass.html).

#### Syntax
<pre class="syntax"> **BegEnum FetchOrientations Access(*Public)** </pre>

#### Remarks
**FetchOrientations** denote values that define the movement when a fetch is issued against the SQL cursor.
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
            <td>Next</td>
            <td>Positions the SqlCursor
          to the reset set row immediately following the current
          cursor position. This is the default.</td>
            <td>0</td>
          </tr>
          <tr>
            <td>Prior</td>
            <td>Positions the SqlCursor
          to the result set row immediately preceding the
          current cursor position.</td>
            <td>1</td>
          </tr>
          <tr>
            <td>First</td>
            <td>Positions the SqlCursor to
          the first row of the result set.</td>
            <td>2</td>
          </tr>
          <tr>
            <td>Last</td>
            <td>Positions the SqlCursor to
          the last row of the result set.</td>
            <td>3</td>
          </tr>
          <tr>
            <td>Before</td>
            <td>Positions the SqlCursor
          before the first row of the result set.</td>
            <td>4</td>
          </tr>
          <tr>
            <td>After</td>
            <td>Positions the SqlCursor after
          the first row of the result set.</td>
            <td>5</td>
          </tr>
          <tr>
            <td>Current</td>
            <td>Maintains the current
          SqlCursor position.  An error will be returned if
          the ScrollType is Dynamic and the current row has been
          updated so its place within the sort order of the result
          set is changed.</td>
            <td>6</td>
          </tr>
          <tr>
            <td>Relative</td>
            <td>If the 
 *variable*  is greater than 0, Relative
          positions the SqlCursor 
 *n*  rows 
 **after**  the current row. If the 
 *variable*  is less than 0, Relative positions
          the SqlCursor 
 *n*  rows 
 **before**  the current row.</td>
            <td>7</td>
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

