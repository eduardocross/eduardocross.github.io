---
title: Icon Selection

Id: amfIconSelection
TocParent: amfIconIDCollection
TocOrder: 80

keywords: ASNA Wings
keywords: ASNA Wings, rational open access - RPG edition
keywords: Icon
keywords: Icons
keywords: IconID
keywords: IconIDs
keywords: Icon Selection
keywords: IConID Selection

---

<table>
			    <tr>

			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span></td>
			    </tr>
</table>

# Icon Selection
This topic describes the Framework's Icon selection feature, introduced in Wings 6.1. 

The [DdsButton](amfUnderstandingButtons.html) control previously allowed the selection of images or text to represent the control onscreen. But frequently, especially in a mobile computing environment, those options can be problematic. Text is language-specific and can become hard to read on smaller devices, while images can be inflexible: matching them to backgrounds, sizing them properly without loss of resolution, and other context-based issues crop up regularly. 

To alleviate this issue, ASNA has added a new option to our DdsButton control's <code>[ButtonStyle](amfDdsButtonClassButtonStyle.html)</code> property: <code>"Icon"</code>

Selecting <code>"Icon"</code> activates the [IconID property](amfDdsButtonClassIcon.html), which has [a wealth of options](amfIconIDCollection.html) (over two hundred and forty) drawn from the open source Font Awesome project. To help assist users with the potentially overwhelming number of options, when a user changes the <code>IconID</code> property, a new Select Icon window will pop up.

The Icon Selection screen has tabs that can be used to browse the options by topic. Alternatively, the **Locate:** box allows you to type in a name and automatically search all of the tabs for a match.

On the upper right of the icon selection screen is a "preview" window showing the selected icon against both dark and light backgrounds, to make color and shape comparisons more convenient. 

The color of the Icon can be changed using the [DdsButton](amfDdsButtonClass.html)'s <code>[DdsLink](https://msdn.microsoft.com/en-us/library/system.windows.forms.control.forecolor(v=vs.110).aspx">ForeColor</a></code> property. This is the color that will be shown in the Select Icon screen's preview window. 

Identical options are also available for the <a href="amfDdsLinkClass.html) control (where the icon will appear to one side), and in the [DdsList](amfDdsListClass.html) controls' <code>[IconID](amfDdsListClassIconIDProperty.html)</code> and <code>[ChevronIconID](amfDdsListClassChevronIconID.html)</code> property.

**Note** &#8211; Icons may not display properly on devices which do not support SVG graphics.

---

