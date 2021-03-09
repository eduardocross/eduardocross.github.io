---
title: DdsTable Column Collection Editor

Id: amfUnderColumnList
TocParent: amfUnderstandingTables
TocOrder: 10

keywords: ASNA Table Control
keywords: Column Data Storage
keywords: DdsTable Data Storage
keywords: DdsTable Column Dialog
keywords: Column List Editor
keywords: Column Collection Editor

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0
				   </span></td>
			    </tr>
</table>

# DdsTable Column Collection Editor

### Column Collection
That data for each DdsTable is stored in Columns, each of which reflects a single DataField on the IBM i. However, the presentation of these data fields is often more complex, as each column has its own properties that control the appearance and data associated with the coulmn. To make these properties easier to work with, the Column Collection Editor (below) is available through the Edit Columns property option in the Property Tasks or Property Window. 

![](Images/ColumnCollectionEditor.png)
<br/>

The Column Collection Editor has two panes:

- The left pane &#8211; contains a dynamic list of each column included in the table.
- The right pane &#8211; displays the properties of the column currently selected in the left pane.

The left pane has only four buttons associated with it:

- **Add**  &#8211; Adds a new column with a generic name to the bottom of the collection.
				Clicking the arrow on the right edge of the button opens a dropdown where the column type can be chosen from:
					<ul>
						<li>BinaryColumn
- CharColumnn
- IconColumn
- PackedColumn
- ZonedColumn

</li>
				<li> **Remove**  &#8211; Removes the selected column from the collction.</li>
				<li> **Up Arrow**  &#8211; Shifts the selected column up one rank in the collection.</li>
				<li> **Down Arrow**  &#8211; Shifts the selected column down one rank in the collection.</li>
			</ul>

The right pane contains two headings, each with associated properties

- Appearance
					<ul>
					<li> *CssClass*  &#8211; Sets a CSS class to apply to the column, useful for setting colors or transparency.
- *CssClassHeading*  &#8211; Sets a CSS class to apply to the column header, useful for setting colors or transparency.
- *[Heading](amfDdsTableClassHeadingProperty.html)*  &#8211; Sets a heading to associate with a column.
- *[HeadingFieldName](amfDdsTableClassHeadingFieldNameProperty.html)*  &#8211; Sets the name of an IFS field that will contain the heading to associate with a column.
- *[HeadingFieldLength](amfDdsTableClassHeadingFieldLengthProperty.html)*  &#8211; Sets the length of an IFS field that will contain the heading to associate with a column.
- *VisibleCondition*  &#8211; Contains a conditional indicator expression that determines whether the column is visible.

</li>
				<li>Data

- [FieldLength](amfDdsTableClassFieldLengthProperty.html) &#8211; Sets the length (in characters)
					for the DataField of the column.
- [FieldName](amfDdsTableClassFieldNameProperty.html) &#8211; Sets a field to contain the data for the column.

</li>

			</ul>

Columns of the IconColumn type also have the following additional properties

- Appearance
					<ul>
					<li> *[IconID](amfddsTableClassIconIdProperty.html)*  &#8211; Identifies which Icon to use from the 
								[IconID Collection](amfIconIDCollection.html).  This takes precdecence over programmatically specified values.
- *[CssClassIcon](amfddsTableClassCSSClassIconProperty.html)*  &#8211; CSSClass of the icon itself.
- *[IconBackColorField](amfddsTableClassIconBackColorFieldProperty.html)*  &#8211; Field that can contain a programmatically set background color to use for the icon.
- *[IconBackColorFieldLength](amfddsTableClassIconBackColorFieldLengthProperty.html)*  &#8211; Length of the IconBackColorField.
- *[IconForeColor](amfddsTableClassIconForeColorProperty.html)*  &#8211; Color used to paint the icon.
- *[IconForeColorField](amfddsTableClassIconForeColorFieldProperty.html)*  &#8211; Field that can contain a programmatically set IconForeColor.
- *[IconForeColorFieldLength](amfddsTableClassIconForeColorFieldLengthProperty.html)*  &#8211; Length of the IconForeColorField.
- *IconHeight*  &#8211; Height of the icon.
- *IconWidth*  &#8211; Width of the icon.

</li>	
				<li>Behavior

- *SelectedValue*  &#8211; Height of the icon. Value to be passed to the RPG program in the
								<code>SelectedField</code> to identify the Icon that the user has selected via click or touch.

</li>

			</ul>

Clicking **Okay** will save any changes made to the column collection. Clicking **Close** will close the dialog without saving. 
