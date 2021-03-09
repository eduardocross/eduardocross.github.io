---
title: Installing ASNA Browser Terminal on the IBM i

Id: emInstallingIBMi
TocParent: emInstallingMain
TocOrder: 30

keywords: ASNA Browser Terminal
keywords: Emu

---

<table>
                <tr>
                    <td>
                        <span class="OH_MultiViewContainerPanelDhtmlTable">
                            ASNA Browser Terminal&#8482; Admin Manual
                        </span>
                    </td>
                </tr>
</table>

# Installing ASNA Browser Terminal on the IBM i
This topic offers an overview of installing Browser Terminal components onto the IBM i. 

---

#### Runtime environment
*Software requirements for the IBM i* . 

- **IBM i V6R1 or higher**
- **ASNA DataGate for IBM i &#8211;** This
                        provides access to the IBM i for reading display file
                        and message file definitions.

#### On the IBM i BTerm will be used on
**1. Confirm IBM i version** <br />Use the WRKLICINF IBM i command to confirm the IBM i is at V6R1 or higher. If not, you will need to upgrade to V6R1 or higher before continuing. 

**2. Install ASNA DataGate for IBM i** 

Be sure to have signed into the [ here ](http://devnet.asna.com">ASNA's Developer Network</a> site before using the links referenced here. Download ASNA DataGate 12.0 for IBM i <a href="http://devnet.asna.com/downloads/Pages/ASNADataGate140forIBMi.aspx"> here </a>. Follow the installation instructions on that page or view them <a href="http://devnet.asna.com/documentation/Help140/Readmes/DataGate_iSeries_140_Readme.html). Be sure to follow the instructions for licensing DataGate for IBM i. If you need a license code, please contact ASNA technical support at 800-289-2762 or 210-408-0212, email us at [ IBM's System value information ](mailto:support@asna.com"> support@asna.com </a>, or contact your ASNA sales representative. 

During the installation of DataGate for IBM i, you will enter a TCP/IP port number. Make a note of that value. You may need it later. 

**3. Update System Values** 

Updating system values requires the use of the IBM i<sup>TM</sup> Navigator, for more information on working with system values in general, see <a href="http://publib.boulder.ibm.com/infocenter/iseries/v7r1m0/index.jsp?topic=%2Frzakz%2Frzakz1.html) entry. 

The following System Values are required on the IBM i to support the ASNA Browser Terminal: 

- [
                            QMLTTHDACN
                        ](http://publib.boulder.ibm.com/infocenter/iseries/v5r3/index.jsp?topic=%2Frzakz%2Frzakzqmltthdacn.html): 1 or 2, required because some  operations are
                        multi-threaded.
- [
                            QRMTSIGN
                        ](http://publib.boulder.ibm.com/infocenter/iseries/v6r1m0/index.jsp?topic=/rzarl/rzarlrmctrl.html): *VERIFY, required because  BTerm doesn't use a standard
                        5250 sign-on.

&#160;
