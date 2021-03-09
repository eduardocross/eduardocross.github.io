---
title: LocalDataCollection Class

Id: amfLocalDataCollectionClass
TocParent: amfMonarchNamespaceClasses
TocOrder: 80

keywords: LocalDataCollection class, about LocalDataCollection
keywords: classes [ASNA.Monarch], LocalDataCollection class
keywords: ErrorMessage Property Editor, container
keywords: local data collection
keywords: ldc
keywords: LDC

---

The **LocalDataCollection** is a derived class that is a container for a collection of name/value pairs for the job. It inherits the properties and methods of and uses the shown in the hierarchy list.

For a list of all members of this type, see [ LocalDataCollection Members](amfLocalDataCollectionMembers.html).

#### Hierarchy
<pre>[ASNA.Monarch](amfMonarchNamespace.html)
   System.Collections 
   System.Collections.IEnumerable 
   System.Collections.ICollection 
   System.Collections.IDictionaryEnumerator
 **ASNA.Monarch.LocalDataCollection**  </pre>

#### Syntax 
<pre class="prettyprint"> **Public class LocalDataCollection Inherits System.Collections**       </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
**LocalDataCollection** is a general-purpose in-memory table to store named values of any type. Similar to the System i LDA (Local Data Area), with the following advantages:

1. The size of the objects are only limited by the
        available memory (the System i LDA is limited to 2K
        bytes)
2. There is no need to remember the position within the
        Data where the object is stored, (unlike the System i
        LDA, unless it is mapped to a data structure). 
        Using 
        [
        this](amfLocalDataCollectionClassthisProperty.html) property, if the specific name already exists in
        the dictionary, the value is replaced; otherwise, a new
        element is created. In contrast, the 
        [
        Add](amfLocalDataCollectionClassAddMethod.html) method adds a name/value pair but does not modify
        existing elements.
3. The syntax to access the values is much simpler with 
        [
        Job.LDC](amfJobClassLDCField.html)
4. The LocalDataCollection is more flexible, one can
        easily: 
<li>determine how many named objects are stored (
          [Count
          property](amfLocalDataCollectionClassCountProperty.html))
5. query whether a particular name has already been
          stored (
          [
          Contains method](amfLocalDataCollectionClassContainsMethod.html))
6. remove all names values (
          [
          Clear](amfLocalDataCollectionClassClearMethod.html) or 
          [
          RemoveAll](amfLocalDataCollectionClassRemoveAllMethod.html) methods) or a single value (
          [
          Remove](amfLocalDataCollectionClassRemoveMethod.html))
7. access the 
          [
          Values](amfLocalDataCollectionClassValuesProperty.html) or 
          [
          Names](amfLocalDataCollectionClassNamesProperty.html) ICollection

</li>

<!-- start -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td>[ASNA.Monarch](amfMonarchNamespace.html)</td>
          </tr>
          <tr>
            <td>Assembly:</td>
            <td>ASNA.VisualRPG.Runtime.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ASNA.Monarch Namespace](amfMonarchNamespace.html) <br /> [ LocalDataCollection Members](amfLocalDataCollectionMembers.html) 
