---
title: ASNA Monarch Templates

Id: amfconDisplayFilesTemplates
TocParent: amfconDisplayFilesThemeComponents
TocOrder: 10

keywords: templates, for ASPX display files
keywords: display files, ASPX templates
keywords: Web server controls [ASNA.Monarch], ASPX display file templates
keywords: ASNA.Monarch.Web server controls, ASPX templates
keywords: Templates.aspx, about
keywords: Web server controls, migration ASPX display file templates
keywords: concepts, ASPX display file templates
keywords: theme components, ASPX display file template

---

The main purpose of a template is to define the default aspx content page layout for the Migration Agents when display files are imported into the solution. The template files are provided with the installation of ASNA Monarch Framework. The default templates are located in the installation default location, which is **C:\Program Files (x86)\ASNA Monarch 80\Templates\DisplayFiles** or **C:\Program Files\ASNA Monarch 80\Templates\DisplayFiles** .

The Templates used when your project is created will depend upon the type of project and the language being used; AVR, C#, or Visual Basic. There are four default aspx template files included with the installation that are listed below.
<dl>
		   <dt> **Template.aspx** </dt>
		   <dd>This defines a standardized aspx display file content page that will be combined with the 
		   [master page definition](amfconDisplayFilesMasterPages.html) when the aspx 
		   is displayed, regardless of the project language.</dd>
		   <dt> **Template.aspx.vr** </dt>
		   <dd>This is the code-behind page for ASNA Visual RPG language projects.</dd>
		   <dt> **Template.aspx.cs** </dt>
		   <dd>This is the code-behind page for C# language projects.</dd>
		   <dt> **Template.aspx.vb** </dt>
		   <dd>This is the code-behind page for Visual Basic language projects.</dd>
</dl>

#### Template.aspx
The following is a partial sample of the default Template.aspx file. Make special note of the <code><span style="color:red">ContentPlaceHolderID</span></code> values as you will see them again in the Master pages and the display file aspx pages. 
<codesnippet enablecopycode="false" runat="server" containsmarkup="true" xmlns="http://msdn2.microsoft.com/mtps">
		   <pre class="example"><span style="color:green;">// section for header</span>
<span style="color:blue;">&lt;<span style="color:Maroon;">asp</span>:<span style="color:Maroon;">Content</span> <span style="color:red">ContentPlaceHolderID</span>=" **HeaderPH** " <span style="color:red;">runat</span>="server" /&gt;
&lt;/<span style="color:Maroon;">asp</span>:<span style="color:Maroon;">Content</span>&gt;

 <span style="color:green;">// section for function keys</span>
<span style="color:blue;">&lt;<span style="color:Maroon;">asp</span>:<span style="color:Maroon;">Content</span> <span style="color:red;">ID</span>="FileContent1" <span style="color:red;">runat</span>="server" <span style="color:red">ContentPlaceHolderID</span>=" **FKeyPH** "&gt;
   &lt;<span style="color:Maroon;">div</span> <span style="color:red;">id</span>="Div0"&gt;
      &lt;<span style="color:Maroon;">mdf</span>:<span style="color:Maroon;">ddsfile</span> <span style="color:red;">id</span>="DdsFile1" <span style="color:red;">runat</span>="server" <span style="color:red;">DisplayErrorMessages</span>="False" <span style="color:red;">BannerStyle</span>="Vertical"&gt;
      &lt;/<span style="color:Maroon;">mdf</span>:<span style="color:Maroon;">ddsfile</span>
   &lt;/<span style="color:Maroon;">div</span>&gt;
&lt;/<span style="color:Maroon;">asp</span>:<span style="color:Maroon;">Content</span>&gt;

<span style="color:green;">// section for main page content</span> 
<span style="color:blue;">&lt;<span style="color:Maroon;">asp</span>:<span style="color:Maroon;">Content</span> <span style="color:red;">ID</span>="FileContent2" <span style="color:red;">runat</span>="server" <span style="color:red">ContentPlaceHolderID</span>=" **CenPH** "&gt;
   &lt;<span style="color:Maroon;">div</span> <span style="color:red;">id</span>="Div1"&gt;
      &lt;<span style="color:Maroon;">mdf</span>:<span style="color:Maroon;">ddsrecord</span> <span style="color:red;">id</span>="DdsRecord1" <span style="color:red;">style</span>="<span style="color:red;">POSITION</span>:relative" <span style="color:red;">runat</span>="server" 
                      <span style="color:red;">Height</span>="64px" <span style="color:red;">Width</span>="712px" <span style="color:red;">ms_positioning</span>="GridLayout"&gt;
      &lt;/<span style="color:Maroon;">mdf</span>:<span style="color:Maroon;">ddsrecord</span>
   &lt;/<span style="color:Maroon;">div</span>&gt;
&lt;/<span style="color:Maroon;">asp</span>:<span style="color:Maroon;">Content</span>&gt;

<span style="color:green;">// section for messages</span> 
<span style="color:blue;">&lt;<span style="color:Maroon;">asp</span>:<span style="color:Maroon;">Content</span> <span style="color:red;">ID</span>="FileContent3" <span style="color:red;">runat</span>="server" <span style="color:red">ContentPlaceHolderID</span>=" **MsgPH** "&gt;
   &lt;<span style="color:Maroon;">div</span> <span style="color:red;">id</span>="Div2"&gt;
      &lt;<span style="color:Maroon;">mdf</span>:<span style="color:Maroon;">DdsMessagePanel</span> <span style="color:red;">ID</span>="DdsMessagePanel1" <span style="color:red;">style</span>="<span style="color:red;">POSITION</span>:relative" <span style="color:red;">runat</span>="server" 
                      <span style="color:red;">Height</span>="64px" <span style="color:red;">ms_positioning</span>="GridLayout"&gt;
      &lt;/<span style="color:Maroon;">mdf</span>:<span style="color:Maroon;">DdsMessagePanel</span>
   &lt;/<span style="color:Maroon;">div</span>&gt;
&lt;/<span style="color:Maroon;">asp</span>:<span style="color:Maroon;">Content</span>&gt;

<span style="color:green;">// section outside the form for page script</span>
<span style="color:blue;">&lt;<span style="color:Maroon;">asp</span>:<span style="color:Maroon;">Content</span> <span style="color:red">ContentPlaceHolderID</span>=" **PageScriptPH** " <span style="color:red;">runat</span>="server" &gt;
&lt;/<span style="color:Maroon;">asp</span>:<span style="color:Maroon;">Content</span>&gt;</span>
</span></span></span></span></pre>
		   </codesnippet>

Always refer to the actual file which is located in the installation default location, **C:\Program Files (x86)\ASNA Monarch 80\Templates\DisplayFiles** or **C:\Program Files\ASNA Monarch 80\Templates\DisplayFiles** for the most current styles. 

#### Next: [ASNA Master Pages](amfconDisplayFilesMasterPages.html)

#### Previous: [ASNA Theme Components](amfconDisplayFilesThemeComponents.html)

#### See Also
<dl>
			   <dd>[ASNA Cascading Style Sheets](amfconDisplayFilesStyleSheets.html)
			   </dd>
</dl>

