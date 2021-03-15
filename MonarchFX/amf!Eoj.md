---
title: !EoJ

Id: amf!Eoj
TocParent: amf!PagesMain
TocOrder: 20

keywords: !EoJ
keywords: !Pages, !EoJ
keywords: !Pages
keywords: end of job
keywords: redirecting user to main menu
keywords: end of job, !EoJ.Aspx
keywords: end of job, !EoJ.Aspx.Vr
keywords: !EoJ.Aspx
keywords: !EoJ.Aspx.Vr
keywords: session, using Page_Load

---

<!-- six -->

**!EoJ** is an application "End of Job" page. Use !Eoj to redirect the user to the main menu or home page. This file is replaceable by the Migrator and is delivered as "!EoJ.aspx", "!EoJ.aspx.vr" (AVR), "!EoJ.aspx.vb" (Visual Basic), and "!EoJ.aspx.cs" (C#).
<dl>
        <dd>![end of job image](Images/Eoj1.jpg)</dd>
</dl>

#### Example
<pre class="example"><span style="color: blue">BegSr </span>Page_Load <span style="color: blue">Event</span>(*this.Load)
    DclSrParm <span style="color: blue">Name</span> (Sender) <span style="color: blue">Type</span>(*Object)
    DclSrParm <span style="color: blue">Name</span>(3) <span style="color: blue">Type</span>(System.EventArgs)
    Session.Abandon()
<span style="color: blue">EndSr</span></pre> 

#### See Also
<dl>
        <dd>[!Diagnose](amf!Diagnose.html)</dd>
       <dd>[!ExpiredSession](amf!SessionExpired.html)</dd>
</dl>

