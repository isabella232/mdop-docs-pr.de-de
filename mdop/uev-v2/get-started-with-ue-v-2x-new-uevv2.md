---
title: Erste Schritte mit UE-V 2.x
description: Erste Schritte mit UE-V 2.x
author: dansimp
ms.assetid: 526ecbf0-0dee-4f0b-b017-8f8d25357b14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 02/13/2017
ms.openlocfilehash: d3f01dd67ea9e5f6cfcf5dc3425265deff3f7df1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809865"
---
# Erste Schritte mit UE-V 2.x


Führen Sie die Schritte in diesem Leitfaden aus, um die Microsoft User Experience Virtualization (UE-V) 2,0 oder 2,1 in einer kleinen Testumgebung schnell bereitzustellen. So können Sie feststellen, ob UE-V die richtige Lösung zur Verwaltung von Benutzereinstellungen auf mehreren Geräten innerhalb Ihres Unternehmens ist.

**Hinweis**  Die Informationen in diesem Abschnitt werden während der restlichen Dokumentation ausführlicher wiederholt. Wenn Sie also bereits wissen, dass UE-v 2 die richtige Lösung ist und Sie es nicht auswerten müssen, können Sie einfach nach rechts [eine UE-v 2. x-Bereitstellung vorbereiten](prepare-a-ue-v-2x-deployment-new-uevv2.md).

 

Die Standardinstallation von UE-V synchronisiert die Standardeinstellungen für Microsoft Windows und Office sowie viele Windows-App-Einstellungen. Stellen Sie sicher, dass Ihre Testumgebung zwei oder Mehrbenutzercomputer umfasst, die den Netzwerkzugriff freigeben, und Sie in kürzester Zeit UE-V evaluieren.

