---
title: Supported Display File DDS Keywords

Id: SupportedDspDDS
TocParent: ExportingDspFile
TocOrder: 30

keywords: ASNA Browser Terminal
keywords: ASNA Browser Terminal display files
keywords: ASNA Browser Terminal display files DDS keywords
keywords: ASNA Browser Terminal display files field level DDS keywords
keywords: ASNA Browser Terminal display files record level DDS keywords
keywords: ASNA Browser Terminal display files subfile keywords
keywords: ASNA Browser Terminal display attributes for DSPATR keyword
keywords: Emu

---

<table>
			    <tr>
			      <td> <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Browser Terminal&#8482; Admin Manual
				   </span></td>
			    </tr>
</table>

# Supported Display File DDS Keywords
The following tables specify the level of support provided by ASNA Browser Terminal for Display File DDS keywords. Links from keywords lead to the Monarch Framework classes and properties that handle them.

## Display Field-Level Keywords
<table  class="members" >
                    <colgroup>
                    <col width="30%" /> 
                    <col width="30%" />
                    <col width="30%" />
                    </colgroup>
                        <tr><th>Supported</th><th>Supported</th><th>Supported in future release</th><th>Not applicable</th></tr>
                        <tr><td style="height: 23px">AID</td>
							<td style="height: 23px">[ERRMSGID](..\..\MonarchFX\_HTML\amfDdsFieldClassErrorMessageIDProperty.html)</td>
							<td style="height: 23px">CHGINPDFT</td>
							<td style="height: 23px">BLKFOLD</td></tr>
                        <tr><td>ALIAS</td><td>LOWER</td>
							<td>DLTCHK</td>
							<td>CMP</td></tr>
						<tr><td style="height: 25px">AUTO<sup>1</sup></td>
							<td style="height: 25px">MSGCON</td>
							<td style="height: 25px">CHKMSGID</td>
							<td style="height: 25px">CHRID</td></tr>	
						<tr><td style="height: 25px">[SFLSIZ](..\..\MonarchFX\_HTML\amfDdsSubfileControlClassSizeProperty.html)</td>
							<td style="height: 25px">MSGID</td>
							<td style="height: 25px"> DLTCHK</td>
							<td style="height: 25px"> DUP</td></tr>
                        <tr><td style="height: 23px">BLANKS</td>
							<td style="height: 23px">OVERLAY<sup>4</sup></td>
							<td style="height: 23px">DFTVAL</td>
							<td style="height: 23px">EDTMSK</td></tr>
                        <tr><td style="height: 25px">CHECK <sup>2</sup></td>
							<td style="height: 25px">RANGE</td>
							<td style="height: 25px">FLDCSRPRG</td>
							<td style="height: 25px">ENTFLDATR</td></tr>
                        <tr><td style="height: 23px">CNTFLD</td>
							<td style="height: 23px">REFFLD</td>
							<td style="height: 23px">FLTFIXDEC</td>
							<td style="height: 23px">NOCCSID</td></tr>
                        <tr><td style="height: 23px">COLOR</td>
							<td style="height: 23px">SYSNAME</td>
							<td style="height: 23px">FLTPCN</td>
							<td style="height: 23px">OVRATR</td></tr>
                        <tr><td style="height: 23px">COMP</td>
							<td style="height: 23px">TEXT</td>
							<td style="height: 23px">HTML</td>
							<td style="height: 23px">OVRDTA</td></tr>
                        <tr><td style="height: 23px">DATE</td>
							<td style="height: 23px">TIME</td>
							<td style="height: 23px">INDTXT</td>
							<td style="height: 23px">PUTRETAIN</td></tr>
                        <tr><td style="height: 24px">DATFMT</td>
							<td style="height: 24px">TIMFMT</td>
							<td style="height: 24px">MAPVAL</td>
							<td style="height: 24px">WRDWRAP</td></tr>
                        <tr><td>DATSEP</td><td>TIMSEP</td>
							<td>VALNUM</td>
							<td></td></tr>
                        <tr><td style="height: 20px">DFT</td>
							<td style="height: 20px">USER</td>
							<td style="height: 20px"></td>
							<td style="height: 20px"></td></tr>
                        <tr><td style="height: 24px">DLTEDT</td>
							<td style="height: 24px">VALUES</td>
							<td style="height: 24px"></td>
							<td style="height: 24px"></td></tr>
                        <tr><td>DSPATR <sup>3</sup></td><td></td>
							<td></td>
							<td></td><td></td></tr>
                        <tr><td>EDTCDE</td><td></td><td></td><td></td></tr>
                        <tr><td style="height: 22px">EDTWRD</td>
							<td style="height: 22px"></td>
							<td style="height: 22px"></td>
							<td style="height: 22px"></td></tr>
                        <tr><td>[ERRMSG](..\..\MonarchFX\_HTML\amfDdsFieldClassErrorMessageProperty.html)</td><td></td><td></td><td></td></tr>
