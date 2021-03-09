---
title: WebDevice.AbEndMessage Field

Id: amfWebDeviceClassAbEndMessageField
TocParent: amfWebDeviceClassFields
TocOrder: 20

keywords: AbEndMessage field
keywords: WebDevice.AbEndMessage field
keywords: device control, abnormal termination message
keywords: abnormal termination message
keywords: how to, abnormal termination message

---

The abnormal device terminate message.

#### Syntax
<pre class="prettyprint"> **BegProp AbEndMessage Access(*Public) Type(*String)**       </pre> 

<!--mine -->

#### Field Value
String. An abnormal termination message.

#### Examples
<pre class="prettyprint">DclFld lblStackTrace Type(System.Web.UI.WebControls.Label) Access(*Protected) WithEvents(*Yes)
DclFld lblMessage Type(System.Web.UI.WebControls.Label) Access(*Protected) WithEvents(*Yes)
BegSr Page_Load Event(*this.Load)
     DclSrParm Name(Sender) Type(*Object)
     DclSrParm Name(e) Type(System.EventArgs)

     DclFld Device Type(ASNA.Monarch.WebDevice)
     Device = Session["Device"] *as ASNA.Monarch.WebDevice
     If (Device = *Nothing )
         Response.Redirect( "!ExpiredSession.htm" )
     EndIf
     lblMessage.Text    = Device.
 **AbEndMessage** 
     lblStackTrace.Text = Device.AbEndStack
     Session.Abandon()
 EndSr
</pre>

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
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

#### See Also
[WebDevice Class](amfWebDeviceClass.html) <br /> [ WebDevice Class Members](amfWebDeviceClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
