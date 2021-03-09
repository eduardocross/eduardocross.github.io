---
title: DdsDataField.LoadPostData Method (string)

Id: amfDdsDataFieldClassLoadPostDataMethod2
TocParent: amfDdsDataFieldClassLoadPostDataMethods
TocOrder: 20

keywords: DecimalCoversionException

---

Processes post back data for an ASP.NET server control.

#### Syntax
<pre class="prettyprint"> **BegFunc LoadPostData Access(*Public) Modifier(*Overrides ) Type(*Boolean)
  DclSrParm *postedValue*  Type(*String)** </pre>

#### Parameters
<dl>
        <dt>
 *postedValue* 
        </dt>
        <dd>String containing the value for the control.</dd>
</dl>

<!--mine -->

#### Return Value
Boolean **True** if the server control's state changed as a result of the postback, otherwise **False** .
<!--mine -->

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="50%" /><col width="50%" />
          </colgroup>
          <tr><th>Value</th><th>Condition</th>
          </tr>
          <tr><td>DecimalConversionException</td><td>For [DdsDecField](amfDdsDecFieldClass.html), the decimal value contains twosigns.</td>
          </tr>
</table>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsDataField Class](amfDdsDataFieldClass.html) <br /> [ DdsDataField Class Members](amfDdsDataFieldClassMembers.html) <br /> [ Derived Classes](amfDdsDataFieldDerivedClasses.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
