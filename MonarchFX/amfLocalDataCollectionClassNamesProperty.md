---
title: LocalDataCollection.Names Property

Id: amfLocalDataCollectionClassNamesProperty
TocParent: amfLocalDataCollectionProperties
TocOrder: 20

keywords: Names property
keywords: LocalDataCollection.Names property
keywords: ldc, names dictionary
keywords: LDC, names dictionary
keywords: local data collection, names dictionary
keywords: how to, retrieve local data collection names dictionary

---

Gets an **ICollection** containing the names in the **IDictionary** .

#### Syntax
<pre class="prettyprint"> **BegProp Names Access(*Public) Type() 
  BegGet;**       </pre>

#### Property Values
An **ICollection** object containing the names in the **IDictionary** .

#### Remarks
The order of the names in the returned **ICollection** is unspecified, but it is guaranteed to be the same order as the corresponding values in the **ICollection** returned by the [ Values](amfLocalDataCollectionClassValuesProperty.html) property.
<!-- start -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td>[ASNA.Monarch](amfMonarchNamespace.html) </td>
          </tr>
          <tr>
            <td>Assembly:</td>
            <td>ASNA.VisualRPG.Runtime.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ LocalDataCollection Class](amfLocalDataCollectionClass.html) <br /> [ LocalDataCollection Members](amfLocalDataCollectionMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
