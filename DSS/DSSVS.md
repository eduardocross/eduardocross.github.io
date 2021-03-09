---
title: Differences Between DataGate, DataGate&#174; for IBM i, and DataGate&#174; for SQL Server

Id: DSSVS
TocParent: DSSConfiguration
TocOrder: 45

keywords: ASNA DataGate
keywords: ASNA DataGate&#174; for SQL Server
keywords: DSS
keywords: DataGate&#174; Differnces
keywords: DataGate&#174; for IBM i vs DataGate&#174; for SQL Server
keywords: DG/400 vs DSS

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">[ASNA 
				   DataGate&#174; for SQL Server Reference Manual
				   ](Welcome.html)</span></td>
			    </tr>
</table>

# Differences Between DataGate, DataGate&#174; for IBM i, and DataGate&#174; for SQL Server

---

###  Contents 

- Object Considerations
- Index (Keys) Considerations
- Data Access Considerations
- Locking Considerations
- Field Considerations
- Native SQL Server Field Interpretation
- Join Considerations
- Calling Programs/Procedures Considerations

###  Object Considerations 
<table class="NormalTable-Heading"
    style="border-style:solid;border-width:1px;margin-right: 6.75pt;margin-left: .15in;left: 0px;top: 96px;border-spacing: 0px;border-spacing: 0px"
    cellspacing="0" width="754" id="table2">

        <tr valign="middle" class="whs3">
            <td bgcolor="#FFFFDD" valign="top" class="whs4" style="border-color: #524D52; background-color: #ECEEF4">

** Item ** 
</td>

            <td bgcolor="#FFFFDD" valign="top" class="whs5" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top-color: #524D52; border-bottom-color: #524D52; background-color: #ECEEF4">

<b style="font-weight: bold;"> DG/400 </b> 
</td>

            <td bgcolor="#FFFFDD" valign="top" class="whs6" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top-color: #524D52; border-bottom-color: #524D52; background-color: #ECEEF4" width="237">

** DSS ** 
</td>

            <td bgcolor="#FFFFDD" valign="top" class="whs6" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top-color: #524D52; border-bottom-color: #524D52; background-color: #ECEEF4" width="237">

** DataGate ** 7 
</td>
        </tr>
        <tr valign="middle" class="whs8">
            <td valign="top" width="188" class="whs9" style="border-left-color: #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Library &amp; file name length 
</td>

            <td valign="top" width="222" class="whs10" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

10 characters
</td>

            <td valign="top" width="237" class="whs11" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

31 characters
</td>

            <td valign="top" width="167" class="whs12" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

31 characters
</td>

        </tr>        
        <tr valign="middle" class="whs13">
            <td valign="top" width="188" class="whs14" style="border-left-color: #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Members per file
</td>
            <td valign="top" width="222" class="whs15" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

0 &#174; <code>*NoMax</code>
</td>
            <td valign="top" width="237" class="whs16" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Exactly 1
</td>
            <td valign="top" width="167" class="whs17" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

0 &#174; <code>*NoMax</code>,
</td>
         </tr>
        <tr valign="middle" class="whs18">
            <td valign="top" width="188" class="whs14" style="border-left-color: #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

File types
</td>
            <td valign="top" width="222" class="whs15" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Physical

&#160;

Simple logical

Join logical

Multiformat logical

Print
</td>
            <td valign="top" width="237" class="whs16" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Physical

SqlLogical

Simple logical

Join logical

&#160;

Print
</td>
            <td valign="top" width="167" class="whs17" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Physical

&#160;

Simple logical

Join logical

Multiformat logical

Print
</td>
        </tr>
        <tr valign="middle" class="whs19">
            <td valign="top" width="188" class="whs14" style="border-left-color: #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Max record length
</td>
            <td valign="top" width="222" class="whs15" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

32,000 bytes
</td>
            <td valign="top" width="237" class="whs16" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

8,060 bytes (Not counting Text and Image fields that are not accessible yet by DSS).
</td>
            <td valign="top" width="167" class="whs17" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

32,000 bytes
</td>
        </tr>
        <tr valign="middle" class="whs20">
            <td valign="top" width="188" class="whs14" style="border-left-color: #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Max number of records per member
</td>
            <td valign="top" width="222" class="whs15" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

&#160;
</td>
            <td valign="top" width="237" class="whs16" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Limit defined by SQL Server instance
</td>
            <td valign="top" width="167" class="whs17" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

<code>2,147,483,646*</code>
</td>
        </tr>
        <tr valign="middle" class="whs21">
            <td valign="top" width="188" class="whs14" style="border-left-color: #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Library implemented as:
</td>
            <td valign="top" width="222" class="whs15" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Library
</td>
            <td valign="top" width="237" class="whs16" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Database
</td>
            <td valign="top" width="167" class="whs17" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Illusion
</td>
        </tr>
        <tr valign="middle" class="whs22">
            <td valign="top" width="188" class="whs14" style="border-left-color: #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Object text (description)
</td>
            <td valign="top" width="222" class="whs15" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

49 characters
</td>
            <td valign="top" width="237" class="whs16" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

