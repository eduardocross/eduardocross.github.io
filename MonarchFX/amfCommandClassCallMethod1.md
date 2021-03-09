---
title: Command.Call Method (string, string, string[ ])

Id: amfCommandClassCallMethod1
TocParent: amfCommandClassCallMethods
TocOrder: 10

keywords: MonarchJobUnavailableException
keywords: MonarchJobEndException
keywords: ProgramCallException

---

Calls a process program from a non-display file aspx page

#### Syntax
<pre class="syntax"> **BegSr Call Access(*Public) Type (Void)
   DclSrParm *assemblyName*  Type (*String)
   DclSrParm *programName*   Type (*String)
   DclSrParm *parms*         Type (*String) Rank (1)** </pre>

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
        parameters are input/output.</dd>
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
          </tr>
          <tr>
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
The called program can define its parameters list using fields of type character and decimal (zoned, packed, binary, and decimal). Each argument in the parameter list (when defined as type character) will be passed left justified and padded on the right for the length specified in the called program.
<!--mine -->

#### Example
<pre class="example"><span style="COLOR: blue">DclFld</span> Command <span style="COLOR: blue">Type</span>(ASNA.Monarch.Command) <span style="COLOR: blue">New</span>(<span style="COLOR: blue">*Base</span>.Context)
<span style="COLOR: blue">   DclArray  </span> Parms <span style="COLOR: blue">Dim</span>(3) <span style="COLOR: blue">Type</span>(<span style="COLOR: gray">*String</span>)
   Parms[0] = CustNo
   Parms[1] = Sales.ToString()
   Parms[2] = Returns
   Command.Call("MyCompany.MyTechnology.Utils",          +
                "MyCompany.MyTechnology.CUSTINQ",        +
                Parms)
   Sales   = Parms[1]
   Returns = Parms[2]
   txtSales.Text = Sales.ToString()
   txtRetrn.Text = Returns.ToString()</pre>

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

