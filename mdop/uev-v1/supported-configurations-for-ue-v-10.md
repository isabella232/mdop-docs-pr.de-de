---
title: Unterstützte Konfigurationen für UE-V 1.0
description: Unterstützte Konfigurationen für UE-V 1.0
author: dansimp
ms.assetid: d90ab83e-741f-48eb-b1d8-a64cb9259f7a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a84514317de8a4cfd9df9c94a9a130933b00874a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811224"
---
# Unterstützte Konfigurationen für UE-V 1.0


Microsoft User Experience Virtualization (UE-V) unterstützt die folgenden beschriebenen Konfigurationen.

**Hinweis**  Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das vorhergehende Service Pack. Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975). Weitere Informationen zu den Microsoft-Supportlebenszyklus Richtlinien finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).

 

## Unterstützte Konfigurationen für UE-v-Agent und UE-v-Generator


In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die den User Experience Virtualization Generator und den User Experience Virtualization Agent unterstützen.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Betriebssystem</strong></th>
<th align="left"><strong>Edition</strong></th>
<th align="left"><strong>Service Pack</strong></th>
<th align="left"><strong>System Architektur</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Ultimate-, Enterprise-oder Professional-Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
<td align="left"><p>.NET Framework 3,5 SP1</p>
<p>.NET Framework 4 (Generator)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard, Enterprise, Rechenzentrum oder Web Server</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>.NET Framework 3,5 SP1</p>
<p>.NET Framework 4 (Generator)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Enterprise-oder Professional-Edition</p></td>
<td align="left"><p>Keine</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
<td align="left"><p>.NET Framework 4 oder .NET Framework 3,5 SP1 (Agent)</p>
<p>.NET Framework 4 (Generator)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard oder Rechenzentrum</p></td>
<td align="left"><p>Keine</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>.NET Framework 4 oder .NET Framework 3,5 SP1 (Agent)</p>
<p>.NET Framework 4 (Generator)</p></td>
</tr>
</tbody>
</table>

 

Es gibt keine speziellen RAM-Anforderungen, die für UE-V spezifisch sind.

Die Installation des UE-v-Agents erfordert Administratorrechte und erfordert einen Neustart des Computers, bevor der UE-v-Agent ausgeführt werden kann.

**Wichtig**  Das Feature "Ihre Einstellungen synchronisieren" in Windows 8 muss deaktiviert sein, damit UE-V ordnungsgemäß funktioniert. Die Synchronisierung von Einstellungen mit Windows 8 und UE-V führt zu einem unvorhersehbaren Synchronisierungsverhalten.

 

### <a href="" id="requirements-for-the-offline-files-feature-"></a>Voraussetzungen für das Feature "Offline Dateien"

Der UE-V-Agent kann Benutzereinstellungen für Computer synchronisieren, die nicht immer mit dem Unternehmensnetzwerk verbunden sind, beispielsweise einen Laptop Computer oder Computer, die sich in Remoteniederlassungen befinden, sowie Computer, die immer mit dem Unternehmensnetzwerk verbunden sind, wie etwa Windows-Server, die VDI-Sitzungen (Virtual Desktop Interface) hosten.

Die Standardkonfiguration UE-V verwendet das Windows-Feature "Offline Datei" zum Synchronisieren von Einstellungen. Offline Dateien stellen sicher, dass die Einstellungen des Benutzers auch dann verfügbar sind, wenn der Computer das Unternehmensnetzwerk verlässt. Alle Änderungen, die an den Einstellungen vorgenommen werden, werden automatisch mit dem Speicherort der Einstellungen synchronisiert, wenn die Verbindung mit dem Unternehmensnetzwerk wiederhergestellt wird. In Offline Dateien wird auch sichergestellt, dass die Einstellungen des Benutzers für Computer verfügbar sind, die sich in einem Remote-Büro mit einer langsamen oder nur geringen Verbindung befinden.

Zum Synchronisieren von Einstellungen für Computer, die gelegentlich das Unternehmensnetzwerk verlässt, muss das Feature Offline Dateien aktiviert und gestartet werden, bevor die UE-V-Agent-Bereitstellung beginnt. Das Feature Offline Dateien ist in Windows7 standardmäßig aktiviert. Das Feature ist unter Windows Server2008R2, Windows Server 2012 und Windows 8 standardmäßig deaktiviert. Wenn das Feature Offline Dateien nicht aktiviert ist, schlägt die Synchronisierung der UE-V-Einstellungen fehl.

-   **Windows7**

    Das Feature "Offline Dateien" ist unter Windows 7 standardmäßig aktiviert. Falls erforderlich, können Offline Dateien mithilfe des folgenden Befehls an einer Eingabeaufforderung mit erhöhten Rechten aktiviert werden:

    ``` syntax
    sc config CscService start=auto
    ```

