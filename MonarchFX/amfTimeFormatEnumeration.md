---
title: TimeFormat Enumeration

Id: amfTimeFormatEnumeration
TocParent: amfWebDspFEnumerations
TocOrder: 130

keywords: enumerations [ASNA.Monarch.WebDspF], TimeFormat
keywords: TimeFormat enumeration
keywords: fields, time format constants
keywords: time format of field constants
keywords: how to, determine time format of field constants
keywords: EUR enumeration member
keywords: HMS enumeration member
keywords: ISO enumeration member
keywords: JIS enumeration member
keywords: USA enumeration member

---

The <code>TimeFormat</code> enumerated constant defines values describing the format of a time field. 

#### Syntax
<pre class="prettyprint"> **BegEnum DataTimeFormat Access(*Public)** </pre>

#### Remarks
<code>TimeFormat</code> defines values in which you can select one of the choices.

#### Members
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="15%" /><col width="80%" /><col width="5%" align="center"/>
          </colgroup>
          <tr><th>Member</th>
  <th>Description</th>
  <th>Value</th>
          </tr>
<tr><td><code>EUR</code></td><td>IBM European Standard. For
          dates dd.mm.yyyy, time format is hh:mm:ss.</td><td>2</td></tr>
          <tr>
          <td><code>HMS</code></td><td>Hours/Minutes/Seconds. Format
          for time is hh:mm:ss.</td>
          <td>4</td></tr>
          <tr>
          <td><code>ISO</code></td><td>International Standards
          Organization. For dates yyyy-mm-dd., time format
          is hh:mm:ss.</td><td>0</td></tr>
          <tr><td><code>JIS</code></td><td>Japanese Industrial Standard
          Christian Era. For dates yyyy-mm-dd, time format is
          hh:mm:ss.</td><td>3</td></tr>
          <tr><td><code>USA</code></td><td>IBM USA Standard. For
          dates mm/dd/yyyy, time format is hh:mm AM.</td><td>1</td></tr></table>

<!-- -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup><col width="15%" style="font-weight:bold" /><col width="85%" />
          </colgroup>
          <tr><td>Namespace:</td>
 <td>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)</td>
          </tr>
          <tr><td>Assembly:</td>
          <td>ASNA.Monarch.WebDspF.DLL</td>
          </tr>
         <tr><td>Platforms:</td>
 <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

#### See Also
<dl>
        <dd>[
        ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
</dl>

