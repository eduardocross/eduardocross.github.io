---
title: Dependent Class

Id: dcsDependentClass
TocParent: dcsASNADataGateClientClasses
TocOrder: 7

keywords: classes [DCS 16.0 Dependent class
keywords: Dependent class
keywords: Dependent class, about Dependent class
keywords: dependent objects, about Dependent class

---

<span> **Dependent** </span> names a database object, its type, and characterizes its dependent relationship to another database object. 
<pre class="prettyprint">
        <span class="lang">[Prototype in C#]</span>
 **<br /> public class DependentClass** 
      </pre>

Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
Remarks

Instances of **Dependent** are returned by the **Dependents** property of [IAdgObject](dcsIAdgObjectClass.html). These instances enumerate logical database objects that are defined in terms of a relationship to the base physical database object, represented by **IAdgObject** . Database providers may place constraints on database objects that have dependents, such as not allowing the object's deletion.

The [AdgObjectType](dcsDependentClassAdgObjectTypeProperty.html) property reveals the dependent object's type, defined by the [ AdgObjectTypes](dcsAdgObjectTypesEnumeration.html) enumeration. Current database providers only list database files and members as dependents. The [ PathName](dcsDependentClassPathNameProperty.html) property is the full path of the dependent object.

The [DependentType](dcsDependentClassDependentTypeProperty.html) property determines the relationship between this dependent and its base (see [ DependentTypes](dcsDependentTypesEnumeration.html) enumeration). 
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [Dependent Class Members](dcsDependentMembers.html)
      <br />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [AdgObjectTypes Enumeration](dcsAdgObjectTypesEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

