---
title: SetFocusAtFR Function

Id: amfFunctionSetFocusAtFR
TocParent: amfFunctionsMainOverview
TocOrder: 100

keywords: setFocusAtFR function
keywords: functions, setFocusAtFR
keywords: display file web controls, setFocusAtFR
keywords: web server control functions, setFocusAtFR
keywords: form control functions, setFocusAtFR
keywords: web server controls, setFocusAtFR
keywords: how to, set record name of control with focus
keywords: how to, set field name of control with focus
keywords: setFocusAtFR, set record name
keywords: setFocusAtFR, field name

---

The **SetFocusAtFR** function sets string values for the field name and record name to those of the control with focus.

#### Syntax
<pre class="prettyprint">
 **SetFocusAtFR( *ddsFieldName* , *ddsRecName* )** 
          </pre>

#### Parameters
<dl>
            <dt>
 *ddsFieldName* 
            </dt>
            <dd>String value containing the field name of the control
        with focus. The value is case sensitive.</dd>
            <dt>
 *ddsRecName* 
            </dt>
            <dd>String value containing the record name of the control
        with focus. The value is case sensitive.</dd>
</dl>

#### Remarks
**SetFocusAtFR** is also called by the [ SetFocusAt](amfFunctionSetFocusAt.html) function.

#### See Also
<dl><dd>[Web
      Functions Overview](amfFunctionsMainOverview.html)</dd></dl>

