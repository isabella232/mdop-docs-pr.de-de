---
title: High-Level-Architektur für UE-V 1.0
description: High-Level-Architektur für UE-V 1.0
author: dansimp
ms.assetid: d54f9f10-1a4d-4e56-802d-22d51646e1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 76703cf4c7297401e6516830bf194cef741d60ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812151"
---
# High-Level-Architektur für UE-V 1.0


In diesem Thema werden die architektonischen Elemente der Microsoft User Experience Virtualization (UE-V)-Einstellungen für die Roaming-Lösung auf hoher Ebene beschrieben. Die folgenden Elemente sind Teil einer Standard-UE-V-Bereitstellung.

![Architekturdiagramm für UE-v-Agents](images/ue-vagentarchitecturaldiagram.gif)

Der UE-v-Agent überwacht die Anwendungen und die Betriebssystemprozesse, wie Sie in den Standort Vorlagen für UE-v-Einstellungen identifiziert werden. Wenn die Anwendung oder das Betriebssystem gestartet wird, werden die Einstellungen aus dem Einstellungspaket gelesen und auf den Computer angewendet. Wenn die Anwendung geschlossen wird oder wenn das Betriebssystem gesperrt oder heruntergefahren wird, werden die Einstellungen in einem UE-V-Einstellungspaket im Speicherort für Einstellungen gespeichert.

## Speicherort des Einstellungs Speichers


Der Speicherort der Einstellungen ist eine Dateifreigabe, auf die der Benutzer von Virtualization Agent Zugriff auf Lese-und Schreib Einstellungen hat. Dieser Speicherort ist entweder das Active Directory-Basisverzeichnis oder während der UE-V-Installation definiert. Sie können den Speicherort während der Installation des UE-V-Agents festlegen, oder Sie können ihn später mit Gruppenrichtlinien, WMI oder PowerShell festlegen. Der Speicherort kann auf jeder gängigen Dateifreigabe liegen, auf die Benutzer zugreifen können. Wenn während der Installation kein Speicherplatz festgelegt wird, verwendet UE-V das Home-Verzeichnis in Active Directory. Der UE-V-Agent überprüft den Standort und erstellt einen Systemordner, der für den Benutzer verborgen ist, in dem die Benutzereinstellungen gespeichert und darauf zugegriffen werden kann. Weitere Informationen zum Speichern von Einstellungen finden Sie unter [Vorbereiten Ihrer Umgebung für UE-V](preparing-your-environment-for-ue-v.md).

## UE-V-Agent


Der UE-V-Agent ist auf jedem Computer mit Einstellungen installiert, die von der Benutzeroberflächen-Virtualisierung synchronisiert werden. Der Agent überwacht die registrierten Anwendungen und das Betriebssystem, damit Änderungen an den Einstellungen vorgenommen werden, und synchronisiert diese Einstellungen zwischen Computern. Einstellungen werden vom Speicherort der Einstellungen auf die Anwendung angewendet, wenn die Anwendung gestartet wird. Die Einstellungen werden dann beim Schließen der Anwendung an den Speicherort der Einstellungen zurückgespeichert. Die Betriebssystemeinstellungen werden angewendet, wenn sich der Benutzer anmeldet, wenn der Computer entriegelt wird, oder wenn der Benutzer mithilfe von Remotedesktopprotokoll (RDP) eine Remoteverbindung mit dem Computer herstellt. Der Agent speichert Einstellungen, wenn sich der Benutzer abmeldet, wenn der Computer gesperrt ist oder wenn eine Remoteverbindung getrennt wird. Weitere Informationen zum UE-v-Agent finden Sie unter [Vorbereiten Ihrer Umgebung für UE-v](preparing-your-environment-for-ue-v.md).

## <a href="" id="bkmk-settingslocationtemplate"></a>Einstellungen-Speicherort Vorlagen


Die Vorlage "Settings Location" ist eine XML-Datei, die die Einstellungsspeicher Orte definiert, die von der Benutzeroberflächen-Virtualisierung überwacht werden sollen. Nur die Einstellungen, die in diesen Einstellungs Vorlagen definiert sind, werden auf Computern erfasst oder angewendet, auf denen der UE-V-Agent ausgeführt wird. Die Vorlage "Settings Location" enthält keine Einstellungswerte, sondern nur die Speicherorte, an denen die Werte auf dem Computer gespeichert sind.

UE-V enthält eine Reihe von Einstellungen für Standort Vorlagen, die Einstellungen für einige Microsoft-Anwendungen und Windows-Einstellungen festlegen. Ein Administrator kann mithilfe des UE-V-Generators benutzerdefinierte Standort Vorlagen für Einstellungen erstellen.

