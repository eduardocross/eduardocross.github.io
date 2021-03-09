---
title: Dependent.DependentType Property

Id: dcsDependentClassDependentTypeProperty
TocParent: dcsDependentProperties
TocOrder: 1

keywords: DependentType property
keywords: Dependent.DependentType property
keywords: DependentTypes enumeration, used by
keywords: enumerations [DCS 16.0 DependentTypes, used by
keywords: dependent objects, type of relationship with its' bases
keywords: database relationships, dependent and base objects
keywords: how to, determine dependent objects' relationship with its bases

---

**DependentType** determines the relationship between a dependent database object and its' [ bases](dcsIAdgObjectClassBasesProperty.html). 
<pre class="prettyprint">
        <span class="lang">
          [C#]
        </span>
 **public [DependentTypes](dcsDependentTypesEnumeration.html) DependentType { get; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property DependentType As [DependentTypes](dcsDependentTypesEnumeration.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp DependentType Type([DependentTypes](dcsDependentTypesEnumeration.html)) Access(*Public)
   BegGet** 
      </pre>

Property Value

[DependentTypes](dcsDependentTypesEnumeration.html). Read-only. The relationship between a dependent and its [ bases](dcsIAdgObjectClassBasesProperty.html). 
Remarks

The value of **DependentType** determines what type of dependency is represented by the **Dependent** instance. See **DependentTypes** for details of the possible values of this property.
Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)
      <br />
      [Dependent Class](dcsDependentClass.html)
      <br />
      [DependentTypes Enumeration](dcsDependentTypesEnumeration.html)
      <br />
      [IAdgObject.Bases Property](dcsIAdgObjectClassBasesProperty.html)

