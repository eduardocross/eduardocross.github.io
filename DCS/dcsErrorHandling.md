---
title: Error Handling

Id: dcsErrorHandling
TocParent: dcsProgrammersGuideMain
TocOrder: 5

keywords: errors, handling
keywords: handling errors

---

In client/server environments such as the ASNA DataGate Component suite (DCS) runtime, certain exceptions can occur that the programmer may wish to allow the program to recover from. For example, suppose that the network between your program (the client) and the database (the server) is disrupted. Instead of crashing or reporting the error and exiting, you could allow the user to try the procedure again when the network has been restored.

Exceptions specific to the DataGate provider being accessed by DCS are communicated through [dgException](dcsdgExceptionClass.html). Most often, these exceptions are in the form of a condition identifier and a text message provided by [Error](dcsdgExceptionClassErrorField.html) field and [Message](dcsdgExceptionClassMessageProperty.html) property respectively.

The [ErrorClass](dcsdgExceptionClassErrorClassField.html) field classifies the condition identifier as one of the categories given by the [dgErrorClass](dcsdgErrorClassEnumeration.html) enumeration. The [SystemError](dcsdgExceptionClassSystemErrorField.html) field contains a provider-dependent exception identifier for certain exceptions. Likewise, the [Text](dcsDisconnectingfromaDatabase.html) field may contain text messages given by the underlying database for the exception.

DCS throws other exceptions besides dgException. Please see the documentation for the particular DCS object or method call for a description of the exceptions thrown.

dgException inherits from System.Exception. System.Exception provides many useful functions for diagnosing and reporting bugs in your code and DCS.

A reference to all DCS error codes is provided in the documentation. Note that DCS may report its own error codes as specified by the type library’s [ dgErrorNumber](dcsdgErrorNumberEnumeration.html) enumeration.

