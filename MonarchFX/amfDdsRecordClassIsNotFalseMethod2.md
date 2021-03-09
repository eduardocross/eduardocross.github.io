---
title: DdsRecord.IsNotFalse Method(string, string)

Id: amfDdsRecordClassIsNotFalseMethod2
TocParent: amfDdsRecordClassIsNotFalseMethods
TocOrder: 20

keywords: IndicatorArrayLengthException

---

This method returns **True** if the condition for the *fieldID* is not false.

#### Syntax
<pre class="prettyprint"> **BegFunc IsNotFalse Access(*Public) Type(*Boolean)
   DclSrParm *fieldID*  Type(*string)
   DclSrParm *condition*  Type(*string)** </pre>

#### Parameters
<dl>
        <dt>
 *fieldID* 
        </dt>
        <dd>String containing the field Id to evaluate.</dd>
        <dt>
 *condition* 
        </dt>
        <dd>String containing the condition to evaluate for the 
 *fieldID* .</dd>
</dl>

#### Return Value
**True** if the *condition* for the *fieldID* is not false; otherwise **False** .
<!--mine -->

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="70%">
          <colgroup><col width="20%" /><col width="50%" />
          </colgroup>
          <tr><th>Value</th>
           <th>Condition</th>
          </tr>
          <tr>
            <td>            IndicatorArrayLengthException</td>
            <td>The provided indicator
            string length is not 100.</td>
          </tr>
</table>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
