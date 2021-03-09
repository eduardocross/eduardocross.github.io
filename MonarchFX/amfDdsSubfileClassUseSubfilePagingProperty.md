---
title: DdsSubfile.UseSubfilePaging Property

Id: amfDdsSubfileClassUseSubfilePagingProperty
TocParent: amfDdsSubfileClassPropertiesMain
TocOrder: 120

keywords: UseSubfilePaging property
keywords: DdsSubfile.UseSubfilePaging property
keywords: subfiles, using paging
keywords: web controls, using subfile paging
keywords: how to, use subfile paging
keywords: subfile records, using paging
keywords: subfile usage, paging

---

Gets or sets a boolean value indicating if subfile paging is used. The default is False. 

#### Syntax
<pre class="prettyprint"> **BegProp UseSubfilePaging Access(*Public) Type(*Boolean)
   BegGet;  BegSet** </pre>

#### Property Values
Boolean. True indicates that subfile paging is used; otherwise False.

#### Remarks
Setting the property True will cause the subfile to render the number of records specified in the [ DdsSubfileControl](amfddsSubfileControlClass.html). If more records are read than the number specified in [ SubfilePage](amfddsSubfileControlClassSubfilePageProperty.html), pressing PgDn or PgUp will send an AJAX request to the server and update the contents of the subfile appropriately. If making a request and the end of the read records has been reached, a postback will be generated.

To set this property at design-time, click on the right of the **UseSubfilePaging** property and select true or false from the drop-down box.

For more detail see [SubFile Paging](amfSubfilePaging.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsSubfile Class](amfDdsSubfileClass.html) <br /> [ DdsSubfile Class Members](amfDdsSubfileClassMembers.html) <br /> [ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
