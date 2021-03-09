---
title: Conditional Properties Overview

Id: amfconConditionalPropertiesOverview
TocParent: amfASNAMonarchFrameworkConceptsMain
TocOrder: 140

keywords: ASNA.Monarch, conditional properties overview
keywords: concepts, ASNA.Monarch conditional properties overview
keywords: ASNA.Monarch, conditions
keywords: ASNA.Monarch, indicator expressions
keywords: indicator expressions
keywords: conditioning expressions
keywords: conditions
keywords: function keys, about resulting indicator
keywords: function keys, about conditions
keywords: attention keys, about resulting indicator
keywords: attention keys, about conditions
keywords: aid keys, about resulting indicator
keywords: aid keys, about conditions

---

Many of the properties of the server controls can be conditioned with an indicator expression. The conditional indicators on the DDS field or constant are migrated to the <code> **VisibleCondition** </code> property of the corresponding control. The VisibleCondition property is similar to the traditional <code> **Visible** </code> property of ASPX controls in that it determines whether the control is displayed or not. 

Note however, that the <code>Visible</code> property is of type <code>Boolean</code> while the <code>VisibleCondition</code> property is of type <code>String</code>. The string is interpreted as a Condition, an expression involving indicators and operators. The following are the syntax elements used by indicator expressions:
<dl>
      <dd> **nn**  Test for Indicator nn </dd>
        <dd>
 **&amp;**  for AND</dd>
        <dd>
 **|**  for OR</dd>
        <dd>
 **!**  for NOT</dd>
        <dd>
 **()**  to specify operator
        precedence</dd></dl>

For example, the equivalent of the following DDS sequence:
<pre class="syntax">  01   N02   03
A 04
O 05   06
O 07</pre>

Becomes this:
<pre class="example">01 &amp; !02 &amp; 03 &amp; 04 | (05 &amp; 06) | 07</pre>

The DDS control list of conditional values are given at design time but when the record is written to the file, the list is processed from start to finish evaluating the "condition" controlling the "value." As soon as a condition is met, the associated value is used for the property. Take for example the color property. It could be assigned the color <code>Red</code> if indicator 17 was on, or <code>Black</code> if not. The state of the indicators in the AVR program at the time the record is written is used to evaluate the conditional expressions. The [ Monarch Web Control Indicator Expression Tester Utility](amfMonarchWebControlIndicatorExpressionTester.html) can be used to test indicator expressions before changing properties and compiling and testing the application where the Display File is being used.

The use of parenthesis can specify an order of precedence in the evaluation of the expression. This is particularly useful when migrating DDS "Non display Attribute, <code>DSPATR(ND)</code>". Using DSPATR(ND), when the indicator expression is <code>True</code>, the control is NOT displayed. In AVR, the <code> **VisibleCondition** </code> evaluating <code>True</code> causes the control to be displayed, which is not correct in the case of the non-display attribute. Because of this, the legacy source is migrated as a negation using "!" and parenthesis around the whole indicator expression to simplify the understanding and maintenance of the migrated Display File. For example, if the above DDS sequence was applied to a non-display attribute, the migrated <code>VisibleCondition</code> would contain <code>!(01 &amp; !02 &amp; 03 &amp; 04 | (05 &amp; 06) | 07)</code>.

### Condition Expression
A ***condition*** is an expression involving indicators and operators as explained above. The special values <code> ***True** , ***False** </code>, and <code>* **None** </code> can be used in place of an indicator.
<table class="mytable" style="border-spacing: 4px" cellspacing="0" width="60%" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 10%" />
            <col span="1" style="WIDTH: 40%" />
          </colgroup>
          <tr>
            <th>Syntax</th>
            <th>Expression</th>
          </tr>
          <tr>
            <td>Example</td>
            <td> **03 &amp; !99** 
            </td>
          </tr>
          <tr>
            <td>Meaning</td>
            <td>True if *IN03 is *ON and
            *IN99 is *OFF; otherwise false.</td>
          </tr>
</table>

### Conditional Value
A ***[ Conditional Value](amfConditionalValueClass.html)*** is a *value* followed by a *colon* and then a *condition* . It is possible to omit either the Value or Condition, but not both. If necessary, the Value should be enclosed in quotes.
<table class="mytable" style="border-spacing: 4px" cellspacing="0" width="60%" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 10%" />
            <col span="1" style="WIDTH: 40%" />
          </colgroup>
          <tr>
            <th>Syntax</th>
            <th><code>Value : Condition</code></th>
          </tr>
          <tr>
            <td>Example</td>
            <td> **Red: 03 &amp; !99** 
            </td>
          </tr>
          <tr>
            <td>Meaning</td>
            <td>The value 
 **Red**  is selected if *IN03 is *ON and
            *IN99 is *OFF</td>
          </tr>
</table>

