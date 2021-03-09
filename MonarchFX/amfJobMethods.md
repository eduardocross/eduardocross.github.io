---
title: Job Class Methods

Id: amfJobMethods
TocParent: amfJobClass
TocOrder: 20

keywords: Job class, methods
keywords: methods [ASNA.Monarch], Job class

---

[Job Class Overview](amfJobClass.html) 
<!-- start public properties table -->	

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
          the database, print, or workstation file overrides
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
            <td><img id="Img5" style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="../Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [EndPrograms](amfJobClassEndProgramsMethod.html)
            </td>
            <td>De-activates any program that
          is still active.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="protected method" src="../Images/Methods.bmp" width="15" border="0" x-maintain-ratio="TRUE" /> GetLdaField</td>
            <td>Deprecated. Use the Visual
          RPG "IN" command.</td>
          </tr>
          <tr>
            <td><img id="Img10" style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="../Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            GetSwitch](amfJobClassGetSwitchMethod.html)
            </td>
            <td>Returns a value indicating
          the 'on'/'off' status of a specific job attribute
          switch.</td>
          </tr>
          <tr>
            <td><img id="Img11" style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="../Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [GetSwitches](amfJobClassGetSwitchesMethod.html)
            </td>
            <td>Returns a string of 8
          characters with values '0' and '1', each character
          represents one of the job attributes switches.</td>
          </tr>
          <tr>
            <td><img id="Img12" style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="../Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
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
            <td><img id="Img18" style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="../Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            SetSwitch](amfJobClassSetSwitchMethod.html)
            </td>
            <td>Set a value indicating the
          'on'/'off' status of a specific job attribute
          switch.</td>
          </tr>
          <tr>
            <td><img id="Img19" style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="../Images/Methods.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            ShutDown](amfJobClassShutDownMethod.html)
            </td>
            <td>Terminates the Job program
          when an abnormal condition occurs.</td>
          </tr>
</table>

<!-- start public properties table -->	

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
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="../Images/promethod.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            getADO_Connection](amfJobClassgetADO_ConnectionMethod.html)
            </td>
            <td>Returns a new instance of
          a 
          [getDatabase](http://msdn2.microsoft.com/en-us/library/system.data.common.dbconnection.aspx">
          System.Data.Common.DbConnection</a> object representing an
          ADO connection to a database.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="../Images/promethod.bmp" border="0" x-maintain-ratio="TRUE" />
              <a href="amfJobClassgetDatabaseMethod.html)
            </td>
            <td>Returns a new instance of
          ASNA.VisualRPG.Runtime.Database connection object for the
          job.</td>
          </tr>
          <tr>
            <td><img style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="../Images/promethod.bmp" border="0" x-maintain-ratio="TRUE" />
              [
            getPrinterDB](amfJobClassgetPrinterDBMethod.html)
            </td>
            <td>Returns a new instance of
          ASNA.VisualRPG.Runtime.Database connection object for
          printer used by the job.</td>
          </tr>
</table>

#### See Also
<dl>
        <dd>[Job Class](amfJobClass.html)
        </dd><dd>
        [Job Class
        Members](amfJobMembers.html)</dd>
       <dd>[Program Class](amfProgramClass.html)</dd>
        <dd>[ASNA.Monarch
        Namespace](amfMonarchNamespace.html)</dd>
</dl>   

