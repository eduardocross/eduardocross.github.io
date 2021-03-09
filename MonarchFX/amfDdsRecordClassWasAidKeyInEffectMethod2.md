---
title: DdsRecord.WasAidKeyInEffect(AidKey, integer, string)

Id: amfDdsRecordClassWasAidKeyInEffectMethod2
TocParent: amfDdsRecordClassWasAidKeyInEffectMethods
TocOrder: 20

---

This method returns a boolean value indicating if the key indicated was in effect. If so, the resulting indicator and text description are also returned.

#### Syntax
<pre class="prettyprint"> **BegFunc WasAidKeyInEffect Access(*Public) Type(*Boolean)
   DclSrParm *key*  Type(ASNA.Monarch.WebDspF.AidKey) Rank(1)
   DclSrParm *resultingIndicator*  Type(*Integer)
   DclSrParm *text*  Type(*String)** </pre>

#### Parameters
<dl>
        <dt>
 *key* 
        </dt>
        <dd>An internal reference to an index value that
        represents the function key.</dd>
        <dt>
 *resultingIndicator* 
        </dt>
        <dd>Integer. The indicator to set 'on' if the key was
        pressed.</dd>
        <dt>
 *text* 
        </dt>
        <dd>String. The text description of the key.</dd>
</dl>

#### Return Value
**True** if the method determines the key specified was in effect; otherwise **False** . If **True** , the *resultingIndicator* will contain the response indicator and *text* will contain the text description for the function key.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
