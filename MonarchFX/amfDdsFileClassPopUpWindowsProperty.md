---
title: DdsFile.PopUpWindows Property

Id: amfDdsFileClassPopUpWindowsProperty
TocParent: amfDdsFileClassPropertiesMain
TocOrder: 160

keywords: PopUpWindows property
keywords: PopUpWindows property, third-party controls
keywords: DdsFile.PopUpWindows property
keywords: popup windows, rendering
keywords: popup windows, third-party controls consideration
keywords: display files, consideration for rendering popup windows
keywords: rendering, popup considerations
keywords: third-party controls, popup windows considerations
keywords: Web server controls [ASNA.Monarch], rendering popup windows
keywords: web controls, rendering popup windows
keywords: ASNA.Monarch.Web server controls, popup windows considerations

---

<span style="font-color:red"> **This property is obsolete.** </span>

Gets or sets a boolean value indicating if record formats marked with Window set <code> **True** </code> will render as a pop-up in the browser (see [ DdsRecord.Window](amfDdsRecordClassWindowProperty.html) property). The default is **True** .

#### Syntax
<pre class="prettyprint"> **BegProp PopUpWindows Access(*Public) Type(*Boolean)
   BegGet;  BegSet** </pre>

#### Property Value
Boolean. **True** indicates record formats marked **Window** ***True** will render as pop-ups in the browser; otherwise **False** .

#### Remarks
This property also controls whether the contents of the 'current' screen are saved to allow other files to popup their windows over this one. The **PopUpWindows** property has no effect if none of the record formats have **Window** set **True** .

To set this property at design-time, click to the right of the **PopUpWindows** property and select the true or false option from the drop-down list. The default is **True** .

**Special Consideration on how the PopUp window is Rendered** 

- The record formats height and width should fit entirely
        within the values specified for the 
        [
        DdsRecord.WindowHeight](amfDdsRecordClassWindowHeightProperty.html) and 
        [
        DdsRecord.WindowWidth](amfDdsRecordClassWindowWidthProperty.html) properties.  If not, scroll
        bars will be displayed in the rendered window.  
 **NOTE:**  Make sure to include room for
        this DdsFile control.
- The 
 **WindowHeight**  and 
 **WindowWidth**  properties dictate the popup
        window size.  The popup window format that is written
        first will be the "container" that dictates height and
        width for any subsequently written popup windows.
- Popup windows use WinPopup.aspx. 
        The cascading style sheet (css) specified in that
        file affects the appearance of only popup
        windows.  You can affect the appearance of popup
        windows by altering the css file referenced in
        WinPopup.aspx.  See 
        [Monarch
        Migration Style Sheets and Templates](amfMoreAboutStyleSheets.html) for additional
        information.
- You will need to use Monarch WebControls 8.1.127 or
        higher when working with Master and Content Pages.

**Special Considerations for Third-Party Controls** 

When windows are used in a record format, the use of third-party controls is discouraged. Here are several factors to consider.

The implementation of popup windows in Monarch requires that the HTML intended for a 'normal' page be copied into a DIV of the popup. Only the HTML is copied and no JavaScript is ran in the popup window. Many third-party controls require client-side JavaScript in order to function properly; this is particularly true if they raise events on the server.

Also, consider that the server loads an ASP.NET page every time it is requested and then unloads it after the request is completed - all the while giving the appearance of a continuous process. This illusion of continuity is maintained using ASP.NET and the Monarch Framework together to control the execution lifecycle of a session. Effectively, the Framework and Server Controls handle the interface with the browser via JavaScript and HTML.

Monarch has an additional phase and also overrides some methods in the lifecycle of a session. See [ Control Execution Lifecycle](amfconControlExecutionLifecycle.html) for more information on the Monarch Framework session lifecycle.

Because of this altered lifecycle, third-party controls are not aware of the control execution sequence and thus are unable to achieve the desired affect. Popup windows do not behavior correctly and events are not fired properly with third-party controls that are out of sync with the Monarch Control Execution Lifecycle.

The ASNA.rovided controls are build to follow the augmented execution lifecycle and should render correctly on popup windows.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsFile Class](amfDdsFileClass.html) <br clear="none" /> [DdsFile Class Members](amfDdsFileClassMembers.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
