---
title: Uploader Controls

Id: amfUnderstandingUploaders
TocParent: amfASNAMobileSupport
TocOrder: 355

keywords: ASNA Mobile RPG
keywords: ASNA Wings, Image Control
keywords: ASNA Mobile, Images
keywords: Image Upload

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span></td>
			    </tr>
</table>

# Uploader Controls

### What is a DdsUploader?
ASNA Mobile Support includes the [DdsUploader control](amfDdsUploaderClass.html) which allows users to upload files (.pdf, .bmp, .png, and so on) easily to the IBM i.

**Applicability:** This control works with Monarch, Mobile RPG, and/or Wings.

### DdsUploader Property Tasks
These are the DdsUploader's property tasks: 

<table class="TaskTable" border="1" cellspacing="0" cellpadding="0" width="637"> <tbody> <tr> <td valign="top" width="169"> <p align="center"> **Property** 
</td>
<td valign="top" width="468">

**Notes** 
</td>
</tr>
<tr>
            <td colspan="2" valign="top">

**Appearance** 
</td>
			</tr>
	<tr>
	<td>
   <code> **[Caption](amfDdsUploaderClassCaptionProperty.html)** </code>
	</td>
	<td valign="top" width="468">
	The caption that will be displayed adjacent to the control.
</td>
</tr>
<tr>
            <td colspan="2" valign="top">

**Upload** 
</td>
			</tr>
		<tr>
	<td>
   <code> **[Directory](amfDdsUploaderClassDirectoryProperty.html)** </code>

</td>
<td valign="top" width="468">

Full path to upload storage in the IFS. This is a constant value established at design time. The path includes all directories and file name.

</td>
</tr>

	<tr>
		<td valign="top" width="169">
			<code> **[DirectoryField](amfDdsUploaderClassDirectoryFieldProperty.html) &amp; [DirectoryFieldLength](amfDdsImageClassDirectoryFieldLengthProperty.html)** </code>
		</td>
		<td valign="top" width="468">
			These properties define a character field whose runtime value is to be used as the full path to the IFS file. If these properties are set,
			the <code> **Directory** </code> property is ignored.
		</td>
	</tr>

	<tr>
		<td valign="top" width="169">
			<code> **[NameField](amfDdsUploaderClassNameFieldProperty.html) &amp; [NameFieldLength](amfDdsImageClassNameFieldLengthProperty.html)** </code>
		</td>
		<td valign="top" width="468">
			These properties define a character field whose runtime value is 
			either the original filename or the basis for a new one. 
		</td>
	</tr>
<tr>
            <td colspan="2" valign="top">

**Layout** 
</td>
			</tr>
<tr>
	<td valign="top" width="169">
		<code> **<a href="http://msdn.microsoft.com/en-us/library/system.web.ui.webcontrols.webcontrol.height(v=vs.110).aspx">Height</a>
		&amp; <br /><a href="http://msdn.microsoft.com/en-us/library/system.web.ui.webcontrols.webcontrol.width(v=vs.110).aspx">Width</a>** </code>
	</td>
		<td valign="top" width="468">
			These properties define the width and height of the uploader control.
		</td>
	</tr>

</tbody>
</table>
</p>

### The Mechanics of a DdsUploader
The DdsUploader control works by simply transferring files that are selected via a standard Windows "choose a file" dialog to an IBM i Directory. This breaks down to a three-step process:

1. The user will see the control much as it is presented below. <br /> <br />
				![](images/Uploader1.png)
2. Clicking the control opens a standard "choose a file" dialog, as shown below. <br /><br />![](images/Uploader2.png)
3. After uploading the filename will be shown instead of the caption text.  A user 
may then click or tap on the red X to doscard the file, or click on the filename to 
select another file and replace the current one. <br /><br />![](images/Uploader3.png)

Alternatively, users can simply drag and drop a file (on most browsers; only IE doesn't support it) from their desktop to the control. This is, also, a three step process:

4. The user selects a file they want to upload (from Windowes Explorer for example) then 
	starts a Drag operation (by holding the left mouse button on a traditional PC).
5. The user can then drag the file onto the uploader, where the icon will change.
6. Finally, the users releases the mouse button press ("Dropping" the file), 
	the DdsUploader receives the file (as if it was selected from a dialog box).

#### Web.config Requirements
Because large file uploads are considered a security vulnerability, the following Web.Config values must be changed if it's intended for users to be able to upload large files.7. <code>executionTimeout (default is 110 seconds)</code>
8. <code>maxRequestLength (default 4MB)</code>

### DdsUploaderExample
<pre>
&lt;mdf:DdsConstant ID="DriverLicenseLabel" runat="server" Text="Driver's License:" 
  style="display: block; float: left; padding-top: 4px; padding-right: 12px; margin-left: 3rem;"
/&gt;
&lt;mdf:DdsUploader ID="DriverLicenseFile" runat="server"
  UploadLocation="ThisWebSite"
  Caption = "Click to select Driver's license file"
  Directory = "UploadedFiles"
  NameField = "UPNAME"
  NameFieldLength ="128"
/&gt;
</pre>

