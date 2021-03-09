---
title: Editing DdsTable Cells

Id: amfUnderstandingTablesEdit
TocParent: amfUnderstandingTables
TocOrder: 95

keywords: ASNA Mobile RPG
keywords: ASNA Mobile RPG, Tables
keywords: ASNA Mobile RPG, Table controls
keywords: Mobile RPG

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0
				   </span></td>
			    </tr>
</table>

# Editing DdsTable Cells and Columns

### New Properties
The following properties have been added to each column type **EXCEPT** IconColumns.
<table>
						 <tr><th>Name</th><th>Description</th></tr>
						 <tr><td><code>CssClassEditableCell</code> </td><td>Specifies the CssClass applied to editable cells.</td></tr>
						 <tr><td><code>CssClassErrorRow</code> </td><td>Specifies the CssClass applied to rows containing errors.</td></tr>
						 <tr><td><code>CssClassHoverRow</code> </td><td>Specifies the CssClass applied to the row the mouse is currently hovering over.</td></tr>
						 <tr><td><code>Usage</code> </td><td>Specifies if this field is output-only, input-only, input/output (both), hidden</td></tr>
						 <tr><td><code>Protect</code></td><td>Protect Value from user input Field Name or Indictaor Number</td></tr>
						 <tr><td><code>EditMode</code></td><td>Determines whether editing uses modal dialog or InLine editing.</td></tr>
						 <tr><td><code>ErrorIndicator</code></td><td>Error Indicator Expression</td></tr>
						 <tr><td><code>ErrorText</code></td><td>Static Error Text to be displayed if ErrorIndicator is true.</td></tr>
						 <tr><td><code>ErrorField</code></td><td>Field that contains the Error Text; used for dynamic error messages.</td></tr>
						 <tr><td><code>ErrorFieldLength</code></td><td>Length of Error Field</td></tr>
</table>

### Mechanics of Editing a DdsTable
When any of the fields' Usage is set to <code>input-only</code> or <code>both</code>, the user will be able to edit the contents of the table. Clicking on an edit-ready cell will highlight the cell and one of two processes will begin, depending on whether the [EditMode](amfddsTableClassEditModeProperty.html) property is set to Modal or InLine.

#### <code>EditMode=Modal</code>
A pop up a dialog will appear, allowing users to update the text. The green check-mark and red X (pictured below) represent Save and Cancel.

![](images/TableEdit1.png)

Clicking a cell that is protected, via the <code>Protect</code> Property will pop up a dialog to notify the user that it cannot be edited.

![](images/TableEdit2.png)

Once a function key is fired, the data in the view will be sent to the 400.

If the <code>ErrorIndicator</code> expression resolves to true, the cell will be marked with an error (using CSS: by default it will have a red border around it). If the cell opened for editing, the error message will appear below the current cell's value in the edit dialog (shown below).

![](images/TableEdit3.png)

#### <code>EditMode=InLine</code>
The cell will be restyled and become open for editing.

![](images/TableEdit5.png)

Hitting enter will end the editing, but unlike with the <code>Modal</code> option, errors will be reported on the table rather than in a separate dialog:

![](images/TableEdit6.png)

The appearance of cells selected for editing can be adjusted through the [CssClassSelectedCell](amfddsTableClassCssClassSelectedCellProperty.html) property. The default class is <code>DdsTableSelectedCell</code>, and its appearance is a blue border, shown below, around <code>WASHINGTON</code>: 

![](images/TableEdit4.png)
