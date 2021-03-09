---
title: Page Class

Id: amfPageClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 650

keywords: Page class, about Page class
keywords: .aspx files
keywords: ASP.NET pages
keywords: ASP.NET Web sites, pages
keywords: aspx files
keywords: aspx files, pages
keywords: code-behind pages, ASNA.Monarch pages
keywords: code-behind classes, ASNA.Monarch pages
keywords: visual elements of Web pages
keywords: Web applications [ASNA.Monarch], pages
keywords: Web sites [ASNA.Monarch], pages

---

Monarch display files are based on the ASP.Net **System.Web.UI.Page** and serves as a container of all records formats and is responsible for coordinating the flow of data between the Workstation and Display files.

For a list of all members of this type, see [Page Members](amfPageClassMembers.html).
<!-- end of introduction -->

<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
 **ASNA.Monarch.WebDspF.Page** </pre>

#### Syntax
<pre class="prettyprint"> **BegClass Page Access(*public) Inherits(System.Web.UI.Page)**  </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
Besides the normal phases that an ASPX goes through in ASP.NET, there are enhanced or additional phases specific to Monarch that a display file goes through. These phases take place when the page is in the ASP.NET Prerender phase (see [ Control Execution Lifecycle)](amfconControlExecutionLifecycle.html)

Refer to [Moving Data in an ASPX Session](amfconFrameworkASPXSessionMovingData.html) for more information on the concepts behind the **Page** class. And see [Data Flow Overview](amfDataFlow.html) for more information on the methods that can be used to get or set field and indicator values.
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl><dd>
        [
        ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
        <dd>[Page
        Members](amfPageClassMembers.html)</dd>
        <dd>[Moving Data
        in an ASPX Session](amfconFrameworkASPXSessionMovingData.html)</dd>
</dl>

