---
title: 5250 Terminal Keyboard Macros

Id: TerminalKeyboardMacros
TocParent: TerminalEmulation
TocOrder: 30

keywords: ASNA Browser Terminal
keywords: ASNA Browser Terminal, terminal keyboard macros
keywords: ASNA Browser Terminal, 5250 terminal keyboard macros
keywords: 5250 terminal keyboard macros
keywords: macros, FKeyPH
keywords: macros
keywords: FKeyPH
keywords: 5250 terminal menus, macros
keywords: function key menu
keywords: function key menu, macros
keywords: Asna5250Terminal.aspx
keywords: ASNA Browser Terminal, Asna5250Terminal.aspx
keywords: Asna5250Terminal.aspx, FKeyPH
keywords: how to, create macro functions
keywords: Wings

---

<table>
			    <tr>

			       <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Browser Terminal&#8482; Admin Manual
				   </span><br /></td>
			    </tr>
</table>

# 5250 Terminal Keyboard Macros
The ASNA 5250 Terminal Emulator code provides a function that accepts an array of <span style="color: blue">Actions</span> and/or <span style="color: blue">characters</span>, and executes each in the sequence specified by the array positions. 

The function is called:
<dl><dd>
					<span style="color: blue">WingsTerminal.executeMacro(<span style="color: red">macro</span>)</span>;</dd></dl>

where, <span style="color: red">macro</span> is an instance of an array of strings, with elements containing names of <span style="color: blue">Actions</span> or, if the length of the string is one, the string is used as a <span style="color: blue">character</span> to be processed by the emulator as if it were entered directly from the keyboard. There is no need to indicate Shift, Control, or Alt on keystrokes, since the <span style="color: blue">Actions</span> produced by such combinations can be requested directly. (The Wings prefix is derived from ASNA Wings, another member of the [Monarch Family](emASNAfamily.html) that uses a similar terminal emulator.)
<!-- end of introduction -->

The first string in the array is reserved for the name of the macro. 

For example, let's assume that we want a macro to execute the following steps.

1. Move the cursor to the first field and position one (Record Home).
2. Enter 'ADDLIBLE CAROLINA' (Add Library List Entry 
						CAROLINA).
3. Submit page with 'Enter' Aidkey.

Let's add a Button control to the ~/Themes/Current/Asna5250Terminal.aspx markup, using the Function Key area in the default MasterPage. The following Button control may be added before the "CenPH" asp:Content section. 
<pre class="prettyprint"> &#60;asp:Content ID="FileContent1" runat="server" ContentPlaceHolderID="FKeyPH"&#62;
   &#60;button onclick= "return testMacro();"&#62;Add Libl Entry Macro&#60;/button&#62;
&#60;/asp:Content&#62; </pre>

The implementation of the testMacro() JavaScript function is as follows.
<pre class="prettyprint">
testMacro = function () 
{
   var macro = [
      'Test Macro', // The name of the Macro (ignored during execution)
      'RECORD',     // First action, goto Home position
      'A', 'D', 'D', 'L', 'I', 'B', 'L', 'E', ' ',
      'N', 'U', 'T', 'S', 'N', 'B', 'O', 'L', 'T', 'S',
      'ENTER' 
    ];

   WingsTerminal.executeMacro(macro);

   return false;
}</pre>

Notice how the array contains two Actions: <span style="color: maroon">'RECORD'</span> and <span style="color: maroon">'ENTER'</span>, which are both case sensitive. These are two of the actions listed in [Keyboard Mapping](TerminalKeyboardMapping.html). <span style="color: maroon">'RECORD'</span> moves the cursor to the Home position and <span style="color: maroon">'ENTER'</span> submits the page with an QSN_ENTER (0xf1) Aid key. The rest are letters that are typed to fill the input field (ADDLIBLE and NUTSNBOLTS). Once the macro array has been declared, all we need to do is call the WingsTerminal.executeMacro function with the macro as the only parameter. Lastly, returning false to the onclick event prevents it from executing any further actions.

#### Macros are Interrupted after Submitting a Page
The macro is interrupted when it executes any Action that causes the Page to be submitted because of the Stateless behavior of Web applications. In fact, the JavaScript that implements the ASNA 5250 Terminal Emulator, as well as any JavaScript in the page, is released from memory and re-loaded when the request is returned.

There are advanced techniques that can be implemented to split a large macro into segments, divided by submitting Actions and those that are to be continued the next time the page renders again, which could also contain submitting Actions.

These techniques involve storing the macro in a file (or local storage) as well as the state regarding the segments already executed. A hidden field may be added to the page with the segment of the macro to be executed the next time; and the JavaScript can control the subsequent segments to be executed. ~/Themes/Current/Asna5250Terminal.aspx code behind may be altered to accomplish these steps.

#### Special Note:
Any references to the directory location of Asna5250Terminal.aspx in the above specifies **~/Themes/Current/** as the location. Refer to [5250 Terminal Branding](WebConfigAppSettings.htm#terminalfolder">Setting the location of the Asna5250Terminal.aspx page</a> for more information.

#### See Also
<dl>
  <dd><a href="TerminalBranding.html)</dd>
  <dd>[Keyboard Mapping](TerminalKeyboardMapping.html)</dd>

</dl>

