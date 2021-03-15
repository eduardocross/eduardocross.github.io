---
title: 5250 Terminal Mobility Support

Id: TerminalMobile
TocParent: TerminalEmulation
TocOrder: 60

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
keywords: 
keywords: macros
keywords: function key menu, macros
keywords: function key menu, FKeyPH
keywords: Asna5250Terminal.aspx
keywords: ASNA Browser Terminal, Asna5250Terminal.aspx
keywords: PageScriptPH
keywords: Mobility
keywords: Wings

---

<table>
                <tr>
                    <td>
                        <span class="OH_MultiViewContainerPanelDhtmlTable">
                            ASNA Browser Terminal&#8482; Admin Manual
                        </span>
                    </td>
                </tr>
</table>

# 5250 Terminal Mobility Support

#### TerminalCanvas Control
The Terminal Emulator is treated as a single ASP.NET control in the underlying HTML. This greatly simplifies the process of maintaining separate versions of the emulator for differing platforms. 

#### Using the ASNA 5250 Terminal Emulator on a Tablet
The 5250 Terminal Emulator is activated on a tablet by opening the tablet's browser to the page in question and then logging in. 

#### Features
BTerm's Mobile Support includes a number of features that make interacting with a green screen interface without the traditional IBM keyboard much simpler. 

- **Touch Cursor-positioning**  &#8211;
                        Touching any non-button space on the 5250 display will
                        instantly move the cursor to the selected location.
- **Swipe Scrolling**  &#8211; Swiping (sliding a finger quickly along the screen) up will
                        issue a PgUp command to the emulator, swiping down will issue a PgDn.
- **Automatic Keyboard**  &#8211; By pressing and
                        holding down on any typable area, the user can open up the
                        tablet's internal keyboard and begin typing. The
                        cursor will automatically be moved to the first position on
                        that field as well.
- **Options Pane**  &#8211; By dragging up the small white bar visbile at the
                        bottom of the emulator the user can access a small Options
                        pane.<br />
                        <img align="center" src="Images/BTermOptions.png" />
                        <br />Each item on it can be set to either Yes or No by tapping on the slider to the right of it.
                        It contains the following items:
- **FKey Hotspots**  &#8211; Each Function key command listed in the display file is converted
                        into a button.  Clicking the button sends that Function key command to the IBM i.<br />
                        <img align="center" src="Images/BTermButtons.png" />
- **Enter/Reset Buttons**  &#8211;
                        Creates an Enter button at the lower right of the
                        display. In circumstances where the Reset key would be activated, a Reset button will
                        appear on the lower left as well
- **IBMKeypad**  &#8211; Shows or hides the IBM Keypad, described below.
                        <img align="center" src="Images/IBMKeypad.png" />
- **Colors**  &#8211; Clicking this opens a color-picker panel where users can customize
                        the appearance of the BTerm emulator.
                        <img align="center" src="Images/colorpicker.png" />

**Warning &#8211;** Not all browsers offer full support for BTerm. The default browser for Android 4.0 (Ice cream sandwich) and earlier does not properly support the automatic keyboard. 

#### The IBM Keypad
By tapping on the left or right edge of the screen, or the status bar at the bottom, the user can open the IBM Keypad. 

The IBM keypad has three fixed buttons (on the left) and five configurable buttons to the right. Tapping on a fixed button will bring up a list of keystrokes included under that button (Function keys for F1-12 and F13-F22, and IBM keys for Special). From there a user can either slide their finger to the key they wish to use or tap it directly (the list will stay in place until another keystroke moves it). 

The five buttons to the right can be activated by tapping on the desired button. They can also be swapped out by pressing and holding the button to be swapped out, which will cause a panel containing all keys on an IBM i terminal to appear. 
<img align="center" src="Images/KeyPadList.png" />

Tap on a key, and it will replace whichever key was in that slot before (tap outside the pane or on the blank area just above the Keypad to go back without making changes). 

#### See Also
<dl>
                <dd>[Keyboard Mapping](TerminalKeyboardMapping.html)</dd>
                <dd>[Keyboard Macros](TerminalKeyboardmacros.html)</dd>
                <dd>[Customizing the Terminal Branding](TerminalBranding.html)</dd>
                <dd>[Terminal Error Codes](TerminalErrorCodes.html)</dd>

</dl>

