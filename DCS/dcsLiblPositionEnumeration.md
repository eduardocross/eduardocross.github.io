---
title: LiblPosition Enumeration

Id: dcsLiblPositionEnumeration
TocParent: dcsDataGateClientEnumerations
TocOrder: 2

keywords: enumerations [DCS 16.0 LiblPosition
keywords: LiblPosition enumeration
keywords: System enumeration member
keywords: First enumeration member
keywords: Last enumeration member
keywords: Before enumeration member
keywords: After enumeration member
keywords: Replace enumeration member

---

<span> **LiblPosition** </span> contains the values used by [ ILibraryList.AddEntry](dcsILibraryListClassAddEntryMethod.html) to specify the position in the library list to add the new library list entry. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum LiblPosition;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Enum LiblPosition** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum LiblPosition Access(*Public)** 
      </pre>

Remarks

**LiblPosition** is a parameter of the **ILibraryList.AddEntry** method. It specifies the position in the library list to add the new library list entry. 
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <col span="1" width="15%" style="FONT-WEIGHT: bold" />
          <col span="1" width="60%" />
          <col span="1" width="10%" />
          <tr>
            <th colspan="1" rowspan="1">
							Member</th>
            <th colspan="1" rowspan="1">
							Description</th>
            <th colspan="1" rowspan="1">
							Value</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

System 
</td>
            <td colspan="1" rowspan="1">

The library belongs in the ** *system* ** portion of the library list. 
</td>
            <td colspan="1" rowspan="1">

1 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

First 
</td>
            <td colspan="1" rowspan="1">

The library is the ** *first* ** entry in the user portion of the library list. 
</td>
            <td colspan="1" rowspan="1">

2 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Last 
</td>
            <td colspan="1" rowspan="1">

The library is the ** *last* ** entry in the user portion of the library list. 
</td>
            <td colspan="1" rowspan="1">

3 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Before 
</td>
            <td colspan="1" rowspan="1">

The library is to be added ** *before* ** the reference library in the user portion of the library list. 
</td>
            <td colspan="1" rowspan="1">

4 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

After 
</td>
            <td colspan="1" rowspan="1">

The library is to be added ** *after* ** the reference library in the user portion of the library list. 
</td>
            <td colspan="1" rowspan="1">

5 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Replace 
</td>
            <td colspan="1" rowspan="1">

The library is to ** *replace* ** the reference library in the user portion of the library list. 
</td>
            <td colspan="1" rowspan="1">

6 
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [ILibraryList.AddEntry Method](dcsILibraryListClassAddEntryMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