### Conditional Property
A ***[ Conditional Property](amfConditionalPropertyClass.html)*** is an array of comma separated *Conditional Values* .
<table class="mytable" style="border-spacing: 4px" cellspacing="0" width="60%" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 10%" />
            <col span="1" style="WIDTH: 40%" />
          </colgroup>
          <tr>
            <th>Syntax</th>
            <th>Conditional value,
            Conditional value, Conditional value...</th>
          </tr>
          <tr>
            <td>Example</td>
            <td> **Red : 03 &amp; !99, Green :
              06, Blue : 05 | 03** 
            </td>
          </tr>
          <tr>
            <td>Meaning</td>
            <td>The value  
 **Red**  is selected if *IN03 is *ON and
            *IN99 is *OFF
            <br clear="none" />otherwise, the value  
 **Green**  is selected if *IN06 is *ON
            <br clear="none" />otherwise, the value  
 **Blue**  is selected if *IN05 or *IN03 are
            *ON</td>
          </tr>
</table>

### Conditional Properties
Conditional properties are utilized when specific properties are set. Classes are also provided to contain these property settings.
<table class="mytable" id="Table5" style="border-spacing: 4px" cellspacing="0" width="60%" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 40%" />
          </colgroup>
          <tr>
            <th>Property</th>
            <th>Container Class</th>
          </tr>
          <tr>
            <td> [Color](amfDdsFieldClassColorProperty.html)
            </td>
            <td> [
              ColorProperty Class](amfColorPropertyClass.html)
            </td>
          </tr>
          <tr>
            <td> [
              EraseFormats](amfDdsRecordClassEraseFormatsProperty.html)
            </td>
            <td> [
              EraseProperty Class](amfErasePropertyClass.html)
            </td>
          </tr>
          <tr>
            <td> [
              ErrorMessage](amfDdsFieldClassErrorMessageProperty.html)
            </td>
            <td> [
              ErrMsgProperty Class](amfErrMsgPropertyClass.html)
            </td>
          </tr>
          <tr>
            <td> [
              ErrorMessageId](amfDdsFieldClassErrorMessageIdProperty.html)
            </td>
            <td> [
              ErrMsgIdProperty Class](amfErrMsgIdPropertyClass.html)
            </td>
          </tr>
          <tr>
            <td> [
              MessageId](amfDdsDataFieldClassMessageIdProperty.html)
            </td>
            <td> [
              MsgIdProperty Class](amfMsgIdPropertyClass.html)
            </td>
          </tr>
          <tr>
            <td> [
              SubfileMessage](amfddsSubfileControlClassSubfileMessageProperty.html)
            </td>
            <td> [
              ErrMsgProperty Class](amfErrMsgPropertyClass.html)
            </td>
          </tr>
          <tr>
            <td> [
              SubfileMessageId](amfddsSubfileControlClassSubfileMessageIdProperty.html)
            </td>
            <td> [
              ErrMsgIdProperty Class](amfErrMsgIdPropertyClass.html)
            </td>
          </tr>
</table>

### Attention Keys and Function Keys
In addition to the properties above, a special note must be made regarding **AttnKeys** and **FuncKeys** properties. These properties may be set once for the file, [DdsFile.AttnKeys](amfDdsFileClassAttnKeysProperty.html) and [ DdsFile.FuncKeys](amfDdsFileClassFuncKeysProperty.html), and once for the record, [DdsRecord.AttnKeys](amfDdsRecordClassAttnKeysProperty.html) and [ DdsRecord.FuncKeys](amfDdsRecordClassFuncKeysProperty.html). The keys aggregate across record formats active on the file when going to the browser.

These keys must be declared as part of each DdsFile, DdsRecord, or DdsSubfile where they are used in addition to being called by DdsButtons or similar controls.

AttnKeys and FuncKeys properties are semi-colon separated arrays representing:
<pre>       FKEY 'Text' Conditional Property </pre>

Where FKEY is the function key, 'Text' is an optional description for the key, and Conditional Property is as described above or the special value <code>*NONE</code>. For instance, the following are two valid examples.
<pre class="example">F3 'Add'; F4 'Delete'

F3 'Add' 07:!99 ; F4 'Delete' *NONE:09</pre>

### Subtopic: [Monarch Web Control Indicator Expression Tester Utility](amfMonarchWebControlIndicatorExpressionTester.html)

#### Next: [Monarch Framework ASPX Session Overview](amfconFrameworkASPXSessionOverview.html)

#### Previous: [Overview of AidKeys](amfconOverviewofAidKeys.html)

#### See Also
<dl>
      <dd>[ConditionalValue Class](amfConditionalValueClass.html)</dd>
      <dd>[ConditionalProperty Class](amfConditionalPropertyClass.html)</dd>
      <dd>[KeyProperty Class](amfKeyPropertyClass.html)</dd>
      <dd>[DdsRecord Class](amfDdsRecordClass.html)</dd>
      <dd>[DdsFile Class](amfDdsFileClass.html)</dd>
</dl>

