---
title: ASNA Monarch Web Server Controls Overview

Id: amfWebServerControlsOverview
TocParent: amfASNAMonarchFrameworkConceptsMain
TocOrder: 120

keywords: ASNA Monarch WebDspF, Display File Web Control
keywords: Display file web controls, about
keywords: Web server controls [ASNA Monarch], about
keywords: concepts, ASNA.Monarch.WebDspF, web server controls
keywords: CssClass property, solution builder setting
keywords: CssClass property, migration considerations
keywords: CssClass property, about style sheets
keywords: CssEnterClass property, about style sheets
keywords: Web server controls [ASNA Monarch], third-party controls considerations
keywords: concepts, ASNA.Monarch, third-party controls considerations
keywords: third-party controls, ASNA Monarch considerations
keywords: concepts, ASNA Monarch, web server controls
keywords: concepts, ASNA Monarch, CssClass property setting
keywords: concepts, ASNA Monarch, CssClass migration considerations

---

The implementation of a Monarch Display File requires the use of specialized controls that provide runtime behavior; similar to those of the IBM i display file fields; and a way to set the formal description of the file including formats and field types. The **Monarch Server** Controls are a set of controls to facilitate the implementation of the semantics of DDS elements contained within the **ASNA.Monarch.WebDspF** namespace and in the **ASNA.Monarch.WebDspF.dll** assembly.

The Monarch Server Controls can be grouped into three categories: **File Level** , **Record Level** , and **Field Level** .

#### File Level
There is one control and one class in the file level category.

1. [DdsFile](amfDdsFileClass.html) ( **System.Web.UI.Control** ) is used mostly to control the location, look, and availability of the buttons that handle the AID key functionality. It also determines the location of the "message line". Messages are displayed immediately after the banner of AID keys. Refer to [ Web.Config Considerations](amfconWebConfigConsiderations.html) for more information on establishing the labels for Aid keys for foreign language applications.
2. [Page](amfPageClass.html) ( **System.Web.UI.Page** ) is a class that serves as the container of all record formats. This class plays the role of the workstation controller. This **Page** class is responsible for coordinating the flow of data from the AVR program to the browser.

#### Record Level (System.Web.UI.WebControls.Panel)
Records are field, constant, and control containers. A program writes records to make them "active". Each record defines an area of the display. When a program issues a read to a record format (or an execute format), the active records are rendered to the browser and the user is expected to enter data on the input capable fields. Once the user presses an AID key, the data for that requested record is returned to the program. (Refer to the [Web Functions Overview](amfFunctionsMainOverview.html) for information on how to programmatically return control to the program by simulating a key press in the browser.)

There are three controls used to define records: one for the regular records, one for the subfile records, and one for the subfile control.

3. [ DdsRecord](amfDdsRecordClass.html) is the container of fields and constants. DdsRecord is displayed as a Panel with Grid Layout allowing its contents to be in an absolute location with regards to the record. The **CssClass DdsRecord** determines the presentation format.
4. [ DdsSubfile](amfDdsSubfileClass.html) ( **ASNA.Monarch.WebDspF.DdsRecord)** defines the format of "row" in a subfile. When the page is rendered, the "row" is repeated multiple times, once for each record in the subfile.
5. [ DdsSubfileControl](amfddsSubfileControlClass.html) ( **ASNA.Monarch.WebDspF.DdsRecord)** is the controller and container of a subfile. A subfile is typically rendered in classic tabular format with each record in the subfile providing the data for a row and field shown as a column. It is possible however to render subfile records as a sequence of checkboxes, radio buttons, in a drop-down or a list box (see [ SubfileStyle](amfddsSubfileControlClassSubfileStyleProperty.html) property).

#### Field Level (System.Web.UI.WebControls.WebControl)
A field is the smallest unit of data that is recognized and handled by the data management support of the system. A field level description allows you to give the system detailed characteristics of a field. Only field-level descriptions can determine that valid data is specified for individual fields on a display. Fields are either:

6. [DdsField](amfDdsFieldClass.html):
        defines the common controls for all other data fields.
7. [DdsLink](amfDdsLinkClass.html): facilitates 
		  adding HTML links to a display file that when
        rendered, displays as a link in a new browser window.
8. [DdsButton](amfDdsButtonClass.html):
        defines a single "button" control for a corresponding
        attention key or function key defined in DdsRecord.
9. [DdsBar](amfDdsBarClass.html): defines a mobile-style navigation bar at the top or bottom of 
		  the screen.
10. [DdsImage](amfDdsImageClass.html): defines an image stored on the IBM i that will be shown on 
		  the Display File.
11. [DdsChart](amfDdsChartClass.html): 
		  defines a chart constructed from subfiles on the IBM i.
12. [DdsHostFile](amfDdsHostFileClass.html): defines a link to a file (such as a pdf) stored on the 
		  IBM i.
13. [DdsGMap](amfDdsGMapClass.html): defines an instance of the Google Maps API based on subfiles 
		  stored on the IBM i.
14. [DdsList](amfDdsListClass.html): defines a Mobile friendly list based on subfiles 
		  stored on the IBM i.
