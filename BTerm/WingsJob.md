---
title: BTermJob

Id: WingsJob
TocParent: emComponents
TocOrder: 70

keywords: ASNA Browser Terminal
keywords: ASNA Browser Terminal, WIngsJob
keywords: WingsJob
keywords: MobileRPG

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

# BTermJob
When an ASNA Browser Terminal website is created, a BTermJob application is created under the application code folder (App_code). The BTermJob will have an extension of .cs (for C#), .vb (for Visual Basic), or .vr (for ASNA Visual RPG) depending on the language selected when the website was created. 

The basic functions of BTermJob are:

1. Provides connection to the database using the
                        server, user, password, and port; all from the user input
                        entered during [Sign On](SignonScreen.html).
2. Calls the program or the menu using the
                        database and library; all from the user input entered during
                        [Sign On](SignonScreen.html). See **callProgram** , **callQCmdExec** , and
 **goMenu** .

