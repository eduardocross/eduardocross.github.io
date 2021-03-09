---
title: ASNA Monarch Cascading Style Sheets

Id: amfconDisplayFilesStyleSheets
TocParent: amfconDisplayFilesThemeComponents
TocOrder: 30

keywords: cascading style sheets, concepts
keywords: CSSClass, concepts
keywords: display files, about cascading style sheets
keywords: Web server controls [ASNA.Monarch], display file cascading style sheets
keywords: Web server controls [ASNA.Monarch], cascading style sheet
keywords: concepts, cascading style sheets
keywords: Web server controls [ASNA.Monarch], cascading style sheets
keywords: ASNA.Monarch.Web server controls, cascading style sheets
keywords: CSS, monarch defaults
keywords: Web server controls, cascading style sheets
keywords: cascading style sheets, CssClass property 
keywords: theme components, cascading style sheets

---

The elements in an HTML document can have attributes that are used to describe the appearance and functionality of that element on the displayed page. You can assign these attributes to each element on the aspx page individually; or styles can be placed inline within a single HTML element, grouped in a <code> **&lt;STYLE&gt;** </code> block in the <code>HEAD</code> portion of your Web page. But the best practice is to combine these attributes to create a style "CcsClass name" in an external cascading style sheet file and then apply the "CssClass name" to each element. The same external style sheet file can be linked to many Web pages, thus giving a common appearance to an entire Web site.

CSS style rules serve as the gold standard for specifying the desired appearance and position of HTML elements.

The <code>CssClass</code> property (inherited from <code> **WebControl** </code>) is used to specify the CSS class to render on the client for the Web Server control. This property will render on browsers for all visible controls. It will always be rendered as the class attribute, regardless of the browser.

#### Example
Put this definition in an external cascading style sheet:
<pre class="syntax"> . **TestStyle** 
{ 
  font: 12pt verdana; 
  font-weight:700;
  color:orange;
}</pre>

Then use the CssClass name <code>TestStyle</code> in your ASPX page.
<pre class="example">&lt;asp:Button id="Button" CssClass=" **TestStyle** " Text="Submit" runat="server"/&gt; </pre>

