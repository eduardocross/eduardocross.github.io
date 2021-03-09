---
title: pushKey Function

Id: amfFunctionpushKey
TocParent: amfFunctionsMainOverview
TocOrder: 50

keywords: how to, simulate key press on client-side
keywords: simulating key presson client-side
keywords: pushKeys client-side function
keywords: client-side functions, simulating key press
keywords: client-side functions, pushKey
keywords: form control functions, simulating key press
keywords: form control functions, pushKey

---

The **pushKey** function simulates a key press by calling the [ prepareSubmit](amfFunctionprepareSubmit.html) function to set the key value prior to submitting the form.

#### Syntax
<pre class="prettyprint">
 **pushKey( *key*  )** 
          </pre>

#### Parameters
<dl>
            <dt>
 *key* 
            </dt>
            <dd>String value containing 'Enter', 'Print', 'PgUp',
        PgDn', 'Help', 'Clear', and 'F1' through
        'F24'.  These values are case sensitive.</dd>
</dl>

#### Remarks
The **pushKey** function is called by [ pushKeyCursor](amfFunctionpushKeyCursor.html), [ pushKeyField](amfFunctionpushKeyField.html), and the [ pushKeyFocus](amfFunctionpushKeyFocus.html) functions.

#### See Also
<dl>
           <dd>[Web Functions Overview](amfFunctionsMainOverview.html)</dd></dl>

