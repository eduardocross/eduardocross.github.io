---
title: ILibraryList.EnumerateCurrentUser Method

Id: dcsILibraryListClassEnumerateCurrentUserMethod
TocParent: dcsILibraryListMethods
TocOrder: 2

keywords: EnumerateCurrentUser method
keywords: ILibraryList.EnumerateCurrentUser method
keywords: AdgEnumerator delegate, used by
keywords: delegates [DCS 16.0 AdgEnumerator, used by
keywords: enumerate contents of library list
keywords: how to, enumerate contents of library list
keywords: library lists, enumerate object contents of

---

**EnumerateCurrentUser** enumerates the object contents of the user portion of the library list represented by **ILibraryList** , with the supplied [AdgEnumerator](dcsAdgEnumeratorDelegate.html) delegate.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void EnumerateCurrentUser(_<br />[AdgEnumerator](dcsAdgEnumeratorDelegate.html) enumerator <br />);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function EnumerateCurrentUser(
   ByVal enumerator As [AdgEnumerator](dcsAdgEnumeratorDelegate.html)
) As Void** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr EnumerateCurrentUser Access(*Public) Type(Void)
   DclSrParm enumerator Type([AdgEnumerator](dcsAdgEnumeratorDelegate.html))** 
      </pre>

Parameters

<dl>
        <dt>
 *enumerator* 
        </dt>
        <dd>

[AdgEnumerator](dcsAdgEnumeratorDelegate.html). The delegate **EnumerateCurrentUser** calls once for database object in the user portion of the library list represented by **ILibraryList** .
</dd>
</dl>

Exceptions

<table class="dtTABLE" id="table2" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Exception Type
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgException 
</td>
            <td colspan="1" rowspan="1">

See table below. 
</td>
          </tr>
</table>

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.<br />

<table class="dtTABLE" id="table3" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells"> <colgroup span="1"> <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" /> <col span="1" style="WIDTH: 70%" /> </colgroup> <tr> <th colspan="1" rowspan="1" style="width: 209px"> Value of dgException.Error </th> <th colspan="1" rowspan="1"> Condition </th> </tr> <tr> <td colspan="1" rowspan="1" style="width: 209px"> <p>dgEmNODIRREAD 
</td>
            <td colspan="1" rowspan="1">

The database provider's security model does not permit the current session to access lists of library contents. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1" style="width: 209px">

dgEINVARG
</td>
            <td colspan="1" rowspan="1">

The path name given for this ILibraryList object does not correspond to a database library.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1" style="width: 209px">

dgExMISSING
</td>
            <td colspan="1" rowspan="1">

The database provider's "exit point" security support discovered a registration for an exit point validation routine for the method but the validation routine itself was not found.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1" style="width: 209px">

dgExINVLIC
</td>
            <td colspan="1" rowspan="1">

The database provider's "exit point" security support encountered an exit point validation routine for the method but the license for this support is invalid or not found.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1" style="width: 209px">

dgExDENIED
</td>
            <td colspan="1" rowspan="1">

Access to the method was denied by the database provider's "exit point" security support.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1" style="width: 209px">

dgEINTERNAL
</td>
            <td colspan="1" rowspan="1">

A database provider internal error occurred. Review the provider's event logs for more information.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1" style="width: 209px">

dgENOMEM
</td>
            <td colspan="1" rowspan="1">

The database provider encountered an "out of memory" exception.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1" style="width: 209px">

dgECHANBUSY
</td>
            <td colspan="1" rowspan="1">

The delegate *enumerator* has attempted to call a restricted method or access a restricted property. See AdgEnumerator for details on what DCS methods the delegate may invoke.
</td>
          </tr>
</table>

Remarks

**EnumerateCurrentUser** provides a call-back interface for enumerating the database object contents of the user portion of an existing library list. This is useful in visual applications, for example, when a library contains a large amount of objects and a separate thread is used to display a view of objects as they are supplied by the database provider. The delegate *enumerator* is called by **EnumerateCurrentUser** as each object is returned by the provider. Each object in the library list is rendered to the delegate as an instance of [ IAdgObject](dcsIAdgObjectClass.html) through which the program can immediately obtain static details, such as path name and object type. However, not all methods of **IAdgObject** are available from the delegate's code (see **AdgEnumerator** for details).

DCS and current database providers only support the enumeration of files and libraries as the contents of libraries. Exceptions raised by the delegate cause **Enumeration** to halt the database provider's stream of objects (safely interrupting the operation) just prior to rethrowing the exception.

Note that the [IDirectory.ItemList](dcsIDirectoryClassItemListProperty.html) property provides similar information, but "all at once" in a cached list format for a specific directory.
Requirements

<span><strong class="hcp2">Namespace:</strong> [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span><strong class="hcp2">Assembly:</strong> ASNA DataGate Client</span> 

<span><strong class="hcp2">Platforms:</strong> Windows Server 2003, Windows XP Professional SP2, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [ILibraryList Class](dcsILibraryListClass.html)
      <br />
      [ILibraryList Members](dcsILibraryListMembers.html)
      <br />
      [EnumerateCurrentSystem 
					Method](dcsILibraryListClassEnumerateCurrentSystemMethod.html)
      <br />
      [AdgEnumerator Delegate](dcsAdgEnumeratorDelegate.html)
      <br />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [IDirectory.ItemList Property](dcsIDirectoryClassItemListProperty.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

