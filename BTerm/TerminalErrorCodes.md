---
title: 5250 Terminal Error Codes

Id: TerminalErrorCodes
TocParent: TerminalEmulation
TocOrder: 12

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

# 5250 Terminal Error Codes

#### 5250 Error Beep
The 5250 Terminal Emulator will (much like a standard Terminal or any particularly good emulator) generate a "beep" sound whenever a user attempts to an invalid input. 

#### 5250 Error Codes and Solutions
The 5250 Emulator uses the same error codes as a standard 5250 terminal, but a listing of the more common ones follows:

<table border="1" style="display: inline; border-collapse: collapse; font-size: 1em; "> <tr> <td> **Error Code** </td> <td> **Description** </td> <td> **Recovery Action** </td> </tr> <tr> <td style="height: 42px"> 0004 </td> <td style="height: 42px"> <p> Entry of data not allowed in this input/output field. 
</td>
							<td style="height: 42px">
								Press Reset or move the cursor to a field where 
								keyboard data can be entered.	                                     
								</td>
						</tr>
						<tr>
							<td style="height: 57px">
								0005	                                     
								</td>
							<td style="height: 57px">
 Cursor in protected area 
								of display. <br/>
								To enter data, the cursor must be in an input 
								field on the display.  Data cannot be entered in 
								a protected area of display.	                                     
								</td>
							<td style="height: 57px">
								Press Error Reset key.  Move the cursor to a 
								field where the data can be entered and then 
								enter the data.	                                     
								</td>
						</tr>
						<tr>
							<td>
								0006	                                     
								</td>
							<td>
 Key pressed following 
								System Request key was not valid. <br/>
								Either the Enter/Receive key, or Error Reset key 
								must be pressed after the Shift key and System 
								Request key.	                                     
								</td>
							<td>
								Press the Error Reset key.  If system request 
								function required, press Shift key, System 
								Request key, and Enter/Receive Advance key.	                                     
								</td>
						</tr>
						<tr>
							<td>
								0007	                                     
								</td>
							<td>
 Mandatory data entry 
								field. Must have data entered. <br/>															
								Data must be entered in mandatory data entry 
									field on the display before the display can 
									be changed or moved. 
								</td>
							<td>
								Press Error Reset key.  Cursor is now at the 
								first character position in the first mandatory 
								enter field that is not filled.

								Enter the required data in this field.	              
								</td>
						</tr>
						<tr>
							<td>
								0008	                                     
								</td>
							<td>
 Field requires alphabetic 
								characters. A character that was not alphabetic was 
								entered.  Valid characters are, A through Z, 
								blank, comma, period, hyphen, and Duplicate key 
								(if the Duplicate key is supported by the 
								executing program).	                                     
								</td>
							<td>
								Press Error Reset key to continue.	                                     
								</td>
						</tr>
						<tr>
							<td>
								0009	                                     
								</td>
							<td>
 Field requires numeric 
								characters. <br/>
								A character that was not numeric was entered.  
								Valid characters are, zero through nine, blank, 
								comma, period, plus, minus, and Duplicate key 
								(if the Duplicate key is supported by the 
								executing program).	                                     
								</td>
							<td>
								Press Error Reset key to continue.	                                     
								</td>
						</tr>
						<tr>
							<td>
								0010	                                     
								</td>
							<td>
 Only characters 0 through 
								9 allowed. <br/>
								Signed numeric data was not entered.  Valid 
								characters are zero through nine and Duplicate 
								key (if the Duplicate key is supported by the 
								executing program).	                                     
								</td>
							<td>
								Press Error Reset key to continue.	                                     
								</td>
						</tr>
						<tr>
							<td>
								0011	                                     
								</td>
							<td>
 Key for sign position of 
								field not valid .								
								<br/>
								Data not allowed in last position of signed 
								numeric field which is sign position.	                                     
								</td>
							<td>
								Press Error Reset key and valid key for sign 
								position (Field+ or Field- key).	                                     
								</td>
						</tr>
						<tr>
							<td>
								0012	                                     
								</td>
							<td>
 No room to insert data. <br/>
								No room in field or cursor in last position of 
								field during the insert mode. 	                                     
								</td>
							<td>
								Press Error Reset key to continue.  Do not use 
								insert mode to change data or enter last 
								character in field.	                                     
								</td>
						</tr>
						<tr>
							<td>
							0013</td>
							<td>