-   [Schritt 1: Überprüfen der Voraussetzungen](#step1): Stellen Sie sicher, dass Ihre Umgebung UE-V ausführen kann, einschließlich Details zu unterstützten Konfigurationen.

-   [Schritt 2: Bereitstellen des Speicherorts für die Einstellungen für UE-v 2](#step2): alle UE-v-Bereitstellungen erfordern einen Speicherort für Einstellungs Pakete, die die synchronisierten Einstellungswerte enthalten.

-   [Schritt 3: Bereitstellen des UE-v 2-Agents](#step3): damit die Einstellungen mit UE-v synchronisiert werden können, muss der UE-v-Agent installiert sein und ausgeführt werden.

-   [Schritt 4: Testen Ihrer UE-v 2-Evaluierungsbereitstellung](#step4): führen Sie einige Tests auf zwei Computern durch, auf denen der UE-v-Agent installiert ist, und sehen Sie, wie UE-v funktioniert.

Das wars! Nachdem Sie die Schritte ausgeführt haben, können Sie bewerten, wie UE-V in Ihrem Unternehmen funktionieren kann.

**Weitere Auswertung:** Sie können auch zusätzliche Schritte ausführen, um einige Drittanbieter-und Branchenanwendungen so zu konfigurieren, dass Ihre Einstellungen mithilfe von UE-v wie in [Bereitstellen von UE-v 2. x für benutzerdefinierte Anwendungen](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)synchronisiert werden.

## <a href="" id="step1"></a>Schritt 1: Voraussetzungen bestätigen


Bevor Sie fortfahren, stellen Sie sicher, dass Ihre Umgebung die folgenden Voraussetzungen für die Ausführung von UE-V umfasst.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Betriebssystem</strong></th>
<th align="left"><strong>Edition</strong></th>
<th align="left"><strong>Service Pack</strong></th>
<th align="left"><strong>System Architektur</strong></th>
<th align="left"><strong>Windows PowerShell</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Ultimate-, Enterprise-oder Professional-Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 oder höher</p></td>
<td align="left"><p>.NET Framework 4 oder höher</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter oder Web Server</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 oder höher</p></td>
<td align="left"><p>.NET Framework 4 oder höher</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows8.1</p></td>
<td align="left"><p>Enterprise oder pro</p></td>
<td align="left"><p>Keine</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 oder höher</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 oder Windows Server 2012 R2</p></td>
<td align="left"><p>Standard oder Rechenzentrum</p></td>
<td align="left"><p>Keine</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 oder höher</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 10, Pre-1607 Version</p></td>
<td align="left"><p>Enterprise oder pro</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 oder höher</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>Standard oder Rechenzentrum</p></td>
<td align="left"><p>Keine</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 oder höher</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
</tbody>
</table>

**Hinweis:** Ab Windows 10, Version 1607, ist UE-V in [Windows 10 für Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) enthalten und nicht mehr Teil des Microsoft-Desktop Optimierungs Pakets.

Auch...

-   **MDOP-Lizenz:** Diese Technologie ist Teil des Microsoft Desktop Optimization Pack (MDOP). Unternehmenskunden können MDOP mit Microsoft Software Assurance erhalten. Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter wie erhalte ich MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   **Administratoranmeldeinformationen** für jeden Computer, auf dem die Installation erfolgen soll

## <a href="" id="step2"></a>Schritt 2: Bereitstellen des Speicherorts für Einstellungen für UE-V 2


Sie müssen einen Speicherort für Einstellungen bereitstellen, eine standardmäßige Netzwerkfreigabe, auf der Benutzereinstellungen in einer Einstellungspaket Datei gespeichert werden. Wenn Sie die Speicherfreigabe für Einstellungen erstellen, sollten Sie den Zugriff auf Benutzer einschränken, für die Sie erforderlich sind. [Bereitstellen eines Einstellungsspeicher Orts](https://technet.microsoft.com/library/dn458891.aspx#ssl) bietet ausführlichere Informationen.

**Erstellen einer Netzwerkfreigabe**

1.  Erstellen Sie eine neue Sicherheitsgruppe, und fügen Sie Ihr UE-V-Benutzer hinzu.

2.  Erstellen Sie einen neuen Ordner auf dem zentral gelegenen Computer, auf dem die UE-v-Einstellungs Pakete gespeichert sind, und gewähren Sie dem UE-v-Benutzer Zugriff mit Gruppen Berechtigungen für den Ordner. Der Administrator, der UE-V unterstützt, muss über Berechtigungen für diesen freigegebenen Ordner verfügen.

3.  Zuweisen von Berechtigungen für UE-V-Benutzer zum Erstellen eines Verzeichnisses, wenn Sie eine Verbindung herstellen. Erteilen Sie allen Unterverzeichnissen dieses Verzeichnisses die vollständige Berechtigung, aber blockieren Sie den Zugriff auf etwas darüber.

    1.  Legen Sie die folgenden SMB-Berechtigungen (Share-Level-Server-Nachrichten Block) für den Ordner "Settings-Speicherort" ein.

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong>Benutzerkonto</strong></th>
        <th align="left"><strong>Empfohlene Berechtigungen</strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>Jeder</p></td>
        <td align="left"><p>Keine Berechtigungen</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>Sicherheitsgruppe der UE-V-Benutzer</p></td>
        <td align="left"><p>Vollzugriff</p></td>
        </tr>
        </tbody>
        </table>

         

    2.  Legen Sie die folgenden NTFS-Dateisystemberechtigungen für den Ordner "Settings Storage Location" ein.

        <table>
        <colgroup>
        <col width="33%" />
        <col width="33%" />
        <col width="33%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong>Benutzerkonto</strong></th>
        <th align="left"><strong>Empfohlene Berechtigungen</strong></th>
        <th align="left"><strong>Ordner</strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>Ersteller/Besitzer</p></td>
        <td align="left"><p>Vollzugriff</p></td>
        <td align="left"><p>Nur Unterordner und Dateien</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>Sicherheitsgruppe der UE-V-Benutzer</p></td>
        <td align="left"><p>Ordner auflisten/Daten lesen, Ordner erstellen/Daten anfügen</p></td>
        <td align="left"><p>Nur diesen Ordner</p></td>
        </tr>
        </tbody>
        </table>

         

**Sicherheitshinweis:**

Wenn Sie die Speicherfreigabe für Einstellungen auf einem Computer erstellen, auf dem ein Windows Server-Betriebssystem ausgeführt wird, konfigurieren Sie UE-V, um zu überprüfen, ob die lokale Gruppe Administratoren oder der aktuelle Benutzer der Besitzer des Ordners ist, in dem die Einstellungs Pakete gespeichert sind. Um diese zusätzliche Sicherheit zu aktivieren, geben Sie diese Einstellung im Windows Server-Registrierungs-Editor an:

1.  Fügen Sie einen Registrierungsschlüssel " **reg \ _DWORD** " mit dem Namen **"RepositoryOwnerCheckEnabled"** zu **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.

2.  Stellen Sie den Wert für den Registrierungsschlüssel auf *1 ein*.

## <a href="" id="step3"></a>Schritt 3: Bereitstellen des UE-V 2-Agents


Der UE-V-Agent synchronisiert die Anwendungs-und Windows-Einstellungen zwischen den Computern und Geräten der Benutzer. Installieren Sie den Agenten zu Evaluierungszwecken auf mindestens zwei Computern in Ihrer Testumgebung, die demselben Benutzer gehören.

Führen Sie die AgentSetup.exe-Datei über die Befehlszeile aus, um den UE-V-Agent zu installieren. Sie wird sowohl auf 32-Bit-als auch 64-Bit-Betriebssystemen installiert.

``` syntax
AgentSetup.exe SettingsStoragePath=\\server\settingsshare\%username%
```

Sie müssen den SettingsStoragePath-Befehlszeilenparameter als Netzwerkfreigabe aus Schritt 2 angeben. [Bereitstellen eines UE-V-Agents](https://technet.microsoft.com/library/dn458891.aspx#agent) bietet ausführlichere Informationen.

## <a href="" id="step4"></a>Schritt 4: Testen Ihrer UE-V 2-Evaluierungsbereitstellung


Sie können jetzt einige Tests für Ihre UE-v-Evaluierungsbereitstellung ausführen, um zu sehen, wie UE-v funktioniert.

****

1.  Führen Sie auf dem ersten Computer (Computer A) eine oder mehrere der folgenden Änderungen aus:

    1.  Öffnen Sie den Windows-Desktop, und verschieben Sie die Taskleiste an eine andere Position im Fenster.

    2.  Ändern Sie die Standardschriftarten.

    3.  Öffnen Sie Calculator, und setzen Sie den Wert auf **Scientific**.

    4.  Ändern Sie das Verhalten einer beliebigen Windows-APP, wie in Verwalten von Einstellungen für den [Standort "UE-V 2. x" mithilfe von Windows PowerShell und WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)erläutert.

    5.  Deaktivieren Sie die Einstellungen für die Synchronisierung und das Roaming von Microsoft-Konten.

2.  Abmelden Computer a. die Einstellungen werden in einem UE-V-Einstellungspaket gespeichert, wenn Benutzer eine Anwendung sperren, abmelden, beenden oder wenn der Synchronisierungsanbieter ausgeführt wird (standardmäßig alle 30 Minuten).

3.  Melden Sie sich beim zweiten Computer (Computer B) als derselbe Benutzer wie Computer A an.

4.  Öffnen Sie den Windows-Desktop, und überprüfen Sie, ob der Speicherort der Taskleiste mit dem von Computer A übereinstimmt. Überprüfen Sie, ob die Standardschriftarten übereinstimmen und dieser Rechner auf **Scientific**festgesetzt ist. Überprüfen Sie auch die Änderung, die Sie an einer beliebigen Windows-App vorgenommen haben.

Sie können die Einstellungen auf dem Computer B wieder auf den ursprünglichen Computer ändern. Melden Sie sich dann bei Computer B ab, und melden Sie sich bei Computer a an, um die Änderungen zu überprüfen.

## Weitere Ressourcen für dieses Produkt


-   [Microsoft User Experience Virtualization (UE-V) 2. x](index.md)

-   [Vorbereiten einer UE-V 2. x-Bereitstellung](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Verwalten von UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Problembehandlung bei UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Technische Referenz für UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





