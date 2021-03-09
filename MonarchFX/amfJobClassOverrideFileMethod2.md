---
title: Job.OverrideFile Method(string,OverrideOptions,object,OverrideScope)

Id: amfJobClassOverrideFileMethod2
TocParent: amfJobClassOverrideFileMethods
TocOrder: 20

keywords: FileOverrideOptionMismatch
keywords: enumerations [ASNA.Monarch], OverrideOptions, used by
keywords: OverrideOptions enumeration, used by
keywords: enumerations [ASNA.Monarch], OverrideScope, used by
keywords: OverrideScope enumeration, used by

---

This method provides Job file override options within Monarch for the specified level of scope.

#### Syntax
<pre class="prettyprint"> **BegSr OverrideFile Access(*Public) Type(Void)
   DclSrParm *fileName*  Type(*String)
   DclSrParm *option*    Type([ASNA.Monarch.OverrideOptions](amfOverrideOptionsEnumeration.html))
   DclSrParm *newValue*  Type(*Object)
   DclSrParm *scope*     Type([ASNA.Monarch.OverrideScope](amfOverrideScopeEnumeration.html))** 
      </pre>

#### Parameters
<dl>
        <dt>
 *fileName* 
        </dt>
        <dd>

String containing the database file name to be overridden.
</dd>
        <dt>
 *option* 
        </dt>
        <dd>

**ASNA.Monarch.OverrideOptions** . The option being overridden as noted in the table below.
</dd>
        <dt>
 *newValue* 
        </dt>
        <dd>

Object. The new value to override the existing option value. The value type must be as indicated below.
</dd>
        <dt>
 *scope* 
        </dt>
        <dd>

**ASNA.Monarch.OverrideScope** . The level the override is being applied to (Job or CallLvl).
</dd>
</dl>

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0">
          <colgroup span="1">
            <col style="FONT-WEIGHT: bold;WIDTH: 50%" />
            <col style="WIDTH: 50%" />
          </colgroup>
          <tr>
            <th>Value</th>
            <th>Condition</th>
          </tr>
          <tr>
            <td>            FileOverrideOptionMismatch</td>
            <td>The option to override
            could not be performed (type mismatch).</td>
          </tr>
</table>

#### Remarks
The following table details the **OverrideOptions** , the value type, and the valid option values for the different types of files.
<table class="mytable"  cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col style="FONT-WEIGHT: bold" width="10%" />
            <col width="20%" />
            <col width="70%" />
            <col width="10%" />
          </colgroup>
          <tr>
            <th>Member</th>
            <th>Value
            <br />Type</th>
            <th>Description</th>
            <th>Applies To</th>
          </tr>
          <tr>
            <td>ToFile</td>
            <td>System.String</td>
            <td>The new file object. In the
            case of WorkStnFile, this refers to the ASP.Net page
            path name.</td>
            <td>DBFile
            <br />WorkStnFile
            <br />PrintFile</td>
          </tr>
          <tr>
            <td>Mbr</td>
            <td>System.String</td>
            <td>The name of the physical
            file member within the 
 *fileName* . The name of the member can be: 
- *FIRST: The first member in the
              database file.
- *LAST: The last member of the
              database file.
- *physical-file-member* : Specify the name of
              the physical file member.

</td>
            <td>DBFile</td>
          </tr>
          <tr>
            <td>WaitRcd</td>
            <td>System.Int32</td>
            <td>Time, in seconds,
            specifying the waiting period for a record.</td>
            <td>DBFile</td>
          </tr>
          <tr>
            <td>Collate</td>
            <td>Boolean</td>
            <td> **True/False** . Indicates the output
            produced by capable printers should be collated when
            this property is set to 
 **True** . Applicable only when printing
            multiple copies, or when the 
 **Copies**  is &gt;1.</td>
            <td>PrintFile</td>
          </tr>
          <tr>
            <td>Copies</td>
            <td>System.Int32</td>
            <td>The number of copies to
            print. See also 
 **Collate** .</td>
            <td>PrintFile</td>
          </tr>
          <tr>
            <td>Duplex</td>
            <td />
            <td>Enumerated constant
            defining values on duplex (double-sided) printing
            options.</td>
            <td>PrintFile</td>
          </tr>
          <tr>
            <td>FormName</td>
            <td>System.String</td>
            <td>The name of the print
            format to use, such as "A4", "Letter", "Tabloid", etc.
            See 
 **PaperSize**  for available print form names.</td>
            <td>PrintFile</td>
          </tr>
          <tr>
            <td>Orientation</td>
            <td />
            <td>Enumerated constant
            defining the landscape or portrait orientation of paper
            in the printer.</td>
            <td>PrintFile</td>
          </tr>
          <tr>
            <td>PaperLength</td>
            <td>System.Int32</td>
            <td>The paper length based upon
            the 
 **Orientation**  of the paper in the
            printer. These values are in tenths of a
            millimeter.</td>
            <td>PrintFile</td>
          </tr>
          <tr>
            <td>PaperSize</td>
            <td />
            <td>Enumerated constant
            defining the size of paper.</td>
            <td>PrintFile</td>
          </tr>
          <tr>
            <td>PaperSource</td>
            <td

 />
            <td>Enumerated constant
            defining values on the printer tray that will be
            used.</td>
            <td>PrintFile</td>
          </tr>
          <tr>
            <td>PaperWidth</td>
            <td>System.Int32</td>
            <td>The paper width based upon
            the 
 **Orientation**  of the paper in the
            printer. Values are in tenths of a millimeter.</td>
            <td>PrintFile</td>
          </tr>
          <tr>
            <td>Printer</td>
            <td>System.String</td>
            <td>The complete path and name
            of the printer. For example, if the printer is on a
            network, you must specify the network, then the printer
            name. For example, "
            <span style="FONT-WEIGHT: bold">\\Network\HP LaserJet
            5M</span>".</td>
            <td>PrintFile</td>
          </tr>
          <tr>
            <td>Quality</td>
            <td />
            <td>Enumerated constant
            defining values for the quality rating for output
            produced by the printer.</td>
            <td>PrintFile</td>
          </tr>
          <tr>
            <td>ReportName</td>
            <td>System.String</td>
            <td>The name of the report as
            seen on the printer spool.</td>
            <td>PrintFile</td>
          </tr>
          <tr>
            <td>Scale</td>
            <td>System.Int32</td>
            <td>The percentage factor by
            which the printed output is to be scaled. The printer
            must support the output to be scaled or resized.</td>
            <td>PrintFile</td>
          </tr>
          <tr>
            <td>ShareOpenDataPath</td>
            <td>Boolean</td>
            <td> **True/False** . Indicator if the display
            file (active server page) used by this 
 **WorkStnFile**  allows any other to refer
            to the same display file.</td>
            <td>WorkStnFile</td>
          </tr>
</table>

<!-- start -->

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
            <td>ASNA.VisualRPG.Runtime.</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td>Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[Job Class](amfJobClass.html) <br /> [Job Class Members](amfJobMembers.html) <br />[ Job.ApplyOverrides Methods](amfJobClassApplyOverridesMethods.html)<br />[ Job.DeleteOverride Methods](amfJobClassDeleteOverrideMethods.html) <br />[ASNA.Monarch Namespace](amfMonarchNamespace.html)
