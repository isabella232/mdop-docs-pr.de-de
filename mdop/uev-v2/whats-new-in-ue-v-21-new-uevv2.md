---
title: Neuigkeiten in UE-V 2.1
description: Neuigkeiten in UE-V 2.1
author: dansimp
ms.assetid: 7f385183-7d97-4602-b19a-baa710334ade
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7816fc8309a29347048172b2104750140c483587
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811650"
---
# Neuigkeiten in UE-V 2.1


Die User Experience Virtualization 2,1 stellt diese neuen Features und Funktionen im Vergleich zu UE-V 2,0 zur Verfügung. Die [Microsoft User Experience Virtualization (UE-v) 2,1-Versionshinweise](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) bieten weitere Informationen zur Version UE-v 2,1.

## Office 2013-Einstellungen, Speicherort Vorlage


UE-V 2,1 enthält die Vorlage für Microsoft Office 2013-Einstellungen mit verbesserter Unterstützung für Outlook-Signaturen. In UE-V 2,1 werden die Signaturdaten zwischen Benutzergeräten synchronisiert. Wir haben die Synchronisierung von standardmäßigen Signatureinstellungen für neue, Antworten und weitergeleitete e-Mails hinzugefügt. Kunden müssen die standardmäßigen Signatureinstellungen nicht mehr auswählen.

**Hinweis**  Für jedes Gerät, auf dem ein Benutzer seine Outlook-Signatur synchronisieren möchte, muss ein Outlook-Profil erstellt werden. Wenn das Profil noch nicht erstellt wurde, kann der Benutzer eine erstellen und dann Outlook auf diesem Gerät neu starten, um die Signatur Synchronisierung zu aktivieren.

 

Zuvor enthielt UE-v die Microsoft Office 2010-Einstellungen für Standort Vorlagen, die automatisch verteilt und beim UE-v-Agent registriert wurden. UE-V 2,1 arbeitet mit Office 365, um festzustellen, ob die Office 2013-Einstellungen von Office 365 durchlaufen werden. Wenn die Einstellungen von Office 365 durchlaufen werden, werden Sie nicht von UE-V durchsucht. Eine Übersicht über die [Einstellungen für Benutzer und Roaming für Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) bietet weitere Informationen.

Führen Sie eine der folgenden Aktionen aus, um die Synchronisierung von Einstellungen mithilfe von UE-V 2,1 zu aktivieren:

-   Verwenden von Gruppenrichtlinien zum Deaktivieren der Office 365-Synchronisierung

-   Aktivieren der Office 365-Synchronisierungs Erfahrung während der Installation von Office 2013

