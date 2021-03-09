---
title: Job Class Members

Id: amfJobMembers
TocParent: amfJobClass
TocOrder: 5

keywords: Job class, all members
keywords: members [ASNA.Monarch], Job class

---

[Job Class Overview](amfJobClass.html) 
<!-- start constructor table -->	

#### Constructor
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Constructor</th>
            <th>Description</th>
          </tr>
<!-- end copy BUT put in extra div and end of table -->          <tr valign="top">
            <td><img id="IMG1" style="WIDTH: 16px; HEIGHT: 16px" alt="constructor" src="../Images/Constructor.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            Job](amfJobClassJobConstructors.html)
            </td>
            <td>Creates a new instance of a
          Job object.</td>
          </tr>
</table>

<!-- start constructor table -->	

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
<!-- end copy BUT put in extra div and end of table -->
          <tr>
            <td><img id="Img3" style="WIDTH: 16px; HEIGHT: 16px" alt="method" src="../Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            DeleteOverride](amfJobClassDeleteOverrideMethods.html)
            </td>
            <td>Overloaded. Removes
          theÂ database, print, or workstation file overrides
          previously applied to the job.</td>
          </tr>
          <tr>
            <td><img id="Img21" style="WIDTH: 16px; HEIGHT: 16px" alt="method" src="../Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            Dispose](amfJobClassDisposeMethod.html)
            </td>
            <td>Releases managed and
          unmanaged or just unmanaged resources used by the
          Job.</td>
          </tr>
          <tr>
            <td><img id="Img5" style="WIDTH: 16px; HEIGHT: 16px" alt="method" src="../Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [EndPrograms](amfJobClassEndProgramsMethod.html)
            </td>
            <td>De-activates any program that
          is still active.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="protected method" src="../Images/Methods.bmp" width="15" border="0" x-maintain-ratio="TRUE" />GetLdaField</td>
            <td>Deprecated. Use the Visual
          RPG "IN" command.</td>
          </tr>
          <tr>
            <td><img id="Img10" style="WIDTH: 16px; HEIGHT: 16px" alt="public method" src="../Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            GetSwitch](amfJobClassGetSwitchMethod.html)
            </td>
            <td>Returns a value indicating
          the 'on'/'off' status of a specific job attribute
          switch.</td>
          </tr>
          <tr>
            <td><img id="Img11" style="WIDTH: 16px; HEIGHT: 16px" alt="method" src="../Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [GetSwitches](amfJobClassGetSwitchesMethod.html)
            </td>
            <td>Returns a string of 8
          characters with values '0' and '1', each character
          represents one of the job attributes switches.</td>
          </tr>
          <tr>
            <td><img id="Img12" style="WIDTH: 16px; HEIGHT: 16px" alt="method" src="../Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            OverrideFile](amfJobClassOverrideFileMethods.html)
            </td>
            <td>Overloaded. Provides Job file
          override options.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="protected method" src="../Images/Methods.bmp" width="15" border="0" x-maintain-ratio="TRUE" /> SetLdaField</td>
            <td>Deprecated. Use the Visual
          RPG "OUT" command.</td>
          </tr>
           <tr>
            <td><img id="Img18" style="WIDTH: 16px; HEIGHT: 16px" alt="method" src="../Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            Request](amfJobClassRequestMethod.html)
            </td>
            <td>Set a value in seconds to wait for programs to shut down elegantly when a session ends.</td>
          </tr>

          <tr>
            <td><img id="Img18" style="WIDTH: 16px; HEIGHT: 16px" alt="method" src="../Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            SetSwitch](amfJobClassSetSwitchMethod.html)
            </td>
            <td>Set a value indicating the
          'on'/'off' status of a specific job attribute
          switch.</td>
          </tr>
          <tr>
            <td><img id="Img19" style="WIDTH: 16px; HEIGHT: 16px" alt="method" src="../Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            ShutDown](amfJobClassShutDownMethod.html)
            </td>
            <td>Terminates the Job program
          when an abnormal condition occurs.</td>
          </tr>
</table>

<!-- start constructor table -->	

#### Protected Methods
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Method</th>
            <th>Description</th>
          </tr>
