---
title: pushKeyCursor Function

Id: amfFunctionpushKeyCursor
TocParent: amfFunctionsMainOverview
TocOrder: 60

keywords: how to, simulate key press on client-side
keywords: how to, simulate key press on client-side at cursor location
keywords: simulating key presson client-side
keywords: pushKeyCursor client-side function
keywords: client-side functions, simulating key press
keywords: client-side functions, simulating key press at cursor location
keywords: client-side functions, pushKeyCursor
keywords: form control functions, simulating key press
keywords: form control functions, pushKeyCursor
keywords: setting client-side virtual row/column of key with focus
keywords: setting client-side function key in focus
keywords: how to, set client-side virtual row/column of control with focus
keywords: how to, set client-side key in focus
keywords: setting row and column function

---

The **pushKeyCursor** function sets a string value containing the virtual row and column of the control with focus and calls the [ pushKey](amfFunctionpushKey.html) function.

#### Syntax
<pre class="prettyprint">
 **pushKeyCursor( *key* , *virtualRowCol*  )** 
          </pre>

#### Parameters
<dl>
            <dt>
 *key* 
            </dt>
            <dd>String value containing 'Enter', 'Print', 'PgUp',
        PgDn', 'Help', 'Clear', and 'F1' through 'F24'. The
        value is case sensitive. This is the
        parameter for the 
 **pushKey**  function.</dd>
            <dt>
 *virtualRowCol* 
            </dt>
            <dd>String value containing a pair of comma-separated
        integers, i.e. '2,7', representing the virtual row and
        column of the control with focus.</dd>
</dl>

#### See Also
<dl>
       <dd>[Web Functions Overview](amfFunctionsMainOverview.html)</dd></dl>