#### CSS Summary Table
The chart below is a general listing of the types of cascading styles in **~Themes/Current/Styles/Framework.css** that you will encounter in your ASNA Wings website. You can refer to the actual file for specific details. For more detailed information on CSS in general, visit [<code>DdsCharField</code>](http://www.csszengarden.com/"> http://www.csszengarden.com/</a>.
<table class="mytable" width="90%"  cellpadding="4" cellspacing="0">
                        <colgroup><col width="20%" /><col
                        width="80%" /></colgroup>
                            <tr>
                                <th class="nameColumn" style="height: 71px">CcsClass<br />(ASNA 
								Monarch Framework Reference)</th>
                                <th class="descriptionColumn" style="height: 71px">Description</th>
                            </tr>

<tr>
							<td style="height: 73px">
							<a href="amfDdsCharFieldClass.html)</td>
							<td style="height: 73px">
							Controls the display 
							characteristics for a character field, a character 
							field that has a validation error (<code>_Error</code>), a 
							character field that is output only (<code>_OutputOnly</code>), and 
							a character field that contains a hyperlink (<code>_Link</code>).</td>
						</tr>
<tr>
							<td>
							[<code>DdsConstant</code>](amfDdsConstantClass.html)</td>
							<td>
							Controls the display 
							characteristics for a constant value. </td>
						</tr>
<tr>
							<td>
							[<code>DdsDateField</code>](amfDdsDateFieldClass.html)</td>
							<td>
							Controls the display 
							characteristics for a date field defining a textbox 
							with button or image control that is linked to a 
							javascript calendar; right justified (<code>_Right</code>), has a 
							validation error (<code>_Error</code>), or is 
							output only (<code>_OutputOnly</code>). </td>
						</tr>
<tr>
							<td>
							[<code>DdsDecDateField</code>](amfDdsDecDateFieldClass.html)</td>
							<td>
							Controls the display characteristics for a 
							date field, type decimal, that may be defined with a 
							button or image that is linked to a JavaScript 
							calendar. Styles also include right justified 
							(<code>_Right</code>), a decimal date that has a validation 
							error(<code>_Error</code>), or is output only (<code>_OutputOnly</code>). </td>
						</tr>
<tr>
							<td>
							[<code>DdsDecFieldK</code>](amfDdsDecFieldClass.html)</td>
							<td>
							Controls the display characteristics for a decimal 
							field, a decimal field that is right aligned 
							(<code>_Right</code>), a decimal field that has an error 
							(<code>_Error</code>), a decimal field that is right aligned and has an error 
							(<code>_Error_Right</code>), a 
							decimal field that is output only (<code>_OutputOnly</code>), a 
							decimal field that is right aligned and output only 
							(<code>_Right_OutputOnly</code>), and if an invalid length is 
							encountered (<code>InvalidLength</code>).</td>
						</tr>
						<tr>
							<td style="height: 48px"><code>DdsInlinePopUpBackground</code></td>
							<td style="height: 48px">Controls the styles for the background of the 
							overlay that appears after a request is submitted to 
							the IBM i.</td>
						</tr>
						<tr>
							<td><code>DdsInlinePopUpContent</code></td>
							<td>Controls the styles for the content of the 
							overlay that appears after a request is sent to the 
							IBM i.</td>
						</tr>

												<tr>
							<td><code>DdsInlinePopUpTable</code></td>
							<td>Controls the styles for tables in the overlay 
							that appears after a request is sent to the IBM i.</td>
						</tr>

						<tr>
							<td><code>DdsInlinePopUpTitle</code></td>
							<td>Controls the styles for the title in the overlay 
							that appears after a request is sent to the IBM i.</td>
						</tr>
						<tr>
							<td style="height: 65px"><code>DdsSflMsgField</code></td>
							<td style="height: 65px">Controls the styles for the 
							subfile message fields, including output only fields 
							(<code>_OutputOnly</code>).</td>
						</tr>

						<tr>
							<td style="height: 65px">
							[<code>DdsSubfileControl</code>](amfddsSubfileControlClass.html)<br />
							[<code>DdsSubfile</code>](amfDdsSubfileClass.html)</td>
							<td style="height: 65px">Controls the styles for the subfile control and 
							subfile records, including the background color for alternating rows 
							displayed on the subfile (<code>DefaultRow</code> and 
							AlternateRow).</td>
						</tr>
<tr>
							<td>
							[<code>DdsTimeField</code>](amfDdsTimeFieldClass.html)</td>
							<td>
							Controls the display 
							characteristics for a time field, a time field that 
							has a validation error (<code>_Error</code>), a time field that 
							is output only (<code>_OutputOnly</code>), and a time field that 
							contains a hyperlink (<code>_Link</code>).</td>
						</tr>
<tr>
							<td style="height: 73px">
							[<code>DdsTimestampField</code>](amfDdsTimeStampFieldClass.html)</td>
							<td style="height: 73px">
							Controls the display 
							characteristics for a timestamp field, a timestamp 
							field that has a validation error (<code>_Error</code>), a 
							timestamp field that is output only (<code>_OutputOnly</code>), 
							and a timestamp field that contains a hyperlink 
							(<code>_Link</code>).</td>
						</tr>
<tr>
							<td style="height: 76px">(CssClass style elements only)</td>
							<td style="height: 76px">Controls the styles of a display file 
							including content 
							placement, popup windows, headers, function 
							keys, and standardizes HTML elements and consistent 
							styling for the 5250 terminal emulation. </td>
						</tr>
						<tr>
							<td><code>SubmitWait</code></td>
							<td>Controls the display of the overlay with a 
							spinner that appears when the submit button is 
							pressed (to prevent multiple submissions and show 
							that the system is working).</td>
						</tr>
<tr>
							<td><code>SubmitWait_2seconds</code></td>
							<td>Controls the display of the overlay (without a 
							spinner) that appears when the submit button is 
							pressed, keeping the <code>SubmitWait</code> spinner from 
							appearing for two seconds.</td>
						</tr>

</table>

**Note &#8211;** On browsers (IE6 or older) that do not support CSS, setting the <code> **CssClass** </code> property will have no effect. 

The following table lists and details CSS classes that appear by default in **~Themes/Current/Styles/Theme.css.** 
<table class="mytable" width="90%"  cellpadding="4" cellspacing="0">
                        <colgroup><col width="20%" /><col
                        width="80%" /></colgroup>
                            <tr>
                                <th class="nameColumn"><code>CSS Class</code><br />(in 
								Theme.css)</th>
                                <th class="descriptionColumn">Description</th>
                            </tr>
<tr>
							<td><code>DdsFileFullBannerKey</code></td>
							<td>
							Controls the display characteristics for Full Banner 
							Keys (large keys displaying all used function keys) It supports hover, active, and disabled 
							styles.</td>
						</tr>
<tr>
							<td><code>DdsFileFullBannerRMarginKey</code></td>
							<td>
							Controls the display characteristics for Full Banner 
							Keys that need to be separated by a horizontal gap, 
							such as by PgUp or PgDn. This class is largely 
							used when implementing **vertical**  
							banner keys. It supports hover, active, and 
							disabled styles.</td>
						</tr>

<tr>
							<td><code>DdsKey</code></td>
							<td>
							Controls the display characteristics for a DDS key.</td>
						</tr>
<tr>
							<td style="height: 52px"><code>DdsVKey</code></td>
							<td style="height: 52px">
							Controls the display characteristics for a virtual 
							DDS Key, used when Wings sites are displayed on 
							mobile devices in a **vertical**  configuration. </td>
						</tr>
<tr>
							<td><code>DdsVKeyW</code></td>
							<td>
							Controls the display characteristics for a virtual 
							DDS Key, used when Wing sites are displayed on 
							mobile devices in **wide screen**  or
 **horizontal**  configuration.</td>
						</tr>
						<tr>
							<td style="height: 73px"><code>SubFileDataFields</code></td>
							<td style="height: 73px">Controls the styles for the Subfile data fields, 
							right-aligned data fields (<code>_Right</code>), data fields that 
							are output only (<code>_OutputOnly</code>), and data fields that 
							that are right aligned and output only 
							(<code>_Right_OutputOnly</code>).</td>
						</tr>

<tr>
							<td style="height: 30px"><code>SubfileHeader</code></td>
							<td style="height: 30px">
							Controls the display characteristics for a subfile 
							header.</td>
						</tr>
<tr>
							<td style="height: 37px"><code>
							SubfileHeaderFields</code></td>
							<td style="height: 37px">
							Controls the display characteristics for subfile 
							header fields.</td>
						</tr>
<tr>
							<td style="height: 65px"><code>SubFileRows</code></td>
							<td style="height: 65px">Controls the styles for the subfile 
							rows, including the background color for alternating rows 
							displayed on the subfile (<code>DefaultRow</code> and 
							<code>AlternateRow</code>).</td>
						</tr>

</table>

#### Next: [Web.config Considerations](amfconWebConfigConsiderations.html)

#### Previous: [Display File Master Pages](amfconDisplayFilesMasterPages.html)

#### See Also
<dl>
        <dd>[Web Server Controls Overview](amfWebServerControlsOverview.html)</dd>
</dl>

#### References
<dl><dd><a href="http://www.w3schools.com/ASPNET/prop_webcontrol_style_cssclass.asphttp://www.w3schools.com/ASPNET/prop_webcontrol_style_cssclass.asp">ASP.NET CssClass Property
		</a></dd></dl>

