---
title: Edit Code Table

Id: sharedEditCodeTable
TocParent: amfDdsDecFieldClassEditCodeProperty
TocOrder: 10

keywords: EditCode, property setting
keywords: edit codes, table

---

Using the **EditCode** property or keyword allows you to punctuate numeric fields, including $ signs, commas, periods, minus sign, and floating minus according to the standard RPG edit code rules. 

Enter a valid edit code as listed in the table below that gives you the desired display. For example, using EditCode **J** will display .00, giving you commas, decimals points, and a minus sign when necessary.

#### Edit Code Values
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
      <colgroup>
      <col width="10%" align="center" valign="middle"  />
      <col width="10%" align="center" valign="middle" />
      <col width="10%" align="center" valign="middle" />
      <col width="15%" align="center" valign="middle" />
      <col width="20%" align="center" valign="middle" />
      <col width="20%" align="center" valign="middle" />
     </colgroup>
        <tr>
          <th align="center" colspan="4" rowspan="1" valign="middle" id="cole" width="50%">
		    </th>
          <th align="center" colspan="2" rowspan="1" valign="middle" id="colf" width="50%">Display
          <br />(assuming US Regional Settings)</th>
        </tr>
        <tr>
          <th>Edit Code</th>
          <th>Commas</th>
          <th>Decimal Point</th>
          <th>Sign for Negative Balance</th>
          <th>'.'</th>
          <th>Zero Suppress</th>
        </tr>
        <tr>
          <td>1</td>
          <td>Yes</td>
          <td>Yes</td>
          <td>No Sign</td>
          <td>.00 or 0</td>
          <td >Yes</td>
        </tr>
        <tr>
          <td>2</td>
          <td>Yes</td>
          <td>Yes</td>
          <td>No Sign</td>
          <td>Blanks</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>3</td>
          <td>
            <br />
          </td>
          <td>Yes</td>
          <td>No Sign</td>
          <td>.00 or 0</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>4</td>
          <td>
            <br />
          </td>
          <td>Yes</td>
          <td>No Sign</td>
          <td>Blanks</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>5 - 9<sup>(1)</sup></td>
          <td>
            <br />
          </td>
          <td>
            <br />
          </td>
          <td>
            <br />
          </td>
          <td>
            <br />
          </td>
          <td>
            <br />
          </td>
        </tr>
        <tr>
          <td>A</td>
          <td>Yes</td>
          <td>Yes</td>
          <td>CR</td>
          <td>.00 or 0</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>B</td>
          <td>Yes</td>
          <td>Yes</td>
          <td>CR</td>
          <td>Blanks</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>C</td>
          <td>
            <br />
          </td>
          <td>Yes</td>
          <td>CR</td>
          <td>.00 or 0</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>D</td>
          <td>
            <br />
          </td>
          <td>Yes</td>
          <td>CR</td>
          <td>Blanks</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>J</td>
          <td>Yes</td>
          <td>Yes</td>
          <td>- (minus)</td>
          <td>.00 or 0</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>K</td>
          <td>Yes</td>
          <td>Yes</td>
          <td>- (minus)</td>
          <td>Blanks</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>L</td>
          <td>
            <br />
          </td>
          <td>Yes</td>
          <td>- (minus)</td>
          <td>.00 or 0</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>M</td>
          <td>
            <br />
          </td>
          <td>Yes</td>
          <td>- (minus)</td>
          <td>Blanks</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>N</td>
          <td>Yes</td>
          <td>Yes</td>
          <td>- (floating
          minus)</td>
          <td>.00 or 0</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>O</td>
          <td>Yes</td>
          <td>Yes</td>
          <td>- (floating
          minus)</td>
          <td>Blanks</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>P</td>
          <td>
            <br />
          </td>
          <td>Yes</td>
          <td>- (floating
          minus)</td>
          <td>.00 or 0</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>Q</td>
          <td>
            <br />
          </td>
          <td>Yes</td>
          <td>- (floating
          minus)</td>
          <td>Blanks</td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>X <sup>(2)</sup></td>
          <td>
            <br />
          </td>
          <td>
            <br />
          </td>
          <td>
            <br />
          </td>
          <td>
            <br />
          </td>
          <td>
            <br />
          </td>
        </tr>
        <tr>
          <td>Y
          <sup>(3)</sup></td>
          <td>
            <br />
          </td>
          <td>
            <br />
          </td>
          <td>
            <br />
          </td>
          <td>
            <br />
          </td>
          <td>Yes</td>
        </tr>
        <tr>
          <td>Z
          <sup>(4)</sup></td>
          <td>
            <br />
          </td>
          <td>
            <br />
          </td>
          <td>
            <br />
          </td>
          <td>
            <br />
          </td>
          <td>Yes</td>
        </tr>

</table>

#### Table Notes:

1. These are the user-defined edit codes.
2. The X edit code ensures a hexadecimal F sign for
              positive values. Because the system does this for
              you, normally you do not have to specify this
              code.
3. The Y edit code suppresses the leftmost zeros of
              date fields, up to but not including the digit
              preceding the first separator. The Y edit code also
              inserts slashes (/) between the month, day, and year
              according to the following pattern: 
              <pre>    nn/n
   nn/nn
   nn/nn/n
   nn/nn/nn
  nnn/nn/nn
   nn/nn/nnnn
  nnn/nn/nnnn
 nnnn/nn/nn
nnnnn/nn/nn
</pre>
4. The Z edit code removes the sign (plus or minus)
              from a numeric field and suppresses leading
              zeros.

#### See Also
<dl>
        <dd>[EditWord
        Usage](sharedEditWordTable.html)</dd>

</dl>

