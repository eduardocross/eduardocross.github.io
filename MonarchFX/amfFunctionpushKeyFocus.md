---
title: pushKeyFocus Function

Id: amfFunctionpushKeyFocus
TocParent: amfFunctionsMainOverview
TocOrder: 80

keywords: setting client-side record name of control with focus
keywords: setting client-side field name of control with focus
keywords: setting client-side virtual row/column of control with focus
keywords: setting client-side function key in focus
keywords: how to, set client-side record name of control with focus
keywords: how to, set client-side field name of control with focus
keywords: how to, set client-side virtual row/column of control with focus
keywords: how to, set client-side function key in focus
keywords: pushKeyFocus client-side function
keywords: client-side functions, simulating key press
keywords: client-side functions, pushKeyFocus
keywords: form control functions, simulating key press
keywords: form control functions, pushKeyFocus

---

**The pushKeyFocus** function calls the [ SetFocusAt](amfFunctionSetFocusAt.html) function (sets ** *row/column* ** ), which calls the SetFocusAtFR function (sets ** *field name* ** and ***record format name*** ) and then calls the [ pushKey](amfFunctionpushKey.html) function, which calls [ prepareSubmit](amfFunctionprepareSubmit.html) (sets ***key*** value) before submitting the form.

#### Syntax
<pre class="prettyprint">
 **pushKeyFocus( *key* , *ddsFieldName* , *virtualRowCol* , *ddsRecName*  )** 
          </pre>

#### Parameters
<dl>
            <dt>
 *key* 
            </dt>
            <dd>String value containing 'Enter', 'Print', 'PgUp',
        PgDn', 'Help', 'Clear', and 'F1' through 'F24'. The
        value is case sensitive. This is the parameter for the

 **prepareSubmit**  function.</dd>
            <dt>
 *ddsFieldName* 
            </dt>
            <dd>String value containing the field name of the control
        with focus. The value is case sensitive. This is the
        parameter for the 
 **SetFocusAtFR**  function.</dd>
            <dt>
 *virtualRowCol* 
            </dt>
            <dd>String value containing a pair of comma-separated
        integers, i.e. '2,7' representing the virtual row and
        column of the control with focus. This is the
        parameter for the 
 **SetFocusAt**  function.</dd>
            <dt>
 *ddsRecName* 
            </dt>
            <dd>String value containing the record name of
        the control with focus. The value is case sensitive.
        This is the parameter for the 
 **SetFocusAtFR**  function.</dd>
</dl>

#### See Also
<dl>
          <dd>[Web Functions Overview](amfFunctionsMainOverview.html)</dd></dl>

