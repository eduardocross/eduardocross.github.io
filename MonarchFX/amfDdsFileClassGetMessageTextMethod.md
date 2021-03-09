---
title: DdsFile.GetMessageText Method

Id: amfDdsFileClassGetMessageTextMethod
TocParent: amfDdsFileClassMethods
TocOrder: 30

keywords: FormatNotFoundException
keywords: EmptyFormatException
keywords: ExternalFieldException
keywords: GetMessageText method
keywords: DdsFile.GetMessageText method
keywords: error message, retrieving message text
keywords: how to, retrieve error message text
keywords: display files, error message text
keywords: web controls, retrieve error message text

---

Retrieves the message text from the ASNA.Monarch.WebDspF.ErrorMessageInfo object.

#### Syntax
<pre class="prettyprint"> **BegFunc GetMessageText Access(*Public) Type(*String)
    DclSrParm *message*  Type(ASNA.Monarch.WebDspF.ErrorMessageInfo)** </pre>

#### Parameters
<dl>
        <dt>
 *message* 
        </dt>
        <dd>
 **ASNA.Monarch.WebDspF.ErrorMessageInfo**  object
        instance. This contains text of the message and information
        about replacement variables, and can include variable data
        that is being provided by the message sender.</dd>
</dl>

<!--mine -->

#### Return Value
String. The message text from the ASNA.Monarch.WebDspF.ErrorMessageInfo object.
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
            <td>EmptyFormatException</td>
            <td>Display file format is
            empty.</td>
          </tr>
          <tr>
            <td>ExternalFieldException</td>
            <td>Requested field does not
            belong to the display file format.</td>
          </tr>
          <tr>
            <td>FormatNotFoundException</td>
            <td>Display file format was not
            found.</td>
          </tr>
</table>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsFile Class](amfDdsFileClass.html) <br clear="none" /> [DdsFile Class Members](amfDdsFileClassMembers.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
