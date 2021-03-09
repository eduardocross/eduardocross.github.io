---
title: DecType Enumeration

Id: amfDecTypeEnumeration
TocParent: amfWebDspFEnumerations
TocOrder: 80

keywords: enumerations [ASNA.Monarch.WebDspF], DecType
keywords: DecType enumeration

keywords: Zoned enumeration member
keywords: Packed enumeration member
keywords: Binary enumeration member

---

The **DecType** enumerated constant defines the type of decimal field. The default is **Zoned** .

#### Syntax
<pre class="prettyprint">
 **BegEnum DecType Access(*Public)** 
          </pre>

#### Members
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
              <colgroup>
                <col width="15%" />
                <col width="80%" />
                <col width="5%" align="center" />
              </colgroup>
              <tr>
                <th>Member</th>
                <th>Description</th>
                <th>Value</th>
              </tr>
              <tr>
                <td>Binary</td>
                <td>The field is binary.</td>
                <td>0</td>
              </tr>
              <tr>
                <td>Packed</td>
                <td>The field is packed.</td>
                <td>1</td>
              </tr>
              <tr>
                <td>Zoned</td>
                <td>The field is zoned. This is
          the default.</td>
            <td>2</td>
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

