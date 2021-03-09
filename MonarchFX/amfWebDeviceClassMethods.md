---
title: WebDevice Class Methods

Id: amfWebDeviceClassMethods
TocParent: amfWebDeviceClass
TocOrder: 20

keywords: WebDevice class, methods
keywords: methods [ASNA.Monarch], WebDevice class

---

[WebDevice Class Overview](amfWebDeviceClass.html) 
<!--mine -->

#### Public Methods
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Method</th>
            <th>Description</th>
          </tr>
          <tr>
            <td>              <img  id="IMG2" height="16" alt="public property" src="../Images/Methods.bmp" width="16" border="0" x-maintain-ratio="TRUE" />
              [Attach](amfWebDeviceClassAttachMethods.html)
            </td>
            <td>Overloaded. Attaches a

 **WebDisplayFile**  to the 
 **WebDevice**  and optionally attaches a shared
            file.</td>
          </tr>
          <tr>
            <td>              <img  id="Img1" height="16" alt="public property" src="../Images/Methods.bmp" width="16" border="0" x-maintain-ratio="TRUE" />
              [Detach](amfWebDeviceClassDetachMethods.html)
            </td>
            <td>Overloaded. Detaches a
            shared file or 
 **WebDisplayFile** (previously attached)
            from the 
 **WebDevice** .</td>
          </tr>
          <tr>
            <td>              <img  id="Img3" height="16" alt="public property" src="../Images/Methods.bmp" width="16" border="0" x-maintain-ratio="TRUE" />
              [Dispose](amfWebDeviceClassDisposeMethod.html)
            </td>
            <td

>Releases the resources of
            the 
 **WebDevice** .</td>
          </tr>
          <tr>
            <td>              <img  id="Img8" height="16" alt="public property" src="../Images/Methods.bmp" width="16" border="0" x-maintain-ratio="TRUE" /> 
            [
            GetRecordIndex](amfWebDeviceClassGetRecordIndexMethod.html)</td>
            <td>Gets an integer
            containing the index for the record
            format specified.</td>
          </tr>
          <tr>
            <td>              <img  id="Img8" height="16" alt="public property" src="../Images/Methods.bmp" width="16" border="0" x-maintain-ratio="TRUE" /> 
            [
            GetRecordIndicators](amfWebDeviceClassGetRecordIndicatorsMethod.html)</td>
            <td>pending Gets an array
            of boolean values representing the evaluation (true or
            false) for each of the indicators of the record
            format specified.</td>
          </tr>
          <tr>
            <td>              <img  id="Img4" height="16" alt="public property" src="../Images/Methods.bmp" width="16" border="0" x-maintain-ratio="TRUE" />
              [
              GetSharedFile](amfWebDeviceClassGetSharedFileMethod.html)
            </td>
            <td>Returns an instance of the 
 **WebDisplayFile**  object for the file name
            specified.</td>
          </tr>
          <tr>
            <td>              <img  id="Img6" height="16" alt="public property" src="../Images/Methods.bmp" width="16" border="0" x-maintain-ratio="TRUE" />
              [
              GetThreadDevice](amfWebDeviceClassGetThreadDeviceMethod.html)
            </td>
            <td

>Returns an instance of a 
 **WebDevice**  thread object.</td>
          </tr>
          <tr>
            <td>              <img  id="Img7" height="16" alt="public property" src="../Images/Methods.bmp" width="16" border="0" x-maintain-ratio="TRUE" />
              [Read](amfWebDeviceClassReadMethod2.html)
            </td>
            <td

>Reads the display file for
            the 
 **WebDevice** .</td>
          </tr>
          <tr>
            <td>              <img  id="Img8" height="16" alt="public property" src="../Images/Methods.bmp" width="16" border="0" x-maintain-ratio="TRUE" /> 
            [
            SetRecordIndex](amfWebDeviceClassSetRecordIndexMethod.html)</td>
            <td

>Sets the
            index for the format name specified.</td>
          </tr>
          <tr>
            <td

 height="23">
              <img  id="Img8" height="16" alt="public property" src="../Images/Methods.bmp" width="16" border="0" x-maintain-ratio="TRUE" /> 
            [
            SetRecordIndicators](amfWebDeviceClassSetRecordIndicatorsMethod.html)</td>
            <td

 height="23">Sets an
            array of boolean values representing the evaluation
            (true or false) for each of the indicators for the
            record format specified.</td>
          </tr>
          <tr>
            <td>              <img  id="Img8" height="16" alt="public property" src="../Images/Methods.bmp" width="16" border="0" x-maintain-ratio="TRUE" />
              [
              SetRecordState](amfWebDeviceClassSetRecordStateMethod.html)
            </td>
            <td

>Sets the index and an
            array of boolean values representing the evaluation
            (true or false) for each of the indicators for the
            record format specified.</td>
          </tr>
          <tr>
            <td>              <img  id="Img9" height="16" alt="public property" src="../Images/Methods.bmp" width="16" border="0" x-maintain-ratio="TRUE" />
              [
              SignalDataReadyForProgram](amfWebDeviceClassSignalDataReadyForProgramMethod.html)
            </td>
            <td

>Signals the 
 **WebDevice**  object thread the device is ready for
            data from a program event.</td>
          </tr>
          <tr>
            <td>              <img  id="Img10" height="16" alt="public property" src="../Images/Methods.bmp" width="16" border="0" x-maintain-ratio="TRUE" />
              [
              SignalDataReadyForUser](amfWebDeviceClassSignalDataReadyForUserMethod.html)
            </td>
            <td

>Signals the 
 **WebDevice**  object thread the device is ready for
            data from a user event.</td>
          </tr>
          <tr>
            <td>              <img  id="Img11" height="16" alt="public property" src="../Images/Methods.bmp" width="16" border="0" x-maintain-ratio="TRUE" />
              [
              WaitForDataForProgram](amfWebDeviceClassWaitForDataForProgramMethod.html)
            </td>
            <td

>Signals the 
 **WebDevice**  object thread the device is to wait for
            data from a program event.</td>
          </tr>
          <tr>
            <td>              <img  id="Img12" height="16" alt="public property" src="../Images/Methods.bmp" width="16" border="0" x-maintain-ratio="TRUE" />
              [
              WaitForDataForUser](amfWebDeviceClassWaitForDataForUserMethod.html)
            </td>
            <td

>Signals the 
 **WebDevice**  object thread the device is to wait for
            data from a user event.</td>
          </tr>
</table>

#### See Also
[ASNA.Monarch Namespace](amfMonarchNamespace.html) <br /> [WebDevice Class](amfWebDeviceClass.html) 
