---
title: FieldUsages Enumeration

Id: amfFieldUsagesEnumeration
TocParent: amfWebDspFEnumerations
TocOrder: 90

keywords: enumerations [ASNA.Monarch.WebDspF], FieldUsages
keywords: FieldUsages enumeration

keywords: Both enumeration member
keywords: InputOnly enumeration member
keywords: OutputOnly enumeration member
keywords: Hidden enumeration member

---

The **FieldUsages** enumerated constant defines how the field is used.

#### Syntax
<pre class="prettyprint">
 **BegEnum FieldUsages Access(*Public)** 
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
                <td>Hidden</td>
                <td>The field is hidden. These
          fields are passed from and to the program but are not
          sent to the display. Hidden fields are useful in
          applications involving subfiles. For example, a subfile
          record can contain record key information in a hidden
          field. The hidden field cannot be seen by the user, but
          is returned to program with the subfile record so that
          the program can return the record to the database.</td>
                <td>0</td>
              </tr>
              <tr>
                <td>OutputOnly</td>
                <td>The field in output only.
          These fields that are passed from the program to the
          display station when the program writes a record to a
          display. Output fields contain data provided by the
          program, not by the user. In the case of subfiles, which
          are special records used to display lists of information,
          output fields are returned to the program as if they were
          output/input fields.</td>
                <td>1</td>
              </tr>
              <tr>
                <td>InputOnly</td>
                <td>The field is input only.
          These fields that are passed from the display station to
          the program when the program reads a record. They can be
          initialized with a default value (specified in the record
          format for the display file). If the user does not change
          the field and the field is selected for input, the
          default value is passed to the program. Input fields that
          are not initialized are displayed as blanks into which
          the user can enter data. 
 **Note** : Trailing blanks on input fields
          are replaced by null and not blank characters; therefore,
          the Insert key can be used to insert characters in all
          input fields that end in blanks.</td>
                <td>2</td>
              </tr>
              <tr>
                <td>Both</td>
                <td>The field is output and
          input. This is the default.</td>
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

