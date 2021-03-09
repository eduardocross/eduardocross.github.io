---
title: 5250 Terminal Menus

Id: TerminalMenuBar
TocParent: TerminalEmulation
TocOrder: 40

keywords: ASNA Browser Terminal
keywords: ASNA Browser Terminal, 5250 terminal menus
keywords: 5250 terminal menus, menu bar
keywords: menu bar
keywords: 5250 terminal menus, function key menu
keywords: function key menu
keywords: function key menu, changing colors
keywords: function key menu, terminal help
keywords: function key menu, exit
keywords: changing colors
keywords: terminal help
keywords: exit
keywords: macros
keywords: function key menu, macros
keywords: function key menu, FKeyPH
keywords: Asna5250Terminal.aspx
keywords: ASNA Browser Terminal, Asna5250Terminal.aspx
keywords: Asna5250Terminal.aspx, PageScriptPH
keywords: Asna5250Terminal.aspx, FKeyPH
keywords: Asna5250Terminal.aspx, MasterPage.master
keywords: MasterPage.master
keywords: MasterPage.master, PageScriptPH
keywords: MasterPage.master, FKeyPH
keywords: PageScriptPH
keywords: FKeyPH
keywords: Wings

---

<table>
			    <tr>

			       <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Browser Terminal&#8482; Admin Manual
				   </span><br /></td>
			    </tr>
</table>

# 5250 Terminal Menus

#### Menu Bar
The Menu bar is the banner that appears at the top to the ASNA 5250 Terminal Emulator with a distinctive background color. These menu options may be executed by pointing with the mouse and clicking the label.
<!-- end of introduction -->

The Menu bar may be collapsed by clicking on the small triangle at the top-left corner of the Terminal Emulator canvas. The "collapsed" state will remain as a browser local storage value. 

The Menu bar height is proportional to the height of a Terminal row. The font adjusts its size as the size of the Terminal changes. 

