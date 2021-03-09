---
title: WebDisplayFile.InitMessageSubfile Method

Id: amfWebDisplayFileClassInitMessageSubfileMethod2
TocParent: amfWebDisplayFileClassMethods
TocOrder: 80

keywords: InitMessageSubfile method
keywords: WebDisplayFile.InitMessageSubfile method
keywords: messages
keywords: messages, initializing subfiles for display file
keywords: how to, initialize display file for message subfiles
keywords: display files, initializing for message subfiles

---

Constructs a new instance of a **WebDisplayFile** object for the message subfile and program queue with option indicators specified.

#### Syntax
<pre class="prettyprint"><code class="language-avr"> **BegSr InitMessageSubfile Access(*Public) Type(Void)
   DclSrParm *subfileName*  Type(*String)
   DclSrParm *programQ*  Type(*String)
   DclSrParm *optionIndicators*  Type(*Char) Rank(1)** </code></pre>

#### Parameters
<dl>
        <dt>
 *subfileName* 
        </dt>
        <dd>

String. The message subfile name to be associated with the display file.
</dd>
        <dt>
 *programQ* 
        </dt>
        <dd>

String. The name of the program queue handling the message subfile.
</dd>
        <dt>
 *optionIndicators* 
        </dt>
        <dd>A character array containing the option
        indicators.</dd>
</dl>
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
            <td>ASNA.VisualRPG.Runtime.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td>Windows Server 2008 R2, Windows Server 2012,  Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ WebDisplayFile Class](amfWebDisplayFileClass.html) <br /> [ WebDisplayFile Members](amfWebDisplayFileClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html)
