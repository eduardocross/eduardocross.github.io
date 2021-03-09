---
title: 5250 Terminal Keyboard Mapping

Id: TerminalKeyboardMapping
TocParent: TerminalEmulation
TocOrder: 20

keywords: ASNA Browser Terminal
keywords: ASNA Browser Terminal, terminal keyboard mapping
keywords: ASNA Browser Terminal, 5250 terminal keyboard mapping
keywords: 5250 terminal keyboard mapping
keywords: ASNA Browser Terminal, 5250 terminal keyboard
keywords: 5250 terminal keyboard
keywords: 5250 terminal keyboard, customizing
keywords: function keys, customizing
keywords: macros
keywords: keyboard, key macros
keywords: keyboard, hotkeys
keywords: Asna5250Terminal.aspx
keywords: ASNA Browser Terminal, Asna5250Terminal.aspx
keywords: Asna5250Terminal.aspx, customizing keyboard
keywords: ASNA Browser Terminal, telnet flags
keywords: telnet flags
keywords: telnet flags, attention key
keywords: telnet flags, system request key
keywords: telnet flags, test request key
keywords: telnet flags, help in error state
keywords: how to, set telnet flags
keywords: how to, set international keys
keywords: international keys
keywords: Aid key, ATTN
keywords: Aid key, BEGIN
keywords: Aid key, CLEAR
keywords: Aid key, COPY
keywords: Aid key, CURSOR
keywords: Aid key, CUT
keywords: Aid key, DELETE
keywords: Aid key, DOWN
keywords: Aid key, DUP
keywords: Aid key, END
keywords: Aid key, ENTER
keywords: Aid key, ERASE
keywords: Aid key, F1...F24
keywords: Aid key, FASTDOWN
keywords: Aid key, FASTLEFT
keywords: Aid key, FASTRIGHT
keywords: Aid key, FASTUP
keywords: Aid key, FIELDMINUS
keywords: Aid key, FIELDEXIT
keywords: Aid key, FIELDEXITENTER
keywords: Aid key, HELP
keywords: Aid key, HEX
keywords: Aid key, INSERT
keywords: Aid key, LAST
keywords: Aid key, LEFT
keywords: Aid key, LEFTDELETE
keywords: Aid key, NEWLINE
keywords: Aid key, NEXT
keywords: Aid key, PASTE
keywords: Aid key, PGDN
keywords: Aid key, PGUP
keywords: Aid key, PREVIOUS
keywords: Aid key, PRINT
keywords: Aid key, RECORD
keywords: Aid key, RESET
keywords: Aid key, REDIRECTPage
keywords: Aid key, RIGHT
keywords: Aid key, SYSREQ
keywords: Aid key, UP

---

<table>
                <tr>

                    <td>
                        <span class="OH_MultiViewContainerPanelDhtmlTable">
                            ASNA Browser Terminal&#8482; Admin Manual
                        </span><br />
                    </td>
                </tr>
</table>

