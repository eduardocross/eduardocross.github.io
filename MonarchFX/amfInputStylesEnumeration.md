---
title: InputStyles Enumeration

Id: amfInputStylesEnumeration
TocParent: amfWebDspFEnumerations
TocOrder: 100

keywords: enumerations [ASNA.Monarch.WebDspF], InputStyles
keywords: InputStyles enumeration
keywords: Checkbox enumeration member
keywords: Textbox enumeration member
keywords: MultiLine enumeration member
keywords: Password enumeration member

---

The **InputStyles** enumerated constant defines the input style for a character field. The default is **Textbox** .

#### Syntax
<pre class="prettyprint"> **BegEnum InputStyles Access(*Public)** 
      </pre>

#### Members
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="15%" /><col width="70%" /><col width="5%" align="center"/>
          </colgroup>
          <tr><th>Member</th>
  <th>Description</th>
  <th>Value</th>
          </tr>
          <tr>
            <td>Textbox</td>
            <td>The field is a single line
          textbox.</td>
                <td>0</td>
              </tr>
              <tr>
                <td>MultiLine</td>
                <td>The field is a multiple line
          textbox.</td>
                <td>1</td>
              </tr>
              <tr>
                <td>Password</td>
                <td>The field is a password
          textbox.</td>
            <td>2</td>
          </tr>
          <tr>
            <td>Checkbox</td>
            <td>The field is checkbox that
          allows the field to be "checked" or "unchecked".</td>
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

