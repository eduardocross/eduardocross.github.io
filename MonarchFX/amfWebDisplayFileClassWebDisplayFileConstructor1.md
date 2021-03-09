---
title: WebDisplayFile Constructor(String, String, AdgDataSet, Boolean)

Id: amfWebDisplayFileClassWebDisplayFileConstructor1
TocParent: amfWebDisplayFileClassWebDisplayFileConstructors
TocOrder: 10

---

Constructs a new instance of a WebDisplayFile object.

#### Syntax
<pre class="prettyprint"><code class="avr"> **BegConstructor WebDisplayFile Access(*Public)
   DclSrParm *fileName*  Type(*String)
   DclSrParm *pageName*  Type (*String)
   DclSrParm *dataSet*  Type(ASNA.DataGate.Client.AdgDataSet)
   DclSrParm *shared*  Type(*Boolean)** </code></pre>

#### Parameters
<dl>
        <dt>
          <code> *fileName* </code>
        </dt>
        <dd>

String. The name of the '.aspx' file containing the web form.
</dd>
        <dt>
          <code> *pageName* </code>
        </dt>
        <dd>

String. The name of the page within the '.aspx' file containing the web form.
</dd>
        <dt>
          <code> *dataSet* </code>
        </dt>
        <dd>

**ASNA.DataGate.Client.AdgDataSet** . The dataset associated with the web form.
</dd>
        <dt>
          <code> *shared* </code>
        </dt>
        <dd>Boolean. Specify 
        <code> **True** </code> to allow sharing, otherwise specify 
        <code> **False** </code>.</dd>
</dl>
<!-- -->

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
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016,  Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ WebDisplayFile Class](amfWebDisplayFileClass.html) <br /> [ WebDisplayFile Class Members](amfWebDisplayFileClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html)
