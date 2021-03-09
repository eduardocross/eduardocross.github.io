---
title: DdsRecord.IsAidKeyInEffect Methods

Id: amfDdsRecordClassIsAidKeyInEffectMethods
TocParent: amfDdsRecordClassMethods
TocOrder: 70

keywords: DdsRecord.IsAidKeyInEffect methods
keywords: IsAidKeyInEffect methods
keywords: how to, test if aid key in effect for dds record
keywords: response indicators, testing for keys
keywords: web controls, testing aid keys for dds record
keywords: subfiles, testing aid keys for dds record
keywords: subfile controls, testing aid keys for dds record
keywords: subfile records, testing aid keys for
keywords: records, testing aid keys for
keywords: display files, testing aid keys for record
keywords: display files, aid keys
keywords: aidkeys, testing condition
keywords: conditioning expressions, aidkeys
keywords: indicator expressions, aidkeys

---

This overloaded method returns a boolean value indicating if the key or conditional value expression is in effect for the key specified. If in effect, the resulting indicator or resulting indicator and text parameters are also returned.

#### Overloaded List
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="40%" /><col width="50%" />
          </colgroup>
          <tr><th>Syntax</th>
          <th>Description</th>
          </tr>
            <tr>
              <td>[
              IsAidKeyInEffect ( *ConditionalValue, integer* )](amfDdsRecordClassIsAidKeyInEffectMethod1.html)
              </td>
              <td>Returns a boolean value
            indicating if the conditional expression is in effect
            for the keys specified, and if so, the resulting
            indicator is also returned.</td>
            </tr>
            <tr>
              <td>[
              IsAidKeyInEffect ( *AidKey, integer, string* )](amfDdsRecordClassIsAidKeyInEffectMethod2.html)
              </td>
              <td>Returns a boolean value
            indicating if the Aidkey Property dialog is in
            effect for the key specified, and if so,
            the resulting indicator and text description are
            also returned.</td>
            </tr>
</table>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html)<br />[DdsRecord Class Members](amfDdsRecordClassMembers.html)<br />[ ConditionalValue Class](amfConditionalValueClass.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