[Planen der Verwendung von Anwendungen zum Synchronisieren mit UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

[Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

[Arbeiten mit benutzerdefinierten UE-V-Vorlagen und dem UE-V-Generator](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

## Einstellungen-Pakete


Anwendungseinstellungen und Windows-Einstellungen werden in den Einstellungen-Paketen gespeichert, die vom UE-V-Agent erstellt werden. Bei einem Einstellungspaket handelt es sich um eine Sammlung der Einstellungen, die in den Einstellungen-Speicherort Vorlagen dargestellt werden. Diese Einstellungs Pakete werden erstellt, lokal gespeichert und dann in den Speicherort der Einstellungen kopiert. "Letzte Write-WINS" legt fest, welche Einstellungen beibehalten werden, wenn ein einzelner Benutzer die mehr als einen Computer mit einem Speicherort synchronisiert. Der Agent, der auf einem Computer ausgeführt wird, liest und schreibt unabhängig von Agents, die auf anderen Computern ausgeführt werden, den Einstellungs Speicherort. Die zuletzt geschriebenen Einstellungen und Werte werden angewendet, wenn der nächste Agent vom Speicherort für Einstellungen liest.

![UE-v-Generator Prozess](images/ue-vgeneratorprocess.gif)

## Vorlagenkatalog für Einstellungen


Der Vorlagenkatalog für Einstellungen ist ein Ordnerpfad auf UE-V-Computern oder eine SMB-Netzwerkfreigabe (Server Message Block), in der alle benutzerdefinierten Einstellungen für den Speicherort gespeichert sind. Der UE-V-Agent ruft neue oder aktualisierte Vorlagen von diesem Speicherort ab. Der UE-V-Agent überprüft diesen Speicherort einmal täglich und aktualisiert sein Synchronisierungsverhalten auf der Grundlage der Vorlagen in diesem Ordner. Die Vorlagen, die seit der letzten Überprüfung in diesem Ordner hinzugefügt oder aktualisiert wurden, werden vom UE-V-Agent registriert. Der UE-V-Agent hebt die Registrierung der Vorlagen auf, die aus diesem Ordner entfernt wurden. Vorlagen werden vom Aufgabenplaner einmal pro Tag registriert und nicht registriert. Wenn Sie nur die Vorlagen für Standardeinstellungen verwenden, die in UE-V enthalten sind, ist ein Einstellungs Vorlagenkatalog nicht erforderlich. Weitere Informationen zu Einstellungen-Bereitstellungs Katalogen finden Sie unter [Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

## User Experience Virtualization-Generator


Mit dem User Experience Virtualization Generator können Sie benutzerdefinierte Standort Vorlagen für Einstellungen erstellen, in denen die Speicherorte der Anwendungen gespeichert werden, die im Unternehmen verwendet werden und die Sie in die Lösung für Roamingeinstellungen einbeziehen möchten. Der UE-V-Generator versucht, die Speicherorte der Registrierungswerte und die Einstellungsdateien für Anwendungen zu ermitteln, und zeichnet dann diese Speicherorte in einer XML-Datei mit einer Einstellungs Speicherort Vorlage auf. Anschließend können Sie die Speicherort Vorlagen für Einstellungen an die Benutzer Computer verteilen. Der UE-V-Generator ermöglicht es einem Administrator auch, eine vorhandene Vorlage zu bearbeiten oder eine Vorlage zu validieren, die mit einem anderen XML-Editor erstellt wurde.

Der UE-V-Generator überwacht eine Anwendung, um herauszufinden, wo Sie Ihre Einstellungen speichert. Zu diesem Zweck überwacht Sie, wo die Anwendung in der HKEY \ _CURRENT \ _User Registrierung oder in den Dateiordnern unter **Benutzer** \ \ \ [Benutzername \] \ \ **AppData**  \\  **Roaming und Benutzer** \ \ \ \ \ \ \ **\ \**  \\  **Local**\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \

Der Ermittlungsprozess schließt Registrierungsschlüssel und Dateien aus, für die der angemeldete Benutzer keine Werte schreiben kann. Keine dieser Dateien wird in der XML-Datei enthalten sein. Der Ermittlungsprozess schließt auch Registrierungsschlüssel und Dateien aus, die mit der Kernfunktionalität des Windows-Betriebssystems verknüpft sind.

Weitere Informationen zum UE-v-Generator finden Sie unter [Installieren des UE-v-Generators](installing-the-ue-v-generator.md).

## Verwandte Themen


[Microsoft-User Experience Virtualization (UE-V) 1.0](index.md)

[Erste Schritte mit User Experience Virtualization 1.0](getting-started-with-user-experience-virtualization-10.md)

[Informationen zu User Experience Virtualization 1.0](about-user-experience-virtualization-10.md)

[Arbeiten mit benutzerdefinierten UE-V-Vorlagen und dem UE-V-Generator](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

 

 





