---
title: BTerm Double Byte Support

Id: emDoubleByte
TocParent: TerminalEmulation
TocOrder: 70

keywords: ASNA Bterm
keywords: ASNA BTerm DoubleByte
keywords: DBCS

---

<table>
                <tr>
                    <td>
                        <span class="OH_MultiViewContainerPanelDhtmlTable">
                            ASNA BTerm Admin Manual
                            <br />
                        </span>
                    </td>
                </tr>
</table>

# Double Byte Support
This topic describes BTerm's support for languages which use the Double Byte Character Set (DBCS). 

### New Support in 14.0
As of version 14.0, the following DBCS code pages will be supported with the optional ASNA DBCS library. This library is a drop-in that can be recognized by the ASNA runtime via the Microsoft Extensibility Framework (MEF). Support for other CCSIDs can be added by the user via MEF by implementing the ASNA.Runtime.IConverterFactory interface. Converters added via MEF will take precedence over existing converters (e.g. if you use the ASNA DBCS library the converter for 37 will be taken from it instead of using the default provided by .Net – 37 is included in the DBCS library as it’s needed by 937). 

For reference, the CCSIDs defined on the IBM i are [ http://www-03.ibm.com/systems/i.software/globalization/codepages.html ](">listed here</a>.
<table>
                    <tr>
                    <td>CCSID</td>
                    <td>Description</td></tr>
                    <tr><td>37</td><td>USA, Canada (S/370), Netherlands, Portugal, Brazil, Australia, New Zealand</td></tr>
                    <tr><td>290</td><td>Japan Katakana (extended)</td></tr>
                    <tr><td>833</td><td>Korea (extended)</td></tr>
                    <tr><td>834</td><td>Korea - including 1880 UDC</td></tr>
                    <tr><td>835</td><td>Traditional Chinese - including 6204 UDC</td></tr>
                    <tr><td>836</td><td>Simplified Chinese (extended)</td></tr>
                    <tr><td>837</td><td>Simplified Chinese - including 1880 UDC</td></tr>
                    <tr><td>939</td><td>Japan English/Kanji (extended) - including 4370 UDC</td></tr>
                    <tr><td>1364</td><td>Korea (extended)</td></tr>
                    <tr><td>1388</td><td>Traditional Chinese</td></tr>
                    <tr><td>1399w</td><td>Japan English/Kanji</td></tr>
                    <tr><td>4396</td><td>Japan - including 1880 UDC</td></tr>
                    <tr><td>4930</td><td>Korea Windows</td></tr>
                    <tr><td>5026</td><td>Japan Katakana/Kanji (extended) - including 1880 UDC</td></tr>
                    <tr><td>5035</td><td>Japan English/Kanji (extended) - including 1880 UDC</td></tr>
                    <tr><td>5123</td><td>Japanese Latin Host Extended SBCS (includes euro)</td></tr>
                    <tr><td>13124</td><td>Traditional Chinese</td></tr>
                    <tr><td>16684</td><td>Japanese Latin Host Double-Byte including 4370 UDC (includes euro)</td></tr>
</table>

The DBCS is the IBM i's support for languages requiring more than 256 characters. In it, each character is represented by 2 bytes (hence Double-Byte). 

The DBCS supports four languages:

- Simplified Chinese
- Traditional Chinese
- Japanese
- Korean

There are multiple CCSIDs that can be used for each of the above languages; these have been introduced and updated over time to include additional characters like the Euro. IBM i and BTerm both support Unicode as a special case (support for Unicode and Double-Byte was added with BTerm 8.0). 

A great deal of information on the topic can be found in at <a href="http://www-03.ibm.com/systems/i.software/globalization/codepages.html) in PDF form. It covers the current IBM code pages, many of which are supported by IBM i servers. 

### DBCS Types
There are 4 "types" of DBCS fields in DDS. For more detail on the types, check here: ([http://pic.dhe.ibm.com/infocenter/iseries/v6r1m0/index.jsp?topic=/rzakc/dbcdtype.htm](http://pic.dhe.ibm.com/infocenter/iseries/v6r1m0/index.jsp?topic=/rzakc/dbcdtype.html)): 

- J (Only) &#8211; accepts only DBCS characters.  The Field Length must be an even number (of bytes).
                        The display station automatically inserts shift-control characters in fields specified with this data type.
- E (Either)  &#8211;
                        accepts either DBCS or alphanumeric (single byte)
                        characters. The field length must be an even number (of
                        bytes)<br />DBCS or alphanumeric characters can be typed
                        into the field. The type of data entered into the
                        field's first position determines the type of data that
                        the rest of the field will accept. If blank, the
                        system assumes alphanumeric data will be entered
                        Positioning the cursor on the field and putting the
                        keyboard in DBCS mode readies the field to accept DBCS
                        data.
- O (Open) &#8211; accepts a mixture of single- and double-byte characters. The length must be a multiple
                        of 1 (bytes). <br />
                        If the field contains DBCS data, the system does not ensure that the data is enclosed between shift-control characters.
- G (Graphic) — accepts exclusively DBCS data. The
                        length specifies the number of characters, not of bytes.<br />
                        Data typed in this field does not contain shift-control characters.

A unicode field is considered type "G" with a explicit CSID value of 1200 for UTF-16 and 13488 for UCS-2. 

For more information on Unicode fields in IBM i, check here [ http://pic.dhe.ibm.com/infocenter/iseries/v6r1m0/topic/rzakc/dspfil.htm ](http://pic.dhe.ibm.com/infocenter/iseries/v6r1m0/topic/rzakc/dspfil.html) 

In BTerm the special case for Unicode has been promoted as a separate DBCS type. 
