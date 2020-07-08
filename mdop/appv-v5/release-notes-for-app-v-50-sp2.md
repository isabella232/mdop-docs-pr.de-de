---
title: Versionshinweise für App-V 5.0 SP2
description: Versionshinweise für App-V 5.0 SP2
author: dansimp
ms.assetid: fe73139d-240c-4ed5-8e59-6ae76ee8e80c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5e885e67023d0e5c1e36aeb340933c64ae92610e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804895"
---
# Versionshinweise für App-V 5.0 SP2


**Drücken Sie STRG + F, um nach einem bestimmten Problem in diesen Versionshinweisen zu suchen.**

Lesen Sie diese Versionshinweise gründlich, bevor Sie App-V 5,0 SP2 installieren.

Diese Anmerkungen zu dieser Version enthalten Informationen, die zur erfolgreichen Installation von App-V 5,0 SP2 erforderlich sind. Die Anmerkungen zu dieser Version enthalten auch Informationen, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es Unterschiede zwischen diesen Anmerkungen zu dieser Version und einer anderen App-V 5,0-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## Informationen zur Produktdokumentation


Informationen zur APP-v 5,0-Dokumentation finden Sie auf der APP-v 5,0-Startseite auf der Microsoft TechNet-Website.

## Feedback geben


Wir sind an Ihrem Feedback zu App-V 5,0 interessiert. Sie können Ihr Feedback an senden <mdopdocs@microsoft.com> .

**Hinweis**  Diese e-Mail-Adresse ist kein Supportkanal, aber Ihr Feedback wird uns helfen, zukünftige Änderungen in unseren Dokumentations-und Produktversionen zu planen.

 

