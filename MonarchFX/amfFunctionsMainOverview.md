---
title: Web Functions Overview

Id: amfFunctionsMainOverview
TocParent: amfWebDspFNamespace
TocOrder: 80

keywords: prepareSubmit client-side function
keywords: pushKey client-side function
keywords: pushKeyCursor client-side function
keywords: pushKeyField client-side function
keywords: pushKeyFocusAt client-side function
keywords: pushKeyFocusAtFR client-side function
keywords: setFocusAt client-side function
keywords: setFocusAtFR client-side function
keywords: shutdown client-side function
keywords: client-side functions, simulating key press
keywords: client-side functions, prepareSubmit
keywords: client-side functions, pushKey
keywords: client-side functions, pushKeyCursor
keywords: client-side functions, pushKeyField
keywords: client-side functions, pushKeyFocusAtFR
keywords: client-side functions, pushKeyFocusAt
keywords: client-side functions, setFocusAtFR
keywords: client-side functions, setFocusAt
keywords: client-side functions, shutdown
keywords: client-side functions, isBrowserClosing
keywords: client-side events, onBrowserClose
keywords: client-side functions, shutdown
keywords: form control functions, simulating key press
keywords: form control functions, prepareSubmit
keywords: form control functions, pushKey
keywords: form control functions, pushKeyCursor
keywords: form control functions, pushKeyField
keywords: form control functions, pushKeyFocusAtFR
keywords: form control functions, pushKeyFocusAt
keywords: form control functions, setFocusAtFR
keywords: form control functions, setFocusAt
keywords: form control functions, isBrowserClosing
keywords: form control events, onBrowserClose
keywords: form control functions, shutdown

---

There may be situations where you want to return control to the program by simulating a key press programmatically. This ultimately controls subsequent processing of the form. This topic provides a list of the JavaScript functions to accomplish this control.

### Functions
In the list below, parameters are shown in ** *bold/italics* ** and refer to the hyperlink for more detail.

1. <code>[
          prepareSubmit](amfFunctionprepareSubmit.html)</code>
<dl>
                <dd>Sets the value for the
 ** *key* **  press.</dd>
</dl>
2. <code>[pushKey](amfFunctionpushKey.html)</code>
<dl>
                <dd>Calls 
            <code>[
          prepareSubmit](amfFunctionprepareSubmit.html)</code></dd>
                <dd>Submits the form</dd>
</dl>
3. <code>[
          pushKeyCursor](amfFunctionpushKeyCursor.html)</code>
<dl>
                <dd>Sets a string value containing a pair of
            comma-separated integers representing the virtual 
 ***row/column***  of the control with focus</dd>
                <dd>Calls 
            <code>[pushKey](amfFunctionpushKey.html)</code></dd>
</dl>
4. <code>[
          pushKeyField](amfFunctionpushKeyField.html)</code>
<dl>
                <dd>Sets a string value containing the 
 ***field name***  of the control with focus</dd>
            <dd>Calls 
            <code>[pushKey](amfFunctionpushKey.html)</code></dd>
</dl>
5. <code>[
          SetFocusAtFR](amfFunctionSetFocusAtFR.html)</code>
<dl>
            <dd>Sets string values containing the 
 ***field name***  and the 
 ***record format name***  of the control with focus</dd>
</dl>
6. <code>[
          SetFocusAt](amfFunctionSetFocusAt.html)</code>
<dl>
                <dd>Sets a string value containing a pair of
            comma-separated integers representing the virtual 
 ** *row/column* **  of the control with focus</dd>
                <dd>Calls 
           [
          SetFocusAtFR](amfFunctionSetFocusAtFR.html)</dd>
</dl>
7. <code>[
          pushKeyFocus](amfFunctionpushKeyFocus.html)</code>
<dl>
                <dd>Calls 
            <code>[
          SetFocusAt](amfFunctionSetFocusAt.html)</code></dd>
                <dd>Calls 
            <code>[pushKey](amfFunctionpushKey.html)</code></dd>
</dl>

The ***key*** value referenced above can contain Enter, Print, PgUp, PgDn, Help, Clear, and F1 through F24. All parameter values are case sensitive.

In addition, two JavaScript functions are used for control of the [shutdown process](amfFunctionsShuttingDown.html). They are <code> **isBrowserClosing()** </code> and <code> **onBrowserClose()** </code>.

#### See Also
<dl>
        <dd>[Web
        Server Controls Overview](amfWebServerControlsOverview.html)</dd>
        <dd>[
        ASNA.Monarch.WebDspF Class Library](amfWebDspFClassLibraryMain.html)</dd>
<dd>[
        ASNA.Monarch.WebDspF Enumerations](amfWebDspFEnumerations.html)</dd>
</dl>

