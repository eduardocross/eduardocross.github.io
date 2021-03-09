---
title: DdsCharField.AutoCapitalize Property

Id: amfDdsCharFieldClassAutoCapitalizeProperty
TocParent: amfDdsCharFieldClassPropertiesMain
TocOrder: 07

keywords: AutoCapitalize property
keywords: DdsCharField.AutoCapitalize property
keywords: web controls, generating AutoCapitalize
keywords: how to, generate AutoCapitalize
keywords: display files, generating AutoCapitalize
keywords: Web server controls [ASNA.Monarch], AutoCapitalize
keywords: field controls, AutoCapitalize

---

Gets or sets the autocapitalization behavior of text elements, capitalizing either no text (default), each sentence, each word, or each character.

#### Syntax
<pre class="syntax"> **BegProp AutoCapitalize Access(*Public) Type([A](amfAutoCapitalizeEnumeration.html)[<span class="auto-style1">utoCapitalize</span>](amfAutoCapitalizeEnumeration.html))
   BegGet;  BegSet** </pre>

#### Property Values
AutoCapitalize enumeration values are as follows: 
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="15%" /><col width="80%" /><col width="5%" align="center"/>
          </colgroup>
          <tr><th>Member</th>
  <th>Description</th>
  <th>Value</th>
          </tr>
          <tr>
            <td>None (default)</td>
            <td>Do not capitalize any text automatically.</td>
            <td>0</td>
          </tr>
          <tr>
            <td>Sentences</td>
            <td>Capitalize the first letter of each sentence automatically.</td>
            <td>1</td>
          </tr>
          <tr>
            <td>Words</td>
            <td>Capitalize the first letter of each word automatically.</td>
            <td>2</td>
          </tr>
          <tr>
            <td>Characters</td>
            <td>Capitalize all characters automatically.</td>
            <td>3</td>
          </tr>
</table>

#### Remarks
Along with [AutoCorrect](amfDdsCharfieldClassAutoCorrectProperty.html), it is a common feature of mobile applications.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsCharField Class](amfDdsCharFieldClass.html) <br /> [ DdsCharField Class Members](amfDdsCharFieldClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
