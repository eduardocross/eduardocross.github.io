---
title: Verifying Results with Exception Handling

Id: dcsVerifyingResultswithExceptionHandling
TocParent: dcsAccessingaFileMain
TocOrder: 4

keywords: handling exceptions, verifying results
keywords: exception handling, verifying results with
keywords: verifying results with exception handling
keywords: accessing a file, verifying results with exception handling

---

Results of [FileAdapter](dcsFileAdapterClass.html) and [ AdgDataSet](dcsAdgDataSetClass.html) methods are provided via .NET exception handling. The standard exception object in DCS is [dgException](dcsdgExceptionClass.html). DCS uses **dgException** to transmit both error conditions and "normal" procedural conditions, such as "end-of-file". In the examples shown so far, tests for dgException have been omitted for clarity. In your own DCS programs, you would use these checks to improve the reliability of your program. The DCS reference documentation for access and other methods lists the common **dgException** objects thrown. 

Revising a previous example, the following code will check for certain conditions, such as end-of-file.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
      </pre>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">using System; </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">using System.Data; </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">using System.Windows.Forms; </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">using ASNA.DataGate.Client; </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">using ASNA.DataGate.Common;</span> <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">namespace NetworkRecovery </span> 

<p> <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">{ </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-tab-count: 1"> </span>public class Form1 | System.Windows.Forms.Form </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-tab-count: 1"> </span>{ </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-tab-count: 1"> </span> <span style="mso-spacerun: yes"> </span>const string srcStr = "asna network database"; </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>private System.Windows.Forms.Button button1; </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-tab-count: 1"> </span> <span style="mso-spacerun: yes"> </span>private System.ComponentModel.Container components = null;</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-tab-count: 1"> </span> <span style="mso-spacerun: yes"> </span>public Form1()... </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-tab-count: 1"> </span> <span style="mso-spacerun: yes"> </span>protected override void Dispose( bool disposing )...</span> <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> </span> 

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-tab-count: 1"> </span> <span style="mso-spacerun: yes"> </span>#region Windows Form Designer generated code </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>...Designer code omitted... </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-tab-count: 1"> </span> <span style="mso-spacerun: yes"> </span>#endregion </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> </span> 

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-tab-count: 1"> </span> <span style="mso-spacerun: yes"> </span>[STAThread] </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-tab-count: 1"> </span> <span style="mso-spacerun: yes"> </span>static void </span> <place> <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">Main</span> </place> <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">()... </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> </span> 

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>private void button1_Click(object sender, System.EventArgs e) </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>{ </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>AdgConnection cx = new AdgConnection(srcStr); </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span> </span> <span lang="ES-TRAD" style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">bool retry = false; </span>

<span lang="ES-TRAD" style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>Cursor origCursor = Cursor.Current; </span>

<span lang="ES-TRAD" style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> </span> 

<span lang="ES-TRAD" style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span> </span> <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">// enter the "retry" loop </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>do </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>{ </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>try </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>{ </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>retry = false; </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>Cursor.Current = Cursors.WaitCursor; // hourglass </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>cx.Open();<span style="mso-spacerun: yes"> </span>// this will throw dgException if errors occur </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>} </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>catch ( dgException ex ) </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>{ </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>string mbMsg = ex.Message; </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>// check for error indicating "service not running" </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>if ( ex.Error == dgErrorNumber.dgEiNORESPONSE ) </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span> </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>mbMsg = "Cannot connect to " + srcStr + </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span> <span style="mso-spacerun: yes"> </span>".<span style="mso-spacerun: yes"> </span>Is the service running?"; </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>// check for error indicating "network down" </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>else if ( ex.Error == dgErrorNumber.dgEiCONNLOST || </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>ex.Error == dgErrorNumber.dgEiHOSTNOTFND ) </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>mbMsg = "Cannot connect to " + srcStr + </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>".<span style="mso-spacerun: yes"> </span>Is the network available?"; </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>DialogResult dr = MessageBox.Show( mbMsg, </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>"Database Provider Unavailable", </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>MessageBoxButtons.RetryCancel, </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>MessageBoxIcon.Hand, </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span> <span style="mso-spacerun: yes"> </span>MessageBoxDefaultButton.Button1, </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>0 ); </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>if ( dr == DialogResult.Retry ) </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>retry = true; </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>} </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>finally </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span> <span style="mso-spacerun: yes"> </span>{ </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>Cursor.Current = origCursor; </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>} </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>} while (retry == true); </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> </span> 

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>// In this simple example, just check the connection state and quit </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>if ( cx.State == ConnectionState.Open ) </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>MessageBox.Show( "Connected!" ); </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>Close(); </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-spacerun: yes"> </span>} </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="mso-tab-count: 1"> </span>} </span>

}
<pre class="prettyprint">
        <span class="lang">[Visual Basic]</span>
      </pre>
      <pre>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">Imports ASNA.DataGate.Client
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">Imports ASNA.DataGate.Common
        </span>
              <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">Public Class Form1</span>     <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">    </span>Inherits System.Windows.Forms.Form</span>

        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">     <span style="mso-spacerun: yes">    </span>Const srcStr As String = "asna network database"</span>

        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">#Region " Windows Form Designer generated code "

          <span style="mso-tab-count: 1">       </span>...Designer code omitted...
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">#End Region
</span>
         <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">    </span>Private Sub btnConnect_Click(ByVal sender As System.Object, _
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                                 </span>ByVal e As System.EventArgs) _
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                   </span>Handles btnConnect.Click
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">        </span>Dim cx As AdgConnection = New AdgConnection(srcStr)
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">        </span>Dim retry As Boolean
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">        </span>Dim origCursor As Cursor = Cursor.Current
</span>
      <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">        </span>' enter the "retry" loop
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">        </span>Do
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">            </span>Try
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                </span>retry = False
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                </span>Cursor.Current = Cursors.WaitCursor ' hourglass
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                </span>cx.Open()<span style="mso-spacerun: yes">   </span>' this will throw dgException if errors occur
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">            </span>Catch ex As dgException
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                </span>Dim dr As DialogResult = DialogResult.Abort
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                </span>' check for error indicating "service not running"
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                </span>If (ex.Error = dgErrorNumber.dgEiNORESPONSE) Then
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                    </span>dr = MessageBox.Show("Cannot connect to " + srcStr + _
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                                         </span>".<span style="mso-spacerun: yes">  </span>Is the service running?", _
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                                          </span>"Database Provider Unavailable", _
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                                          </span>MessageBoxButtons.RetryCancel, _
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                                          </span>MessageBoxIcon.Hand, _
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                                          </span>MessageBoxDefaultButton.Button1, _
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">      <span style="mso-spacerun: yes">                                       </span>
          <span style="mso-spacerun: yes">   </span>0)
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                    </span>' check for error indicating "network down"
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                </span>ElseIf (ex.Error = dgErrorNumber.dgEiCONNLOST Or _
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                        </span>ex.Error = dgErrorNumber.dgEiHOSTNOTFND) Then
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                    </span>dr = MessageBox.Show("Cannot connect to " + srcStr + _
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                                         </span>".<span style="mso-spacerun: yes">  </span>Is the network available?", _
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                                          </span>"Database Provider Unavailable", _
</span>

       <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">          <span style="mso-spacerun: yes">                                     </span>MessageBoxButtons.RetryCancel, _
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">   </span>
          <span style="mso-spacerun: yes">                                       </span>MessageBoxIcon.Hand, _
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                                          </span>MessageBoxDefaultButton.Button1, _
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                                          </span>0)
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                </span>End If
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                </span>If (dr = DialogResult.Retry) Then
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                    </span>retry = True
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">                </span>End If
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">            </span>End Try
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">            </span>Cursor.Current = origCursor
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">        </span>Loop Until (retry = False)
</span>
<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">         </span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">        </span>' In this simple example, just check the connection state and quit
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">        </span>If (cx.State = ConnectionState.Open) Then
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">            </span>MessageBox.Show("Connected!")
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">        </span>End If
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">        </span>Close()
</span>
        <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">
          <span style="mso-spacerun: yes">    </span>End Sub
