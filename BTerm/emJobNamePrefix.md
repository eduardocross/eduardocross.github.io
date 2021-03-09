---
title: Naming an IBM i Job

Id: emJobNamePrefix
TocParent: AppLifeCycle
TocOrder: 60

keywords: ASNA Browser Terminal
keywords: ASNA Browser Terminal, Naming Jobs
keywords: Job Prefixes
keywords: RPG Job names

---

<table>
                <tr>
                    <td>
                        <span class="OH_MultiViewContainerPanelDhtmlTable">
                            ASNA Browser Terminal&#8482; Admin Manual
                        </span>
                    </td>
                </tr>
</table>

# Naming an IBM i Job
In BTerm users can designate the names of IBM i jobs using the [TerminalDeviceName](..\..\MonarchFX\_HTML\amfTerminalDeviceName.html) property. 

### Implementation
The property is applied in the [MobileRPGJob](WingsJob.html) class:

<span style="font-family:Consolas"> myDatabase = <span style="color:blue"> new </span> AVRRuntime.<span style="color:#2B91AF">Database</span>(<span style="color:#A31515">&quot;&quot;</span>, AVRRuntime.<span style="color:#2B91AF">VirtualTerminal</span>.MonarchWeb, AVRRuntime.<span style="color:#2B91AF">OpenAccessDspF</span>.MobileRPG); </span> 

<span style="font-family:Consolas"> myDatabase.TerminalDeviceName = <span style="color:#A31515">&quot;MYDEV??&quot;</span>; </span> 

The TerminalDeviceName property takes any string the developer inputs, and as a special option the string can include up to four question marks (?) after the string (i.e. MYDEV??). If any question marks are used, Wings will attempt to create a Job with a name matching the string, while appending a number (in hex) in the place of the question marks (i.e. MYDEV17). 

The string length must be 8 or fewer characters, including any question marks. If a job using the specified name already exists, BTerm will loop, and attempt to create a job one hex-digit higher until it lands on a job name that does not exist. If the name specified in the database connection is not available (or exceeds 8 characters), DataGate will throw an exception with one of the following values: 
<table class="auto-style1">
                        <tr>
                            <th>Name</th>
                            <th style="width: 233px">Value</th>
                        </tr>
                        <tr>
                            <td>dgEx</td>
                            <td style="width: 233px">{&quot;DeviceName Not Available&quot;}</td>
                        </tr>
                        <tr>
                            <td>base</td>
                            <td style="width: 233px">{&quot;DeviceName Not Available&quot;}</td>
                        </tr>
                        <tr>
                            <td>DefaultErrorClass</td>
                            <td style="width: 233px">dgEC_Base</td>
                        </tr>
                        <tr>
                            <td>Error</td>
                            <td style="width: 233px">dgEDEVICENAME</td>
                        </tr>
                        <tr>
                            <td>ErrorClass</td>
                            <td style="width: 233px">dgEC_Base</td>
                        </tr>
                        <tr>
                            <td>Message</td>
                            <td style="width: 233px">&quot;DeviceName Not Available&quot;</td>
                        </tr>
                        <tr>
                            <td>ErrorClass</td>
                            <td style="width: 233px">dgEC_Base</td>
                        </tr>
                        <tr>
                            <td style="height: 25px">Message</td>
                            <td style="width: 233px; height: 25px">&quot;DeviceName Not Available&quot;</td>
                        </tr>
                        <tr>
                            <td style="height: 25px">SystemError</td>
                            <td style="width: 233px; height: 25px">0</td>
                        </tr>
                        <tr>
                            <td style="height: 25px">Text</td>
                            <td style="width: 233px; height: 25px">""</td>
                        </tr>
</table>

The same exception will be thrown if the device name specified contains a suffix of question marks and no device available satisfies the name (all ‘numbers’ have been exhausted). 

**Important &#8211;** While this can potentially support a very high number of job names, the number of iterations it demands makes this a very inefficient choice for supporting more than 20-30 simultaneous jobs with one application. 

If the application is going to be naming Jobs, it is highly recommended that the system value QDEVRCYACN be set to either *ENDJOB or *ENDJOBNOLIST. Please see IBM’s documentation at [http://publib.boulder.ibm.com/infocenter/iseries/v7r1m0/topic/rzakz/rzakzqdevrcyacn.htm](http://publib.boulder.ibm.com/infocenter/iseries/v7r1m0/topic/rzakz/rzakzqdevrcyacn.html) 
To support larger numbers of similarly named jobs
                    without excessive wait times,  BTerm is compatible with
                    [
                        Telnet exit-point programs
                    ](http://publib.boulder.ibm.com/infocenter/iseries/v5r3/index.jsp?topic=%2Frzaiw%2Frzaiwprogramtypes.html) that can dynamically fulfill
                    that need without resorting to repeated
                    calls to the IBM i.

