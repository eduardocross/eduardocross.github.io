---
title: Enhancing Applications using Non-Display File ASPX Pages

Id: amfconEnhancingWithNonDisplayFileASPX
TocParent: amfconFrameworkASPXSessionOverview
TocOrder: 10

keywords: overview of using non-display file aspx pages
keywords: ASNA.Monarch, Non-Display File aspx pages
keywords: display files, about Non-Display File ASPX pages
keywords: ASNA.Monarch, Monarch Non-Display File ASPX pages
keywords: enhancements, ASNA.Monarch, Non-Display File ASPX pages
keywords: ASNA.Monarch, enhancements using Non-Display File ASPX pages
keywords: aspx files, ASNA.Monarch, enhancements using Non-Display File ASPX pages
keywords: enhancing application using non-display file aspx pages
keywords: command mode
keywords: command mode, about
keywords: non-display file aspx.vr
keywords: non-display file aspx.vr, about
keywords: aspx.vr, non-display file

---

Monarch-based programs execute within the context of a Monarch Job and conform to certain conventions allowing the job to be the target of a <code>CALLB</code> or <code>CALLD</code> operation. This Job provides a program with a connection to the database, with a set of *global* variables shared amongst all the programs in the Job (the LDA and LDC), and with a mechanism to support instantiation based on activation groups, which is particularly important in supporting the call commands. 

A Job also provides an interactive program with the infrastructure supporting display files. Refer to [Framework ASPX Session Overview](amfconFrameworkASPXSessionOverview.html) for a more complete description of the interaction of the Program and Monarch Job during a normal ASPX session. The Job currently has general 'states' as follows.

- A. Just created
- B. Executing a Program
- C. Waiting for input from the user

After a Job has been created, it is in state A and transitions to state B when the Job.Start method is executed. When the program executes a <code>READ</code> or <code>EXFMT</code> on a workstation format, the job goes into state C.

In order to invoke a program from within the code behind a NDF aspx page, it is necessary to have a Job providing the context where the program can run. This Job should be in a state able to accept requests to execute arbitrary programs outside of the normal calling graph created by program calls.

The cooperation of the Job is essential so a program within the Job must make the Job enter a new state:

- D. Accepting Commands

In this state, the Job can accept commands.

##### Note
The <code>LDC</code> can contain **any** type of object, however only those that are of type **string** can be sent to the Yellow side.

To access the LDC strong values from the Yellow side use ASNA.Monarch.Command class' methods:
- <code>public string GetLdcObject( string name )</code>
- <code>public void SetLdcObject( string name, string value )</code>

This command can be executed only when the Job is waiting in either of these states:
- Waiting for input from the user (in a <code>READ</code> or <code>EXFMT</code> of a display file)
- Accepting Commands via the AcceptCommand method on MonarchJob

#### New Facilities Summary
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
          <col width="12%" />
          <col width="28%" />
          <col width="30%" />
          <col width="30%" />
          </colgroup>
          <tr><th>Facility</th>
              <th>Enter Command Mode</th>
              <th>Exit Command Mode</th>
              <th>Execute Command(s)</th>
          </tr>
           <tr>
            <td> **Description** 
            </td>
            <td>Prepares a job to accept commands</td>
            <td>Returns a Job to procedural processing</td>
            <td>Allows code in aspx.vr to
            invoke a function within a Job, particularly program
            calls.</td>
          </tr>
          <tr>
            <td> **Methods** 
            </td>
            <td>[
            ShowPage](amfWebJobClassShowPageMethod.html)  
            [
            AcceptCommands](amfWebJobClassAcceptCommandsMethod.html) </td>
            <td>[
              Command.Return](amfCommandClassReturnMethod.html)
            </td>
            <td>
