---
title: Supported Display File DDS Keywords

Id: SupportedDspDDS
TocParent: amfWebServerControlsOverview
TocOrder: 30

keywords: ASNA Monarch
keywords: ASNA Wings display files
keywords: ASNA Monarch display files DDS keywords
keywords: ASNA Monarch display files field level DDS keywords
keywords: ASNA Monarch display files record level DDS keywords
keywords: ASNA Monarch display files subfile keywords
keywords: ASNA Monarch display attributes for DSPATR keyword
keywords: Monarch

---

<table>
			    <tr>
			       <td> <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0
				   </span><br /></td>
			    </tr>
</table>

# Supported Display File DDS Keywords
The following tables specify the level of support provided by ASNA Monarch Framework for DDS keywords. Links from keywords lead to the classes and properties that handle them.

## Display Field-Level Keywords
<table  class="members" >
                    <colgroup>
                    <col width="30%" /> 
                    <col width="30%" />
                    <col width="30%" />
                    </colgroup>
                        <tr><th>Supported</th><th>Supported</th><th>May Be Supported in Future Release</th><th>Not Applicable</th></tr>
                        <tr><td style="height: 23px">AID</td>
							<td style="height: 23px">[ERRMSG](amfDdsFieldClassErrorMessageProperty.html)</td>
							<td style="height: 23px">CHKMSGID</td>
							<td style="height: 23px">BLKFOLD</td></tr>
                        <tr><td>ALIAS</td><td>[ERRMSGID](amfDdsFieldClassErrorMessageIDProperty.html)</td>
							<td>DFTVAL</td>
							<td>CHRID</td></tr>
						<tr><td style="height: 25px">AUTO<sup>1</sup></td>
							<td style="height: 25px">LOWER</td>
							<td style="height: 25px">DLTCHK</td>
							<td style="height: 25px">DUP</td></tr>	
						<tr><td style="height: 25px">[BLANKS](amfDdsDecFieldClassBlanksIndProperty.html)</td>
							<td style="height: 25px">MSGCON</td>
							<td style="height: 25px">FLDCSRPRG</td>
							<td style="height: 25px"> EDTMSK</td></tr>
                        <tr><td style="height: 23px">CHECK <sup>2</sup></td>
							<td style="height: 23px">MSGID</td>
							<td style="height: 23px">FLTFIXDEC</td>
							<td style="height: 23px">ENTFLDATR</td></tr>
                        <tr><td>CHGINPDFT</td><td>OVERLAY<sup>4</sup></td><td>FLTPCN</td><td>NOCCSID</td></tr>
                        <tr><td style="height: 23px">CMP</td>
							<td style="height: 23px">RANGE</td>
							<td style="height: 23px">HTML</td>
							<td style="height: 23px">OVRATR</td></tr>
                        <tr><td style="height: 23px">[CNTFLD](amfDdsCharfieldClassInputStyleProperty.html)</td>
							<td style="height: 23px">REFFLD</td>
							<td style="height: 23px">INDTXT</td>
							<td style="height: 23px">OVRDTA</td></tr>
                        <tr><td style="height: 23px">COLOR</td>
							<td style="height: 23px">[SFLSIZ](amfDdsSubfileControlClassSubfileSizeProperty.html)</td>
							<td style="height: 23px">MAPVAL</td>
							<td style="height: 23px">PUTRETAIN</td></tr>
                        <tr><td style="height: 23px">COMP</td>
							<td style="height: 23px">SYSNAME</td>
							<td style="height: 23px">VALNUM</td>
							<td style="height: 23px">WRDWRAP</td></tr>
                        <tr><td style="height: 24px">DATE</td>
							<td style="height: 24px">TEXT</td>
							<td style="height: 24px"></td>
							<td style="height: 24px"></td></tr>
                        <tr><td>DATFMT</td><td>TIME</td>
							<td></td>
							<td></td></tr>
                        <tr><td style="height: 20px">DATSEP</td>
							<td style="height: 20px">TIMFMT</td>
							<td style="height: 20px"></td>
							<td style="height: 20px"></td></tr>
                        <tr><td style="height: 24px">DFT</td>
							<td style="height: 24px">TIMSEP</td>
							<td style="height: 24px"></td>
							<td style="height: 24px"></td></tr>
                        <tr><td>DLTEDT</td><td>USER</td>
							<td></td>
							<td></td><td></td></tr>
                        <tr><td>DSPATR <sup>3</sup></td><td>VALUES</td><td></td><td></td></tr>
                        <tr><td style="height: 22px">[EDTCDE](SharedEditCodeTable.html)</td>
							<td style="height: 22px"></td>
							<td style="height: 22px"></td>
							<td style="height: 22px"></td></tr>
                        <tr><td>[EDTWRD](SharedEditWordTable.html)</td><td> </td><td></td><td></td></tr>
</table>
<div>

<sup>1 </sup>The supported function are RA, RAB, and RAZ.

