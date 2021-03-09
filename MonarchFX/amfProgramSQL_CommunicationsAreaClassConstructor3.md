---
title: Program.SQL_CommunicationsArea Constructor (string,int,int,System.Exception)

Id: amfProgramSQL_CommunicationsAreaClassConstructor3
TocParent: amfProgramSQL_CommunicationsAreaClassConstructors
TocOrder: 30

---

Constructs a new instance of a **SQL_CommunicationsArea** object with command text, execution status code and state, and systems exception.

#### Syntax
<pre class="syntax"> **BegConstructor SQL_CommunicationsArea
   DclSrParm *cmdText*  Type(*string)
   DclSrParm *iSeriesCode*  Type(*Integer)
   DclSrParm *iSeriesState*  Type(*Integer)
   DclSrParm *e*  Type(System.Exception)**       </pre>

#### Parameters
<dl>
        <dt>
 *cmdText* 
        </dt>
        <dd>String. The actual command text.</dd>
        <dt>
 *iSeriesCode* 
        </dt>
        <dd>Integer. The execution code.</dd>
        <dt>
 *iSeriesState* 
        </dt>
        <dd>Integer. The execution state.</dd>
        <dt>
 *e* 
        </dt>
        <dd>
 **System.Exception** .</dd>
</dl>

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td>[ASNA.Monarch](amfMonarchNamespace.html)</td>
          </tr>
          <tr>
            <td>Assembly:</td>
            <td>ASNA.VisualRPG.Runtime.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ Program.SQL_CommunicationsArea Class](amfProgramSQL_CommunicationsAreaClass.html) <br /> [ Program.SQL_CommunicationsArea Class Members](amfProgramSQL_CommunicationsAreaClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
