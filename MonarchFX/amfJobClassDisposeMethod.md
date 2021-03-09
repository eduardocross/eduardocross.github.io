---
title: Job.Dispose Method

Id: amfJobClassDisposeMethod
TocParent: amfJobMethods
TocOrder: 40

keywords: Dispose method
keywords: Job.Dispose method
keywords: managed resources, releasing
keywords: unmanaged resources, releasing
keywords: jobs, releasing resources
keywords: how to, release job resources
keywords: how to, release managed job resources
keywords: how to, release unmanaged job resources

---

Releases resources used by the **Job** object.
<!-- start -->

#### Syntax
<pre class="prettyprint"> **BegSr Dispose Access(*Public) Type(void)
   DclSrParm *disposing*  Type(*Boolean)**       </pre>

#### Parameters
<dl>
        <dt>
 *disposing* 
        </dt>
        <dd>Boolean. Set 
 **true**  to release both managed and unmanaged
        resources; otherwise set 
 **false**  to release just unmanaged
        resources.</dd>
</dl>

#### Remarks
When the **Job** is being disposed of, it can no longer be referenced. Even though the instance of a **Job** object is disposed of, it is still in memory until removed through garbage collection.
<!-- start -->

#### Examples
<pre class="prettyprint"> <code class="language-avr">BegSr Dispose Access(*Public)Modifier(*Overrides)
    DclSrParm disposing Type(*Boolean)
    If disposing
      Disconnect MyDatabase
      Disconnect MyPrinterDB
      Close SDP100D
    EndIf *Base.Dispose(Disposing)
EndSr</code></pre>

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
            <td style="height: 29px">Assembly:</td>
            <td style="height: 29px">ASNA.VisualRPG.Runtime.</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[Job Class](amfJobClass.html) <br clear="none" /> [Job Class Members](amfJobMembers.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
