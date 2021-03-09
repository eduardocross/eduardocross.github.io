---
title: WebDevice.GetSharedFile Method

Id: amfWebDeviceClassGetSharedFileMethod
TocParent: amfWebDeviceClassMethods
TocOrder: 60

keywords: GetSharedFile method
keywords: WebDevice.GetSharedFile method
keywords: device control, getting shared file
keywords: display files, getting shared file
keywords: shared files, getting for device
keywords: how to, getting shared file for device

---

Returns an instance of the [ WebDisplayFile](amfWebDisplayFileClass.html) object for the file name specified.

#### Syntax
<pre class="syntax"><code class="avr"> **BegFunc GetSharedFile Access(*Public) Type([WebDisplayFile](amfWebDisplayFileClass.html))
   DclSrParm *shareFileName*  Type(*String)**       </code></pre>  

#### Parameters
<dl>
        <dt>
 *shareFileName* 
        </dt>
        <dd>The name of the file.</dd>
</dl>  

<!--mine -->

#### Return Value
An instance of the **WebDisplayFile** object.
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
[WebDevice Class](amfWebDeviceClass.html) <br /> [ WebDevice Class Members](amfWebDeviceClassMembers.html) <br /> [ WebDisplayFile Class](amfWebDisplayFileClass.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
