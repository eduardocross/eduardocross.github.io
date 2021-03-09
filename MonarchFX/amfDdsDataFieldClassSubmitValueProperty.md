---
title: DdsDataField.SubmitValue Property

Id: amfDdsDataFieldClassSubmitValueProperty
TocParent: amfDdsDataFieldClassProperties
TocOrder: 90

keywords: SubmitValue property
keywords: DdsDataField.SubmitValue property
keywords: web controls, setting submit value for field control
keywords: web controls, getting submit value for field control
keywords: web controls, replace drop-down selection with submit value
keywords: how to, set submit value for field control
keywords: how to, get submit value for field control
keywords: how to, replace drop-down selection with submit value
keywords: display files, replace drop-down selection with submit value
keywords: display files, submission value for control field
keywords: Web server controls [ASNA.Monarch], field submit value
keywords: field controls, submit value

---

Gets or sets a value for the field that when selected, is treated the same as if the user had entered this value and pressed &lt;enter&gt;. 

#### Syntax
<pre class="prettyprint"> **BegProp SubmitValue Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String containing a value for the field that is the same as if the user had entered this value and pressed &lt;enter&gt;.

#### Remarks
When **SubmitValue** is defined, the field will be displayed as output only and clicking on it will be the same as if the user had typed in the value of **SubmitValue** . The text to be displayed is set on [ Text](amfDdsDataFieldClassTextProperty.html) property. [ AutoPostBackKey](amfDdsDataFieldClassAutoPostBackKeyProperty.html) property simulates a key press after the field has been clicked on. Default key pressed is 'Enter'.

#### Example
Notice in the partial sample display below, the ***Sel*** field where the user can pick from the drop down value of 0, 1, or 3 to either select the customer record or display the customer sales.

![](Images/ zzSubmitValueBefore.bmp) 

The underlying aspx source shows the definition for the drop down box as follows:
<pre class="example"><span style="color:blue">&lt;<span style="color:maroon">mdf</span>:<span style="color:maroon">DdsDecField</span> <span style="color:red">id</span>="SFL1_SFSEL" <span style="color:red">runat</span>= "server"
        <span style="color:red">CssClass</span>="DdsCharField"
        <span style="color:red">Length</span>="2"          
        <span style="color:red">Decimals</span>="0"
        <span style="color:red">style</span>="<span style="color:red">POSITION</span>: absolute; <span style="color:red">LEFT</span>: 2px; <span style="color:red">TOP</span>: 0px;"
        <span style="color:red">Alias</span>="SFSEL"
        <span style="color:red">VisibleCondition</span>="!( 60 )"
        <span style="color:red">Usage</span>="Both"
        <span style="color:red">VirtualRowCol</span>="8,4"
        <span style="color:red">Protect</span>="60"
        <span style="color:red">EditCode</span>="Z"
        <span style="color:red">ValuesStyle</span>="DropdownValues"
        <span style="color:red">Values</span>="0 1 3"&gt;</span> </pre>

To affectively use this property, we want to replace the Sel field to allow the user to select a 'text' value for (one of) the two options available. There are several changes that need to be made. The **CssClass** property needs to be changed to an output only field (DdsDecField_Link). The **Text** property value is set to "Select". The **ValuesStyle** property is replaced with **SubmitValue** with a value of "1", which was the value for selecting the customer. **AutoPostBackKey** property is added with the "Enter" key.

When the changes are completed, the aspx for ** *Sel* ** will look like the following:
<pre class="example"><span style="color:blue">&lt;<span style="color:maroon">mdf</span>:<span style="color:maroon">DdsDecField</span> <span style="color:red">id</span>="SFL1_SFSEL" <span style="color:red">runat</span>= "server"
        <span style="color:red">CssClass</span>="DdsCharField_link"
        <span style="color:red">Length</span>="2"          
        <span style="color:red">Decimals</span>="0"
        <span style="color:red">style</span>="<span style="color:red">POSITION</span>: absolute; <span style="color:red">LEFT</span>: 2px; <span style="color:red">TOP</span>: 0px;"
        <span style="color:red">Alias</span>="SFSEL"
        <span style="color:red">VisibleCondition</span>="!( 60 )"
        <span style="color:red">Usage</span>="Both"
        <span style="color:red">VirtualRowCol</span>="8,4"
        <span style="color:red">Protect</span>="60"
        <span style="color:red">EditCode</span>="Z"
 **<span style="color:red">Text</span>="Select"
        <span style="color:red">SubmitValue</span>="1"
        <span style="color:red">AutoPostBackKey</span>="Enter"** &gt;</span> </pre>

This change only provides one of the two previous options, so a second field would need to be added to allow the same ease of selection for the Display Sales function. Once the field was added, it would provide a solution something similar to that shown below. The user can click on either <u>Select</u> or <u>Sales</u> where before they selected 1 or 3 from the drop down box.

![](Images/ zzSubmitValueAfter.bmp) 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsDataField Class](amfDdsDataFieldClass.html) <br /> [ DdsDataField Class Members](amfDdsDataFieldClassMembers.html) <br /> [ Derived Classes](amfDdsDataFieldDerivedClasses.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