49 characters
</td>
            <td valign="top" width="167" class="whs17" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

49 characters
</td>
        </tr>
        <tr valign="middle" class="whs23">
            <td valign="top" width="188" class="whs14" style="border-left-color: #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Stored Procedures
</td>
            <td valign="top" width="222" class="whs15" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Any AS/400 language
</td>
            <td valign="top" width="237" class="whs16" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Programmed in SQL-Transact
</td>
            <td valign="top" width="167" class="whs17" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

None
</td>
        </tr>
        <tr valign="middle" class="whs24">
            <td valign="top" width="188" class="whs14" style="border-left-color: #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Triggers
</td>
            <td valign="top" width="222" class="whs15" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Any AS/400 language
</td>
            <td valign="top" width="237" class="whs16" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Programmed in SQL-Transact
</td>
            <td valign="top" width="167" class="whs17" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

None
</td>
        </tr>
        <tr valign="middle" class="whs25">
            <td valign="top" width="188" class="whs26" style="border-left-color: #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Field Reference File (FRF)
</td>
            <td valign="top" width="222" class="whs27" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

A physical file can refer to any number of FRF, which are any physical file in any library. However, DG/400 will report only those coming from the file stated in the DDS REF keyword.
</td>
            <td valign="top" width="237" class="whs28" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

Refers to the collection of 'User Defined Data Types', which is one per Database (i.e.: Library).&#160; This collection is surfaced via the special file '<code>*FieldRef</code>' which is the ** *ONLY* ** file usable as a FRF.
</td>
            <td valign="top" width="167" class="whs17" style="border-left: 1pt solid #524D52; border-right-color: #524D52; border-top: 1pt solid #524D52; border-bottom-color: #524D52">

A physical file can refer to only ** *ONE* ** FRF, which FRF, which can be any physical file in any library.
</td>
        </tr>
</table>

** *Note:&#160; For Max number of records per member* ** *, DataGate&#174; for Windows and Desktop Servers Release 14.0 and higher support member/file sizes limit of 16 **exabytes** ( 2^4 * 2^60).* 

###  Index (Keys) Considerations 
<table class="normal"	style="border-style:Solid; border-width:1px; margin-left: .15in; border-spacing: 0px; border-spacing: 0px"
		cellspacing="0"	width="754" id="table3" >
    <col class="whs29"/>
    <col class="whs30"/>
    <col class="whs29"/>
    <col class="whs30"/>

    <tr valign="middle" class="whs3">
        <td bgcolor="#FFFFDD" valign="top" class="whs31" style="border-color: #524D52; border-width: 1px; padding: 0; background-color: #ECEEF4">

**Item** 
</td>
        <td bgcolor="#FFFFDD" valign="top" width="95px" class="whs32" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top-color: #524D52; border-top-width: 1px; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0; background-color: #ECEEF4">

**DG/400** 
</td>
        <td bgcolor="#FFFFDD" valign="top" class="whs33" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top-color: #524D52; border-top-width: 1px; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0; background-color: #ECEEF4" width="212">

**DSS** 
</td>
        <td bgcolor="#FFFFDD" valign="top" class="whs34" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top-color: #524D52; border-top-width: 1px; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0; background-color: #ECEEF4" width="161">

<b style="font-weight: bold;"><span>DataGate</span></b> 
</td>
    </tr>

    <tr valign="middle" class="whs8">
        <td valign="top" width="239px" class="whs35" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

Indexed logical files per physical file
</td>
        <td valign="top" width="95px" class="whs36" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

&#160;
</td>
        <td valign="top" width="212" class="whs37" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

249
</td>
        <td valign="top" width="161" class="whs36" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

<code>*NoMax</code>
</td>
    </tr>

    <tr valign="middle" class="whs13">
        <td valign="top" width="239px" class="whs38" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

Imposing 'uniqueness' via select/omit rules in logical files
</td>
        <td valign="top" width="95px" class="whs39" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

Supported
</td>
        <td valign="top" width="212" class="whs40" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

Not directly supported. See <span style="font-weight: bold; color: #000080;"> **work-around** </span><span style="font-weight: bold;"> </span>note below.
</td>
        <td valign="top" width="161" class="whs39" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

Supported
</td>
    </tr>

    <tr valign="middle" class="whs13">
        <td valign="top" width="239px" class="whs38" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

Logical field used as a key field must be based on a physical field with the same name
</td>
        <td valign="top" width="95px" class="whs39" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

No
</td>
        <td valign="top" width="212" class="whs40" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

Yes.&#160; Notice that this eliminates the possibility of using Renamed, Concatenated and Sub-stringed fields as keys. 
</td>
        <td valign="top" width="161" class="whs39" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

No
</td>
   </tr>

    <tr valign="middle" class="whs18">
        <td valign="top" width="239px" class="whs38" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

Maximum number of key fields per key
</td>
        <td valign="top" width="95px" class="whs39" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

&#160;
</td>
        <td valign="top" width="212" class="whs40" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

16
</td>
        <td valign="top" width="161" class="whs39" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

250
</td>
    </tr>

    <tr valign="middle" class="whs41">
        <td valign="top" width="239px" class="whs42" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

