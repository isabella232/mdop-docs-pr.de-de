---
title: Bereitstellen von UE-V-Speicherortvorlagen für UE-V 1.0
description: Bereitstellen von UE-V-Speicherortvorlagen für UE-V 1.0
author: dansimp
ms.assetid: 7e0cc553-14f7-40fa-828a-281c8d2d1934
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b276fb9d6c0b3749f9818483869dfe98bbc147c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812166"
---
# Bereitstellen von UE-V-Speicherortvorlagen für UE-V 1.0


Microsoft User Experience Virtualization (UE-V) verwendet Einstellungen-Standort Vorlagen (XML-Dateien), die die Einstellungen definieren, die von der Benutzeroberflächen-Virtualisierung erfasst und angewendet werden. UE-v umfasst eine Reihe von Standardvorlagen sowie ein Tool, den UE-v-Generator, mit dem Sie benutzerdefinierte Speicherort Vorlagen für Einstellungen erstellen können. Nachdem Sie eine Vorlage für Einstellungs Speicherort erstellt haben, sollten Sie Sie testen, um sicherzustellen, dass die Anwendungseinstellungen in einer Testumgebung ordnungsgemäß durchlaufen werden. Anschließend können Sie die Vorlage für die Einstellungsposition sicher auf Computern im Unternehmen bereitstellen.

Einstellungen Speicherort Vorlagen können mithilfe von ESD (Enterprise Software Distribution), Gruppenrichtlinieneinstellungen oder durch Konfigurieren eines UE-V-Einstellungs Vorlagen Katalogs bereitgestellt werden. Vorlagen, die mithilfe einer ESD-oder Gruppenrichtlinie bereitgestellt werden, müssen über UE-V WMI oder PowerShell registriert werden. Vorlagen, die im Katalogspeicherort für Einstellungs Vorlagen gespeichert sind, werden vom UE-V-Agent automatisch registriert.

## Bereitstellen der Einstellungen-Speicherort Vorlagen mit einem Katalogpfad für Einstellungs Vorlagen


Der Katalogpfad der UE-V-Einstellungen für die Standort Vorlage kann mithilfe der folgenden Methoden definiert werden: Gruppenrichtlinien, Befehlszeilenparameter für Agenteninstallation, WMI oder PowerShell. Nach dem Definieren des Vorlagenkatalog Pfads ruft der UE-V-Agent die neuen oder aktualisierten Vorlagen von diesem Speicherort ab. Der UE-V-Agent überprüft diesen Standort einmal täglich und aktualisiert sein Synchronisierungsverhalten auf der Grundlage der in diesem Ordner gefundenen Vorlagen. Vorlagen, die seit der letzten Überprüfung in diesem Ordner hinzugefügt oder aktualisiert wurden, werden vom UE-V-Agent registriert. Der UE-V-Agent hebt auch die Registrierung von Vorlagen auf, die aus diesem Ordner entfernt wurden. Vorlagen werden vom Aufgabenplaner einmal pro Tag registriert und nicht registriert.

**So verwenden Sie den Katalogpfad der Einstellungs Vorlage zum Bereitstellen von UE-V-Einstellungen Speicherort Vorlagen**

1.  Navigieren Sie zu dem Netzwerkfreigabeordner, der als Vorlagenkatalog für Einstellungen definiert ist.

2.  Hinzufügen, entfernen oder Aktualisieren von Einstellungen für Standort Vorlagen im Einstellungs Vorlagenkatalog, um die gewünschte UE-v-Agent-Vorlagenkonfiguration für UE-v-Computer wiederzugeben.

3.  Vorlagen auf Computern werden basierend auf Änderungen am Vorlagenkatalog für Einstellungen täglich aktualisiert.

4.  Öffnen Sie eine Eingabeaufforderung mit erhöhten Rechten, und navigieren Sie zu **% Program Files%\\Microsoft User Experience Virtualization \ \ Agent \ \ &lt; x86 oder x64 &gt; **, und führen Sie dann **ApplySettingsTemplateCatalog.exe** aus, um Vorlagen auf einem Computer, auf dem der UE-V-Agent ausgeführt wird, manuell zu aktualisieren.

## Verwandte Themen


[Microsoft-User Experience Virtualization (UE-V) 1.0](index.md)

[Bereitstellen von UE-V 1.0](deploying-ue-v-10.md)

[Planen der Verwendung von Anwendungen zum Synchronisieren mit UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

 

 





