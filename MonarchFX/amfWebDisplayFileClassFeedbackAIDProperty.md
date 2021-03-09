---
title: WebDisplayFile.FeedbackAID Property

Id: amfWebDisplayFileClassFeedbackAIDProperty
TocParent: amfWebDisplayFileClassProperties
TocOrder: 40

keywords: FeedbackAID property
keywords: WebDisplayFile.FeedbackAID property
keywords: AidKeyIBM enumeration, used by
keywords: enumerations [ASNA.Monarch.WebDspF], AidKeyIBM, used by
keywords: aid keys, to provide feedback for field in display file
keywords: feedback, Aid key to provide feedback for field in display file
keywords: aid key to provide feedback for field in display file
keywords: display files, aid key to provide feedback for field
keywords: how to, set aid key to provide feedback for field in display file
keywords: how to, return aid key to provide feedback for field in display file

---

Gets or sets the feedback AID key used to provide feedback for a specific field on the web form.

#### Syntax
<pre class="prettyprint"> **BegProp FeedbackAID Access(*Public) Type(*Byte)
   BegGet;  BegSet** </pre>

#### Property Values
**Byte** . See [ AidKeyIBM](amfAidKeyIBMEnumeration.html) enumeration for a list of valid values. Please note that this value must be converted from/to Type *Byte. The hexadecimal values for the enumeration values are noted within the enumeration table.
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
            <td style="height: 27px">Assembly:</td>
            <td style="height: 27px">ASNA.VisualRPG.Runtime.DLL</td>
          </tr>
         <tr>
            <td style="height: 46px">Platforms:</td>
            <td style="height: 46px">Windows Server 2008 R2, Windows Server 2012,  Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ WebDisplayFile Class](amfWebDisplayFileClass.html) <br /> [ WebDisplayFile Class Members](amfWebDisplayFileClassMembers.html) <br /> [ AidKeyIBM Enumeration](amfAidKeyIBMEnumeration.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html)
