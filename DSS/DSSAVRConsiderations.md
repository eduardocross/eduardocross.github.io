---
title: AVR Programming Considerations

Id: DSSAVRConsiderations
TocParent: DSSProgramming
TocOrder: 40

keywords: ASNA DataGate
keywords: ASNA DataGate&#174; for SQL Server
keywords: DSS
keywords: AVR and DSS
keywords: Programming Considerations
keywords: Programming AVR for DSS

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">[
				   ASNA DataGate&#174; for SQL Server Reference Manual
				   ](Welcome.html)</span></td>
			    </tr>
</table>

# AVR Programming Considerations

---

**<span style='font-size:10.0pt;font-family:Arial'>Contents</span>** 

Error Handling 

New Error Conditions 

Range Opcodes 

Considerations for Adapting Existing Applications to DSS 

Not Implemented Yet 

Other Considerations 

### Error Handling
<p class="MsoNormalSmall" style='margin-top:12.0pt;margin-right:0in;margin-bottom:12.0pt;margin-left:0in'> Strong consideration should be given to Visual RPG Error Indicators when performing I/O operations as they could be turned on now for reasons not present before. For instance, when the Chain opcode returned an error, the cause was commonly assumed to be that the record was busy. With DSS, error indicators can be turned on for various reasons such as the use of the <code>*NOLOCK</code> option on I/O operations. (See Locking considerations in the DG400 vs. DSS document). 

### New Error Conditions under DSS
The following situations will cause the error indicator to be set on. 

1. **Arrival Random Access.** 

When a file is opened for <span style='color:red;font-weight:normal;'>*Arrival</span> access, commands such as Chain, SetLL, etc, will cause an error condition.
2. **Use of the <code>*NOLOCK</code> option is not supported under DSS.** 

Any I/O operations that make use of the **<span style='color:red'>*NOLOCK</span>** option when working with files opened for update will cause an error condition.

To assist in finding areas in code that will potentially cause an error, a new IDE option is added to give warnings for invalid operations for DSS. This option is located in the " **Compiler** " Tab of the **Project &gt;Settings** menu option. 

###  Range Opcodes 
I/O op codes provide better performance when working with large files. 

- <code>SetRange</code> – Use the SetRange opcode in place of SetLL when you're doing <code>SetLL/ReadE</code> loops.
- <code>ReadRange</code> – Use the ReadRange opcode in place of the Chain opcode when you're doing <code>Chain/ReadE</code> loops.
- <code>DeleteRange</code> – Use the DeleteRange when performing delete loops.

###  Considerations for Adapting Existing Applications to DSS 
In DataGate&#174; for SQL Server, the record format name is always " **R" + Filename** . If the record format name is anything else, **and** you've specified this record format name on I/O operations, a rename format will need to be specified on the <code>DCLDISKFILE</code> statement as follows. <code> **RNMFMT(OldFormatName)** </code> where <code> *OldFormatName* </code> is the name of the existing format. &#160;No changes will need to be made to the actual I/O statements. 

The old syntax of <code>RNMFMT(OldFormatName,NewFormatName)</code> is not needed. 

- **Arrival sequence processing**  must be changed to indexed processing. 
        The simplest method for handling this would be to employ the use of a key field in the file.
- If you're using **multi-member files** , you will need to provide an alternative method for handling
	the logic involving these files.
- If your file's **record length is &gt; 8060** , you will need to consider changes necessary in order 
	to make the record length smaller.
- Be sure to include the <a href="#New_Range_Opcodes">range operations</a> to enhance speed.
- If you were using the <code> ***NOLOCK** </code> opcode for files opened for update, you will need to declare an 
	<code> ***Input** </code> instance of the file for <code> ***NOLOCK** </code> access.
- If an application is going to run against both DataGate&#174; for SQL Server and DataGate&#174; 400, and your file 
	currently contains **binary**  fields, you will need to consider changing the field type.

### Other Considerations 

- It is recommended that you do not use <code> **ADBFEDIT** </code> to browse files that are not
indexed because of the inability to scroll within the file. &#160;These types
of files can be viewed with the **Microsoft SQL Server Management Studio** .