During insert mode, only data keys allowed. <br/>Key that was pressed was not data.
</td>
							<td>
							Press Error Reset key.  For insert mode press Insert 
							key.</td>
						</tr>
						<tr>
							<td>
							0014</td>
							<td>
 Mandatory fill field. Must fill to exit. <br/>Key 
							pressed that moved cursor from field.  The 
							field must be filled unless you exit from first 
							position and no other data entered in field.
							</td>
							<td>
							Press Error Reset key.  Enter data in entire field 
							or press Field-, Field+, or Field Exit key to blank 
							entire field.</td>
						</tr>
						<tr>
							<td>
							0015</td>
							<td>

Check digit error. <br/> The number and check digit did not agree.<br/> 
</td>
							<td>
							Press Error Reset key.  The cursor is at beginning 
							of field.  Enter correct number and check digit or 
							press Field Plus, Field Minus, or Field Exit key to 
							clear field.</td>
						</tr>
						<tr>
							<td>
							0016</td>
							<td>

Field Minus key not valid in field. <br/>Field where data entered not signed numeric field.
</td>
							<td>
							Press the Error Reset key to continue operation at 
							present cursor position.  Continue entering data or 
							press Field Exit key to leave field.</td>
						</tr>
						<tr>
							<td>
							0017</td>
							<td>
 This field must be filled 
							before exiting. Key used not valid. <br/>
							Field-, Field+, or Field Exit key pressed.  This 
							field must be filled unless the field is exited from 
							first position and no data entered.<br/></td>
							<td>
							Press Error Reset key.  Cursor positioned to 
							continue entering data in field.  Enter data to the 
							end of field or position the cursor to beginning of 
							field and press Field-, Field+, or Field Exit key to 
							blank entire field.</td>
						</tr>
						<tr>
							<td>
							0018</td>
							<td>
 The key used to exit field not 
							valid. <br/>Cursor is in the last position of 
							the field.</td>
							<td>
							Press the Error Reset key and the Field Exit key to 
							leave the field.</td>
						</tr>
						<tr>
							<td>
							0019</td>
							<td>
 Duplicate key or Field Mark 
							key not allowed in field.<br/> The DUP or Field 
							Mark key was pressed and is not allowed in this 
							field.<br/></td>
							<td>
							Press Error Reset key to continue entering data in 
							the field.</td>
						</tr>
						<tr>
							<td>
							0020</td>
							<td>
 Enter key not allowed in 
							field.<br/> The field is either right-adjust or 
							a signed numeric field.  Exit before pressing 
							command keys, Test, Clear, Enter/Adv, Print, Help, 
							Roll, or Home keys.<br/></td>
							<td>
							Press Error Reset key and Field-, Field+, or Field 
							Exit key.</td>
						</tr>
						<tr>
							<td>
							0021</td>
							<td>

Mandatory enter field must have data entered. <br/>Mandatory enter field must have data entered before exiting the field.
</td>
							<td>
							Press Error Reset key and continue entering data in 
							field.</td>
						</tr>
						<tr>
							<td>
							0026</td>
							<td>

0-9 required for last position of numeric-only field.<br/> 
</td>
							<td>
							Press Error Reset key to continue.</td>
						</tr>
</table>
				</p>

#### See Also
<dl>
  <dd>[Keyboard Mapping](TerminalKeyboardMapping.html)</dd>
  <dd>[Keyboard Macros](TerminalKeyboardmacros.html)</dd>
  <dd>[Customizing Terminal Branding](TerminalBranding.html)</dd>
  <dd>[Resizing the Terminal](TerminalSizing.html)</dd>

</dl>