-   **Windows 8**

    Das Feature Offline Dateien ist unter Windows 8-Version standardmäßig deaktiviert. Offline Dateien können unter Windows 8 unter Verwendung des folgenden Befehls an einer Eingabeaufforderung mit erhöhten Rechten aktiviert werden:

    ``` syntax
    sc config CscService start=auto
    ```

-   **Windows Server 2008 R2 und Windows Server 2012**

    Das Feature "Offline Dateien" wird unter Windows Server 2008 R2 oder Windows Server 2012 nicht standardmäßig installiert. Um das Feature "Offline Dateien" zu aktivieren, muss das Desktop Experience Pack installiert sein. Hierbei handelt es sich um eine optionale Serverkomponente, die das Feature "Offline Dateien" enthält. Sobald die Installation erfolgt ist, starten Sie das Feature "Offline Dateien" mit den folgenden Befehlen an einer Eingabeaufforderung mit erhöhten Rechten:

    ``` syntax
    sc config csc start= system
    ```

    ``` syntax
    sc config cscservice start= auto
    ```

Der Computer muss neu gestartet werden, bevor die Einstellungen synchronisiert werden.

### Synchronisierung für Computer mit immer verfügbaren Verbindungen

Wenn Sie UE-V auf Computern verwenden, die immer mit dem Unternehmensnetzwerk verbunden sind, beispielsweise einem Windows Server-Computer, auf dem VDI-Sitzungen gehostet werden, sollten Offline Dateien deaktiviert sein.

Wenn der UE-V-Agent so konfiguriert ist, dass Einstellungen ohne Verwendung von Offline Dateien synchronisiert werden, wird der Speicherserver für Einstellungen als Standardnetzwerk Freigabe behandelt. Die Einstellungen werden synchronisiert, wenn das Netzwerk verfügbar ist. In dieser Konfiguration kann der UE-V-Agent so konfiguriert werden, dass er eine Benachrichtigung erhält, wenn der Import der Anwendungseinstellungen verzögert wird.

Wenn das Feature Offline Dateien nicht verwendet wird, müssen Sie das Standardverhalten UE-v vor oder während der Bereitstellung des UE-v-Agents deaktivieren. Führen Sie eine der folgenden Aktionen aus, um Offline Dateien für UE-V zu deaktivieren:

-   Bevor Sie den UE-v-Agent bereitstellen, markieren Sie das Kontrollkästchen "keine Offline Dateien verwenden" in der Gruppenrichtlinieneinstellung UE-v.

-   Legen Sie während der UE-V-Installation den Parameter AgentSetup.exe `SyncMethod = None` an der Eingabeaufforderung oder in einer Batchdatei ab. Weitere Informationen zum Bereitstellen des Agents finden Sie unter [Bereitstellen des UE-V-Agents](deploying-the-ue-v-agent.md).

Wenn Sie die Einstellung für die Offline Dateien für UE-v deaktivieren und den **SyncMethod** -Parameter während der Installationszeit nicht angeben, schlägt die Installation des UE-v-Agents fehl. Sie können die Offline Dateien auch mit PowerShell oder WMI deaktivieren. Weitere Informationen zu WMI-und PowerShell-Befehlen finden Sie unter [Verwalten des UE-V 1,0-Agents und von Paketen mit PowerShell und WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).

Der Computer muss neu gestartet werden, bevor die Einstellungen synchronisiert werden.

### Voraussetzungen für das UE-V PowerShell-Feature

Für das UE-V PowerShell-Feature des Agents muss .NET Framework, Version 3,5 SP1, aktiviert sein, und PowerShell-Version 2,0 oder höher.

### Voraussetzungen für die Unterstützung des UE-V-Generators

Installieren Sie den UE-V-Generator auf dem Computer, der zum Erstellen benutzerdefinierter Einstellungen für Standort Vorlagen verwendet wird. Auf diesem Computer sollten die Anwendungen installiert sein, deren Einstellungen durchlaufen werden. Sie müssen ein Mitglied der Gruppe Administratoren auf dem Computer sein, auf dem die UE-V-Generator Software ausgeführt wird. Darüber hinaus muss der UE-V-Generator auf einem Computer installiert sein, auf dem ein NTFS-Dateisystem verwendet wird. Die UE-V-Generator Software erfordert .NET Framework, Version 4. Weitere Informationen finden Sie unter [Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

## Verwandte Themen


[Planen für UE-V 1.0](planning-for-ue-v-10.md)

[Vorbereiten der Umgebung für UE-V](preparing-your-environment-for-ue-v.md)

[Bereitstellen von UE-V 1.0](deploying-ue-v-10.md)

Unterstützte Konfigurationen für die Virtualisierung der Benutzeroberfläche [Bereitstellen des Speicherorts für die Einstellungen für UE-V 1,0](deploying-the-settings-storage-location-for-ue-v-10.md)

[Installieren von UE-V-Generator](installing-the-ue-v-generator.md)

[Bereitstellen von UE-V-Agent](deploying-the-ue-v-agent.md)

 

 