<sup>2 </sup>The supported functions are AB, LC, ER, RB, RZ, [ME](amfddsDataFieldClassMandatoryEnterProperty.html), [MF](amfddsDataFieldClassMandatoryEnterProperty.html), M10, and M11.

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
                        <tr><th>Supported </th><th>May Be Supported in Future Release</th><th>Not Applicable</th><th>Not Applicable</th></tr>
                        <tr><td>ALTNAME</td><td>CLEAR</td><td>ALARM</td><td>KEEP</td></tr>
                        <tr><td>[CAnn](amfDdsRecordClassAttnKeysProperty.html)</td><td>CLRL</td><td>ALWGPH</td><td>LOCK</td></tr>
                        <tr><td>[CFnn](amfDdsRecordClassFuncKeysProperty.html)</td><td>INZRCD</td><td>ALWROL</td><td>MDTOFF</td></tr>
                        <tr><td>CHANGE</td><td>INDTXT</td><td>ASSUME</td><td>MSGALARM</td></tr>
                        <tr><td>[CHECK](SupportedDspDDSCheck.html)<sup>2</sup></td><td>LOGINP</td><td>BLINK</td><td>OVRATR</td></tr>
                        <tr><td style="height: 23px">CHGINPDFT</td>
							<td style="height: 23px">LOGOUT</td>
							<td style="height: 23px">CCSID</td>
							<td style="height: 23px">OVRDTA</td></tr>
                        <tr><td>CSRLOC</td><td>VALNUM</td><td>CSRINPONLY</td><td>PUTOVR</td></tr>
                        <tr><td>ERASE</td><td></td><td>DSPMOD</td><td>PUTRETAIN</td></tr>
                        <tr><td>HELP<sup>5</sup></td><td> </td><td>ENTFLDATR</td><td>RETCMDKEY</td></tr>
                        <tr><td>OVERLAY<sup>6</sup></td><td> </td><td>ERASEINP</td><td>RETKEY</td></tr>
                        <tr><td>PAGEDOWN</td><td> </td><td>FRCDTA</td><td>RETLCKSTS</td></tr>
                        <tr><td>PAGEUP</td><td> </td><td>GETRETAIN</td><td>RMVWDW</td></tr>
                        <tr><td>PRINT</td><td> </td><td>HOME</td><td>UNLOCK</td></tr>
                        <tr><td>PROTECT</td><td> </td><td>INVITE</td><td>USRDFN</td></tr>
                        <tr><td>RTNCSRLOC <sup>7</sup></td><td></td><td>INZINP</td><td>WDWBORDER</td></tr>
                        <tr><td>RTNDTA</td><td></td><td></td><td>WRDWRAP</td></tr>
                        <tr><td>ROLLDOWN</td><td></td><td> </td><td> </td></tr>
                        <tr><td>ROLLUP</td><td></td><td> </td><td> </td></tr>
                        <tr><td>SETOF(F)</td><td></td><td></td><td></td></tr>
                        <tr><td>SLNO <sup>8</sup></td><td></td><td></td><td></td></tr>
                        <tr><td>TEXTVL</td><td> </td><td></td><td></td></tr>
                        <tr><td>DCMDKEY</td><td> </td><td> </td><td></td></tr>
                        <tr><td>[WDWTITLE](amfDdsRecordClassWindowTitleProperty.html)</td><td> </td><td></td><td></td></tr>
                  <tr><td>[WINDOW](amfDdsRecordClassWindowProperty.html)</td><td> </td><td></td><td></td></tr>
</table>
<div>

<sup>5 </sup>Only supported when used with a Response indicator.

<sup>6 </sup>Wings has a special procedure for handling the OVERLAY keyword.

<sup>7 </sup>Support is not provided for cursor positioning within a field.

<sup>8 </sup>Support is not provided for (*VAR)

