---
title: Program.RemoveMessage Method (string)

Id: amfProgramClassRemoveMessageMethod1
TocParent: amfProgramClassRemoveMessageMethods
TocOrder: 10

keywords: MessageQueueNotFoundException

---

Remove messages from the program message queue of the caller's caller.

#### Syntax
<pre class="prettyprint"> **BegSr RemoveMessage Access(*Protected) Type(Void)
   DclSrParm *messageKey*  Type(*String)** </pre>

#### Parameters
<dl>
        <dt>
 *messageKey* 
        </dt>
        <dd>String.  The unique identification key of the
        message to remove, or a keyword identifying a class of one
        or more messages to remove (see Remarks below).</dd>
</dl>

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <th>Value</th>
            <th>Condition</th>
          </tr>
          <tr>
            <td>            MessageQueueNotFoundException</td>
            <td>The message queue was not
            found in the invocation stack.</td>
          </tr>
          <tr>
            <td>            UnsupportedOperationException</td>
            <td>Currently, the Monarch
            Framework only supports the keyword "*ALL"
            for the value of 
 *messageKey* .</td>
          </tr>
</table>

#### Remarks
**RemoveMessage** may be used to remove one or more messages placed on a program message queue by a prior call to [ SendProgramMessage](amfProgramClassSendProgramMessageMethods.html). Messages are removed from the program message queue corresponding to the calling program of the caller of this method.

Note that invoking this method is equivalent to calling the two-method overload with the value of "*PRV *" for the program queue parameter; e.g. RemoveMessage("*PRV *", *messageKey* ).

*messageKey* may be a value returned by a preceding call to **SendProgramMessage** . In this case, the message in the **SendProgramMessage** call is removed. Alternately, the value of *messageKey* may be the keyword "*ALL", indicating that all messages on the program message queue should be removed. NOTE: currently, the Monarch Framework only supports the keyword "*ALL" for the value of *messageKey* .
<!-- -->

 <!-- start -->

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
            <td>ASNA.VisualRPG.Runtime.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[Program Class](amfProgramClass.html) <br /> [Program Class Members](amfProgramClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
