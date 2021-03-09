---
title: LocalDataCollection.Values Property

Id: amfLocalDataCollectionClassValuesProperty
TocParent: amfLocalDataCollectionProperties
TocOrder: 30

keywords: Values property
keywords: LocalDataCollection.Values property
keywords: ldc, values dictionary
keywords: LDC, values dictionary
keywords: local data collection, values dictionary
keywords: how to, retrieve local data collection values dictionary

---

Gets an **ICollection** containing the values in the .

#### Syntax 
<pre class="prettyprint"> **BegProp Values Access(*Public) Type() 
    BegGet;**       </pre>

#### Property Values
An **ICollection** object containing the values in the **IDictionary** .

#### Remarks
The order of the values in the returned **ICollection** is unspecified, but it is guaranteed to be the same order as the corresponding names in the ICollection returned by the [ Names](amfLocalDataCollectionClassNamesProperty.html) property.
<!-- start -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td>[ASNA.Monarch](amfMonarchNamespace.html)</td>
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
