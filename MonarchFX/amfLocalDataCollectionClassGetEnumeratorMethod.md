---
title: LocalDataCollection.GetEnumerator Method

Id: amfLocalDataCollectionClassGetEnumeratorMethod
TocParent: amfLocalDataCollectionMethods
TocOrder: 40

keywords: GetEnumerator method
keywords: LocalDataCollection.GetEnumerator method
keywords: ldc, get enumerator
keywords: LDC, get enumerator
keywords: local data collection, enumerator
keywords: how to, set local data collection enumerator

---

Returns an enumerator that can iterate through the elements in a dictionary.

#### Syntax
<pre class="prettyprint"> **BegFunc GetEnumerator() Access(*Public) Type(IDictionaryEnumerator)**       </pre>

#### Return Value
An **IDictionaryEnumerator** for the **IDictionary** .

#### Remarks
Enumerators only allow reading the data in the collection and cannot be used to modify the underlying collection.
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
[ LocalDataCollection Class](amfLocalDataCollectionClass.html) <br /> [ LocalDataCollection Members](amfLocalDataCollectionMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) <br />System.Collections.IDictionaryEnumerator <br />System.Collections.IDictionary 
