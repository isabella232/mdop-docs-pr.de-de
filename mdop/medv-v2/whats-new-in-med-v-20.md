---
title: Neuigkeiten in MED-V 2.0
description: Neuigkeiten in MED-V 2.0
author: dansimp
ms.assetid: 53b10bff-2b6f-463b-bdc2-5edc56526792
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 78dba25fec7ae2bb41da00902b59dcd15030f2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810114"
---
# Neuigkeiten in MED-V 2.0


Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 hat die Unterstützung für die Anwendungskompatibilität für Windows 7 entwickelt und Funktionen entfernt, die für dieses Szenario nicht erforderlich sind. Beispielsweise wurden Features wie die Verschlüsselung des Med-v-Arbeitsbereichs, der zentralisierte Med-v-Server und die Übertragung des Med-v-Arbeitsbereichs entfernt.

## Änderungen der Standard Funktionalität


In diesem Abschnitt werden die wichtigsten Bereiche erläutert, in denen sich die MED-V 2,0-Funktionalität geändert hat.

### Erstellen eines MED-V-Arbeitsbereichs

Die für den MED-V-Arbeitsbereich verwendete virtuelle Festplatte wird jetzt in Windows Virtual PC erstellt. Die zum Erstellen des MED-V-Arbeitsbereichs verwendeten Methoden umfassen die Installation von Windows XP SP3, das Aktualisieren des Betriebssystems und das Vorbereiten der Verwaltung über die Softwareverwaltungsinfrastruktur.

Die Funktion für die Offlineverwaltung und die Trimm Übertragung wurde zusätzlich zur proprietären MED-V Workspace-Verschlüsselungs-und-Komprimierungsfunktion entfernt. Wenn Sie einen Med-v-Arbeitsbereich erstellen, sollte ein Administrator geeignete Anwendungen und Verwaltungstools im Abbild vorbereiten und konfigurieren, anstatt das Tool zur Vorbereitung der virtuellen Maschine zu verwenden, das in Med-v 1,0 bereitgestellt wird.

Das Ausführen von Sysprep für das Med-v-Abbild ist jetzt erforderlich und wird während der Verpackung des Med-v-Arbeitsbereichs überprüft. Der MED-V Workspace Packager bietet eine grafische Benutzeroberfläche (Graphical User Interface, GUI), die den Administrator durch den Verpackungsprozess führt. Die Konsole von Med-v 1,0 wurde zusammen mit der Funktionalität zum Verwalten von Bildern, Verwalten von Med-v-Arbeitsbereichs Profilen und der Anforderung zum Bereitstellen und Verschlüsseln von Med-v-Arbeitsbereichen entfernt.

### Bereitstellung von MED-V Workspace

Zur Bereitstellungeines MED-V-Arbeitsbereichs kann ein Administrator nun die Vorteile der Tools für die elektronische Softwareverteilung nutzen. Die in Med-v 1,0 verfügbare Client-Pull-Methode wurde entfernt, und der Med-v-Arbeitsbereich wird jetzt mithilfe von Methoden außerhalb von Med-v bereitgestellt. Administratoren können Med-v-Arbeitsbereiche wie jedes andere Anwendungspaket behandeln und Bereitstellungen und Installationen von Med-v mithilfe der vorhandenen Tools und Prozesse planen. MED-V-Installationen können lautlos bereitgestellt werden und können problemlos innerhalb einer vorhandenen Softwareverteilungsinfrastruktur verwaltet werden.

### MED-V-Arbeitsbereichsverwaltung

Der Med-v-Arbeitsbereich in Med-v 2,0 basiert auf einer virtuellen Windows Virtual PC-Festplatte. Med-v hat die von Windows Virtual PC bereitgestellten Funktionen erweitert, indem die nahtlose Benutzeroberfläche verbessert wird, ohne dass Verschlüsselung oder spezielle Tools für den Zugriff auf den MED-V-Arbeitsbereich erforderlich sind.

Nachdem Med-v auf einer Workstation bereitgestellt wurde, kann der Med-v-Arbeitsbereich mithilfe von Windows Virtual PC im Vollbildmodus geöffnet werden. Mit dieser neuen Funktionalität wurde die Anforderung für Richtlinien entfernt, die eine Einstellung für Seamless-oder Vollbild-Modi festlegten, und auch die Notwendigkeit, den Vollbildmodus für Diagnose und Problembehandlung zu erzwingen, wurde entfernt.

Das Veröffentlichen von Anwendungen im MED-V-Arbeitsbereich wird nicht mehr mit Profilen durchgeführt und manuell in den Pfad zu Anwendungen eingegeben. Stattdessen tritt sie automatisch auf, wenn Anwendungen auf dem Gast installiert werden. Das zentrale Bild-Repository, in dem Versionen der Bilder enthalten sind, die über die Trimm Übertragung übermittelt wurden, wird entfernt. Stattdessen ermöglicht Med-v Administratoren das Verwalten des Med-v-Arbeitsbereichs wie ein physischer Computer, indem Anwendungen und Updates ohne die Komplexität einer dedizierten MED-V-Infrastruktur verteilt werden.

## Änderungen in MED-V-Features


In einigen wichtigen Bereichen von MED-V 2,0 werden Verbesserungen oder Ergänzungen der folgenden Features widergespiegelt.

