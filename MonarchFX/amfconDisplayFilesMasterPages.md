---
title: ASNA Monarch Master Pages

Id: amfconDisplayFilesMasterPages
TocParent: amfconDisplayFilesThemeComponents
TocOrder: 20

keywords: display files, master pages
keywords: Web server controls [ASNA.Monarch], master pages
keywords: ASNA.Monarch.Web server controls, master pages
keywords: master pages
keywords: Web server controls, master pages
keywords: concepts, master pages
keywords: theme components, master pages

---

Monarch uses two master page files that contain the JavaScript coding that defines the master page layout with divisions identified by a <code><span style="color:maroon">ContentPlaceHolder</span> <span style="color:red">ID</span></code> matching the <code><span style="color:red">ContentPlaceHolderID</span></code> in the ASPX content pages. When an ASPX Content Page is requested, the content is merged with the Master Page, which creates a standardized look and behavior for all the ASPX and windows pages in your solution. The default master pages are located in the installation default location, which is **C:\Program Files (x86)\ASNA.Monarch 10.0\Templates\Themes\Current** or **C:\Program Files\ASNA.Monarch 10.0\Templates\Themes\Current** .

#### MasterPage.master
The Display File agents will use this master page file, MasterPage.master, when displaying ASPX pages. A partial master page example is shown below. 

Notice the first ID, <code>HeaderPH</code>. This identifies the place holder for the ASPX page header. The second ID, <code>FKeyPH</code>, identifies an area for function keys. The third and fourth ID&#39;s, <code>CenPH</code> and <code>MsgPH</code>, identifies the place for the main contents and a message line. This is where the majority of the individual ASPX content will be displayed for the user. A final placeholder section outside the form, ID <code>PageScriptPH</code>, is for any scripts that may be needed to execute on the page. 
<codesnippet enablecopycode="false" runat="server" containsmarkup="true" xmlns="http://msdn2.microsoft.com/mtps">
<pre class="example"><span style="color:green;">// section for header</span>
  <span style="color:blue;">&lt;<span style="color:Maroon;">head</span>&gt;
        &lt;<span style="color:Maroon;">asp:ContentPlaceHolder</span> <span style="color:red;">ID</span>=" **HeaderPH** " <span style="color:red;">runat</span>="server" /&gt;
  &lt;/<span style="color:Maroon;">head</span>&gt;
  &lt;<span style="color:Maroon;">body</span>&gt;
    &lt;</span><span class="maroon">form</span><span style="color:blue;">&gt;
<span style="color:green;">// division for function keys</span>
      &lt;<span style="color:Maroon;">div</span> <span style="color:red;">id</span>="Div1" &gt;
          &lt;<span style="color:Maroon;">asp:ContentPlaceHolder</span> <span style="color:red;">ID</span>=" **FKeyPH** " <span style="color:red;">runat</span>="server" /&gt;
      &lt;/<span style="color:Maroon;">div</span>&gt;

<span style="color:green;">// divisions for main page content and messages</span>          
      &lt;<span style="color:Maroon;">div</span> <span style="color:red;">id</span>="centralDiv" <span style="color:red;">class</span>="CenPH" &gt;
          &lt;<span style="color:Maroon;">asp:ContentPlaceHolder</span> <span style="color:red;">ID</span>=" **CenPH** " <span style="color:red;">runat</span>="server" /&gt;
      &lt;/<span style="color:Maroon;">div</span>&gt;                  
      &lt;<span style="color:Maroon;">div</span> <span style="color:red;">id</span>="msgDiv" &gt;
          &lt;<span style="color:Maroon;">asp:ContentPlaceHolder</span> <span style="color:red;">ID</span>=" **MsgPH** " <span style="color:red;">runat</span>="server" /&gt;
      &lt;/<span style="color:Maroon;">div</span>&gt;    
<span style="color:green;">// section outside the form for page script</span>                 
    &lt;/<span style="color:Maroon;">form</span>&gt;
         &lt;<span style="color:Maroon;">asp:ContentPlaceHolder</span> <span style="color:red;">ID</span>=" **PageScriptPH** " <span style="color:red;">runat</span>="server" /&gt;
  &lt;/<span style="color:Maroon;">body</span>&gt;</span></pre>
         </codesnippet>

