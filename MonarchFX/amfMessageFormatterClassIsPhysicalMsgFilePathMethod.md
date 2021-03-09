---
title: MessageFormatter.IsPhysicalMsgFilePath Method

Id: amfMessageFormatterClassIsPhysicalMsgFilePathMethod
TocParent: amfMessageFormatterMethods
TocOrder: 50

keywords: IsPhysicalMsgFilePath method
keywords: MessageFormatter.IsPhysicalMsgFilePath method
keywords: message files, physical message file path
keywords: how to, get physical message file path
keywords: how to, get database name of physical message file path
keywords: how to, get library of physical message file path
keywords: how to, get file name of physical message file path

---

Returns a formatted message.

#### Syntax
<pre class="syntax"> **BegFunc IsPhysicalMsgFilePath Access(*Public) Type(*Boolean)
   DclSrParm *xmlDoc*  Type(System.Xml.XmlDocument)
   DclSrParm *dbName*   Type(*String)
   DclSrParm *library*  Type(*String)
   DclSrParm *file*  Type(*String)**       </pre>  

#### Parameters
<dl>
        <dt>
 *xmlDoc* 
        </dt>
        <dd>System.Xml.XmlDocument object representing an Xml
        message file.</dd>
        <dt>
 *dbName* 
        </dt>
        <dd>String. The database name of the physical message file
        path.</dd>
        <dt>
 *library* 
        </dt>
        <dd>String. The library of the physical message file
        path.</dd>
        <dt>
 *file* 
        </dt>
        <dd>String. The file name of the physical message file
        path.</dd>
</dl>  

<!--mine -->

#### Return Value
Boolean True if the message is a physical file path and also the database name, library, and file name.
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
            <td>ASNA.Monarch.WebDspF.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ MessageFormatter Class](amfMessageFormatterClass.html) <br /> [ MessageFormatter Class Members](amfMessageFormatterMembers.html) <br /> [ ASNA.Monarch.Message Class](amfMessageClass.html) <br />[ASNA.Monarch Namespace](amfMonarchNamespace.html)
