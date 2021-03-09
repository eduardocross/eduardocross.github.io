---
title: WebDevice.Attach Method(string, WebDisplayFile)

Id: amfWebDeviceClassAttachMethod
TocParent: amfWebDeviceClassAttachMethods
TocOrder: 10

---

Attaches the [ WebDisplayFile](amfWebDisplayFileClass.html) and a shared file to a **WebDevice** .

#### Syntax 
<pre class="prettyprint"> **BegSr Attach Access(*Public) Type(Void)
   DclSrParm *shareFileName*  Type(*String)
   DclSrParm *displayFile*  Type(ASNA.Monarch.WebDisplayFile)**       </pre>  

#### Parameters
<dl>
        <dt>
          <code> *shareFileName* </code>
        </dt>
        <dd>The shared file name to be attached to the device.</dd>
        <dt>
          <code> *displayFile* </code>
        </dt>
        <dd>
          [
        ASNA.Monarch.WebDisplayFile](amfWebDisplayFileClass.html). The 
 **WebDisplayFile**  to be attached to the 
 **WebDevice** .</dd>
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
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[WebDevice Class](amfWebDeviceClass.html) <br /> [ WebDevice Class Members](amfWebDeviceClassMembers.html) <br /> [ Attach (ASNA.Monarch.WebDisplayFile)](amfWebDeviceClassAttachMethod2.html) <br /> [ WebDisplayFile Class](amfWebDisplayFileClass.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
