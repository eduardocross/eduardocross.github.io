---
title: DdsConstant.Text Property

Id: amfDdsConstantClassTextProperty
TocParent: amfDdsConstantClassPropertiesMain
TocOrder: 40

keywords: Text property
keywords: DdsConstant.Text property
keywords: DATE
keywords: _Star_DATE field text
keywords: TIME
keywords: _Star_TIME field text
keywords: USER
keywords: _Star_USER field text
keywords: SYSNAME
keywords: _Star_SYSNAME field text
keywords: Web server controls [ASNA.Monarch], setting field text
keywords: how to, set field control text
keywords: how to, get field control text
keywords: display files, setting field control text
keywords: display files, getting field control text
keywords: web controls, setting field control text
keywords: web controls, getting field control text
keywords: field controls, text
keywords: field controls, _Star_DATE
keywords: field controls, _Star_TIME
keywords: field controls, _Star_USER
keywords: field controls, _Star_SYSNAME

---

Gets or sets a string containing either a constant to display, or the special value *DATE, *TIME, *USER or *SYSNAME.

#### Syntax
<pre class="prettyprint"> **BegProp Text Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A constant or the system's special values *DATE, *TIME, *USER or *SYSNAME.

#### Remarks
The default of **Constant** will display. You can change the text Constant to a constant value, such as Name:, or Address:, etc., or enter in one of the following special values.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="20%" /><col width="80%" />

          </colgroup>
          <tr><th>Special Value</th><th>Description</th>
          </tr>
          <tr><td>*DATE</td><td>When you enter *DATE in theText property, the contents of the field will displaythe current system's **date** , such as **12/27/2007** .</td>
          </tr>
          <tr><td>*TIME</td><td>When you enter *TIME in theText property, the contents of the field will displaythe current system's **Time** , such as **4:00.00 PM.** </td>
          </tr>
          <tr><td>*USER</td><td>When you enter *USER in theText property, the contents of the field will displaythe name of the current system's **User,**  such as **Julie.** </td>
          </tr>
          <tr><td>*SYSNAME</td><td>When you enter *SYSNAME inthe Text property, the contents of the field willdisplay the current system's **Name,**  such as **Juliexp.** </td>
          </tr>
</table>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsConstant Class](amfDdsConstantClass.html) <br /> [ DdsConstant Class Members](amfDdsConstantClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
