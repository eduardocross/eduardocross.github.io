---
title: pushKeyField Function

Id: amfFunctionpushKeyField
TocParent: amfFunctionsMainOverview
TocOrder: 70

keywords: setting client-side field name of control with focus
keywords: setting client-side function key in focus
keywords: how to, set client-side field name of control with focus
keywords: how to, set client-side key in focus
keywords: pushKeyField client-side function
keywords: client-side functions, simulating key press
keywords: client-side functions, pushKeyField
keywords: form control functions, simulating key press
keywords: form control functions, pushKeyField

---

The **pushKeyField** function sets a string value to the field name of the control with focus and calls the [ pushKey](amfFunctionpushKey.html) function.

### Syntax
<pre class="prettyprint">
 **pushKeyField( *key* , *ddsFieldName* )** 
          </pre>

### Parameters
<dl>
            <dt>
 *key* 
            </dt>
            <dd>String value containing 'Enter', 'Print', 'PgUp',
        PgDn', 'Help', 'Clear', and 'F1' through 'F24'. The
        value is case sensitive. This is the parameter for the

 **pushKey**  function.</dd>
            <dt>
 *ddsFieldName* 
            </dt>
            <dd>String value containing the field name of the control
        with focus. The value is case sensitive.</dd>
</dl>

#### See Also
<dl>
       <dd>[Web Functions Overview](amfFunctionsMainOverview.html)</dd></dl>

