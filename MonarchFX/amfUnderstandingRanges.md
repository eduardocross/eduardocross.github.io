---
title: DdsDecRange Controls

Id: amfUnderstandingRanges
TocParent: amfASNAMobileSupport
TocOrder: 77

keywords: ASNA Range Control
keywords: ASNA slider Control
keywords: ASNA number picker Control
keywords: ASNA Mobile RPG, Range
keywords: ASNA Mobile, DdsDecRange
keywords: Mobile Signatures

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span></td>
			    </tr>
</table>

# DdsDecRange Controls

### What is a DdsDecRange?
A [DdsDecRange control](amfDdsDecRangeClass.html) is used to create an on-screen control that allows users to select from a range of numbers in a variety of ways, including typing into a box, increasing or decreasing using "step" buttons, or by moving a slider.<br/> 

**Applicability:** These controls can be used in Monarch, Wings, and Mobile RPG pages/apps.

### The Mechanics of a DdsDecRange
The DdsDecRange control is, from the standpoint of the IBM i, a normal decimal field. The control allows the user to decide which numeric value goes into the field, and its main role is presenting simple, mobile-friendly ways to do that.

DdsDecRange currently supports two modes of input:

- Step buttons
- Slider

#### Step buttons
![](Images/DecRangeButtons.png)

If the [InteractionStyle](amfddsdecrangeclassInteractionStyleProperty.html) property is <code>Buttons</code>, minus (-) and plus (+) buttons will appear allowing users to step through regular numerical values in units defined by the [Steps](amfddsdecrangeclassStepsProperty.html) property (often 1.0, 5.0, or 10.0).

#### Slider
![](Images/DecRangeSlider1.png)

If the [InteractionStyle](amfddsdecrangeclassInteractionStyleProperty.html) property is <code>Slider</code>, users will see a mobile-friendly slider that will allow them to adjust the numeric value to anything from [Min](amfddsdecrangeclassMinProperty.html) to [Max](amfddsdecrangeclassMaxProperty.html) in increments set by the [Steps](amfddsdecrangeclassStepsProperty.html) property. If the [NumericValueStyle](amfddsdecrangeclassNumericValueStyleProperty.html) is set to <code>Right</code> (shown below) or <code>Left</code> a visible field holding the number will be displayed in the appropriate location.

![](Images/DecRangeSlider2.png)
![](Images/DdsDecRangeTasks.png)

### DdsDecRange Property Tasks
<table class="TaskTable" border="1" cellspacing="0" cellpadding="0" width="637">
	  <tbody>
          <colgroup>
           <col width="30%" />
           <col width="70%" />
          </colgroup>
          <tr><th>Property</th>
          <th>Description</th>
          </tr>
		<tr>
            <td colspan="2" valign="top" width="185">

**Behavior** 
</td>
        </tr>
		<tr>
            <td> <code> **[InteractionStyle](amfDdsDecRangeClassInteractionStyleProperty.html)** </code>
            </td>
            <td>Specifies the interaction style for the DdsDecRange control: Slider or Buttons</td>
          </tr>
		<tr>
			<td> <code> **[NumericValueStyle](amfDdsDecRangeClassNumericValueStyleProperty.html)** </code>
            </td>
            <td>(Required) The actual numeric value.</td>
        </tr>
		<tr>
            <td colspan="2" valign="top" width="185">

**Data** 
</td>
        </tr>
		        <tr>
			<td> <code> **[Alias](amfDdsDecRangeClassAliasProperty.html)** </code>
            </td>
            <td>(Required) Tthe field name for the compiler to use for externally described files.</td>
        </tr>
	 <tr>
			<td> <code> **[Type](amfDdsDecRangeClassTypeProperty.html)** </code>
            </td>
            <td>(Required) Tthe field name for the compiler to use for externally described files.</td>
        </tr>
        <tr>
			<td> <code> **[Length](amfDdsDecRangeClassLengthProperty.html)** </code>
            </td>
            <td>(Required) The length of the field (in characters), as seen by the IBM i.</td>
        </tr>
		<tr>            
		    <td> <code> **[Decimals](amfDdsDecRangeClassDecimalsProperty.html)** </code></td>
            <td>Sets the number of decimal places for the Numeric Value.</td>
          </tr>
		<tr>
            <td colspan="2" valign="top" width="185">

**Layout** 
</td>
        </tr>
		<tr>
	<td valign="top" width="169">
 **<code><a href="http://msdn.microsoft.com/en-us/library/system.web.ui.webcontrols.webcontrol.height(v=vs.110).aspx">Height</a>
		 &amp; <br /><a href="http://msdn.microsoft.com/en-us/library/system.web.ui.webcontrols.webcontrol.width(v=vs.110).aspx">Width</a></code>** 
	</td>
	<td valign="top" width="468">
		These properties set the height and width of the control in whichever unit is specified (pixels, by default).</td>
</tr>
</tbody>  
</table>

