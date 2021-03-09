---
title: Display File Concepts Overview

Id: amfconDisplayFiles
TocParent: amfASNAMonarchFrameworkConceptsMain
TocOrder: 80

keywords: display files, overview
keywords: overview of display files
keywords: ASNA Monarch, Display Files
keywords: concepts, ASNA.Monarch Display Files
keywords: display files, ASNA.Monarch versus Legacy
keywords: ASNA.Monarch, Monarch Display Files vs Legacy Display Files
keywords: ASNA.Monarch concepts, Monarch Display Files vs Legacy Display Files

---

#### IBM i Display Files
An IBM i Display File is composed of one or more formats, each defining a template of what is to be shown in a segment of the screen. Each format may contain input and/or output fields and constants as well as directives on how to display each of these elements and the interaction of this format with other formats present on the screen.

DDS is the primary means of defining a display file. <span style="mso-spacerun: yes">As part of the write operation, each</span> element in a display file might be conditioned with an array of boolean indicators enabling the display file engine to determine whether to display conditioned elements. See [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) for more information on conditioning elements.

With each format definition, a list of AID keys (i.e. function and Attention keys) available to the user is specified. As part of each entry in the list, a caption is provided and the index of the indicator array to "turn on" if the user does indeed press that key.

#### Externally Described Display Files
Besides describing the layout of a portion of the screen, a record format defines a group of fields whose data is obtained or delivered to a program using the file. When a programmer wants to manipulate a display file in an RPG program, all they have to do is code a "File Specification" (or F-Spec)naming the desired file and then use the name of the fields and records throughout the program. When the program is compiled, the RPG compiler requests (from the system) the layout of the record format with all the definitions of the fields and includes these definitions as part of the compilation. This technique is commonly referred to in the IBM i as using "externally described files", in contrast to "program described files". Program described files include explicit definitions of the fields in a record format and the actual layout of the fields in the record.

By using externally described files, when a field is added, deleted, or modified in any of the record's formats, the programmer need only recompile the program and the compiler will pick-up the new definition. Obviously if a format was modified, the program will typically have to do something about the new/modified fields, but it is not necessary to have the program describe the actual change of the record format. If the change to a display file only affects the presentation of the data in the screen, then it is not even necessary to recompile the program.

**Note &#8211;** Externally described display files are a requirement for working with ASNA Wings<sup>TM</sup> and ASMA Mobile RPG<sup>TM</sup>.

#### Monarch Display Files
As part of the Monarch Framework, a new generation of Display Files is provided. The Monarch Display File Agent targets these new Monarch Display Files when migrating IBM i Display Files.

The facilities provided by Monarch for the implementation of Display Files are:

- Framework uses ASPX pages as Display Files ([Framework
        ASPX Session Overview](amfconFrameworkASPXSessionOverview.html))
- Set of Server Controls to implement records, fields and
        constants ([Web
        Server Controls Overview](amfWebServerControlsOverview.html))
- Allows aid key text values to be applied globally in
        the web.config file ([Web.config Considerations](amfconWebConfigConsiderations.html))
- Migrated Display Files are &quot;content&quot; pages and use the master page 
		  files MasterPages.master and MasterPages.window.master ([Master Pages](amfconDisplayFilesMasterPages.html))
- Support to AVR to implement Workstation files (see
        following commands)

The Framework and Server Controls handle the interface with the browser via JavaScript and HTML. They are responsible for creating the html sent to the browser and handling the incoming request's data. A .NET dataset is used to communicate the data (and indicator array) to and from the server controls and the program using the display file.

Monarch Framework <code> **DclWorkstnFile** </code> provides the command specifically to declare a workstation file. A workstation file is the RPG construct that permits the programmer to perform I/O operations against a display file, thus treating it as if it were a virtual data file. Most of the logic deals with handling the user input and the preparation of output directed to the workstation file formats. Moving data between the Workstation File and the Display File in an interactive application is a cooperative effort between the procedural program running and the code behind the page implementing the Display File.

The procedural program uses a workstation file via the and issues read and write instructions against the record formats that provide data to or request data from the user. Connected to this workstation file is the code behind a web page containing the definition of the record formats and fields in the display file.

#### Legacy Display Files vs. Monarch Display Files
The similarities and differences of a Legacy IBM i Display File and a Monarch Display File follow.

Both files are multi-format files. Monarch uses a special web control called [ DdsRecord](amfDdsRecordClass.html) that operates as a panel or group box to contain the other controls serving as fields. Both files allow the use of conditional indicators to control the visibility and other behavior and presentation attributes of properties. Conditional indicators can also be used to control which AID keys are available to the application user. [DdsFile](amfDdsFileClass.html) is used for the availability of the AID keys, their respective values and for error messages, while the master page themes manipulate the overall look. 