# 5250 Terminal Keyboard Mapping
<a name="top"></a>This topic contains multiple sections. 
<dl>
                        <dt>[
                                Menu
                                bar
                            ](#top">Default Keyboard Setting</a> </dt>
                        <dt><a href="#custom">Customizing the Keyboard</a></dt>
                        <dd><a href="#hotkeys">Adding Hot-keys for International Characters</a></dd>
                        <dt>
                            <br /> Note that some of these keyboard actions are accessible through the <a href="TerminalMenuBar.html).
                        </dt>
</dl>

<!-- end of introduction -->

#### Default Keyboard Settings
The following keyboard 'actions' are identified and mapped to either an IBM Aid key that gets submitted or a terminal command to edit field content or to move the cursor position.
<table class="mytable" cellspacing="0" cellpadding="4" width="100%">
                    <colgroup>
                        <col width="10%" style="vertical-align: middle" />
                        <col width="30%" style="vertical-align: middle" />
                        <col width="10%" style="vertical-align: middle" />
                        <col width="50%" style="vertical-align: middle" />
                    </colgroup>
                    <tr>
                        <th style="height: 23px">Action</th>
                        <th style="height: 23px">Description</th>
                        <th style="height: 23px">Default<br /> Mapping</th>
                        <th style="height: 23px">Comment</th>
                    </tr>

                    <tbody>
                        <tr>
                            <td class="action">'ATTN'</td>
                            <td>
                                Alerts the host system that a requested function is not being
                                honored.
                            </td>
                            <td class="keyMap">Ctrl + F5</td>
                            <td>
                                Sets Bit 1 on Telnet flags header field and submits the page to the IBM i.
                                See the Telnet flags below. <br />Also accessible on the [menu bar](terminalmenubar.html).
                            </td>
                        </tr>

                        <tr>
                            <td class="action">'BEGIN'</td>
                            <td>Place cursor at the start of field.</td>
                            <td class="keyMap">Ctrl + F9</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'CLEAR'</td>
                            <td>Submit QSN_CLEAR (0xbd) to IBM i.</td>
                            <td class="keyMap">Scroll Lock</td>
                            <td>Also accessible on the [menu bar](terminalmenubar.html).</td>
                        </tr>

                        <tr>
                            <td class="action">'COPY'</td>
                            <td>Copy selected text to the Windows clipboard.</td>
                            <td class="keyMap">Ctrl + C<br />IE Menu 'Copy'</td>
                            <td>Context menus do not work. IE Browser Edit menu is supported.</td>
                        </tr>

                        <tr>
                            <td class="action">&#39;CURSOR&#39;</td>
                            <td>Toggle between normal cursor and cross-hair cursor.</td>
                            <td class="keyMap">(None)</td>
                            <td class="keyCd">Cross-hair cursor not implemented.</td>
                        </tr>

                        <tr>
                            <td class="action">'CUT'</td>
                            <td>Cut selected text (inside input capable field).</td>
                            <td class="keyMap">Ctrl + X<br />IE Menu 'Cut'</td>
                            <td>Context menus do not work. IE Browser Edit menu is supported.</td>
                        </tr>

                        <tr>
                            <td class="action">'DELETE'</td>
                            <td>Delete character at cursor position.</td>
                            <td class="keyMap">Delete<br />Del</td>
                            <td>JavaScript does not distinguish between &#39;Delete&#39; and &#39;Del&#39;.</td>
                        </tr>

                        <tr>
                            <td class="action">'DOWN'</td>
                            <td>Move cursor one position down.</td>
                            <td class="keyMap">any Down Arrow</td>
                            <td>
                                JavaScript does not distinguish between the different &#39;Down Arrow&#39; keys on the
                                keyboard.
                            </td>
                        </tr>

                        <tr>
                            <td class="action">&#39;DUP&#39;</td>
                            <td>
                                If field has DUP attribute, the field is filled with the DUP
                                characters from the cursor postion.
                            </td>
                            <td class="keyMap">Ctrl + F6</td>
                            <td class="keyCd" />
                        </tr>

                        <tr>
                            <td class="action">'END'</td>
                            <td>
                                Place cursor at the end of a field.<br />(Note: this is different
                                from LAST, which positions the cursor at the **last character
                                    entered**  into the field).
                            </td>
                            <td class="keyMap">Ctrl + F11</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'ENTER'</td>
                            <td>Submit QSN_ENTER (0xf1) to IBMi.</td>
                            <td class="keyMap">any Enter</td>
                            <td>
                                JavaScript does not distinguish between the different 'Enter' keys on the
                                keyboard.
                            </td>
                        </tr>

                        <tr>
                            <td class="action">&#39;ERASE&#39;</td>
                            <td>Clears all input fields and sets them to their default value.</td>
                            <td class="keyMap">(None)</td>
                            <td>Not mapped to a key. On the [Menu bar](TerminalMenuBar.html).</td>
                        </tr>

                        <tr>
                            <td class="action">'F1' ... 'F24'</td>
                            <td>Submit QSN_F1 (0x31)... QSN_F24 (0xbc) to IBMi.</td>
                            <td class="keyMap">F1 ... F12<br />Shift + F1 ... Shift + F12</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'FASTDOWN'</td>
                            <td>Move cursor three positions down.</td>
                            <td class="keyMap">Ctrl + Down Arrow</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'FASTLEFT'</td>
                            <td>Move cursor three positions left.</td>
                            <td class="keyMap">Ctrl + Left Arrow</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'FASTRIGHT'</td>
                            <td>Move cursor three positions right.</td>
                            <td class="keyMap">Ctrl + Right Arrow</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'FASTUP'</td>
                            <td>Move cursor three positions up.</td>
                            <td class="keyMap">Ctrl + Up Arrow</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'FIELDMINUS'</td>
                            <td>
                                Erase the rest of the field and move the cursor to the next field.<br />
                                For numeric fields, change the sign to negative.
                            </td>
                            <td class="keyMap">Shift + - (numeric keypad)</td>
                            <td>Not mapped to a key.</td>
                        </tr>

                        <tr>
                            <td class="action">'FIELDPLUS'</td>
                            <td>
                                Erase the rest of the field and move the cursor to the next field.<br />
                                For numeric fields, change the sign to positive.
                            </td>
                            <td class="keyMap">Shift + + (numeric keypad)</td>
                            <td>Not mapped to a key.</td>
                        </tr>

                        <tr>
                            <td class="action">'FIELDEXIT'</td>
                            <td>Erase the rest of the field and move the cursor to the next field.</td>
                            <td class="keyMap">Shift + Enter</td>
                            <td>Not mapped to a key.</td>
                        </tr>

                        <tr>
                            <td class="action">&#39;FIELDEXITENTER&#39;</td>
                            <td>Justify the field and send the ENTER command to the IBM i.</td>
                            <td class="keyMap">Ctrl + Enter</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'HELP'</td>
                            <td>
                                Help in error state. When input validation fails, error codes are set
                                and a help on error request is sent to the IBM i.
                            </td>
                            <td class="keyMap">(None)</td>
                            <td>
                                Not mapped to a key.<br />
                                Sets Bit 7 on Telnet flags header field. Sets error code in 5250 data stream and
                                submits the page to the IBM i.<br />Also accessible on the [menu bar](terminalmenubar.html).
                            </td>
                        </tr>

                        <tr>
                            <td class="action">&#39;HEX&#39;</td>
                            <td>
                                Shows a dialog where Hex can be typed to enter a character not on
                                the keyboard. If only one character is entered, the character will be
                                taken verbatim.
                            </td>
                            <td class="keyMap">(None)</td>
                            <td>Not mapped to a key. <br />Accessible on the [menu bar](terminalmenubar.html).</td>
                        </tr>

                        <tr>
                            <td class="action">'INSERT'</td>
                            <td>Toggle insert mode.</td>
                            <td class="keyMap">Insert<br />Ins</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'LAST'</td>
                            <td>Jump to the last character of a field.</td>
                            <td class="keyMap">any End</td>
                            <td>
                                JavaScript does not distinguish between the different &#39;End&#39; keys on the
                                keyboard.
                            </td>
                        </tr>

                        <tr>
                            <td class="action">'LEFT'</td>
                            <td>Move cursor one position left.</td>
                            <td class="keyMap">any Left Arrow</td>
                            <td>
                                JavaScript does not distinguish between the different &#39;Left Arrow&#39; keys on the
                                keyboard.
                            </td>
                        </tr>

                        <tr>
                            <td class="action">'LEFTDELETE'</td>
                            <td>Delete character left of the cursor.</td>
                            <td class="keyMap">Backspace</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'NEWLINE'</td>
                            <td>Jump to next line</td>
                            <td class="keyMap">Shift + Enter</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'NEXT'</td>
                            <td>Jump to the next field.</td>
                            <td class="keyMap">Tab</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'PASTE'</td>
                            <td>Copy the contents of the Clipboard to the current cursor's position.</td>
                            <td class="keyMap">Ctrl + V (IE &#39;Paste&#39; menu)</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'PGDN'</td>
                            <td>Roll UP the screen</td>
                            <td class="keyMap">Page Down</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'PGUP'</td>
                            <td>Roll DOWN the screen</td>
                            <td class="keyMap">Page Up</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'PREVIOUS'</td>
                            <td>Jump to the previous field.</td>
                            <td class="keyMap">Shift + Tab</td>
                            <td></td>
                        </tr>

                        <tr>
                            <td class="action">'PRINT'</td>
                            <td>Submit QSN_PRINT (0xf6) to the IBMi.</td>
                            <td class="keyMap">(None)</td>
                            <td>Not mapped to a key.</td>
                        </tr>

                        <tr>
                            <td class="action">'RECORD'</td>
                            <td>Record Backspace (Home). Put cursor at the Home position (first input field, position 1).</td>
                            <td class="keyMap">any Home</td>
                            <td>
                                JavaScript does not distinguish between the different &#39;Home&#39; keys on the
                                keyboard.
                            </td>
                        </tr>

                        <tr>
                            <td class="action">'RESET'</td>
                            <td>Opens the keyboard for input (if keyboard is LOCKED due to error).</td>
                            <td class="keyMap">Esc</td>
                            <td>May be re-mapped to Ctrl + R. See [5250 Terminal Branding](custom">Customizing the Keyboard</a>.</td>
                        </tr>

                        <tr>
                            <td class="action">'REDIRECT: *Page* '</td>
                            <td>Navigate to new *Page* </td>
                            <td class="keyMap">(None)</td>
                            <td>
                                Page is relative to the location of the Asna5250Terminal.aspx. It could
                                specify a folder but make sure to provide a way to get back to the
                                Asna5250Terminal.aspx page.
                            </td>
                        </tr>

                        <tr>
                            <td class="action">'RIGHT'</td>
                            <td>Move cursor one position right.</td>
                            <td class="keyMap">any Right Arrow</td>
                            <td>
                                JavaScript does not distinguish between the different &#39;Right Arrow&#39; keys on the
                                keyboard.
                            </td>
                        </tr>

                        <tr>
                            <td class="action" style="height: 46px">&#39;SYSREQ&#39;</td>
                            <td style="height: 46px">System request interrupt.</td>
                            <td class="keyMap" style="height: 46px">
                                Shift + Esc<br />
                                Ctrl + F4
                            </td>
                            <td style="height: 46px">Not implemented.</td>
                        </tr>

                        <tr>
                            <td class="action">'UP'</td>
                            <td>Move cursor one position Up.</td>
                            <td class="keyMap">any Up Arrow</td>
                            <td>
                                JavaScript does not distinguish between the different &#39;Up Arrow&#39; keys on the
                                keyboard.
                            </td>
                        </tr>
                    </tbody>
</table>

**Telnet Flags** 

A few of the 'Actions' that submit but do not send Aid Key to the IBM i need to effect the Telnet message header instead. According to http://www.ietf.org/rfc/rfc1205.txt, there is a 16 bit flag field in the Telnet header. Eight of those bits are reserved and should be set to zero. 
<table class="mytable" cellspacing="0" cellpadding="4" width="60%">
                    <colgroup>
                        <col width="10%" style="vertical-align: middle" />
                        <col width="10%" style="vertical-align: middle" />
                        <col width="80%" style="vertical-align: middle" />
                    </colgroup>
                    <tr>
                        <th style="height: 23px">Bit</th>
                        <th style="height: 23px" colspan="2">Description</th>
                    </tr>

                    <tbody>
                        <tr>
                            <td>0 </td>
                            <td>ERR</td>
                            <td>This bit is set to indicate a data stream output **error** . The negative response code is sent as data following the op code field.</td>
                        </tr>
                        <tr>
                            <td>1</td>
                            <td>ATN</td>
                            <td>This bit is set to indicate that the 5250 **attention key**  was pressed.</td>
                        </tr>
                        <tr>
                            <td>2, 3, 4 </td>
                            <td>*</td>
                            <td>These bits are reserved (set to zero).</td>
                        </tr>
                        <tr>
                            <td>5</td>
                            <td>SRQ</td>
                            <td>This bit is set to indicate that the 5250 **System Request key**  was pressed.</td>
                        </tr>
                        <tr>
                            <td>6</td>
                            <td>TRQ</td>
                            <td>This bit is set to indicate that the 5250 **Test Request key**  was pressed.</td>
                        </tr>
                        <tr>
                            <td>7</td>
                            <td>HLP</td>
                            <td>This bit is set to indicate the **Help in Error State**  function. The error code is sent as data following the header and is a four digit packed decimal number. For example, an error code of '0005'X indicates the operator attempted to type in an area of the display that is not enabled for input.</td>
                        </tr>
                        <tr>
                            <td>8 thru 15</td>
                            <td>*</td>
                            <td>These bits are reserved (set to zero).</td>
                        </tr>
                    </tbody>
</table>

<a href="#top">Return to the top</a>

#### Special Note:
The references to the directory location of Asna5250Terminal.aspx in the above information specifies **~/Themes/Current/** as the location used. Refer to <a href="WebConfigAppSettings.htm#terminalfolder">Setting the location of the Asna5250Terminal.aspx page</a> for more information. 

#### See Also
<dl>
                    <dd><a href="TerminalBranding.html)</dd>

</dl>