</table>
<div>

<sup>1 </sup>The only supported function is RA.

<sup>2 </sup>The only supported functions are AB, LC, and ER.

<sup>3 </sup>See table of display attributes supported later in this section.

<sup>4 </sup>Wings has a special procedure for handling the OVERLAY keyword.

## Display Record-Level Keywords
<table  class="members" >
                    <colgroup >
                    <col width="20%" /> 
                    <col width="20%" /> 
                    <col width="20%" />
                    <col width="20%" />
                    </colgroup>
                        <tr><th>Supported </th><th>Supported in future release</th><th>Not applicable</th><th>Not applicable</th></tr>
                        <tr><td>ALTNAME</td><td>CHGINPDFT</td><td>ALARM</td><td>KEEP</td></tr>
                        <tr><td>[CAnn](..\..\MonarchFX\_HTML\amfDdsRecordClassAttnKeysProperty.html)</td><td>CLEAR</td><td>ALWGPH</td><td>LOCK</td></tr>
                        <tr><td>[CFnn](..\..\MonarchFX\_HTML\amfDdsRecordClassFuncKeysProperty.html)</td><td>CLRL</td><td>ALWROL</td><td>MDTOFF</td></tr>
                        <tr><td>CHANGE</td><td>HELP</td><td>ASSUME</td><td>MSGALARM</td></tr>
                        <tr><td>CHECK</td><td>INZRCD</td><td>BLINK</td><td>OVRATR</td></tr>
                        <tr><td style="height: 23px">CSRLOC</td>
							<td style="height: 23px">INDTXT</td>
							<td style="height: 23px">CCSID</td>
							<td style="height: 23px">OVRDTA</td></tr>
                        <tr><td>ERASE</td><td>LOGINP</td><td>CSRINPUT</td><td>PUTOVR</td></tr>
                        <tr><td>OVERLAY<sup>5</sup></td><td>LOGOUT</td><td>CSRINPONLY</td><td>PUTRETAIN</td></tr>
                        <tr><td>PAGEDOWN</td><td>PROTECT</td><td>DSPMOD</td><td>RETCMDKEY</td></tr>
                        <tr><td>PAGEUP</td><td>VALNUM</td><td>ENTFLDATR</td><td>RETKEY</td></tr>
                        <tr><td>PRINT</td><td> </td><td>ERASEINP</td><td>RETLCKSTS</td></tr>
                        <tr><td>RTNCSRLOC <sup>6</sup></td><td> </td><td>FRCDTA</td><td>RMVWDW</td></tr>
                        <tr><td>RTNDTA</td><td></td><td>GETRETAIN</td><td>UNLOCK</td></tr>
                        <tr><td>ROLLDOWN</td><td></td><td>HOME</td><td>USRDFN</td></tr>
                        <tr><td>ROLLUP</td><td></td><td>INVITE</td><td>WDWBORDER</td></tr>
                        <tr><td>SETOF(F)</td><td></td><td>INZINP</td><td>WRDWRAP</td></tr>
                        <tr><td>SLNO <sup>7</sup></td><td></td><td></td><td></td></tr>
                        <tr><td>TEXT</td><td></td><td></td><td></td></tr>
                        <tr><td>VLDCMDKEY</td><td> </td><td></td><td></td></tr>
                        <tr><td>[WDWTITLE](..\..\MonarchFX\_HTML\amfDdsRecordClassWindowTitleProperty.html)</td><td> </td><td> </td><td></td></tr>
                        <tr><td>[WINDOW](..\..\MonarchFX\_HTML\amfDdsRecordClassWindowProperty.html)</td><td> </td><td></td><td></td></tr>
