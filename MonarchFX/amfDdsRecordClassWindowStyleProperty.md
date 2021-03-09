---
title: DdsRecord.WindowStyle Property

Id: amfDdsRecordClassWindowStyleProperty
TocParent: amfDdsRecordClassPropertiesMain
TocOrder: 160

keywords: WindowStyle property
keywords: DdsRecord.WindowStyle property
keywords: Window pop-up, setting implementation style
keywords: Window PopUp, setting implementation style
keywords: Window Popup, setting implementation style
keywords: Popup Window, setting implementation style
keywords: Popup window, setting implementation style
keywords: Popup window, setting style
keywords: web controls, setting Pop-up Window style
keywords: how to, set Window pop-up style
keywords: display files, Window pop-up styles

---

Gets or sets the Window Pop-up implementation style.

#### Syntax
<pre class="prettyprint"> **BegProp WindowStyle Access(*Public) Type(ASNA.Monarch.WebDspF.WindowStyles)
   BegGet;  BegSet** </pre>

#### Property Values
**ASNA.Monarch.WebDspF.WindowStyles** containing the style to be used for the implementation of Window Pop-up.

#### Remarks
The enumeration **ASNA.Monarch.WebDspF.WindowStyles** defines two possible implementation styles:
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
           <col width="20%" />
           <col width="80%" />
          </colgroup>
          <tr><th>Value</th>
          <th>Description</th>
          </tr>

          <tr>
            <td>Modal   
 *(Default)* </td>
            <td>Calls showModalDialog()
            javaScript function.</td>
          </tr>
          <tr>
            <td>InLine</td>
            <td>Moves the record's fields
            into an HTML table and making use of the Z-index HTML
            element attribute to sort the order in which display
            elements are drawn, gives the appearance of an
            overlapping window. 
           <br />To give the illusion that elements
            in the 
 **background**  are not active, a cascading
            style with a dark background-color value and opacity
            filter is applied. This implementation includes
            javaScript to handle mouse events to allow the Pop-up
            table to be dragged around the application's window,
            repositioning the table when the mouse movement is
            released.</td>
          </tr>
</table>

Notes:

1. This property is inherited by class [ DdsSubfileControl](amfddsSubfileControlClass.html) and by [ DdsSubfile](amfDdsSubfileClass.html). In the case of DdsSubfile, the property is ignored.

2. This property shows up in the ASPX form Designer's property window under *Appearance* category.

####  Differences
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
           <col width="33%" />
           <col width="33%" />
           <col width="33%" />
           </colgroup>
          <tr><th>Feature</th>
          <th>Modal</th>
           <th>InLine</th>
         </tr>
          <tr>
            <td>Moving supported</td>
            <td>Yes 
            <br />Anywhere, including outside browser
            window.</td>
            <td>Yes 
            <br />Within application's window
            boundaries.</td>
                </tr>
                <tr>
                  <td>Re-sizing supported</td>
                  <td>Yes. Auto-scroll</td>
                  <td>No</td>
                </tr>
                <tr>
                  <td>Close window icon</td>
                  <td>Yes</td>
                  <td>No</td>
                </tr>
                <tr>
                  <td>Browser compatibility</td>
                  <td>Microsoft Internet Explorer
            only.</td>
                  <td>All major browsers.</td>
                </tr>
                <tr>
                  <td>Third party control
            compatibility</td>
                  <td>No</td>
                  <td>Yes</td>
                </tr>
                <tr>
                  <td>Configurable HTML
            style(s)</td>
            <td>Yes 
            <br />Defined by Yes
            <br />Defined by DdsRecord_Control.css"&gt;styles: 
            <pre>
DdsInlinePopUpBackground
<br />DdsInlinePopUpTable
<br />DdsInlinePopUpTitle
<br />DdsInlinePopUpContent
</pre></td><td></td>
          </tr>
</table>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ DdsFile.PopUpWindows Property](amfDdsFileClassPopUpWindowsProperty.html) <br /> [Monarch Migration Style Sheets and Templates](amfMoreAboutStyleSheets.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
