---
title: DdsDataField Class

Id: amfDdsDataFieldClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 180

keywords: MessageFileException
keywords: MessageIDException
keywords: DdsDataField class, about DdsDataField class
keywords: classes [ASNA.Monarch.WebDspF], DdsDataField class

---

**DdsDataField** is a derived class that further defines properties and methods common to display file fields. In addition, **DdsDataField** is also a base class for the derived classes **DdsCharField** , **DdsDecField** , **DdsBaseDate** , **DdsTimeField** , and **DdsTimestampField** .

For a list of all members of this type, see [ DdsDataField Members](amfDdsDataFieldClassMembers.html).

#### Applicable Products:
**Monarch, Wings, Mobile RPG** 
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)         
    [ASNA.Monarch.WebDspF.DdsField](amfDdsFieldClass.html)
 **ASNA.Monarch.WebDspF.DdsDataField** 
            [Derived Classes](amfDdsDataFieldDerivedClasses.html)</pre>

#### Syntax
<pre class="prettyprint"> **Public MustInherit class DdsDataField : Inherits ASNA.Monarch.WebDspF.DdsField** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
This class is intended for use as a base class only and instances of this class cannot be created directly; they can only be created as base class instances of the derived classes.

#### Exceptions
The following exceptions may be encountered when the control field is rendered.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="50%" /><col width="50%" />
          </colgroup>
          <tr><th>Value</th><th>Condition</th>
          </tr>
          <tr><td>MessageFileException</td><td>The Message file used by the control could not be found.</td>
          </tr>
          <tr><td>MessageIDException</td><td>A Message with the requested ID could not be found.</td>
          </tr>
</table>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ Derived Classes](amfDdsDataFieldDerivedClasses.html) 