## Display File-Level Keywords
<table  class="members" ><col width="30%" /> <col width="30%" /><col width="30%" />
                        <tr><th style="width: 233px">Supported</th><th>My Be Supported in Future Release</th><th>Not Applicable</th></tr>
                        <tr><td style="width: 233px; height: 23px">CAnn</td>
							<td style="height: 23px">ALTHELP</td>
							<td style="height: 23px">ALTPAGEDWN</td></tr>
                        <tr><td style="width: 233px">CFnn</td><td>CLEAR</td><td>ALTPAGEUP</td></tr>
                        <tr><td style="width: 233px">CHECK</td><td>DSPRL</td><td>ALWGPH</td></tr>
                        <tr><td style="width: 233px">CHGINPDFT</td><td>INDTXT</td><td>CSRINPONLY</td></tr>
                        <tr><td style="width: 233px">[ERRSFL](amfDdsFileClassErrorSubfileProperty.html)</td>MSGLOC<td></td><td>DSPSIZ</td></tr>
                        <tr><td style="height: 23px; width: 233px">INDARA</td>
							<td style="height: 23px">VALNUM</td>
							<td style="height: 23px">ENTFLDATR</td></tr>
                        <tr><td style="width: 233px">PAGEDOWN</td><td></td><td>HOME</td></tr>
                        <tr><td style="height: 23px; width: 233px;">PAGEUP</td>
							<td style="height: 23px"> </td>
							<td style="height: 23px">INVITE</td></tr>
                        <tr><td style="width: 233px">PRINT</td><td> </td><td>MSGALARM</td></tr>
                        <tr><td style="width: 233px; height: 23px;">REF</td>
							<td style="height: 23px"></td>
							<td style="height: 23px">OPENPRT</td></tr>
                        <tr><td style="width: 233px">ROLLDOWN</td><td></td><td>PASSRCD</td></tr>
                        <tr><td style="height: 23px; width: 233px">ROLLUP</td>
							<td style="height: 23px"></td>
							<td style="height: 23px">PRINT(Lib)/File)</td></tr>
                        <tr><td style="width: 233px; height: 23px;">VLDCMDKEY</td>
							<td style="height: 23px"></td>
							<td style="height: 23px">USRDSPMGT</td></tr>
                        <tr><td style="width: 233px">WDWBORDER</td><td> </td><td>WRDWRAP</td></tr>
						<tr><td style="width: 233px">HELP<sup>9 </sup></td><td> </td><td>MNUFLD</td></tr>
						<tr><td style="width: 233px"></td><td> </td><td>MNUBAR</td></tr>
						<tr><td style="width: 233px"></td><td> </td><td>MNUBARCHC</td></tr>
</table>

<sup>9 </sup>Only supported when used with a Response indicator.

## Subfile Keywords
<table class="members" >
					<colgroup>
						<col width="30%" />
						<col width="30%" /> 
						<col width="30%" />
					</colgroup>
				<tr><th>Supported</th><th>Supported</th><th>Not Applicable</th></tr>
				<tr><td>SFL</td><td>[SFLMODE ](amfDdsSubfileControlClassModeProperty.html)</td><td>SFLCSRPRG</td></tr>
				<tr><td>[SFLCLR](amfDdsSubfileControlClassClearProperty.html)</td><td>[SFLMSG](amfDdsSubfileControlClassMessageProperty.html)</td><td>SFLENTER</td></tr>
				<tr><td>[SFLCTL](amfddsSubfileControlClass.html)</td><td>[SFLMSGID](amfDdsSubfileControlClassMessageIDProperty.html)</td>	<td>SFLROLVAL</td></tr>
				<tr><td>SFLCSRRRN</td><td>SFLMSGKEY</td><td>SFLSCROLL</td></tr>
				<tr><td>SFLDLT</td><td>SFLRCDNBR</td><td></td></tr>

				<tr><td>[SFLDROP](amfDdsSubfileControlClassSflDropProperty.html)</td><td>SFLSMGRCD</td><td></td></tr>
				<tr><td>SFLDSP</td><td>SFLNXTCHG</td><td></td></tr>
				<tr><td>SFLDSPCTL</td><td>[SFLPAG](amfDdsSubfileControlClassPageProperty.html)</td><td></td></tr>
				<tr><td>[SFLEND](amfDdsSubfileControlClassSflEndProperty.html) </td><td>SFLPGMQ</td><td></td></tr>
				<tr><td>[SFLFOLD](amfDdsSubfileControlClassSflFoldProperty.html) </td><td>[SFLRNA](amfDdsSubfileControlClassInitNotActiveProperty.html)</td><td></td></tr>
				<tr><td>[SFLINZ](amfDdsSubfileControlClassInitializeRecordsProperty.html)</td><td>[SFLSIZ](amfDdsSubfileControlClassSizeProperty.html)</td>	<td></td></tr>
				<tr><td>SFLLIN</td>	<td></td><td></td></tr>

</table>	

## Display Attributes for DSPATR Keyword
<table  class="members" >
                     <colgroup>
                    <col width="30%" /> 
                    <col width="30%" />  
                    <col width="30%" /> 
                    </colgroup>

                        <tr><th>Supported</th><th>Not Applicable</th></tr>
                        <tr><td>BL-Blinking Field </td><td>MDT-Set Change Data Tag</td></tr>
                        <tr><td style="height: 20px">CS-Column Separator </td>

							<td style="height: 20px">OID-Operator Identification</td></tr>
						 <tr><td>HI-High Intensity</td> 

							<td>SP-Select by Light Pen</td></tr>
                        <tr><td>ND-Non Display </td><td></td></tr>
                        <tr><td> PC-Position Cursor</td> 
							<td></td></tr>
						<tr><td>PR-Protect</td><td></td></tr>
						<tr><td>Program-to-system field </td><td></td></tr>
               <tr><td>[RI-Reverse Image](amfDdsFieldClassInvertFontColor.html) </td>
							<td></td></tr>
                        <tr><td>[UL-Underline](amfDdsFieldClassUnderlineProperty.html) </td><td></td></tr>

</table>

