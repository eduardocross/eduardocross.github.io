---
title: DdsRecord.WindowFeatures Property

Id: amfDdsRecordClassWindowFeaturesProperty
TocParent: amfDdsRecordClassPropertiesMain
TocOrder: 120

keywords: WindowFeatures property
keywords: DdsRecord.WindowFeatures property
keywords: how to, set control pop-up window features
keywords: how to, get control pop-up window features
keywords: web controls, setting pop-up window features
keywords: web controls, getting pop-up window features
keywords: subfiles, setting pop-up window features
keywords: subfiles, getting pop-up window features
keywords: subfile controls, setting pop-up window features
keywords: subfile controls, getting pop-up window features
keywords: subfile records, setting pop-up window features
keywords: subfile records, getting pop-up window features
keywords: records, setting pop-up window features
keywords: records, getting pop-up window features
keywords: display files, setting pop-up window features
keywords: display files, getting pop-up window features
keywords: pop-up windows, setting window features
keywords: pop-up windows, getting window features
keywords: windows, setting pop-up window features
keywords: windows, getting pop-up window features

---

This property is a string that is passed as the features parameter to the ShowModalDialog of IE. It is used to control some of the features of the pop-up windows. 
<!-- -->
 <pre class="prettyprint"> **BegProp WindowFeatures Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

<!-- -->

#### Property Value
String. Gets or sets a value specifying the features of the windows ornaments for the dialog box, using one or more of the following semicolon-delimited values. The default is **status:no;resizable:yes** .
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
          <col width="20%" />
           <col width="20%" />
			<col width="60%" />
          </colgroup>
          <tr><th>Values</th>
          <th>Settings</th>
          <th>Description</th>
          </tr>
<tr><td>center:</td>
          <td><pre>{ yes  | no
    1  |  0
   on  | off }</pre></td>

          <td>This feature specifies
          whether to center the dialog window within the desktop.
          The default is 
 **yes** .</td></tr>
          <tr>
          <td>dialogHide:</td>

          <td><pre>{ yes  | no
    1  |  0
   on  | off }</pre></td>
<td>This feature specifies
          whether to hide the dialog window when printing or using
          print preview. It is only available when a dialog box is
          opened from a trusted application. The default is 
 **no** .</td>
          </tr>         
          <tr>
          <td>edge:</td>
          <td><pre>{ sunken | raised }</pre></td>
          <td>This feature specifies the
          edge style of the dialog window. The default is 
 **raised** .</td></tr><tr><td>help:</td>
          <td><pre>{ yes  | no
    1  |  0
   on  | off }</pre></td>
          <td>This feature specifies
          whether the dialog window displays the context-sensitive
          Help icon. The default is 
 **yes** .</td></tr><tr><td>resizable:</td>
          <td><pre>{ yes  | no
    1  |  0
   on  | off }</pre></td>
<td>This feature specifies
          whether the dialog window has fixed dimensions. The
          default is 
 **no** .</td></tr><tr><td>scroll:</td>
          <td><pre>{ yes  | no
    1  |  0
   on  | off }</pre></td>
<td>This feature specifies
          whether the dialog window displays scroll bars. The
          default is 
 **yes** .</td></tr><tr><td>status:</td>
          <td><pre>{ yes  | no
    1  |  0
   on  | off }</pre></td>
<td>This feature specifies
          whether the dialog window displays a status bar. The
          default is 
 **yes**  for untrusted dialog windows and 
 **no**  for trusted dialog windows.</td></tr><tr><td>unadorned:</td>
          <td><pre>{ yes  | no
    1  |  0
   on  | off }</pre></td>
<td>This feature specifies
          whether the border window chrome displays for the dialog
          window It is only available when a dialog box is opened
          from a trusted application. The default is 
 **no** .</td>
          </tr>
</table>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecordClass](amfDdsRecordClass.html)<br />[DdsRecord Class Members](amfDdsRecordClassMembers.html)<br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
