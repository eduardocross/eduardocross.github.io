---
title: Program.SqlCursor Class Members

Id: amfProgramSqlCursorClassMembers
TocParent: amfProgramSqlCursorClass
TocOrder: 5

keywords: Program.SqlCursor class, all members
keywords: members [ASNA.Monarch], Program.SqlCursor class
keywords: SqlCursor class, members

---

[ Program.SqlCursor Class Overview](amfProgramSqlCursorClass.html) 
<!--mine -->

#### Constructor
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Method</th>
            <th>Description</th>
          </tr>
         <tr>
            <td><img id="IMG1" style="WIDTH: 16px; HEIGHT: 16px" alt="public property" src="../Images/Constructor.bmp" width="15" border="0" x-maintain-ratio="TRUE" />  
            [
            SqlCursor](amfProgramSqlCursorClassConstructors.html)</td>
            <td>Overloaded. Creates a
            new instance of a Program.SqlCursor object.</td>
          </tr>
</table>

<!--mine -->

#### Public Methods
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Method</th>
            <th>Description</th>
          </tr>
          <tr>
            <td><img id="Img6" style="WIDTH: 16px; HEIGHT: 16px" alt="public method" src="../Images/Methods.bmp" width="15" border="0" x-maintain-ratio="TRUE" />  
            [
            Close](amfProgramSqlCursorClassCloseMethod.html)</td>
            <td>Closes a
            Program.SqlCursor.</td>
          </tr>
          <tr>
            <td><img id="Img7" style="WIDTH: 16px; HEIGHT: 16px" alt="public method" src="../Images/Methods.bmp" width="15" border="0" x-maintain-ratio="TRUE" />  
            [
            Fetch](amfProgramSqlCursorClassFetchMethod.html)</td>
            <td>Determines if results
            are available and conditions the lines that
            retrieve the query results by the 
            [
            SqlCursor.FetchOrientations](amfProgramSqlCursorFetchOrientationsEnumeration.html) value.</td>
          </tr>
          <tr>
            <td><img id="Img8" style="WIDTH: 16px; HEIGHT: 16px" alt="public method" src="../Images/Methods.bmp" width="15" border="0" x-maintain-ratio="TRUE" />  
            [
            Open](amfProgramSqlCursorClassOpenMethods.html)</td>
            <td>Overloaded. Executes the
            select statement and populates the SQL cursor with
            or without select statement variables</td>
          </tr>
          <tr>
            <td><img id="Img9" style="WIDTH: 16px; HEIGHT: 16px" alt="public method" src="../Images/Methods.bmp" width="15" border="0" x-maintain-ratio="TRUE" />  
            [
            SqlQueryResultsByIndex](amfProgramSqlCursorClassSqlQueryResultsByIndexMethod.html)</td>
            <td>Returns an object from the
            SqlCursor result set by index.</td>
          </tr>
</table>

#### Public Fields
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Field</th>
            <th>Description</th>
          </tr>          <tr>
            <td><img id="Img2" style="WIDTH: 16px; HEIGHT: 16px" alt="fields" src="../Images/Field.bmp" width="15" border="0" x-maintain-ratio="TRUE" />
              [
              ScrollType](amfProgramSqlCursorClassScrollTypeField.html)
            </td>
            <td>A 
            [
            SqlCursor.ScrollTypes](amfProgramSqlCursorScrollTypesEnumeration.html) enumeration value
            defining the type of scrolling for the cursor.</td>
          </tr>
          <tr>
            <td><img id="Img3" style="WIDTH: 16px; HEIGHT: 16px" alt="fields" src="../Images/Field.bmp" width="16" border="0" x-maintain-ratio="TRUE" />
              [
              SelectStatement](amfProgramSqlCursorClassSelectStatementField.html)
            </td>
            <td>The select
            statement with which the result set was
            created.</td>
          </tr>
          <tr>
            <td><img id="Img5" style="WIDTH: 16px; HEIGHT: 16px" alt="fields" src="../Images/Field.bmp" border="0" x-maintain-ratio="TRUE" />
              [
              SQLCA](amfProgramSqlCursorClassSQLCAField.html)
            </td>
            <td>[
            SQL_CommunicationsArea](amfProgramSQL_CommunicationsAreaClass.html) object to trap and report
            run-time errors for the SqlCursor.</td>
          </tr>
          <tr>
            <td><img id="Img4" style="WIDTH: 16px; HEIGHT: 16px" alt="fields" src="../Images/Field.bmp" width="15" border="0" x-maintain-ratio="TRUE" />
              [
              SqlQueryResults](amfProgramSqlCursorClassSqlQueryResultsField.html)
            </td>
            <td>A collection
            representing the query results (string and object)
            allowing values for a particular column to be
            accessed by name.</td>
          </tr>
</table>

#### See Also
[ASNA.Monarch Namespace](amfMonarchNamespace.html) <br /> [Program.SqlCursor Class](amfProgramDBParmClass.html) <br /> [ Program.SQL_CommunicationsArea Class](amfProgramSQL_CommunicationsAreaClass.html) <br /> [ SqlCursor.ScrollTypes Enumeration](amfProgramSqlCursorScrollTypesEnumeration.html) <br /> [ SqlCursor.FetchOrientations Enumeration](amfProgramSqlCursorFetchOrientationsEnumeration.html) 