[ Command.Call](amfCommandClassCallMethods.html) [ Command.CallSilent](amfCommandClassCallSilentMethod.html) [ Command.SetLdaField](amfCommandClassSetLdaFieldMethod.html) [ Command.GetLdaField](amfCommandClassGetLdaFieldMethod.html) [ Command.SetLdcObject](amfCommandClassSetLdcObjectMethod.html) [ Command.GetLdcObject](amfCommandClassGetLdcObjectMethod.html) [ Command.PushKeyFocus](amfCommandClassPushKeyFocusMethod.html) [ Command.RemoveLdcObject](amfCommandClassRemoveLdcObjectMethod.html) [ Command.RequestShutdown](amfCommandClassRequestShutdownMethod.html) 
</td>
          </tr>
          <tr>
            <td> **Parent Object** 
            </td>
            <td>[
            ASNA.Monarch.WebJob](amfWebJobClass.html)(ASNA.isualRPG.Runtime.dll)</td>
            <td>[
            ASNA.Monarch.Command](amfCommandClass.html)<br />(ASNA.Monarch.WebDspF.dll) or (ASNA.isualRPG.Runtime.dll)</td>
            <td>[
            ASNA.Monarch.Command](amfCommandClass.html)<br />(ASNA.Monarch.WebDspF.dll) or
             (ASNA.isualRPG.Runtime.dll)</td>
          </tr>
</table>

# Enter Command Mode (Blue thread)

#### ShowPage and AcceptCommands
These commands prepare a job to accept commands.
<pre class="prettyprint"><code class="language-avr">
        public string ShowPage(string outsidePage, string parameter)</code></pre>
      <pre class="prettyprint"><code class="language-avr">
        public string AcceptCommands(string parameter)     </code>   
</pre>

<code> **ShowPage** </code> receives an ASPX page that is presented to initiate the conversation with the user. In a way, this command enables a procedural program to 'call' an ASPX.

A single string parameter can be passed to these methods; the parameter will be stored in the session object where the ASPX code behind can retrieve it like this:
<pre class="prettyprint"><code class="language-avr">Parameter = Session["MONARCH_CMDPARM"] *as *String
   Session["MONARCH_CMDPARM"] = *Nothing</code></pre>

#### Example
**In the procedure code (blue thread):** 
<pre class="prettyprint"><code class="language-avr">DclFld Result Type(*String)
  Result = (monarchJob *as ASNA.Monarch.WebJob).ShowPage("~/Clifton.aspx", "23,ABC,X")
  If (Result = "Function Completed")
       Return
   EndIf</code></pre>

Or
<pre class="prettyprint"><code class="language-avr">DclFld Result Type(*String)
   Result = (monarchJob *as ASNA.Monarch.WebJob).AcceptCommands()
    If (Result = "Function Completed")
Return
   EndIf</code></pre>

**In 'Clifton.aspx' (yellow thread):** 
<pre class="prettyprint"><code class="language-avr">BegSr Page_Load Access(*Private) Event(*This.Load)
   DclSrParm sender Type(*Object)
   DclSrParm e Type(System.EventArgs)
   DclArray  Parms Rank(1) Type(*String)
   DclFld    Parameters Type(*String)
   If (NOT Page.IsPostBack)
        Parameter = Session["MONARCH_CMDPARM"] *as*String
        Session["MONARCH_CMDPARM"] = *Nothing
          If (Parameter = *Nothing)
            Response.Redirect("./PageRequestOutOfSequence.html")
          EndIf        Parms = Parameter.Split(O',')
        txtCustNumber.Text = Parms[0]
   EndIf
EndSr</code></pre>

# Execute Commands (Yellow thread)

#### Call Command
<pre class="prettyprint"><code class="language-avr">public void Call(string assemblyName, string programName, string[] parms)</code></pre>

or
<pre class="prettyprint"><code class="language-avr">public void Call(string assemblyName, string programName, string[] parms string 

callbackPage)</code></pre>

Call can invoke an interactive or process program. Programs receive parameters by reference, i.e. the ASPX code can send and receive data to/from the called programs; the parameters are stored in an array of strings. The called program can define its parameters list using fields of type character and decimal (zoned, packed, binary, and decimal).

Interactive calls also require an ASPX page reference where control will be relinquished once the called program finish execution. Calling interactive programs effectively means a transfer of control, first to the interactive program being called, and then to the callback Page reference. Calls that invoke interactive programs can send data into the program via parameters but the output parameters list will be sent to the callback page by storing the array in the Session under the [<code>"MONARCH_CMDPARM"</code>] key.

