---
title: Command.IvokeQCmdExc Method

Id: amfCommandClassIvokeQCmdExcMethod
TocParent: amfCommandClassMethods
TocOrder: 53

keywords: IvokeQCmdExct method
keywords: Command.IvokeQCmdExc method
keywords: non-display file aspx.vr, IvokeQCmdExc command
keywords: aspx.vr, non-display file, IvokeQCmdExc command
keywords: local data collection, non-display file
keywords: local data collection, getting
keywords: MonarchJobUnavailableException
keywords: MonarchJobEndException

---

Executes a command on the IBM i's Job associated with the database connection by calling IBM's <code>QCMDEXC</code>.

#### Syntax
<pre class="syntax"> **BegFunc IvokeQCmdExc Access(*Public) Type(*String)
   DclSrParm *name*  Type (*String)** </pre>

<!--mine -->

#### Parameters
<dl>
        <dt>
          <code> *name* </code>
        </dt>
        <dd>The name of the object whose value is to be
        returned.</dd>
</dl>

<!--mine -->

#### Return Value
A string containing a value for the named entry from the jobs' local data collection.
<!--mine -->

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="50%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <code><th>Value</th></code>
            <th>Condition</th>
          </tr>          <tr>
            <code><td>MonarchJobEndedException</td></code>
            <td>The Monarch Job has ended
            in an exception.</td>
          </tr>
          <tr>
            <code><td>MonarchJobUnavailableException</td></code>
            <td>There is no Monarch Job
            available to accept commands.</td>
          </tr>
</table>

<!--mine -->

#### Remarks
This method (added in 8.0) executes a command on the IBM i's Job associated with the database connection by calling IBM's <code>QCMDEXC</code>.

The WingsJob or MobileRPG Job should have suspended its execution by calling either <code>AcceptCommands</code> or <code>ShowPage</code> (see http://devnet.asna.com/documentation/Help140/MonarchFX/_HTML/amfconEnhancingWithNonDisplayFileASPX.htm). While the executing thread is in this suspended state, a method in the code-behind of the web site can call <code>InvokeQCmdExc</code>, which will forward the command to the IBM i Job for its execution.
<pre class="prettyprint">
	<code class="language-avr">public string QCmdExc(string command, string callbackPage)</code></pre>

<code>QCmdExc</code> executes a command on the IBM i's Job associated with the database connection. <br /> If during the execution of the command a screen is displayed, control does not return to the caller, instead, control is transferred to the page on the <code>callbackPageCaller</code> parameter.
<pre class="prettyprint">
	<code class="language-avr">public string QCmdExc(string command)</code></pre>

<code>QCmdExc</code> executes a command on the IBM i's Job associated with the database connection.<br /> The execution of the command should not involve any screen I/O.

#### Wings Example
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

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10 Pro
<!-- end -->

<!--mine -->

#### See Also
<dl>
        <dd>[Command Class](amfCommandClass.html)</dd>
        <dd>[Command Class Members](amfCommandClassMembers.html)</dd>
        <dd>[ASNA.Monarch Namespace](amfWebDspFASNAMonarchNamespace.html)</dd>
</dl>

