---
title: IAdgObject.Dependents Property

Id: dcsIAdgObjectClassDependentsProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 7

keywords: Dependents property
keywords: IAdgObject.Dependents property
keywords: dependent objects, return an array for a base object
keywords: base objects, return dependent object(s) array
keywords: how to, return dependent object(s) array for a base object

---

**Dependents** is an array of [Dependent](dcsDependentClass.html) objects denoting the set of objects that depend upon the database object represented by **IAdgObject** .
<pre>        <span class="lang">[C#]</span>
 **Public [Dependent](dcsDependentClass.html)[] Dependents { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property Dependents As [Dependent](dcsDependentClass.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Dependents Access(*Public) Type([Dependent](dcsDependentClass.html))
   BegGet** 
      </pre>

Property Value <p> [Dependent](dcsDependentClass.html) array. Read-only. The **Length** of the array is equal to the number of dependent objects. 
Exceptions

None.
Remarks

Physical database files and members may have "dependent" objects. That is, the other database objects may depend on an object as a base object, as in a logical file definition. The **Dependents** property provides a list of all database objects that refer to the database object represented by **IAdgObject** as a base, in the form of an array of **Dependent** objects.

If the database object has no dependents, **Dependents** returns an empty array.

Depending upon the database provider, **IAdgObject** queries for some properties, such as **Dependents** , only once in the lifetime of the **IAdgObject** instance. If the list of dependents for the database object changes after the query, the change will not be reflected in the **Dependents** property value of the **IAdgObject** . Also, modifying the array returned by **Dependents** changes the **IAdgObject** property value, but does not change the list of dependents of the database object.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [Dependent 
					Class](dcsDependentClass.html)
      <br />
      [ASNA.DataGate.Client 
					Namespace](dcsDataGateClientNamespace.html)

