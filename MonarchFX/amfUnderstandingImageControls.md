---
title: Image Controls

Id: amfUnderstandingImageControls
TocParent: amfASNAMobileSupport
TocOrder: 50

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

# Image Controls

### What is a DdsImage?
ASNA Mobile Support includes the [DdsImage control](amfDdsImageClass.html) which allows users to display image files (.jpg, .bmp, .png, and so on) saved on the IBM i directly within the mobile application. This allows designers to easily display products or more elaborate, static graphical elements while keeping all of the files securely on the IBM i.

If more than one image is contained in a DdsImage control, it will display a gallery that presents each image in the order it was uploaded.

**Applicability:** This control was created for Mobile RPG, but will also work normally with Wings. It can be used in Monarch, but Monarch apps cannot use it to access images on the IFS.
![](Images/DdsImageTasks.png)

### DdsImage Property Tasks
These are the DdsImage's property tasks: 

<table class="TaskTable" border="1" cellspacing="0" cellpadding="0" width="637"> <tbody> <tr> <td valign="top" width="169"> <p align="center"> **Property** 
</td>
<td valign="top" width="468">

**Notes** 
</td>
</tr>
		 <tr>
            <td colspan="2" valign="top" width="185">

**Appearance** 
</td>
        </tr>
		<tr>
	<td>
   <code> **[Directory](amfDdsImageClassDirectoryProperty.html)** </code>

</td>
<td valign="top" width="468">

Full path to the file in the IFS. This is a constant value established at design time. The path includes all directories and file name.

</td>
</tr>
	<tr>
	<tr>
		<td valign="top" width="169">
			<code> **[DirectoryField](amfDdsImageClassDirectoryFieldProperty.html) &amp; [DirectoryFieldLength](amfDdsImageClassDirectoryFieldLengthProperty.html)** </code>
		</td>
		<td valign="top" width="468">
			These properties define a character field whose runtime value is to be used as the full path to the IFS file. If these properties are set,
			the <code> **Directory** </code> property is ignored.
		</td>
	</tr>
	<td>
   <code> **[Name](amfDdsImageClassNameProperty.html)** </code>
</td>
<td valign="top" width="468">

A name for the image control. This is a constant value established at design time.

</td>
</tr>
	<tr>
		<td valign="top" width="169">
			<code> **[NameField](amfDdsImageClassNameFieldProperty.html) &amp; [NameFieldLength](amfDdsImageClassNameFieldLengthProperty.html)** </code>
		</td>
		<td valign="top" width="468">
			These properties define a character field whose runtime value is to be used as the name of the image. If these properties are set,
			the <code> **Name** </code> property is ignored.
		</td>
	</tr>
			<tr>
	<td valign="top" width="169">
		<code> **[ViewType](amfDdsImageClassViewTypeProperty.html)** </code>
	</td>
		<td valign="top" width="468">
			This property defines how the images are displayed, <code>DisplayAll</code>, <code>None</code>, or <code>SwipeShow</code>.
		</td>
	</tr>

		 <tr>
            <td colspan="2" valign="top" width="185">