Maximum length of key in bytes
</td>
        <td valign="top" width="95px" class="whs43" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

2,000
</td>
        <td valign="top" width="212" class="whs44" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

900
</td>
        <td valign="top" width="161" class="whs39" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding: 0">

250
</td>
    </tr>
</table>

**Work-around:** 

As a work-around to support &quot;Imposing 'uniqueness' via select/omit rules in logical files&quot;: 

1. Change the logical  file definition to allow duplicate keys.
2. Create the logical file.
3. Alter the SQL view with the &quot;<code> **SCHEMABINDING** </code>&quot; attribute.
4. Add a Unique, Clustered Index to the SQL view (logical file).
5. Make sure the &quot;<code> **ARITHABORT** </code>&quot; <code>SET</code> option is on/true for the database.

###  Data Access Considerations 
<table class="normal" style="border-left-style: Solid; border-top-style: Solid; border-right-style: Solid;	border-bottom-style: Solid;	border-left-width: 1px;
				border-right-width: 1px;
				border-top-width: 1px;
				border-bottom-width: 1px;
				margin-left: .15in;
				left: 0px;
				top: 1085px;
				width: 754px;
				border-spacing: 0px;"
        		cellspacing="0"
		        width="754" id="table4" >
    <col class="whs30" />
    <col class="whs47" />
    <col class="whs48" />
    <col class="whs47" />

    <tr valign="middle" class="whs3">
        <td bgcolor="#FFFFDD" valign="top" width="99px" class="whs49" style="border-color:#524D52; border-width:1px; background-color: #ECEEF4">

<b style="font-weight: bold;"><span>Item</span></b>
</td>
        <td bgcolor="#FFFFDD" valign="top" width="149px" class="whs50" style="border-left:1px solid #524D52; background-color: #ECEEF4; border-right-color:#524D52; border-right-width:1px; border-top-color:#524D52; border-top-width:1px; border-bottom-color:#524D52; border-bottom-width:1px">

**DG/400** 
</td>
        <td bgcolor="#FFFFDD" valign="top" width="274px" class="whs51" style="border-left:1px solid #524D52; background-color: #ECEEF4; border-right-color:#524D52; border-right-width:1px; border-top-color:#524D52; border-top-width:1px; border-bottom-color:#524D52; border-bottom-width:1px">

**DSS** 
</td>
        <td bgcolor="#FFFFDD" valign="top" width="149px" class="whs52" style="border-left:1px solid #524D52; background-color: #ECEEF4; border-right-color:#524D52; border-right-width:1px; border-top-color:#524D52; border-top-width:1px; border-bottom-color:#524D52; border-bottom-width:1px">

**DataGate** 
</td>
    </tr>

    <tr valign="middle" class="whs8">
        <td valign="top" width="99px" class="whs53" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Arrival Access
</td>
        <td valign="top" width="149px" class="whs54" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Relative Record Number is used for Sequential and Random access.
</td>
        <td valign="top" width="274px" class="whs55" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Only Consecutive access is supported, but there is no guaranteed order of retrieval unless the file is indexed.&#160; The only random operation allowed is SetLL and this is only when used with *Start and *End. No other kind of seeking (SetGT,CHAIN) is allowed. 
</td>
        <td valign="top" width="149px" class="whs54" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Relative Record Number is used for Sequential and Random access.
</td>
    </tr>

    <tr valign="middle" class="whs13">
        <td valign="top" width="99px" class="whs56" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Format Name (see Note below)
</td>
        <td valign="top" width="149px" class="whs57" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Given by file creator.
</td>
        <td valign="top" width="274px" class="whs58" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

<b style="font-weight: bold;">Always 'R' followed by File Name.</b>

<span style="color: #ff0000;"> Note to AVR Users </span>: The Format can be renamed in the DclDiskFile, using the <code>RNMFMT</code> keyword by providing a new name, it is not necessary to provide the existing Name in the <code>RNMFMT</code>. This allows the creation of single-source apps that can compile against DG/400 and DSS.
</td>
        <td valign="top" width="149px" class="whs57" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Given by File creator.
</td>
    </tr>

    <tr valign="middle" class="whs59">
        <td valign="top" width="99px" class="whs60" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Open Query File
</td>
        <td valign="top" width="149px" class="whs61" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Implemented with OpenQry.
</td>
        <td valign="top" width="274px" class="whs62" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Select expression is used as the <code>WHERE</code> clause of a <code>SELECT</code>.&#160; The key field list is used as the <code>ORDER BY</code> clause. 

The SELECT expression is passed directly to the SQL analyzer with no interpretation.&#160; The expression must follow valid SQL Server syntax.&#160; Pay special attention to uses of logical operators.&#160; Use <code>'AND'</code> and <code>'OR'</code> not '&amp;' and '|'. 
</td>
        <td valign="top" width="149px" class="whs57" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

A temporary logical file is created using the SELECT expression as a <code>SELECT/OMIT</code> expression and the key field list to define the new key.
</td>
    </tr>
</table>

