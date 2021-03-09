---
title: LocalDataCollection.Contains Method

Id: amfLocalDataCollectionClassContainsMethod
TocParent: amfLocalDataCollectionMethods
TocOrder: 30

keywords: Contains Method
keywords: LocalDataCollection.Contains Method
keywords: ldc, checking contents
keywords: LDC, checking contents
keywords: local data collection, checking contents
keywords: how to, check local data collection contents

---

This method returns a boolean value indicating if the **IDictionary** contains an element with the name specified.

#### Syntax
<pre class="prettyprint"> **BegFunc Contains Access(*Public) Type(*Boolean) 
   DclSrParm *name*  Type(*String)**       </pre>

#### Parameters
<dl>
        <dt>
 *name* 
        </dt>
        <dd>String containing the name to search for in the local
        data table.</dd>
</dl>

#### Return Values
Boolean. **True** if the IDictionary contains an element with the name provided, otherwise **false** .
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
[ LocalDataCollection Class](amfLocalDataCollectionClass.html) <br /> [ LocalDataCollection Members](amfLocalDataCollectionMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) <br />System.Collections.IDictionary 
