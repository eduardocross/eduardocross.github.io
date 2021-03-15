---
title: Job Class Properties

Id: amfJobProperties
TocParent: amfJobClass
TocOrder: 30

keywords: Job class, properties
keywords: properties [ASNA.Monarch], Job class

---

[Job Class Overview](amfJobClass.html) 
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
            <td><img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" />
              [
              ADO_Connection](amfJobClassADO_ConnectionProperty.html)
            </td>
            <td>Gets the 
            [
              CurrentJob](http://msdn2.microsoft.com/en-us/library/system.data.common.dbconnection.aspx">
            System.Data.Common.DbConnection</a> object representing
            an ADO connection to a database.</td>
          </tr>
          <tr valign="top">
            <td><img height="16" alt="public property" src="Images/property.bmp" border="0" />
              <a href="amfJobClassCurrentJobProperty.html)
            </td>
            <td>Gets the Job object
            corresponding to this Job.</td>
          </tr>
          <tr>
            <td><img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" />
              [Database](amfJobClassDatabaseProperty.html)
            </td>
            <td>Gets the
            ASNA.VisualRPG.Runtime.Database connection object
            corresponding to this Job.</td>
          </tr>
          <tr>
            <td><img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" />
              [
              MesssageFileFolder](amfJobClassMessageFileFolderProperty.html)
            </td>
            <td>Gets or sets the name of
            the folder containing the message file for this
            job.</td>
          </tr>
          <tr>
            <td><img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" />
              [PrinterDB](amfJobClassPrinterDBProperty.html)
            </td>
            <td>Gets the
            ASNA.VisualRPG.Runtime.Database connection object for
            the printer corresponding to this Job.</td>
          </tr>
          <tr>
            <td><img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" />
              [
              StartupMoment](amfJobClassStartupMomentProperty.html)
            </td>
            <td>Gets the System.DateTime
            when the Job was started.</td>
          </tr>
</table>

#### See Also
<dl>
        <dd>[Job Class](amfJobClass.html)
        </dd>
                <dd>[ASNA.Monarch
        Namespace](amfMonarchNamespace.html)</dd>
</dl>