***Note -** &#160;&#160; Multi-format logical files are not supported on SQL Server. The migrated code is normalized for SQL Server especially when I/O commands target single-format record format names instead of the file name but this does **not** change the application's behavior when accessing files on the IBM i.<br /> <br /> If the Rename keyword is present in the legacy file description, the migrated <code>RNMFMT</code> keyword will contain the legacy New Format Name. &#160;If the Rename keyword is **not** present in the legacy file description, the migrated <code>RNMFMT</code> keyword will contain the files Externally Described Record Format name.* 

###  Locking Considerations 

####  **Record Locking** 
**<span style="font-size: 10.0pt;">DG/400</span>** <p class="normal"> DG/400 determines the type and duration of record locks depending on how the file was opened. 

For read-only files, when a record is read, there is no lock requested on it, and if some other application has the record lock, the reading application does not block on the lock, that is, the record is read in spite of being locked by somebody else. 

For files open for update, every time a record is read it is write-locked so that other updating applications cannot read it. The write lock is held until the record is updated or explicitly unlocked by the application or when another record is read or positioned to. 
**<span style="font-size: 10.0pt;">DSS</span>** 

DSS (using server cursors) determines the locking characteristics based on how the file is opened. 

For read-only files DSS behaves like DG/400, that is, locks are neither placed nor considered on records being read. 

The behavior of DSS when the file is opened for update is similar to DG/400 but with <span style="color: #ff0000;"> two significant differences </span>: updating a record does not release the lock on the record and explicitly unlocking a record causes the 'current record position' to be lost. These differences bear the following considerations. 
<table class="MsoNormalTable" style="margin-left: .15in; border-left-style: Solid; border-top-style: Solid;
				border-right-style: Solid; border-bottom-style: Solid; border-left-width: 1px;
				border-right-width: 1px; border-top-width: 1px; border-bottom-width: 1px;
				left: 0px; top: 1772px; width: 754px; border-spacing: 0px; border-spacing: 0px;"
		        cellspacing="0"
		width="754" id="table5" >
    <col class="whs64" />
    <col class="whs64" />
    <col class="whs65" />

    <tr valign="middle" class="whs3">
        <td bgcolor="#FFFFDD" valign="top" width="177px" class="whs66" style="border-color:#524D52; border-width:1px; background-color: #ECEEF4">

**Item** 
</td>
        <td bgcolor="#FFFFDD" valign="top" width="177px" class="whs67" style="border-left:1px solid #524D52; background-color: #ECEEF4; border-right-color:#524D52; border-right-width:1px; border-top-color:#524D52; border-top-width:1px; border-bottom-color:#524D52; border-bottom-width:1px">

**DG/400** 
</td>
        <td bgcolor="#FFFFDD" valign="top" width="448px" class="whs68" style="border-left:1px solid #524D52; background-color: #ECEEF4; border-right-color:#524D52; border-right-width:1px; border-top-color:#524D52; border-top-width:1px; border-bottom-color:#524D52; border-bottom-width:1px">

**DSS** 
</td>
	</tr>

    <tr valign="middle" class="whs8">
        <td valign="top" width="177px" class="whs69" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Unlock Record 
</td>
        <td valign="top" width="177px" class="whs70" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Cursor position is unchanged. 
</td>
        <td valign="top" width="387px" class="whs71" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

The file has no 'current' position after the *Unlock.* 
</td>
    </tr>

    <tr valign="middle" class="whs13">
        <td valign="top" width="177px" class="whs73" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Update Record 
</td>
        <td valign="top" width="177px" class="whs74" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

The record just updated is released. 
</td>
        <td valign="top" width="387px" class="whs75" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

The record just updated is kept locked. 
</td>
    </tr>

    <tr valign="middle" class="whs18">
        <td valign="top" width="177px" class="whs73" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

<code> **NoLock* </code> option on *Read* operations 
</td>
        <td valign="top" width="177px" class="whs74" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Supported but deprecated. 
</td>
        <td valign="top" width="387px" class="whs75" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Unsupported. 

The better way to achieve this is to open the file twice, once for input only and the other for update. Where the read appears with the <code>*NoLock</code> option, the file should be substituted with the one open for input only. By doing this, the application can take advantage of network blocking - yielding better performance. 
</td>
    </tr>
    <tr valign="middle" class="whs19">
        <td valign="top" width="177px" class="whs73" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Range operations 
</td>
        <td valign="top" width="177px" class="whs74" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

When the end of the range is reached, the file has no 'current' position. 
</td>
        <td valign="top" width="387px" class="whs75" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

When the end of the range is reached, the file has no 'current' position. 
</td>
    </tr>
    <tr valign="middle" class="whs20">
        <td valign="top" width="177px" class="whs73" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Hit <code>EOF</code> on a <code>ReadE (P)</code> 
</td>
        <td valign="top" width="177px" class="whs74" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Lose Record position. 
</td>
        <td valign="top" width="387px" class="whs75" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Lose Record position. 
</td>
    </tr>

    <tr valign="middle" class="whs76">
        <td valign="top" width="177px" class="whs77" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Other Operations like <code>SetLL</code> 
</td>
        <td valign="top" width="177px" class="whs78" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Unlock Record. 
