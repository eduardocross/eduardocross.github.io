---
title: Page Members

Id: amfPageClassMembers
TocParent: amfPageClass
TocOrder: 5

keywords: Page class
keywords: Page class, all members
keywords: members [ASNA.Monarch.WebDspF], Page class

---

[Page Overview](amfPageClass.html) 
<!--mine -->

#### Public Constructors
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="30%" /><col width="70%" />
          </colgroup>
          <tr><th>Method</th>
              <th>Description</th>
          </tr>
          <tr valign="top">
            <td>![public property" src="../Images/promethod.bmp" width="15" border="0" x-maintain-ratio="TRUE](../Images/Methods.bmp" />
              [Page](amfPageClassPageConstructors.html)
            </td>
            <td>Creates a new instance of a

 **Page**  object.</td>
          </tr>
</table>

<br />

<!--mine -->

#### Public Properties
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="30%" /><col width="70%" />
          </colgroup>
          <tr><th>Property</th>
              <th>Description</th>
          </tr>
          <tr>
            <td><img alt="public property" src="../Images/property.bmp" width="16" border="0" />
              [DataSet](amfPageClassDataSetProperty.html)
            </td>
            <td>Gets an instance of 
 **System.Data.DataSet** , which represents
            an in-memory cache of data.</td>
          </tr>
          <tr>
            <td><img alt="public property" src="../Images/property.bmp" width="16" border="0" />
              [
              RunProgram](amfPageClassRunProgramProperty.html)
            </td>
            <td>Gets or sets a boolean
            value indicating whether to pass control to the AVR
            program waiting.</td>
          </tr>
</table>

<!--mine -->

#### Protected Methods
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="30%" /><col width="70%" />
          </colgroup>
          <tr><th>Method</th>
              <th>Description</th>
          </tr>
          <tr>
            <td style="height: 31px"><img height="15)
              [
              ContinueExecution](amfPageClassContinueExecutionMethod.html)
            </td>
            <td style="height: 31px">Continues execution after
            execution has been paused.</td>
          </tr>
		  <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              GetDataRow](amfPageClassGetDataRowMethod.html)
            </td>
            <td>Gets the data from a row in a datatable.</td>
          </tr>
		  	<tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              GetDataTable](amfPageClassGetDataTableMethod.html)
            </td>
            <td>Gets a datatable from a specified format.</td>
          </tr>
		  <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              GetFieldValue](amfPageClassGetFieldValueMethod.html)
            </td>
            <td>Gets the value of a specified field.</td>
          </tr>
          <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              GetFileName](amfPageClassGetFileNameMethod.html)
            </td>
            <td>Gets the name of the file
            on the page.</td>
          </tr>
		  		  <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              GetOptionIndicator](amfPageClassGetOptionIndicatorMethod.html)
            </td>
            <td>Gets the specified indicator.</td>
          </tr>
		  		  <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              GetOptionIndicators](amfPageClassGetOptionIndicatorsMethod.html)
            </td>
            <td>Gets the specified indicators.</td>
          </tr>
		  		  		  <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              GetResponseIndicator](amfPageClassGetResponseIndicatorMethod.html)
            </td>
            <td>Gets the specified indicator.</td>
          </tr>
		  		  <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              GetResponseIndicators](amfPageClassGetResponseIndicatorsMethod.html)
            </td>
            <td>Gets the specified indicators.</td>
          </tr>
		  <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
            IsFormatActive](amfPageClassIsFormatActiveMethod.html)
            </td>
            <td>Tests whether the specified record format is active.</td>
          </tr>
          <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              OnCopyBrowserToDspFile](amfPageClassOnCopyBrowserToDspFileMethod.html)
            </td>
            <td>Allows you to intervene
            when data is being copied from the data sent by the
            browser to the display buffer data set. The Request is
            processed here.</td>
          </tr>
          <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0" x-maintain-ratio="TRUE" />
              [
              OnCopyDspFileToBrowser](amfPageClassOnCopyDspFileToBrowserMethod.html)
            </td>
            <td>Allows you to intervene
            when data is being copied from the display buffer data
            sent to the 'dds' controls in the page. The Response is
            formulated here.</td>
          </tr>
		 <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              Onload](amfPageClassOnLoadMethod.html)
            </td>
            <td>Allows you to intervene
            when data is being copied from the display buffer data
            sent to the 'dds' controls in the page. The Response is
            formulated here.</td>
          </tr>
          <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0" x-maintain-ratio="TRUE" />
              [
              PrepareRecord](amfPageClassPrepareRecordMethods.html)
            </td>
            <td>Overloaded. Returns the 
 **System.Data.DataRow**  object in
            preparation for the rendering phase.</td>
          </tr>
		  <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              SetFieldValue](amfPageClassSetFieldValueMethod.html)
            </td>
            <td>Sets the value of a selected field.</td>
          </tr>
		 <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              SetOptionIndicator](amfPageClassSetOptionIndicatorMethod.html)
            </td>
            <td>Sets the value of a selected option indicator.</td>
          </tr>
		  <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              SetResponseIndicator](amfPageClassSetResponseIndicatorMethod.html)
            </td>
            <td>Sets the value of a selected response indicator.</td>
          </tr>
		  		 <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              SetSubfileOptionIndicator](amfPageClassSetSubfileOptionIndicatorMethod.html)
            </td>
            <td>Sets the value of a selected subfile option indicator.</td>
          </tr>
		  <tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              SetSubfileResponseIndicator](amfPageClassSetSubfileResponseIndicatorMethod.html)
            </td>
            <td>Sets the value of a selected subfile response indicator.</td>
          </tr>
		<tr>
            <td><img height="15" alt="public property" src="../Images/promethod.bmp" width="15" border="0"  />
              [
              SetSubfileFieldValue](amfPageClassSetSubfileFieldValueMethod.html)
            </td>
            <td>Sets the value of a selected subfile field.</td>
          </tr>
</table>

<!--mine -->

#### Protected Fields
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="30%" /><col width="70%" />
          </colgroup>
          <tr><th>Field</th>
              <th>Description</th>
          </tr>
          <tr>
            <td>![](Images/ProtectedField.bmp)
              [
              Device](amfPageClassDeviceField.html)
            </td>
            <td>Reference to an
            unknown-type device.</td>
          </tr>
          <tr>
            <td>![](Images/ProtectedField.bmp)
              [
              DspF](amfPageClassDspFField.html)
            </td>
            <td>Reference to an
            unknown-type display file.</td>
          </tr>
          <tr>
            <td>![](Images/ProtectedField.bmp)
              [
              OutOfSequence](amfPageClassOutOfSequenceField.html)
            </td>
            <td>A boolean value indicating
            the request from the browser is out of sequence ( **True** ).</td>
          </tr>
</table>

#### See Also
<dl>
      <dd>[Page Class](amfPageClass.html)</dd>
      <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd></dl>

