---
title: Neuigkeiten in UE-V 2.1 SP1
description: Neuigkeiten in UE-V 2.1 SP1
author: dansimp
ms.assetid: 9a40c737-ad9a-4ec1-b42b-31bfabe0f170
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1f4b6210d95795c352a7ef1402b0353c6f52774b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812349"
---
# Neuigkeiten in UE-V 2.1 SP1


Die Benutzeroberflächen-Virtualisierung 2,1 SP1 bietet diese neuen Features und Funktionen im Vergleich zu UE-V 2,1. In den Versionshinweisen für [Microsoft User Experience Virtualization (UE-v) 2,1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) finden Sie weitere Informationen zur Version UE-v 2,1 SP1.

## Unterstützung für Windows 10


UE-v 2,1 SP1 bietet zusätzlich zur gleichen Software, die in früheren Versionen von UE-v unterstützt wird, Unterstützung für Windows 10.

### Kompatibilität mit Microsoft Azure

Windows 10 ermöglicht es Unternehmensbenutzern, Windows-App-Einstellungen und Windows-Betriebssystemeinstellungen zu Azure anstatt zu OneDrive zu synchronisieren. Sie können die Windows 10 Enterprise-Synchronisierungs Funktionalität zusammen mit UE-V für lokale Domänen verbundene Computer verwenden. Um die Koexistenz zwischen Windows 10 und UE-v zu aktivieren, müssen Sie die folgenden UE-v-Vorlagen mithilfe von PowerShell auf jedem Client oder in einer Gruppenrichtlinie deaktivieren.

Konfigurieren Sie in Gruppenrichtlinien unter dem Knoten Microsoft User Experience Virtualization die folgenden Richtlinieneinstellungen:

-   Aktivieren von "Windows-apps nicht synchronisieren"

-   Deaktivieren von "Windows-Synchronisierungseinstellungen"

### Einstellungen-Synchronisierungsverhalten für Windows 10-Unterstützung geändert

UE-V 2,1 SP1 durchstreift die Taskleisteneinstellungen zwischen Windows 10-Geräten. UE-V synchronisiert jedoch keine Taskleisteneinstellungen zwischen Windows 10-Geräten und Geräten, auf denen frühere Betriebssysteme ausgeführt werden.

Darüber hinaus synchronisiert UE-V 2,1 SP1 keine Einstellungen zwischen dem Microsoft-Rechner in Windows 10 und dem Microsoft-Rechner in früheren Betriebssystemen.

## Support für Roaming-Netzwerkdrucker hinzugefügt


Mit UE-V 2,1 SP1 können Netzwerkdrucker zwischen Geräten Roaming durchlaufen, damit ein Benutzer auf seine Netzwerkdrucker zugreifen kann, wenn er sich bei einem beliebigen Gerät im Netzwerk anmeldet. Dies umfasst das Roaming des Druckers, den Sie als Standard festlegen.

Für das Drucker-Roaming in UE-V ist eines der folgenden Szenarien erforderlich:

-   Der Druckserver kann den erforderlichen Treiber herunterladen, wenn er auf ein neues Gerät wechselt.

-   Der Treiber für den Roaming-Netzwerkdrucker ist auf allen Geräten vorinstalliert, die auf diesen Netzwerkdrucker zugreifen müssen.

-   Der Druckertreiber kann über Windows Update abgerufen werden.

**Hinweis**  Das UE-V Printer-Roaming-Feature unterstützt **keine** Druckereinstellungen oder-Einstellungen, beispielsweise das doppelseitige Drucken.

 

## Office 2013-Einstellungen, Speicherort Vorlage


UE-V 2,1 und 2,1 SP1 beinhalten die Vorlage Microsoft Office 2013 Settings Location mit verbesserter Unterstützung für Outlook-Signaturen. Wir haben die Synchronisierung von standardmäßigen Signatureinstellungen für neue, Antworten und weitergeleitete e-Mails hinzugefügt. Kunden müssen die standardmäßigen Signatureinstellungen nicht mehr auswählen.

**Hinweis**  Für jedes Gerät, auf dem ein Benutzer seine Outlook-Signatur synchronisieren möchte, muss ein Outlook-Profil erstellt werden. Wenn das Profil noch nicht erstellt wurde, kann der Benutzer eine erstellen und dann Outlook auf diesem Gerät neu starten, um die Signatur Synchronisierung zu aktivieren.

 

Zuvor enthielt UE-v die Microsoft Office 2010-Einstellungen für Standort Vorlagen, die automatisch verteilt und beim UE-v-Agent registriert wurden. UE-V 2,1 arbeitet mit Office 365, um festzustellen, ob die Office 2013-Einstellungen von Office 365 durchlaufen werden. Wenn die Einstellungen von Office 365 durchlaufen werden, werden Sie nicht von UE-V durchsucht. Eine Übersicht über die [Einstellungen für Benutzer und Roaming für Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) bietet weitere Informationen.

Führen Sie eine der folgenden Aktionen aus, um die Synchronisierung von Einstellungen mithilfe von UE-V 2,1 zu aktivieren:

-   Verwenden von Gruppenrichtlinien zum Deaktivieren der Office 365-Synchronisierung

-   Aktivieren der Office 365-Synchronisierungs Erfahrung während der Installation von Office 2013

UE-V 2,1 liefert [Office 2013-und Office 2010-Vorlagen](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings). Diese Version entfernt die Office 2007-Vorlagen. Benutzer können weiterhin Office 2007-Vorlagen aus UE-v 2,0 oder früheren Versionen verwenden und können weiterhin die Vorlagen aus dem [hier](https://go.microsoft.com/fwlink/p/?LinkID=246589)befindlichen UE-v-Vorlagenkatalog abrufen.






## Verwandte Themen


[Erste Schritte mit UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

[Vorbereiten einer UE-V 2. x-Bereitstellung](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

 

 