</td>
        <td valign="top" width="387px" class="whs75" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px">

Unlock Record. 
</td>
    </tr>
</table>

Loops involving <code>SetLL/SetGT</code> and <code>Read/ReadE/ReadPE</code> should be re-coded to use the Range operations. 

The most demanding change is the one requiring segments of code involving <code>CHAIN-UPDATE</code>.&#160; Combinations have to be studied and possibly modified.&#160; 

- If the <code>CHAIN-UPDATE</code> happens in a tight loop, then at the end of the loop an <code>UNLOCK</code> should be issued to release the last record updated. 
            Note however that the record position will be lost after the <code>UNLOCK</code>.
- If the <code>CHAIN-UPDATE</code> is sprinkled throughout the code, then each case has to be closely studied.

####  Object Locking 
For DSS, object locking is implemented only for Data Area objects. 

**Field Considerations** <table class="MsoNormalTable" cellspacing="0" width="752" id="table6" style="border: 1px solid #524D52; padding-left: 4px; padding-right: 4px; padding-top: 1px; padding-bottom: 1px"> <col class="whs82" /> <col class="whs83" /> <col class="whs83" /> <col class="whs83" /> <tr valign="top" class="whs84"> <td bgcolor="#FFFFDD" width="19%" class="whs85" style="border-color:#524D52; background-color: #ECEEF4; padding-left:4px; padding-right:4px"> <p class="normal" align="center" style="margin-left: 9px"> **ITEM** 
</td>
        <td bgcolor="#FFFFDD" width="27%" class="whs87" style="background-color: #ECEEF4; border-left-style:solid; border-left-width:1px; border-right-color:#524D52; border-top-color:#524D52; border-bottom-color:#524D52; padding-left:4px; padding-right:4px">

**DG/400** 
</td>
        <td bgcolor="#FFFFDD" width="27%" class="whs87" style="background-color: #ECEEF4; border-left-style:solid; border-left-width:1px; border-right-color:#524D52; border-top-color:#524D52; border-bottom-color:#524D52; padding-left:4px; padding-right:4px">

**DSS** 
</td>
        <td bgcolor="#FFFFDD" width="27%" class="whs88" style="background-color: #ECEEF4; border-left-style:solid; border-left-width:1px; border-right-color:#524D52; border-top-color:#524D52; border-bottom-color:#524D52; padding-left:4px; padding-right:4px">

**DataGate** 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs90" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Field Name Length 
</td>
        <td width="27%" class="whs92" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

10 Characters 
</td>
        <td width="27%" class="whs92" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

31 Characters 
</td>
        <td width="27%" class="whs92" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

31 Characters 
</td>
    </tr>
    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Supported 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">
            &#160;
        </td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">
            &#160;
        </td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

&#160; 
</td>
    </tr>
    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

- Char 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*CHAR</code> 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

char 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*CHAR</code> 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

- Packed 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*PACKED</code> 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

decimal 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*PACKED</code> 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

- Zoned 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*ZONED</code> 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

numeric 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*ZONED</code> 
</td>
    </tr>
    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

- Binary 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*BINARY</code> 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

numeric 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*BINARY</code> 
</td>
    </tr>
    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

- Float 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*FLOAT</code> 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Float(4): float 

Float(8): real 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*FLOAT</code> 
</td>
    </tr>
    <tr>
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

- Integer 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*INTEGER</code> 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Integer(2): smallint 

Integer(4): int 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*INTEGER</code> 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

- Date 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*DATE</code> 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>ASNA_DSS.DATE</code> 

datetime: 00:00:00 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*DATE</code> 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

- Time 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*TIME</code> 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>ASNA_DSS.TIME</code> 

<code>datetime: 1899/12/30</code> 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*TIME</code> 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

- Timestamp 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*TIMESTAMP</code> 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

datetime 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*TIMESTAMP</code> 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

- Hex 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*HEX</code> 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

binary 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*HEX</code> 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

- DBCS 
</td>
    <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*DBCS</code> 
</td>
    <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

nchar 
</td>
    <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*DBCS</code> 
</td>
 </tr>
    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

- Unicode 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*DBCS</code> 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

nchar 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*DBCS</code> 
</td>
    </tr>

<tr valign="top" class="whs89">
    <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

- Boolean 
</td>
    <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*CHAR(1)</code> 
</td>
    <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Bit 
</td>
    <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

<code>*CHAR(1)</code> 
</td>
 </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Allows Nulls 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Yes 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Yes 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

No 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Variable length Field 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Char 

Hex 

Dbcs 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

varchar 

varbinary 

varnchar 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

No 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Date value range 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

0001-01-01 to 

9999-12-31 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Datetime: 1753-01-01 to 9999-12-31 (0001-01-01 maps to 1753-01-01) 

Smalldatetime: 1900-01-01 to 2079-06-06 

&#160; 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

00001-01-01 to 

9999-12-31 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Decimal number storage 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Packed: 1 nibble per digit 

Zoned: 1 byte per digit 

Binary 1 - 4 digits: 2 bytes 

Binary 5 - 9 digits: 4 bytes 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Decimal / Numeric 

