---
title: Class Library

Id: amfClassLibraryMain
TocParent: amfReferenceMain
TocOrder: 20

keywords: class libraries, ASNA.Monarch

---

ASNA.Monarch Framework contains two assemblies &#8211; **ASNA.Monarch.WebDspF** and **ASNA.VisualRPG.Runtime** . ASNA.Monarch.WebDspF supports the Web Server Controls to facilitate the implementation of the semantics of DDS elements and support of Non-ASPX Display files ASNA.VisualRPG.Runtime supports the language capabilities of migrated applications.

#### Namespaces
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">          <colgroup>
            <col width="25%" />
            <col width="25%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <th>Namespace</th>
            <th>Assembly</th>
            <th>Description</th>
          </tr>
          <tr>
            <td>
              [
              ASNA.Monarch](amfMonarchNamespace.html)
            </td>
            <td>ASNA.VisualRPG.Runtime</td>
            <td>This namespace provides the
            primary support for migrated applications.</td>
          </tr>
          <tr>
            <td>[ASNA.Monarch](amfWebDspFASNAMonarchNamespace.html)
            </td>
            <td>ASNA.Monarch.WebDspF</td>
            <td>The namespace supports
            Non-ASPX Display files.</td>
          </tr>
          <tr>
            <td>
              [
              ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
            </td>
            <td>ASNA.Monarch.WebDspF</td>
            <td>This
            namespace contains the classes that make up
            the Web Server Controls in support of DDS
            elements.</td>
          </tr>
</table>

#### Exceptions
The class library documentation lists the exceptions that each member throws along with a description of the condition under which it is thrown.

#### Thread Safety
All public static members (methods, properties, fields, and events) within ASNA.Monarch support concurrent access within a multi-threaded environment. Therefore, any ASNA Monarch static member can be simultaneously invoked from two threads without encountering race conditions, deadlocks, or crashes.

For all classes and structures in ASNA.Monarch, check the Thread Safety section in the Language Reference documentation to determine whether it is thread safe. If you want to use a class that is not thread-safe in a multi-threaded environment, you must wrap an instance of the class with code that supplies the necessary synchronization constructs.

#### See Also
<dl>
      <dd>[ASNA.Monarch Language
        Reference](amfReferenceMain.html)</dd>
        <dd>[Monarch
        Framework Concepts](amfASNA.narchFrameworkConceptsMain.html)</dd>
</dl>

