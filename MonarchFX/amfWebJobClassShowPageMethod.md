---
title: WebJob.ShowPage Method

Id: amfWebJobClassShowPageMethod
TocParent: amfWebJobClassMethods
TocOrder: 60

keywords: how to, initiating web conversation
keywords: web job, initiating conversation
keywords: web job, using non-display files
keywords: ShowPage method
keywords: WebJob.ShowPage method
keywords: non-display file aspx.vr, show page
keywords: aspx.vr, non-display file, show page
keywords: Web server controls, non-display file aspx.vr showing page
keywords: Web server controls [ASNA Monarch], non-display file aspx.vr showing page
keywords: MONARCH_CMDPARM

---

Prepares a job to accept commands by presenting an ASPX page to initiate the conversation with the user.

#### Syntax
<pre class="prettyprint"><code class="avr"> **BegFunc ShowPage Access(*Public) Type(*String)
  DclSrParm *outsidePage*  Type (*String)
  DclSrParm *parameter*  Type (*String)**  </code></pre>

#### Parameters
<dl>
        <dt>
          <code> *outsidePage* </code>
        </dt>
        <dd>A string containing the name of the ASPX page presented
        to the user to initiate the conversation.</dd>
        <dt>
          <code> *parameter* </code>
        </dt>
        <dd>The string parameter that will be stored in the session
        object where the ASPX code behind can retrieve it.</dd>
</dl>

<!--mine -->

#### Return Value
**String** containing values being returned.

#### Remarks
The ASPX code behind can retrieve the parameter like this:
<pre class="prettyprint">Parameter = Session["MONARCH_CMDPARM"] <span style="color:#0000ff">*as</span><span style="color:gray">*String</span>
   Session["MONARCH_CMDPARM"] = <span style="color:#0000ff">*Nothing</span></pre>

<!-- start -->

#### Example
**In the blue thread:** 
<pre class="example"><span style="color:#0000ff">DclFld</span> Result <span style="color:#0000ff">Type</span>(<span style="color:gray">*String</span>)
   Result = (monarchJob <span style="color:#0000ff">*as</span> ASNA.Monarch.WebJob).ShowPage("~/Clifton.aspx", "23,ABC,X")
   <span style="color:#0000ff">If</span> (Result = "Function Completed")
<span style="color:#0000ff">      Return
   EndIf</span></pre>

**In 'Clifton.aspx' in the yellow thread:** 
<pre class="example"><span style="color:#0000ff">BegSr</span> Page_Load <span style="color:#0000ff">Access</span>(<span style="color:gray">*Private</span>) <span style="color:#0000ff">Event</span>(<span style="color:#0000ff">*This</span>.Load)
  <span style="color:#0000ff">DclSrParm</span> sender <span style="color:#0000ff">Type</span>(<span style="color:gray">*Object</span>)
  <span style="color:blue">DclSrParm</span> e <span style="color:#0000ff">Type</span>(System.EventArgs)
  <span style="color:#0000ff">DclArray</span>  Parms <span style="color:#0000ff">Rank</span>(1) <span style="color:#0000ff">Type</span>(<span style="color:gray">*String</span>)
  <span style="color:#0000ff">DclFld</span>    Parameters <span style="color:#0000ff">Type</span>(<span style="color:gray">*String</span>)
    <span style="color:#0000ff">If</span> (NOT Page.IsPostBack)
      Parameter = Session["MONARCH_CMDPARM"] <span style="color:#0000ff">*as</span><span style="color:gray">*String</span>
      Session["MONARCH_CMDPARM"] = <span style="color:#0000ff">*Nothing</span>
      <span style="color:#0000ff">If</span> (Parameter = *Nothing)       
        Response.Redirect("./PageRequestOutOfSequence.html")
<span style="color:#0000ff">      EndIf</span>
        Parms = Parameter.Split(O',')
        txtCustNumber.Text = Parms[0]
<span style="color:#0000ff">   EndIf
EndSr</span></pre>

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
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016,  Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[WebJob Class](amfWebJobClass.html) <br /> [WebJob Class Members](amfWebJobClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