1 - 9 digits: 4 + 1 bytes 

10 - 19 digits: 8 + 1 bytes 

20 - 29 digits: 12 + 1 bytes 

30 - 38 digits: 16 &#160;+1 bytes 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Packed: 1 nibble per digit 

Zoned: 1 byte per digit 

Binary 1 - 4 digits: 2 bytes 

Binary 5 - 9 digits: 4 bytes 
</td>
   </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Data storage 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

1 byte per digit / character 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Datetime: 8 bytes 

ASNA_DSS_DATE: 8 bytes 

SmallDatetime: 4 bytes 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

1 byte per digit / character 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Fields per file 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

&#160; 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

1,024 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

32,000 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Re-typing logical fields 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Unrestricted 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Logical fields whose type differs from that of the corresponding physical field cannot be updated 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Unrestricted 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Column Heading Definitions 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Up to 3 31 characters 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

The 3 headings are concatenated into the MS Access CAPTION field 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Up to 3 31 characters 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="19%" class="whs93" style="border-left-color: #524D52; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Text Description 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Up to 49 characters 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Up to 49 characters 
</td>
        <td width="27%" class="whs94" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; padding-left: 4px; padding-right: 4px">

Up to 49 characters 
</td>
    </tr>
</table>

###  Native SQL Server field interpretation 
<table class="MsoNormalTable" cellspacing="0" width="754" id="table7" style="border: 1px solid #524D52; padding-left: 4px; padding-right: 4px; padding-top: 1px; padding-bottom: 1px"> <col class="whs97" /> <col class="whs97" /> <col class="whs97" /> <col class="whs97" /> <col class="whs97" /> <col class="whs97" /> <tr valign="top" class="whs84"> <td colspan="2" bgcolor="#FFFFDD" width="226px" class="whs98" style="border-width:1px; background-color: #ECEEF4" > <p align="center" class="normal"> **Numerics** 
</td>
        <td colspan="2" bgcolor="#FFFFDD" width="226px" class="whs100" style="background-color: #ECEEF4; border-left-style:solid; border-left-width:1px; border-right-width:1px; border-top-width:1px; border-bottom-width:1px" >

**Date/Time** 
</td>
        <td colspan="2" bgcolor="#FFFFDD" width="226px" class="whs102" style="background-color: #ECEEF4; border-left-style:solid; border-left-width:1px; border-right-width:1px; border-top-width:1px; border-bottom-width:1px" >

**Char/Other** 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="113px" class="whs103" style="border-left-width: 1px; border-right-style: solid; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

Float 
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

*Float(4) 
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px" >

DateTime 
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

*Timestamp 
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px; padding-left: 4px; padding-right: 4px" >

Bit 
</td>
        <td width="113px" class="whs107" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px" >

*Boolean 
</td>
   </tr>

    <tr valign="top" class="whs89">
        <td width="113px" class="whs103" style="border-left-width: 1px; border-right-style: solid; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

Real 
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

*Float (8) 
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px" >

SmallDateTime 
</td>

        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

*Timestamp 
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px; padding-left: 4px; padding-right: 4px" >

Char 
</td>
        <td width="113px" class="whs108" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px" >

*Char 
</td>
   </tr>

    <tr valign="top" class="whs89">
        <td width="113px" class="whs103" style="border-left-width: 1px; border-right-style: solid; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

Int 
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

*Integer (4) 
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px" >

&#160; 
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

&#160; 
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px; padding-left: 4px; padding-right: 4px" >

VarChar 
</td>
        <td width="113px" class="whs107" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px" >

*Char (VarLen) 
</td>
   </tr>

    <tr valign="top" class="whs89">
        <td width="113px" class="whs103" style="border-left-width: 1px; border-right-style: solid; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

SmallInt 
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

*Integer (2) 
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px" >

&#160; 
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

&#160;
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px; padding-left: 4px; padding-right: 4px" >

NChar 
</td>
        <td width="113px" class="whs107" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px" >

*Unicode 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="113px" class="whs103" style="border-left-width: 1px; border-right-style: solid; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

TinyInt 
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

*Integer (2) 
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px" >

&#160; 
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

&#160; 
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px; padding-left: 4px; padding-right: 4px" >

NVarChar 
</td>
        <td width="113px" class="whs107" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px" >

*Unicode (VarLen) 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="113px" class="whs103" style="border-left-width: 1px; border-right-style: solid; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

Decimal 
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

*Packed 
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px" >

&#160;
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

&#160;
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px; padding-left: 4px; padding-right: 4px" >

Binary 
</td>
        <td width="113px" class="whs107" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px" >

*Hex 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="113px" class="whs103" style="border-left-width: 1px; border-right-style: solid; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

BigInt 
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

*Zoned (19,0) 
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px" >

&#160;
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

&#160;
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px; padding-left: 4px; padding-right: 4px" >

VarBinary 
</td>
        <td width="113px" class="whs107" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px" >

*Hex (VarLen) 
</td>
   </tr>

    <tr valign="top" class="whs89">
        <td width="113px" class="whs103" style="border-left-width: 1px; border-right-style: solid; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

