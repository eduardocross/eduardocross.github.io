---
title: Link Controls

Id: amfUnderstandingLinkControls
TocParent: amfASNAMobileSupport
TocOrder: 55

keywords: ASNA Mobile RPG
keywords: ASNA Mobile RPG, Links
keywords: ASNA Mobile RPG, Link controls
keywords: Mobile RPG

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span></td>
			    </tr>
</table>

# Link Controls

### What is a DdsLink?
ASNA Mobile support includes the [DdsLink control](amfDdsLinkClass.html) which allows the use of web-style hyperlinks.

**Applicability:** These controls can be used in Monarch, Wings, and Mobile RPG pages/apps.

### The Mechanics of a DdsLink
By Default, the DdsLink control is rendered as a hyperlink widget on the user's screen. Hyperlinks require two character fields to operate: first, the text shown to the user (in many applications this text is shown underlined, and with a distinct color); second, the location of the page to be shown when the user touches the hyperlink. This second value is given as a URL (Uniform Resource Locator). 

For example, the text to be shown to the user could be 'Search Engine' and the URL could be 'www.google.com'. When the user touches the text Mobile RPG opens the default internet browser to the specified address.

The DdsLink can also be used to provide links to phone numbers, email addresses, text messaging numbers, and other "profiles" such as Facebook and Skype accounts, interfacing with the apps installed on the mobile device. 
![](Images/DdsLinkTasks.png)

### DdsLink Property Tasks
Here are the DdsLink properties used to establish the two core values and other interesting properties: <br/> 
<table class="TaskTable" border="1" cellspacing="0" cellpadding="0" width="637">
    <tbody>
        <tr>
            <td valign="top" width="169" align="center">

 **Property** 

            </td>
            <td valign="top" width="468" align="center">

 **Notes** 

            </td>
			</tr>
		<tr>
            <td colspan="2" valign="top">

**Appearance** 
</td>
		  </tr>		
          <tr>
            <td valign="top" width="169">    
                    <code> **[IconID](amfDdsButtonClassIconIDProperty.html)** </code>     
            </td>
            <td valign="top" width="468">        
                    The [ID of the Icon](amfIconIDCollection.html) to use to represent the link. (<code>LinkStyle=Icon</code> only.)
            </td>
           </tr> 
		   	        <tr>
            <td valign="top" width="169">           
                    <code> **[Image](amfDdsLinkClassImageProperty.html)** </code>          
           </td>
            <td valign="top" width="468">            
                    Sets the path to the image used for the link. (<code>LinkStyle=Image</code> only.)             
            </td>
		</tr>
					<tr>
            <td colspan="2" valign="top">

**Behavior** 
</td>
			</tr>
		<tr>
            <td valign="top" width="169">
                    <code> **[AppType](amfDdsLinkClassAppTypeProperty.html)** </code>
            </td>
            <td valign="top" width="468">
                    Sets the type of the link, allowing for access to 
					APIs like phone calls, email, instant messaging, and social 
					networking messages.</td>
        </tr>
        <tr>
        	<td><code> **[LinkStyle](amfDdsLinkClassLinkStyleProperty.html)** </code>
        	</td>
        	<td>This property defines whether the DdsLink will appear as a traditional hyperlink or as an Image.
        	</td>
        </tr>
		<tr>
            <td colspan="2" valign="top">

**External Description** 
</td>
			</tr>

        <tr>
            <td valign="top" width="169">

 **<code>[TextFieldName](amfDdsLinkClassTextFieldNameProperty.html)</code>
                     &amp; <code>[TextFieldLength](amfDdsLinkClassTextFieldLengthProperty.html)</code>** 

            </td>
            <td valign="top" width="468">

                    These properties define the field whose value is to be shown on the screen.  Overrides <code>TextValue</code>.

            </td>
        </tr>

        <tr>
            <td valign="top" width="169">

                    <code> **[UrlFieldName](amfDdsLinkClassURLFieldNameProperty.html)
                     &amp; [UrlFieldLength](amfDdsLinkClassURLFieldLengthProperty.html)** </code>

            </td>
            <td valign="top" width="468">

                    These properties define the field whose value is to be used as the target URL of the hyperlink.
					Overrides <code>URLValue</code>.

            </td>
        </tr>

    </tbody>
</table>

###  **Example** 
Dds Links can be added inside of other onscreen controls. When placing a DdsLink inside of a subfile it must be nested within a DdsCharfield. The following example presents a subfile populated with a charfield, which itself presents a link. In this case, the link takes the form of an image (a mail icon).
<pre class="prettyprint"><code class="html">&lt;mdf:DdsSubfile id="_PEOSFL" runat="server" 
       style="position: absolute; left: 0px; top: 40px; width: 600px; height: 28px" 
       Alias="PEOSFL" CssClass="DdsSubfileRecord"
       UseSubfilePaging="True" VirtualRowCol="7,2" VirtualWidth="24" 
       VirtualRowsPerRecord="1" RowsCssClasses="DefaultRow AlternateRow" &gt;

...

        &lt;mdf:DdsCharField id="PEOSFL_NAME" runat="server" 
          style="position: absolute; left: 73px; top: 0px; width: 181px"
          CssClass="DdsCharField" Length="20" Alias="PEONAME" Usage="OutputOnly"
          VirtualRowCol="7,5"  /&gt;

        &lt;mdf:DdsLink ID="DdsLink1" runat="server" AppType="EMail" 
          Image="Themes/Current/Images/Mail.jpg" 
          UrlFieldName="PEOMAIL" UrlFieldLength="100" TextValue="Mail" 
          LinkStyle="Image" Width="24px" Height="24px" /&gt;

      &lt;/mdf:DdsSubfile &gt;</code></pre>

This snippet of code will draw the destination of the link from an RPG element named PEOMAIL, using the folloing RPG code as code-behind.
<pre style="background-color:black;color:lime">0002.00 FPEOPLEDF  CF   E             WORKSTN SFile(PEOSFL:sflrrn)      

0003.00 F                                     INFDS(Feedback)   

0004.00 F                                     Handler('ASNAWINGS')      

0005.00 D*********************************************************************

…

0087.00 C                   Eval      *IN90=*ON                 

0088.00 C                   WRITE     PEOSFC                  

0089.00 C                   Eval      *IN90=*OFF              

0090.00 C                   Z-Add     0             sflrrn            4 0  

0091.00 C                   Eval      PEONAME = 'Abraham Baldwin'   

0092.00 C                   Eval      PEOMail = 'AbBa@signer.gov'          

0093.00 C                   Add       1             sflrrn                 

0094.00 C                   WRITE     PEOSFL                               

0095.00 C                   Eval      PEONAME = 'Richard Bassett'          

0096.00 C                   Eval      PEOMail = 'RiBa@signer.gov'          

0097.00 C                   Add       1             sflrrn                 

0098.00 C                   WRITE     PEOSFL                               

…

0116.00 C     *In03         Doueq     '1'                           

0117.00 C                   EXFMT     PEOSFC                        

0118.00 C                   EndDo                                   

0119.00 C                   Eval      *INLR = *ON                   </pre>

The output will look something like this:

![](images/ddslink.png)
