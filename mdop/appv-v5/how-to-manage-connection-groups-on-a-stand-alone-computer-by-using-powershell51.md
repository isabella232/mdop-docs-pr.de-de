---
title: So verwalten Sie Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell
description: So verwalten Sie Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell
author: dansimp
ms.assetid: e1589eff-d306-40fb-a0ae-727190dafe26
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ab120f7089619fa01885d5182313dc33fc47f827
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805315"
---
# So verwalten Sie Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell


Mit einer App-V-Verbindungsgruppe können Sie alle virtuellen Anwendungen als definierten Satz von Paketen in einer einzelnen virtuellen Umgebung ausführen. So können Sie beispielsweise eine Anwendung und ihre Plug-Ins mithilfe separater Pakete virtualisieren, Sie aber in einer einzelnen Verbindungsgruppe zusammenführen.

Eine Verbindungsgruppen-XML-Datei definiert die Verbindungsgruppe, die auf dem Computer ausgeführt wird, auf dem Sie den App-V-Client installiert haben. Informationen zur XML-Verbindungsgruppen-Datei und deren Konfiguration finden Sie unter Informationen zur [Verbindungsgruppen Datei](about-the-connection-group-file51.md).

In diesem Thema werden die folgenden Verfahren erläutert:

-   [So fügen Sie die App-V-Pakete in der Verbindungsgruppe hinzu und veröffentlichen Sie](#bkmk-add-pub-pkgs-in-cg)

-   [So fügen Sie die Verbindungsgruppe auf dem App-V-Client hinzu und aktivieren Sie](#bkmk-add-enable-cg-on-clt)

-   [So aktivieren oder deaktivieren Sie eine Verbindungsgruppe für einen bestimmten Benutzer](#bkmk-enable-cg-for-user-poshtopic)

-   [So ermöglichen Sie es nur Administratoren, Verbindungsgruppen zu aktivieren](#bkmk-admin-only-posh-topic-cg)

<a href="" id="bkmk-add-pub-pkgs-in-cg"></a>*So fügen Sie die App-V-Pakete in der Verbindungsgruppe hinzu und veröffentlichen Sie**

1.  Zum Hinzufügen und Veröffentlichen der APP-v 5,1-Pakete auf dem Computer, auf dem der APP-v-Client ausgeführt wird, geben Sie den folgenden Befehl ein:

    Add-AppvClientPackage – Pfad-c:\\tmpstore\\quartfin.AppV | Publish-AppvClientPackage

2.  Wiederholen Sie **Schritt 1** dieses Verfahrens für jedes Paket in der Verbindungsgruppe.

<a href="" id="bkmk-add-enable-cg-on-clt"></a>**So fügen Sie die Verbindungsgruppe auf dem App-V-Client hinzu und aktivieren Sie**

1.  Fügen Sie die Verbindungsgruppe hinzu, indem Sie den folgenden Befehl eingeben:

    Add-AppvClientConnectionGroup – Pfad c:\\tmpstore\\financ.xml

2.  Aktivieren Sie die Verbindungsgruppe, indem Sie den folgenden Befehl eingeben:

    Enable-AppvClientConnectionGroup – Name "Financial Applications"

    Wenn alle virtuellen Anwendungen, die sich in den Mitglieds Paketen befinden, auf dem Zielcomputer ausgeführt werden, werden Sie innerhalb der virtuellen Umgebung der Verbindungsgruppe ausgeführt und stehen für alle virtuellen Anwendungen in den anderen Paketen in der Verbindungsgruppe zur Verfügung.

<a href="" id="bkmk-enable-cg-for-user-poshtopic"></a>**So aktivieren oder deaktivieren Sie eine Verbindungsgruppe für einen bestimmten Benutzer**

1.  Überprüfen Sie die Parameter Beschreibung und die Anforderungen:

    -   Mithilfe des Parameters kann ein Administrator eine Verbindungsgruppe für einen bestimmten Benutzer aktivieren oder deaktivieren.

    -   Sie müssen App-V 5,0 SP2-Hotfix-Paket 5 oder höher verwenden, um diesen Parameter zu verwenden.

    -   Sie können dieses Cmdlet in der Benutzer-oder Administrator Sitzung ausführen.

    -   Sie müssen mit administrativen Anmeldeinformationen angemeldet sein, um den Parameter verwenden zu können.

    -   Der Endbenutzer muss angemeldet sein.

    -   Sie müssen die Sicherheits-ID (Security Identifier, SID) des Endbenutzers angeben.

2.  Verwenden Sie die folgenden Cmdlets, und fügen Sie den optionalen **– Users** -Parameter hinzu, wobei **-Benutzer-** ID die Sicherheits-ID (SID) des Endbenutzers darstellt:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Cmdlet</th>
    <th align="left">Beispiele</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Enable-AppVClientConnectionGroup</p></td>
    <td align="left"><p>Enable-AppVClientConnectionGroup "ConnectionGroupA"-Benutzer-e-1-2-34-56789012-3456789012-345678901-2345</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Deaktivieren-AppVClientConnectionGroup</p></td>
    <td align="left"><p>Disable-AppVClientConnectionGroup "ConnectionGroupA"-Benutzer-e-1-2-34-56789012-3456789012-345678901-2345</p></td>
    </tr>
    </tbody>
    </table>

<a href="" id="bkmk-admin-only-posh-topic-cg"></a>**So ermöglichen Sie es nur Administratoren, Verbindungsgruppen zu aktivieren**

1.  Überprüfen Sie die Beschreibung und die Voraussetzungen für die Verwendung dieses Cmdlets:

    -   Mithilfe dieses Cmdlets und Parameters können Sie den App-V-Client so konfigurieren, dass nur Administratoren (nicht Endbenutzer) Verbindungsgruppen aktivieren oder deaktivieren können.

    -   Sie müssen mindestens App-V 5,0 SP3 verwenden, um dieses Cmdlet verwenden zu können.

2.  Führen Sie das folgende Cmdlet und den folgenden Parameter aus:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Cmdlet</th>
    <th align="left">Parameter und Werte</th>
    <th align="left">Beispiel</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Satz-AppvClientConfiguration</p></td>
    <td align="left"><p>–RequirePublishAsAdmin</p>
    <ul>
    <li><p>0-falsch</p></li>
    <li><p>1-wahr</p></li>
    </ul></td>
    <td align="left"><p>Satz-AppvClientConfiguration – RequirePublishAsAdmin1</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)

[Verwalten von App-V 5.1 mithilfe von PowerShell](administering-app-v-51-by-using-powershell.md)









