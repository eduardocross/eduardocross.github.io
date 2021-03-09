---
title: Monarch Web Control Indicator Expression Tester

Id: amfMonarchWebControlIndicatorExpressionTester
TocParent: amfconConditionalPropertiesOverview
TocOrder: 10

keywords: monarch web control indicator expression tester dialog
keywords: ASNA Monarch, web control indicator expression tester
keywords: concepts, ASNA Monarch web control indicator expression tester
keywords: ASNA Monarch, conditional values
keywords: ASNA Monarch, indicator expressions
keywords: ASNA Monarch, testing indicator expressions
keywords: indicator expressions
keywords: testing indicator expressions
keywords: Color property, testing indicator expression
keywords: Color Property Editor, testing indicator expression
keywords: ErrorMessageId property, testing indicator expression
keywords: ErrorMessageID Property Editor, testing indicator expression
keywords: ErrorMessage property, testing indicator expression
keywords: ErrorMessage Property Editor, testing indicator expression
keywords: EraseFormats property, testing indicator expression
keywords: EraseFormats Property Editor, testing indicator expression
keywords: MessageId property, testing indicator expression
keywords: MessageID Property Editor, testing indicator expression
keywords: SubfileMessage property, testing indicator expression
keywords: SubfileMessage Property Editor, testing indicator expression
keywords: SubfileMessageId property, testing indicator expression
keywords: SubfileMessageID Property Editor, testing indicator expression
keywords: ClearRecords property, testing indicator expression
keywords: DisplayFields property, testing indicator expression
keywords: DisplayRecords property, testing indicator expression
keywords: InitializeRecords property, testing indicator expression
keywords: VisibleCondition property, testing indicator expression
keywords: FuncKeys property, testing indicator expression
keywords: AttnKeys property, testing indicator expression
keywords: available aid keys, testing expression indicators
keywords: aidkeys, testing expression indicators
keywords: Aid Property Dialog, testing expression indicators

---

Many of the properties of the server controls can be conditioned with an indicator expression that may be challenging for the migrator to master. The syntax is a one-line free-form expression that uses the following symbols:
<dl>
        <dd>
 **&amp;**  for AND</dd>
        <dd>
 **|**  for OR</dd>
        <dd>
 **!**  for NOT</dd>
        <dd>
 **()**  to specify operator
        precedence</dd>
</dl>

A ***condition*** is an expression involving indicators and operators. The special values ***True** , ***False** , and * **None** can be used in place of an indicator. To test an expression, the **Indicator Expression Tester** can be used. This utility, called **"WebDspfExpr.exe"** , is located in the same folder where Monarch was installed. Using this utility, the migrator can experiment with indicator expressions to get the desired result before changing the properties and compiling and testing the application where the Display File is being used. This tool can also be used during training to teach the use of Monarch properties with indicator expression syntax.

To use the tool, the checkboxes represent the state of the 99 indicators where checked means *True (on) and unchecked means *False (off). You enter an expression and click the " **Evaluate** " button to see the result. Any runtime exceptions that may be thrown due to an invalid expression are shown in the textbox at the bottom of the dialog box.
<dl>
          <dd>![Monarch Web Control Indicator Expression Tester](../Images/zzIndicatorExpressionTester.JPG) </dd>
</dl>

#### Next: [Monarch Framework ASPX Session Overview](amfconFrameworkASPXSessionOverview.html)

#### Previous: [ ConditionalValue Class](amfconConditionalPropertiesOverview">Conditional Properties Overview</a>

#### See Also
<a href="amfConditionalValueClass.html) <br /> [ ConditionalProperty Class](amfConditionalPropertyClass.html) <br />[Conditional Properties Overview](amfconConditionalPropertiesOverview.html)

---