</span>
        <span style="FONT-SIZE: 8pt; ">End Class</span>

         </pre>

        <span style="FONT-SIZE: 8pt; ">
          <span class="lang">[Visual RPG]</span>
        </span>

<span style="FONT-SIZE: 8pt; COLOR: blue; FONT-FAMILY: 'Courier New'">Using</span> <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> ASNA.DataGate.Client</span>

<span style="FONT-SIZE: 8pt; COLOR: blue; FONT-FAMILY: 'Courier New'">Using</span> <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> ASNA.DataGate.Common</span>

<p > <span style="FONT-SIZE: 8pt; COLOR: blue; FONT-FAMILY: 'Courier New'">BegClass</span> <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> Form1 <span style="COLOR: blue">Extends</span>(System.Windows.Forms.Form) <span style="COLOR: blue">Access</span>(<span style="COLOR: gray">*Public</span>)</span>

<span style="FONT-SIZE: 8pt; COLOR: blue; FONT-FAMILY: 'Courier New'">DclFld</span> <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">Name</span> (srcStr)<span style="COLOR: blue">Type</span> (<span style="COLOR: gray">*String </span>= "asna network database")</span>

<span style="FONT-SIZE: 8pt; COLOR: blue; FONT-FAMILY: 'Courier New'">DclFld</span> <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">Name</span> (cx) <span style="COLOR: blue">Type</span> (AdgConnection = <span style="COLOR: blue">New</span> AdgConnection(srcStr)</span>

<span style="FONT-SIZE: 8pt; COLOR: blue; FONT-FAMILY: 'Courier New'">DclFld</span> <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">Name</span> (retry) <span style="COLOR: blue">Type</span> (<span style="COLOR: gray">*Boolean</span>)</span>

