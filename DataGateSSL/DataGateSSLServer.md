---
title: DataGate SSL Support

Id: DataGateSSLServer
TocParent: Welcome
TocOrder: 10

keywords: ASNA DataGate
keywords: ASNA DataGate SSL
keywords: Secure Socket Layer
keywords: DataGate with SSL Support
keywords: SSL
keywords: SSL Support

---

<table>
                    <tr>
                        <td>
                            <span class="OH_MultiViewContainerPanelDhtmlTable">
                                [
                                    ASNA DataGate&#174; SSL Reference Manual
                                ](Welcome.html)
                            </span>
                        </td>
                    </tr>
</table>

# DataGate SSL Support

---

## SSL Overview
The Secure Sockets Layer (SSL) is much evolved from its origins as the Netscape-implemented solution for encrypting and authenticating HTTP sessions over TCP/IP. SSL is actually a more generalized network protocol, intended to be implemented above the network transport layer (or, the connection "socket"). The SSL standard is documented in a series of Internet technical drafts and RFCs, some of which serve only to deprecate prior standards, which were later proven to be insecure. However, the fundamentals of SSL have remained generally constant: SSL provides network *privacy* via data encryption, and network *authentication* via a system of authorized certificate signing (including services offered by the so-called trusted third-party certificate authorities, such as [DataGate SSL Deployment](https://www.digicert.com/">DigiCert</a>, <a href="https://www.thawte.com/">Thawte</a>, and others). 

SSL certificates are machine-formatted documents that minimally express a network node's public key and the separate, authorized certificate used to cryptographically sign it. Such a certificate can be sent to the network peer upon initial connection. Network nodes generally also have a certificate containing the node's private key, which is used with the peer node's public key to encrypt and decrypt SSL messages. The swapping of the nodes' public key-containing certificates is part of the *negotiation* phase of an SSL connection. 

SSL history and the current standard is well documented by the Internet Engineering Task Force's RFC process, and today all well-known security omissions in the latest versions of the protocol have been addressed by either abandoning earlier versions, or extending newer ones. However, the implementations of operating system and hardware vendors are almost continually refined by software updates. For example, a serious vulnerability was found in the SSL 3.0 protocol (the so-called POODLE attack) leading to the deprecation of SSL 3.0 in the current standard. The subsequent TLS 1.0, 1.1, and 1.2 protocols in the current SSL standard are not vulnerable to POODLE and similar attacks. 

## SSL and DataGate
DataGate SSL support exclusively utilizes the latest TLS protocols of SSL. DataGate uses SSL system library APIs provided by Microsoft.NET, Windows, and OS/400. The well-known, open-source OpenSSL library is not used by DataGate at this time, though certificates generated by OpenSSL tools may be used if permitted by the certificate stores provided by the platform. 

As threats to SSL implementations emerge in the future, ASNA will attempt to track and notify its users of possible problems and upgrade DataGate software as necessary, just as IBM and Microsoft do for their platforms. Note however, that no security system is ever completely invulnerable. DataGate SSL support should be only one component of an application's overall system network security design. 

## DataGate Server Supported Security Levels
Often DataGate client and server software are not always deployed simultaneously. Also, some client and server hardware may not be up to the challenge of efficiently utilizing the complete SSL feature set. Therefore, DataGate Server's SSL support will be offered as a set of configurable levels and options with increasing security. The basic security levels are outlined below. 

- **No SSL** . Requests from clients for strictly SSL-secured connections will be denied as an error. This will be the security level of
                                previous-generation DataGate servers without SSL support.
- **Low-security SSL** . Encrypted content connections will be honored for clients requesting SSL support. The server certificate
                                used for negotiating the secure channel may be created by the server program itself, at either connect-time or server-start-time,
                                or a "default" certificate may be used. The client cannot securely authenticate the server with this certificate, but network data
                                packets are encrypted. This is likely a good choice for "default-level" functionality because it requires little or no corresponding
                                platform or network management. Due to the lack of reliable server authentication however, it is more vulnerable to
                                "man-in-the-middle" attacks than higher levels.
- **Medium-security SSL** . Secure connections will be honored for clients requesting this service. The certificate used for
                                negotiating the secure connection must be installed in the server platform's certificate store, along with the corresponding
                                private key. The certificate's subject name (Common Name, CN=) must be A) the fully qualified domain name of the server, as
                                verified by the network DNS service, or B) an alias known to the client as corresponding to the server's IP address (say, as
                                configured by the client's TCP/IP hosts file). The client may compare the certificate's subject name against the server's
                                identity, as revealed by the DNS network service, for the purpose of server authentication. Optionally, the client may allow
                                the server certificate subject name to match a given name, rather than the DNS name.
- **High-security SSL** . Builds upon Medium-security SSL, with the further restriction that the server's certificate must be
                                the end element in a secure chain of signed certificates originating from a well-known root certificate authority (CA). The
                                certificate of the CA must be installed in the client platform's trusted CA certificate store. If the client cannot verify
                                the authenticity of the CA by comparing it to the contents of the certificate store, it may abandon the request. Additionally,
                                the client may demand that the server offer only high-security connections to all clients, as opposed to combinations of
                                connections with varying levels of security.

## Configuration Considerations
Note that the above options need not be mutually exclusive. For example, the server may honor any contiguous range of the above four options. If a client requests an option above the maximum level or below the minimum level offered by the server, the request must be denied with an error. If the client requests an option within the range of allowable options offered by the server, the client may in turn be offered a security level within the server's range, but higher than requested. The client may then choose to abandon the request, based on its abilities or configuration. 

Also note, the SSL platform implementations, in particular OS/400, may impose restrictions and requirements, including the installation of additional software and/or hardware, that make the administration of higher levels difficult or impractical. Furthermore, there is run-time overhead associated with SSL-enabled connections, because of the need to encrypt/decrypt each network message. In general, the higher the level of security, the greater the imposition on client and server resources. 

## Client Authentication
SSL includes optional features used to authenticate client credentials, such as, say, the user of the database. However, DataGate already implements a well-established and reliable method of authenticating database users. Therefore, the client authentication feature of SSL will not be employed by DataGate. 

## DataGate SSL Configuration
To help simplify the task of configuring SSL connections, DataGate client and server software will respect a single "SSL level" each, which will dictate how the client will initiate, and the server respond to, requests for secure connections. Additionally, the client may be configured to recognize a server certificate as authentic at connection-time. The following tables summarize the SSL levels that the server and client can be configured with, and following the tables are some examples of their usages. 
<table align="center" border="1">

                            <tr><td bgcolor="66CBEE" align="center"> ***DataGate Server Level*** </td><td bgcolor="66CBEE" align="center"> ***Description*** </td></tr>
                            <tr>
                                <td> *Unavailable* </td>
                                <td>
                                    SSL connections not offered, clients may only connect with clear-text
                                    communications. SSL connection requests are denied.
                                </td>
                            </tr>
                            <tr>
                                <td> *Best Available* </td>
                                <td>
                                    SSL TLS 1.x connections are offered to clients that request them,
                                    and clear-text connections are offered to clients that request them.
                                </td>
                            </tr>
                            <tr>
                                <td> *SSL Required* </td>
                                <td>
                                    Only SSL TLS 1.x connections are offered to clients. Clear-text
                                    connections are denied.
                                </td>
                            </tr>

<table align="center" border="1">

                                <tr><td bgcolor="66CBEE" align="center"> ***DataGate Client Level*** </td><td bgcolor="66CBEE" align="center"> ***Description*** </td></tr>
                                <tr><td> *Clear* </td><td>Request a clear-text connection to the server, not utilizing SSL.</td></tr>
                                <tr><td> *Request* </td><td>Request an SSL connection, but if not offered by the server, request a clear-text connection.</td></tr>
                                <tr><td> *Require* </td><td>Request an SSL connection, and do not connect if unavailable.</td></tr>
                                <tr>
                                    <td> *Require Exclusively* </td>
                                    <td>
                                        Request an SSL connection. Do not connect if unavailable, nor if the server offers any
                                        clear-text connections to other clients (e.g., server level "Best Available").
                                    </td>
                                </tr>
<table align="center" border="1">

                                    <tr><td colspan="2" rowspan="2" align="center"> **Established <br /> Connection** </td><td colspan="3" bgcolor="66CBEE" align="center"> ***Server Configuration*** </td></tr>
                                    <tr><td bgcolor="BCD3EF">Unavailable</td><td bgcolor="BCD3EF">Best Available</td><td bgcolor="BCD3EF">SSL Only</td></tr>
                                    <tr><td rowspan="4" bgcolor="orange" align="center">Client<br /> Config.</td><td bgcolor="EFDCBC">Clear</td><td font="color:orange">Clear</td><td font="color:orange">Clear</td><td style="color:red">Denied</td></tr>
                                    <tr><td bgcolor="EFDCBC">Request</td><td font="color:orange">Clear</td><td>Secure</td><td>Secure</td></tr>
                                    <tr><td bgcolor="EFDCBC">Require</td><td style="color:red">Denied</td><td>Secure</td><td>Secure</td></tr>
                                    <tr><td bgcolor="EFDCBC">Req. Exc.</td><td style="color:red">Denied</td><td style="color:red">Denied</td><td>Secure</td></tr>
<table>

### Example 1: Server Level = Unavailable, Client Level = Request
In this case, the client's level of "Request" will be honored by the server, because this level allows either SSL or non-SSL connections. 

### Example 2: Server Level = SSL Required, Client Level = Clear
In this case, the server cannot allow the client to connect using a clear-text connection, because the server is required to offer only SSL connections. 

### Example 3: Server Level = Best Available, Client Level = Require Exclusively
In this case, the connection is not allowed, since the "Require Exclusively" level stipulates that the client may not connect to a server that offers any clear-text connections, even though "Best Available" indicates that it offers both SSL and non-SSL connections. 

## DataGate Server Certificate Authentication
To accommodate server authentication, DataGate client can be further configured to test the server's certificate for certain criteria, as shown below. Note that desktop apps additionally may be configured to prompt the user to override problems that DataGate discovers with the server's certificate. 
<table align="center" border="1">

                                            <tr><td bgcolor="66CBEE" align="center"> ***Certificate Authentication Option*** </td><td></td></tr>
                                            <tr>
                                                <td> *Subject Name Match* </td>
                                                <td>
                                                    The server certificate's subject name must be as specified by the configuration. The subject
                                                    name is the X509 "Common Name", e.g., CN=MyServerCertName.
                                                </td>
                                            </tr>
                                            <tr>
                                                <td> *DNS Host Subject Name* </td>
                                                <td>
                                                    The server certificate subject name must match the Domain Name Server's fully-qualified host name for the
                                                    server. For example, "myserver.asna.com".
                                                </td>
                                            </tr>
                                            <tr>
                                                <td> *Certificate Installed* </td>
                                                <td>
                                                    A copy of the server certificate must exist in the user's local certificate store. A system administrator
                                                    would typically import a copy of the server's certificate not containing the private key, into the client machine's certificate store before
                                                    connections can be established using this option.
                                                </td>
                                            </tr>
                                            <tr>
                                                <td> *CA Signed* </td>
                                                <td>
                                                    The server certificate must be traceable by a chain of signed certificates to a trusted certificate authority certificate,
                                                    which must reside in the client machine's certificate store. Typically, the signing certificate authority will be one of the well-known
                                                    certificate authorities, or, say, an enterprise-wide authority.
                                                </td>
                                            </tr>
<table>

With the exception of Subject Name Match and DNS Host Subject Name, the above options are not mutually exclusive, and can thus be combined to suit the security needs of the application. 

DataGate provides tools to help configure and administer these options. Please see <a href="DataGate SSL Deployment.html).
</table>
</table>
</table>
</table>
</table>
</table>