UE-V 2,1 liefert [Office 2013-und Office 2010-Vorlagen](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings). Diese Version entfernt die Office 2007-Vorlagen. Benutzer können weiterhin Office 2007-Vorlagen aus UE-v 2,0 oder früheren Versionen verwenden und können weiterhin die Vorlagen aus dem [hier](https://go.microsoft.com/fwlink/p/?LinkID=246589)befindlichen UE-v-Vorlagenkatalog abrufen.

## Fix für Benutzer von verteilten Datei System-Namespaces


UE-v hat eine verbesserte Unterstützung für Distributed File System Namespace (DFSN) durch Hinzufügen einer UE-v-Konfiguration mit dem Namen SyncProviderPingEnabled. Durch das Deaktivieren dieser Konfiguration mithilfe von PowerShell oder WMI können Benutzer den UE-V-Ping deaktivieren. Der UE-V-Ping verursacht einen Fehler bei der Verwendung von DFSN-Servern, da diese Server nicht auf Pings reagieren. Die nicht Antwort verhindert, dass UE-V die Einstellungen synchronisiert. Durch Deaktivieren des UE-v-Pings kann die UE-v-Synchronisierung normal funktionieren.

Verwenden Sie dieses PowerShell-Cmdlet, um UE-V-Ping zu deaktivieren:

``` syntax
Set-UevConfiguration -DisableSyncProviderPing
```

## Synchronisierung für Anmeldeinformationen


UE-V 2,1 bietet Kunden die Möglichkeit, die im Windows-Anmelde Informations-Manager gespeicherten Anmeldeinformationen und Zertifikate zu synchronisieren. Diese Komponente ist standardmäßig deaktiviert. Wenn Sie diese Komponente aktivieren, können Benutzer ihre Domänenanmeldeinformationen und Zertifikate synchron halten. Benutzer können sich einmal auf einem Gerät anmelden, und diese Anmeldeinformationen werden für diesen Benutzer auf allen ihren UE-V-fähigen Geräten gespeichert. [Zum Verwalten von Anmeldeinformationen mit UE-V 2,1](https://technet.microsoft.com/library/dn458932.aspx#creds) finden Sie weitere Informationen.

**Hinweis**  In Windows 8 und höher enthält der Anmelde Informations-Manager webanmelde Informationen. Diese Anmeldeinformationen werden nicht zwischen den Geräten der Benutzer synchronisiert.

 

## UE-V und Microsoft-Konto Synchronisierung


UE-V erkennt, ob "Synchronisierungseinstellungen mit OneDrive", auch bekannt als Microsoft-Konto Synchronisierung, aktiviert ist. Wenn das Microsoft-Konto nicht für die Synchronisierung von Einstellungen konfiguriert ist, synchronisiert UE-V Windows-apps, AppX-Pakete und Windows-Desktopeinstellungen zwischen Geräten. Auf diese Weise können Benutzer auf Ihre Store-Apps, Musik, Bilder und andere Microsoft-Konto fähige Anwendungen zugreifen, ohne die Synchronisierung außerhalb der Unternehmensfirewall zu synchronisieren. UE-V überprüft, ob Gruppenrichtlinien die Synchronisierung von Einstellungen mit OneDrive beenden oder ob der Benutzer die **Synchronisierung Ihrer Einstellungen auf diesem Computer** in den Benutzersteuerelementen deaktiviert.

## Unterstützung für das SyncMethod extern


Eine neue [SyncMethod-Konfiguration](https://technet.microsoft.com/library/dn554321.aspx) mit dem Namen **External** gibt an, dass wenn UE-V-Einstellungen in einen lokalen Ordner auf dem Benutzer Computer geschrieben werden, dann ein externes Synchronisierungsmodul (wie OneDrive for Business, Arbeitsordner, SharePoint oder Dropbox) verwendet werden kann, um diese Einstellungen auf die verschiedenen Computer anzuwenden, auf die Benutzer zugreifen.

## Verbesserte Unterstützung für den VDI-Modus


UE-V 2,1 umfasst [Unterstützung für VDI-Sitzungen](https://technet.microsoft.com/library/dn458932.aspx#vdi) , die von Endbenutzern freigegeben werden. Als Administrator können Sie eine spezielle VDI-Vorlage registrieren und konfigurieren, die sicherstellt, dass UE-V alle Funktionen für nicht persistente VDI-Sitzungen intakt hält.

**Hinweis**  Wenn Sie den VDI-Modus nicht für nicht persistente VDI-Sitzungen aktivieren, funktionieren bestimmte Features nicht, beispielsweise die Datensicherung/-Wiederherstellung und LKG.

 

## Administrative Sicherung und Wiederherstellung


Sie können zusätzliche Einstellungen wiederherstellen, wenn ein Benutzer ein neues Gerät annimmt, indem Sie eine Vorlage für die Einstellungsposition im **Backup** -oder Roam-Profil **(Standard)** mithilfe des PowerShell-Cmdlets "UevTemplateProfile" festlegen. Auf diese Weise können Computereinstellungen zusätzlich zu den Benutzereinstellungen mit dem neuen Computer synchronisiert werden. Vorlagen, die dem Sicherungsprofil zugewiesen sind, werden für dieses Gerät gesichert und auf Gerätebasis konfiguriert. Das [Verwalten von Verwaltungs-Backup und-Wiederherstellung in UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) enthält weitere Informationen.

## Synchronisierung für zusätzliche Windows-Einstellungen


UE-V synchronisiert nun die Personalisierung von Touchscreen-Tastaturen, das Rechtschreibwörterbuch und ermöglicht die APP-Umschaltung für aktuelle apps und Einstellungen für den Bildschirmrand, um zwischen Windows 8-und Windows 8,1-Geräten zu synchronisieren.






## Verwandte Themen


[Erste Schritte mit UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

[Vorbereiten einer UE-V 2. x-Bereitstellung](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

 

 