Die neuesten Informationen zu MDOP und weiteren Lernressourcen finden Sie auf der Seite [MDOP-Informationen](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Wenn Sie weitere Informationen zu neuen Updates oder Feedback geben möchten, folgen Sie uns auf [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) oder [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Bekannte Probleme mit dem Hotfix-Paket 4 für Application Virtualization 5,0 SP2


### Pakete funktionieren nach dem Deinstallieren des Hotfix-Pakets 4 für Application Virtualization 5,0 SP2 nicht mehr

Pakete, die veröffentlicht werden, wenn Hotfix-Paket 4 für Application Virtualization 5,0 SP2 angewendet wird, funktionieren nicht mehr, wenn das Hotfix-Paket 4 für Application Virtualization 5,0 SP2 entfernt wird.

WORKAROUND

Wenn der folgende Ordner vorhanden ist, müssen Sie ihn löschen:

**% LocalAppData%**  \\  **Microsoft Office**  \\  **AppV**  \\  **Client**  \\  **VFS**  \\  die ** &lt; Paket &gt; -ID** für jedes veröffentlichte Paket.

**Hinweis**  Sie müssen über erhöhte Berechtigungen verfügen, um diesen Ordner zu löschen.

 

So verwenden Sie ein Skript für jedes Benutzerkonto auf dem Computer und für jede Paket-ID, die nach der Installation des Hotfix-Pakets 4 für Application Virtualization 5,0 SP2 veröffentlicht wurde:

`Rd /s /q “%systemdrive%\users\[UserName]\AppData\Local\Microsoft\AppV\Client\VFS\[Package ID]`

-   Die Tastenkombinationen bleiben auch nach dem Löschen des Ordners aus dem Verzeichnis im vorherigen Abschnitt in den Benutzersitzungen erhalten, sodass Sie auf die Verknüpfung klicken können, um die Anwendung erneut auszuführen. Die Anwendung muss nicht erneut veröffentlicht werden.

-   Dieses Problem tritt für veröffentlichte, von Benutzern veröffentlichte, verpackte und Global veröffentlichte Pakete auf, beispielsweise Microsoft Office2013. Der Ordner muss für beide Arten von Paketen gelöscht werden.

-   Sie müssen den VFS-Ordner in den Roaming-App-Daten (**% AppData%**) nicht löschen. Nur die **% LocalAppData%** müssen gelöscht werden.

### Microsoft Office-Integration verweist auf falschen Speicherort für das Dateisystem

Microsoft Office-Integration verweist auf den falschen Speicherort des Dateisystems (Groove.exe-Fehlermeldung).

WORKAROUND

Verwenden Sie eine der folgenden Methoden:

1.  Löschen Sie die Verknüpfung im Startordner nach dem Upgrade.

2.  Ändern Sie die Verknüpfung im Startordner mithilfe eines Skripts.

3.  Verwenden Sie die Konfigurationsdatei für die Bereitstellung, um das Verknüpfungsziel für den Integrations Stamm festzulegen.

### <a href="" id="-------------hotfix-package-4-for-application-virtualization-5-0-sp2-installer-can-take-a-long-time"></a> Hotfix-Paket 4 für Application Virtualization 5,0 SP2-Installationsprogramm kann sehr lange dauern

Das Hotfix-Paket 4 für das Application Virtualization 5,0 SP2-Installationsprogramm kann möglicherweise sehr lange dauern, je nachdem, wie viele Dateien im vorhandenen Paketcache gespeichert sind.

Das Aktualisieren der zugehörigen Paket Sicherheitsbeschreibungen während des Hotfix-Pakets 4 für die Installation von Application Virtualization 5,0 SP2 hat erhebliche Auswirkungen darauf, wie lange die Installation dauern wird. Zuvor war die Installations Installation standardmäßig in Dauer. Es hängt nun jedoch davon ab, wie viele Dateien im Paketcache bereitgestellt wurden.

Problemumgehung: keine

### Deinstallieren des Hotfix-Pakets 4 für Application Virtualization 5,0 SP2 schlägt fehl, wenn das JIT-V-Paket verwendet wird

Wenn Sie das Hotfix-Paket 4 für Application Virtualization 5,0 SP2 installieren und dann versuchen, den Hotfix zu deinstallieren, wenn Just-in-Time-Virtualisierung (JIT-V) verwendet wird, schlägt der Vorgang fehl, wenn alle der folgenden Bedingungen erfüllt sind:

-   Sie haben mithilfe einer Windows Installer-Datei (MSI) installiert, und Sie können Updates dann mithilfe einer Microsoft Installer-Patchdatei (MSP) anwenden.

-   Sie versuchen, ein Update mithilfe des Elements "Software" in der Systemsteuerung zu deinstallieren.

-   Auf dem Computer wird ein JIT-V-fähiges Paket ausgeführt.

Problemumgehung: führen Sie die folgenden Schritte aus:

1.  Öffnen Sie Windows PowerShell, und führen Sie die folgenden Befehle aus:

    -   **Import-Modul appvclient**

    -   **Get-AppvClientPackage | Stopp-AppvClientPackage**

2.  Deinstallieren Sie das Update mithilfe von Software.

## Bekannte Probleme mit App-V 5,0 SP2


### <a href="" id="bkmk-folderredirection"></a>App-V-Clientordner Umleitung schlägt manchmal fehl, um Dateien von% APPDATA% auf% LocalAppData% zu verschieben.

Wenn% APPDATA% ein freigegebener Netzwerkordner ist, den Sie für die Ordnerumleitung konfiguriert haben, können die Änderungen, die Endbenutzer an APPDATA (Roaming) vornehmen, verloren gehen, wenn Sie den Computer wechseln oder wenn die lokale APPDATA gelöscht wird, wenn Sie sich abmelden und dann wieder anmelden. Dieser Fehler tritt auf, weil der Registrierungsschlüssel (AppDataTime), der den letzten bekannten Upload angibt, nicht mehr mit dem lokalen zwischengespeicherten APPDATA synchronisiert wird.

Problemumgehung: Löschen Sie den folgenden Registrierungsschlüssel für jedes relevante Paket manuell, wenn sich ein Endbenutzer anmeldet oder deaktiviert:

``` syntax
HKCU\Software\Microsoft\AppV\Client\Packages\<PACKAGE_GUID>\AppDataTime
```

Wenn Endbenutzer zum ersten Mal eine Anwendung im Paket starten, nachdem Sie sich angemeldet haben, erzwingt App-V einen Download des gezippten% APPDATA%, auch wenn% LocalAppData% bereits auf dem neuesten Stand ist.

### <a href="" id="-------------app-v-5-0-service-pack-2--app-v-5-0-sp2--does-not-include-a-new-version-of-the-app-v-server"></a> App-v 5,0 Service Pack 2 (app-v 5,0 SP2) enthält keine neue Version des App-v-Servers

App-v 5.0 SP2 enthält keine neue Version des App-v-Servers. Wenn Sie App-v 5,0 SP2-Clients mit Windows 8,1 in Ihrer Umgebung bereitstellen und planen, die Clients mithilfe der APP-v-Infrastruktur zu verwalten, müssen Sie das [Hotfix-Paket 2 für Microsoft Application Virtualization 5,0 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=386634)installieren. (https://go.microsoft.com/fwlink/?LinkId=386634)

Wenn Sie App-V 5,0 SP2-Clients mit einer der folgenden Methoden ausführen und verwalten, ist kein Client Update erforderlich:

-   Eigenständiger Modus.

-   Konfigurations-Manager.

-   ESD von Drittanbietern.

Der App-V 5,0 SP2-Client ist vollständig mit Windows 8,1 kompatibel

Problemumgehung: keine.

## Anmerkungen zu dieser Version Copyright-Informationen


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune und WindowsPowerShell sind Marken der Microsoft-Unternehmensgruppe. Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.








## Verwandte Themen


[Informationen zu App-V 5.0 SP2](about-app-v-50-sp2.md)

 

 