</table>
<div>

<sup>5 </sup>Wings has a special procedure for handling the OVERLAY keyword.

<sup>6 </sup>Support is not provided for cursor positioning within a field.

<sup>7 </sup>Support is not provided for (*VAR)

## Display File-Level Keywords
<table  class="members" ><col width="30%" /> <col width="30%" /><col width="30%" />
                        <tr><th style="width: 233px">Supported</th><th>Supported in future release</th><th>Not applicable</th></tr>
                        <tr><td style="width: 233px; height: 23px">CAnn</td>
							<td style="height: 23px">ALTHELP</td>
							<td style="height: 23px">ALTPAGEDWN</td></tr>
                        <tr><td style="width: 233px">CFnn</td><td>CHGINPDFT</td><td>ALTPAGEUP</td></tr>
                        <tr><td style="width: 233px">CHECK</td><td>CLEAR</td><td>ALWGPH</td></tr>
                        <tr><td style="width: 233px; height: 23px;">[ERRSFL](..\..\MonarchFX\_HTML\amfDdsFileClassErrorSubfileProperty.html)</td>
							<td style="height: 23px">DSPRL</td>
							<td style="height: 23px">CSRINPONLY</td></tr>
                        <tr><td style="width: 233px">INDARA</td><td>HELP</td><td>DSPSIZ</td></tr>
                        <tr><td style="height: 23px; width: 233px">PAGEDOWN</td>
							<td style="height: 23px">INDTXT</td>
							<td style="height: 23px">ENTFLDATR</td></tr>
                        <tr><td style="width: 233px">PAGEUP</td><td>MSGLOC</td><td>HOME</td></tr>
                        <tr><td style="height: 23px; width: 233px;">PRINT</td>
							<td style="height: 23px">VALNUM</td>
							<td style="height: 23px">INVITE</td></tr>
                        <tr><td style="width: 233px">REF</td><td> </td><td>MSGALARM</td></tr>
                        <tr><td style="width: 233px; height: 23px;">ROLLDOWN</td>
							<td style="height: 23px"></td>
							<td style="height: 23px">OPENPRT</td></tr>
                        <tr><td style="width: 233px">ROLLUP</td><td></td><td>PASSRCD</td></tr>
                        <tr><td style="height: 23px; width: 233px">VLDCMDKEY</td>
							<td style="height: 23px"></td>
							<td style="height: 23px">PRINT(Lib)/File)</td></tr>
                        <tr><td style="width: 233px; height: 23px;">WDWBORDER</td>
							<td style="height: 23px"></td>
							<td style="height: 23px">USRDSPMGT</td></tr>
                        <tr><td style="width: 233px"></td><td> </td><td>WRDWRAP</td></tr>
</table>

