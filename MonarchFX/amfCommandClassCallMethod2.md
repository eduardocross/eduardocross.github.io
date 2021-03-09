---
title: Command.Call Method (string,string,string[ ],string)

Id: amfCommandClassCallMethod2
TocParent: amfCommandClassCallMethods
TocOrder: 20

keywords: MonarchJobUnavailableException
keywords: MonarchJobEndException
keywords: ProgramCallException

---

Calls an interactive program from a non-display file aspx.vr.

#### Syntax
<pre class="syntax"> **BegSr Call Access(*Public) Type(Void)
   DclSrParm *assemblyName*  Type (*String)
   DclSrParm *programName*   Type (*String)
   DclSrParm *parms*         Type (*String) Rank (1)
   DclSrParm *callbackPage*  Type (*String)** </pre>

<!--mine -->

#### Parameters
<dl>
        <dt>
 *assemblyName* 
        </dt>
        <dd>String.  The name of the assembly that
        contains the program to be called.  The assembly
        must be placed in a folder visible to the blue
        thread. This is typically the 
 **/bin**  folder of the web site.  The
        assembly name is typically the DLL name but without the
        ".DLL" extension.</dd>
        <dt>
 *programName* 
        </dt>
        <dd>String.  The fully qualified name of the
        program to be invoked.  This name must include the
        namespace of the program.</dd>
        <dt>
 *parms* 
        </dt>
        <dd>String.  An array of string parameters to be
        passed to the program's *ENTRY procedure.  The
        parameters are input/output. </dd>
        <dt>
 *callbackPage* 
        </dt>
        <dd>String.  The name of the ASPX
        page reference where control will be relinquished once
        the called program finishes execution.</dd>
</dl>

<!--mine -->

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="50%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <th>Value</th>
            <th>Condition</th>
          </tr>          <tr>
            <td>MonarchJobEndedException</td>
            <td>The Monarch Job has ended
            in an exception.</td>
          </tr>
          <tr>
            <td>MonarchJobUnavailableException</td>
            <td>There is no Monarch Job
            available to accept commands.</td>
          </tr>
          <tr>
            <td>ProgramCallException</td>
            <td>There was an error calling
            the program.</td>
          </tr>
</table>

<!--mine -->

#### Remarks
The additional parameter ( *callbackPage* ) is required. It indicates where control will be relinquished once the called program finishes execution. Calling interactive programs effectively means a transfer of control, first to the interactive program being called and then to the callback page reference. Calls that invoke interactive programs can also send data into the called program via parameters but the output parameter list will be sent to the callback page by storing the array in the Session under the ["MONARCH_CMDPARM"] key.

The called program can define its parameters list using fields of type character and decimal (zoned, packed, binary, and decimal). Each argument in the parameter list (when defined as type character) will be passed left justified and padded on the right for the length specified in the called program.
<!--mine -->

#### Example
<pre class="prettyprint"><code class="language-avr">DclFld Command Type(ASNA.Monarch.Command) New(*Base.Context)
DclArray   Parms Dim(1) Type(*String)
Parms[0] = CustName
Command.Call("MyCompany.MyTechnology.Utils",          +
             "MyCompany.MyTechnology.CUSTINQ",        +
             Parms, "~/Brooklyn.aspx")</code></pre>

The updated parameters stored in *Parms* can be retrieved in "Brooklyn.aspx" with code similar to this one:
<pre class="prettyprint"><code class="language-avr">BegSr Page_Load Access(*Private)Event(*this.Load) 
  DclSrParm sender Type(*Object)
  DclSrParm e Type(System.EventArgs)
  DclFld ParmArray Type(System.Array)
  If (NOT Page.IsPostBack)
     ParmArray = Session["MONARCH_CMDPARM"] *as System.Array     
     If (ParmArray &lt;;&gt; *Nothing)
         Session["MONARCH_CMDPARM"] = *Nothing
         txtState.Text = ParmArray.GetValue(0).ToString()
      // Parms[0] 
     Endif
  EndIf
EndSr</code></pre>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

<!--mine -->

#### See Also
<dl>
        <dd>[Command Class](amfCommandClass.html)</dd>
        <dd>[Command Class Members](amfCommandClassMembers.html)</dd>
        <dd>[ASNA.Monarch Namespace](amfWebDspFASNAMonarchNamespace.html)</dd>
</dl>

