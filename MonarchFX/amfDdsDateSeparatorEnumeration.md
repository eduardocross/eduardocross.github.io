---
title: DdsBaseDate.DdsDateSeparator Enumeration

Id: amfDdsDateSeparatorEnumeration
TocParent: amfWebDspFEnumerations
TocOrder: 60

keywords: enumerations [ASNA.Monarch.WebDspF], DdsBaseDate.DdsDateSeparator
keywords: DdsBaseDate.DdsDateSeparator enumeration
keywords: fields, date/time format constants
keywords: date/time format of field constants
keywords: how to, determine date/time format of field constants
keywords: DEFAULT enumeration member
keywords: SERVER enumeration member
keywords: SLASH enumeration member
keywords: DASH enumeration member
keywords: PERIOD enumeration member
keywords: COMMA enumeration member
keywords: BLANK enumeration member

---

The **DdsBaseDate.DdsDateSeparator** enumerated constant defines values for the character that will be used as the separation character in the date field.

#### Syntax
<pre class="prettyprint"> **BegEnum DdsBaseDate.DdsDateSeparator Access(*Public)** </pre>

#### Remarks
**DdsBaseDate.DdsDateSeparator** defines values in which you can select one of the choices.

#### Members
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="15%" /><col width="80%" /><col width="5%" align="center"/>
          </colgroup>
          <tr><th>Member</th>
  <th>Description</th>
  <th>Value</th>
          </tr>
          <tr>
            <td>DEFAULT</td>
            <td>The default is
            used. </td>
            <td>0</td>
          </tr>
          <tr>
            <td>SERVER</td>
            <td>The default defined on the
            server.</td>
            <td>1</td>
          </tr>
          <tr>
            <td>SLASH</td>
            <td>A "/" (slash) will be used
            as the date field separator.</td>
            <td>2</td>
          </tr>
          <tr>
            <td>DASH</td>
            <td>A "-" (dash) will be used
            as the date field separator.</td>
            <td>3</td>
          </tr>
          <tr>
            <td>PERIOD</td>
            <td>A "." (period) will be used
            as the date field separator.</td>
            <td>4</td>
          </tr>
          <tr>
            <td>COMMA</td>
            <td>A "," (comma) will be used
            as the date field separator.</td>
            <td>5</td>
          </tr>
          <tr>
            <td>BLANK</td>
            <td>A " " (blank) will be used
            as the date field separator.</td>
            <td>6</td>
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

