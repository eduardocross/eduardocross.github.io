---
title: DdsBaseDate.LoadPostData Method

Id: amfDdsBaseDateClassLoadPostDataMethod
TocParent: amfDdsBaseDateClassMethods
TocOrder: 90

keywords: LoadPostData method
keywords: DdsBaseDate.LoadPostData method
keywords: how to, process post back data for date field control
keywords: display files, process post back data for date field control
keywords: web controls, process post back data for date field control
keywords: Web server controls [ASNA.Monarch], field control process post back data
keywords: field controls, date field, process post back data

---

Processes post back data for an ASP.NET server control.

#### Syntax
<pre class="syntax"> **BegFunc LoadPostData Access(*Public) Modifier(*Overrides) Type(*Boolean)
   DclSrParm *postDataKey*    Type(*String)
   DclSrParm *values*         Type(System.Collections.Specialized.NameValueCollection)** </pre>

#### Parameters
<dl>
        <dt>
 *postDataKey* 
        </dt>
        <dd>String containing the identifier for the control.</dd>
        <dt>
 *values* 
        </dt>
        <dd>
 **System.Collections.Specialized.NameValueCollection**  containing
        a collection of all incoming name values. This represents a
        sorted collection of associated System.String keys and
        System.String values that can be accessed either with the
        key or with the index.</dd>
</dl>

#### Return Value
Boolean value set **True** if the server control's state changed as a result of the postback; otherwise **False** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsBaseDate Class](amfDdsBaseDateClass.html) <br /> [ DdsBaseDate Class Members](amfDdsBaseDateClassMembers.html) <br /> [ Derived Classes](amfDdsBaseDateDerivedClasses.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
