---
title: DdsRecord.GetResultIndicator Method

Id: amfDdsRecordClassGetResultIndicatorMethod
TocParent: amfDdsRecordClassMethods
TocOrder: 60

keywords: IndicatorException
keywords: GetResultIndicator method
keywords: DdsRecord.GetResultIndicator method
keywords: how to, test response indicator for dds record
keywords: response indicators, testing
keywords: web controls, testing response indicator for dds record
keywords: subfiles, testing response indicator for dds record
keywords: subfile controls, testing response indicator for dds record
keywords: subfile records, testing response indicator for
keywords: records, testing response indicator for
keywords: display files, testing response indicator for record
keywords: display files, response indicator

---

This method returns the integer value for the result indicator specified.

#### Syntax
<pre class="prettyprint"> **BegFunc GetResultIndicator Access(*Public) Type(*Integer)
  DclSrParm *indValue*  Type(*String)** </pre>

#### Parameters
<dl>
        <dt>
 *indValue* 
        </dt>
        <dd>
 **String**  that contains the indicator value.</dd>
</dl>

#### Return Value
Integer value containing 0 (False) or 1 (True).
<!--mine -->

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="50%" /><col width="50%" />
          </colgroup>
          <tr><th>Value</th>
           <th>Condition</th>
          </tr>
          <tr>
            <td>IndicatorException</td>
            <td>An indicator outside the
            01-99 range has been provided.</td>
          </tr>
</table>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
