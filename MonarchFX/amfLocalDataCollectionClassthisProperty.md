---
title: LocalDataCollection.this Property

Id: amfLocalDataCollectionClassthisProperty
TocParent: amfLocalDataCollectionProperties
TocOrder: 30

keywords: this property
keywords: LocalDataCollection.this property
keywords: how to, add element to local data collection
keywords: how to, change element in local data collection
keywords: ldc, adding element
keywords: ldc, changing element
keywords: LDC, adding element
keywords: LDC, changing element
keywords: local data collection, adding element
keywords: local data collection, changing element

---

Gets or sets the collection element with the specified name.

#### Property Values
<pre class="prettyprint"> **BegProp this Access(*Public) Type(*Object) 
   DclSrParm *name*  Type(*String)
 BegGet;   BegSet;**       </pre>

#### Parameters
<dl>
        <dt>
 *name* 
        </dt>
        <dd>

String used as a string value (key) of the element to get or set.
</dd>
</dl>

#### Property Values
The element with the specified name.

#### Remarks
This property provides the ability to access a specific element in the collection.

When setting the property, if the specific name already exists in the dictionary, the value is replaced; otherwise, a new element is created. In contrast, the [Add](amfLocalDataCollectionClassAddMethod.html) method does not modify existing elements.
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
[ LocalDataCollection Class](amfLocalDataCollectionClass.html) <br /> [ LocalDataCollection Members](amfLocalDataCollectionMembers.html) <br /> [Add Method](amfLocalDataCollectionClassAddMethod.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
