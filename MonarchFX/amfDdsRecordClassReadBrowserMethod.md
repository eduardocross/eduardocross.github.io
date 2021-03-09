---
title: DdsRecord.ReadBrowser Method

Id: amfDdsRecordClassReadBrowserMethod
TocParent: amfDdsRecordClassMethods
TocOrder: 110

keywords: SubfileCursorException
keywords: SubfilePropertyException
keywords: ReadBrowser method
keywords: DdsRecord.ReadBrowser method
keywords: how to, read record from browser
keywords: reading browser records
keywords: web controls, reading records from browser
keywords: subfiles, reading records from browser
keywords: subfile controls, reading records from browser
keywords: subfile records, reading from browser
keywords: records, reading from browser
keywords: display files, reading records from browser

---

This method reads the browser.

#### Syntax
<pre class="prettyprint">
 **BegSr ReadBrowser() Access(*Public) Type(Void)** 
            </pre>

<!--mine -->

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
                <colgroup>
                  <col width="50%" />
                  <col width="50%" />
                </colgroup>
                <tr>
                  <th>Value</th>
                  <th>Condition</th>
                </tr>
                <tr>
                  <td>SubfileCursorException</td>
                  <td>Subfile record cursor field
            could not be found.</td>
                </tr>
                <tr>
                  <td>SubfilePropertyException</td>
                  <td>There was an error
            processing property for the current format.</td>
          </tr>
</table>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