15. [DdsExpandingList](amfDdsExpandingListClass.html): defines a less feature rich list that gives users the ability to add more records based on subfiles 
		  stored on the IBM i.
16. [DdsTable](amfDdsTableClass.html): defines a Mobile friendly Table based on subfiles 
		  stored on the IBM i.
17. [DdsSwitch](amfDdsSwitchClass.html): defines a 
		 big, mobile friendly on/off switch control.
18. [Ddsarcode](amfDdsBarcodeClass.html): defines a 
		 control that allows users to scan barcode data directly to fields on the IBM i.

**DdsField Class is the base class for:** 

19. [
        DdsConstant](amfDdsConstantClass.html): defines a constant that displays as text
        i.e. for headings and field labels.
20. [
        DdsDataField](amfDdsDataFieldClass.html): base class for controls common to data
        fields.

**DdsDataField is the base class for:** 

21. [
        DdsCharField](amfDdsCharFieldClass.html): further defines a field of type *CHAR
        that can be displayed as a text box, a dropdown box, or a
        checkbox.
22. [
        DdsDecField](amfDdsDecFieldClass.html): further defines a decimal field of type
        Binary, Packed, or Zoned that displays as a text box or
        dropdown box for user input.
23. [
        DdsBaseDate](amfDdsBaseDateClass.html): further defines common fields for date
        fields.
24. [
        DdsTimeField](amfDdsTimeFieldClass.html): further defines a time field.
25. [
        DdsTimestampField](amfDdsTimeStampFieldClass.html): further defines a timestamp
        field.

**DdsBaseDate is the base class for** :

26. [
        DdsDateField](amfDdsDateFieldClass.html): further defines the properties and
        methods for a date field.
27. [
        DdsDecDateField](amfDdsDecDateFieldClass.html): further defines the properties and
        methods for a decimal date field.

There is some commonality in the behavior to these fields. Monarch captures this commonality in a class hierarchy as shown in the following diagram.
<dl><dd>
        <img id="IMG1" src="../Images/zzFieldHierarchy1.jpg" />
      </dd></dl>

#### Display Files
The image below shows a sample of a display file rendered by the browser with the server controls noted.
<dl><dd>
        <img id="IMG2" src="../Images/ServerControls.JPG" />
    </dd></dl>

#### Setting Properties
The implementation of a Monarch Display File requires the use of specialized controls that provide runtime behavior and a way to set the properties for the individual controls.

Setting properties can be accomplished in one of four ways:

28. Drag and drop a new DDS control onto the form and
        set the properties in the 
 **Property Task**  window that will appear as the control is
        added.
29. Drag and drop a new DDS control onto the form and
        set the properties in the 
 **Properties**  window.
30. Click the specific control on the form you want to edit
        and change the properties settings in the 
 **Properties**  window.
31. Select the control from the 
 **Properties**  window as shown below and select
        the control to edit from the drop-down list. Then edit the
        properties for the selected control.

<dl><dd>
        ![](Images/zzSettingPropertiesMain.jpg)
 </dd></dl>

#### Special Note Regarding Third-Party Controls
Here are several factors to consider when using 3rd party controls with Monarch. 

The implementation of popup windows in Monarch requires that the HTML intended for a "normal" page be copied into a &lt;div&gt; of the popup. Only the HTML is copied and no JavaScript is run in the popup window. Many third-party controls require client-side JavaScript in order to function properly; this is particularly true if they raise events on the server.

Also, consider that the server loads an ASP.NET page every time it is requested and then unloads it after the request is completed - all the while giving the appearance of a continuous process. This illusion of continuity is maintained using ASP.NET and the Monarch Framework together to control the execution lifecycle of a session. Effectively, the Framework and Server Controls handle the interface with the browser via JavaScript and HTML.

Monarch has an additional phase and overrides some methods in the lifecycle of a session. See [ Control Execution Lifecycle](amfconControlExecutionLifecycle.html) for more information on the Monarch Framework session lifecycle.

Because of this altered lifecycle, third-party controls are not aware of the control execution sequence and thus are unable to achieve the desired effect. Popup windows do not behave correctly and events are not fired properly with third-party controls that are out of sync with the Monarch Control Execution Lifecycle.

The ASNA provided controls are build to follow the augmented execution lifecycle and should render correctly on popup windows.

#### CssClass Property Migration Considerations
During migration, the Solution Builder in ASNA Monarch Cocoon updates the CssClass and CssEnterClass properties that control the appearance (font, font weight, point size, underline, italics, color, etc.) of individual controls. This file can be changed so that common formatting can be applied to all controls during the migration process. 

#### Next: [Overview of AidKeys](amfconOverviewofAidKeys.html)

#### Previous: [Web.Config Considerations](amfconWebConfigConsiderations.html)

#### See Also
[DdsFile Class](amfDdsFileClass.html)<br />[DdsSubfile Class](amfDdsSubfileClass.html)<br />[ DdsSubfileControl Class](amfddsSubfileControlClass.html)<br />[Page Class](amfPageClass.html)<br /> [ASNA Monarch Style Sheet Overview](amfConDisplayFilesStyleSheets.html)<br /> [Monarch Migration Style Sheets and Templates](amfMoreAboutStyleSheets.html) 
