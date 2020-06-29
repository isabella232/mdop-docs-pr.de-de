---
title: Verwalten von mit App-V 5.0 virtualisierten Anwendungen mithilfe der Verwaltungskonsole
description: Verwalten von mit App-V 5.0 virtualisierten Anwendungen mithilfe der Verwaltungskonsole
author: dansimp
ms.assetid: e9280dbd-782b-493a-b495-daab25247795
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: 7a71f7c0fd82f8ef9d1efd5b978591b6838a648a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806050"
---
# Verwalten von mit App-V 5.0 virtualisierten Anwendungen mithilfe der Verwaltungskonsole


Verwenden Sie den Microsoft Application Virtualization (App-V) 5,0-Verwaltungsserver, um Pakete, Verbindungsgruppen und den Paketzugriff in Ihrer Umgebung zu verwalten. Der Server veröffentlicht Anwendungssymbole, Verknüpfungen und Dateitypzuordnungen auf autorisierten Computern, auf denen der App-V 5,0-Client ausgeführt wird. Mindestens ein Verwaltungsserver gibt in der Regel einen gemeinsamen Datenspeicher für Konfigurations-und Paketinformationen frei.

Der Verwaltungsserver verwendet Active Directory-Domänendienste (AD DS)-Gruppen, um die Benutzerautorisierung zu verwalten und SQL Server zum Verwalten der Datenbank und des Datenspeichers zu installieren.

Da die Verwaltungsserver Anwendungen bei Bedarf an Endbenutzer streamen, eignen sich diese Server ideal für Systemkonfigurationen mit zuverlässigen LANs mit hoher Bandbreite. Der Verwaltungsserver besteht aus den folgenden Komponenten:

-   Verwaltungsserver – verwenden Sie den Verwaltungsserver, um Pakete und Verbindungsgruppen zu verwalten.

-   Publishing Server – verwenden Sie den Veröffentlichungsserver zum Bereitstellen von Paketen auf Computern, auf denen der App-V 5,0-Client ausgeführt wird.

-   Verwaltungsdatenbank – verwenden Sie die Verwaltungsdatenbank, um den Paketzugriff zu verwalten und die Synchronisierung des Servers mit dem Verwaltungsserver zu veröffentlichen.

## Verwaltungskonsolen Aufgaben


Die häufigsten Aufgaben, die Sie mit der App-V 5,0-Verwaltungskonsole ausführen können, sind:

-   [So stellen Sie eine Verbindung mit der Verwaltungskonsole her](how-to-connect-to-the-management-console-beta.md)

-   [So fügen Sie mithilfe der Verwaltungskonsole Pakete hinzu oder aktualisieren sie](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)

-   [So konfigurieren Sie mithilfe der Verwaltungskonsole den Zugriff auf Pakete](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

-   [So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket](how-to-publish-a-package-by-using-the-management-console-50.md)

-   [So löschen Sie ein Paket in der Verwaltungskonsole](how-to-delete-a-package-in-the-management-console-beta.md)

-   [So fügen Sie mithilfe der Verwaltungskonsole einen Administrator hinzu oder entfernen einen Administrator](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)

-   [So registrieren Sie mithilfe der Verwaltungskonsole einen Veröffentlichungsserver oder heben die Registrierung eines Veröffentlichungsservers auf](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console.md)

-   [So erstellen Sie mithilfe der App-V 5.0-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md)

-   [So übertragen Sie mithilfe der Verwaltungskonsole Zugriff und Konfigurationen auf eine andere Version eines Pakets](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console.md)

-   [So passen Sie mithilfe der Verwaltungskonsole virtuelle Anwendungserweiterungen für eine spezifische AD-Gruppe an](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console.md)

-   [Konfigurieren von Anwendungen und Standard-Erweiterungen für virtuelle Anwendungen in der Verwaltungskonsole](configure-applications-and-default-virtual-application-extensions-in-management-console.md)

Die Hauptelemente der App-V 5,0-Verwaltungskonsole sind:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Registerkarte "Verwaltungskonsole"</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Übersicht</p></td>
<td align="left"><p></p>
<ul>
<li><p><strong>App-v Sequencer </strong> - Wählen Sie diese Option aus, um allgemeine Informationen zur Verwendung des App-v 5,0-Sequenzers zu überprüfen.</p></li>
<li><p><strong>Bibliothek für Anwendungspakete </strong> – Wählen Sie diese Option aus, um die <strong> </strong> Seite Pakete der Verwaltungskonsole zu öffnen. Auf dieser Seite können Sie die Pakete überprüfen, die dem Server hinzugefügt wurden. Sie können auch die Verbindungsgruppen verwalten sowie Pakete hinzufügen oder aktualisieren.</p></li>
<li><p><strong>Server </strong> – Wählen Sie diese Option aus, um die <strong> </strong> Seite Server der Verwaltungskonsole zu öffnen. Auf dieser Seite können Sie die Liste der Server überprüfen, die bei ihrer App-V 5,0-Infrastruktur registriert wurden.</p></li>
<li><p><strong>Clients </strong> – Wählen Sie diese Option aus, um allgemeine Informationen zu App-V 5,0-Clients zu überprüfen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Registerkarte "Pakete"</p></td>
<td align="left"><p>Verwenden <strong> Sie die </strong> Registerkarte Pakete, um Pakete hinzuzufügen oder zu aktualisieren. Sie können Verbindungsgruppen auch verwalten, indem Sie auf <strong> Verbindungsgruppen klicken </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Server (Registerkarte)</p></td>
<td align="left"><p>Verwenden Sie <strong> die </strong> Registerkarte Server, um einen neuen Server zu registrieren.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registerkarte "Administratoren"</p></td>
<td align="left"><p>Verwenden Sie <strong> die </strong> Registerkarte Administratoren, um Administratoren in ihrer App-V 5,0-Umgebung zu registrieren, hinzuzufügen oder zu entfernen.</p></td>
</tr>
</tbody>
</table>

 






## <a href="" id="other-resources-for-this-app-v-5-0-deployment-"></a>Weitere Ressourcen für diese App-V 5,0-Bereitstellung


-   [Microsoft Application Virtualization 5,0-Administrator Handbuch](microsoft-application-virtualization-50-administrators-guide.md)

-   [Vorgänge für App-V 5.0](operations-for-app-v-50.md)

 

 





