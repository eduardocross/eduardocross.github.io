---
title: DdsSignature.Name Property

Id: amfDdsSignatureClassNameProperty
TocParent: amfDdsSignatureClassPropertiesMain
TocOrder: 30

keywords: Name property
keywords: DdsSignature.Name property

---

Gets or sets a Name for the file to be presented by the Image Control.

#### Syntax
<pre class="prettyprint"> **BegProp Name Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the Name for the file to be presented in the Web Display by the Image Control. Can be either a single fixed name or a wildcard name. Wildcards can be either:

- *****  represents a group of characters of any length. (<code>ABC*.png</code> 
		would be correct for <code>ABC.png</code>, <code>ABCD.png</code>, or <code>ABC123.png</code>.)
- **?**  represents a single character per <code>?</code>. (<code>ABC?.png</code> would return 
		<code>ABC1.jpg</code> or <code>ABCD.png</code>.)

**Note &#8212;** If there are multiple files found that satisfy the wildcard parameters, all of them will be displayed.

#### Remarks
If the control is not used to upload images, this property sets up an absolute Name, this control may best be used when the file to be presented on the page is unlikely to change at any forseeable point. This property is overriden by [NameField](amfDdsSignatureClassNameFieldProperty.html). 

#### Uploading
When uploading a file the *Name* value is used to name the uploaded image file. When uploading, the name may contain up to four question marks <code>?</code>. The question mark positions will be replaced, when a file is uploaded, with digits that will make the file name unique.

For example, assume the following:

- <code>UploadedNameField</code> is set to <code>'UPLOADNAME'</code>
- At the time of a user uploading a file the <code>UPLOADNAME</code> field has the value of <code>'ITEM-ABCXYZ-??.jpg'</code>

Then the uploaded file would be given a name in the range of <code>ITEM-ABCXYZ-00.jpg</code> through <code>ITEM-ABCXYZ-99.jpg</code>.

The actual number is detemined at random.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsSignature Description](amfUnderstandingImageControls.html)<br /> [ DdsSignature Class](amfDdsSignatureClass.html) <br /> [ DdsSignature Class Members](amfDdsSignatureClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
