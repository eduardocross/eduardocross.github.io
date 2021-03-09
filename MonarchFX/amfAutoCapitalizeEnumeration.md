---
title: AutoCapitalize Enumeration

Id: amfAutoCapitalizeEnumeration
TocParent: amfWebDspFEnumerations
TocOrder: 99

keywords: enumerations [ASNA.Monarch.WebDspF], InputStyles
keywords: InputStyles enumeration
keywords: Checkbox enumeration member
keywords: Textbox enumeration member
keywords: MultiLine enumeration member
keywords: Password enumeration member

---

The <code> **Autocapitalize** </code> enumerated constant defines the capitalization behavior for text elements. The default is <code> **None** </code>.

#### Syntax
<pre class="prettyprint"> **BegEnum AutoCapitalize Access(*Public)** 
      </pre>

#### Members
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="15%" /><col width="80%" /><col width="5%" align="center"/>
          </colgroup>
          <tr><th>Member</th>
  <th>Description</th>
  <th>Value</th>
          </tr>
          <tr>
            <td><code><u>None</u></code></td>
            <td>Do not capitalize any text automatically.</td>
            <td>0</td>
          </tr>
          <tr>
            <td><code>Sentences</code></td>
            <td>Capitalize the first letter of each sentence automatically.</td>
            <td>1</td>
          </tr>
          <tr>
            <td><code>Words</code></td>
            <td>Capitalize the first letter of each word automatically.</td>
            <td>2</td>
          </tr>
          <tr>
            <td><code>Characters</code></td>
            <td>Capitalize all characters automatically.</td>
            <td>3</td>
          </tr>
</table>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
        <dd>[
        ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
</dl>