Money 
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

*Zoned (19,4) 
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px" >

&#160;
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

&#160;
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px; padding-left: 4px; padding-right: 4px" >

UniqueIdentifier 
</td>
        <td width="113px" class="whs107" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px" >

*Hex (16) 
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="113px" class="whs103" style="border-left-width: 1px; border-right-style: solid; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

Numeric 
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

*Zoned 
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px" >

&#160;
</td>
        <td width="113px" class="whs105" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px" >

&#160;
</td>
        <td width="113px" class="whs106" style="border-style: solid; border-width: 1px; padding-left: 4px; padding-right: 4px" >

&#160;
</td>
        <td width="113px" class="whs107" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-style: solid; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px" >

&#160;
</td>
    </tr>

    <tr valign="top" class="whs89">
        <td width="113px" class="whs111" style="border-left-width: 1px; border-right-style: solid; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-width: 1px" >

SmallMoney 
</td>
        <td width="113px" class="whs112" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-width: 1px" >

*Zoned (9,4) 
</td>
        <td width="113px" class="whs113" style="border-left-style: solid; border-left-width: 1px; border-right-style: solid; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-width: 1px" >

&#160;
</td>
        <td width="113px" class="whs112" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-width: 1px" >

&#160;
</td>
        <td width="113px" class="whs113" style="border-left-style: solid; border-left-width: 1px; border-right-style: solid; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px" >

&#160;
</td>
        <td width="113px" class="whs114" style="border-left-style: solid; border-left-width: 1px; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px" >

&#160;
</td>
    </tr>
</table>

The types **Image, Text, and NText** are not supported; nor are their replacements <code> **VARBINARY(MAX), VARCHAR(MAX), and NVARCHAR(MAX)** </code>.&#160; Fields of these types are hidden from the file definition. &#160;You will be able to display the file definition in DataGate&#174; Studio but will not be able to open the file. To ensure future application compatibility, you should not use files containing these field types.&#160; Instead, you should create logical files naming the individual fields that your application will manipulate.&#160; That way, if in a future release the fields 'appear', your application will not break. 

###  Join Considerations 
<table class="MsoNormalTable" style=" border-left-style: Solid; border-top-style: Solid; border-right-style: Solid; border-bottom-style: Solid; border-left-width: 1px; border-right-width: 1px; border-top-width: 1px; border-bottom-width: 1px; margin-left: .15in; left: 0px; top: 3685px; width: 754px; border-spacing: 0px; border-spacing: 0px;" cellspacing="0" width="754" id="table8" > <col /> <col /> <col class="whs115" /> <col class="whs30" /> <tr valign="middle" class="whs3"> <td bgcolor="#FFFFDD" valign="top" width="1.506in" class="whs116" style="border-color:#524D52; border-width:1px; background-color: #ECEEF4; padding-left:4px; padding-right:4px; padding-top:1px; padding-bottom:1px"> <p class="normal" style="margin-right: 0in; margin-left: 0in; text-align: center; font-size: 10pt; align: center;"> **Item** 
</td>
        <td bgcolor="#FFFFDD" valign="top" width="123.6pt" class="whs117" style="border-left:1px solid #524D52; background-color: #ECEEF4; border-right-color:#524D52; border-right-width:1px; border-top-color:#524D52; border-top-width:1px; border-bottom-color:#524D52; border-bottom-width:1px; padding-left:4px; padding-right:4px; padding-top:1px; padding-bottom:1px">

**DG/400** 
</td>
        <td bgcolor="#FFFFDD" valign="top" width="251px" class="whs118" style="border-left:1px solid #524D52; background-color: #ECEEF4; border-right-color:#524D52; border-right-width:1px; border-top-color:#524D52; border-top-width:1px; border-bottom-color:#524D52; border-bottom-width:1px; padding-left:4px; padding-right:4px; padding-top:1px; padding-bottom:1px">

**DSS** 
</td>
        <td bgcolor="#FFFFDD" valign="top" width="95px" class="whs119" style="border-left:1px solid #524D52; background-color: #ECEEF4; border-right-color:#524D52; border-right-width:1px; border-top-color:#524D52; border-top-width:1px; border-bottom-color:#524D52; border-bottom-width:1px; padding-left:4px; padding-right:4px; padding-top:1px; padding-bottom:1px">

**DataGate** 
</td>
    </tr>

    <tr valign="middle" class="whs8">
        <td valign="top" width="1.506in" class="whs120" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px; padding-top: 1px; padding-bottom: 1px">

Supports Use Default for Joins by: 
</td>
        <td valign="top" width="123.6pt" class="whs121" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px; padding-top: 1px; padding-bottom: 1px">

DDS Keyword <code>JOINDFLT??</code> 

When a record is not found in the secondary file, logical fields whose base is that file will be populated with the default values specified in the physical file definition. 
</td>
        <td valign="top" width="251px" class="whs122" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px; padding-top: 1px; padding-bottom: 1px">

Creating a Left Outer Join instead of an Inner Join. 

From SQL Docs: 

*<code>LEFT JOIN</code> or <code>LEFT OUTER JOIN</code>* 

