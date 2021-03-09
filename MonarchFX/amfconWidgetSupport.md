---
title: Widget Support

Id: amfconWidgetSupport
TocParent: amfASNAMonarchFrameworkConceptsMain
TocOrder: 110

keywords: ASNA SelectionField Control
keywords: ASNA Widgets, SelectionFields
keywords: ASNA Widgets, DdsSelectionFields
keywords: ASNA Widgets, SingleChoiceSelectionFields
keywords: ASNA Widgets, DdsSingleChoiceSelectionFields
keywords: Widget SelectionFields
keywords: ASNA Widgets, MultipleChoiceSelectionFields
keywords: ASNA Widgets, DdsMultipleChoiceSelectionFields
keywords: Widget SelectionFields
keywords: ASNA PushButtonField Control
keywords: ASNA Push Button Field Control
keywords: ASNA Push Button Control
keywords: PushButtonFields

---

### What is a DdsSelectionField?
As of version 8.0 Monarch and Wings have added support for the <code>PSHBTNFLD</code>, <code>SNGCHCFLD</code>, and <code>MLTCHCFLD</code> widgets. This has been implemented with controls generically referred to as "DdsSelectionFields", which can refer to any one of three controls (and their required child controls):

- [MultipleChoiceSelectionField](amdDdsMultipleChoiceSelectionFieldCLass.html)
- [SingleChoiceSelectionField](amdDdsSingleChoiceSelectionFieldCLass.html)
<ul>
<li>[SelectionFieldChoice](amdDdsSelectionFieldChoiceClass.html)

</li>
<li>[PushButtonField](amdDdsPushButtonFieldClass.html)

- [PushButtonFieldChoice](amdDdsPushButtonFieldChoiceClass.html)

</li>
</ul>

<code>SelectionFieldChoice</code> is used by both <code>MultipleChoiceSelectionField</code> and <code>SingleChoiceSelectionField</code>.

**Applicability:** These controls can be used in Monarch and Wings pages.

### The Mechanics of a DdsSelection Field
Selection fields are designed to smoothly take the green-screen <code>MLTCHCFLD</code>, <code>SNGCHCFLD</code>, and <code>PSHBTNFLD</code> keywords and migrate or modernize them one-for-one into .NET controls. Each widget is migrated to a selection field, and each option within those widgets is converted to a "Choice" control. From there the controls can be readily styled by the developer.

The <code>VirtualRowCol</code> property is the Monarch mechanism by which the Display file (ASPX) reports the "legacy" cursor position to the "legacy" RPG code. During migration, Monarch Cocoon saves the legacy cursor location where DDS keywords were specified. Even if the Web control is repositioned (in the graphical world), this property may remain unchanged with its row, column green-screen positions, so that when the page submits, the "Displayfile Controller" may "simulate" that the input element was at a particular (row, col) "cursor" position, and the RPG logic may test for it.

The "green-screen" display file controller, can report the real "cursor position", independent of how things were designed in DDS (the video hardware has the precise row, col or the cursor when Enter of FKey was pressed). For Monarch is more challenging, it can determine which HTML element had the "pointer" (mouse, caret or Tap), and from there it can retrieve the stored legacy row, col (<code>VirtualRowCol</code>).

To ensure the proper placement of the controls, the <code>VirtualRowCol</code> property is associated with each <code>SelectionFieldChoice</code> or <code>PushButtonFieldChoice</code>. It is more precise to have one <code>VirtualRowCol</code> per choice in the group than one for the entire group. Note that Monarch Displayfile Migration Agent will "estimate" the <code>VirtualRowCol</code> values: The developer may need to adjust these values. This manual "remediation" will only be required if the RPG is using the "feedback" area, where the cursor position is reported back to the RPG program. It is uncommon that developers use cursor position information alongside these Widgets, since they provide a better mechanism (the "choice-number" value), but the <code>VirtualRowCol</code> is introduced to account for those scenarios.

#### Styling DdsPushButtonField
There are various ways to improve the style of <code>DdsPushButtonFieldChoice</code>(s), for example by going from the default:

![](images/PushbuttonDefault.png)

To a better looking rendering:

![](images/PushbuttonImproved.png)

You can set the "<code>cssClass</code>" property of the <code>DdsPushButtonFieldChoice</code>(s) to a particular style, like "<code>TwelveButtons</code>": <p>1. Define a new CSS style in: <code>&lt;my website path&gt;\Themes\Current\Styles\Theme.css</code>, like:
<pre class="prettyprint"><code class="CSS">
      .TwelveButtons {
         width: 100px;
         margin-bottom: 5px;
         cursor: pointer;
         background-color: white;
         border-style: solid;
         border-color: antiquewhite;
      }
</code></pre>

2. Set the property "CssClass" of each of the DdsPushButtonFieldChoice web control instances (for example, notice highlight)
<pre class="prettyprint"><code class="C#">
&lt;mdf:DdsPushButtonField id="DdsPushButtonField2" runat="server" style="position: absolute; left: 20px; top: 360px; width: 19px"
   CssClass="DdsPushButtonField"
   Alias="FUNKEY3" 
   Usage="Both" 
   TabIndex="6" 
   Gutter="20px"
   Rows="3"
   EnabledChoiceColor="Orange"
   EnabledChoiceStyle="Bold"
