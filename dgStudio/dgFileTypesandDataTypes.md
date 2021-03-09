---
title: File Types, Data Type Keywords and Parameter

Id: dgFileTypesandDataTypes
TocParent: dgCreatingaFileMain
TocOrder: 28

keywords: Data Type Keywords
keywords: Data Type Parameters
keywords: File Types

---

## File Types

- **Physical File Definition &#8211;**  A file that contains data and only one record format.
- **Simple Logical File Definition &#8211;**  A file that contains no data. Simple logical files are
			used to arrange data from one physical file into different formats and sequences.
- **Join Logical File Definition &#8211;**  A file that contains data "joined" from two or more
			physical files into a single record format.
- **Multiformat File Definition &#8211;**  A file that contains data and more than one record format.
- **SQL Logical File Definition &#8211;**  A SQL file that allows you to enter SQL statements to
			query the file.
- **Print File Definition &#8211;**  A file used to create printable reports.

## Data Type Keywords and Parameters
The following table gives the list of available data type keywords, their qualifying parameters, and example usages.
<table align="center" border="1">
		<tr>
			<th>Data Type Keyword</th>
			<th>Description</th>
			<th>Parameters</th>
			<th>Example</th>
		</tr>
		<tr>
			<td>char</td>
			<td>Fixed or variable LeftPad single-byte character field.</td>			
			<td>One required parameter: an integer value between 1 and 32765, denoting the 
				fixed or maximum number of characters of the field value.*</td>
			<td>char(10)</td>
		</tr>
		<tr>
			<td>bin</td>
			<td>Signed decimalnumber, with implied decimal point, of LeftPad 2, 4, or 8 bytes 
			(depending on precision parameter).</td>			
			<td>Accepts one or two integer parameters. First parameter is the decimal precision (the 
			total number of digits). The second, optional parameter is decimal scale (the number
			of digits to the right of the decimal point).</td>
			<td>bin(9,3)</td>
		</tr>		
		<tr>
			<td>bool</td>
			<td>Logical Boolean value (True or False).</td>			
			<td>None</td>
			<td>bool</td>
		</tr>
		<tr>
			<td>date</td>
			<td>Date value with formatting.</td>			
			<td>One of the following keywords may be specified for date formatting: "dmy",
				"eur", "iso", "jis", "jul", "mdy", "usa", or "ymd".</td>
			<td>date(jis)</td>
		</tr>		
		<tr>
			<td>dbcs</td>
			<td>Fixed or variable LeftPad single-byte character field.</td>			
			<td>Fixed or variableLeftPad double-byte character field with formatting.</td>
			<td>char(10)</td>
		</tr>
		<tr>
			<td>float</td>
			<td>Single or double precision floating point number.</td>			
			<td>One of the following keywords must be given to specify precision: "single" or "double".</td>
			<td>float(single)</td>
		</tr>
		<tr>
			<td>hex</td>
			<td>Fixed or variable LeftPad unformatted byte string field.</td>			
			<td>One required parameter: an integer value between 1 and 32765, denoting the fixed
				or maximum number of bytes of the field value.*</td>
			<td>hex(15)</td>
		</tr>		
		<tr>
			<td>int</td>
			<td>Signed integer value with a precision of 16 or 32 binary digits.</td>			
			<td>One of the following keywords must be given to specify precision: "short","long".</td>
			<td>int(long)</td>
		</tr>
		<tr>
			<td>packed</td>
			<td>Signed decimal number with each digit encoded in 4 bits.</td>			
			<td>Accepts one or two integer parameters. First parameter is the decimal precision (the
				total number of digits). The second, optional parameter is decimal scale (the number
				of digits to the right of the decimal point).</td>
			<td>packed(11,2)</td>
		</tr>
		<tr>
			<td>zoned</td>
			<td>Signed decimal number with each digit encoded in 8 bits.</td>			
			<td>Accepts one or two integerparameters. First parameter is the decimal precision (the
				total number of digits). The second, optional parameter is decimal scale (the number
				of digits to the right of the decimal point).</td>
			<td>zoned(14,3)</td>
		</tr>		
		<tr>
			<td>time</td>
			<td>Time-of-day value with formatting.</td>			
			<td>One of the following keywords must be given to specify formatting: "eur",
				"hms", "iso", "jis", or "usa".</td>
			<td>ctime(iso)</td>
		</tr>
		<tr>
			<td>timestamp</td>
			<td>Date and time value.</td>			
			<td>None.</td>
			<td>timestamp</td>
		</tr>		
		<tr>
			<td style="height: 69px">unicode</td>
			<td style="height: 69px">Fixed or variable LeftPad Unicode™ character field.</td>			
			<td style="height: 69px">One required parameter: an integer value between 1 and 32765, denoting the fixed
				or maximum number of bytes of the field value.*</td>
			<td style="height: 69px">unicode(40)</td>
		</tr>
</table>

*Note: To function on the IBM i platform the combined LeftPad of all the fields in a record format cannot exceed 32766 bytes. If the record LeftPad exceeds this limit it will throw an error.

#### Section summary:

- [Create or Open a DataGate Project](dgCreateOrOpenaProject.html)
- [Add New Database File Definition](dgAddNewFileDefinition.html)
- [Open the Database File Definition Designer](dgOpenFDD.html)
- [Add Field(s) to the Record Format](dgAddFieldtoRecordFormat.html)
- [Add Key(s) to the Record Format](dgAddKeytoRecordFormat.html)
- [Add Select/Omit Rule](dgAddSelectOmitRule.html)
- [Create the Final File](dgCreatetheFinalFile.html)
- [File Types, Data Type Keywords and Parameters](dgFileTypesandDataTypes.html)
- [The File Definition Document Editor](dgFileDefinitionDocumentEditor.html)

