---
title: Neuigkeiten in UE-V 2.0
description: Neuigkeiten in UE-V 2.0
author: dansimp
ms.assetid: 5d852beb-f293-4e3a-a33b-c40df59a7515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a7566bd82432dcf7e4c46e1fa3e66e55d1515b79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810870"
---
# Neuigkeiten in UE-V 2.0


Microsoft User Experience Virtualization (UE-v) 2,0 stellt diese neuen Features und Funktionen im Vergleich zu UE-v 1,0 zur Verfügung. Die [Microsoft User Experience Virtualization (UE-v) 2,0-Versionshinweise](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) bieten weitere Informationen zur Version UE-v 2,0.

## Client seitiger Cache (CSC) nicht mehr erforderlich


Diese Version von UE-V führt den **Synchronisierungsanbieter**ein, der die Anforderung für das Windows-Feature "Offline Dateien" ersetzt, um einen clientseitigen Cache von Einstellungen zu unterstützen.

Während UE-V zum Synchronisieren von Einstellungen nur verwendet wird, wenn eine Anwendung geöffnet, geschlossen oder wenn Windows gesperrt oder entriegelt wurde, oder bei der Anmeldung oder Abmeldung der Synchronisierungsanbieter auch...

-   Synchronisiert lokale Anwendungs-und Windows-Einstellungen out-of-Band mit "**Trigger-Ereignisse**"

-   Verwendet eine **geplante Aufgabe** zum Synchronisieren des Einstellungen-Speicher Pakets in einem beliebigen Intervall, das Sie für Ihre Unternehmensanforderungen auswählen (standardmäßig alle 30 Minuten)

Bestimmte Bedingungen bieten eine häufigere Synchronisierung.

-   Einstellungen werden synchronisiert, wenn der Benutzer auf die Schaltfläche " **Jetzt synchronisieren** " in der neuen Unternehmenseinstellungen-Center-Anwendung klickt.

-   Der Synchronisierungsanbieter kann auch für eine einzelne Anwendung gestartet werden, ohne auf den geplanten Synchronisierungstask zu warten. Wenn beispielsweise eine Anwendung geschlossen wird, werden alle Einstellungsänderungen in den lokalen Cache geschrieben, und der Synchronisierungsanbieter Prozess wird asynchron ausgeführt, um diese neuen Einstellungsänderungen in den Speicherort der Einstellungen zu verschieben.

## Windows-App-Synchronisierung


Der Entwickler einer Windows-App kann definieren, welche Einstellungen, falls vorhanden, synchronisiert werden sollen, und diese Einstellungen können nun mit UE-V erfasst und synchronisiert werden.

Standardmäßig synchronisiert UE-V die Einstellungen für viele der Windows-apps, die in Windows 8 und Windows 8,1 enthalten sind. Sie können die Liste synchronisierter apps mit Windows PowerShell, Windows-Verwaltungsinstrumentation (WMI) oder Gruppenrichtlinie ändern.

**Hinweis**  UE-V synchronisiert keine Windows-App-Einstellungen, wenn die Domänenbenutzer Ihre Anmeldeinformationen mit Ihrem Microsoft-Konto verknüpfen. Diese Verknüpfung synchronisiert Einstellungen mit Microsoft OneDrive, damit UE-V nur die Desktopanwendungen synchronisiert.

 

## Verknüpfung des Microsoft-Kontos


Die Synchronisierung von Einstellungen über OneDrive ist neu bei Windows 8, wenn Sie mit einem Microsoft-Konto angemeldet sind oder wenn Sie Ihr Microsoft-Konto mit Ihrem Domänenkonto verknüpfen. Wenn ein Domänenbenutzer UE-V verwendet und sich bei einem Microsoft-Konto angemeldet hat,...

-   UE-V synchronisiert nur Einstellungen für Desktopanwendungen

-   Microsoft-Konto verarbeitet Windows-App-Einstellungen und Windows-Desktopeinstellungen

## Unternehmenseinstellungen (Center)


Sie können Ihren Benutzern eine gewisse Kontrolle darüber bieten, welche Einstellungen über eine Anwendung in UE-V 2 mit dem Namen Unternehmenseinstellungen-Center synchronisiert werden. Das Unternehmenseinstellungen-Center wird zusammen mit dem UE-v-Agent installiert, und die Benutzer können über die Systemsteuerung, das **Startmenü** oder den **Start** Bildschirm sowie über das Symbol UE-v-Benachrichtigungsbereich darauf zugreifen.

Das Unternehmenseinstellungen-Center zeigt an, welche Einstellungen synchronisiert sind, und ermöglicht Benutzern, den Synchronisierungsstatus von UE-V anzuzeigen. Wenn Sie Sie zulassen, können Benutzer mithilfe des Unternehmenseinstellungen-Centers auswählen, welche Einstellungen synchronisiert werden sollen. Sie können auch auf die Schaltfläche " **Jetzt synchronisieren** " klicken, um alle Einstellungen sofort zu synchronisieren.






## Verwandte Themen


[Erste Schritte mit UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

[Vorbereiten einer UE-V 2. x-Bereitstellung](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

 

 