### Erstellen eines MED-V-Arbeitsbereichs

MED-V-Arbeitsbereiche müssen mithilfe von Windows Virtual PC erstellt werden. Vorhandene Virtual PC 2007-Bilder müssen migriert werden. Das Tool für die Vorbereitung virtueller Computer ist nicht in Med-v 2,0 enthalten, und Administratoren sollten Ihre Bilder entsprechend der Med-v 2,0-Hilfedatei konfigurieren, aktualisieren und optimieren. Das Ausführen von Sysprep auf dem MED-V-Abbild ist ein erforderlicher Schritt und muss vor dem Verpacken ausgeführt werden.

### MED-V-Arbeitsbereichs Verpackung

Windows PowerShell ist die Grundlage des MED-V-Arbeitsbereichs Pakets. Diese Funktion ersetzt einige frühere Konsolen Fähigkeiten und-Funktionen, die zentralisierte Funktionen von MED-V verwaltet haben. Der MED-V Workspace-Paketer verpackt lediglich die virtuelle Festplatte mit den entsprechenden Einstellungen und dem Bild, sodass Sie von Administratoren problemlos bereitgestellt werden kann. Erweiterte Features werden mithilfe von Windows PowerShell bereitgestellt.

### MED-V-Arbeitsbereichs Verteilung

Für med-v 2,0 ist keine dedizierte Serverinfrastruktur mehr erforderlich, und die Client Pull-Methode zum Bereitstellen von Med-v-Arbeitsbereichen wurde entfernt. MED-V-Arbeitsbereiche werden jetzt mithilfe Ihrer Infrastruktur für die elektronische Softwareverteilung bereitgestellt und können auf allgemeinen Freigaben gespeichert werden, die für andere Installationspakete verwendet werden.

### Erstmaliges Einrichten

Der erstmalige Setupprozess ist jetzt in die Standard-Imaging-Konvention von Sysprep integriert. Beim erstmaligen Einrichten des Med-v-Arbeitsbereichs können die im Med-v-Arbeitsbereichs Paket angegebenen Einstellungen dynamisch auf das Bild angewendet werden, während das Mini Setup beginnt. Das Skript Tool in der Konsole wurde entfernt, und der erstmalige Setup-Vorgang basiert nun auf Optionen, die vom Administrator im MED-V Workspace-Paketer konfiguriert sind.

### Anwendungsveröffentlichung

Administratoren können Anwendungen auf dem Med-v-Abbild entweder vor dem Verpacken, nach der Bereitstellung des Med-v-Arbeitsbereichs oder mithilfe einer Kombination aus beidem installieren. Med-v untersucht nicht mehr die Med-v Workspace-Richtlinie, um Anwendungen zu veröffentlichen, sondern bezieht sich stattdessen auf das, was tatsächlich auf dem Gast installiert ist. Wenn Anwendungen auf dem Gast installiert sind, werden Sie automatisch erkannt und **im Startmenü des Hosts veröffentlicht** und können vom Endbenutzer gestartet werden.

### URL-Umleitung

MED-V 2,0 bietet eine nahtlose Umleitung von Host-zu-Guest-Webadressen basierend auf den vom Administrator konfigurierten und verwalteten Richtlinien. Nachdem eine URL an den Gast Browser umgeleitet wurde, besteht die standardmäßige Erfahrung darin, den Benutzer auf die umgeleitete Website zu beschränken. Auf diese Weise werden die Browseraktivitäten minimiert, die ein Benutzer ausführen kann, die nicht vom Administrator vorgesehen sind. Die Guest-to-Host-Browserumleitung wurde entfernt.

### Problembehandlung

MED-V nutzt nun die standardmäßigen hostbasierten Prozesse für die Problembehandlung. Da der MED-V-Arbeitsbereich nicht mehr verschlüsselt ist, kann er innerhalb der Windows Virtual PC-Konsole im Vollbildmodus geöffnet werden, wo er als standardarbeitsstation angezeigt und bearbeitet werden kann. Darüber hinaus werden die Protokolle nicht mehr lokal verschlüsselt und zentral protokolliert. MED-V nutzt nun die lokalen Ereignisprotokolle umfassend, und der Protokolliergrad der Ausgabe, vom Informations-zu Debug-Level, kann einfach konfiguriert werden. Schließlich wird jetzt ein Toolkit zur Problembehandlung bereitgestellt, damit Administratoren und Helpdesk-Mitarbeiter über eine grafische, aggregierte Ansicht aller Problembehandlungsoptionen verfügen können, und Sie können mühelos die Aktivitäten auswählen, die Ihren Anforderungen am besten entsprechen.

MED-V wird nicht mehr als Systemdienst ausgeführt. Stattdessen wird Sie als Benutzer eigene Prozesse ausgeführt und nur ausgeführt, wenn ein Benutzer angemeldet ist.Funktionen, die zuvor vom systemeigenen Dienst bereitgestellt wurden, werden jetzt in den benutzerseitigen Prozessen bereitgestellt.

## Verwandte Themen


[Bereitstellung von MED-V](deployment-of-med-v.md)

[Vorgänge für MED-V](operations-for-med-v.md)

 

 





