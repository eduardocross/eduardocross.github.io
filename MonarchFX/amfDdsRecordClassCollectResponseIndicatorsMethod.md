---
title: DdsRecord.CollectResponseIndicators Method

Id: amfDdsRecordClassCollectResponseIndicatorsMethod
TocParent: amfDdsRecordClassMethods
TocOrder: 10

keywords: CollectResponseIndicators method
keywords: DdsRecord.CollectResponseIndicators method
keywords: how to, get all response indicators for dds record
keywords: response indicators, all for dds record
keywords: web controls, getting all response indicators for dds record
keywords: subfiles, getting all response indicators for dds record
keywords: subfile controls, getting all response indicator for dds record
keywords: subfile records, getting all response indicator for
keywords: records, getting all response indicator for
keywords: display files, getting all response indicator for record

---

This method collects an array containing the response indicators for the record.

#### Syntax
<pre class="prettyprint"> **BegSr CollectResponseIndicators Access(*Public) Type(Void)
   DclSrParm *responseIndicators*  Type(System.Collections.ArrayList) Rank(1)** </pre>

#### Parameters
<dl>
        <dt>
 *responseIndicators* 
        </dt>
        <dd>
 **System.Collections.ArrayList**  that represents an array
        of response indicators for the record.</dd>
</dl>

#### Remarks
The response indicators are used to pass information from the system to an application program when an input request completes. These indicators can be used to determine which function keys were pressed or whether data was changed. Response indicators can be specified at the file, record format, and field levels.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
