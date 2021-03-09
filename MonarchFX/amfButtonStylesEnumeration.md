---
title: ButtonStyles Enumeration

Id: amfButtonStylesEnumeration
TocParent: amfWebDspFEnumerations
TocOrder: 30

keywords: enumerations [ASNA.Monarch.WebDspF], ButtonStyles
keywords: ButtonStyles enumeration

keywords: Button enumeration member
keywords: Image enumeration member
keywords: Link enumeration member

---

The <code> **ButtonStyles** </code> enumerated constant defines the type of DdsButton control field. The default is **Button** .

#### Syntax
<pre class="syntax"> **BegEnum ButtonStyles Access(*Public)** </pre>

#### Members
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="15%" /><col width="80%" /><col width="5%" align="center" />
          </colgroup>
          <tr><th>Member</th>
  <th>Description</th>
  <th>Value</th>
          </tr>
          <tr>
            <td><code>Button</code></td>
            <td>The field control is a
            regular button control and has that functionality.</td>
            <td>0</td>
          </tr>
          <tr>
            <td><code>Link</code></td>
            <td>The field control is a
            hyperlink-style button that has the same appearance as
            a 
 **HyperLink**  but the same
            functionality as a Button control.</td>
            <td>1</td>
          </tr>
          <tr>
            <td><code>Image</code></td>
            <td>The field control is an
            image that is a clickable button on the web
            page. This appears as an image but has the same
            functionality as a Button control.</td>
            <td>2</td>
          </tr>
</table>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl><dd>
        [
        ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
</dl>

