---
title: DdsTimestampField.LoadPostData Method (string,System.Collections.Specialized.NameValueCollection)

Id: amfDdsTimestampFieldClassLoadPostDataMethod
TocParent: amfDdsTimestampFieldClassMethods
TocOrder: 10

---

Processes post back data for an ASP.NET server control for the named collection. 

#### Syntax
<pre class="prettyprint"> **BegFunc LoadPostData Access(*Public) Modifier(*Overrides) Type(*Boolean)
  DclSrParm *postDataKey*  Type(*String)
  DclSrParm *values*  Type(System.Collections.Specialized.NameValueCollection)** </pre>

#### Parameters
<dl>
        <dt>
 *postDataKey* 
        </dt>
        <dd>String containing the key identifier for the
        control.</dd>
        <dt>
 *values* 
        </dt>
        <dd>
 **System.Collections.Specialized.NameValueCollection**  containing
        a collection of all incoming name values. Represents a
        sorted collection of associated System.String keys and
        System.String values that can be accessed either with the
        key or with the index.</dd>
</dl>

#### Return Value
Boolean set **True** if the server control's state changed as a result of the postback; otherwise **False** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsTimestampField Class](amfDdsTimeStampFieldClass.html) <br /> [ DdsTimestampField Class Members](amfDdsTimeStampFieldClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
