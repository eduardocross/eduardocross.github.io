---
title: CLProgram.OverrideFile(string, OverrideOptions, object, OverrideScope)

Id: amfCLProgramClassOverrideFileMethod2
TocParent: amfCLProgramClassOverrideFileMethods
TocOrder: 20

keywords: enumerations [ASNA.Monarch], OverrideOptions, used by
keywords: OverrideOptions enumeration, used by
keywords: enumerations [ASNA.Monarch], OverrideScope, used by
keywords: OverrideScope enumeration, used by

---

This method provides CLProgram file override options within Monarch for the specified level of scope.

#### Syntax
<pre class="syntax"> **BegSr OverrideFile Access(*Public) Type(Void)
   DclSrParm *fileName*  Type(*String)
   DclSrParm *option*    Type([ASNA.Monarch.OverrideOptions](amfOverrideOptionsEnumeration.html))
   DclSrParm *newValue*  Type(*Object)
   DclSrParm *scope*     Type([ASNA.Monarch.OverrideScope](amfOverrideScopeEnumeration.html))**       </pre>

#### Parameters
<dl>
        <dt>
          <code> *fileName* </code>
        </dt>
        <dd>

String containing the database file name to be overridden.
</dd>
        <dt>
          <code> *option* </code>
        </dt>
        <dd>

**ASNA.Monarch.OverrideOptions** . The option being overridden as noted in the table below.
</dd>
        <dt>
          <code> *newValue* </code>
        </dt>
        <dd>

Object. The new value to override the existing option value. The value type must be as indicated below.
</dd>
        <dt>
          <code> *scope* </code>
        </dt>
        <dd>

**ASNA.Monarch.OverrideScope** . The level the override is being applied to (Job or CallLvl).
</dd>
</dl>

#### Remarks
The following table details the member name, the value type, and the valid option values for the different types of files.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup >
            <col style="FONT-WEIGHT: bold" width="10%" />
            <col width="10%" />
            <col width="70%" />
            <col width="10%" />
          </colgroup>
          <tr>
            <th>Member</th>
            <th>Value
            <br clear="none" />Type</th>
            <th>Description</th>
            <th>Applies To</th>
          </tr>
          <tr>
            <td><code>ToFile</code></td>
            <td>System.String</td>
            <td>The new file object. In the
            case of WorkStnFile, this refers to the ASP.Net page
            path name.</td>
            <td><code>DBFile
            <br clear="none" />WorkStnFile
            <br clear="none" />PrintFile</code></td>
          </tr>
          <tr>
            <td><code>Mbr</code></td>
            <td>System.String</td>
            <td>              <span>The member name of the database
              file.</span>
            </td>
            <td><code>DBFile</code></td>
          </tr>
          <tr>
            <td><code>WaitRcd</code></td>
            <td>System.Int32</td>
            <td>Time, in seconds, specifying the waiting period for a record.</td>
            <td><code>DBFile</code></td>
          </tr>
          <tr>
            <td><code>Collate</code></td>
            <td>Boolean</td>
            <td> **True/False** . Indicates the output
            produced by capable printers should be collated when
            this property is set to 
 **True** . Applicable only when printing
            multiple copies, or when the 
 **Copies**  is &gt;1.</td>
            <td><code>PrintFile</code></td>
          </tr>
          <tr>
            <td><code>Copies</code></td>
            <td>System.Int32</td>
            <td>The number of copies to
            print. See also 
            <code> **Collate** </code>.</td>
            <td><code>PrintFile</code></td>
          </tr>
          <tr>
            <td><code>Duplex</code></td>
            <td />
            <td>Enumerated constant
            defining values on duplex (double-sided) printing
            options.</td>
            <td><code>PrintFile</code></td>
          </tr>
          <tr>
            <td><code>FormName</code></td>
            <td>System.String</td>
            <td>The name of the print
            format to use, such as "A4", "Letter", "Tabloid", etc.
            See 
            <code> **PaperSize** </code> for available print form names.</td>
            <td><code>PrintFile</code></td>
          </tr>
          <tr>
            <td><code>Orientation</code></td>
            <td/>
            <td>Enumerated constant
            defining the landscape or portrait orientation of paper
            in the printer.</td>
            <td><code>PrintFile</code></td>
          </tr>
          <tr>
            <td><code>PaperLength</code></td>
            <td>System.Int32</td>
            <td>The paper length based upon
            the 
            <code> **Orientation** </code> of the paper in the
            printer. These values are in tenths of a
            millimeter.</td>
            <td><code>PrintFile</code></td>
          </tr>
          <tr>
            <code><td>PaperSize</td></code>
            <td/>
            <td>Enumerated constant
            defining the size of paper.</td>
            <td><code>PrintFile</code></td>
          </tr>
          <tr>
            <td><code>PaperSource</code></td>
            <td/>
            <td>Enumerated constant
            defining values on the printer tray that will be
            used.</td>
            <td><code>PrintFile</code></td>
          </tr>
          <tr>
            <td><code>PaperWidth</code></td>
            <td>System.Int32</td>
            <td>The paper width based upon the 
            <code> **Orientation** </code> of the paper in the
            printer. Values are in tenths of a millimeter.</td>
            <td><code>PrintFile</code></td>
          </tr>
          <tr>
            <td><code>Printer</code></td>
            <td>System.String</td>
            <td>The complete path and name
            of the printer. For example, if the printer is on a
            network, you must specify the network, then the printer
            name. For example, " **\\Network\HP LaserJet
            5M** ".</td>
            <td><code>PrintFile</code></td>
          </tr>
          <tr>
            <td><code>Quality</code></td>
            <td/>
            <td>Enumerated constant
            defining values for the quality rating for output
            produced by the printer.</td>
            <td><code>PrintFile</code></td>
          </tr>
          <tr>
            <td><code>ReportName</code></td>
            <td>System.String</td>
            <td>The name of the report as
            seen on the printer spool.</td>
            <td><code>PrintFile</code></td>
          </tr>
          <tr>
            <td><code>Scale</code></td>
            <td>System.Int32</td>
            <td>The percentage factor by
            which the printed output is to be scaled. The printer
            must support the output to be scaled or resized.</td>
            <td><code>PrintFile</code></td>
          </tr>
          <tr>
            <td><code>ShareOpenDataPath</code></td>
            <td>Boolean</td>
            <td> **True/False** . Indicator if the display
            file (active server page) used by this 
            <code> **WorkStnFile** </code> allows any other to refer
            to the same display file.</td>
            <td><code>WorkStnFile</code></td>
          </tr>
</table>

<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[CLProgram Class](amfCLProgramClass.html) <br clear="none" /> [ CLProgram Class Members](amfCLProgramClassMembers.html) <br clear="none" /> [ DeleteOverride Method](amfCLProgramClassDeleteOverrideMethods.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