Monarch also provides specialized versions of the **DdsRecord** control for subfiles ([DdsSubfile](amfDdsSubfileClass.html)) and for subfile controls ([DdsSubfileControl](amfddsSubfileControlClass.html)). To implement fields, Monarch provides the controls: [ DdsCharField](amfDdsCharFieldClass.html), [ DdsDecField](amfDdsDecFieldClass.html), [ DdsDecDateField](amfDdsDecDateFieldClass.html), [ DdsTimeField](amfDdsTimeFieldClass.html), [ DdsTimestampField](amfDdsTimeStampFieldClass.html), and [ DdsDateField](amfDdsDateFieldClass.html), while [ DdsConstant](amfDdsConstantClass.html) and [DdsLink](amfDdsLinkClass.html) are provided for constants and HTML links respectively.

**Special Note:** During Migration, a record format name from the Legacy Source Display File will have an underscore (<code>_</code>) prefixed to it in the ID property when the .aspx file is created. This alters the record format name that may otherwise conflict with a keyword in the forms designer. The <code>Alias</code> property is set to the original record format name used by the compiler. For example if the DDS record format name is "<code>MYWINDOW</code>", the .aspx file would contain <code>id="_MYWINDOW"</code> and <code>Alias="MYWINDOW"</code>. The same applies to subfile and subfile control records as well.

As an RPG construct, the way to use Display Files in legacy RPG or Visual RPG is fairly identical. The workstation file must be declared in the program followed by the use of an operation code (Open, Close, Read, Write, Delete, Update, <code>EXFMT</code> or <code>READC</code>).

The big difference between the Legacy and Monarch Display Files is the fact that you can include arbitrary .NET controls in Monarch, HTML is used to define the aspx page, and master pages with themes are utilized to provide a standardized appearance. On an IBM i, you are restricted to only those capabilities made available via DDS.

The following table shows a summary of the differences between the two display file types:
<table class="mytable" style="border-spacing: 2px" cellspacing="0" width="80%" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 40%" />
            <col span="1" style="WIDTH: 40%" />
          </colgroup>
          <tr>
            <th>Legacy Display File</th>
            <th>Monarch Display File</th>
          </tr>
          <tr>
            <td>As an IBM i Object 
- A special 
 **multi-format**  file object.
- **DDS**  is used to describe it.
- **Elements**  may be conditioned by
              indicators.
- AID (function) key behavior is defined for each
              format.

</td>
            <td>As a windows file 
- A special 
 **multi-panel** *Flow layout*  aspx Web Form 
				using **master pages and themes** .
- **HTML**  is used to describe it.
- **Web server controls**  allow conditional
              indicators.
- AID (function) key behavior is defined for each
              format **and has placement controlled with master pages** .
- **Arbitrary .NET controls allowed.**

</td>
          </tr>
          <tr>
            <td>As an RPG&#174; construct 
- Declared by 
              <code> **WORKSTN** </code> opcode in <code>'F'</code> specs.
- Basic means to implement interactive
              applications.
- Allows reading from keyboard and displaying data
              to the terminal.

</td>
            <td>As an ASNA Visual RPG&#174;
            construct 
- Declared by 
              <code> **DclWorkstnFile** </code> operation code.
- Basic means to implement interactive
              applications.
- Allows reading from keyboard and displaying data
              to the web browser.

</td>
          </tr>
</table>

#### Next: [ASNA Monarch Theme Components](amfconDisplayFilesThemeComponents.html)

#### Previous: [ASNA Monarch Templates](amfconMonarchJobandProgramClasses">Monarch Job and Program Classes</a>

#### See Also
<dl>
       <dd><a href="amfconDisplayFilesTemplates.html)</dd>
      <dd>[ASNA Monarch Master Pages](amfconDisplayFilesMasterPages.html)</dd>
      <dd>[ASNA Monarch Cascading Style Sheets](amfconDisplayFilesStyleSheets.html)</dd>
      <dd>[Web.config Considerations](amfconWebConfigConsiderations.html)</dd>
      <dd>[Monarch Framework ASPX Session Overview](amfconFrameworkASPXSessionOverview.html) </dd>
      <dd>[Aid Keys Overview](amfconOverviewofAidKeys.html)</dd>
      <dd>[Enhancing Applications with Non-Display File ASPX Pages](amfconEnhancingWithNonDisplayFileASPX.html)</dd>
</dl>

