---
title: SetFocusAt Function

Id: amfFunctionSetFocusAt
TocParent: amfFunctionsMainOverview
TocOrder: 90

keywords: setFocusAt function
keywords: functions, setFocusAt
keywords: display file web controls, setFocusAt
keywords: web server control functions, setFocusAt
keywords: form control functions, setFocusAt
keywords: web server controls, setFocusAt
keywords: how to, set record name of control with focus
keywords: how to, set field name of control with focus
keywords: how to, set virtual row/column of control with focus
keywords: setFocusAt, set record name
keywords: setFocusAt, field name
keywords: setFocusAt, virtual row/column

---

The **SetFocusAt** function sets a string value to the virtual row and column of the control with focus and calls the [ SetFocusAtFR](amfFunctionSetFocusAtFR.html) function.

#### Syntax
<pre class="prettyprint">
 **SetFocusAt( *ddsFieldName* , *virtualRowCol* , *ddsRecName* )** 
          </pre>

#### Parameters
<dl>
            <dt>
 *ddsFieldName* 
            </dt>
            <dd>String value containing the field name of the control
        with focus. The value is case sensitive. This is the
        parameter for the 
 **SetFocusAtFR**  function. </dd>
            <dt>
 *virtualRowCol* 
            </dt>
            <dd>String value containing a pair of comma-separated
        integers, i.e. '2,7' representing the virtual row and
        column of the control with focus.</dd>
            <dt>
 *ddsRecName* 
            </dt>
            <dd>String value containing the record name of the control
        with focus. The value is case sensitive. This is the
        parameter for the 
 **SetFocusAtFR**  function.</dd>
</dl>

#### Remarks
**SetFocusAt** is also called by the [ pushKeyFocus](amfFunctionpushKeyFocus.html) function.

#### See Also
<dl>
      <dd>[Web Functions Overview](amfFunctionsMainOverview.html)</dd></dl>