## Subfile Keywords
<table class="members" >
					<colgroup>
						<col width="30%" />
						<col width="30%" /> 
						<col width="30%" />
					</colgroup>
				<tr><th>Supported</th><th>Supported in future release</th><th>Not applicable</th></tr>
				<tr><td style="height: 23px">SFL</td><td style="height: 23px">SFLRNA</td>
					<td style="height: 23px">SFLCSRPRG</td></tr>
				<tr><td>[SFLCLR](..\..\MonarchFX\_HTML\amfDdsSubfileControlClassClearProperty.html)</td>
					<td></td><td>SFLDLT</td></tr>
				<tr><td>[SFLCTL](..\..\MonarchFX\_HTML\amfddsSubfileControlClass.html)</td><td></td><td>SFLENTER </td></tr>
				<tr><td>SFLCSRRRN</td>
					<td></td><td>SFLROLVAL</td></tr>
				<tr><td>[SFLDROP](..\..\MonarchFX\_HTML\amfDdsSubfileControlClassSflDropProperty.html)</td><td></td><td>SFLSCROLL</td></tr>
				<tr><td>SFLDSP</td><td></td><td></td></tr>
				<tr><td>SFLDSPCTL</td>
					<td></td><td></td></tr>
				<tr><td>[SFLEND](..\..\MonarchFX\_HTML\amfDdsSubfileControlClassSflEndProperty.html) </td><td></td><td></td></tr>
				<tr><td>[SFLFOLD](..\..\MonarchFX\_HTML\amfDdsSubfileControlClassSflFoldProperty.html) </td>
					<td></td><td></td></tr>
				<tr><td>[SFLINZ](..\..\MonarchFX\_HTML\amfDdsSubfileControlClassInitializeRecordsProperty.html)</td>
					<td></td><td></td></tr>
				<tr><td>SFLLIN</td>
					<td></td><td></td></tr>
				<tr><td>[SFLMODE ](..\..\MonarchFX\_HTML\amfDdsSubfileControlClassModeProperty.html)</td><td> </td><td></td></tr>
				<tr><td>[SFLMSG](..\..\MonarchFX\_HTML\amfDdsSubfileControlClassMessageProperty.html)</td>
					<td> </td><td></td></tr>
				<tr><td>[SFLMSGID](..\..\MonarchFX\_HTML\amfDdsSubfileControlClassMessageIDProperty.html)</td>
					<td> </td><td> </td></tr>
				<tr><td>SFLMSGKEY</td><td> </td><td> </td></tr>
				<tr><td>SFLRCDNBR</td><td> </td><td> </td></tr>
				<tr><td>SFLSMGRCD</td>
					<td> </td><td> </td></tr>
				<tr><td>SFLNXTCHG</td>
					<td> </td><td> </td></tr>
				<tr><td>[SFLPAG](..\..\MonarchFX\_HTML\amfDdsSubfileControlClassPageProperty.html)</td>
					<td> </td><td> </td></tr>
				<tr><td>SFLPGMQ</td><td> </td><td> </td></tr>
				<tr><td>[SFLSIZ](..\..\MonarchFX\_HTML\amfDdsSubfileControlClassSizeProperty.html)</td><td> </td><td> </td></tr>
</table>	

## Display Attributes for DSPATR Keyword
<table  class="members" >
                     <colgroup>
                    <col width="30%" /> 
                    <col width="30%" />  
                    <col width="30%" /> 
                    </colgroup>

                        <tr><th>Supported</th><th>Supported in future release</th><th>Not applicable</th></tr>
                        <tr><td style="height: 21px">ND-Non Display</td>
							<td style="height: 21px">HI-High Intensity</td>
							<td style="height: 21px">BL-Blinking Field</td></tr>
                        <tr><td style="height: 20px">PC-Position Cursor</td>
							<td style="height: 20px"></td>
							<td style="height: 20px">CS-Column Separator</td></tr>
                        <tr><td>PR-Protect</td><td> </td><td>MDT-Set Change Data Tag</td></tr>
                        <tr><td> </td>
							<td> </td>
							<td>OID-Operator Identification</td></tr>
                        <tr><td> </td>
							<td> </td>
							<td>SP-Select by Light Pen</td></tr>
                        <tr><td> </td><td> </td><td>RI-Reverse Image</td></tr>
                        <tr><td> </td><td> </td><td>UL-Underline</td></tr>
                        <tr><td> </td><td> </td><td>Program-to-system field</td></tr>
</table>

