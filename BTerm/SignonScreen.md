---
title: Sign on Screen

Id: SignonScreen
TocParent: emComponents
TocOrder: 40

keywords: ASNA Browser Terminal
keywords: ASNA Browser Terminal, sign on screen
keywords: ASNA Browser Terminal, how to
keywords: how to, change ASNA Browser Terminal Sign on
keywords: Emu

---

<table>
			    <tr>
			      <td> <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Browser Terminal&#8482; Admin Manual
				   </span></td>
			    </tr>
</table>

# Sign on Screen
The ASNA Browser Terminal signon screen, SignOn.aspx, works in conjunction with [WingsJob](WingsJob.html)&lt;.vr&gt;/&lt;.cs&gt;/&lt;.vb&gt; to capture the user login credentials when running ASNA Browser Terminal.

**AVR** 
<pre class="PrettyPrint">
&lt;PermissionSetAttribute(SecurityAction.LinkDemand, Name := <span style="color:maroon">&quot;FullTrust&quot;</span>)&gt; _
&lt;PermissionSetAttribute(SecurityAction.InheritanceDemand, Name := <span style="color:maroon">&quot;FullTrust&quot;</span>)&gt; _
<span style="color:blue">Public</span> <span style="color:blue">Class</span> VBCodeProvider _
    <span style="color:blue">Inherits</span> CodeDomProvider
						</pre>

**C** #
<pre class="prettyprint">&lt;PermissionSetAttribute(SecurityAction.LinkDemand, Name := <span style="color:maroon">&quot;FullTrust&quot;</span>)&gt; _
&lt;PermissionSetAttribute(SecurityAction.InheritanceDemand, Name := <span style="color:maroon">&quot;FullTrust&quot;</span>)&gt; _
<span style="color:blue">Public</span> <span style="color:blue">Class</span> VBCodeProvider _
    <span style="color:blue">Inherits</span> CodeDomProvider						</pre>

#### Sign On Display
The SignOn.aspx, if left unchanged, will resemble the image below and have the data fields shown in the subsequent table.

![Runtime view of Original Signon.aspx](../Images/SignonRuntime.png)
<table  class="members" id="memberList" width="90%"><colgroup><col width="15%" /><col width="70%" /></colgroup>

					   <tr><th style="height: 19px">Data Fields</th>
						   <th style="height: 19px">Description</th></tr>
					    <tr><td> **System** </td><td>The IBM i server name 
							containing the RPG/ILE programs with the Handler 
							keyword if in modernization mode, or the server 
							that is used for production after your application 
							has been deployed.</td></tr>
					    <tr><td style="height: 32px"> **Port** </td>
							<td style="height: 32px">The port number of the server 
							connection. The default is 5042. However, this should be the same port number assigned 
							when you installed[ ASNA DataGate for IBM i](InstallingWings.html).</td></tr>
					    <tr><td> **User** </td><td>The user name.</td></tr>
					    <tr><td> **Password** </td><td>The user's password.</td></tr>
					    <tr><td style="height: 37px"> **Program/procedure<br />
							Menu** </td><td style="height: 37px">The cl program or procedure 
							you want to execute or the menu program.</td></tr>
					    <tr><td> **Current Library** </td><td>The library 
							the program, procedure, or menu is located in. This 
							would be the library containing the RPG ILE programs 
							that have the Handler keyword.</td></tr>
</table>

#### Modifying the Sign on Logic
The sign on display file and logic provided with BTerm may be functional for the programmer in a testing environment but it does not provide restricted access to the other servers that may not be available to all users and it can be cumbersome for most daily users in a runtime environment. To eliminate both of these issues the sign on display and logic can be changed in a couple of ways.

**Preload Variables and Display Only** 

One option is to set all of the variable values except for the user name and password in the WingsJob.cs, .vr, or .vb code and change the <span style="color:red">Usage</span> attribute in the SignOn.aspx for those variables that you preset to <span style="color:blue">"OutputOnly"</span>. The WingsJob.cs example is shown below setting the server, program, library, and port to specific values; and the user, password, menu, and message to spaces. 

In practice, instead of a single program (Custinqcl in the example), a menu may be the starting program which the user works from throughout the day. In that case, set the menu name instead of the program name and set the <span style="color:red">Usage</span> attribute to <span style="color:blue">"OutputOnly"</span> for both the program and menu.
<pre class="prettyprint"></pre>

![WingsJob.cs with variable settings shown](../Images/WingsJobLogonInfo.png)
<br />
Next, you want to change the Signon.aspx to reflect a <span style="color:red">Usage</span> attribute of <span style="color:blue">"OutputOnly" for </span> those variables that you preset in WingsJob that you do not want the user to override, namely server, program, menu, library, and port. The following image shows the <span style="color:red">Usage</span> attribute changed to <span style="color:blue">"OutputOnly"</span> for the server field.

![SignOn.aspx shownwith usageequal outputonly](../Images/SignonASPXLogonInfo.png)
<br />
**Preload Variable and Remove from the SignOn.aspx** 

In the above example, the user sign on still displays all of the sign on information but only the user name and password are entered. Under some circumstances you may want to display only the user name and password and hide the remaining fields that you preset with values.

**Remove SignOn.aspx and Call your Sign On Program** 

There may be an instance where you already have your own sign on program that you want to use instead of the SignOn provided with the ASNA Browser Terminal Design Aid. If that is the case, you will need to do several things.

1. Remove SignOn.aspx from the Web Site.

								<li>In the server's filesystem, locate SignOn.aspx. Right mouse click and select 
 **Delete**  from the dropdown menu. The file will be 
								removed from the project.

</li>
2. Remove all references to the Signon.aspx from the 
						WingsJob code and add the appropriate values to the WingsJob 
					code to call your IBM i server signon program.

								<li>Remove the **LogonScreen**  region. 
								Collapse the region, right mouse click, and select 
 **Cut**  from the dropdown menu.
3. Remove **goMenu** . Collapse the 
								code section, right mouse click, and select **Cut**  from 
								the dropdown menu.
4. Remove **CallQcmdExec** . Collapse 
								the code section, right mouse click, and select 
 **Cut**  
								from the dropdown menu.

</li>
5. Change MobileRPGJob code to call your sign on program.

