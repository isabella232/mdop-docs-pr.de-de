---
title: Informationen zu User Experience Virtualization 1.0
description: Informationen zu User Experience Virtualization 1.0
author: dansimp
ms.assetid: 3758b100-35a8-4e10-ac08-f583fb8ddbd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6010f9c4ebc260eec0324fb880dc2c92fd675130
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809520"
---
# Informationen zu User Experience Virtualization 1.0


Microsoft User Experience Virtualization (UE-V) überwacht die von Benutzern vorgenommenen Änderungen an den Anwendungseinstellungen und den Einstellungen des Windows-Betriebssystems. Die Benutzereinstellungen werden erfasst und an einem Einstellungs Speicherort zentralisiert. Diese Einstellungen können dann auf die verschiedenen Computer angewendet werden, auf die der Benutzer zugreifen kann, einschließlich Desktopcomputern, Laptops und Virtual Desktop Infrastructure (VDI)-Sitzungen.

Die Virtualisierung der Benutzeroberfläche verwendet Einstellungen für Standort Vorlagen, um anzugeben, welche Anwendungen und Windows-Einstellungen auf den Benutzercomputern überwacht und zentralisiert werden. Die Vorlage "Settings Location" ist eine XML-Datei, die angibt, welche Datei-und Registrierungsspeicherorte den einzelnen Anwendungs-oder Betriebssystem Einstellungen zugeordnet sind. Die Vorlage enthält keine Werte für die Einstellungen; Sie enthält nur die Speicherorte der Einstellungen, die überwacht werden sollen.

Die Anwendungseinstellungen und Windows-Einstellungen werden von UE-V überwacht, wenn Benutzer auf ihren Computern arbeiten. Die Werte für die Anwendungseinstellungen werden auf dem Speicherserver für Einstellungen gespeichert, wenn der Benutzer die Anwendung schließt. Die Werte für die Windows-Einstellungen werden gespeichert, wenn sich der Benutzer abmeldet, wenn der Computer gesperrt ist oder wenn er die Verbindung von einem Computer entfernt trennt.

Ein Administrator kann eine Standort Vorlage für UE-V-Einstellungen erstellen, um anzugeben, welche Enterprise-Anwendungseinstellungen durchlaufen werden. UE-V enthält eine Reihe von Einstellungen für die Speicherort Vorlagen für einige Microsoft-Anwendungen und Windows-Einstellungen. Eine Liste der Standardanwendungen und-Einstellungen in UE-v finden Sie unter [Planen der zu synchronisierenden Anwendungen mit UE-v 1,0](planning-which-applications-to-synchronize-with-ue-v-10.md).

## UEV 1,0-Versionshinweise


Weitere Informationen sowie aktuelle Nachrichten, die nicht in die Dokumentation eingehen, finden Sie unter [Microsoft User Experience Virtualization (UE-V) 1,0-Versionshinweise](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).

## Verwandte Themen


[Erste Schritte mit User Experience Virtualization 1.0](getting-started-with-user-experience-virtualization-10.md)

[Microsoft-User Experience Virtualization (UE-V) 1.0](index.md)

[High-Level-Architektur für UE-V 1.0](high-level-architecture-for-ue-v-10.md)

 

 





