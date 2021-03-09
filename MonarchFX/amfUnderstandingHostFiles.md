---
title: HostFile Controls

Id: amfUnderstandingHostFiles
TocParent: amfASNAMobileSupport
TocOrder: 45

keywords: ASNA Mobile RPG
keywords: ASNA Mobile RPG HostFiles
keywords: ASNA Mobile RPG, Hosted Files
keywords: Mobile RPG
keywords: FileHolders

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span></td>
			    </tr>
</table>

# HostFile Controls

### What is a DdsHostfile?
Just like the files holding images in the IFS can be sent to the device with [DdsImage](amfUnderstandingImages.html), other kinds of files in the IFS can be sent with the [DdsHostFile](amfDdsHostFileClass.html) control. For example, a PDF file holding a copy of an invoice could be made available to the app's user. 

**Applicability:** These controls can be used in Wings and Mobile RPG pages/apps.

### The Mechanics of a DdsHostfile.
The <code>DisplayType</code> property of DdsHostFile controls how the file sent to the device is shown to the user with the following options: 
- Show a hyperlink to display the file in a separate instance of the browser
- Show a hyperlink to display the file in the current window
- Embedded in a frame within the page

![](Images/DdsHostFileTasks.png)

### DdsHostFile Property Tasks
These are the DdsHostFile's significant properties: 

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
<td valign="top" width="169">

<code> **[Path](amfDdsHostFileClassPathProperty.html)** </code>

</td>
<td valign="top" width="468">

Full path to the file in the IFS. This is a constant value established at design time. The path includes all directories and file name.

</td>
</tr>
<tr>
<td valign="top" width="169">

<code> **[PathField](amfDdsHostFileClassPathFieldProperty.html) &amp; 
[PathFieldLength](amfDdsHostFileClassPathFieldLengthProperty.html)** </code>

</td>
<td valign="top" width="468">

These properties define a character field whose runtime value is to be used as the full path to the IFS file. If these properties are set,
the <code> **Path** </code> property is ignored.

</td>
</tr>
<tr>
<td valign="top" width="169">

<code> **[Text](amfDdsHostFileClassTextProperty.html)** </code>

</td>
<td valign="top" width="468">

A constant used as the hyperlink's text

</td>
</tr>
<tr>
<td valign="top" width="169">

<code> **[TextField](amfDdsHostFileClassTextFieldProperty.html) &amp; 
[TextFieldLength](amfDdsHostFileClassTextFieldLengthProperty.html)** </code>

</td>
<td valign="top" width="468">

These properties define a character field whose runtime value is to be used as the text for the hyperlink. If these properties are set, the **Text**  property is ignored.

</td>
</tr>
			<tr>
            <td colspan="2" valign="top">

**Behavior** 
</td>
			</tr>
<tr>
	<td valign="top" width="169">
		<code> **[DisplayType](amfDdsHostFileClassDisplayTypeProperty.html)** </code>
	</td>
	<td valign="top" width="468">
		Sets how the file is displayed on screen. May be a link that opens 
		a new window, a link that opens the file in the current window, or a 
		frame embedded in the current page.</td>
</tr>
	<tr>
            <td colspan="2" valign="top">

**Layout** 
</td>
			</tr>
<tr>
	<td valign="top" width="169">
		<code> **<a href="http://msdn.microsoft.com/en-us/library/system.web.ui.webcontrols.webcontrol.height(v=vs.110).aspx">Height</a>
		 &amp; 
		 <br /><a href="http://msdn.microsoft.com/en-us/library/system.web.ui.webcontrols.webcontrol.width(v=vs.110).aspx">Width</a>** 
		 </code>
	</td>
	<td valign="top" width="468">
		These properties set the height and width of the control in whichever unit is specified (pixels, by default).</td>
</tr>

</tbody>
</table>
</p>

### Example
The following sample has two DdsHostFile contols, one using a link, the other an EmbeddedFrame. They both target the same PDF file: "nv5555.pdf".
<pre class="prettyprint"><code class="html">		
	&lt;mdf:DdsBar ID="JobFootBar" runat="server" CssClass="DdsBar"&gt;
            &lt;mdf:DdsBarSegment ID="DdsBarSegment13"  &gt;
                &lt;mdf:DdsButton ID="JobFootBar_Refresh" runat="server" CssClass="NavButtonIcon"
                   AidKey="F5" ButtonStyle="Image" Image="../Themes/Current/Images/Refresh.png" /&gt;
            &lt;/mdf:DdsBarSegment&gt;
        &lt;/mdf:DdsBar&gt;

            &lt;br /&gt;

            The following pdf has a display type of LinkInNew

            &lt;br /&gt;

            &lt;mdf:DdsHostFile ID="DdsHostFile1" runat="server"
                      Path="Inv5555.pdf" 
                      DisplayType="LinkInNew" Text="Attachment One" /&gt;

            &lt;br /&gt;
            &lt;br /&gt;

            The following pdf has an EmbeddedFrame 

            &lt;br /&gt;

            &lt;mdf:DdsHostFile ID="DdsHostFile2" runat="server"
                      Path="Inv5555.pdf" 
                      DisplayType="EmbeddedFrame" Text="Attachement One" Width="320" Height="150" /&gt;			
    </code></pre>

This produces the following output:

![](..\images\HostFileOutput.png)

When the link is clicked it, it will download the .pdf with a browser-standard download dialog (Google Chrome on the left, Microsoft Internet Explorer on the right):

![](..\images\HostFileOutputChrome.png)![](..\images\HostFileOutputIE.png)

Clicking "Open" in Internet explorer (or opening the download through Chrome) will yield something like the following, as Adobe reader is called to open the pdf.

![](..\images\HostFileInAdobe.png)

Note that the display of PDFs on various devices might be affected by the software present on that machine. It may be necessary to download viewing software (such as Adobe reader) on some platforms.
