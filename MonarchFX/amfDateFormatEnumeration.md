---
title: DateFormat Enumeration

Id: amfDateFormatEnumeration
TocParent: amfWebDspFEnumerations
TocOrder: 35

keywords: enumerations [ASNA.Monarch.WebDspF], DateFormat
keywords: DateFormat enumeration
keywords: fields, date/time format constants
keywords: date/time format of field constants
keywords: how to, determine date/time format of field constants
keywords: DMY enumeration member
keywords: EUR enumeration member
keywords: ISO enumeration member
keywords: JIS enumeration member
keywords: MDY enumeration member
keywords: USA enumeration member
keywords: YMD enumeration member
keywords: SERVER enumeration member

---

The **<code>DateFormat</code>** enumerated constant defines values for the format of a date and decimal date field for dates linked to a javascript calendar.

#### Syntax
<pre class="syntax"> **BegEnum DateFormat Access(*Public)** </pre>

#### Remarks
DateFormat defines values in which you can select one of the choices.

#### Members
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="15%" /><col width="80%" /><col width="5%" align="center"/>
          </colgroup>
          <tr><th>Member</th>
  <th>Description</th>
  <th>Value</th>
          </tr>
          <tr>
            <td><code>DMY</code></td>
            <td>Day/Month/Year. For
            date: dd/mm/yy.</td>
            <td>8</td>
          </tr>
          <tr>
            <td><code>EUR</code></td>
            <td>IBM European Standard. For
            date: dd.mm.yyyy. For time: hh:mm:ss.</td>
            <td>4</td>
          </tr>
          <tr>
            <td><code>ISO</code></td>
            <td>International Standards
            Organization. For date: yyyy-mm-dd. For time:
            hh:mm:ss.</td>
            <td>2</td>
          </tr>
          <tr>
            <td><code>JIS</code></td>
            <td>Japanese Industrial
            Standard Christian Era. For date: yyyy-mm-dd. For time:
            hh:mm:ss.</td>
            <td>5</td>
          </tr>
          <tr>
            <td><code>MDY</code></td>
            <td>Month/Day/Year. For date:
            mm/dd/yy.</td>
            <td>7</td>
          </tr>
          <tr>
            <td><code>SERVER</code></td>
            <td>The default specified for
            the server.</td>
            <td>2</td>
          </tr>
          <tr>
            <td><code>USA</code></td>
            <td>IBM USA Standard. For date:
            mm/dd/yyyy. For time: hh:mm AM.</td>
            <td>3</td>
          </tr>
          <tr>
            <td><code>YMD</code></td>
            <td>Year/Month/Day. For date:
            yy/mm/dd.</td>
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