&gt;
   &lt;mdf:DdsPushButtonFieldChoice id="TWELVE_001" runat="server" 
      ChoiceNumber="1"
      ChoiceText="One"
      CssClass="TwelveButtons"
   /&gt;
   &lt;mdf:DdsPushButtonFieldChoice id="TWELVE_002" runat="server" 
      ChoiceNumber="2"
      ChoiceText="Two"
      CssClass="TwelveButtons"
   /&gt;
   .
   . 
   . 
</code></pre>

#### Styling DdsSingle or MultipleChoiceSelectionFields
As with <code>DdsPushButtonFieldChoice</code> there are numerous ways to improve on the default appearance of a selection field.

One CSS style that works here is:
<pre class="prettyprint"><code class="CSS">
.TwelveRadioButtons, .TwelveCheckboxes {
   line-height: 30px;
   cursor: pointer;
}
</code></pre>
</p>

Note: In these cases we want to increase the "line-height" as opposed to changing the "margin-bottom"

SingleChoice Before:

![](SingleChoiceSelectionBefore.png)

After:

![](SingleChoiceSelectionAfter.png)

MultipleChoice Before:

![](MultipleChoiceSelectionBefore.png)

After:

![](MultipleChoiceSelectionAfter.png)
![](Images/DdsSingleChoiceSelectionFieldTasks.png)

### DdsSelectionField Property Tasks
The property tasks are identical for SingleChoiceSelectionField, MultipleChoiceSelectionField, and PushButtonField).
<table class="TaskTable" border="1" cellspacing="0" cellpadding="0" width="637">
	  <tbody>
          <colgroup>
           <col width="30%" />
           <col width="70%" />
          </colgroup>
          <tr><th>Property</th>r
          <th>Description</th>
          </tr>
		<tr>
            <td colspan="2" valign="top">

**Appearance** 
</td>
        </tr>
<tr>
            <td><code> **[
              Gutter](amfDdsSingleChoiceSelectionFieldClassGutterProperty.html)** </code>
            </td>
            <td>Sets the spacing between columns (in pixels).</td>
          </tr>
<tr>
    <td><code> **[
              Columns](amfDdsSingleChoiceSelectionFieldClassColumnsProperty.html)** </code>
            </td>
            <td>Sets the number of columns to display choices in.</td>
          </tr>
<tr>
    <td><code> **[
              Rows](amfDdsSingleChoiceSelectionFieldClassRowsProperty.html)** </code>
            </td>
            <td>	Sets the number of rows to display choices in (defaults to 999).</td>
          </tr>
<tr>
    <td><code> **[
              EnabledChoiceColor](amfDdsSingleChoiceSelectionFieldClassEnabledChoiceColorProperty.html)** </code>
            </td>
            <td>Sets a color to identify enabled choices with.</td>
          </tr>
<tr>
    <td><code> **[
              EnabledChoiceStyle](amfDdsSingleChoiceSelectionFieldClassEnabledChoiceStyleProperty.html)** </code>
            </td>
            <td>Sets a style to identify enabled choices with.</td>
          </tr>
<tr>
    <td><code> **[
              DisabledChoiceColor](amfDdsSingleChoiceSelectionFieldClassDisabledChoiceColorProperty.html)** </code>
            </td>
            <td>Sets a color to identify disabled choices with.</td>
          </tr>
<tr>
    <td><code> **[
              DisabledChoiceStyle](amfDdsSingleChoiceSelectionFieldClassDisabledChoiceStyleProperty.html)** </code>
            </td>
            <td>Sets a style to identify disabled choices with.</td>
          </tr>
		<tr>
            <td colspan="2" valign="top" width="185">

**Behavior** 
</td>
        </tr>

<tr>
            <td><code> **[
              Protect](amfDdsDataFieldClassProtectProperty.html)** </code>
            </td>
            <td>Protects Selection Field from user interaction. (Inherited from 
			DdsDataField.)</td>
          </tr>
<tr>
            <td> <code> **[Usage](amfDdsDataFieldClassUsageProperty.html)** </code>
            </td>
            <td>Specifies if this field is output-only, input-only (both), or hidden. (Inherited from DdsDataField.)</td>
          </tr>
		  <tr>
            <td> <code> **[VisibleCondition](amfDdsDataFieldClassVisibleConditionProperty.html)** </code>
            </td>
            <td>Gets or sets the RPG indicator expression that, when evaluated, determines if the tableshould be visible. (Inherited from DdsField.)</td>
          </tr>
		  <tr>
            <td> <code> **[Protect](amfDdsRecordClassProtectProperty.html)** </code>
            </td>
            <td>Gets or sets an indicator expression (or *True) which determines whether the fields in this record are protected.</td>
          </tr>
		<tr>
            <td colspan="2" valign="top" width="185">

**External Description** 
</td>
        </tr>
		<tr>
            <td> <code> **[Choices](amfDdsDataFieldClassChoicesProperty.html)** </code>
            </td>
            <td>Sets the available choices via a Collection of DdsSelectionFieldChoice controls.</td>
          </tr>
		<tr>
            <td> <code> **[Alias](amfDdsDataFieldClassAliasProperty.html)** </code>
            </td>
            <td>Field name to be used by compiler for externally described files</td>
          </tr>
</tbody>
</table>

