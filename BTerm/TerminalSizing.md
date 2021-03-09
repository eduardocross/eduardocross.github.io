---
title: 5250 Terminal Sizing

Id: TerminalSizing
TocParent: TerminalEmulation
TocOrder: 50

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
keywords: Wings

---

<table>
			    <tr>

			       <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Browser Terminal&#8482; Admin Manual
				   </span><br /></td>
			    </tr>
</table>

# 5250 Terminal Resizing

#### Changing the Terminal Display Size
The initial size of the BTerm window is controlled by the entry-point Javascript function (WingsTerminal.render) called right after the Monarch/Asna5250Terminal.aspx\ page gets loaded. (The Wings prefix is derived from ASNA Wings, another member of the [Monarch Family](emASNAfamily.html) that uses a similar terminal emulator.)

The script that controls it is:
<pre class="prettyprint">&#60;script type="text/javascript"&#62;
   WingsTerminal.render({"width": 960,"height": 720});
&#60;/script&#62;
</pre>

The WingsTerminal.render function takes one parameter, which can be either:

1. An object with two properties: width and height (see fixed 
					size below). These properties have numeric 
					values (in pixels) representing the size of the &lt;div&gt; where the 
					5250 screen will be presented. Given the size in pixels, an 
					appropriate font height will be selected to show exactly the 
					number of rows contained in the 5250 screen (24 or 27, 
					depending on the Terminal's screen size).<br />Or,
2. A function that will be called by the Emulator's rendering 
					engine whenever the current size is required to paint the 
					page.

#### Setting a Fixed Size
Setting the Terminal Emulation window to a static size is fairly simple: If the WingsTerminal.Render function is passed an unnamed object, by listing the height and width properties using the JavaScript syntax, the render will dynamically create an object, like in the following example:<br /> 
<pre class="prettyprint">WingsTerminal.render({"width": 960, "height": 720});</pre>

To figure out the pixel dimensions of the &lt;div&gt; where you want the Terminal to be rendered, you can either use the Internet Explorer's Developer tools "ruler" feature and measure the width and height visually, or use JavaScript code to compute the dimensions. If you are using jQuery (available for free), you may use the width() method to get the width of the &lt;div&gt;, and use a width-to-height ratio factor to compute the height. For example, assuming that the&lt;div&gt; in your Master Page where the Terminal wll be rendered is named "content", the following parameter may be passed: 
<pre class="prettyprint">WingsTerminal.Render( { "width": $("#content").width(), "height": $("#content").width() * 0.75 } ); // 4:3 ratio</pre>

#### Setting an Adjustable Size
To configure the display size to change with the size of the Browser's Window size, you can pass a function to the Render function, so that it is called each time the size of the Browser's Window changes.

For example, assuming that you are using jQuery library, you may want to compute a new size such that the Terminal DIV grows or shrinks as the Browser Window resizes. This confuguration will change the font height to adjust according to the available real-state that the Browser provides as it changes size. A full-screen Browser Window will give you a very nice font size making it easy to read text.

Assume that you want to preserve a 4:3 ratio, giving you the propertions of the IBM Terminal.

Lastly, assume that the name of the &lt;div&gt; container is "content".

The technique used consists of computing the design-time width proportions in relation to the Browser's Window width measurement, and as the size changes, maintain those proportions, given the illusion that the user is actually changing the size of the Terminal, to change the text font height. As for the DIV's height, the proportion maintained from the start is 75% of its width (or 4:3 ratio).
First, compute the current width of the Browser's window:
<pre>var browserWidth = $(window).width();
</pre>

Next, set the proportion of the design-time width of the terminal in relation to the current Browser's width: 
<pre>window.resizeWidthPercent = ( $("#content").width() * 100.0 ) / browserWidth;</pre>

**Note &#8211;** resizeWidthPercent is defined as a property of the window object, to make it explicit that we want to preserve that value as a 'global' variable (we'll use that value every time the Browser is resized, later).

The computed width and height will always be: 
<pre>var newWidth  = (window.resizeWidthPercent * browserWidth) / 100.0;
var newHeight = newWidth  * 0.75; // 4:3 ratio.
</pre>

To put it all together:
<pre class="prettyprint">WingsTerminal.Render( function () {
            var browserWidth = $(window).width();

            if (typeof (window.resizeWidthPercent) === 'undefined') { // First time (design-time proportion)
                window.resizeWidthPercent = ($("#content").width() * 100.0) / browserWidth;
            }

            var newWidth = (window.resizeWidthPercent * browserWidth) / 100.0;

            $("#content").width(newWidth); // Adjust width of container(s) - avoid clipping

            return { "width": newWidth, "height": newWidth * 0.75 };
        });</pre>

These settings can be further tweaked to improve user experience. for example by setting a minimum size for the Terminal window, to prevent using font sizes that are too small to read. You can do so by adding code similar to:
<pre>        if ( newWidth &lt; 200 ) {
           newWidth = 200;
        }</pre>

immediately before adjusting the width of the object. The complete call would look like:
<pre>       WingsTerminal.Render(function () {
            var browserWidth = $(window).width();

            if (typeof (window.resizeWidthPercent) === 'undefined') { // First time (design-time proprtion)
                window.resizeWidthPercent = ($("#content").width() * 100.0) / browserWidth;
            }
            var newWidth = (window.resizeWidthPercent * browserWidth) / 100.0;

            if (newWidth &lt; 200) {
                newWidth = 200;
            }
            $("#content").width(newWidth); // Adjust width of container(s) - avoid clipping
            return { "width": newWidth, "height": newWidth * 0.75 };
        });
</pre>

**Note &#8211;** The older WingsTerminal.renderDisplay_init function is deprecated.

#### See Also
<dl>
  <dd>[Keyboard Mapping](TerminalKeyboardMapping.html)</dd>
  <dd>[Keyboard Macros](TerminalKeyboardmacros.html)</dd>  
  <dd>[Customizing the Terminal Branding](TerminalBranding.html)</dd>
  <dd>[Terminal Error Codes](TerminalErrorCodes.html)</dd>

</dl>

