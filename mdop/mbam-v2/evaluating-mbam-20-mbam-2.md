---
title: Auswerten von MBAM 2.0
description: Auswerten von MBAM 2.0
author: dansimp
ms.assetid: bfc77eec-0fd7-4fec-9c78-6870afa87152
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7be883f44f5f09a904f619972ae3e7c35261d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810735"
---
# Auswerten von MBAM 2.0


Bevor Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) in einer Produktionsumgebung bereitstellen, sollten Sie Sie in einer Testumgebung auswerten. Die Informationen in diesem Thema können verwendet werden, um die Microsoft BitLocker-Verwaltung und-Überwachung mit einer eigenständigen Topologie in einer einzigen Server Testumgebung zu Evaluierungszwecken einzurichten. Eine Single-Server-Topologie wird für Produktionsumgebungen nicht empfohlen.

Anweisungen zum Bereitstellen von MBAM in einer Testumgebung finden Sie unter so wird es [gemacht: Installieren und Konfigurieren von MBAM auf einem einzelnen Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).

## Einrichten der Test Umgebung


Auch wenn Sie eine Nichtproduktionsinstanz von MBAM für die Auswertung in einer Testumgebung einrichten, sollten Sie dennoch überprüfen, ob Sie die Voraussetzungen und Hardware-und Softwareanforderungen erfüllt haben. Bevor Sie mit der Installation beginnen, lesen Sie [MBAM 2,0-Bereitstellungsvoraussetzungen](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2,0-unterstützte Konfigurationen](mbam-20-supported-configurations-mbam-2.md)und [Vorbereiten Ihrer Umgebung für MBAM 2,0](preparing-your-environment-for-mbam-20-mbam-2.md).

### Planen einer MBAM-Evaluierungsbereitstellung

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Aufgabe</th>
<th align="left">Verweise</th>
<th align="left">Anmerkungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Lesen Sie die Informationen zu den ersten Schritten zu MBAM, um ein grundlegendes Verständnis des Produkts zu erhalten, bevor Sie mit der Bereitstellungsplanung beginnen.</p></td>
<td align="left"><p><a href="getting-started-with-mbam-20-mbam-2.md" data-raw-source="[Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)">Erste Schritte mit MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planen Sie die Voraussetzungen für MBAM 2,0-Bereitstellung, und bereiten Sie Ihre Computerumgebung vor.</p></td>
<td align="left"><p><a href="mbam-20-deployment-prerequisites-mbam-2.md" data-raw-source="[MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md)">Bereitstellungsvoraussetzungen für MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planen und Konfigurieren von MBAM-Gruppenrichtlinienanforderungen</p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Planen der Gruppenrichtlinienanforderungen für MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planen und erstellen Sie die erforderlichen ActiveDirectoryDomainServices-Sicherheitsgruppen, und planen Sie die MBAM-Mitgliedschaftsanforderungen für lokale Sicherheitsgruppen.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planen der Administratorrollen für MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planen der Bereitstellung der MBAM-Server Features</p></td>
<td align="left"><p><a href="planning-for-mbam-20-server-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md)">Planen der Serverbereitstellung für MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planen der Bereitstellung der MBAM-Client Bereitstellung</p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)">Planen der Clientbereitstellung für MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

### Durchführen einer MBAM-Evaluierungsbereitstellung

Nachdem Sie die erforderlichen Planungs-und Softwarevoraussetzungen installiert haben, um Ihre Computing-Umgebung für die MBAM-Installation vorzubereiten, können Sie mit der MBAM-Evaluierungsbereitstellung beginnen.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Überprüfen Sie die MBAM-unterstützten Konfigurationsinformationen, um sicherzustellen, dass ausgewählte Client-und Server Computer für die MBAM-Feature-Installation unterstützt werden.</p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Von MBAM 2.0 unterstützte Konfigurationen</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Führen Sie MBAM-Setup aus, um MBAM-Server Features für Evaluierungszwecke auf einem einzelnen Server bereitzustellen.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)">So installieren und Konfigurieren von MBAM auf einem Server</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Hinzufügen von ActiveDirectoryDomainServices-Sicherheitsgruppen, die Sie während der Planungsphase erstellt haben, zu den entsprechenden lokalen MBAM-Server Features für lokale Gruppen auf dem neuen MBAM-Server.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planen von MBAM 2,0-Administratorrollen </a> und <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Verwalten von MBAM-Administratorrollen</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Erstellen und Bereitstellen erforderlicher MBAM-Gruppenrichtlinienobjekte</p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Bereitstellen der MBAM-Client Software.</p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)">Bereitstellen des MBAM 2.0-Clients</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## Konfigurieren von Lab-Computern für die MBAM-Evaluierung


Dieser Abschnitt enthält Informationen, die verwendet werden können, um die MBAM-Client Statusberichte zu beschleunigen. Diese Änderungen sollten jedoch nur zu Testzwecken verwendet werden.

**Hinweis**  Die Informationen im folgenden Abschnitt beschreiben, wie Sie die Windows-Registrierung ändern. Wenn Sie den Registrierungs-Editor falsch verwenden, kann dies zu schwerwiegenden Problemen führen, die eine Neuinstallation von Windows erforderlich machen. Microsoft kann nicht garantieren, dass Probleme, die sich aus der fehlerhaften Verwendung des Registrierungs-Editors ergeben, behoben werden können. Verwenden Sie den Registrierungs-Editor auf eigenes Risiko.

 

### Ändern der Häufigkeitseinstellungen für MBAM-Client Status Berichte

Die MBAM-Client Aktivierungs-und Statusberichts Frequenzen weisen einen Mindestwert von 90 Minuten auf, wenn Sie mithilfe von Gruppenrichtlinien eingerichtet werden. Sie können die Windows-Registrierung verwenden, um diese Frequenzen auf MBAM-Clientcomputern auf einen niedrigeren Wert zu ändern, um die Test Geschwindigkeit zu beschleunigen.

So ändern Sie die Häufigkeitseinstellungen für MBAM-Client Statusberichte:

1.  Verwenden Sie einen Registrierungs-Editor, um zu **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**zu navigieren.

2.  Ändern Sie die Werte für **ClientWakeupFrequency** und **StatusReportingFrequency** in **1** als mindestens vom Client unterstützter Wert. Diese Änderung bewirkt, dass der MBAM-Client jede Minute meldet.

3.  Starten Sie den **BitLocker-Verwaltungs Client Dienst**neu.

**Hinweis**  Um Werte festzulegen, die so gering sind, müssen Sie Sie manuell in der Registrierung festzulegen.

 

### Ändern der Startverzögerung des MBAM-Client Diensts

Zusätzlich zu den MBAM-Client Wakeup-und Statusberichts Frequenzen gibt es eine zufällige Verzögerung von bis zu 90 Minuten, wenn der MBAM-Client-Agent-Dienst auf Clientcomputern gestartet wird. Wenn Sie die zufällige Verzögerung nicht möchten, erstellen Sie einen **DWORD** -Wert von **NoStartupDelay** unter **HKLM\\Software\\Microsoft\\MBAM**, legen Sie seinen Wert auf **1**, und starten Sie dann den **BitLocker-Verwaltungs Client Dienst**erneut.

## Verwandte Themen


[Erste Schritte mit MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





