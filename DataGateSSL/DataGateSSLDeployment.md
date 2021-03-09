---
title: DataGate SSL Deployment Guide

Id: DataGateSSLDeployment
TocParent: Welcome
TocOrder: 20

keywords: ASNA DataGate
keywords: ASNA DataGate SSL
keywords: Secure Socket Layer
keywords: Deploying DataGate with SSL
keywords: SSL
keywords: SSL Deployment

---

<table>
                    <tr>
                        <td>
                            <span class="OH_MultiViewContainerPanelDhtmlTable">
                                [
                                    SSL for ASNA
                                    DataGate &#174; Reference Manual
                                ](Welcome.html)
                            </span>
                        </td>
                    </tr>
</table>

# DataGate SSL Deployment

---

Several tools are included in the DataGate suite to assist in the configuration of SSL-based secure connections. This document introduces these tools and provides step-by-step guidance for configuring connections for typical scenarios. To use this document effectively, you should be familiar with SSL basics. For advanced scenarios including secure server authentication, you should be familiar with the general concepts of SSL certificates, certificate stores, and the Windows and/or IBM i platform tools for managing them. This document must not be considered a basis for securing your network from unwanted intrusions. Rather it is a reference for using the SSL facilities provided by DataGate and its platforms for implementing a small facet of an overall network security policy. 

- [Windows-based DataGate Server](DataGateSSLWindows.html)
- [DataGate for IBM i](DataGateSSLIBMi.html)
- [DataGate Client](DataGateSSLClient.html)

## DataGate Server
DataGate/400, DataGate for SQL Server (DSS) and DataGate for Windows Servers and Desktops are the ASNA servers which support SSL connections to DataGate client programs such as AVR and DataGate Studio. Windows and IBM i platforms have different tools for configuring SSL specifically for their environments. 
