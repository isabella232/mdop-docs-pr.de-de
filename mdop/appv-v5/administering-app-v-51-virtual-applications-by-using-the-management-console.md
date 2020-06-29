---
title: Verwalten von mit App-V 5.1 virtualisierten Anwendungen mithilfe der Verwaltungskonsole
description: Verwalten von mit App-V 5.1 virtualisierten Anwendungen mithilfe der Verwaltungskonsole
author: dansimp
ms.assetid: a4d078aa-ec54-4fa4-9463-bfb3b971d724
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63ec965519bedef08b09c961dc5d1c90e1d8d694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806047"
---
# Verwalten von mit App-V 5.1 virtualisierten Anwendungen mithilfe der Verwaltungskonsole


Verwenden Sie den Microsoft Application Virtualization (App-V) 5,1-Verwaltungsserver, um Pakete, Verbindungsgruppen und den Paketzugriff in Ihrer Umgebung zu verwalten. Der Server veröffentlicht Anwendungssymbole, Verknüpfungen und Dateitypzuordnungen auf autorisierten Computern, auf denen der App-V 5,1-Client ausgeführt wird. Mindestens ein Verwaltungsserver gibt in der Regel einen gemeinsamen Datenspeicher für Konfigurations-und Paketinformationen frei.

Der Verwaltungsserver verwendet Active Directory-Domänendienste (AD DS)-Gruppen, um die Benutzerautorisierung zu verwalten und SQL Server zum Verwalten der Datenbank und des Datenspeichers zu installieren.

Da die Verwaltungsserver Anwendungen bei Bedarf an Endbenutzer streamen, eignen sich diese Server ideal für Systemkonfigurationen mit zuverlässigen LANs mit hoher Bandbreite. Der Verwaltungsserver besteht aus den folgenden Komponenten:

-   Verwaltungsserver – verwenden Sie den Verwaltungsserver, um Pakete und Verbindungsgruppen zu verwalten.

-   Publishing Server – verwenden Sie den Veröffentlichungsserver zum Bereitstellen von Paketen auf Computern, auf denen der App-V 5,1-Client ausgeführt wird.

-   Verwaltungsdatenbank – verwenden Sie die Verwaltungsdatenbank, um den Paketzugriff zu verwalten und die Synchronisierung des Servers mit dem Verwaltungsserver zu veröffentlichen.

## Verwaltungskonsolen Aufgaben


Die häufigsten Aufgaben, die Sie mit der App-V 5,1-Verwaltungskonsole ausführen können, sind:

-   [So stellen Sie eine Verbindung mit der Verwaltungskonsole her](how-to-connect-to-the-management-console-51.md)

-   [So fügen Sie mithilfe der Verwaltungskonsole Pakete hinzu oder aktualisieren sie](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)

-   [So konfigurieren Sie mithilfe der Verwaltungskonsole den Zugriff auf Pakete](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

-   [So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket](how-to-publish-a-package-by-using-the-management-console-51.md)

-   [So löschen Sie ein Paket in der Verwaltungskonsole](how-to-delete-a-package-in-the-management-console-51.md)

-   [So fügen Sie mithilfe der Verwaltungskonsole einen Administrator hinzu oder entfernen einen Administrator](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)

-   [So registrieren Sie mithilfe der Verwaltungskonsole einen Veröffentlichungsserver oder heben die Registrierung eines Veröffentlichungsservers auf](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console51.md)

-   [So erstellen Sie mithilfe der App-V 5.1-Verwaltungskonsole eine benutzerdefinierte Konfigurationsdatei an](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md)

-   [So übertragen Sie mithilfe der Verwaltungskonsole Zugriff und Konfigurationen auf eine andere Version eines Pakets](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console51.md)

-   [So passen Sie mithilfe der Verwaltungskonsole virtuelle Anwendungserweiterungen für eine spezifische AD-Gruppe an](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console51.md)

-   [So zeigen Sie mithilfe der Verwaltungskonsole Anwendungen und virtuelle Standardanwendungserweiterungen an und konfigurieren sie](how-to-view-and-configure-applications-and-default-virtual-application-extensions-by-using-the-management-console-beta.md)

Die Hauptelemente der App-V 5,1-Verwaltungskonsole sind:

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
<td align="left"><p>Registerkarte "Pakete"</p></td>
<td align="left"><p>Verwenden <strong> Sie die </strong> Registerkarte Pakete, um Pakete hinzuzufügen oder zu aktualisieren.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registerkarte "Verbindungsgruppen"</p></td>
<td align="left"><p>Verwenden Sie die <strong> </strong> Registerkarte Verbindungsgruppen, um Verbindungsgruppen zu verwalten.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Server (Registerkarte)</p></td>
<td align="left"><p>Verwenden Sie <strong> die </strong> Registerkarte Server, um einen neuen Server zu registrieren.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registerkarte "Administratoren"</p></td>
<td align="left"><p>Verwenden Sie <strong> die </strong> Registerkarte Administratoren, um Administratoren in ihrer App-V 5,1-Umgebung zu registrieren, hinzuzufügen oder zu entfernen.</p></td>
</tr>
</tbody>
</table>

 

**Wichtig**  JavaScript muss im Browser aktiviert sein, über den die Webverwaltungs Konsole geöffnet wird.

 






## <a href="" id="other-resources-for-this-app-v-5-1-deployment-"></a>Weitere Ressourcen für diese App-V 5,1-Bereitstellung


-   [Microsoft Application Virtualization 5,1-Administrator Handbuch](microsoft-application-virtualization-51-administrators-guide.md)

-   [Vorgänge für App-V 5.1](operations-for-app-v-51.md)

 

 





