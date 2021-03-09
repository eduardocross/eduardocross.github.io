---
title: 5250 Terminal Branding

Id: TerminalBranding
TocParent: TerminalEmulation
TocOrder: 10

keywords: ASNA Browser Terminal
keywords: ASNA Browser Terminal, terminal branding
keywords: ASNA Browser Terminal, 5250 terminal emulation colors
keywords: 5250 terminal emulation colors
keywords: 5250 terminal emulation colors, changing
keywords: changing 5250 terminal emulation colors
keywords: 5250 terminal menus, function key menu
keywords: function key menu
keywords: function key menu, changing colors
keywords: changing colors
keywords: changing colors, PageScriptPH
keywords: client side local storage
keywords: macros
keywords: function key menu, macros
keywords: function key menu, FKeyPH
keywords: Asna5250Terminal.aspx
keywords: ASNA Browser Terminal, Asna5250Terminal.aspx
keywords: Asna5250Terminal.aspx, PageScriptPH
keywords: Asna5250Terminal.aspx, FKeyPH
keywords: PageScriptPH
keywords: FKeyPH
keywords: BTERM

---

<table>
			    <tr>

			       <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Browser Terminal&#8482; Admin Manual
				   </span><br /></td>
			    </tr>
</table>

# 5250 Terminal Branding

#### Changing Color and/or Background Defaults
The end user is able to change the colors of the Terminal Emulator using the Change Colors option, but in order to modify the defaults, changes should be made to the CSS file Framework.css.

