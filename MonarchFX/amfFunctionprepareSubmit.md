---
title: prepareSubmit Function

Id: amfFunctionprepareSubmit
TocParent: amfFunctionsMainOverview
TocOrder: 40

keywords: display file web controls, prepareSubmit
keywords: web server control functions, prepareSumbit
keywords: form control functions, simulating key press
keywords: web server controls, prepareSubmit
keywords: how to, simulate key presss
keywords: prepareSumbit, simulating key press
keywords: prepareSubmit function
keywords: functions, prepareSubmit
keywords: simulating key press function

---

The **prepareSubmit** function sets the value of the key press.

### Syntax
<pre class="prettyprint">
 **prepareSubmit( *key*  )** 
          </pre>

### Parameters
<dl>
            <dt>
 *key* 
            </dt>
            <dd>String value containing Enter, Print, PgUp,
        PgDn, Help, Clear, and F1 through F24.  This value is case sensitive.</dd>
</dl>

### Remarks
This function is called by the [ pushKey](amfFunctionpushKey.html) function prior to submitting the form.
<dl>
      <dd>

#### See Also
[Web Functions Overview](amfFunctionsMainOverview.html)</dd></dl>

