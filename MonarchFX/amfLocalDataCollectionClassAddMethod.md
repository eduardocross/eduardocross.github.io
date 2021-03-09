---
title: LocalDataCollection.Add Method

Id: amfLocalDataCollectionClassAddMethod
TocParent: amfLocalDataCollectionMethods
TocOrder: 10

keywords: Add method
keywords: LocalDataCollection.Add method
keywords: how to, add element to local data collection
keywords: ldc, adding element
keywords: LDC, adding element
keywords: local data collection, adding element

---

Adds an element to the collection with the provided name and value.
<!-- start -->

#### Syntax
<pre class="prettyprint"> **BegSr Add Access(*Public) Type(Void) 
   DclSrParm *name*  Type(*String)
   DclSrParm *value*  Type(*Object)**       </pre>

#### Parameters
<dl>
        <dt>
 *name* 
        </dt>
        <dd>

String used as a string value (key) of the element to be added.
</dd>
        <dt>
 *value* 
        </dt>
        <dd>

The object used as the value of the element to be added.
</dd>
</dl>

<!-- start -->

#### Example
<pre class="example"> //add the object value (system date and time) to the local data collection named "Snap Shot" MonarchJob.LDC.Add("Snap Shot", System.DateTime.Now.ToString())
   . . .
 DclFld Moment Type (DateTime) 

 // gets the object from the local data collection (for the job) whose value is named "Snap Shot" Moment = MonarchJob.LDC["Snap Shot"] *AS DateTime</pre>

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
[ LocalDataCollection Class](amfLocalDataCollectionClass.html) <br /> [ LocalDataCollection Members](amfLocalDataCollectionMembers.html) <br /> [Job.LDC Field](amfJobClassLDCField.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) <br />System.Collection.ICollection 
