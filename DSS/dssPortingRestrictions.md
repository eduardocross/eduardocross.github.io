---
title: Porting AVR.NET Applications Restrictions

Id: dssPortingRestrictions
TocParent: dssPortingMain
TocOrder: 05

---

<table>
			    <tr>

			       <td><span class="OH_MultiViewContainerPanelDhtmlTable"> DataGate&#174; 16.0 for SQL Server Reference Guide
				   </span><br />
				   </td>
			    </tr>
</table>

# Porting AVR.NET Applications: Restrictions
Even though DSS tries to make *SQL Server* look like DB2/400, there are several features that cannot be implemented in a totally transparent fashion. The *SQL Server* database engine is of a different design and implementation than the IBM i and DataGate&#174; engines. 

The intent of this paget is to help you become aware of the items that will most likely affect your application and the process of using *SQL Server* as your database. Through it all, remember the goal you are seeking is to create applications that take advantage of the many features of *SQL Server* and to create applications that can run with either *SQL Server* or DB2/400 as the underlying database engine. 

In other sections we'll deal with all of the issues that will need your attention, but the following items are probably the ones with the most impact for many users. 

#### No Multi-Format Logical Files:
DSS implements a physical file through the use of a native *SQL Server* table. A logical file is implemented through a native view. *SQL Server* Views are single formatted in nature, so there is no support for multi-format logical data files. You will have to eliminate any reference to multi-format logical files in your application. 

Print files, although they are typically multi-formatted, are fully supported in DSS, however. 

#### Single Member Files:
*SQL Server* doesn't have the concept of members of a table/view. DSS for .NET makes it appear as though each file had one (and only one) member; the member name is exactly the same as the file name. For the member name, you can use the exact name or the special values *FIRST and *FILE. You should be careful when using the Copy Data and Copy Library tools of the DataGate&#174; Database Manager to copy a file from DataGate&#174; or IBM i, because they default to *SAME for the target member name; if the source member name was different than the file name, the copy will fail. 

If your application depends on the existence of multiple members per file, you will want to re-architect it to provide an alternative method for handling the logic involving these files. 

#### Logical Field Restrictions: 
There are two restrictions on the usage of logical fields when they change the name or the type of their corresponding base physical field. When the field is retyped, most typically because the field is a concatenation or substring of the physical, then the field becomes read only. A logical field, whose name has changed from its physical base field, can't be used as a key field in the logical file. 

#### Unlocking Records:
This is probably the most demanding area of application adaptation between the differences of implementation between IBM i method of record locking and that of the *SQL Server* database engine. The problem arises in two areas: Using the *nolock keyword on the read operations and on the implementation of the UNLOCK command. 

DSS for .NET uses *SQL Server* 'Server Cursors' to implement file access. When a file is opened for update, it is not possible to tell *SQL Server* to not lock the record on a read, so a read with *nolock has no effect for files opened for Update. There are two methods to resolve this problem: 

1. Declare a second instance of the file marked as 
							input only and use it wherever the NoLock option 
							would have been given on a read/chain.
2. Retain the *nolock and follow the read/chain 
							with an UNLOCK command. Be aware this method imposes 
							some restrictions as stated in the next paragraph.

The UNLOCK command leaves the cursor in a no-position state, meaning you can't perform a subsequent read (next/previous) without repositioning the file with a SETLL, SETGT or CHAIN. 
