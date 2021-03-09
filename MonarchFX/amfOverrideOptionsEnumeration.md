---
title: OverrideOptions Enumeration

Id: amfOverrideOptionsEnumeration
TocParent: amfMonarchNamespaceEnumerations
TocOrder: 40

keywords: enumerations [ASNA.Monarch], OverrideOptions
keywords: OverrideOptions enumeration
keywords: file overrides, options
keywords: Collate enumeration member
keywords: Copies enumeration member
keywords: Duplex enumeration member
keywords: FormName enumeration member
keywords: Mbr enumeration member
keywords: Orientation enumeration member
keywords: PaperLength enumeration member
keywords: PaperSize enumeration member
keywords: PaperSource enumeration member
keywords: PaperWidth enumeration member
keywords: Printer enumeration member
keywords: Quality enumeration member
keywords: ReportName enumeration member
keywords: Scale enumeration member
keywords: ShareOpenDataPath enumeration member
keywords: ToFile enumeration member
keywords: WaitRcd enumeration member

---

The **OverrideOptions** enumerated constant defines file override options within Monarch. Used by the [ CLProgram.OverrideFile](amfCLProgramClassOverrideFileMethods.html) and [ Job.OverrideFile](amfJobClassOverrideFileMethods.html) methods.

#### Syntax
<pre class="prettyprint"> **BegEnum OverrideOptions Access(*Public)** </pre>

#### Remarks
The **OverrideOptions** enumerated constants defines file override options within Monarch. For each option value within the description below, the value type (of the new option value) and the valid type of files are also noted.
<!--mine -->

#### Enumerators
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="15%" />
            <col width="80%" />
            <col width="5%" align="center" />
          </colgroup>
          <tr>
            <th>Member</th>
            <th>Description</th>
            <th>Value</th>
          </tr>
          <tr>
            <td>ToFile</td>
            <td>System.String. The new file
            object. In the case of WorkStnFile, this refers to the
            ASP.Net page path name. Applies to DBFile, WorkStnFile,
            and PrintFile.</td>
            <td>0</td>
          </tr>
          <tr>
            <td>Mbr</td>
            <td>System.String. The name of
            the physical file member within the 
 *fileName* . Applies to DBFile.</td>
            <td>1</td>
          </tr>
          <tr>
            <td>WaitRcd</td>
            <td>System.Int32. Time, in
            seconds, specifying the waiting period for a record.
            Applies to DBFile.</td>
            <td>2</td>
          </tr>
          <tr>
            <td>Collate</td>
            <td>Boolean. 
 **True/False** . Indicates the output
            produced by capable printers should be collated when
            this property is set to 
 **True** . Applicable only when printing
            multiple copies, or when the 
 **Copies**  is &gt;1. Applies to
            PrintFile.</td>
            <td>3</td>
          </tr>
          <tr>
            <td>Copies</td>
            <td>System.Int32. The number of
            copies to print. See also 
 **Collate** . Applies to PrintFile.</td>
            <td>4</td>
          </tr>
          <tr>
            <td>Duplex</td>
            <td>Enumerated constant
            defining values on duplex (double-sided) printing
            options. Applies to PrintFile.</td>
            <td>5</td>
          </tr>
          <tr>
            <td>FormName</td>
            <td>System.String. The name of
            the print format to use, such as "A4", "Letter",
            "Tabloid", etc. See 
 **PaperSize**  for available print form names. Applies
            to PrintFile.</td>
            <td>6</td>
          </tr>
          <tr>
            <td>Orientation</td>
            <td>Enumerated constant
            defining the landscape or portrait orientation of paper
            in the printer. Applies to PrintFile.</td>
            <td>7</td>
          </tr>
          <tr>
            <td>PaperLength</td>
            <td>System.Int32. The paper
            length based upon the 
 **Orientation**  of the paper in the
            printer. These values are in tenths of a millimeter.
            Applies to PrintFile.</td>
            <td>8</td>
          </tr>
          <tr>
            <td>PaperSize</td>
            <td>Enumerated constant
            defining the size of paper. Applies to PrintFile.</td>
            <td>9</td>
          </tr>
          <tr>
            <td>PaperSource</td>
            <td>Enumerated constant
            defining values on the printer tray that will be used.
            Applies to PrintFile.</td>
            <td>10</td>
          </tr>
          <tr>
            <td>PaperWidth</td>
            <td>System.Int32. The paper
            width based upon the 
 **Orientation**  of the paper in the
            printer. Values are in tenths of a millimeter. Applies
            to PrintFile.</td>
            <td>11</td>
          </tr>
          <tr>
            <td>Printer</td>
            <td>System.String. The complete
            path and name of the printer. For example, if the
            printer is on a network, you must specify the network,
            then the printer name. For example, "
 **\\Network\HP LaserJet 5M** ". Applies to
            PrintFile.</td>
            <td>12</td>
          </tr>
          <tr>
            <td>Quality</td>
            <td>Enumerated constant
            defining values for the quality rating for output
            produced by the printer. Applies to PrintFile.</td>
            <td>13</td>
          </tr>
          <tr>
            <td>ReportName</td>
            <td>System.String. The name of
            the report as seen on the printer spool. Applies to
            PrintFile.</td>
            <td>14</td>
          </tr>
          <tr>
            <td>Scale</td>
            <td>System.Int32. The
            percentage factor by which the printed output is to be
            scaled. The printer must support the output to be
            scaled or resized. Applies to PrintFile.</td>
            <td>15</td>
          </tr>
          <tr>
            <td>ShareOpenDataPath</td>
            <td>Boolean. 
 **True/False** . Indicator if the display
            file (active server page) used by this 
 **WorkStnFile**  allows any other to refer
            to the same display file. Applies to WorkStnFile.</td>
            <td>16</td>
          </tr>
</table>

<!-- -->

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
<dl><dd>
        [ASNA.Monarch
        Namespace](amfMonarchNamespace.html)</dd>
</dl>

