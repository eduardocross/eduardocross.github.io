---
title: DdsBar.HideWhenEmpty Property

Id: amfDdsBarClassHideWhenEmptyProperty
TocParent: amfDdsBarClassProperties
TocOrder: 5

keywords: HideWhenEmpty property
keywords: ddsbar, HideWhenEmpty
keywords: field controls, ddsbar, HideWhenEmpty

---

If <code>true</code>, causes the bar to be hidden from users when it is empty.

#### Syntax
<pre class="syntax"> **BegProp HideWhenEmpty Access(*Public) Type(Boolean)
   BegGet:  BegSet** </pre>

#### Property Values
**Boolean.** If <code>true</code> when all DdsBar segments have no content, the bar will not be visible. Defaults to <code>false</code>

#### Remarks
This property is most useful for DdsBars (used as [FooterBarControl](amfddsRecordClassFooterBarControlProperty.html) for a [DdsRecord](amfDdsRecordClass.html)) that only contain a [DdsMessagePanel](amfddsMessagePanelClass.html) used to display errors on the page. When no error messages exist on a DdsRecord, the DdsMessagePanel should not appear.

If this property is <code>true</code>, pressing the "Reset" button on a DdsMessagePanel contained in an affected bar will cause the bar (and message panel) to once again be hidden.

#### Optional Enhancements
In this use case, consider optimizing space and readability by simpifying the "Reset" button and making the following CSS changes:

1. Change the "Reset" text to an "x":
<pre>&lt;mdf:DdsMessagePanel runat="server" ID="MyMessagePanel" ResetButtonText="x"&lt;
	  &gt;/mdf:DdsMessagePanel&lt;  </pre>

This is the markup for setting the [ResetButtonText](amfddsMessagePanelClassResetButtonTextPoperty.html) property set to "x".

2. Change the CSS to show a Round Button (as more commonly seen in mobile environments):
<pre>.DdsErrorReset {
    right: 5px;
    top: 5px;
    position: absolute;
    display: block;
    width: 30px;
    height: 30px;
    border: 2px solid #f5f5f5;
    border-radius: 50%;
    color: #f5f5f5;
    text-align: center;
    text-decoration: none;
    background: #464646;
    box-shadow: 0 0 3px gray;
    font-size: 13px;
}</pre>	  

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsBar Class](amfDdsBarClass.html) <br /> [DdsBar Class Members](amfDdsBarClassMembers.html) <br />[DdsRecord Class](amfDdsRecordClass.html)<br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
