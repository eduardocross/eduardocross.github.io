---
title: Job Class Fields

Id: amfJobFields
TocParent: amfJobClass
TocOrder: 40

keywords: Job class, fields
keywords: fields [ASNA.Monarch], Job class

---

[Job Class Overview](amfJobClass.html) 
<!-- start public properties table -->	

#### Public Fields
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Field</th>
            <th>Description</th>
          </tr>
<!-- end copy BUT put in extra div and end of table -->
          <tr valign="top">
            <td><img id="Img8" style="WIDTH: 16px; HEIGHT: 16px" alt="public fields" src="Images/Field.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            ExternalQueue](amfJobClassExternalQueueField.html)
            </td>
            <td>A reference to an instance of
          an 
          [
          ASNA.Monarch.MessageQueue](amfMessageQueueClass.html) object for an external
          message queue for this job.</td>
          </tr>
          <tr>
            <td><img id="Img1" style="WIDTH: 16px; HEIGHT: 16px" alt="public fields" src="Images/Field.bmp" border="0" x-maintain-ratio="TRUE" />
              [LDC](amfJobClassLDCField.html)
            </td>
            <td>A reference to an instance of
          a 
          [
          LocalDataCollection](amfLocalDataCollectionClass.html) object containing a collection of
          name/value pairs.</td>
          </tr>
          <tr>
            <td><img id="Img4" style="WIDTH: 16px; HEIGHT: 16px" alt="public fields" src="Images/Field.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            PsdsJobName](amfJobClassPsdsJobNameField.html)
            </td>
            <td>The 10-character job name
          field in the program status data structure.</td>
          </tr>
          <tr>
            <td><img id="Img22" style="WIDTH: 16px; HEIGHT: 16px" alt="public fields" src="Images/Field.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            PsdsJobNumber](amfJobClassPsdsJobNumberField.html)
            </td>
            <td>The 6-digit job number field
          in the program status data structure.</td>
          </tr>
          <tr>
            <td><img id="Img23" style="WIDTH: 16px; HEIGHT: 16px" alt="public fields" src="Images/Field.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            PsdsJobUser](amfJobClassPsdsJobUserField.html)
            </td>
            <td>The 10-character user name
          field in the program status data structure.</td>
          </tr>
</table>

<!-- start public properties table -->	

#### Protected Fields
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Field</th>
            <th>Description</th>
          </tr>
<!-- end copy BUT put in extra div and end of table -->
          <tr>
            <td><img id="Img2" style="WIDTH: 16px; HEIGHT: 16px" alt="fields" src="Images/
ProtectedField.bmp" width="15" border="0" x-maintain-ratio="TRUE" />
              [
            FileOverrideTable](amfJobClassFileOverrideTableField.html)
            </td>
            <td>A reference to an
          instance of a System.Collection.Hashtable representing
          the file overrides for the job.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="protected method" src="Images/
ProtectedField.bmp" width="15" border="0" x-maintain-ratio="TRUE" /> Lda</td>
            <td>Deprecated.</td>
          </tr>
          <tr>
            <td><img id="Img25" style="WIDTH: 16px; HEIGHT: 16px" alt="fields" src="Images/
ProtectedField.bmp" width="15" border="0" x-maintain-ratio="TRUE" />
              [
            messageFileFolder](amfJobClassmessageFileFolderField.html)
            </td>
            <td>A reference to the message
          file folder object containing the message file for this
          job.</td>
          </tr>
</table>

#### See Also
<dl>
        <dd>[Job Class](amfJobClass.html)
        </dd><dd>
        [Job Class
        Members](amfJobMembers.html)</dd>
       <dd>[MessageQueue
    Class](amfMessageQueueClass.html)</dd>
    <dd>[
    LocalDataCollection Class](amfLocalDataCollectionClass.html)</dd>
        <dd>[ASNA.Monarch
        Namespace](amfMonarchNamespace.html)</dd>
</dl>