<!-- end copy BUT put in extra div and end of table -->
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="protected method" src="../Images/promethod.bmp
" border="0" x-maintain-ratio="TRUE" />
              [
            getADO_Connection](amfJobClassgetADO_ConnectionMethod.html)
            </td>
            <td>Returns a new instance of
          aÂ 
          [getDatabase](http://msdn2.microsoft.com/en-us/library/system.data.common.dbconnection.aspx">
          System.Data.Common.DbConnection</a> object representing an
          ADO connection to a database.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="protected method" src="../Images/promethod.bmp
" border="0" x-maintain-ratio="TRUE" />
              <a href="amfJobClassgetDatabaseMethod.html)
            </td>
            <td>Returns a new instance of
          ASNA.VisualRPG.Runtime.Database connection object for the
          job.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="../Images/promethod.bmp
" border="0" x-maintain-ratio="TRUE" />
              [
            getPrinterDB](amfJobClassgetPrinterDBMethod.html)
            </td>
            <td>Returns a new instance of
          ASNA.VisualRPG.Runtime.Database connection object for
          printer used by the job.</td>
          </tr>
</table>

<!-- start public properties table -->	

#### Public Properties
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Property</th>
            <th>Description</th>
          </tr>
<!-- end copy BUT put in extra div and end of table -->
          <tr>
            <td><img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" />
              [
            ADO_Connection](amfJobClassADO_ConnectionProperty.html)
            </td>
            <td>Gets the 
          [CurrentJob](http://msdn2.microsoft.com/en-us/library/system.data.common.dbconnection.aspx">
          System.Data.Common.DbConnection</a> object representing an
          ADO connection to a database.</td>
          </tr>
          <tr valign="top">
            <td><img height="16" alt="public property" src="../Images/property.bmp" border="0" />
              <a href="amfJobClassCurrentJobProperty.html)
            </td>
            <td>Gets the Job object
          corresponding to this Job.</td>
          </tr>
          <tr>
            <td><img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" />
              [
            Database](amfJobClassDatabaseProperty.html)
            </td>
            <td>Gets the
          ASNA.VisualRPG.Runtime.Database connection object
          corresponding to this Job.</td>
          </tr>
          <tr>
            <td><img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" />
              [
            MesssageFileFolder](amfJobClassMessageFileFolderProperty.html)
            </td>
            <td>Gets or sets the name of the
          folder containing the message file for this job.</td>
          </tr>
          <tr>
            <td><img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" />
              [PrinterDB](amfJobClassPrinterDBProperty.html)
            </td>
            <td>Gets the
          ASNA.VisualRPG.Runtime.Database connection object for the
          printer corresponding to this Job.</td>
          </tr>
          <tr>
            <td><img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" />
              [
            StartupMoment](amfJobClassStartupMomentProperty.html)
            </td>
            <td>Gets the System.DateTime when
          the Job was started.</td>
          </tr>
</table>

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
            <td style="height: 29px"><img id="Img8" style="WIDTH: 16px; HEIGHT: 16px" alt="public fields" src="../Images/Field.bmp
" border="0" x-maintain-ratio="TRUE" />
              [
            ExternalQueue](amfJobClassExternalQueueField.html)
            </td>
            <td style="height: 29px">A reference to an instance of
          an 
          [
          ASNA.Monarch.MessageQueue](amfMessageQueueClass.html)Â object for an external
          message queue for this job.</td>
          </tr>
          <tr>
            <td><img id="Img4" style="WIDTH: 16px; HEIGHT: 16px" alt="public fields" src="../Images/Field.bmp
" border="0" x-maintain-ratio="TRUE" />
              [LDC](amfJobClassLDCField.html)
            </td>
            <td>A reference to an instance of
          a 
          [
          LocalDataCollection](amfLocalDataCollectionClass.html) object containing a collection of
          name/value pairs.</td>
          </tr>
          <tr>
            <td><img id="Img6" style="WIDTH: 16px; HEIGHT: 16px" alt="public fields" src="../Images/Field.bmp
" border="0" x-maintain-ratio="TRUE" />
              [
            PsdsJobName](amfJobClassPsdsJobNameField.html)
            </td>
            <td>The 10-character job name
          field in the program status data structure.</td>
          </tr>
          <tr>
            <td><img id="Img22" style="WIDTH: 16px; HEIGHT: 16px" alt="public fields" src="../Images/Field.bmp
" border="0" x-maintain-ratio="TRUE" />
              [
            PsdsJobNumber](amfJobClassPsdsJobNumberField.html)
            </td>
            <td>The 6-digit job number field
          in the program status data structure.</td>
          </tr>
          <tr>
            <td><img id="Img23" style="WIDTH: 16px; HEIGHT: 16px" alt="public fields" src="../Images/Field.bmp
" border="0" x-maintain-ratio="TRUE" />
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
            <td><img id="Img7" style="WIDTH: 16px; HEIGHT: 16px" alt="fields" src="../Images/ProtectedField.bmp" width="15" border="0" x-maintain-ratio="TRUE" />
              [
            FileOverrideTable](amfJobClassFileOverrideTableField.html)
            </td>
            <td>A referenceÂ to an
          instance of a System.Collection.Hashtable representing
          the file overrides for the job.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="protected method" src="../Images/ProtectedField.bmp" width="15" border="0" x-maintain-ratio="TRUE" />Lda</td>
            <td>Deprecated.</td>
          </tr>
          <tr>
            <td><img id="Img25" style="WIDTH: 16px; HEIGHT: 16px" alt="fields" src="../Images/ProtectedField.bmp" width="15" border="0" x-maintain-ratio="TRUE" />
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
 <dd>[
    LocalDataCollection Class](amfLocalDataCollectionClass.html)</dd>
    <dd>[MessageQueue
    Class](amfMessageQueueClass.html)</dd>
       <dd>[Program Class](amfProgramClass.html)</dd>
        <dd>[ASNA.Monarch
        Namespace](amfMonarchNamespace.html)</dd>
</dl>

