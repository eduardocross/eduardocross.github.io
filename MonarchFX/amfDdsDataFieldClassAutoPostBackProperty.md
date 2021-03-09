---
title: DdsDataField.AutoPostBack Property

Id: amfDdsDataFieldClassAutoPostBackProperty
TocParent: amfDdsDataFieldClassProperties
TocOrder: 20

keywords: AutoPostBack property
keywords: DdsDataField.AutoPostBack property
keywords: web controls, generating AutoPostBack
keywords: how to, generate AutoPostBack
keywords: display files, generating AutoPostBack
keywords: Web server controls [ASNA.Monarch], AutoPostBack
keywords: field controls, AutoPostBack

---

Gets or sets a boolean value that if true, causes the control to generate a post back to the server when the field is output-only. 

#### Syntax
<pre class="prettyprint">
 **BegProp AutoPostBack Access(*Public) Type(*Boolean) Modifier(*MustOverride)
   BegGet;  BegSet** 
            </pre>

#### Property Values
Boolean. True will cause the control to generate a post back to the server when the field is output-only; otherwise false will generate no post back.

#### Remarks
<a shape="rect" href="amfDdsCharFieldClass.htm"> DdsCharField</a> and <a shape="rect" href="amfDdsDecFieldClass.htm"> DdsDecField</a> are the only derived classes that override this property.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html) 

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<a shape="rect" href="amfDdsDataFieldClass.htm"> DdsDataField Class</a> <br clear="none" /> <a shape="rect" href="amfDdsDataFieldClassMembers.htm"> DdsDataField Class Members</a> <br clear="none" /> <a shape="rect" href="amfDdsDataFieldDerivedClasses.htm"> Derived Classes</a> <br clear="none" /> <a shape="rect" href="amfWebDspFNamespace.htm"> ASNA.Monarch.WebDspF Namespace</a> 
