---
title: DdsSubfile.DataOnly Property

Id: amfDdsSubfileClassDataOnlyProperty
TocParent: amfDdsSubfileClassPropertiesMain
TocOrder: 10

keywords: DataOnly property
keywords: DdsSubfile.DataOnly property
keywords: how to, control rendering subfile data to browser
keywords: subfiles, determine if data is rendered to browser
keywords: subfile fields, controlling data displayed
keywords: subfile records, controlling data displayed
keywords: web controls, controlling data rendered to browser
keywords: subfile usage, data only
keywords: subfile usage, controlling data rendering

---

Gets or sets a boolean value indicating whether the subfile has data only and the subfile contents are not to be rendered to the browser. The default is **False** .

#### Syntax
<pre class="prettyprint"> **BegProp DataOnly Access(*Protected) Type(*Boolean)
   BegGet;  BegSet** </pre>

#### Property Values
**True** if the subfile records contains data and the contents should not be rendered to the browser. **False** if the contents of the subfile are to be rendered to the browser.

#### Remarks
To set this property at design-time, click on the right of the **DataOnly** property and select ** *True* ** or ** *False* ** from the drop-down box.

If this property is set ** *True* ** , it is the responsibility of the programmer to process the data during the various control execution lifecycle phases and render the contents of the subfile. If needed, this may include:

- Copy Browser to Display File Phase: If this request is
        a postback, the data sent by the browser is normally copied
        to the display buffer data set. See 
        [
        Page.OnCopyBrowserToDspFile](amfPageClassOnCopyBrowserToDspFileMethod.html). Code-behind logic in the
        AVR Program can stop the processing of the
        business logic phase.
- Copy Display File to Browser Phase: Data is copied from
        the display buffer data set to the 'dds' controls in the
        page. Perform any updates before the output is rendered.
        Any changes made to the state of controls can be saved,
        while changes made in the rendering phase are lost. See 
        [
        Page.OnCopyDspFileToBrowser](amfPageClassOnCopyDspFileToBrowserMethod.html).

See the [ ASNA Monarch Control Execution Lifecycle Concepts](amfconControlExecutionLifecycle.html) for more information regarding the ASNA.Monarch.WebDspF methods and events that override the ASP.NET control execution life cycle.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsSubfile Class](amfDdsSubfileClass.html) <br /> [ DdsSubfile Class Members](amfDdsSubfileClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