#### Example
**Non-Interactive program call:** 
<pre class="prettyprint"><code class="language-avr">DclFld Command Type(ASNA.Monarch.Command) New(*Base.Context)
   DclArray   Parms Dim(3)  Type(*String)
   Parms[0] = CustNo
   Parms[1] = Sales.ToString()
   Parms[2] = Returns
   Command.Call("MyCompany.MyTechnology.Utils", "MyCompany.MyTechnology.CUSTINQ", Parms)
   Sales   = Parms[1]
   Returns = Parms[2]
   txtSales.Text = Sales.ToString()
   txtRetrn.Text = Returns.ToString()</code></pre>

**Interactive program call:** 
<pre class="prettyprint"><code class="language-avr">DclFld Command Type(ASNA.Monarch.Command) New(*Base.Context)
DclArray   Parms Dim(1) Type(*String)
   Parms[0] = CustName
   Command.Call("MyCompany.MyTechnology.Utils",          +
                "MyCompany.MyTechnology.CUSTINQ",        +
                Parms, "~/Brooklyn.aspx")</code></pre>

The updated parameters stored in *Parms* can be retrieved in "Brooklyn.aspx" with code similar to this one:
<pre class="prettyprint"><code class="language-avr">BegSr Page_Load Access(*Private) Event(*This.Load)     
  DclSrParm sender Type(Object)   
  DclSrParm e Type(System.EventArgs)
  DclFld ParmArray Type(System.Array)
  If (NOT Page.IsPostBack)
        ParmArray = Session["MONARCH_CMDPARM"] *as System.Array
        If (ParmArray &lt;&gt; *Nothing)
             Session["MONARCH_CMDPARM"] = *Nothing
             txtState.Text = ParmArray.GetValue(0).ToString()
            // Parms[0] 
        Endif
   EndIf
EndSr</code></pre>

