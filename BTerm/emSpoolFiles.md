---
title: Spooled File Viewer

Id: emSpoolFiles
TocParent: Welcome
TocOrder: 130

keywords: Spool Files
keywords: BTerm Spool Files
keywords: BTerm Spooled Files
keywords: Spool File Viewer
keywords: Spooled File Viewer
keywords: Spooled Files

---

<table>
			    <tr>
			       <td> <span class="OH_MultiViewContainerPanelDhtmlTable">[ASNA Browser Terminal&#8482;  Admin Manual
				   ](../_Helphome.html)</span><br />
				   </td>
			    </tr>
</table>

# Spooled File Viewer
Added in version 9.0, BTerm allows users to "download" and print spooled files directly to .pdf files. This technique works via the <code>VIEWSPLF</code> and <code>LSTSPLF</code> commands:

#### VIEWSPLF
This command displays spooled files as .pdfs. It opens a browser page similar to the image below:

![](Images/Spooledfiles2.png)

Figure 1.

The parameters for <code>VIEWSPLF</code> are shown below:

![](Images/Spooledfiles4.png)

Figure 2.

The most vital parameters and how they're handled, are: <pre> FILE - same as CPYSPLF JOB - same as CPYSPLF SPLNBR - same as CPYSPLF CRTDATE - same as CPYSPLF PDFSTMF - Output IFS pathname for unique temp PDF RMVPDF(*YES/*NO) - Remove temp PDF after Display RMVSPLF(*YES/*NO) - Remove Spoolfile after Display </pre>

#### LSTSPF
This command lists all spooled files as .pdfs. When called as part of the Spoolfile Viewer it opens a browser page similar to the image below:

![](Images/Spooledfiles1.png)

Figure 3.

Tapping on the eye (![](Images/SpooledView.png)) icon will call <code>VIEWSPLF</code> for the selected file, opening a page as shown above in Figure 1.<br/> Any number of files for download (![](Images/SpooledDL.png)) or deletion (![](Images/SpoolTrash.png)) by tapping the appropriate icons. <br/> Tapping the green check mark (![](Images/SpoolCheck.png)) will download or delete any selected files.<br /> Tapping the reload {![](Images/Spoolreload.png)) icon refreshes the spooled file list.<br /> 

The <code>LISTSPLF</code> command takes the following parameters:

![](Images/Spooledfiles3.png)

Figure 4.

It calls <code>VIEWSPLF</code>, passing:
<pre>FILE, JOB, SPLNBR, CRTDATE (from DdsTable), plus:

      PDFSTMF: with user's home IFS + "/spoolfiles/" + unique (internal spoolfile identifier ) + &lt;file&gt;.pdf 

      RMVPDF(*YES) 

      RMVSPLF(*NO)</pre>