The following styles in Framework.css set the default colors:
<pre class="prettyprint"><code class="css">    .AsnaTermDEF_GREEN      { color: #00FF00; }
    .AsnaTermDEF_BKGD       { color: #000000; }
    .AsnaTermDEF_BLUE       { color: #0099FF; }
    .AsnaTermDEF_RED        { color: #FF0000; }
    .AsnaTermDEF_WHITE      { color: #FFFFFF; }
    .AsnaTermDEF_TURQUOISE  { color: #AFEEEE; }
    .AsnaTermDEF_YELLOW     { color: #FFFF00; }
    .AsnaTermDEF_PINK       { color: #FF1493; }
    .AsnaTermDEF_CURSOR     { color: #FFFFFF; }
    .AsnaTermDEF_SEL        { color: #FFFFFF; }</code></pre>

Modifying the colors in the .css will alter the defaults, but end users can still modify the colors locally using the options on the "color picker" panel. End users can also reset to the defaults by clicking the "Restore Defaults" button on the color picker.

In the event of a conflict or one of the colors being absent in Framework.css, the terminal emulator will fall back on the colors defined the client's local storage, as outlined in the following table: 
<table  class="mytable" cellpadding="4" cellspacing="0" width="50%"><colgroup><col width="50%" /><col width="50%" /></colgroup>

						<tr>
							<th>Item Key </th>

							<th>Default Value (Some values shown with black 
							background for easier viewing.)</th>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.greenColor</td>

							<td><span style="color:#00FF00">&#39;#00FF00&#39;</span></td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.blackColor</td>

							<td><span style="color:#000000">&#39;#000000&#39;</span></td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.blueColor</td>

							<td>&#39;<span style="color:#0099FF">#0099FF&#39;</span></td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.redColor </td>

							<td><span style="color:#FF0000">&#39;#FF0000&#39;</span></td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.whiteColor</td>

							<td><span style="color:#FFFFFF; background:black">&#39;#FFFFFF&#39;</span> </td>
						</tr>
						<tr>
							<td style="height: 27px">ASNA.5250Terminal.turquoiseColor</td>

							<td style="height: 27px"> <span style="color:#AFEEEE; background:black">&#39;#AFEEEE&#39;</span></td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.yellowColor</td>

							<td><span style="color:#FFFF00; background:black">&#39;#FFFF00&#39;</span> </td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.pinkColor</td>

							<td><span style="color:#FF1493; background:black">&#39;#FF1493&#39;</span></td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.backgroundColor</td>

							<td>&#39;#000000&#39;</td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.cursorColor</td>

							<td><span style="color:#FFFFFF; background:black">&#39;#FFFFFF&#39;</span></td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.selectColor</td>

							<td><span style="color:#FFFFFF; background:black">&#39;#FFFFFF&#39;</span></td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.menubarTextColor</td>

							<td>&#39;#000000&#39;</td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.menubarColor</td>

							<td><span style="color:#FFFFFF; background:black">&#39;#FFFFFF&#39;</span></td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.menubarBackgroundImage</td>

							<td>&#39;url(Images/menubar_terminal_default.jpg)'</td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.menubarBackgroundRepeat</td>

							<td>'repeat-y'</td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.statusbarTextColor</td>

							<td>'#000000'</td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.statusbarColor</td>

							<td><span style="color:#FFFFFF; background:black">&#39;#FFFFFF&#39;</span></td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.statusbarBackgroundImage</td>

							<td>&#39;url(Images/statusbar_terminal_default.jpg)'</td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.statusbarBackgroundRepeat</td>

							<td>'repeat-y'</td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.backgroundRepeat</td>

							<td>'no-repeat'</td>
						</tr>
						<tr>
							<td>ASNA.5250Terminal.menuColorsRedirectLocation</td>

							<td>'5250ColorSchemas'</td>
						</tr>
</table>

It's also possible (but not reccommended) to change the default colors and /or background images by changing the entries in the client local storage with JavaScript, **before** calling the renderDisplayInit function by following the steps below.
1. Edit the Asna5250Terminal.aspx markup.
2. Identify the JavaScript code at the bottom of the page
					in the ContentPlaceHolderID = PageScriptPH.
	<pre class="prettyprint"><span style="color: blue">&lt;<span style="color: maroon">asp:Content</span> <span style="color: red">ID</span>="Content1" <span style="color: red">runat</span>="server" <span style="color: red">ContentPlaceHolderID</span>=" **PageScriptPH** "&gt;</span>
  <span style="color: blue">&lt;<span style="color: maroon">script</span> <span style="color: red">type</span>="text/javascript"&gt;</span>
     . . .
     . . .
     WingsTerminal.renderDisplay_init(<span style="color: maroon">"85%","100%"</span>);
  <span style="color: blue">&lt;/<span style="color: maroon">script</span>&gt;
&lt;/<span style="color: maroon">asp:Content</span>&gt;</span></pre>
3. Add entries with your new defaults, BEFORE the call to the function renderDisplay_init(). The following example 
demonstrates the entries you could add.
<pre class="prettyprint"><span style="color: blue">&lt;<span style="color: maroon">asp:Content</span> <span style="color: red">ID</span>="Content1" <span style="color: red">runat</span>="server" <span style="color: red">ContentPlaceHolderID</span>="PageScriptPH"&gt;</span>
   <span style="color:blue">&lt;<span style="color:maroon">Script</span> <span style="color:red">type</span>="text/javascript"&gt;
      . . .
      . . .
      var</span> keyNamespace = <span style="color:maroon">'ASNA.5250Terminal.'</span>;

      localStorage.setItem(keyNamespace + <span style="color: maroon">'greenColor'</span>, <span style="color: maroon"> *newGreenDefault* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'blackColor'</span>, <span style="color: maroon"> *newBlackDefault* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'blueColor'</span>, <span style="color: maroon"> *newBlueDefault* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'redColor'</span>, <span style="color: maroon"> *newRedDefault* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'whiteColor'</span>, <span style="color: maroon"> *newWhiteDefault* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'turquoiseColor'</span>, <span style="color: maroon"> *newTurquioseDefault* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'yellowColor'</span>, <span style="color: maroon"> *newYellowDefault* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'pinkColor'</span>, <span style="color: maroon"> *newPinkDefault* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'backgroundColor'</span>, <span style="color: maroon"> *newBackgroundColorDefault* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'cursorColor'</span>, <span style="color: maroon"> *newCursorColorDefault* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'selectColor'</span>, <span style="color: maroon"> *newSelectColorDefault* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'menubarTextColor'</span>, <span style="color: maroon"> *newMenubarTextColorDefault* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'menubarColor'</span>, <span style="color: maroon"> *newMenubarColorDefault* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'menubarBackgroundImage'</span>, <span style="color: maroon"> *newUrl* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'menubarBackgroundRepeat'</span>, <span style="color: maroon"> *newCSSRepeat* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'statusbarTextColor'</span>, <span style="color: maroon"> *newStatusTextColorDefault* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'statusbarColor'</span>, <span style="color: maroon"> *newStatusbarColorDefault* </span>  );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'statusbarBackgroundImage'</span>, <span style="color: maroon"> *newUrl* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'statusbarBackgroundRepeat'</span>, <span style="color: maroon"> *newCSSRepeat* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'backgroundImage'</span>, <span style="color: maroon"> *newImage* </span> );
      localStorage.setItem(keyNamespace + <span style="color: maroon">'backgroundRepeat'</span>, <span style="color: maroon"> *newCSSRepeat* </span> );

 **WingsTerminal.renderDisplay_init();** <span style="color:blue">&lt;/<span style="color:maroon">Script</span>&gt;</span></pre>

#### Special Note:
The references to the directory location of Asna5250Terminal.aspx in the examples above specify **~/Themes/Current/** as the location used. Refer to [Keyboard Mapping](WebConfigAppSettings.htm#terminalfolder">Setting the location of the Asna5250Terminal.aspx page</a> for more information.

#### See Also
<dl>
  <dd><a href="TerminalKeyboardMapping.html)</dd>
  <dd>[Keyboard Macros](TerminalKeyboardmacros.html)</dd>
  <dd>[5250 Terminal Emulator Menus](TerminalMenuBar.html)</dd>
  <dd>[5250 Terminal Emulator Resizing](TerminalSizing.html)</dd>
</dl>

