---
title: MessageFormatter.FormatMessageText Method

Id: amfMessageFormatterClassFormatMessageTextMethod
TocParent: amfMessageFormatterMethods
TocOrder: 30

keywords: InvalidMessageFormatException

keywords: FormatMessage method
keywords: MessageFormatter.FormatMessage method
keywords: message files, newly formatted message
keywords: how to, format new message

---

The FormatMessageText method retrieves the message's first- and second-level texts and inserts the replacement data provided in the message parameter. The FormatMessage method affects the first level texts.

#### Syntax
<pre class="syntax">public static bool FormatMessageText(string msgFilePath, Message message, 
                                     out string firstLevelText, 
                                     out string secondLevelText)</pre>  

#### Parameters
<dl>
        <dt>
 *msgFilePath* 
        </dt>
        <dd>String. The file path for the message being
        formatted.</dd>
        <dt>
 *message* 
        </dt>
        <dd>An instance of an 
        [
        ASNA.Monarch.Message](amfMessageClass.html) object being
        formatted.</dd>
</dl> 

<!--mine -->

#### Return Value
String. The formatted message.
<!--mine -->

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="50%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <th>Value</th>
            <th>Condition</th>
          </tr>
          <tr>
            <td>InvalidMesssageFormatException</td>
            <td>The message file is not
            properly formatted.</td>
          </tr>
          <tr />
</table>

<!-- -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td>[ASNA.Monarch](amfMonarchNamespace.html)</td>
          </tr>
          <tr>
            <td>Assembly:</td>
            <td>ASNA.Monarch.WebDspF.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td>Windows
      Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ MessageFormatter Class](amfMessageFormatterClass.html) <br /> [ MessageFormatter Class Members](amfMessageFormatterMembers.html) <br /> [ ASNA.Monarch.Message Class](amfMessageClass.html) <br />[ASNA.Monarch Namespace](amfMonarchNamespace.html)
