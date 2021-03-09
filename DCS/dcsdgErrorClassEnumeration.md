---
title: dgErrorClass Enumeration

Id: dcsdgErrorClassEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 11

keywords: dgErrorClass enumeration
keywords: enumerations [DCS 16.0 dgErrorClass
keywords: classes of errors
keywords: run time errors, category of
keywords: category of run-time errors
keywords: errors, classes of
keywords: dgEC_Access enumeration member
keywords: dgEC_APPC enumeration member
keywords: dgEC_AS400CPF enumeration member
keywords: dgEC_AS400CPI enumeration member
keywords: dgEC_AS400DG8 enumeration member
keywords: dgEC_AS400MCH enumeration member
keywords: dgEC_Base enumeration member
keywords: dgEC_CallParm enumeration member
keywords: dgEC_Catalog enumeration member
keywords: dgEC_Command enumeration member
keywords: dgEC_CommitCtrl enumeration member
keywords: dgEC_Compiler enumeration member
keywords: dgEC_ExitPoints enumeration member
keywords: dgEC_License enumeration member
keywords: dgEC_Object enumeration member
keywords: dgEC_Print enumeration member
keywords: dgEC_Repository enumeration member
keywords: dgEC_SqlServer enumeration member
keywords: dgEC_Stream enumeration member
keywords: dgEC_Supervisor enumeration member
keywords: dgEC_System enumeration member
keywords: dgEC_TCPIP enumeration member
keywords: dgEC_Unknown enumeration member

---

Specifies the class, or category of the DCS run-time error.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public enum dgErrorClass;** 
      </pre>
		  <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Enum dgErrorClass** 
      </pre>
		  <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegEnum dgErrorClass Access(*Public)** 
      </pre>

				  Remarks

The <span>dgErrorClass</span> enumeration is used as a parameter by the [ErrorClass](dcsdgExceptionClassErrorClassField.html) field of the [dgException](dcsdgExceptionClass.html) class.
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
						  <colgroup span="1">
							  <col align="middles" span="1" width="15%" style="FONT-WEIGHT: bold" />
							  <col span="1" width="40%" />
							  <col span="1" width="5%" />
						  </colgroup>
						  <tr>
							  <th colspan="1" rowspan="1">Member</th>
							  <th colspan="1" rowspan="1">Description</th>
							  <th colspan="1" rowspan="1">Value</th>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_Access
</td>
							  <td colspan="1" rowspan="1">

Access errors.
</td>
							  <td colspan="1" rowspan="1">

3
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_APPC
</td>
							  <td colspan="1" rowspan="1">

APPC errors.
</td>
							  <td colspan="1" rowspan="1">

10
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_AS400CPF
</td>
							  <td colspan="1" rowspan="1">

IBM i CPF errors.
</td>
							  <td colspan="1" rowspan="1">

16
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_AS400CPI
</td>
							  <td colspan="1" rowspan="1">

IBM i CPI errors.
</td>
							  <td colspan="1" rowspan="1">

18
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_AS400DG8
</td>
							  <td colspan="1" rowspan="1">

IBM i DataGate errors.
</td>
							  <td colspan="1" rowspan="1">

19
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_AS400MCH
</td>
							  <td colspan="1" rowspan="1">

IBM i MCH errors.
</td>
							  <td colspan="1" rowspan="1">

17
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_Base
</td>
							  <td colspan="1" rowspan="1">

Base errors.
</td>
							  <td colspan="1" rowspan="1">

1
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_CallParm
</td>
							  <td colspan="1" rowspan="1">

Call/Parm errors.
</td>
							  <td colspan="1" rowspan="1">

8
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_Catalog
</td>
							  <td colspan="1" rowspan="1">

Catalog errors. 
</td>
							  <td colspan="1" rowspan="1">

2 
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_Command
</td>
							  <td colspan="1" rowspan="1">

Command errors.
</td>
							  <td colspan="1" rowspan="1">

13
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_CommitCtrl
</td>
							  <td colspan="1" rowspan="1">

Commitment Control errors.
</td>
							  <td colspan="1" rowspan="1">

20
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_Compiler
</td>
							  <td colspan="1" rowspan="1">

Compiler errors.
</td>
							  <td colspan="1" rowspan="1">

5
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_ExitPoints
</td>
							  <td colspan="1" rowspan="1">

ExitPoints errors.
</td>
							  <td colspan="1" rowspan="1">

22
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_License
</td>
							  <td colspan="1" rowspan="1">

License errors.
</td>
							  <td colspan="1" rowspan="1">

14
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_Object
</td>
							  <td colspan="1" rowspan="1">

Object errors.
</td>
							  <td colspan="1" rowspan="1">

7
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_Print
</td>
							  <td colspan="1" rowspan="1">

Print errors
</td>
							  <td colspan="1" rowspan="1">

9
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_Repository
</td>
							  <td colspan="1" rowspan="1">

Repository errors.
</td>
							  <td colspan="1" rowspan="1">

6
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_SqlServer
</td>
							  <td colspan="1" rowspan="1">

SQL Server errors.
</td>
							  <td colspan="1" rowspan="1">

21
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_Stream
</td>
							  <td colspan="1" rowspan="1">

Stream errors.
</td>
							  <td colspan="1" rowspan="1">

4
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_Supervisor
</td>
							  <td colspan="1" rowspan="1">

Supervisor errors.
</td>
							  <td colspan="1" rowspan="1">

12
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_System
</td>
							  <td colspan="1" rowspan="1">

System errors.
</td>
							  <td colspan="1" rowspan="1">

15
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_TCPIP
</td>
							  <td colspan="1" rowspan="1">

TCP/IP errors.
</td>
							  <td colspan="1" rowspan="1">

11
</td>
						  </tr>
						  <tr>
							  <td colspan="1" rowspan="1">

dgEC_Unknown
</td>
							  <td colspan="1" rowspan="1">

Unknown errors.
</td>
							  <td colspan="1" rowspan="1">

0
</td>
						  </tr>
</table>

Examples

<pre class="prettyprint">        <span class="lang">
 **[C#]** 
        </span>
  /* This code attempts to open a file exclusively. 
   * If it fails, we print out the IBM i exception responsible.
   * "dbFile" is of type FileAdapter. */ 
  dbFile.AccessMode = AccessMode.Write;
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive;

  AdgDataSet dataSet = null;
  try
  {
      dbFile.Open(dataSet);
  }
  catch(dgException dgEx)
  {
      string msg;
      switch(dgEx.ErrorClass)
      {
          case dgErrorClass.dgEC_AS400CPF:
              msg = "CPF";
              break;
          case dgErrorClass.dgEC_AS400CPI:
              msg = "CPI";
              break;
          case dgErrorClass.dgEC_AS400DG8:
              msg = "DG8";
              break;
          case dgErrorClass.dgEC_AS400MCH:
              msg = "MCH";
              break;
          default:
              throw dgEx; /* Throw exception otherwise. */
      }
      /* Append the hexadecimal value of the SystemError to
       * form the classic name of the IBM i exception. */
      msg = msg + dgEx.SystemError.ToString("X");
      MessageBox.Show("iSeries threw exception " + msg + 
          " while opening file.", "iSeries exception.");
      /* Throw exception otherwise. */
      throw dgEx;
  }
</pre>
					  <pre class="prettyprint">        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' This code attempts to open a file exclusively. 
  ' If it fails, we print the IBM i exception responsible.
  ' "dbFile" is of type FileAdapter. 
  dbFile.AccessMode = AccessMode.Write
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive

  Dim dataSet As AdgDataSet = Nothing
  Try
      dbFile.Open(dataSet)
  Catch dgEx As dgException
      Dim msg As String
      Select Case dgEx.ErrorClass
          Case dgErrorClass.dgEC_AS400CPF
              msg = "CPF"
          Case dgErrorClass.dgEC_AS400CPI
              msg = "CPI"
          Case dgErrorClass.dgEC_AS400DG8
              msg = "DG8"
          Case dgErrorClass.dgEC_AS400MCH
              msg = "MCH"
          Case Else
              Throw dgEx ' Throw exception otherwise. 
      End Select
      ' Append the hexaDecimal value of the SystemError to
      ' Form the classic name of the IBM i exception. 
      msg = msg + dgEx.SystemError.ToString("X")
      MsgBox("iSeries threw exception " &amp; msg &amp; _
          " While opening file.", "iSeries exception.")
      ' Throw exception otherwise. 
      Throw dgEx
  End Try
</pre>

							  Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
								  [ErrorClass Field](dcsdgExceptionClassErrorClassField.html)
								  <br />
								  [dgException Class](dcsdgExceptionClass.html)
								  <br />
								  [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