Visual Basic also provides special constructs for handling class object errors. In particular, the "On Error" statement is highly effective for handling DCS object errors. Like Visual RPG, Visual Basic provides a global Err object, providing error number, description, and other error details. Again, most ActiveX development environments do provide options for handling DCS’s standard COM exceptions.
<pre>        <span class="lang">
 **[C#]** 
        </span>
using System;
using System.Data;
using System.Windows.Forms;
using ASNA.DataGate.Client;
using ASNA.DataGate.Common;

namespace NetworkRecovery 
{
      public class Form1 | System.Windows.Forms.Form
      {
          const string srcStr = "asna network database";
          private System.Windows.Forms.Button button1;
          private System.ComponentModel.Container components = null;

          public Form1()...
          protected override void Dispose( bool disposing )...
          #region Windows Form Designer generated code
               ...Designer code omitted...
          #endregion
          [STAThread]
          static void 
<place>Main</place>()...
          private void button1_Click(object sender, System.EventArgs e)
          {
                AdgConnection cx = new AdgConnection(srcStr);
                bool retry = false;
                Cursor origCursor = Cursor.Current;
                // enter the "retry" loop
                do
                {
                    try
                    {
                        retry = false;
                        Cursor.Current = Cursors.WaitCursor; // hourglass
                        cx.Open();   // this will throw dgException if errors occur
                    }
                    catch ( dgException ex )
                    {
                        string mbMsg = ex.Message;
                        // check for error indicating "service not running"
                        if ( ex.Error == dgErrorNumber.dgEiNORESPONSE )

                            mbMsg = "Cannot connect to " + srcStr + 
                                                ".  Is the service running?"; 
                        // check for error indicating "network down"
                        else if ( ex.Error == dgErrorNumber.dgEiCONNLOST ||
                                  ex.Error == dgErrorNumber.dgEiHOSTNOTFND )
                            mbMsg = "Cannot connect to " + srcStr + 
                                                ".  Is the network available?";
                        DialogResult dr = MessageBox.Show( mbMsg,
                                        "Database Provider Unavailable",
                                         MessageBoxButtons.RetryCancel,
                                         MessageBoxIcon.Hand,
                                         MessageBoxDefaultButton.Button1,
                                         0 );
                        if ( dr == DialogResult.Retry )
                            retry = true;
                    }
                    finally
                    {
                        Cursor.Current = origCursor;
                    }
                } while (retry == true);
               // In this simple example, just check the connection state and quit
                if ( cx.State == ConnectionState.Open )
                    MessageBox.Show( "Connected!" );
                Close();
          }
      }</pre>
      <br />
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
Imports ASNA.DataGate.Client
Imports ASNA.DataGate.Common
Public Class Form1
    Inherits System.Windows.Forms.Form
Const srcStr As String = "asna network database"
#Region " Windows Form Designer generated code "
      ...Designer code omitted...
#End Region
    Private Sub btnConnect_Click(ByVal sender As System.Object, _
                                 ByVal e As System.EventArgs) _
                   Handles btnConnect.Click
        Dim cx As AdgConnection = New AdgConnection(srcStr)
        Dim retry As Boolean
        Dim origCursor As Cursor = Cursor.Current
        ' enter the "retry" loop
        Do
            Try
                retry = False
                Cursor.Current = Cursors.WaitCursor ' hourglass
                cx.Open()   ' this will throw dgException if errors occur
            Catch ex As dgException
                Dim dr As DialogResult = DialogResult.Abort
                ' check for error indicating "service not running"
                If (ex.Error = dgErrorNumber.dgEiNORESPONSE) Then
                    dr = MessageBox.Show("Cannot connect to " + srcStr + _
                         ".  Is the service running?", _
                         "Database Provider Unavailable", _
                         MessageBoxButtons.RetryCancel, _
                         MessageBoxIcon.Hand, _
                         MessageBoxDefaultButton.Button1, _
                         0)
                    ' check for error indicating "network down"
                ElseIf (ex.Error = dgErrorNumber.dgEiCONNLOST Or _
                        ex.Error = dgErrorNumber.dgEiHOSTNOTFND) Then
                    dr = MessageBox.Show("Cannot connect to " + srcStr + _
                         ".  Is the network available?", _
                         "Database Provider Unavailable", _
                          MessageBoxButtons.RetryCancel, _
                          MessageBoxIcon.Hand, _
                          MessageBoxDefaultButton.Button1, _
                          0)
                End If
                If (dr = DialogResult.Retry) Then
                    retry = True
                End If
            End Try
            Cursor.Current = origCursor
        Loop Until (retry = False)

        ' In this simple example, just check the connection state and quit
        If (cx.State = ConnectionState.Open) Then
            MessageBox.Show("Connected!")
        End If
        Close()
    End Sub
End Class</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>					
Using ASNA.DataGate.Client
Using ASNA.DataGate.Common</pre>
      <pre class="prettyprint">BegClass Form1 Extends (System.Windows.Forms.Form) Access(*Public)
DclFld Name (srcStr)Type (*String = "asna network database")
DclFld Name (cx) Type (AdgConnection = New AdgConnection(srcStr)
DclFld Name (retry) Type (*Boolean)
DclFld Name (origCursor) Type (Cursor = Cursor.Current)
DclFld Name (dr) Type (DialogResult = DialogResult.Abort)
  Begsr btnConnect_Click(*ByVal e Type (System.Object), *ByVal e Type (System.EventArgs)) 
      Handles btnConnect.Click
      // enter the "retry" loop
       Do
           Try
               retry = *False
               Cursor.Current = Cursors.WaitCursor
               // hourglass
               cx.Open()
               // this will throw dgException if errors occur
           Catch Name (ex) Type (dgException)
       EndDo
     // check for error indicating "service not running"
     If&lt;&gt; (ex.Error = dgErrorNumber.dgEiNORESPONSE)
         dr = MessageBox.Show("Cannot connect to " + srcStr + ". +
              Is the service running?", +
              "Database Provider Unavailable", +
              MessageBoxButtons.RetryCancel, +
              MessageBoxIcon.Hand, +
              MessageBoxDefaultButton.Button1, 0)
           // check for error indicating "network down"
     ElseIf COND(ex.Error = dgErrorNumber.dgEiCONNLOST) Or ex.Error = dgErrorNumber.dgEiHOSTNOTFND)
            dr = MessageBox.Show("Cannot connect to " + srcStr + ". +
            Is the network available?", +
            "Database Provider Unavailable", +
            MessageBoxButtons.RetryCancel, +
            MessageBoxIcon.Hand, +
            MessageBoxDefaultButton.Button1, +
            0)
     EndIf
     If  (dr = DialogResult.Retry)
         retry = *True
     EndIf
 EndTry
 Cursor.Current = origCursor
  Loop Until (retry = *False)
 // In this simple example, just check the connection state and quit
If (cx.State = ConnectionState.Open)
    MessageBox.Show("Connected!")
    ElseIf
        Close()
    EndIf
EndIf
EndSr
EndClass</pre>

See Also

<dl />
      [dgException Class](dcsdgExceptionClass.html)
      <br />
      [dgException.ErrorClass Field](dcsdgExceptionClassErrorClassField.html)
      <br />
      [dgException.Text Field](dcsDisconnectingfromaDatabase.html)
      <br />
      [dgException.Message 
					Property](dcsdgExceptionClassMessageProperty.html)
      <br />
      [dgErrorClass Enumeration](dcsdgErrorClassEnumeration.html)
      <br />
      [dgErrorNumber Enumeration](dcsdgErrorNumberEnumeration.html)

