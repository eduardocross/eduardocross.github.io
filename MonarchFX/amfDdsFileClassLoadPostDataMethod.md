---
title: DdsFile.LoadPostData Method

Id: amfDdsFileClassLoadPostDataMethod
TocParent: amfDdsFileClassMethods
TocOrder: 50

keywords: VirtualRowColException
keywords: LoadPostData method
keywords: DdsFile.LoadPostData method
keywords: how to, process post back data for file control
keywords: display files, process post back data for file control
keywords: web controls, process post back data for file control

---

Processes post back data for an ASP.NET server control.

#### Syntax
<pre class="prettyprint"> **BegFunc LoadPostData Access(*Public) Modifier(*Overrides) Type(*Boolean)
    DclSrParm *postDataKey*  Type(*String)
    DclSrParm *values*  Type(System.Collections.Specialized.NameValueCollection)** </pre>

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
        a collection of all incoming name values. Represents a
        sorted collection of associated System.String keys and
        System.String values that can be accessed either with the
        key or with the index.</dd>
</dl>

<!--mine -->

#### Return Value
Returns **True** if the server control's state changed as a result of the postback; otherwise **False** .
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
            <td>VirtualRowColException</td>
            <td>VirtualRowCol string was in
            correct format.</td>
          </tr>
</table>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsFile Class](amfDdsFileClass.html) <br clear="none" /> [DdsFile Class Members](amfDdsFileClassMembers.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
