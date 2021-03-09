---
title: List Controls

Id: amfUnderstandingLists
TocParent: amfASNAMobileSupport
TocOrder: 60

keywords: ASNA Mobile RPG
keywords: ASNA Mobile Lists
keywords: ASNA Mobile RPG, Lists
keywords: Mobile RPG
keywords: Lists
keywords: List Control

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span></td>
			    </tr>
</table>

# List Controls

### What is a DdsList?
Often, mobile applications express their data and options in the form of lists. While simple lists of items can be created with a subfile, many apps present feature-rich lists with descriptive text, thumbnail images, checkboxes, switches, and other interactive widgets. The [DdsList Control](amfDdsListClass.html) can be used to create these more complex lists while still using a straightforward RPG Subfile on the IBM i.

**Applicability:** The Navigation ListType is exclusive to Mobile RPG; all other features of the DdsList are available in both Mobile RPG and Wings.
<div>

Each DdsList draws its data from a subfile (defined by the <code>[SubfileName](amfDdsListClassSubfileNameProperty.html)</code> property) on the IBM i. Each record on the RPG subfile represents an item that will appear on the DdsList. 

Each record of the RPG subfile contains at least two mandatory fields:

1. A text field: 
						Which holds the text that will be displayed in the list 
						item (defined by the <code>[TextField](amfDdsListClassTextFieldProperty.html)</code> property)
2. A selection field: Which determines whether the item 
						is selected or not (defined by the <code>[SelectedField](amfDdsListClassSelectedFieldProperty.html)</code> property)

The selection field can have a value of either "<code>1</code>" or "<code>0</code>" with "<code>1</code>" indicating that the field is selected. This value can be set for each record by the programmer. The User can also change the item selection (usually just by tapping on it) and the changes will be reflected in the RPG subfile as the selection field value changes to "<code>0</code>" or "<code>1</code>".

### The Four List Styles
The DdsList lets the programmer set the the overall style of the list set at design time (via the <code>[ **ListType** ](amfDdsListClassListTypeProperty.html)</code> property). DdsLists can take any of the following forms: 

- Checkbox list - Consisting of one or more items accompanied by checkboxes.
- Radio button list - Consisting of one or more items accompanied by radio buttons, only one of which can be 
						selected at a time.
- Dropdown list - Consisting of one or more items presented in a low-profile list that must be dropped down to be selected.
- Navigation list - Consisting of one or more 
						items presented with a wider variety of mobile-friendly 
						options.

In the Navigation <code>ListType</code>, up to five visible features can be added to each list entry: main **Text** , **Detail** text, an **Image** , a checkbox (or radio button), and a right-pointing chevron that indicates whether a field is **Navigable** . The default locations of these parts are detailed on the image of a navigable list below:

![](images/Checkboxlist.png)![](images/radiobuttonlist.png)![](images/dropdownlist.png)![](images/NavigationList.png)

From left to right, a checkbox list, a radio button list, a dropdown list, and a navigation list.

### The Mechanics of a DdsList
A DdsList, like most Monarch controls, must be placed inside of a [DdsRecord](amfddsRecordClass.html). A DdsList has properties that define the RPG subfile, its record formats, its fields, and the subfile controller on which the RPG subfile depends.

#### On Output
When the DdsList is going to be shown, the RPG subfile must be populated with its data, by means of code similar to this:
<pre>SetOff										99 //To clear subfile record
WRITE   SubCTLR
SetOff										99
//Loop reading subfile reload
WRITE	Subfile
SetOff										99
WRITE	SubCTLR				
EXTFMT</pre>