<i style="font-style: italic;"> The result set of a left outer join includes all the rows from the left table specified in the <code>LEFT OUTER</code> clause, not just the ones in which the joined columns match. When a row in the left table has no matching rows in the right table, the associated result set row contains null values for all select list columns coming from the right table.</i> 
</td>

        <td valign="top" width="95px" class="whs123" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px; padding-top: 1px; padding-bottom: 1px">

Yes 
</td>
   </tr>

    <tr valign="middle" class="whs124">
        <td valign="top" width="1.506in" class="whs125" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px; padding-top: 1px; padding-bottom: 1px">

Supports 'Join Duplicates By' 
</td>
        <td valign="top" width="123.6pt" class="whs126" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px; padding-top: 1px; padding-bottom: 1px">

DDS Keyword <code>JDUP</code> 
</td>
        <td valign="top" width="251px" class="whs127" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px; padding-top: 1px; padding-bottom: 1px">

Not supported.&#160;Duplicate rows in the 'secondary' tables may be returned in random order. 
</td>
        <td valign="top" width="95px" class="whs128" style="border-left: 1px solid #524D52; border-right-color: #524D52; border-right-width: 1px; border-top: 1px solid #524D52; border-bottom-color: #524D52; border-bottom-width: 1px; padding-left: 4px; padding-right: 4px; padding-top: 1px; padding-bottom: 1px">

Yes 
</td>
    </tr>
</table>

<br />

###  Calling Programs/Procedures Considerations 
<table class="MsoNormalTable" style="border-left-style: Solid; border-top-style: Solid; border-right-style: Solid; border-bottom-style: Solid; border-left-width: 1px;
				border-right-width: 1px; border-top-width: 1px; border-bottom-width: 1px; margin-left: .15in;
				left: 0px; top: 3962px; width: 754px; border-spacing: 0px; border-spacing: 0px;"
		cellspacing="0"	width="754" id="table9" >
    <col class="whs129" />
    <col class="whs130" />
    <col class="whs130" />
    <col class="whs130" />

    <tr valign="middle" class="whs3">
        <td bgcolor="#FFFFDD" valign="top" width="191px" class="whs131" style="border-color:#524D52; border-width:1px; background-color: #ECEEF4">

**Item** 
</td>
        <td bgcolor="#FFFFDD" valign="top" width="167px" class="whs132" style="background-color: #ECEEF4; border-left-style:solid; border-left-width:1px; border-right-color:#524D52; border-right-width:1px; border-top-color:#524D52; border-top-width:1px; border-bottom-color:#524D52; border-bottom-width:1px">

**DG/400** 
</td>
        <td bgcolor="#FFFFDD" valign="top" width="167px" class="whs132" style="background-color: #ECEEF4; border-left-style:solid; border-left-width:1px; border-right-color:#524D52; border-right-width:1px; border-top-color:#524D52; border-top-width:1px; border-bottom-color:#524D52; border-bottom-width:1px">

**DSS** 
</td>
        <td bgcolor="#FFFFDD" valign="top" width="167px" class="whs133" style="background-color: #ECEEF4; border-left-style:solid; border-left-width:1px; border-right-color:#524D52; border-right-width:1px; border-top-color:#524D52; border-top-width:1px; border-bottom-color:#524D52; border-bottom-width:1px">

**DataGate** 
</td>
    </tr>

    <tr valign="middle" class="whs8">
        <td valign="top" width="191px" class="whs134" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; border-bottom-width: 1px">

Maximum Number of Parameters 
</td>
        <td valign="top" width="167px" class="whs135" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; border-bottom-width: 1px">

36 
</td>
        <td valign="top" width="167px" class="whs135" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; border-bottom-width: 1px">

1024 
</td>
        <td valign="top" width="167px" class="whs135" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; border-bottom-width: 1px">

N/A 
</td>
    </tr>

    <tr valign="middle" class="whs124">
        <td valign="top" width="191px" class="whs136" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; border-bottom-width: 1px">

Maximum Length of Stored Procedure Name 
</td>
        <td valign="top" width="167px" class="whs137" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; border-bottom-width: 1px">

N/A 
</td>
        <td valign="top" width="167px" class="whs137" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; border-bottom-width: 1px">

31 
</td>
        <td valign="top" width="167px" class="whs138" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; border-bottom-width: 1px">

N/A 
</td>
    </tr>

    <tr valign="middle" class="whs124">
        <td valign="top" width="191px" class="whs136" style="border-left-color: #524D52; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; border-bottom-width: 1px">

Parameter Direction 
</td>
        <td valign="top" width="167px" class="whs137" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; border-bottom-width: 1px">

*Input, *Output, *Both 
</td>
        <td valign="top" width="167px" class="whs137" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; border-bottom-width: 1px">

*Input, *Both 
</td>
        <td valign="top" width="167px" class="whs138" style="border-left-style: solid; border-left-width: 1px; border-right-color: #524D52; border-right-width: 1px; border-top-style: solid; border-top-width: 1px; border-bottom-color: #524D52; border-bottom-width: 1px">

N/A 
</td>
   </tr>
</table>

