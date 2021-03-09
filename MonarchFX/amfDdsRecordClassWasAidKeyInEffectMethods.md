---
title: DdsRecord.WasAidKeyInEffect Methods

Id: amfDdsRecordClassWasAidKeyInEffectMethods
TocParent: amfDdsRecordClassMethods
TocOrder: 260

keywords: DdsRecord.WasAidKeyInEffect methods
keywords: WasAidKeyInEffect methods
keywords: how to, test if aid key in effect for dds record
keywords: response indicators, returning for function key
keywords: web controls, testing if aid key in dds record
keywords: subfiles, testing if aid key for dds record
keywords: subfile controls, testing if aid keys for dds record
keywords: subfile records, testing if aid keys for
keywords: records, testing if aid keys for
keywords: display files, testing if aid keys for record
keywords: display files, aid key used
keywords: indicator expressions, aidkeys

---

This overloaded method returns a boolean value indicating if the key or conditional value expression was in effect for the DdsRecord. If in effect, the resulting indicator or resulting indicator and text are also returned.

#### Overloaded List
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="50%" /><col width="50%" />
          </colgroup>
          <tr><th>Syntax</th>
          <th>Description</th>
          </tr>
            <tr>
              <td>[
              WasAidKeyInEffect ( *ConditionalValue, integer* )](amfDdsRecordClassWasAidKeyInEffectMethod1.html)
              </td>
              <td>Returns a boolean value
            indicating if the conditional expression indicated
            was in effect, and if so, the resulting
            indicator is also returned.</td>
            </tr>
            <tr>
              <td>[
              WasAidKeyInEffect ( *AidKey, integer, string* )](amfDdsRecordClassWasAidKeyInEffectMethod2.html)
              </td>
              <td>Returns a boolean value
            indicating if the key indicated was in effect, and
            if so, the resulting indicator and text
            description are also returned.</td>
            </tr>
</table>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html)<br />[DdsRecord Class Members](amfDdsRecordClassMembers.html)<br />[ ConditionalValue Class](amfConditionalValueClass.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