#### <code>CallSilent</code> Command
<code> **CallSilent** </code> invokes an interactive program from a non-display file aspx.vr (yellow thread) and prevents the display of the program's display file in the browser.
<pre class="prettyprint"><code class="language-avr">public ASNA.Monarch.WebDisplayFile
CallSilent(string assemblyName, string programName, string [] parms</code></pre>

When the interactive program performs an <code>EXFMT</code> (or <code>READ</code>), it will stop waiting for input from the user and <code> **CallSilent** </code> will return the WebDisplayFile object allowing the caller to inspect the dataset containing the data tables of the record formats written by the interactive program on the blue thread.

The caller of <code> **CallSilent** </code> is responsible for feeding input to the waiting interactive program. This is done by updating the appropriate rows of the data table of the WebDisplayFile and then executing the method <code> **PushKeyFocus** </code>.

#### <code>PushKeyFocus</code> Command
<code> **PushKeyFocus** </code> is invoked from the yellow thread to provide input to the blue thread program waiting for input. It sets the parameter values and returns a WebDisplayFile with the focus set as dictated by the parameters.
<pre class="prettyprint"><code class="language-avr">public ASNA.Monarch.WebDisplayFile PushKeyFocus( + +
ASNA.Monarch.Command.AidKey key, short virtualRowCol, string fieldname )</code></pre>

This method does not affect the indicators that would normally be set/reset if the display file would have gone to the browser. In particular, no numeric indicator will be set based on the key "pressed". The waiting program must base its actions on the feedback AID or the <code>IN *xx* </code> indicators.

**Example** 
<pre class="example"><span style="color:blue">DclFld</span> Command <span style="color:blue">Type</span>(ASNA.Monarch.Command) <span style="color:blue">New</span>(<span style="color:blue">*Base</span>.Context)
<span style="color:blue">DclFld</span> DspF <span style="color:blue">Type</span>(ASNA.Monarch.WebDisplayFile) 
<span style="color:blue">DclSrParm</span> sender <span style="color:gray">*Object</span>
<span style="color:blue">DclSrParm</span> e System.EventArgs
<span style="color:blue">DclFld</span> Command <span style="color:blue">Type</span>(ASNA.Monarch.Command) <span style="color:blue">New</span>(<span style="color:blue">*Base</span>.Context)
      Command.RequestShutdown()
</pre>

#### <code>InvokeQCmdExc</code> Method
This method (added in 8.0) executes a command on the IBM i's Job associated with the database connection by calling IBM's <code>QCMDEXC</code>.

The WingsJob or MobileRPG Job should have suspended its execution by calling either <code>AcceptCommands</code> or <code>ShowPage</code> (see http://devnet.asna.com/documentation/Help140/MonarchFX/_HTML/amfconEnhancingWithNonDisplayFileASPX.htm). While the executing thread is in this suspended state, a method in the code-behind of the web site can call <code>InvokeQCmdExc</code>, which will forward the command to the IBM i Job for its execution.
<pre class="prettyprint"><code class="language-avr">public string QCmdExc(string command, string callbackPage)</code></pre>

<code>QCmdExc</code> executes a command on the IBM i's Job associated with the database connection. <br /> If during the execution of the command a screen is displayed, control does not return to the caller, instead, control is transferred to the page on the callbakPageCaller parameter.
<pre class="prettyprint"><code class="language-avr">public string QCmdExc(string command)</code></pre>

<code>QCmdExc</code> executes a command on the IBM i's Job associated with the database connection.<br /> The execution of the command should not involve any screen I/O.

**Wings Example** 
<pre class="prettyprint"><code class="language-avr">public partial class Menu : System.Web.UI.Page
{
    protected void btnGo_Click(object sender, EventArgs e)
    {
        ASNA.Monarch.Command command = new ASNA.Monarch.Command(Context);
        int option = int.Parse(txtOption.Text);
        switch (option)
        {
            case 1:
                {
                    command.InvokeQCmdExc("CHGCURLIB ERNUEXPRES");
                    command.InvokeQCmdExc("CALL CUSTINQ", "~/Menu.aspx");
                    break;
                }
            case 2:
                {
                    command.InvokeQCmdExc("DSPLIBL", "~/Menu.aspx");
                    break;
                }
            case 3:
                {
                    Response.Redirect("~/CommandLine.aspx");
                    break;
                }
            case 4:
                {
                    command.Return("SIGNOFF");
                    break;
                }
        }
    }

}
</code></pre>

The resulting WingsJob will resemble the following.
<pre class="prettyprint">
	<code class="language-avr">public partial class WingsJob : ASNA.Monarch.WebJob
{
    private AVRRuntime.Database myDatabase;

    override protected AVRRuntime.Database getDatabase()
    {
        return myDatabase;
    }

    override public void Dispose( bool disposing )
    {
        if( disposing )
            myDatabase.Close();
        base.Dispose( disposing );
    }

    protected override void ExecuteStartupProgram()
    {
        myDatabase = new AVRRuntime.Database("", AVRRuntime.VirtualTerminal.MonarchWeb, AVRRuntime.OpenAccessDspF.Wings);
        myDatabase.Server   = "MyServer";
        myDatabase.Label    = "DB2";
       myDatabase.Port     = 5042;
        myDatabase.User     = LDC["UserName"] as string;
        myDatabase.Password = LDC["Password"] as string;
        LDC["Password"]     = "";
        try
        {
            myDatabase.Open();
        }
        catch (Exception e)
        {
            string error = e.Message;
        }
        string rv = AcceptCommands();
    }
}
</code></pre>

# Exit Command Mode (Yellow Thread)

#### <code>Return</code> Command
Returns a Job to procedural processing thus exiting command mode.
<pre class="example"><span style="color:blue">public void</span> Return(<span style="color:blue">string</span> result)
</pre>

When an ASPX page wants to return the Job state to continue its procedural processing, it executes this command, passing a string back to the original code in the blue thread that prepared the job to accept commands.

**Example** 
<pre class="example"><span style="color:blue">DclFld</span> Command <span style="color:blue">Type</span>(ASNA.Monarch.Command) <span 

style="color:blue">New</span>(<span style="color:blue">*Base</span>.Context)
   Command.Return("Function Completed")
</pre>

#### Next: [Moving Data between Workstation and Display Files](amfconFrameworkASPXSessionMovingData.html)

#### Previous: [Monarch Framework ASPX Session Overview](amfconFrameworkASPXSessionOverview.html)

#### See Also
<dl>
        <dd>[Monarch
      Framework ASPX Session Overview](amfconFrameworkASPXSessionOverview.html) </dd>
      <dd>[Job Class](amfJobClass.html)</dd>
<dd>[Program Class](amfProgramClass.html)</dd>
<dd>[
      LocalDataCollection Class](amfLocalDataCollectionClass.html)</dd></dl>

