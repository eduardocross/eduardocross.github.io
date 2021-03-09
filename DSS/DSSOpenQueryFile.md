---
title: Open Query File in DSS

Id: DSSOpenQueryFile
TocParent: DSSPorting
TocOrder: 100

keywords: ASNA DataGate
keywords: DSS
keywords: Open Query File
keywords: Using Open Quesry File in DSS
keywords: Open Quesry File and DSS
keywords: Open Query File and DataGate&#174; for SQL Server

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">[ASNA DataGate&#174; for SQL Server Reference Manual
				   ](Welcome.html)</span></td>
			    </tr>
</table>

# Employing Open Query File and ASNA DataGate&#174; <sup>&#174;</sup> for SQL Server<sup>&#174;</sup>

##  
If your application makes use of the Open Query File with DataGate&#174; for SQL Server, the following restrictions apply: 

- The string passed in the <code>QrySelect</code> must comply with the syntax of SQL Server, for example you should 
	use the word '<code>and</code>' not the symbol '<code>&amp;</code>'.
- If you are changing the order of the file by providing a value in the <code>QryKeyFlds</code> parameter, you must:
		<ul>
			<li>Specify <code>RANDOM(*NO)</code> in the <code>DCLDISKFILE</code> to state that you will be accessing this file only consecutively.
- Open the file for <code>*INPUT</code> only

</li>
</ul>

