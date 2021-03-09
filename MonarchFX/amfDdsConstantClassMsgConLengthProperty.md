---
title: DdsConstant.MsgConLength Property

Id: amfDdsConstantClassMsgConLengthProperty
TocParent: amfDdsConstantClassPropertiesMain
TocOrder: 30

keywords: MsgConLength property
keywords: DdsConstant.MsgConLength property
keywords: Web server controls [ASNA.Monarch], setting MSGCON length
keywords: how to, set MSGCON length
keywords: how to, get MSGCON length
keywords: message files, setting MSGCON length
keywords: message files, getting MSGCON length
keywords: web controls, setting MSGCON length
keywords: web controls, getting MSGCON length
keywords: field controls, MSGCON length
keywords: MSGCON, message length

---

Gets or sets an integer containing the maximum number of characters to copy from the message. 

#### Syntax
<pre class="prettyprint"> **BegProp MsgConLength Access(*Public) Type(*Integer)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. An integer containing the maximum number of characters to copy from the message. If the message file contains a longer text for the message ID ( **MsgConId** ), the text in the constant will be truncated. Note: This property is different from the Web control&#39;s inherited **Length** property.

#### Remarks
If message file contains a larger text for the message ID, the text in the constant will be truncated. Note: This property is different from the Web control&#39;s inherited **Length** property.

#### Example
Before we look at an example of the usage of **MsgConLength** , [MsgCondId](amfDdsConstantClassMsgConIdProperty.html), and [MsgConFile](amfDdsConstantClassMsgConFileProperty.html), review the following example of the ILE usage of MSGCON.
<pre class="prettyprint">
 |...+....1....+....2....+....3....+....4....+....5....+....6....+....7....+....8
00010A          R RECORD1
00020A                                  2  1MSGCON(10 MSG0001 MESSAGE/MSGF)
     A</pre>
In the example you will notice three parameters: message length (10), message id (MSG0001), and library(Message/) message file name (MSGF). These three parameters in Monarch are the values in MsgConLength, MsgCondId, and MsgConFile, with ONE exception. The absolute path to the message file named will be generated at run-time by appending the MsgConFile value to the value of **MonarchMessageFileFolder** entry in Web.Config. For example, assume that the the following value has been set in the appSettings in the Web.config file.
<pre class="prettyprint"><span style="color:blue">&lt;<span style="color:Maroon">appSettings</span><span style="color:red;"> file</span>=<span style="color:black;">"</span>AppSettings.Config<span style="color:black;">"</span>&gt;
 **&lt;<span style="color:Maroon">add</span><span style="color:red;"> key</span>=<span style="color:black">"</span>MonarchMessageFileFolder<span style="color:black;">"</span> <span style="color:red;">value</span>=<span style="color:black;">"</span>~\MessageFiles\<span style="color:black;">"</span> /&gt;** 
&lt;/<span style="color: maroon">appSettings</span>&gt; </span></pre>
With that assumption, "~\MessageFiles\MSGF" would be the concatenated value for the message file name at runtime.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
        <dd>[DdsConstant Class](amfDdsConstantClass.html)</dd>
        <dd>[DdsConstant Class Members](amfDdsConstantClassMembers.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
        <dd>[DdsConstant MsgConFile Property](amfDdsConstantClassMsgConFileProperty.html)</dd>
        <dd>[DdsConstant MsgConId Property](amfDdsConstantClassMsgConIdProperty.html)</dd>
        <dd>[Web.config Considerations](amfconWebConfigConsiderations.html)</dd>
</dl>