**Layout** 
</td>
        </tr>
		<tr>
	<td valign="top" width="169">
		<code> **[ImageLocation](http://msdn.microsoft.com/en-us/library/system.web.ui.webcontrols.webcontrol.height(v=vs.110).aspx">Height</a>
		&amp; <br /><a href="http://msdn.microsoft.com/en-us/library/system.web.ui.webcontrols.webcontrol.width(v=vs.110).aspx">Width</a>** </code>
	</td>
		<td valign="top" width="468">
			These properties define a character field whose runtime value is to be used as the name of the image. If these properties are set,
			the <code> **Name** </code> property is ignored.
		</td>
	</tr>

			 <tr>
            <td colspan="2" valign="top" width="185">

**Misc** 
</td>
        </tr>
	<tr>
	<td valign="top" width="169">
		<code> **<a href="amfDdsImageClassImageLocationProperty.html)** </code>
	</td>
	<td valign="top" width="468">
		Sets whether the Image file is stored locally, on the IFS, or online.</td>
	</tr>
			 <tr>
            <td colspan="2" valign="top" width="185">

**Data** 
</td>
        </tr>

<tr>
<td valign="top" width="169">

<code> **[MaxImages](amfDdsImageClassMaxImagesProperty.html)** </code>

</td>
<td valign="top" width="468">

Sets the maximum number of images that can be uploaded/displayed by a DdsImage control.

</td>
</tr>
		 <tr>
            <td colspan="2" valign="top" width="185">

**upload** 
</td>
        </tr>
	<tr>
	<td valign="top" width="169">

	<code> **[UploadCaption](amfDdsImageClassUploadCaptionProperty.html)** </code>

	</td>
	<td valign="top" width="468">

	Sets text to be displayed in order to explain the upload process.

	</td>
	</tr>
	<tr>
	<td valign="top" width="169">

	<code> **[UploadCondition](amfDdsImageClassUploadConditionProperty.html)** </code>

	</td>
	<td valign="top" width="468">

	An indicator expression enabling the upload capability of the control.
	</td>
	</tr>
	<tr>
		<td valign="top" width="169">
 **<code>[UploadedNameField](amfDdsImageClassUploadedNameFieldProperty.html)</code> &amp; 
			<code>[UploadedNameFieldLength](amfDdsImageClassUploadedNameFieldLengthProperty.html)</code>** 
		</td>
		<td valign="top" width="468">
			These properties define a character field where the name of the uploaded file will be made available to the RPG program.
		</td>
	</tr>
	<tr>
		<td valign="top" width="169">
			<code> **[UploadImageType](amfDdsImageClassUploadImageTypeProperty.html)** </code>
		</td>
		<td valign="top" width="468">
			The filetype that all uploaded images will be stored as. This is useful for keeping file sizes under control.
		</td>
	</tr>
	<tr>
		<td valign="top" width="169">

 **<code>[UploadKey](amfDdsImageClassUploadKeyProperty.html)</code>** 

		</td>
		<td valign="top" width="468">

	   Sets the function key reported to the IBM i when the upload button is touched. 
	   Can take any Function Key value. Defaults to <code>UNKNOWN</code>.

		</td>
	</tr>

</tbody>
</table>
</p>

### The Mechanics of a DdsImage
The <code>ImageLocation</code> property controls the location of the image files, these are the operations available for each one of the <code>ImageLocation</code> values:
<table border="0" cellPadding="0" cellSpacing="0">
						<tr>
							<td rowSpan="2" vAlign="top" width="130"><span>

 ImageLocation </span></td>
							<td colSpan="2" vAlign="top" width="246"><span>

 Wings/MR </span></td>
							<td colSpan="2" vAlign="top" width="246"><span>

 Monarch </span></td>
						</tr>
						<tr>
							<td vAlign="top" width="123"><span>

 Download </span></td>
							<td vAlign="top" width="123"><span>

 Upload </span></td>
							<td vAlign="top" style="width: 123px"><span>

 Download </span></td>
							<td vAlign="top" width="123"><span>

 Upload </span></td>
						</tr>
						<tr>
							<td vAlign="top" width="130">
							<div>
 <span>
 **HostIFS** </span> </td>
							<td vAlign="top" width="123">

 <span>
 Yes </span> </td>
							<td vAlign="top" width="123">

 <span>
 Yes </span> </td>
							<td vAlign="top" style="width: 123px">

 <span>
 no </span> </td>
							<td vAlign="top" width="123">

 <span>
 no </span> </td>
						</tr>
						<tr>
							<td vAlign="top" width="130">
							<div>
 <span>
 **ThisWebSite** </span> </td>
							<td vAlign="top" width="123">

 <span>
 Yes </span> </td>
							<td vAlign="top" width="123">

 <span>
 Yes </span> </td>
							<td vAlign="top" style="width: 123px">

 <span>
 Yes </span> </td>
							<td vAlign="top" width="123">

 <span>
 Yes </span> </td>
						</tr>
						<tr>
							<td vAlign="top" width="130">
							<div>
 <span>
 **ExternalSource** </span> </td>
							<td vAlign="top" width="123">

 <span>
 Yes </span> </td>
							<td vAlign="top" width="123">

 <span>
 no </span> </td>
							<td vAlign="top" style="width: 123px">

 <span>
 Yes </span> </td>
							<td vAlign="top" width="123">

 <span>
 no </span> </td>
						</tr>
</table>

The DdsImage makes it very easy to send an image stored in the IFS of the IBM i where the application is running to the mobile device, although it can also be used to present images from the web server or external sources. The control offers the below properties to point to the IFS file location and name: 
<table border="1" cellspacing="0" cellpadding="0" width="637">
    <tbody>
        <tr>
            <td valign="top" width="169">

**Property** 
</td>
            <td valign="top" width="468">

**Notes** 
</td>
        </tr>
                <tr>
            <td valign="top" width="169">

<code> **[ImageLocation](amfDdsImageClassImageLocationProperty.html)** </code> 
</td>
            <td valign="top" width="468">

This property determines whether the image file is stored on the IFS, the web server, or an external location.
</td>
        </tr>

        <tr>
            <td valign="top" width="169">

<code> **[Directory](amfDdsImageClassDirectoryProperty.html)** </code> 
</td>
            <td valign="top" width="468">

The path to the Directory in the IFS or Web Server. This is a constant value established at design time. 
</td>
        </tr>
        <tr>
            <td valign="top" width="169">

**<code>[DirectoryField](amfDdsImageClassDirectoryFieldProperty.html)</code> &amp; <code>[DirectoryFieldLength](amfDdsImageClassDirectoryFieldLengthProperty.html)</code>** 
</td>
            <td valign="top" width="468">

These properties define a character field whose runtime value is used as the path to the directory holding the image file. If these properties are set, the <code> **Directory** </code> property is ignored. 
</td>
        </tr>
        <tr>
            <td valign="top" width="169">

<code> **[Name](amfDdsImageClassNameProperty.html)** </code> 
</td>
            <td valign="top" width="468">

The name of the image file. This is a constant value established at design time. 
</td>
        </tr>
        <tr>
            <td valign="top" width="169">

**<code>[NameField](amfDdsImageClassNameFieldProperty.html)</code> &amp; <code>[NameFieldLength](amfDdsImageClassNameFieldLengthProperty.html)</code>** 
</td>
            <td valign="top" width="468">

These properties define a character field whose runtime value is used to get the name of the image file. If these properties are set, the <code> **Name** </code> property is ignored. 
</td>
        </tr>
    </tbody>
</table>

For example, an inventory processing application could rely on pictures stored in the IFS on the directory <code>'/Items/Pictures'</code>, each item could have its image stored in a .JPG file named as the Item's ID. If the developer wanted to show the user the item's image, he could add a DdsImage to the record format and set the following properties like this: <br/> <br/> 
<table border="1" cellspacing="0" cellpadding="0" width="313">
        <tbody>
            <tr>
                <td valign="top" width="169">

**Property** 
</td>
                <td valign="top" width="143">

**Value** 
</td>
            </tr>
            <tr>
                <td valign="top" width="169">

**[Directory](amfDdsImageClassDirectoryProperty.html)** 
</td>
                <td valign="top" width="143">

'/Items/Pictures' 
</td>
            </tr>
            <tr>
                <td valign="top" width="169">

**[NameField](amfDdsImageClassNameFieldProperty.html)** 
</td>
                <td valign="top" width="143">

Item_Image 
</td>
            </tr>
            <tr>
                <td valign="top" width="169">

**[NameFieldLength](amfDdsImageClassNameFieldLengthProperty.html)** 
</td>
                <td valign="top" width="143">

20 
</td>
            </tr>
        </tbody>
</table>

This would define a character field of length 20 called Item_Image. Before issuing the EXFMT to the record, the developer would move the file name to the Item_Image field, something like this: 
<pre>
    *...1....+....2....+....3....+....4....+....5....+....6....+....7...+....
   CL0N01Factor1+++++++Opcode(E)+Factor2+++++++Result++++++++Len++D+HiLoEq....
    *
 **C 	ITEMID 		CAT(P) 	'.JPG':0 	ITEM_IMAGE** 
 **C 			EXFMT 	MYREC** 
                    </pre>

The name of the file may contain the wild characters '*' and '?'. If a wild carded name is provided, Mobile RPG will search the directory for all image files that satisfy the name pattern. If more than one file is found, then the DdsImage will render as a group of images. For instance, the picture below used the following values: 
<table border="1" cellspacing="0" cellpadding="0" width="313">
        <tbody>
            <tr>
                <td valign="top" width="169">

**Property** 
</td>
                <td valign="top" width="143">

**Value** 
</td>
            </tr>
            <tr>
                <td valign="top" width="169">

<code> **[Directory](amfDdsImageClassDirectoryProperty.html)** </code> 
</td>
                <td valign="top" width="143">

'/Vehicles/Pictures' 
</td>
            </tr>
            <tr>
                <td valign="top" width="169">

<code> **[NameField](amfDdsImageClassNameFieldProperty.html)** </code> 
</td>
                <td valign="top" width="143">

ImgName 
</td>
            </tr>
            <tr>
                <td valign="top" width="169">

<code> **[NameFieldLength](amfDdsImageClassNameFieldLengthProperty.html)** </code> 
</td>
                <td valign="top" width="143">

32 
</td>
            </tr>
        </tbody>
</table>

<pre>
    *...1....+....2....+....3....+....4....+....5....+....6....+....7...+....
   CL0N01Factor1+++++++Opcode&amp;ExtExtended-factor2+++++++++++++++++++++++++++++
    *
 **C 			EVAL 	ImgName = %trimr(VHID) + '-????.jpg'** 
 **C 			EXFMT 	MYREC** 
 </pre>

All JPG files whose names were formed by concatenating the vehicle Id (VHID field) with a dash and 4 characters would appear on the screen. If the vehicle id was 'ABC', files named ABC-0001.jpg, ABC-0002.jpg, ABC-WXYZ.jpg, or ABC-A1B2.jpg would be selected (if present in the 'Vehicles/Pictures' directory).

![](images/DdsImage.png)

The Image control also includes upload functionality. which allows authorized users to upload pictures to the Mobile Page directly from their mobile device. This feature is dependent on the capabilities of the browser that the Mobile Page is accessed through, and may not function perfectly on older browsers. This option can be disabled at design time if the page is intended for more public use. Upload is controlled by the following properties:
<table border="1" cellspacing="0" cellpadding="0" width="637">
    <tbody>
        <tr>
            <td valign="top" width="169">

**Property** 
</td>
            <td valign="top" width="468">

**Notes** 
</td>
        </tr>
            <tr>
            <td valign="top" width="169">

<code> **[UploadButtonText](amfDdsImageClassUploadButtonTextProperty.html)** </code> 
</td>
            <td valign="top" width="468">

Sets the text on the upload button itself.
</td>
        </tr>

        <tr>
            <td valign="top" width="169">

<code> **[UploadCondition](amfDdsImageClassUploadConditionProperty.html)** </code> 
</td>
            <td valign="top" width="468">

An indicator expression enabling the upload capability of the control. 
</td>
        </tr>
        <tr>
            <td valign="top" width="169">

<code> **[UploadCaption](amfDdsImageClassUploadCaptionProperty.html)** </code> 
</td>
            <td valign="top" width="468">

Text to be shown explaining the upload process. 
</td>
        </tr>
        <tr>
            <td valign="top" width="169">

<code> **[UploadImageType](amfDdsImageClassUploadImageTypeProperty.html)** </code> 
</td>
            <td valign="top" width="468">

The filetype that all uploaded images will be stored as. This is useful for keeping file sizes under control. 
</td>
        </tr>
            <tr>
            <td valign="top" width="169">

<code> **[UploadMaxHeight](amfDdsImageClassUploadMaxHeightProperty.html)<br /> &amp;<br /> [UploadMaxWidth](amfDdsImageClassUploadMaxWidthProperty.html)** </code>
</td>
            <td valign="top" width="468">

These properties set limits on the dimensions of the uploaded images. They are useful in controlling file size and maintaining consistency.
</td>
        </tr>

        <tr>
            <td valign="top" width="169">

<code> **[UploadedNameField](amfDdsImageClassUploadedNameFieldProperty.html) &amp; [UploadedNameFieldLength](amfDdsImageClassUploadedNameFieldLengthProperty.html)** </code> 
</td>
            <td valign="top" width="468">

These properties define a character field where the name of the uploaded file will be made available to the RPG program. 
</td>
        </tr>
    </tbody>
</table>

If uploading is enabled, a set of widgets on the screen allow users to select an image from the mobile device's gallery, or to take a picture if the device has an integrated camera. (The <u>Add Picture</u> link and Upload button in the image above.) A thumbnail of the image will appear to confirm the upload, and the Upload button will turn green: touching red cancel button that appears on the thumbnail will delete the image. These elements are shown below:

![](images/DdsImage2.png)

When the user is satisfied with the chosen image, the touch of a button will start the upload process.

The image file is given the name specified in the <code> **Name/NameField** </code> properties. If the value given contains wildcards, Mobile RPG will generate a new name following the pattern of the wildcard name with random numbers used in place of the wild cards. The name used by Mobile RPG will be reported back in the field defined in the <code> **UploadedNameField** </code> property. The location of the new file will be the one specified in the <code> **Directory/DirectoryField** </code> properties.

Images can be extremely large files and there are often a lot of them, both of which can considerably slow down your Mobile App if it is not optimized to handle them properly. Four properties (three listed above) are helpful in managing the amount of bandwidth and storage space that images can take up:

- <code>[MaxImages](amfDdsImageClassMaxImagesProperty.html)</code> &#8211;

						Sets the maximum number of images that can be sent to 
					the browser when a user searches for images.
- <code>[UploadImageType](amfDdsImageClassUploadImageTypeProperty.html)</code> &#8211;
						Sets image type for uploaded images. More 
						efficient file types, like .png, can save a great deal 
						of space.
- <code>[UploadMaxHeight](amfDdsImageClassUploadMaxHeightProperty.html)</code> 
						and <code>[UploadMaxWidth](amfDdsImageClassUploadMaxWidthProperty.html)</code> &#8211;
						These let designers set limits on the dimensions of uploaded images. This 
						prevents very large files from using excessive system 
						resources on upload. Files that are already smaller than 
						the maximum dimensions will be unaffected.

#### Drag and drop Uploading
Images may now be uploaded using the familiar drag-and-drop technique:

1. The user selects a file they want to upload (from Windowes Explorer for example) then 
	starts a Drag operation (by holding the left mouse button on a traditional PC).
2. The user can then drag the file onto the uploads section, where the icon will change and a thumbnail version of the image will be shown.
3. Finally, the user releases the mouse button press ("Dropping" the file), and
	the DdsImage receives the file (as if it was selected from a dialog box).

### Swipe Galleries
As of version 8.0, DdsImage controls can display multiple images as either a thumbnail gallery or a mobile-style swipe gallery, based on the new [<code>ViewStyle</code>](amfDdsImageClassViewStyleProperty.html) property.

The behavior of the swipe gallery varies slightly based on the end-users' platform: On PC, large buttons that allow scrolling from image to image will appear to the left and/or right of the selected image (as long as there are more images before/after the selected one in the gallery). On a mobile platform, the buttons are absent and performing a swipe gesture scrolls through the images.

On both platform types, doubleclicking an image will show it in the fullest size allowed by the window, up to the full resolution of the original file. Users can continue scrolling through the full-sized images, until the translucent close button in the upper left corner is clicked or tapped. 