<span style="FONT-SIZE: 8pt; COLOR: blue; FONT-FAMILY: 'Courier New'">DclFld</span> <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">Name</span> (origCursor) <span style="COLOR: blue">Type</span> (Cursor = Cursor.Current)</span>

<span style="FONT-SIZE: 8pt; COLOR: blue; FONT-FAMILY: 'Courier New'">DclFld</span> <span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">Name</span> (dr) <span style="COLOR: blue">Type</span> (DialogResult = DialogResult.Abort)</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">Begsr</span> btnConnect_Click(*ByVal e Type (System.Object), *ByVal e Type (System.EventArgs)) </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> Handles btnConnect.Click <br /> </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="BACKGROUND: white">// enter the "retry" loop</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">Do</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">Try</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> retry = <span style="COLOR: blue">*False</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> Cursor.Current = Cursors.WaitCursor <span style="BACKGROUND: white">// hourglass</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> cx.Open() <span style="BACKGROUND: white">// this will throw dgException if errors occur</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">Catch</span><span style="COLOR: blue">Name</span> (ex) <span style="COLOR: blue">Type</span> (dgException)</span>
<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'">             </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">EndDo</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <br /> <span style="BACKGROUND: white">// check for error indicating "service not running"</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">If</span> (ex.Error = dgErrorNumber.dgEiNORESPONSE) </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> dr = MessageBox.Show("Cannot connect to " + srcStr + ". + </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> Is the service running?", +</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> "Database Provider Unavailable", +</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> MessageBoxButtons.RetryCancel, +</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> MessageBoxIcon.Hand, +</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> MessageBoxDefaultButton.Button1, 0)</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> </span> 

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="BACKGROUND: white">// check for error indicating "network down"</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">ElseIf</span><span style="COLOR: blue">COND</span>(ex.Error = dgErrorNumber.dgEiCONNLOST) </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> Or ex.Error = dgErrorNumber.dgEiHOSTNOTFND) </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> dr = MessageBox.Show("Cannot connect to " + srcStr + ". +</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> Is the network available?", +</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> "Database Provider Unavailable", +</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> MessageBoxButtons.RetryCancel, +</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> MessageBoxIcon.Hand, +</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> MessageBoxDefaultButton.Button1, +</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> 0)</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">EndIf</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">If</span> (dr = DialogResult.Retry) </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> retry = <span style="COLOR: blue">*True</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">EndIf</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">EndTry</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> Cursor.Current = origCursor</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> Loop Until (retry = <span style="COLOR: blue">*False</span>)</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="BACKGROUND: white">// In this simple example, just check the connection state and quit</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">If</span> (cx.State = ConnectionState.Open) </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> MessageBox.Show("Connected!")</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">ElseIf</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">Close</span>()</span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">EndIf</span></span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">EndIf</span> </span>

<span style="FONT-SIZE: 8pt; FONT-FAMILY: 'Courier New'"> <span style="COLOR: blue">EndSr</span></span>
<span style="FONT-SIZE: 8pt; COLOR: blue; FONT-FAMILY: 'Courier New'">EndClass</span>

The code in this simple example opens a keyed-access file, then enters a "<span>try-catch</span>" block, to perform read operations. The first [ReadSequential](dcsFileAdapterClassReadSequentialMethod.html) method reads the first record in the file. Next, [ ReadRandomKey](dcsFileAdapterClassReadRandomKeyMethod.html) is called to read the first record with a particular key. If the file has no records, <span>dgException</span> will be thrown from the <span>ReadSequential</span> method, and the value of the <span>dgException.Error</span> property will be dgEaEOF. In this case, the program will print the result "End of file." If the file has at least one record, but none with a CMCustNo value of 200000, then dgException will be thrown from <span>ReadRandomKey</span> with an Error value of dgEaNOTFND. 

Note that not all traditional "feedback" information regarding the last access performed is transmitted through dgException. Other properties of FileAdapter, such as [ ExactSeek](dcsFileAdapterClassExactSeekProperty.html), [RRN](dcsFileAdapterClassRRNProperty.html) and [ CurrentFormatIndex](dcsFileAdapterClassCurrentFormatIndexProperty.html) are provided for this purpose. 

For a general introduction to .NET exception handling, please see the <span>.NET Framework referenc</span>e. 
See Also

<dl />[AdgDataSet Class](dcsAdgDataSetClass.html)<br />[Database File Records and 
						AdgDataSet](dcsDatabaseFileRecordsandAdgDataSet.html)<br />[Efficient File Access](dcsEfficientFileAccess.html)<br />[FileAdapter Class](dcsFileAdapterClass.html)<br />[Reading and Writing to Database 
						Files](dcsReadingandWritingtoDatabaseFiles.html)<br />[Using the FileAdapter Class](dcsUsingtheFileAdapterClass.html)   