#### On Input
As part of the definition of DdsList the a field in the subfile is used to tell the program when the user has selected a record. As noted in the introduction, this field is defined by the [SelectedField](amfDdsListClassSelectedFieldProperty.html) property, and it can take a value of either "1" (selected) or "0" (not selected). The value can be set by the programmatically or swtiched by the user (the user taps an empty checkbox or radio button, and it's filled, or vice versa). If altered by the user, the change will then be communicated back to the IBM i when the page is submitted.

### Using Checkbox Lists
Lists featuring checkboxes allow the deliberate and simultaneous selection of several options. This can come in handy whenever the user is adjusting multiple options, or making selections before submitting the information to the RPG Program. They generally only have Text elements.

Note that <code>ReadC</code> only looks for the most recent changes to the underlying subfile. In the case of Checkboxes, the program will fail to pick up previous selections on subsequent loops. So if item 2 is changed after item 1, ReadC will only detect item 2. 

### Using Radio Button Lists
Lists featuring radio buttons allow for the exclusive selection of a single option. Selecting another list item will immediately de-select the first option. 

### Using Dropdown Lists
Dropdowns are perhaps the simplest type of lists: they only hold text, and tapping on them generally causes something (navigation, turning something on or off) to happen immediately.

### Using Navigation Lists
Navigation lists represent the most complex and modern-looking lists that the DdsList control can create. In the Navigation ListType, up to five visible features can be added to each list entry: main **Text** , **Detail** text, an **Image** , a checkbox (or radio button), and a right-pointing chevron that indicates whether a field is **Navigable** . The default locations of these parts are detailed on the image of a navigable list below:

![](images/Fig92.jpg)

#### DdsList Property Tasks
The following list details the properties most essential to creating, populating, and styling a DdsList. They can all be changed in the Property Window.
![](Images/DdsListTasks.png)

<table class="TaskTable" border="1" cellspacing="0" cellpadding="0" width="637"> <tbody> <tr> <td valign="top" width="185"> <p align="center"> **Property** 
</td>
            <td valign="top" width="452">

**Notes** 
</td>
        </tr>
		       <tr>
            <td colspan="2" valign="top" width="185">

**Appearance** 
</td>

        </tr>
		       <tr>
            <td valign="top" width="185">

                    <code> **[ChevronIconID](amfDdsListClassChevronIconIDProperty.html)** </code>

            </td>
            <td valign="top" width="452">

                  ID of the Icon that will be used as a chevron.

            </td>
        </tr> 
		      <tr>
            <td valign="top" width="185">

                    <code> **[DetailAlignment](amfDdsListClassDetailAlignmentProperty.html)** </code>

            </td>
            <td valign="top" width="452">

                    Sets the Alignment of the Detail within the list.

            </td>
        </tr>
		  <tr> 
		   <td colspan="2" valign="top" width="185">

**Behavior** 
</td>
		</tr>	
        <tr>
            <td valign="top" width="185">

                    <code> **[ListType](amfDdsListClassListTypeProperty.html)** </code>

            </td>
            <td valign="top" width="452">
             An enumeration the sets the type of the list: Checkbox, Dropdown, 
			 Listbox, Radio, or Navigation</td>
        </tr>
		<tr>
            <td valign="top" width="185" style="height: 23px">

                    <code> **[SelectChevronKey](amfDdsListClassSelectChevronKeyProperty.html)** </code>

            </td>
            <td valign="top" width="452" style="height: 23px">

                    Sets the AidKey pressed when a chevron is selected by a 
					user.</td>
        </tr>
		 <tr>
            <td valign="top" width="185" style="height: 23px">

                    <code> **[SelectItemKey](amfDdsListClassSelectItemKeyProperty.html)** </code>

            </td>
            <td valign="top" width="452" style="height: 23px">

                    Sets the AidKey pressed when a list item is selected by a 
					user.</td>
        </tr>
		  <tr> 
		   <td colspan="2" valign="top" width="185">

**Data** 
</td>
		</tr>
        <tr>
            <td valign="top" width="185">

 **<code>[CategoryField](amfDdsListClassCategoryFieldProperty.html)</code> &amp; 
					<code>[CategoryFieldLength](amfDdsListClassCategoryFieldLengthProperty.html)</code>** 

            </td>
            <td valign="top" width="452">

                    These properties define a character field whose runtime value is used to get the text content of the Category.

            </td>
        </tr>		

		        <tr>
            <td valign="top" width="185">

                    <code> **[ClearIndicator](amfDdsListClassClearIndicatorProperty.html)** </code>

            </td>
            <td valign="top" width="452">

                   Sets the clear indicator for the list's underlying subfile.

            </td>
        </tr>
       		        <tr>
            <td valign="top" width="185">

                    <code> **[DetailField](amfDdsListClassDetailFieldProperty.html) 
					&amp; [DetailFieldLength](amfDdsListClassDetailFieldLengthProperty.html)** </code>

            </td>
            <td valign="top" width="452">

                    These properties define a character field whose runtime value is used to get the text content of the Detail area.

            </td>
        </tr>
		    <tr>
            <td valign="top" width="185">

 **<code>[NavigableField](amfDdsListClassNavigableFieldProperty.html)</code>** 

            </td>
            <td valign="top" width="452">

                    This property defines a character field whose runtime 
					value is used to set the value for the address to navigate 
					to when a list item or chevron is tapped. The special value <code> ***TRUE** </code> is used to 
					indicate that all items should be navigable.</td>
        </tr>
		<tr>
            <td valign="top" width="185" style="height: 23px">

                    <code> **[ProtectValueField](amfDdsListClassProtectValueFieldProperty.html)** </code>

            </td>
            <td valign="top" width="452" style="height: 23px">

                   Protect Value from user input Field Name or Indicator Number.

            </td>
        </tr>
		<tr>
            <td valign="top" width="185" style="height: 23px">

                    <code> **[SelectedField](amfDdsListClassSelectedFieldProperty.html)** </code>

            </td>
            <td valign="top" width="452" style="height: 23px">

                    Displays whether the record is selected (charfield).

            </td>
        </tr>
        <tr>
            <td valign="top" width="185" style="height: 44px">

                    <code> **[SubfileControlName](amfDdsListClassSubfileControlNameProperty.html)** </code>

            </td>
            <td valign="top" width="452" style="height: 44px">

                    The name of the subfile control record format used for the list data.

            </td>
        </tr>
        <tr>
            <td valign="top" width="185">

                    <code> **[SubfileName](amfDdsListClassSubfileNameProperty.html)** </code>

            </td>
            <td valign="top" width="452">

                    The name of the subfile record format used for the list data.

            </td>
        </tr>
        <tr>
            <td valign="top" width="185">

                    <code> **[TextField](amfDdsListClassTextFieldProperty.html) &amp; 
					[TextFieldLength](amfDdsListClassTextFieldLengthProperty.html)** </code>

            </td>
            <td valign="top" width="452">

                    These properties define a character field whose runtime value is used to get the text content of the Text area.

            </td>
        </tr>
        <tr>
            <td valign="top" width="185">
 **<code>[ValueField](amfDdsListClassValueFieldProperty.html)</code>
									&amp; <code>[ValueFieldLength](amfDdsListClassValueFieldLengthProperty.html)</code>** 
                            </td>
            <td valign="top" width="452">

                    These properties define hidden fields that may contain data the program will need.

            </td>
        </tr>
		  <tr> 
		   <td colspan="2" valign="top" width="185">

**Image** 
</td>
		</tr>
		<tr>
            <td valign="top" width="185">

                    <code> **[IconID](amfDdsListClassIconIDProperty.html)** </code>

            </td>
            <td valign="top" width="452">

                  ID of the Icon that will be used as a list-item image.

            </td>
        </tr>

		       <tr>
            <td valign="top" width="185">

                    <code> **[ImageDirectory](amfDdsListClassImageDirectoryProperty.html)** </code>
                   </td>
            <td valign="top" width="452">

                    Sets a character field whose runtime value is used as the path to the directory holding the image file.

            </td>
        </tr>
      <tr>
            <td valign="top" width="185">

                 <code> **[ImageName](amfDdsListClassImageNameProperty.html)** </code>
				 </td><td valign="top" width="452">

                    Sets a character field whose runtime value is used to get the name of the image file.

            </td>
        </tr>
        <tr>
            <td valign="top" width="185" >

                    <code> **[ImageLocation](amfDdsListClassImageLocationProperty.html)** </code>

            </td>
            <td valign="top" width="452" >

                    Sets the location of the image within the list.

            </td>
        </tr>
    </tbody>
</table>
				</p>

The <code>[NavigableField](amfDdsListClassNavigableFieldProperty.html)</code> property is a special case: It defines a field, setting it to a value, for instance <code>'DRILL'</code> indicates the request to define a field called <code>'DRILL'</code>, the program can then set the value of the field <code>'DRILL'</code> to <code>'1'</code> before adding a record to the subfile, indicating that the user will be able to tap on that record, setting <code>'DRILL'</code> to <code>'0'</code> before adding the subfile record would prevent the user from tapping on it. If all the list items are going to be navigable, do not specify the <code>NavigableField</code> property at all, or set it to the special value <code>'*True'</code>. 

If all the list items are going to be navigable, do not specify this property at all, or set it to the special value '<code>*True</code>'.

### The List Types
The <code>ListType</code> property determines the impact of several other properties, as the Navigation list type in particular has several features not available in the other formats:
<table border="1" cellspacing="0" cellpadding="0" width="637">
    <tbody>
        <tr>
            <td valign="top" width="185">

**ListType** 
</td>
            <td valign="top" width="452">

**Navigation** 
</td>
            <td>
**Checkbox** 
</td>
        <td style="width: 81px">
**Dropdown** 
</td><td>
**Radiobutton** 
</td>

</tr>
        <tr>
            <td valign="top" width="185" style="height: 22px">

 **<code>[CssClass](amfDdsListClassCssClassProperty.html)</code>** 

            </td>
            <td valign="top" width="452" style="height: 22px">

                    Yes</td><td style="height: 22px">Yes</td>
			<td style="height: 22px; width: 81px;">Yes</td><td style="height: 22px">Yes</td>

        </tr>
        <tr>
            <td valign="top" width="185">

                    <code> **[CssClassList](amfDdsListClassCssClassListProperty.html)** </code>

            </td>
            <td valign="top" width="452">

                    Yes</td><td>Yes</td><td style="width: 81px">Yes</td><td>Yes</td>

        </tr>
        <tr>
            <td valign="top" width="185">

                    <code> **[CssClassDetail](amfDdsListClassCssClassDetailProperty.html)** </code>
					</td>
            <td align="top" width="452">
             Yes</td><td>No</td><td style="width: 81px">No</td><td>No</td>
        </tr>
		<tr>
            <td valign="top" width="185">

                    <code> **[CssClassImage](amfDdsListClassCssClassImageProperty.html)** </code></td>
            <td align="top" width="452">
             Yes</td><td>Yes</td><td style="width: 81px">No</td><td>Yes</td>
        </tr>
		<tr>
            <td valign="top" width="185">

                    <code> **[CssClassChevron](amfDdsListClassCssClassChevronProperty.html)** </code>

            </td>
            <td align="top" width="452">
             Yes</td><td>No</td><td style="width: 81px">No</td><td>No</td>
        </tr>
        <tr>
            <td valign="top" width="185" style="height: 23px">

                    <code> **[SubfileControlName](amfDdsListClassSubfileControlNameProperty.html)** </code>

            </td>
            <td valign="top" width="452" style="height: 23px">

                    Yes</td><td style="height: 23px">Yes</td>
			<td style="width: 81px; height: 23px;">Yes</td>
			<td style="height: 23px">Yes</td>

        </tr>
        <tr>
            <td valign="top" width="185" >

                    <code> **[SubfileName](amfDdsListClassSubfileNameProperty.html)** </code>

            </td>
            <td valign="top" width="452" >

                    Yes</td><td >Yes</td>
			<td style="width: 81px" >Yes</td><td >Yes</td>

        </tr>
        <tr>
            <td valign="top" width="185" style="height: 23px">

                    <code> **[SelectedField](amfDdsListClassSelectedFieldProperty.html)** </code>

            </td>
            <td valign="top" width="452" style="height: 23px">

                    Yes</td><td style="height: 23px">
			Yes</td><td style="width: 81px; height: 23px">Yes</td>
			<td style="height: 23px">Yes</td>

        </tr>
                <tr>
            <td valign="top" width="185" style="height: 23px" >

                    <code> **[SelectChevronKey](amfDdsListClassSelectChevronKeyProperty.html)** </code>

            </td>
            <td valign="top" width="452" style="height: 23px" >

                    Yes</td><td style="height: 23px" >No</td>
			<td style="height: 23px; width: 81px;" >No</td><td style="height: 23px" >No</td>

        </tr>
		<tr>
            <td valign="top" width="185" >

                    <code> **[SelectItemKey](amfDdsListClassSelectItemKeyProperty.html)** </code>

            </td>
            <td valign="top" width="452" >

                    Yes</td><td >
			Yes</td>
			<td style="width: 81px" >Yes</td><td >Yes</td>

        </tr>
                <tr>
            <td valign="top" width="185" style="height: 23px">

                    <code> **[Categorized](amfDdsListClassCategorizedProperty.html)** </code>

            </td>
            <td valign="top" width="452" style="height: 23px">

                    Yes</td><td>Yes</td><td style="width: 81px">
					Yes</td><td>Yes</td>

        </tr>

        <tr>
            <td valign="top" width="185">

                    <code> **[CategoryField](amfDdsListClassCategoryFieldProperty.html) &amp; 
					[CategoryFieldLength](amfDdsListClassCategoryFieldLengthProperty.html)** </code>

            </td>
            <td valign="top" width="452">

                    Yes</td><td>Yes</td><td style="width: 81px">
			Yes</td><td>Yes</td>

        </tr>
        <tr>
            <td valign="top" width="185">

                    <code> **[TextField](amfDdsListClassTextFieldProperty.html) &amp; 
					[TextFieldLength](amfDdsListClassTextFieldLengthProperty.html)** </code>

            </td>
            <td valign="top" width="452">

                    Yes</td><td>Yes</td><td style="width: 81px">
			Yes</td><td>Yes</td>

        </tr>
        <tr>
            <td valign="top" width="185">

                    <code> **[DetailField](amfDdsListClassDetailFieldProperty.html) &amp; 
					[DetailFieldLength](amfDdsListClassDetailFieldLengthProperty.html)** </code>

            </td>
            <td valign="top" width="452">

                    Yes</td><td>No</td><td style="width: 81px">No</td><td>No</td>

        </tr>
        <tr>
            <td valign="top" width="185">

                    <code> **[DetailAlignmnet](amfDdsListClassDetailAlignmentProperty.html)** </code>

            </td>
            <td valign="top" width="452">

                    Yes</td><td>No</td><td style="width: 81px">No</td><td>No</td>

        </tr>
        <tr>
            <td valign="top" width="185" >

                    <code> **[ImageLocation](amfDdsListClassImageLocationProperty.html)** </code>

            </td>
            <td valign="top" width="452" >

                    Yes</td><td>
			Yes</td><td style="width: 81px">No</td><td>Yes</td>

        </tr>
        <tr>
            <td valign="top" width="185">

                    <code> **[ImageDirectoryField](amfDdsListClassImageDirectoryFieldProperty.html)
                     &amp; 
					[ImageDirectoryFieldLength](amfDdsListClassImageDirectoryFieldLengthProperty.html)** </code>

            </td>
            <td valign="top" width="452">

                    Yes</td><td>Yes</td><td style="width: 81px">
			No</td><td>Yes</td>

        </tr>
        <tr>
            <td valign="top" width="185" style="height: 44px">

                    <code> **[ImageNameField](amfDdsListClassImageNameFieldProperty.html)
                     &amp; 
					[ImageNameFiedLength](amfDdsListClassImageNamFieldLengthProperty.html)** </code>

            </td>
            <td valign="top" width="452" style="height: 44px">

                    Yes</td><td style="height: 44px">Yes</td>
			<td style="height: 44px; width: 81px;">No</td><td style="height: 44px">Yes</td>

        </tr>
        <tr>
            <td valign="top" width="185">
                    <code> **[ValueField](amfDdsListClassValueFieldProperty.html)** </code>
            </td>
            <td valign="top" width="452">

                    Yes

            </td><td>Yes</td><td style="width: 81px">Yes</td><td>Yes</td>

        </tr>
        <tr>
            <td valign="top" width="185" style="height: 44px">

                    <code> **[NavigableField](amfDdsListClassNavigableFieldProperty.html) 
                    &amp; 
					[NavigableFieldLength](amfDdsListClassNavigableFieldLengthProperty.html)** </code>

            </td>
            <td valign="top" width="452" style="height: 44px">

                    Yes</td><td style="height: 44px">No</td>
			<td style="height: 44px; width: 81px;">No</td><td style="height: 44px">No</td>

        </tr>
        <tr>
            <td valign="top" width="185">

                    <code> **[SortCategory](amfDdsListClassSortCategoryProperty.html)** </code>

            </td>
            <td valign="top" width="452">

                    Yes</td>
              <td>Yes</td><td style="width: 81px">Yes</td><td>Yes</td>

        </tr>
<tr>
            <td valign="top" width="185">

                    <code> **[SortItems](amfDdsListClassSortItemsProperty.html)** </code>

            </td>
            <td valign="top" width="452">

                    Yes</td>
                  <td>Yes</td><td style="width: 81px">Yes</td><td>Yes</td>

        </tr>
    </tbody>
</table>

