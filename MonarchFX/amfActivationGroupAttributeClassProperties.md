---
title: ActivationGroupAttribute Properties

Id: amfActivationGroupAttributeClassProperties
TocParent: amfActivationGroupAttributeClass
TocOrder: 20

keywords: ActivationGroupAttribute class, properties
keywords: properties [ASNA.Monarch], ActivationGroupAttribute class

---

[ ActivationGroupAttribute Overview](amfActivationGroupAttributeClass.html) 
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
          <tr valign="top">
            <td>              <img class="hcp4" style="WIDTH: 16px; HEIGHT: 16px" height="16" alt="public property" src="Images/property.bmp" width="16" border="0" />
              [
              GroupName](amfActivationGroupAttributeClassGroupNameProperty.html)
            </td>
            <td

>Gets a string value
            containing the name of the activation
            group to use for the program.</td>
          </tr>
          <tr>
            <td>              ![](Images/property.bmp)
              [
              IsCaller](amfActivationGroupAttributeClassIsCallerProperty.html)
            </td>
            <td>Gets a boolean value
            indicating whether the program will be allocated in the
            same activation group as the program calling this
            program. The default is 
 **False** .</td>
          </tr>
          <tr>
            <td>              ![](Images/property.bmp)
              [
              IsDefault](amfActivationGroupAttributeClassIsDefaultProperty.html)
            </td>
            <td>Gets a boolean value
            indicating whether the program falls into the *Default
            activation group.  Those without an
            ActivationGroup attribute are allocated to this
            group. The default is 
 **True** .</td>
          </tr>
          <tr>
            <td>              ![](Images/property.bmp)
              [
              IsNew](amfActivationGroupAttributeClassIsNewProperty.html)
            </td>
            <td

>Gets a boolean value
            indicating whether the program is to be run in a new
            activation group. The default is 
 **False** .</td>
          </tr>
</table>

#### See Also
[ ActivationGroupAttribute Class](amfActivationGroupAttributeClass.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
