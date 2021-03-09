---
title: dgErrorNumber Enumeration

Id: dcsdgErrorNumberEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 12

keywords: dgErrorNumber enumeration
keywords: enumerations [DCS 16.0 dgErrorNumber
keywords: run-time errors, type of
keywords: type of run-time error

---

Specifies the type of DCS run-time error.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum dgErrorNumber;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Enum dgErrorNumber** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum dgErrorNumber Access(*Public)** 
      </pre>

Remarks

The <span>dgErrorNumber</span> enumeration is used as a parameter by the [ Error](dcsdgExceptionClassErrorField.html) field of the [dgException](dcsdgExceptionClass.html) class.
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="30%" style="FONT-WEIGHT: bold" />
            <col span="1" width="60%" />
            <col align="middles" span="1" width="10%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Member</th>
            <th colspan="1" rowspan="1">
							Description</th>
            <th colspan="1" rowspan="1">
							Value</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaBADACCESS 
</td>
            <td colspan="1" rowspan="1">

Bad Access. 
</td>
            <td colspan="1" rowspan="1">

110 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaBADFARM 
</td>
            <td colspan="1" rowspan="1">

Bad farm. 
</td>
            <td colspan="1" rowspan="1">

132 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaBADFD 
</td>
            <td colspan="1" rowspan="1">

Bad File Descriptor. 
</td>
            <td colspan="1" rowspan="1">

109 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaBADFRMT 
</td>
            <td colspan="1" rowspan="1">

Invalid Format. 
</td>
            <td colspan="1" rowspan="1">

125 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaBADGROVE 
</td>
            <td colspan="1" rowspan="1">

Bad Grove. 
</td>
            <td colspan="1" rowspan="1">

123 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaBADIDX 
</td>
            <td colspan="1" rowspan="1">

Bad Index. 
</td>
            <td colspan="1" rowspan="1">

131 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaBADREC 
</td>
            <td colspan="1" rowspan="1">

Bad Record. 
</td>
            <td colspan="1" rowspan="1">

105 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaBUSYFILE 
</td>
            <td colspan="1" rowspan="1">

File is Busy. 
</td>
            <td colspan="1" rowspan="1">

107 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaBUSYREC 
</td>
            <td colspan="1" rowspan="1">

Record is Busy. 
</td>
            <td colspan="1" rowspan="1">

108 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaCORRFARM 
</td>
            <td colspan="1" rowspan="1">

Corrupted Data File (File Length not multiple of Record Length). 
</td>
            <td colspan="1" rowspan="1">

138 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaCORRNODE 
</td>
            <td colspan="1" rowspan="1">

Corrupted node encountered. 
</td>
            <td colspan="1" rowspan="1">

135 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaDEADLOCK 
</td>
            <td colspan="1" rowspan="1">

Dead Lock. 
</td>
            <td colspan="1" rowspan="1">

114 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaDUPKEY 
</td>
            <td colspan="1" rowspan="1">

Duplicate Key. 
</td>
            <td colspan="1" rowspan="1">

101 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaEOF 
</td>
            <td colspan="1" rowspan="1">

End of File. 
</td>
            <td colspan="1" rowspan="1">

106 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaIDXFNOTFND 
</td>
            <td colspan="1" rowspan="1">

Index File Not Found. 
</td>
            <td colspan="1" rowspan="1">

134 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaIDXNOTFND 
</td>
            <td colspan="1" rowspan="1">

Index Not Found. 
</td>
            <td colspan="1" rowspan="1">

113 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaINTERRUPT 
</td>
            <td colspan="1" rowspan="1">

Interrupt Received. 
</td>
            <td colspan="1" rowspan="1">

120 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaINVARG 
</td>
            <td colspan="1" rowspan="1">

Invalid Access Argument. 
</td>
            <td colspan="1" rowspan="1">

111 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaINVBFOPEN 
</td>
            <td colspan="1" rowspan="1">

Blocking factor attribute not allowed with files opened for output. 
</td>
            <td colspan="1" rowspan="1">

133 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaINVDATETIMEDATA 
</td>
            <td colspan="1" rowspan="1">

Corrupted Data File (File Length not multiple of Record Length). 
</td>
            <td colspan="1" rowspan="1">

138 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaINVDMOP 
</td>
            <td colspan="1" rowspan="1">

Invalid operation on database. 
</td>
            <td colspan="1" rowspan="1">

136 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaINVFTOP 
</td>
            <td colspan="1" rowspan="1">

Invalid Operation for This Type. 
</td>
            <td colspan="1" rowspan="1">

130 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaINVINST 
</td>
            <td colspan="1" rowspan="1">

Invalid Instructions. 
</td>
            <td colspan="1" rowspan="1">

129 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaINVMODE 
</td>
            <td colspan="1" rowspan="1">

Invalid Mode. 
</td>
            <td colspan="1" rowspan="1">

122 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaINVNOLOCK 
</td>
            <td colspan="1" rowspan="1">

Invalid Lock. 
</td>
            <td colspan="1" rowspan="1">

141 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaINVNUMERICDATA 
</td>
            <td colspan="1" rowspan="1">

Corrupted Data File (File Length not multiple of Record Length). 
</td>
            <td colspan="1" rowspan="1">

138 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaINVTYPE 
</td>
            <td colspan="1" rowspan="1">

Invalid Type. 
</td>
            <td colspan="1" rowspan="1">

102 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaIOERROR 
</td>
            <td colspan="1" rowspan="1">

I/O Error. 
</td>
            <td colspan="1" rowspan="1">

117 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaKEYNOTFND 
</td>
            <td colspan="1" rowspan="1">

Key Not Found. 
</td>
            <td colspan="1" rowspan="1">

139 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaMAXFILES 
</td>
            <td colspan="1" rowspan="1">

Maximum Files Opened. 
</td>
            <td colspan="1" rowspan="1">

119 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaNEEDFRMT 
</td>
            <td colspan="1" rowspan="1">

Need Format for this Operation. 
</td>
            <td colspan="1" rowspan="1">

126 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaNOCURR 
</td>
            <td colspan="1" rowspan="1">

No Current Record. 
</td>
            <td colspan="1" rowspan="1">

116 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaNOFILE 
</td>
            <td colspan="1" rowspan="1">

File Not Found. 
</td>
            <td colspan="1" rowspan="1">

118 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaNOLOCK 
</td>
            <td colspan="1" rowspan="1">

Record Not Locked by Caller. 
</td>
            <td colspan="1" rowspan="1">

115 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaNOSPACE 
</td>
            <td colspan="1" rowspan="1">

No Space Available. 
</td>
            <td colspan="1" rowspan="1">

121 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaNOTFND 
</td>
            <td colspan="1" rowspan="1">

Not Found. 
</td>
            <td colspan="1" rowspan="1">

103 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaNOTINDEX 
</td>
            <td colspan="1" rowspan="1">

Not open for Index Access. 
</td>
            <td colspan="1" rowspan="1">

124 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaNOTINDEXED 
</td>
            <td colspan="1" rowspan="1">

The file is not indexed. 
</td>
            <td colspan="1" rowspan="1">

140 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaRECDEL 
</td>
            <td colspan="1" rowspan="1">

Record Deleted. 
</td>
            <td colspan="1" rowspan="1">

104 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaRECPREVLOCK 
</td>
            <td colspan="1" rowspan="1">

Record is already locked to this job. 
</td>
            <td colspan="1" rowspan="1">

137 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaSTKOVF 
</td>
            <td colspan="1" rowspan="1">

Stack Overflow. 
</td>
            <td colspan="1" rowspan="1">

127 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaSTKUNF 
</td>
            <td colspan="1" rowspan="1">

Stack Underflow. 
</td>
            <td colspan="1" rowspan="1">

128 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEACCESS 
</td>
            <td colspan="1" rowspan="1">

Access Errors. 
</td>
            <td colspan="1" rowspan="1">

100 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEAPPC 
</td>
            <td colspan="1" rowspan="1">

APPC Errors. 
</td>
            <td colspan="1" rowspan="1">

800 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcADDIX 
</td>
            <td colspan="1" rowspan="1">

Adding Index. 
</td>
            <td colspan="1" rowspan="1">

407 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcBADREFFILE 
</td>
            <td colspan="1" rowspan="1">

Field reference file must be a physical file. 
</td>
            <td colspan="1" rowspan="1">

430 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcBADSRC 
</td>
            <td colspan="1" rowspan="1">

Bad Source. 
</td>
            <td colspan="1" rowspan="1">

401 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEccIORECERR 
</td>
            <td colspan="1" rowspan="1">

Recoverable I/O error occurred in commit/rollback operation. 
</td>
            <td colspan="1" rowspan="1">

1401 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcCLONEDFORMAT 
</td>
            <td colspan="1" rowspan="1">

The format has a fixed set of fields, those of the base file. 
</td>
            <td colspan="1" rowspan="1">

428 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcVRTACF 
</td>
            <td colspan="1" rowspan="1">

Creating Access File. 
</td>
            <td colspan="1" rowspan="1">

406 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcCRTACP 
</td>
            <td colspan="1" rowspan="1">

Creating Access Program. 
</td>
            <td colspan="1" rowspan="1">

418 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcFLDEXISTS 
</td>
            <td colspan="1" rowspan="1">

Field already exists in Format. 
</td>
            <td colspan="1" rowspan="1">

419 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcFLDINVDEC 
</td>
            <td colspan="1" rowspan="1">

Invalid Field Decimal. 
</td>
            <td colspan="1" rowspan="1">

416 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcFLDINVFMT 
</td>
            <td colspan="1" rowspan="1">

Invalid Field format. 
</td>
            <td colspan="1" rowspan="1">

422 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcFLDINVINT 
</td>
            <td colspan="1" rowspan="1">

Invalid Field Integral. 
</td>
            <td colspan="1" rowspan="1">

417 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcFLDINVLEN 
</td>
            <td colspan="1" rowspan="1">

Invalid Filed Length. 
</td>
            <td colspan="1" rowspan="1">

415 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcFLDNOTFND 
</td>
            <td colspan="1" rowspan="1">

Field Not Found. 
</td>
            <td colspan="1" rowspan="1">

414 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcFLDTYPENONNULL 
</td>
            <td colspan="1" rowspan="1">

Field Type does not allow nulls. 
</td>
            <td colspan="1" rowspan="1">

433 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcFORMATEXISTS 
</td>
            <td colspan="1" rowspan="1">

Format already exists in file. 
</td>
            <td colspan="1" rowspan="1">

421 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcFORMATNOTFND 
</td>
            <td colspan="1" rowspan="1">

Format not found. 
</td>
            <td colspan="1" rowspan="1">

420 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcINVCONCAT 
</td>
            <td colspan="1" rowspan="1">

Invalid Concat. 
</td>
            <td colspan="1" rowspan="1">

440 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcINVCONST 
</td>
            <td colspan="1" rowspan="1">

Invalid Constant. 
</td>
            <td colspan="1" rowspan="1">

408 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcINVCONSTLEN 
</td>
            <td colspan="1" rowspan="1">

Invalid Constant Length. 
</td>
            <td colspan="1" rowspan="1">

409 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcINVDER 
</td>
            <td colspan="1" rowspan="1">

Invalid Derivation. 
</td>
            <td colspan="1" rowspan="1">

423 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcINVDERDBCS 
</td>
            <td colspan="1" rowspan="1">

Invalid Derivation, base field length invalid. 
</td>
            <td colspan="1" rowspan="1">

427 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcINVDERDEC 
</td>
            <td colspan="1" rowspan="1">

Invalid Derivation, Decimals not 0. 
</td>
            <td colspan="1" rowspan="1">

425 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcINVERDERSIZ 
</td>
            <td colspan="1" rowspan="1">

Invalid Derivation, Sizes don't match. 
</td>
            <td colspan="1" rowspan="1">

424 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcINVFILETYPE 
</td>
            <td colspan="1" rowspan="1">

Invalid File Type. 
</td>
            <td colspan="1" rowspan="1">

439 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcINVFLDREMAP 
</td>
            <td colspan="1" rowspan="1">

Invalid Field Remap. 
</td>
            <td colspan="1" rowspan="1">

441 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcINVINST 
</td>
            <td colspan="1" rowspan="1">

Invalid Instruction. 
</td>
            <td colspan="1" rowspan="1">

404 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcINVJOINLEN 
</td>
            <td colspan="1" rowspan="1">

Invalid length for join file. 
</td>
            <td colspan="1" rowspan="1">

435 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcINVKEYFORFILE 
</td>
            <td colspan="1" rowspan="1">

Invalid key for file. 
</td>
            <td colspan="1" rowspan="1">

432 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcINVKEYLEN 
</td>
            <td colspan="1" rowspan="1">

Invalid key length. 
</td>
            <td colspan="1" rowspan="1">

434 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcINVKEYREMAP 
</td>
            <td colspan="1" rowspan="1">

Invalid key Remap. 
</td>
            <td colspan="1" rowspan="1">

442 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcINVOPTYPE 
</td>
            <td colspan="1" rowspan="1">

Invalid operator type. 
</td>
            <td colspan="1" rowspan="1">

436 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcNEWVERSION 
</td>
            <td colspan="1" rowspan="1">

Need new version. 
</td>
            <td colspan="1" rowspan="1">

431 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcNONULLSUPPORT 
</td>
            <td colspan="1" rowspan="1">

No Null Support. 
</td>
            <td colspan="1" rowspan="1">

437 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcNOREFFILE 
</td>
            <td colspan="1" rowspan="1">

Filed reference file not found. 
</td>
            <td colspan="1" rowspan="1">

429 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcNOTALL 
</td>
            <td colspan="1" rowspan="1">

Not all objects are supported. 
</td>
            <td colspan="1" rowspan="1">

436 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcNOVARLENSUPPORT 
</td>
            <td colspan="1" rowspan="1">

No variable length support. 
</td>
            <td colspan="1" rowspan="1">

438 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcNUMEXP 
</td>
            <td colspan="1" rowspan="1">

Number Expected. 
</td>
            <td colspan="1" rowspan="1">

402 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcOPEREXP 
</td>
            <td colspan="1" rowspan="1">

Operand Expected. 
</td>
            <td colspan="1" rowspan="1">

411 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcOPNACF 
</td>
            <td colspan="1" rowspan="1">

Opening Access File. 
</td>
            <td colspan="1" rowspan="1">

405 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcOPNTYPE 
</td>
            <td colspan="1" rowspan="1">

Operand Type. 
</td>
            <td colspan="1" rowspan="1">

403 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcQUOTEXP 
</td>
            <td colspan="1" rowspan="1">

Quotation Expected. 
</td>
            <td colspan="1" rowspan="1">

412 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcRPAREXP 
</td>
            <td colspan="1" rowspan="1">

')' Expected. 
</td>
            <td colspan="1" rowspan="1">

410 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcSQL400FILE 
</td>
            <td colspan="1" rowspan="1">

File is SQL 400 file. 
</td>
            <td colspan="1" rowspan="1">

443 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEcVAREXP 
</td>
            <td colspan="1" rowspan="1">

Variable Expected. 
</td>
            <td colspan="1" rowspan="1">

413 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgECALLPARM 
</td>
            <td colspan="1" rowspan="1">

Call/Parm Errors. 
</td>
            <td colspan="1" rowspan="1">

700 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgECATALOG 
</td>
            <td colspan="1" rowspan="1">

Catalog Errors. 
</td>
            <td colspan="1" rowspan="1">

50 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgECHANBUSY 
</td>
            <td colspan="1" rowspan="1">

Channel busy. 
</td>
            <td colspan="1" rowspan="1">

10 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgECOMMAND 
</td>
            <td colspan="1" rowspan="1">

Command Errors. 
</td>
            <td colspan="1" rowspan="1">

1100 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgECOMMITCTL 
</td>
            <td colspan="1" rowspan="1">

Commitment Control Errors. 
</td>
            <td colspan="1" rowspan="1">

1400 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgECOMPILER 
</td>
            <td colspan="1" rowspan="1">

Compiler Errors. 
</td>
            <td colspan="1" rowspan="1">

400 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgBADLIBL 
</td>
            <td colspan="1" rowspan="1">

Bad Library. 
</td>
            <td colspan="1" rowspan="1">

1027 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgCONVUNAVAIL 
</td>
            <td colspan="1" rowspan="1">

CCSID conversion unavailable. 
</td>
            <td colspan="1" rowspan="1">

1012 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgDGMEMSRV 
</td>
            <td colspan="1" rowspan="1">

Can't create dgmemsrv process. 
</td>
            <td colspan="1" rowspan="1">

1004 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgDUPDB 
</td>
            <td colspan="1" rowspan="1">

Duplicate Database. 
</td>
            <td colspan="1" rowspan="1">

1013 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgDUPLIBLE 
</td>
            <td colspan="1" rowspan="1">

Duplicate library list entry. 
</td>
            <td colspan="1" rowspan="1">

1022 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgEXCLUSIVE 
</td>
            <td colspan="1" rowspan="1">

Database locked for exclusive use. 
</td>
            <td colspan="1" rowspan="1">

1020 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgLIMIT 
</td>
            <td colspan="1" rowspan="1">

Too many databases registered. 
</td>
            <td colspan="1" rowspan="1">

1003 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgMAPCREATE 
</td>
            <td colspan="1" rowspan="1">

Registry shared memory File create failed. 
</td>
            <td colspan="1" rowspan="1">

1007 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgMAPOPEN 
</td>
            <td colspan="1" rowspan="1">

Registry shared memory open failed. 
</td>
            <td colspan="1" rowspan="1">

1006 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgMAPVIEW 
</td>
            <td colspan="1" rowspan="1">

Registry shared memory view mapping failed. 
</td>
            <td colspan="1" rowspan="1">

1008 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgMAXLIBL 
</td>
            <td colspan="1" rowspan="1">

Library List reached max capacity. 
</td>
            <td colspan="1" rowspan="1">

1023 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgMUTEXNOTFOUND 
</td>
            <td colspan="1" rowspan="1">

System mutex object not found. 
</td>
            <td colspan="1" rowspan="1">

1001 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgMUTEXWAIT 
</td>
            <td colspan="1" rowspan="1">

Database startup procedure failed. (System mutex wait error). 
</td>
            <td colspan="1" rowspan="1">

1002 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNODBCSSUPP 
</td>
            <td colspan="1" rowspan="1">

DBCS unsupported in this version. 
</td>
            <td colspan="1" rowspan="1">

1011 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNODBNAME 
</td>
            <td colspan="1" rowspan="1">

Database Name not found. 
</td>
            <td colspan="1" rowspan="1">

1019 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOINITLIBL 
</td>
            <td colspan="1" rowspan="1">

Initial Library List not set. 
</td>
            <td colspan="1" rowspan="1">

1021 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOLABEL 
</td>
            <td colspan="1" rowspan="1">

The Requested Database Label doesn't exist. 
</td>
            <td colspan="1" rowspan="1">

1016 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOLIBL 
</td>
            <td colspan="1" rowspan="1">

The Requested Database Library doesn't exist. 
</td>
            <td colspan="1" rowspan="1">

1026 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOQCCSID 
</td>
            <td colspan="1" rowspan="1">

Count not retrieve QCCSID system value. 
</td>
            <td colspan="1" rowspan="1">

1010 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOREPAIR 
</td>
            <td colspan="1" rowspan="1">

dgFixDB wouldn't start. 
</td>
            <td colspan="1" rowspan="1">

1015 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOTALLLIBL 
</td>
            <td colspan="1" rowspan="1">

At least one library not set in Library List. 
</td>
            <td colspan="1" rowspan="1">

1025 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOTINLIBL 
</td>
            <td colspan="1" rowspan="1">

Library not in Library List. 
</td>
            <td colspan="1" rowspan="1">

1024 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgREGCREATE 
</td>
            <td colspan="1" rowspan="1">

System error creating Database label. 
</td>
            <td colspan="1" rowspan="1">

1014 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgREGDELETEDB 
</td>
            <td colspan="1" rowspan="1">

The operation did not complete; the registry entries could not be removed. 
</td>
            <td colspan="1" rowspan="1">

1017 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgREGDENIED 
</td>
            <td colspan="1" rowspan="1">

Insufficient access permission on the registry. 
</td>
            <td colspan="1" rowspan="1">

1018 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgREGFILEDIR 
</td>
            <td colspan="1" rowspan="1">

Registration File Library not found. 
</td>
            <td colspan="1" rowspan="1">

1005 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEdbSYNC 
</td>
            <td colspan="1" rowspan="1">

Unprotected registry access not allowed. 
</td>
            <td colspan="1" rowspan="1">

1009 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEDELERROR 
</td>
            <td colspan="1" rowspan="1">

Delete error. 
</td>
            <td colspan="1" rowspan="1">

3 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEEXCEPTION 
</td>
            <td colspan="1" rowspan="1">

Unexpected Exception. 
</td>
            <td colspan="1" rowspan="1">

9 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEEXPANDFS 
</td>
            <td colspan="1" rowspan="1">

Expand File System. 
</td>
            <td colspan="1" rowspan="1">

5 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEfirstError 
</td>
            <td colspan="1" rowspan="1">

Don't Remove. 
</td>
            <td colspan="1" rowspan="1">

0 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgBADAP 
</td>
            <td colspan="1" rowspan="1">

Bad Access Program Stream. 
</td>
            <td colspan="1" rowspan="1">

53 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgBADATTR 
</td>
            <td colspan="1" rowspan="1">

Bad Creation Attribute Stream. 
</td>
            <td colspan="1" rowspan="1">

59 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgBADAUTH 
</td>
            <td colspan="1" rowspan="1">

Bad Authorization record. 
</td>
            <td colspan="1" rowspan="1">

77 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgBADDEPEND 
</td>
            <td colspan="1" rowspan="1">

Bad Dependency Stream. 
</td>
            <td colspan="1" rowspan="1">

67 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgBADEXT 
</td>
            <td colspan="1" rowspan="1">

Bad Extension Stream. 
</td>
            <td colspan="1" rowspan="1">

69 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgBADFARM 
</td>
            <td colspan="1" rowspan="1">

Bad Farm Stream. 
</td>
            <td colspan="1" rowspan="1">

65 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgBADGROVE 
</td>
            <td colspan="1" rowspan="1">

Bad File Definition Stream. 
</td>
            <td colspan="1" rowspan="1">

55 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgBADMATTER 
</td>
            <td colspan="1" rowspan="1">

Bad Grove Stream. 
</td>
            <td colspan="1" rowspan="1">

63 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgBADPP 
</td>
            <td colspan="1" rowspan="1">

Bad Matter Stream. 
</td>
            <td colspan="1" rowspan="1">

61 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgBADREL 
</td>
            <td colspan="1" rowspan="1">

Bad Relations Stream. 
</td>
            <td colspan="1" rowspan="1">

51 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgBADTEXT 
</td>
            <td colspan="1" rowspan="1">

Bad Text Stream. 
</td>
            <td colspan="1" rowspan="1">

71 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgCANTAUTH 
</td>
            <td colspan="1" rowspan="1">

Could not add Security record. 
</td>
            <td colspan="1" rowspan="1">

76 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgCORRFDEFC 
</td>
            <td colspan="1" rowspan="1">

Corrupt file definition cache member. 
</td>
            <td colspan="1" rowspan="1">

84 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgINVVOLPATH 
</td>
            <td colspan="1" rowspan="1">

Invalid Volume Library Path. 
</td>
            <td colspan="1" rowspan="1">

81 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNEWDB 
</td>
            <td colspan="1" rowspan="1">

Database is newer than supported by this version. 
</td>
            <td colspan="1" rowspan="1">

74 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOAP 
</td>
            <td colspan="1" rowspan="1">

No Access Program Stream exists. 
</td>
            <td colspan="1" rowspan="1">

54 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOATTR 
</td>
            <td colspan="1" rowspan="1">

No Creation Attribute Stream exists. 
</td>
            <td colspan="1" rowspan="1">

60 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOAUTHLOCK 
</td>
            <td colspan="1" rowspan="1">

Could not lock the security record. 
</td>
            <td colspan="1" rowspan="1">

79 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOCATALOG 
</td>
            <td colspan="1" rowspan="1">

Could not open the database's Catalog. 
</td>
            <td colspan="1" rowspan="1">

75 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNODBAUTH 
</td>
            <td colspan="1" rowspan="1">

Not authorized to database. 
</td>
            <td colspan="1" rowspan="1">

80 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNODEPEND 
</td>
            <td colspan="1" rowspan="1">

No Dependency stream exists. 
</td>
            <td colspan="1" rowspan="1">

68 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOEXT 
</td>
            <td colspan="1" rowspan="1">

No Extension Stream exists. 
</td>
            <td colspan="1" rowspan="1">

70 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOFARM 
</td>
            <td colspan="1" rowspan="1">

No Farm Stream exists. 
</td>
            <td colspan="1" rowspan="1">

66 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOFDEF 
</td>
            <td colspan="1" rowspan="1">

No File Definition Stream exists. 
</td>
            <td colspan="1" rowspan="1">

56 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOGROVE 
</td>
            <td colspan="1" rowspan="1">

No Grove Stream exists. 
</td>
            <td colspan="1" rowspan="1">

64 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOMATTER 
</td>
            <td colspan="1" rowspan="1">

No Matter Stream exists. 
</td>
            <td colspan="1" rowspan="1">

62 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNONSECUREDB 
</td>
            <td colspan="1" rowspan="1">

Database is not secure. 
</td>
            <td colspan="1" rowspan="1">

78 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOPP 
</td>
            <td colspan="1" rowspan="1">

No Path Program Stream exists. 
</td>
            <td colspan="1" rowspan="1">

58 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOREL 
</td>
            <td colspan="1" rowspan="1">

No Relations exists. 
</td>
            <td colspan="1" rowspan="1">

52 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOTEXT 
</td>
            <td colspan="1" rowspan="1">

No Text Stream exists. 
</td>
            <td colspan="1" rowspan="1">

72 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgOLDDB 
</td>
            <td colspan="1" rowspan="1">

Database is older than supported y this version. 
</td>
            <td colspan="1" rowspan="1">

73 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgOSNOTSECURE 
</td>
            <td colspan="1" rowspan="1">

Tried to open secure Database from an insecure Operating System. 
</td>
            <td colspan="1" rowspan="1">

83 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgVOLNOTSECURE 
</td>
            <td colspan="1" rowspan="1">

Volume's File IBM is not secure capable. 
</td>
            <td colspan="1" rowspan="1">

82 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEiCONNLOST 
</td>
            <td colspan="1" rowspan="1">

The TCP/IP Connection was terminated unexpectedly. The Server was probably shut down. 
</td>
            <td colspan="1" rowspan="1">

913 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEiDG8START 
</td>
            <td colspan="1" rowspan="1">

Remote TCP/IP host not found. 
</td>
            <td colspan="1" rowspan="1">

914 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEiHOSTNOTFND 
</td>
            <td colspan="1" rowspan="1">

Remote TCP/IP host not found. 
</td>
            <td colspan="1" rowspan="1">

908 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEiNETDOWN 
</td>
            <td colspan="1" rowspan="1">

TCP/IP Network subsystem has failed. 
</td>
            <td colspan="1" rowspan="1">

910 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEiNETUNREACH 
</td>
            <td colspan="1" rowspan="1">

Could not reach the TCP/IP network from this machine. 
</td>
            <td colspan="1" rowspan="1">

911 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEiNOBIND 
</td>
            <td colspan="1" rowspan="1">

Cannot bind socket. 
</td>
            <td colspan="1" rowspan="1">

902 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEiNORESPONSE 
</td>
            <td colspan="1" rowspan="1">

The Server Machine or the DataGate/DG Service did not respond. 
</td>
            <td colspan="1" rowspan="1">

912 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEiNORNTTCPIPSUPPORT 
</td>
            <td colspan="1" rowspan="1">

Connecting to a remove database with TCP/IP is not supported on this platform. 
</td>
            <td colspan="1" rowspan="1">

906 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEiNOSERVER 
</td>
            <td colspan="1" rowspan="1">

Cannot connect to database server. 
</td>
            <td colspan="1" rowspan="1">

903 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEiNOSOCKET 
</td>
            <td colspan="1" rowspan="1">

Cannot get socket. 
</td>
            <td colspan="1" rowspan="1">

901 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEiRESOLVER 
</td>
            <td colspan="1" rowspan="1">

TCP/IP resolver error. 
</td>
            <td colspan="1" rowspan="1">

909 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEiSERVERSTART 
</td>
            <td colspan="1" rowspan="1">

Could not start database server process. 
</td>
            <td colspan="1" rowspan="1">

905 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEiSOCKETIO 
</td>
            <td colspan="1" rowspan="1">

Socket I/O error. 
</td>
            <td colspan="1" rowspan="1">

904 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEiCPDOWN 
</td>
            <td colspan="1" rowspan="1">

TCP/IP subsystem not currently available. 
</td>
            <td colspan="1" rowspan="1">

907 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINTERNAL 
</td>
            <td colspan="1" rowspan="1">

Internal error. 
</td>
            <td colspan="1" rowspan="1">

7 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVARG 
</td>
            <td colspan="1" rowspan="1">

Invalid argument. 
</td>
            <td colspan="1" rowspan="1">

8 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVHANDLE 
</td>
            <td colspan="1" rowspan="1">

Invalid Handle. 
</td>
            <td colspan="1" rowspan="1">

6 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVPLATFORM 
</td>
            <td colspan="1" rowspan="1">

Invalid operating system platform. 
</td>
            <td colspan="1" rowspan="1">

18 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgELastError 
</td>
            <td colspan="1" rowspan="1">

Last error. 
</td>
            <td colspan="1" rowspan="1">

1604 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgELICENSE 
</td>
            <td colspan="1" rowspan="1">

License Errors. 
</td>
            <td colspan="1" rowspan="1">

1200 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEm400OBJNAMELEN 
</td>
            <td colspan="1" rowspan="1">

The object length of the 400 is invalid. 
</td>
            <td colspan="1" rowspan="1">

672 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmANOTFND 
</td>
            <td colspan="1" rowspan="1">

Access Path Not Found. 
</td>
            <td colspan="1" rowspan="1">

605 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmARCCHKSUMWRONG 
</td>
            <td colspan="1" rowspan="1">

Archive checksum is wrong. Archive is corrupted. 
</td>
            <td colspan="1" rowspan="1">

651 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmARCFAILI 
</td>
            <td colspan="1" rowspan="1">

Could not restore data due to an input error. 
</td>
            <td colspan="1" rowspan="1">

649 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmBADARCHTYPE 
</td>
            <td colspan="1" rowspan="1">

Archive type not supported. 
</td>
            <td colspan="1" rowspan="1">

674 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmBADCAT 
</td>
            <td colspan="1" rowspan="1">

Catalog is broken. 
</td>
            <td colspan="1" rowspan="1">

634 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmBADFRMTID 
</td>
            <td colspan="1" rowspan="1">

Base File has invalid Format ID. 
</td>
            <td colspan="1" rowspan="1">

637 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmBASENOTPH 
</td>
            <td colspan="1" rowspan="1">

Base File is not Physical. 
</td>
            <td colspan="1" rowspan="1">

638 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmBUSYOBJ 
</td>
            <td colspan="1" rowspan="1">

Object is Busy. 
</td>
            <td colspan="1" rowspan="1">

681 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmCANCEL 
</td>
            <td colspan="1" rowspan="1">

Operation canceled by user. 
</td>
            <td colspan="1" rowspan="1">

673 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmCLIENTNOTFND 
</td>
            <td colspan="1" rowspan="1">

Client not found. 
</td>
            <td colspan="1" rowspan="1">

679 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmCORRDATFIL 
</td>
            <td colspan="1" rowspan="1">

Corrupted system data file encountered in member; retry after using DataGate Database Manager's Fix Index Tool. 
</td>
            <td colspan="1" rowspan="1">

648 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmCORRENV 
</td>
            <td colspan="1" rowspan="1">

Environment is corrupted. 
</td>
            <td colspan="1" rowspan="1">

612 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmCRTSHM 
</td>
            <td colspan="1" rowspan="1">

Error creating Shared Memory File. 
</td>
            <td colspan="1" rowspan="1">

668 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmCRTSHMLOCK 
</td>
            <td colspan="1" rowspan="1">

Cannot create Shared Memory File because it is locked by another program. 
</td>
            <td colspan="1" rowspan="1">

666 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmCRTSHMMAP 
</td>
            <td colspan="1" rowspan="1">

Error creating Shared Memory File Mapping. 
</td>
            <td colspan="1" rowspan="1">

669 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmCRTSHMPATH 
</td>
            <td colspan="1" rowspan="1">

Cannot create Shared Memory File because path to database doesn't exist. 
</td>
            <td colspan="1" rowspan="1">

667 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmDIRNOTEMPTY 
</td>
            <td colspan="1" rowspan="1">

Library is not empty. 
</td>
            <td colspan="1" rowspan="1">

644 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmDIRTYENV 
</td>
            <td colspan="1" rowspan="1">

Environment is dirty. 
</td>
            <td colspan="1" rowspan="1">

611 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmDNOTFND 
</td>
            <td colspan="1" rowspan="1">

Library Not Found. 
</td>
            <td colspan="1" rowspan="1">

602 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmDUPINDEX 
</td>
            <td colspan="1" rowspan="1">

Index is a duplicate. 
</td>
            <td colspan="1" rowspan="1">

623 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmDUPNOTFND 
</td>
            <td colspan="1" rowspan="1">

Duplicate base not found. 
</td>
            <td colspan="1" rowspan="1">

636 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmDUPOBJ 
</td>
            <td colspan="1" rowspan="1">

Duplicate object. 
</td>
            <td colspan="1" rowspan="1">

606 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmENVEXISTS 
</td>
            <td colspan="1" rowspan="1">

Environment already exists. 
</td>
            <td colspan="1" rowspan="1">

609 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmEOFSAVEREST 
</td>
            <td colspan="1" rowspan="1">

End of Save/Restore File. 
</td>
            <td colspan="1" rowspan="1">

615 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmERRAUTH 
</td>
            <td colspan="1" rowspan="1">

Error found when dealing with authority. 
</td>
            <td colspan="1" rowspan="1">

662 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmFILENOTOPEN 
</td>
            <td colspan="1" rowspan="1">

File is not open. 
</td>
            <td colspan="1" rowspan="1">

680 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmFNOTFND 
</td>
            <td colspan="1" rowspan="1">

File Not Found. 
</td>
            <td colspan="1" rowspan="1">

603 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmHASDEPEND 
</td>
            <td colspan="1" rowspan="1">

Object has dependents. 
</td>
            <td colspan="1" rowspan="1">

614 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINCOMPLETE 
</td>
            <td colspan="1" rowspan="1">

Operation did not complete. 
</td>
            <td colspan="1" rowspan="1">

622 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINUSEBYYOU 
</td>
            <td colspan="1" rowspan="1">

Object is in use by yourself. 
</td>
            <td colspan="1" rowspan="1">

675 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINV400OP 
</td>
            <td colspan="1" rowspan="1">

Invalid operation against IBM i server. 
</td>
            <td colspan="1" rowspan="1">

645 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVDIRNAME 
</td>
            <td colspan="1" rowspan="1">

Invalid Library Name. 
</td>
            <td colspan="1" rowspan="1">

641 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVFILENAME 
</td>
            <td colspan="1" rowspan="1">

Invalid File Name. 
</td>
            <td colspan="1" rowspan="1">

642 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVFOP 
</td>
            <td colspan="1" rowspan="1">

Invalid File Operation. 
</td>
            <td colspan="1" rowspan="1">

639 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVMEMBNAME 
</td>
            <td colspan="1" rowspan="1">

Invalid Member Name. 
</td>
            <td colspan="1" rowspan="1">

640 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVOBJ 
</td>
            <td colspan="1" rowspan="1">

Invalid Object. 
</td>
            <td colspan="1" rowspan="1">

607 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVOBJNAME 
</td>
            <td colspan="1" rowspan="1">

Invalid Object Name 
</td>
            <td colspan="1" rowspan="1">

643 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVOTYPE 
</td>
            <td colspan="1" rowspan="1">

Invalid Object. 
</td>
            <td colspan="1" rowspan="1">

608 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVOWNER 
</td>
            <td colspan="1" rowspan="1">

Invalid Owner. This account may not be assigned as the owner of this object. 
</td>
            <td colspan="1" rowspan="1">

661 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVPRTFILE 
</td>
            <td colspan="1" rowspan="1">

Not a valid DataGate Database print file. 
</td>
            <td colspan="1" rowspan="1">

652 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVSQLOP 
</td>
            <td colspan="1" rowspan="1">

Not a valid SQL server operation. 
</td>
            <td colspan="1" rowspan="1">

646 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVTAROBJNAME 
</td>
            <td colspan="1" rowspan="1">

Invalid object name. 
</td>
            <td colspan="1" rowspan="1">

626 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVUSER 
</td>
            <td colspan="1" rowspan="1">

Invalid user account. 
</td>
            <td colspan="1" rowspan="1">

660 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmCKNOTFND 
</td>
            <td colspan="1" rowspan="1">

Object Lock not found. 
</td>
            <td colspan="1" rowspan="1">

678 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmLIBLTARGET 
</td>
            <td colspan="1" rowspan="1">

Error connecting to the Target library. 
</td>
            <td colspan="1" rowspan="1">

686 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmMAPSHM 
</td>
            <td colspan="1" rowspan="1">

Error Mapping view of Shared Memory File. 
</td>
            <td colspan="1" rowspan="1">

670 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmMAXMERGE 
</td>
            <td colspan="1" rowspan="1">

Maximum number of merged members over a physical. 
</td>
            <td colspan="1" rowspan="1">

632 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmMNOTFND 
</td>
            <td colspan="1" rowspan="1">

Member Not Found. 
</td>
            <td colspan="1" rowspan="1">

604 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOBASEAUTH 
</td>
            <td colspan="1" rowspan="1">

Not authorized to base object for this operation. 
</td>
            <td colspan="1" rowspan="1">

663 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNODIRADD 
</td>
            <td colspan="1" rowspan="1">

Not authorized to add objects to Library. 
</td>
            <td colspan="1" rowspan="1">

656 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNODIRDEL 
</td>
            <td colspan="1" rowspan="1">

Not authorized to delete object from Library. 
</td>
            <td colspan="1" rowspan="1">

657 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNODIRREAD 
</td>
            <td colspan="1" rowspan="1">

Not authorized to read object in Library. 
</td>
            <td colspan="1" rowspan="1">

655 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOENV 
</td>
            <td colspan="1" rowspan="1">

Database not available or does not exist. Also means Database Name not found. 
</td>
            <td colspan="1" rowspan="1">

610 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOLOCK 
</td>
            <td colspan="1" rowspan="1">

Object is not locked by caller. 
</td>
            <td colspan="1" rowspan="1">

682 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOMEMADD 
</td>
            <td colspan="1" rowspan="1">

Not authorized to add members to file. 
</td>
            <td colspan="1" rowspan="1">

664 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOMEMDEL 
</td>
            <td colspan="1" rowspan="1">

Not authorized to delete members from file. 
</td>
            <td colspan="1" rowspan="1">

665 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNONEXISTAUTH 
</td>
            <td colspan="1" rowspan="1">

Cannot revoke non-existing authorities. 
</td>
            <td colspan="1" rowspan="1">

659 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOOBJAUTH 
</td>
            <td colspan="1" rowspan="1">

Not authorized to object for this operation. 
</td>
            <td colspan="1" rowspan="1">

654 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOPARENTUPD 
</td>
            <td colspan="1" rowspan="1">

Not authorized to update objects in Parent. 
</td>
            <td colspan="1" rowspan="1">

658 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOPATHAUTH 
</td>
            <td colspan="1" rowspan="1">

Not authorized to path. 
</td>
            <td colspan="1" rowspan="1">

653 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOPERMINTEMP 
</td>
            <td colspan="1" rowspan="1">

Permanent object can't reside in a temporary library. 
</td>
            <td colspan="1" rowspan="1">

677 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOSEMS 
</td>
            <td colspan="1" rowspan="1">

Cannot get requested number of semaphores. 
</td>
            <td colspan="1" rowspan="1">

627 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOTEMPTY 
</td>
            <td colspan="1" rowspan="1">

Library is not empty. 
</td>
            <td colspan="1" rowspan="1">

613 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOTFND 
</td>
            <td colspan="1" rowspan="1">

Object Not Found. 
</td>
            <td colspan="1" rowspan="1">

601 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOTONQTEMP 
</td>
            <td colspan="1" rowspan="1">

Operation is not valid on QTemp. 
</td>
            <td colspan="1" rowspan="1">

676 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOTSAME 
</td>
            <td colspan="1" rowspan="1">

Not the same device or File system. 
</td>
            <td colspan="1" rowspan="1">

633 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmOPENSHM 
</td>
            <td colspan="1" rowspan="1">

Error opening Shared Memory File. 
</td>
            <td colspan="1" rowspan="1">

671 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmPROCACTIVE 
</td>
            <td colspan="1" rowspan="1">

Process is active. 
</td>
            <td colspan="1" rowspan="1">

631 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmPROCNOTFND 
</td>
            <td colspan="1" rowspan="1">

Process not found. 
</td>
            <td colspan="1" rowspan="1">

630 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmQUSCRTUQ 
</td>
            <td colspan="1" rowspan="1">

QUSCRTUQ create user queue OS/400 api failure. 
</td>
            <td colspan="1" rowspan="1">

683 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmRMGSHM 
</td>
            <td colspan="1" rowspan="1">

Cannot remove global shared memory. 
</td>
            <td colspan="1" rowspan="1">

629 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmRMSEM 
</td>
            <td colspan="1" rowspan="1">

Cannot remove semaphore ID. 
</td>
            <td colspan="1" rowspan="1">

628 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmRNOBJUSRQ 
</td>
            <td colspan="1" rowspan="1">

RNMOBJ OBJTYPE (*USRQ) failed to rename user queue. 
</td>
            <td colspan="1" rowspan="1">

684 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmROOTDIR 
</td>
            <td colspan="1" rowspan="1">

Invalid operation on Root Library. 
</td>
            <td colspan="1" rowspan="1">

635 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmRSLVSPUSRQ 
</td>
            <td colspan="1" rowspan="1">

RSLVSP(_Usrq) failed to get user queue pointer. 
</td>
            <td colspan="1" rowspan="1">

685 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmSRCORRDATA 
</td>
            <td colspan="1" rowspan="1">

Corrupted Save/Restore data. 
</td>
            <td colspan="1" rowspan="1">

618 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmSRINVMODE 
</td>
            <td colspan="1" rowspan="1">

Invalid Save/Restore mode. 
</td>
            <td colspan="1" rowspan="1">

617 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmSRINVORD 
</td>
            <td colspan="1" rowspan="1">

Invalid Block order. 
</td>
            <td colspan="1" rowspan="1">

620 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmSRINVSYS 
</td>
            <td colspan="1" rowspan="1">

Incompatible Source or target machine. 
</td>
            <td colspan="1" rowspan="1">

621 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmSRINVVER 
</td>
            <td colspan="1" rowspan="1">

Invalid Save/Restore version. 
</td>
            <td colspan="1" rowspan="1">

619 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmSRNOTCOMP 
</td>
            <td colspan="1" rowspan="1">

Save/Restore not complete. 
</td>
            <td colspan="1" rowspan="1">

616 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEMGTOBJ 
</td>
            <td colspan="1" rowspan="1">

Object Management Errors. 
</td>
            <td colspan="1" rowspan="1">

600 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnAddingMember 
</td>
            <td colspan="1" rowspan="1">

A member could not be added. 
</td>
            <td colspan="1" rowspan="1">

1109 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnAddingRecord 
</td>
            <td colspan="1" rowspan="1">

A record could not be added. 
</td>
            <td colspan="1" rowspan="1">

1116 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnCantCreateLf 
</td>
            <td colspan="1" rowspan="1">

Can't create logical files using CopyData; Use Copy Logical File instead. 
</td>
            <td colspan="1" rowspan="1">

1131 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnCDNOCOMMONFLDS 
</td>
            <td colspan="1" rowspan="1">

Source and destination files must have at least one common field name. 
</td>
            <td colspan="1" rowspan="1">

1127 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnCDNODROPFLDS 
</td>
            <td colspan="1" rowspan="1">

Source and destination files have different field names and the 'Drop Fields' options was not set. 
</td>
            <td colspan="1" rowspan="1">

1128 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnCDSRCNOTPHY 
</td>
            <td colspan="1" rowspan="1">

Source file must be physical when mapping fields. 
</td>
            <td colspan="1" rowspan="1">

1126 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnCharExpected 
</td>
            <td colspan="1" rowspan="1">

Character expected for character field. 
</td>
            <td colspan="1" rowspan="1">

1114 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnCopyToSelf 
</td>
            <td colspan="1" rowspan="1">

Cannot copy a file onto itself. 
</td>
            <td colspan="1" rowspan="1">

1121 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnDateExpected 
</td>
            <td colspan="1" rowspan="1">

Date expected for date field. 
</td>
            <td colspan="1" rowspan="1">

1123 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnDelimeterExpected 
</td>
            <td colspan="1" rowspan="1">

Delimiter expected. 
</td>
            <td colspan="1" rowspan="1">

1112 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnEndOfArchiveUnit 
</td>
            <td colspan="1" rowspan="1">

Source and destination files have different format Ids. 
</td>
            <td colspan="1" rowspan="1">

1132 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnFromFileNotFnd 
</td>
            <td colspan="1" rowspan="1">

The 'From' file could not be opened. 
</td>
            <td colspan="1" rowspan="1">

1117 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnHexExpected 
</td>
            <td colspan="1" rowspan="1">

Hex value expected for date field. 
</td>
            <td colspan="1" rowspan="1">

1122 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnInDefinition 
</td>
            <td colspan="1" rowspan="1">

Inconsistency found in file definition. 
</td>
            <td colspan="1" rowspan="1">

1104 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnInvalidFieldTpe 
</td>
            <td colspan="1" rowspan="1">

Invalid field type. 
</td>
            <td colspan="1" rowspan="1">

1106 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnInvalidFromFileType 
</td>
            <td colspan="1" rowspan="1">

Invalid from-file type. 
</td>
            <td colspan="1" rowspan="1">

1133 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnInvalidToFileType 
</td>
            <td colspan="1" rowspan="1">

Invalid to-file type. 
</td>
            <td colspan="1" rowspan="1">

1134 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnMultiFormat 
</td>
            <td colspan="1" rowspan="1">

Multiformat file type expected. 
</td>
            <td colspan="1" rowspan="1">

1103 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnNoMemory 
</td>
            <td colspan="1" rowspan="1">

Out of memory. 
</td>
            <td colspan="1" rowspan="1">

1105 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnNumberExpected 
</td>
            <td colspan="1" rowspan="1">

Number expected for numeric field. 
</td>
            <td colspan="1" rowspan="1">

1113 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnOpenFileDef 
</td>
            <td colspan="1" rowspan="1">

Error opening file definition. 
</td>
            <td colspan="1" rowspan="1">

1102 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnOpeningFile 
</td>
            <td colspan="1" rowspan="1">

A file could not be opened. 
</td>
            <td colspan="1" rowspan="1">

1108 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnOpeningFromFile 
</td>
            <td colspan="1" rowspan="1">

The from-file could not be opened. 
</td>
            <td colspan="1" rowspan="1">

1135 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnOpeningToFile 
</td>
            <td colspan="1" rowspan="1">

The to-file could not be opened. 
</td>
            <td colspan="1" rowspan="1">

1136 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnReadingNext 
</td>
            <td colspan="1" rowspan="1">

Sequential read of database file failed. 
</td>
            <td colspan="1" rowspan="1">

1110 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnReadingRecord 
</td>
            <td colspan="1" rowspan="1">

A record could not be read. 
</td>
            <td colspan="1" rowspan="1">

1115 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnRemoveBaseFile 
</td>
            <td colspan="1" rowspan="1">

Base file cannot be replaced. 
</td>
            <td colspan="1" rowspan="1">

1129 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnRemoveLogicalFile 
</td>
            <td colspan="1" rowspan="1">

Logical file cannot be replaced. 
</td>
            <td colspan="1" rowspan="1">

1130 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnSeparatorExpected 
</td>
            <td colspan="1" rowspan="1">

Separator expected. 
</td>
            <td colspan="1" rowspan="1">

1111 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnTextFile 
</td>
            <td colspan="1" rowspan="1">

Failed to open specified text file. 
</td>
            <td colspan="1" rowspan="1">

1107 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnTimeExpected 
</td>
            <td colspan="1" rowspan="1">

Time expected for time field. 
</td>
            <td colspan="1" rowspan="1">

1124 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnTimestampExpected 
</td>
            <td colspan="1" rowspan="1">

Timestamp expected for timestamp field. 
</td>
            <td colspan="1" rowspan="1">

1125 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnToFileNotCrt 
</td>
            <td colspan="1" rowspan="1">

The 'To file could not be created. 
</td>
            <td colspan="1" rowspan="1">

1119 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnToFileNotFnd 
</td>
            <td colspan="1" rowspan="1">

The 'From' file was not found. 
</td>
            <td colspan="1" rowspan="1">

1118 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEnUnknown 
</td>
            <td colspan="1" rowspan="1">

Unknown dgECOMMAND error. 
</td>
            <td colspan="1" rowspan="1">

1101 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgENOATLASCTX 
</td>
            <td colspan="1" rowspan="1">

Internal error: No atlas context. 
</td>
            <td colspan="1" rowspan="1">

15 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgENOMEM 
</td>
            <td colspan="1" rowspan="1">

No Memory Available or database memory exhausted. Try increasing the memory size in the "Work with Databases" dialog in Database Manager. 
</td>
            <td colspan="1" rowspan="1">

4 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgENONPRVSERVER 
</td>
            <td colspan="1" rowspan="1">

Server Account not privileged; Security context not established. 
</td>
            <td colspan="1" rowspan="1">

12 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgENOTEMPFILE 
</td>
            <td colspan="1" rowspan="1">

There is no temp file. 
</td>
            <td colspan="1" rowspan="1">

16 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgENOTIMPL 
</td>
            <td colspan="1" rowspan="1">

Not implemented. 
</td>
            <td colspan="1" rowspan="1">

2 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgENOTSECURE 
</td>
            <td colspan="1" rowspan="1">

Invalid User/Password: Security context not established. 
</td>
            <td colspan="1" rowspan="1">

11 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEOBSOLETE 
</td>
            <td colspan="1" rowspan="1">

This command is now obsolete. 
</td>
            <td colspan="1" rowspan="1">

17 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEOK 
</td>
            <td colspan="1" rowspan="1">

Operation went OK. 
</td>
            <td colspan="1" rowspan="1">

-1 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEOLDSERVER 
</td>
            <td colspan="1" rowspan="1">

This operation is not supported on an old server. 
</td>
            <td colspan="1" rowspan="1">

14 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpAPXEXTERN 
</td>
            <td colspan="1" rowspan="1">

Apx Externalize method failed. 
</td>
            <td colspan="1" rowspan="1">

759 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpAPXGETPROP 
</td>
            <td colspan="1" rowspan="1">

Apx GetProp method Failed. 
</td>
            <td colspan="1" rowspan="1">

761 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpAPXMATER 
</td>
            <td colspan="1" rowspan="1">

Apx Materialize method Failed. 
</td>
            <td colspan="1" rowspan="1">

758 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpAPXMETHOD 
</td>
            <td colspan="1" rowspan="1">

Apx Method Failed. 
</td>
            <td colspan="1" rowspan="1">

757 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpAPXPRINT 
</td>
            <td colspan="1" rowspan="1">

Apxz Print method Failed. 
</td>
            <td colspan="1" rowspan="1">

762 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpASXSETPROP 
</td>
            <td colspan="1" rowspan="1">

Apx SetProp method Failed. 
</td>
            <td colspan="1" rowspan="1">

760 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpCRTDC 
</td>
            <td colspan="1" rowspan="1">

Print DC creation Failed. 
</td>
            <td colspan="1" rowspan="1">

753 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpINITAPXFAILED 
</td>
            <td colspan="1" rowspan="1">

InitApx Failed. 
</td>
            <td colspan="1" rowspan="1">

756 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpINITAPXNOTFND 
</td>
            <td colspan="1" rowspan="1">

InitApx not found. 
</td>
            <td colspan="1" rowspan="1">

755 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpINVPARMCOUNT 
</td>
            <td colspan="1" rowspan="1">

Invalid Parameter Count. 
</td>
            <td colspan="1" rowspan="1">

705 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpINVPARMTYPE 
</td>
            <td colspan="1" rowspan="1">

Invalid Parameter Type. 
</td>
            <td colspan="1" rowspan="1">

703 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpLIBNOTFND 
</td>
            <td colspan="1" rowspan="1">

Apx Library not found. 
</td>
            <td colspan="1" rowspan="1">

754 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpMEMEXCEPTION 
</td>
            <td colspan="1" rowspan="1">

Memory Exception. 
</td>
            <td colspan="1" rowspan="1">

708 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

OPENPRINT 
</td>
            <td colspan="1" rowspan="1">

Open printer failed. 
</td>
            <td colspan="1" rowspan="1">

774 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpOPENSPLVIEWER 
</td>
            <td colspan="1" rowspan="1">

Open print previewer failed. 
</td>
            <td colspan="1" rowspan="1">

775 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpPARMTYPENOTSUP 
</td>
            <td colspan="1" rowspan="1">

Parm type not supported. 
</td>
            <td colspan="1" rowspan="1">

704 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpPGNERR 
</td>
            <td colspan="1" rowspan="1">

Program errored. 
</td>
            <td colspan="1" rowspan="1">

702 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpPGMNOTFND 
</td>
            <td colspan="1" rowspan="1">

Program not found. 
</td>
            <td colspan="1" rowspan="1">

701 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpPRINTNOTFND 
</td>
            <td colspan="1" rowspan="1">

Printer Not Found. 
</td>
            <td colspan="1" rowspan="1">

751 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpPROMPTCANCEL 
</td>
            <td colspan="1" rowspan="1">

Print Prompter Canceled. 
</td>
            <td colspan="1" rowspan="1">

763 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpPROMPTFAILED 
</td>
            <td colspan="1" rowspan="1">

Print Prompter Failed. 
</td>
            <td colspan="1" rowspan="1">

752 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpSERVERTOOOLD 
</td>
            <td colspan="1" rowspan="1">

The print file's version is newer than the server; an updated server is required for access. 
</td>
            <td colspan="1" rowspan="1">

764 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpSPOOLBADPAGE 
</td>
            <td colspan="1" rowspan="1">

Corrupted Spool File: Invalid spool page format. 
</td>
            <td colspan="1" rowspan="1">

773 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpSPOOLCREATE 
</td>
            <td colspan="1" rowspan="1">

Could Not create spool file. 
</td>
            <td colspan="1" rowspan="1">

765 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpSPOOLNODM 
</td>
            <td colspan="1" rowspan="1">

Corrupted Spool File: No Device Mode. 
</td>
            <td colspan="1" rowspan="1">

769 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpSPOOLNOHEAD 
</td>
            <td colspan="1" rowspan="1">

Corrupted Spool File: No Header. 
</td>
            <td colspan="1" rowspan="1">

768 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpSPOOLNOPAGE 
</td>
            <td colspan="1" rowspan="1">

Corrupted Spool File: No Full Page. 
</td>
            <td colspan="1" rowspan="1">

772 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpSPOOLNOSD 
</td>
            <td colspan="1" rowspan="1">

Corrupted Spool File: No Start of Document. 
</td>
            <td colspan="1" rowspan="1">

770 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpSPOOLNOSP 
</td>
            <td colspan="1" rowspan="1">

Corrupted Spool File: No Start of Page. 
</td>
            <td colspan="1" rowspan="1">

771 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpSPOOLREOPEN 
</td>
            <td colspan="1" rowspan="1">

Could not reopen the spool file. 
</td>
            <td colspan="1" rowspan="1">

767 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpSPOOLWRITE 
</td>
            <td colspan="1" rowspan="1">

Could not write to the spool file. 
</td>
            <td colspan="1" rowspan="1">

766 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpTOOFEWPARMS 
</td>
            <td colspan="1" rowspan="1">

There are too few parms for this parameter. 
</td>
            <td colspan="1" rowspan="1">

706 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpTOOMANYPARMS 
</td>
            <td colspan="1" rowspan="1">

There are too many parms for this parameter. 
</td>
            <td colspan="1" rowspan="1">

707 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEPRINT 
</td>
            <td colspan="1" rowspan="1">

Print Errors. 
</td>
            <td colspan="1" rowspan="1">

750 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqCONNECTION 
</td>
            <td colspan="1" rowspan="1">

Error connecting to the Sql Server. 
</td>
            <td colspan="1" rowspan="1">

1509 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqDUPOWNOBJ 
</td>
            <td colspan="1" rowspan="1">

The owner's object is a duplicate. 
</td>
            <td colspan="1" rowspan="1">

1511 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqEXECUTION 
</td>
            <td colspan="1" rowspan="1">

Execution error. 
</td>
            <td colspan="1" rowspan="1">

1508 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqINVALIDOBJECT 
</td>
            <td colspan="1" rowspan="1">

The object is invalid. 
</td>
            <td colspan="1" rowspan="1">

1502 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqINVALIDOBJECTDEFINITION 
</td>
            <td colspan="1" rowspan="1">

The object definition is invalid. 
</td>
            <td colspan="1" rowspan="1">

1503 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqINVALIDPARAMETER 
</td>
            <td colspan="1" rowspan="1">

The parameter is invalid. 
</td>
            <td colspan="1" rowspan="1">

1504 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqINVALIDPLATFORM 
</td>
            <td colspan="1" rowspan="1">

The operating system platform is invalid for this version. 
</td>
            <td colspan="1" rowspan="1">

1505 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqINVOPFIELDREF 
</td>
            <td colspan="1" rowspan="1">

The field reference file is invalid. 
</td>
            <td colspan="1" rowspan="1">

1513 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqINVSQLSYN 
</td>
            <td colspan="1" rowspan="1">

The SQL synonym was invalid. 
</td>
            <td colspan="1" rowspan="1">

1514 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqINVUSRSQLSYN 
</td>
            <td colspan="1" rowspan="1">

The SQL synonym for the user was invalid. 
</td>
            <td colspan="1" rowspan="1">

1515 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqITEMNOTFOUND 
</td>
            <td colspan="1" rowspan="1">

The item was not found in the database file. 
</td>
            <td colspan="1" rowspan="1">

1506 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqKEYNAMENOTINBASE 
</td>
            <td colspan="1" rowspan="1">

The key name was not found in the base file. 
</td>
            <td colspan="1" rowspan="1">

1516 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqNOSQLSERVER 
</td>
            <td colspan="1" rowspan="1">

The Sql Server was not found. 
</td>
            <td colspan="1" rowspan="1">

1501 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqRESOURCE 
</td>
            <td colspan="1" rowspan="1">

The resource was not found. 
</td>
            <td colspan="1" rowspan="1">

1510 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqSQLUNKNOWN 
</td>
            <td colspan="1" rowspan="1">

Sql Server Unknown. 
</td>
            <td colspan="1" rowspan="1">

1507 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEqUNPRIVILEGEDLOGIN 
</td>
            <td colspan="1" rowspan="1">

The user does not have login privileges. 
</td>
            <td colspan="1" rowspan="1">

1512 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEr2FEWJOINS 
</td>
            <td colspan="1" rowspan="1">

Too few JoinDefs. 
</td>
            <td colspan="1" rowspan="1">

516 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEr2MANYFLDS 
</td>
            <td colspan="1" rowspan="1">

Too many Fields in JoinDef. 
</td>
            <td colspan="1" rowspan="1">

506 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErADENOTFND 
</td>
            <td colspan="1" rowspan="1">

Active Dictionary Entry Not Found. 
</td>
            <td colspan="1" rowspan="1">

519 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErBADSRC 
</td>
            <td colspan="1" rowspan="1">

Bad base filed; format or file. 
</td>
            <td colspan="1" rowspan="1">

501 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErBASEMBRNOTFND 
</td>
            <td colspan="1" rowspan="1">

Base source member not found. 
</td>
            <td colspan="1" rowspan="1">

522 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErCRTADE 
</td>
            <td colspan="1" rowspan="1">

Creating Active Dictionary Entry. 
</td>
            <td colspan="1" rowspan="1">

518 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErFDNOCHG 
</td>
            <td colspan="1" rowspan="1">

FileDef cannot be changed. 
</td>
            <td colspan="1" rowspan="1">

517 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErINVDUPFLD 
</td>
            <td colspan="1" rowspan="1">

Duplicate Field not found in Format. 
</td>
            <td colspan="1" rowspan="1">

512 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErINVSECFLD 
</td>
            <td colspan="1" rowspan="1">

Secondary Field not found in Format. 
</td>
            <td colspan="1" rowspan="1">

511 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErINVSELFLD 
</td>
            <td colspan="1" rowspan="1">

Selected Field not found in Format. 
</td>
            <td colspan="1" rowspan="1">

510 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErINVTYPE 
</td>
            <td colspan="1" rowspan="1">

Invalid type. 
</td>
            <td colspan="1" rowspan="1">

502 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErJFLDCONFL 
</td>
            <td colspan="1" rowspan="1">

Conflicting join field types. 
</td>
            <td colspan="1" rowspan="1">

521 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErJOINNOSTATIC 
</td>
            <td colspan="1" rowspan="1">

Join files can't have static select/omits. 
</td>
            <td colspan="1" rowspan="1">

520 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErJSECKEY 
</td>
            <td colspan="1" rowspan="1">

Invalid key for join file, the key field used is from a secondary file. 
</td>
            <td colspan="1" rowspan="1">

523 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErNODUPNAME 
</td>
            <td colspan="1" rowspan="1">

No duplicate Filed name was specified. 
</td>
            <td colspan="1" rowspan="1">

509 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErNOSECNAME 
</td>
            <td colspan="1" rowspan="1">

No Secondary Filed name was specified. 
</td>
            <td colspan="1" rowspan="1">

508 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErNOSELFLDS 
</td>
            <td colspan="1" rowspan="1">

No Selected Fields were specified. 
</td>
            <td colspan="1" rowspan="1">

505 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErNOSELNAME 
</td>
            <td colspan="1" rowspan="1">

No Selected Field name was specified. 
</td>
            <td colspan="1" rowspan="1">

507 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErNOSEQJOIN 
</td>
            <td colspan="1" rowspan="1">

JoinDef out of sequence. 
</td>
            <td colspan="1" rowspan="1">

514 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErNOTJOINED 
</td>
            <td colspan="1" rowspan="1">

File is not Joined. 
</td>
            <td colspan="1" rowspan="1">

515 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErSECNOTDEF 
</td>
            <td colspan="1" rowspan="1">

Secondary File not defined. 
</td>
            <td colspan="1" rowspan="1">

504 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErSELNOTDEF 
</td>
            <td colspan="1" rowspan="1">

Selected File not defined yet. 
</td>
            <td colspan="1" rowspan="1">

503 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErTYPECONFL 
</td>
            <td colspan="1" rowspan="1">

Conflicting Field types. 
</td>
            <td colspan="1" rowspan="1">

513 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEREPOSITORY 
</td>
            <td colspan="1" rowspan="1">

Repository Access Errors. 
</td>
            <td colspan="1" rowspan="1">

500 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsALLOCERRCONTYPE 
</td>
            <td colspan="1" rowspan="1">

Allocate Error Conversation Type. 
</td>
            <td colspan="1" rowspan="1">

837 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsALLOCERRNORETRY 
</td>
            <td colspan="1" rowspan="1">

Allocate Error No Retry. 
</td>
            <td colspan="1" rowspan="1">

831 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsALLOCERRPGNNOTAVAILNR 
</td>
            <td colspan="1" rowspan="1">

Allocate Error Pgm Not Avail No Retry. 
</td>
            <td colspan="1" rowspan="1">

833 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsALLOCERRPGNNOTAVAILR 
</td>
            <td colspan="1" rowspan="1">

Allocate Error Pgm Not Avail Retry. 
</td>
            <td colspan="1" rowspan="1">

835 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsALLOCERRIPNOTALLOWED 
</td>
            <td colspan="1" rowspan="1">

Allocate Error PIP Not Allowed. 
</td>
            <td colspan="1" rowspan="1">

838 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsALLOCERRPIPNOTCORRECT 
</td>
            <td colspan="1" rowspan="1">

Allocate Error PIP Not Correct. 
</td>
            <td colspan="1" rowspan="1">

839 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsALLOCERRRETRY 
</td>
            <td colspan="1" rowspan="1">

Allocate Error Retry. 
</td>
            <td colspan="1" rowspan="1">

832 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsALLOCERRSECNOTVALID 
</td>
            <td colspan="1" rowspan="1">

Allocate Error Sec Not Valid. 
</td>
            <td colspan="1" rowspan="1">

836 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsALLOCERRSYNCHLEVEL 
</td>
            <td colspan="1" rowspan="1">

Allocate Error Sync Level. 
</td>
            <td colspan="1" rowspan="1">

840 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsALLOCERRTPNNOTRECOG 
</td>
            <td colspan="1" rowspan="1">

Allocate Error Transaction Program Not Recognized 
</td>
            <td colspan="1" rowspan="1">

834 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsAPPCBUSY 
</td>
            <td colspan="1" rowspan="1">

APPC Busy. 
</td>
            <td colspan="1" rowspan="1">

809 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsAS400ERROR 
</td>
            <td colspan="1" rowspan="1">

Error text contained in extended error info. 
</td>
            <td colspan="1" rowspan="1">

1301 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsCONVTABLEFULL 
</td>
            <td colspan="1" rowspan="1">

Conversation Table Full. 
</td>
            <td colspan="1" rowspan="1">

845 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsDEALLOCABENDPROGRAM 
</td>
            <td colspan="1" rowspan="1">

Deallocate Abend Program. 
</td>
            <td colspan="1" rowspan="1">

841 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsDEALLOCNORMAL 
</td>
            <td colspan="1" rowspan="1">

Deallocate Normal. 
</td>
            <td colspan="1" rowspan="1">

802 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsDUPSTRM 
</td>
            <td colspan="1" rowspan="1">

Duplicate Stream. 
</td>
            <td colspan="1" rowspan="1">

301 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsHDRCORRUPT 
</td>
            <td colspan="1" rowspan="1">

Corrupted header in APPC packet. 
</td>
            <td colspan="1" rowspan="1">

854 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsINSUFFICIENTMEMORY 
</td>
            <td colspan="1" rowspan="1">

Insufficient Memory. 
</td>
            <td colspan="1" rowspan="1">

832 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsINVALIDLUNAME 
</td>
            <td colspan="1" rowspan="1">

Invalid User Name. 
</td>
            <td colspan="1" rowspan="1">

852 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsINVALIDPASSWORDLEN 
</td>
            <td colspan="1" rowspan="1">

Invalid Password Length. 
</td>
            <td colspan="1" rowspan="1">

851 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsINVALIDREQ 
</td>
            <td colspan="1" rowspan="1">

Invalid request 1 received by license manager. 
</td>
            <td colspan="1" rowspan="1">

1206 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsINVALIDSUR 
</td>
            <td colspan="1" rowspan="1">

Invalid request 2 received by license manager. 
</td>
            <td colspan="1" rowspan="1">

1207 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsINVALIDUSERIDLEN 
</td>
            <td colspan="1" rowspan="1">

Invalid User ID Length. 
</td>
            <td colspan="1" rowspan="1">

850 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsINVSRLNBR 
</td>
            <td colspan="1" rowspan="1">

Invalid Serial Number. 
</td>
            <td colspan="1" rowspan="1">

1203 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsLICSRVRFAIL 
</td>
            <td colspan="1" rowspan="1">

The server in which the license is located has failed. 
</td>
            <td colspan="1" rowspan="1">

1227 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsLMERR01 
</td>
            <td colspan="1" rowspan="1">

License manager recovery error 1 
</td>
            <td colspan="1" rowspan="1">

1212 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsLMERR02 
</td>
            <td colspan="1" rowspan="1">

License manager recovery error 2. 
</td>
            <td colspan="1" rowspan="1">

1213 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsLMERR03 
</td>
            <td colspan="1" rowspan="1">

License manager recovery error 3. 
</td>
            <td colspan="1" rowspan="1">

1214 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsLMERR04 
</td>
            <td colspan="1" rowspan="1">

License manager recovery error 4. 
</td>
            <td colspan="1" rowspan="1">

1215 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsLMERR05 
</td>
            <td colspan="1" rowspan="1">

License manager recovery error 5. 
</td>
            <td colspan="1" rowspan="1">

1216 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsLMERR06 
</td>
            <td colspan="1" rowspan="1">

License manager recovery error 6. 
</td>
            <td colspan="1" rowspan="1">

1217 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsLMERR07 
</td>
            <td colspan="1" rowspan="1">

License manager recovery error 7. 
</td>
            <td colspan="1" rowspan="1">

1218 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsLMERR08 
</td>
            <td colspan="1" rowspan="1">

License manager recovery error 8. 
</td>
            <td colspan="1" rowspan="1">

1219 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsLMMUTEX 
</td>
            <td colspan="1" rowspan="1">

License manager service not accessible. 
</td>
            <td colspan="1" rowspan="1">

1208 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsLMPID 
</td>
            <td colspan="1" rowspan="1">

License manager service not started. 
</td>
            <td colspan="1" rowspan="1">

1211 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsLMSTART 
</td>
            <td colspan="1" rowspan="1">

License manager service not synchronized. 
</td>
            <td colspan="1" rowspan="1">

1210 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsLMSYNCDQ 
</td>
            <td colspan="1" rowspan="1">

License manager service sync object creation error. 
</td>
            <td colspan="1" rowspan="1">

1209 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsLMSYNCDQD 
</td>
            <td colspan="1" rowspan="1">

License manager PID data area could not be deleted 
</td>
            <td colspan="1" rowspan="1">

1223 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsMEMORYALLOCERROR 
</td>
            <td colspan="1" rowspan="1">

Memory Allocate Error. 
</td>
            <td colspan="1" rowspan="1">

843 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsMTSPCODE 
</td>
            <td colspan="1" rowspan="1">

Invalid or missing DataGate multi-tier license. 
</td>
            <td colspan="1" rowspan="1">

1220 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsMTSPRCCNT 
</td>
            <td colspan="1" rowspan="1">

DataGate multi-tier license processor count exceeded. 
</td>
            <td colspan="1" rowspan="1">

1222 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsMTSTRLEXP 
</td>
            <td colspan="1" rowspan="1">

DataGate multi-tier license expired. 
</td>
            <td colspan="1" rowspan="1">

1221 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsNODBCSCONV 
</td>
            <td colspan="1" rowspan="1">

DBCS translation not supported for given CCSIDs 
</td>
            <td colspan="1" rowspan="1">

1302 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsNOLICDLL 
</td>
            <td colspan="1" rowspan="1">

No DLL license was found. 
</td>
            <td colspan="1" rowspan="1">

1224 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsNOLICSRVR 
</td>
            <td colspan="1" rowspan="1">

No license was found on the DataGate server. 
</td>
            <td colspan="1" rowspan="1">

1225 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsNOPRODUCT 
</td>
            <td colspan="1" rowspan="1">

No license was found for this product. 
</td>
            <td colspan="1" rowspan="1">

1226 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsOK 
</td>
            <td colspan="1" rowspan="1">

OK. 
</td>
            <td colspan="1" rowspan="1">

801 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHKBADDEALLOCTYPE 
</td>
            <td colspan="1" rowspan="1">

Parm Check Bad Deallocate Type. 
</td>
            <td colspan="1" rowspan="1">

820 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHKBADFILLTYPE 
</td>
            <td colspan="1" rowspan="1">

Parm Check Bad Fill Type. 
</td>
            <td colspan="1" rowspan="1">

822 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHKBADPARTNERNAME 
</td>
            <td colspan="1" rowspan="1">

Parm Check Bad Partner Name. 
</td>
            <td colspan="1" rowspan="1">

818 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHKBADRETURNCTRL 
</td>
            <td colspan="1" rowspan="1">

Parm Check Bad Return Control. 
</td>
            <td colspan="1" rowspan="1">

816 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHKBADSUNCLVALLOC 
</td>
            <td colspan="1" rowspan="1">

Parm Check Bad Sync Level Allocated. 
</td>
            <td colspan="1" rowspan="1">

815 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHKBUFFERCROSSSEG 
</td>
            <td colspan="1" rowspan="1">

Parm Check Buffer Crosses Segment. 
</td>
            <td colspan="1" rowspan="1">

812 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHKCONFNOTALLOWED 
</td>
            <td colspan="1" rowspan="1">

Parm Check Configuration Not Allowed. 
</td>
            <td colspan="1" rowspan="1">

819 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHKINVALIDCONVERID 
</td>
            <td colspan="1" rowspan="1">

Parm Check Invalid Conversation Id. 
</td>
            <td colspan="1" rowspan="1">

811 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHKINVALIDVERB 
</td>
            <td colspan="1" rowspan="1">

Parm Check Invalid Verb. 
</td>
            <td colspan="1" rowspan="1">

810 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHKINVCONVERTYPE 
</td>
            <td colspan="1" rowspan="1">

Parm Check Invalid Conversation Type. 
</td>
            <td colspan="1" rowspan="1">

814 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHKIPTOOLONG 
</td>
            <td colspan="1" rowspan="1">

Parm Check PIP Too Long. 
</td>
            <td colspan="1" rowspan="1">

817 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHKPROPTORCVTYPE 
</td>
            <td colspan="1" rowspan="1">

821 Parm Check Prepare To Receive Type. 
</td>
            <td colspan="1" rowspan="1">

821 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHECKRECMAXLEN 
</td>
            <td colspan="1" rowspan="1">

Parm Check Record Maximum Length. 
</td>
            <td colspan="1" rowspan="1">

823 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHKRESFLDNOTZERO 
</td>
            <td colspan="1" rowspan="1">

825 Parm Check Result Field Not Zero. 
</td>
            <td colspan="1" rowspan="1">

825 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHKTPNAMELENGTH 
</td>
            <td colspan="1" rowspan="1">

Parm Check Transaction Program Name Length. 
</td>
            <td colspan="1" rowspan="1">

813 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPARMCHKUNKNOWNSECTYPE 
</td>
            <td colspan="1" rowspan="1">

Parm Check Unknown Sec Type. 
</td>
            <td colspan="1" rowspan="1">

824 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPCODE 
</td>
            <td colspan="1" rowspan="1">

Invalid or missing DataGate license. Use Registration Assistant to verify/install a valid license key. 
</td>
            <td colspan="1" rowspan="1">

1205 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPCSWINNOTLOADED 
</td>
            <td colspan="1" rowspan="1">

PCSWIN Not Loaded. 
</td>
            <td colspan="1" rowspan="1">

848 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPCSWINOUTOFMEMORY 
</td>
            <td colspan="1" rowspan="1">

PCSWIN Out Of Memory. 
</td>
            <td colspan="1" rowspan="1">

849 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPROGRAMERRNOTRUNCATION 
</td>
            <td colspan="1" rowspan="1">

Program Error No Truncation. 
</td>
            <td colspan="1" rowspan="1">

803 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPROGRAMERRPURGING 
</td>
            <td colspan="1" rowspan="1">

Program Error Purging. 
</td>
            <td colspan="1" rowspan="1">

805 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPROGRAMERRTRUNCATION 
</td>
            <td colspan="1" rowspan="1">

Program Error Truncation. 
</td>
            <td colspan="1" rowspan="1">

804 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsRESOURCEFAILURENORETR 
</td>
            <td colspan="1" rowspan="1">

Resource Failure No Retry. 
</td>
            <td colspan="1" rowspan="1">

807 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsRESOURCEFAILURERETRY 
</td>
            <td colspan="1" rowspan="1">

Resource Failure Retry. 
</td>
            <td colspan="1" rowspan="1">

806 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsROUTERNOTINSTALLED 
</td>
            <td colspan="1" rowspan="1">

Router Not Installed. 
</td>
            <td colspan="1" rowspan="1">

846 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsROUTERWRONGLEVEL 
</td>
            <td colspan="1" rowspan="1">

Router At Wrong Level. 
</td>
            <td colspan="1" rowspan="1">

847 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsSTATECHKNOTINCONFSTAT 
</td>
            <td colspan="1" rowspan="1">

State Check Not In Conf Stat. 
</td>
            <td colspan="1" rowspan="1">

826 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsSTATECHKNOTINRECEIVE 
</td>
            <td colspan="1" rowspan="1">

State Check Not In Receive. 
</td>
            <td colspan="1" rowspan="1">

827 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsSTATECHKREQSNDBADSTAT 
</td>
            <td colspan="1" rowspan="1">

State Check Not In Receive. 
</td>
            <td colspan="1" rowspan="1">

827 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsSTATECHKDNDERRBADSTAT 
</td>
            <td colspan="1" rowspan="1">

State Check Send Error in Bad State. 
</td>
            <td colspan="1" rowspan="1">

830 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsSTATECHKFNDINBADSTATE 
</td>
            <td colspan="1" rowspan="1">

State Check Send in Bad State. 
</td>
            <td colspan="1" rowspan="1">

829 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsSTRMNOTOPEN 
</td>
            <td colspan="1" rowspan="1">

Stream not open. 
</td>
            <td colspan="1" rowspan="1">

302 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsTOOMANYCONVERSATION 
</td>
            <td colspan="1" rowspan="1">

Too Many Conversations. 
</td>
            <td colspan="1" rowspan="1">

844 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsTRLEXP 
</td>
            <td colspan="1" rowspan="1">

DataGate server license expired. 
</td>
            <td colspan="1" rowspan="1">

1201 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsUNDEFINED 
</td>
            <td colspan="1" rowspan="1">

Undefined. 
</td>
            <td colspan="1" rowspan="1">

853 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsUNSUCCESSFUL 
</td>
            <td colspan="1" rowspan="1">

Unsuccessful. 
</td>
            <td colspan="1" rowspan="1">

808 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsUSRCNT 
</td>
            <td colspan="1" rowspan="1">

User Count Exceeded. 
</td>
            <td colspan="1" rowspan="1">

1204 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgSERVEXCEPTION 
</td>
            <td colspan="1" rowspan="1">

Unexpected exception on the server. 
</td>
            <td colspan="1" rowspan="1">

13 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgSQLSERVER 
</td>
            <td colspan="1" rowspan="1">

SQL Server Errors. 
</td>
            <td colspan="1" rowspan="1">

1500 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgSTREAM 
</td>
            <td colspan="1" rowspan="1">

Stream Errors. 
</td>
            <td colspan="1" rowspan="1">

300 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgSUPERVISOR 
</td>
            <td colspan="1" rowspan="1">

Supervisor Errors. 
</td>
            <td colspan="1" rowspan="1">

1000 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgSYSTEM 
</td>
            <td colspan="1" rowspan="1">

System Errors. 
</td>
            <td colspan="1" rowspan="1">

1300 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgTCPIP 
</td>
            <td colspan="1" rowspan="1">

TCP/IP Errors. 
</td>
            <td colspan="1" rowspan="1">

900 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgUNKNOWN 
</td>
            <td colspan="1" rowspan="1">

Unknown Errors. 
</td>
            <td colspan="1" rowspan="1">

1 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExDENIED 
</td>
            <td colspan="1" rowspan="1">

Access is Denied. 
</td>
            <td colspan="1" rowspan="1">

1602 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExINVLIC 
</td>
            <td colspan="1" rowspan="1">

Invalid License. 
</td>
            <td colspan="1" rowspan="1">

1603 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExMISSING 
</td>
            <td colspan="1" rowspan="1">

File is missing. 
</td>
            <td colspan="1" rowspan="1">

1601 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEXITPROG 
</td>
            <td colspan="1" rowspan="1">

Exit Program Errors. 
</td>
            <td colspan="1" rowspan="1">

1600 
</td>
          </tr>
</table>

Examples

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      /* There are many reasons why opening a file can fail. Here, we
       * catch some of the more general ones. */
      if (dgEx.Error == dgErrorNumber.dgEmMNOTFND)
          MessageBox.Show("Member " + dbFile.MemberName + " not found!", "Error opening file");
      else if (dgEx.Error == dgErrorNumber.dgEmFNOTFND)
          MessageBox.Show("File " + dbFile.FileName + " not found!", "Error opening file");
      else
          MessageBox.Show(dgEx.Message, "Error opening file");
          //Exit procedure here.
  }

  /* Do some action here. */

  dbFile.Close();
  db.Close();</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.Read

  Dim myDS As AdgDataSet = Nothing
  Try
      dbFile.OpenNewAdgDataSet(myDS)
  Catch dgEx As dgException
      ' There are many reasons why opening a file can fail. Here, we
      ' catch some of the more general ones. 
      If (dgEx.Error = dgErrorNumber.dgEmMNOTFND) Then
          MsgBox("Member " + dbFile.MemberName + " not found!", "Error opening file")
      ElseIf (dgEx.Error = dgErrorNumber.dgEmFNOTFND) Then
          MsgBox("File " + dbFile.FileName + " not found!", "Error opening file")
      Else
          MsgBox(dgEx.Message, "Error opening file")
          'Exit procedure here.
      End If
  End Try

  ' Do some action here. 

  dbFile.Close()
  db.Close()</pre>

Requirements

**Namespace:** [ ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [Error Field](dcsdgExceptionClassErrorField.html)
      <br />
      [dgException Class](dcsdgExceptionClass.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

