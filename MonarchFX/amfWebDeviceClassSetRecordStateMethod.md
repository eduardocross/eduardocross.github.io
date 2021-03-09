---
title: WebDevice.SetRecordState Method

Id: amfWebDeviceClassSetRecordStateMethod
TocParent: amfWebDeviceClassMethods
TocOrder: 110

keywords: SetRecordState method
keywords: WebDevice.SetRecordState method
keywords: device control, setting record format
keywords: device control, setting record index
keywords: device control, setting record indicators
keywords: display files, setting record format
keywords: display files, setting record index
keywords: display files, setting record indicators
keywords: record states, setting index
keywords: record states, setting format
keywords: record states, setting indicators
keywords: record indexes, setting
keywords: record formats, setting
keywords: record indicators, setting
keywords: how to, set record index
keywords: how to, set record format
keywords: how to, set record indicators

---

Sets the index and an array of boolean values representing the evaluation (true or false) for each of the indicators for the record format specified.

#### Syntax
<pre class="prettyprint"> **BegSr SetRecordState Access(*Public) Type(*void)
   DclSrParm *fmtName*  Type(*String)
   DclSrParm *index*  Type(*Integer)
   DclSrParm *indicators*  Type(*Boolean) Rank(1)**       </pre>  

#### Parameters
<dl>
        <dt>
 *fmtName* 
        </dt>
        <dd>The format name of the record to set the index and
        indicators for.</dd>
        <dt>
 *index* 
        </dt>
        <dd>The integer value of the index.</dd>
        <dt>
 *indicators* 
        </dt>
        <dd>An array of boolean values representing the evaluation
        (true or false) for each of the indicators of the
        record.</dd>
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

#### See Also
[WebDevice Class](amfWebDeviceClass.html) <br /> [ WebDevice Class Members](amfWebDeviceClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
