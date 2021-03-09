---
title: WebDisplayFile.FeedbackCursor Property

Id: amfWebDisplayFileClassFeedbackCursorProperty
TocParent: amfWebDisplayFileClassProperties
TocOrder: 50

keywords: FeedbackCursor property
keywords: WebDisplayFile.FeedbackCursor property
keywords: feedback, cursor cooridinates to provide feedback for field in display file
keywords: cursor cooridinates to provide feedback for field in display file
keywords: display files, cursor cooridinates to provide feedback for field
keywords: how to, set cursor cooridinates to provide feedback for field in display file
keywords: how to, return cursor cooridinates to provide feedback for field in display file

---

Location of the Cursor corresponding to the last non-subfile input operation (returning data to the program). It is a single two-byte value, where the MSB (most significant byte) contains the legacy row and the LSB (least significant byte) contains the legacy column. If a Window (popup) is active, the location is the absolute location with respect to the legacy screen.

#### Syntax
<pre class="prettyprint"> **BegProp FeedbackCursor Access(*Public) Type(*Short)
   BegGet;  BegSet** </pre>

#### Property Values
**Short** . The cursor coordinates.
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
            <td>Windows Server 2008 R2, Windows Server 2012,  Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ WebDisplayFile Class](amfWebDisplayFileClass.html) <br /> [ WebDisplayFile Class Members](amfWebDisplayFileClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html)