The Menu options are determined by the JavaScript in the **~/Themes/Current/Asna5250Terminal.aspx** page, right before the call to **WingsTerminal.renderDisplay_init** . The following is the default setup. (The Wings prefix is derived from ASNA Wings, another member of the [Monarch Family](emASNAfamily.html) that uses a similar terminal emulator.)
<pre class="prettyprint"><span style="color: blue">&lt;<span style="color: maroon">asp:Content</span> <span style="color: red">ID</span>="Content1" <span style="color: red">runat</span>="server" <span style="color: red">ContentPlaceHolderID</span>="PageScriptPH"&gt;</span>
  <span style="color: blue">&lt;<span style="color: maroon">script</span> <span style="color: red">type</span>="text/javascript"&gt;</span>
     WingsTerminal.addMenuBarMacro([<span style="color: maroon">'Hex'</span>, <span style="color: maroon">&#39;HEX'</span>]);
     WingsTerminal.addMenuBarMacro([<span style="color: maroon">'Clear'</span>, <span style="color: maroon">&#39;CLEAR'</span>]);
     WingsTerminal.addMenuBarMacro([<span style="color: maroon">'Erase'</span>, <span style="color: maroon">'ERASE'</span>]);
     WingsTerminal.addMenuBarMacro([<span style="color: maroon">'Attn'</span>, <span style="color: maroon">'ATTN'</span>]);
     WingsTerminal.addMenuBarMacro([<span style="color: maroon">'Help'</span>, <span style="color: maroon">'HELP'</span>]);

     WingsTerminal.renderDisplay_init(<span style="color: maroon">"85%","100%"</span>);
  <span style="color: blue">&lt;/<span style="color: maroon">script</span>&gt;
&lt;/<span style="color: maroon">asp:Content</span>&gt;</span></pre>

Where each macro executes the corresponding action shown in the [Keyboard Mapping](TerminalKeyboardMapping.html) topic. Any macro can be used to display Menu options on the Menu bar according to the rules described in [5250 Terminal Branding](TerminalKeyboardMacros">Keyboard Macros</a>.

**Note** : <br />Any of the labels shown as the first parameter in the WingsTerminal.addMenuBarMacro may be localized in any language.

#### Terminal Emulator Mobile Support
The Terminal Emulator supports mobile devices with an 
				additional set of "IBM keys" that appear at the top of the touch 
				screen when BTerm detects that the page is being veiwed by 
				a mobile device. These keys allow users access to Aid keys that 
				normally require a full IBM keyboard. They are sized to 
				comfortably fit a 
				large number of keys on the screen, with a slightly 
				smaller font and less bordering space than most default buttons. 

#### Master Page Function Key Menu
The MasterPage.master provides a place holder with ID 'FKeyPH' for active function keys to be displayed on each Wings page. This area can be customized to provide complete integration into your application. The default area is used by the 5250 Terminal Emulator to access functionality that pertains to the use of the ASNA 5250 Terminal emulation. The three default functions are as follows.

- CHANGE COLORS<br />

					There are three "Color schema" setting pages provided in the 
			   ASNA Browser Terminal projects under folder **Monarch/5250ColorSchemas** . The files are Earth.htm, Wind.htm,
                     and Fire.htm. Selection of this option will 
					redirect the browser to that folder and show a list of 
						these files so you can select one. The 
			   JavaScript in the file is executed setting the color values before being redirected back to the ASNA 5250 Terminal emulator page. To add an enhanced user interface see
						<a href="TerminalBranding.htm#DefaultColorSchemas">Changing Default Color Schemas</a>.
- TERMINAL HELP<br />This option redirects the browser to 
					a page that provides information on the use of the ASNA 5250 
					Terminal keyboard showing the action assignments.
- EXIT<br />This option redirects the browser to the 'End 
						of Job' page. This page code-behind includes a call to 
						abandon the browser session, which effectively 
						terminates the application and the associated job on 
						the IBM i.

Each of the function key area menu options is an HTML input element of type 'button', that has a click event assigned to execute a macro. The following shows the default settings in ~/Themes/Current/Asna5250Terminal.aspx.
<pre class="prettyprint"> &#60;asp:Content ID="FileContent1" runat="server" ContentPlaceHolderID="FKeyPH"&#62;

   &#60;input class="DdsKey" id="ChgColors" onclick="WingsTerminal.executeMacro(['Change Colors', 'REDIRECT:../../Monarch/5250ColorSchemas']);" 
         type="button" value="Change Colors" /&#62;
   &#60;input class="DdsKey" id="TermHelp"  onclick="WingsTerminal.executeMacro(['Terminal Help', 'REDIRECT:Asna5250TerminalHelp.htm']);" 
         type="button" value="Terminal Help" /&#62;
   &#60;input class="DdsKey" id="Exit"      onclick="WingsTerminal.executeMacro(['Exit', 'REDIRECT:../../Monarch/!EOj.aspx']);" 
         type="button" value="Exit" /&#62;

&#60;/asp:Content&#62;
</pre>

**Notes** :

1. The menu option label will appear in ALL UPPERCASE with a red font and a link-like hover affect. These styles are defined in the DdsKey CSS Class elements in the 
~/Themes/Current/Theme.css file.
2. When configuring macros to be associated with Menu options, if the 
						"REDIRECT:Page" action is used, make sure the destination Page has a way to redirect back to the ~/Themes/Current/Asna5250Terminal.aspx page.

#### Special Note:
The references to the directory location of Asna5250Terminal.aspx in the above information specify **~/Themes/Current/** as the location used. Refer to <a href="WebConfigAppSettings.htm#terminalfolder">Setting the location of the Asna5250Terminal.aspx page</a> for more information.

#### See Also
<dl>
  <dd><a href="TerminalBranding.html)</dd>
  <dd>[Keyboard Mapping](TerminalKeyboardMapping.html)</dd>
  <dd>[Keyboard Macros](TerminalKeyboardmacros.html)</dd>
</dl>

