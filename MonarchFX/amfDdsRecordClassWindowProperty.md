---
title: DdsRecord.Window Property

Id: amfDdsRecordClassWindowProperty
TocParent: amfDdsRecordClassPropertiesMain
TocOrder: 110

keywords: Window property
keywords: Window property, third-party controls
keywords: DdsRecord.Window property
keywords: Web server controls [ASNA Monarch], rendering popup windows
keywords: ASNA Monarch web server controls, popup windows considerations
keywords: windows, third-party controls consideration
keywords: third-party controls, window property considerations
keywords: how to, set window as pop-up
keywords: how to, get if window is pop-up
keywords: web controls, setting window as pop-up
keywords: web controls, getting if window is pop-up
keywords: subfiles, setting window as pop-up
keywords: subfiles, getting if window is pop-up
keywords: subfile records, setting window as pop-up
keywords: subfile records, getting if window is pop-up
keywords: records, setting window as pop-up
keywords: records, getting if window is pop-up
keywords: display files, setting window as pop-up
keywords: display files, getting if window is pop-up
keywords: windows, setting as pop-up
keywords: windows, getting if window is pop-up
keywords: pop-up windows, setting as
keywords: pop-up windows, getting if

---

Gets or sets a boolean value indicating if the record is to be displayed as a popup window. The default is **False** .

#### Syntax
<pre class="prettyprint">
 **BegProp Window Access(*Public) Type(*Boolean)
   BegGet;  BegSet** 
            </pre>

#### Property Values
Boolean. **True** indicates the record is a window; otherwise **False** .

#### Remarks
If [ DdsFile.PopUpWindows](amfDdsFileClassPopUpWindowsProperty.html) property is **TRUE** and this property is also **True** , this record will render as a pop-up window. The style of the pop-up window, depends ond the [ DdsRecord.WindowStyle](amfDdsRecordClassWindowStyleProperty.html) property (each of the two styles has browser compatibilities restrictions).

To set this property at design-time, click on the right of the **Window** property and select the true or false option from the drop-down list. The default is **False** .
**
Special Consideration on how the PopUp window is Rendered
** 

- The record formats height and width should fit entirely
        within the values specified for the 
        [
        WindowHeight](amfDdsRecordClassWindowHeightProperty.html) and 
        [
        WindowWidth](amfDdsRecordClassWindowWidthProperty.html) properties.  If not, scroll bars will
        be displayed in the rendered window.  
 **NOTE:**  Make sure to include room for
        the DdsFile control.
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

**
Special Considerations for Third-Party Controls
** 

When windows are used in a record format, the use of third-party controls is discouraged. Here are several factors to consider.

The implementation of popup windows in Monarch requires that the HTML intended for a 'normal' page be copied into a DIV of the popup. Only the HTML is copied and no JavaScript is ran in the popup window. Many third-party controls require client-side JavaScript in order to function properly; this is particularly true if they raise events on the server.

Also, consider that the server loads an ASP.NET page every time it is requested and then unloads it after the request is completed - all the while giving the appearance of a continuous process. This illusion of continuity is maintained using ASP.NET and the Monarch Framework together to control the execution lifecycle of a session. Effectively, the Framework and Server Controls handle the interface with the browser via JavaScript and HTML.

Monarch has an additional phase and also overrides some methods in the lifecycle of a session. See [ Control Execution Lifecycle](amfconControlExecutionLifecycle.html) for more information on the Monarch Framework session lifecycle.

Because of this altered lifecycle, third-party controls are not aware of the control execution sequence and thus are unable to achieve the desired affect. Popup windows do not behave correctly and events are not fired properly with third-party controls that are out of sync with the Monarch Control Execution Lifecycle.

The ASNA provided controls are build to follow the augmented execution lifecycle and should render correctly on popup windows.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ DdsRecord.WindowStyle Property](amfDdsRecordClassWindowStyleProperty.html) <br /> [ DdsFile.PopUpWindows Property](amfDdsFileClassPopUpWindowsProperty.html) <br /> [Monarch Migration Style Sheets and Templates](amfMoreAboutStyleSheets.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
