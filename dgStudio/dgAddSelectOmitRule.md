---
title: Adding a Select/Omit Rule

Id: dgAddSelectOmitRule
TocParent: dgCreatingaFileMain
TocOrder: 26

keywords: Adding a Select Omit Rule
keywords: Select Omit Rule
keywords: Select Rule
keywords: Omit Rule
keywords: Adding a Rule
keywords: Adding rules

---

When a logical file record is to be accessed by a program, the select/omit rules are evaluated sequentially by the database until an expression is found to be true, then the related action (Select or Omit) is taken.

Use the *TRUE keyword to specify the action to be taken after all other Select/Omit statements have been processed. Specify "Select: *TRUE" to direct the database to select any records that do not meet any of the previous Select/Omit rules. Conversely, specify "Omit: *TRUE" to omit any records that do not meet any of the previous Select/Omit rules.

If the *TRUE rule is omitted, the default action is to presume you want all remaining records to be either selected or omitted depending upon the last Select/Omit statement. That is:

- If the last statement was a **Select** , the default is to assume "Omit: *TRUE" wherein
			all records that did not meet the any of the previous Select/Omit rules will be
			omitted.
- If the last statement was an **Omit** , the default is to assume "Select: *TRUE" wherein
			all records that did not meet the any of the previous Select/Omit rules will be
			selected.

#### To Add a Select/Omit Rule to a Logical Format

1. Open the physical file definition source file in the Database File Definition Designer.
2. In the details tree view of the designer, select the record format node as shown
				below with the RCMMASTL1 record format.
3. Select the **Select/Omit**  tab in the lower right panel to display the select/omit grid
				as shown below.			

![](../images/KeysGrid.bmp)
4. Scroll to the bottom of the select/omit grid, if necessary. Select the **New Row**  
				(the last row of the grid) by clicking on the leftmost column of the row.
5. Select the **rule**  verb by clicking on the drop-down box in the **Verb**  cell. Change 
				the rule expression from the default "*none" to a logical expression
				pertaining to the rule. Note that the rule will not be added to the format until you
				select a verb and enter an expression.

A logical expression consists of a field name, an operator, and a constant. The valid relational operators are: &#62;, &#62;=, &#60;, &#60;=, =, !=,. Refer also to the illustration below comparing AS/400 and DataGate coding of rules.

#### Illustration:
The Select/Omit Rules below compare the rule implementation in DDS and DataGate.

#### DDS Example:
<pre class="prettyprint">
       	O PRTDSC COMP(EQ 'HAMMER')
	S UNTPRC COMP(GT PRCLVL)
	ONHAND COMP(LT 10)
	O ALL
		</pre>

The same rules as above coded for DataGate:
<pre class="prettyprint">
	Omit: PRTDSC = 'HAMMER'
	Select: UNTPRC &#62; PRCLVL &#38; ONHAND &#60; 10
	Omit: *TRUE
		</pre>

If the expression is incorrectly constructed, an error may occur when creating the file.

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

