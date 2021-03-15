---
title: DdsRecord.EraseFormats Property

Id: amfDdsRecordClassEraseFormatsProperty
TocParent: amfDdsRecordClassPropertiesMain
TocOrder: 70

keywords: EraseFormats property
keywords: DdsRecord.EraseFormats property
keywords: EraseFormats Property Editor, setting values
keywords: Web server controls [ASNA Monarch], erasing record formats
keywords: erasing record formats
keywords: how to, set record formats to erase
keywords: how to, get record formats to erase
keywords: formats, erasing
keywords: record formats, erasing
keywords: web controls, setting record formats to erase
keywords: web controls, getting record formats to erase
keywords: subfiles, setting record formats to erase
keywords: subfiles, getting record formats to erase
keywords: subfile controls, setting record formats to erase
keywords: subfile controls, getting record formats to erase
keywords: subfile records, setting formats to erase
keywords: subfile records, getting formats to erase
keywords: records, setting record formats to erase
keywords: records, getting record formats to erase
keywords: display files, erasing record formats
keywords: conditioning expressions, record formats to erase
keywords: indicator expressions, record formats to erase

---

Gets or creates an instance of **ASNA.Monarch.WebDspF.EraseProperty** specifying which record formats are to be erased from the display when this record is written.

#### Syntax
<pre class="prettyprint"> **BegProp EraseFormats Access(*Public) Type(ASNA.Monarch.WebDspF.EraseProperty)
   BegGet;  BegSet** </pre>

#### Property Values
**ASNA.Monarch.WebDspF.EraseProperty** object containing the record format ID's to be erased from the display.

#### Remarks
The **EraseFormats** property allows you to specify which record formats you want to be erased from the display when this record is written. The default is ***ALL** , which indicates to remove all records.

To set the **EraseFormats** property at design-time, click on the far right side of the **EraseFormats** property and the **EraseFormats Property Editor** will display as shown below. See [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) and [ Monarch Web Control Indicator Expression Tester](amfMonarchWebControlIndicatorExpressionTester.html) for more information on setting the conditional indicators and testing your expressions.

<img id="Img1" src="Images/zzDdsRecordEraseFormats.JPG" /> 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ EraseProperty Class](amfErasePropertyClass.html) <br /> [ Conditional Properties Overview](amfconConditionalPropertiesOverview.html) <br /> [ Monarch Web Control Indicator Expression Tester](amfMonarchWebControlIndicatorExpressionTester.html) 