The master page code-behind file used when your project is created will depend upon the type of project and the language being used; AVR, C#, or Visual Basic. There are three default code-behind files for this master page.
<dl>
		   <dt>MasterPage.master</dt>
		   <dd>MasterPage.master.vr - This is the code-behind page for ASNA Visual RPG language projects.</dd>
		   <dd>MasterPage.master.cs - This is the code-behind page for C# language projects.</dd>
		   <dd>MasterPage.master.vb - This is the code-behind page for Visual Basic language projects.</dd>
</dl>

#### MasterPage.Window.master
The Display File agents will switch to use this master page when a DDS Record as a <code>WINDOW</code> is encountered. This is specifically useful on pop-up windows to standardize the layout of the content with the defined element placement and coloring controlled by the Windows Master Page. 

This file is very similar to the normal master page above. The content placeholders have a different class, but the content place holder ids are the same as shown below. This allows a content page to be displayed easily by either master page.
<table class="mytable" width="90%" cellpadding="4" cellspacing="0">
                        <colgroup><col width="15%" />
                        <col  width="15%" />
                        <col  width="15%" />
                        <col  width="15%" />
                        <col  width="15%" />
                        <col  width="15%" />
                        </colgroup>
                            <tr>
                                <th colspan="3">MasterPage.master</th>
                                <th colspan="3">MasterPage.Window.master</th>
                            </tr>
                           <tr>
                                <th>Division id</th>
                                <th>Class</th>
                                <th>ContentPH ID</th>
                                <th>Division id</th>
                                <th>Class</th>
                                <th>ContentPH id</th>
                            </tr>
										<tr>
											<td>None</td>
											<td> **None** </td>
											<td><code>HeaderPH</code></td>
											<td>None</td>
											<td> **None** </td>
											<td><code>HeaderPH</code></td>
										</tr>

										<tr>
											<td><code>FunkeyDiv</code></td>
											<td><code> **FKeyPH** </code></td>
											<td><code>FKeyPH</code></td>
											<td><code>FunkeyDiv</code></td>
											<td><code> **FKeyWinPH** </code></td>
											<td><code>FKeyPH</code></td>
										</tr>

										<tr>
											<td><code>centralDiv</code></td>
											<td><code> **CenPH** </code></td>
											<td><code>CenPH</code></td>
											<td><code>centralDiv</code></td>
											<td><code> **CenWinPH** </code></td>
											<td><code>CenPH</code></td>
										</tr>

										<tr>
											<td><code>msgDiv</code></td>
											<td><code> **MsgPH** </code></td>
											<td><code>MsgPH</code></td>
											<td><code>msgDiv</code></td>
											<td><code> **MsgWinPH** </code></td>
											<td><code>MsgPH</code></td>
										</tr>

										<tr>
											<td>None</td>
											<td> **None** </td>
											<td><code>PageScriptPH</code></td>
											<td>None</td>
											<td> **None** </td>
											<td><code>PageScriptPH</code></td>
										</tr>

</table>

The master page code-behind file used when your project is created will depend upon the type of project and the language being used; AVR, C#, or Visual Basic. There are three default code-behind files for this master window page.
<dl>
		   <dt>MasterPage.Window.master</dt>
		   <dd>MasterPage.Window.master.vr &#8211; This is the code-behind page for ASNA Visual RPG language projects.</dd>
		   <dd>MasterPage.Window.master.cs &#8211; This is the code-behind page for C# language projects.</dd>
		   <dd>MasterPage.Window.master.vb &#8211; This is the code-behind page for Visual Basic language projects.</dd>
</dl>

#### Next: [ASNA Cascading Style Sheets](amfconDisplayFilesStyleSheets.html)

#### Previous: [ASNA Monarch Templates](amfconDisplayFilesTemplates.html)

#### See Also
<dl>

        <dd>[Web
        Server Controls Overview](amfWebServerControlsOverview.html)</dd>
</dl>

