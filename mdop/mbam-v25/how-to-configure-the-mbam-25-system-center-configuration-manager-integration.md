---
title: So konfigurieren Sie die Integration von MBAM 2.5 in System Center Configuration Manager
description: So konfigurieren Sie die Integration von MBAM 2.5 in System Center Configuration Manager
author: dansimp
ms.assetid: 2b8a4c13-1dad-41e8-89ac-6889c5f7e051
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c6fb0a0b06399baf1dc6493a40d17e76a51741f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804232"
---
# So konfigurieren Sie die Integration von MBAM 2.5 in System Center Configuration Manager


In diesem Thema wird erläutert, wie Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) für die Verwendung der System Center Configuration Manager-Integrations Topologie konfigurieren, die MBAM mit Configuration Manager integriert.

In den Anweisungen wird erläutert, wie Sie die Configuration Manager-Integration mit folgenden Schritten konfigurieren:

-   Ein Windows PowerShell-Cmdlet

-   Der Serverkonfigurations-Assistent von MBAM

Die Anweisungen basieren auf der empfohlenen Architektur in der [Architektur auf hoher Ebene für MBAM 2,5](high-level-architecture-for-mbam-25.md).

**Bevor Sie die Konfiguration starten:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schritt</th>
<th align="left">Wo erhalte ich Anweisungen?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Überprüfen Sie die empfohlene Architektur für MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md" data-raw-source="[High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)">High-Level-Architektur von MBAM 2.5 mit Configuration Manager-Integrationstopologie</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Überprüfen Sie die unterstützten Konfigurationen für MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Von MBAM 2.5 unterstützte Konfigurationen</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Führen Sie die erforderlichen Voraussetzungen für jeden Server aus.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Bei dieser Topologie müssen Sie die Configuration Manager-Konsole auf dem Computer installieren, auf dem Sie die MBAM-Server Software installieren.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installieren der MBAM 2.5-Serversoftware</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Überprüfen Sie die Voraussetzungen für Windows PowerShell (nur anwendbar, wenn Sie Windows PowerShell-Cmdlets zum Konfigurieren von MBAM verwenden möchten).</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**So konfigurieren Sie die Integration von Configuration Manager mithilfe von Windows PowerShell**

1.  Bevor Sie die Konfiguration starten, lesen Sie [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) zum Überprüfen der Voraussetzungen für die Verwendung von Windows PowerShell.

2.  Verwenden Sie das Windows PowerShell **-Cmdlet Enable-MbamCMIntegration** , um die Berichte zu konfigurieren. Um Informationen zu diesem Cmdlet abzurufen, geben **Sie Get-Help enable-MbamCMIntegration**ein.

**So konfigurieren Sie die Integration von System Center Configuration Manager mithilfe des Assistenten**

1.  Starten Sie auf dem Server, auf dem Sie das System Center Configuration Manager-Integrations Feature konfigurieren möchten, den MBAM-Serverkonfigurations-Assistenten. Sie können **MBAM Server Configuration** im **Startmenü** auswählen, um den Assistenten zu öffnen.

2.  Klicken Sie auf **neue Features hinzufügen**, wählen Sie **System Center Configuration Manager-Integration**aus, und klicken Sie dann auf **weiter**.

    Der Assistent überprüft, ob alle Voraussetzungen für die Integration von Configuration Manager erfüllt sind.

3.  Wenn die Voraussetzungsprüfung erfolgreich ist, klicken Sie auf **weiter** , um fortzufahren. Beheben Sie andernfalls alle fehlenden Voraussetzungen, und klicken Sie dann **erneut auf Voraussetzungen prüfen**.

4.  Verwenden Sie die folgenden Beschreibungen, um die Feldwerte im Assistenten einzugeben:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Feld</th>
    <th align="left">Beschreibung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>SQL Server Reporting Services-Server</strong></p></td>
    <td align="left"><p>Vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Servers mit der Rolle des Berichterstattungsdienst Punkts. Dies ist der Server, auf dem die MBAM Configuration Manager-Berichte bereitgestellt werden.</p>
    <p>Wenn Sie keinen Server angeben, werden die Configuration Manager-Berichte auf dem lokalen Server bereitgestellt.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>SQL Server Reporting Services-Instanz</strong></p></td>
    <td align="left"><p>Der Name der SQL Server Reporting Services (SSRS)-Instanz, in der die Configuration Manager-Berichte bereitgestellt werden.</p>
    <p>Wenn Sie keine Instanz angeben, werden die Configuration Manager-Berichte im standardmäßigen SSRS-Instanzennamen bereitgestellt. Der eingegebene Wert wird ignoriert, wenn auf dem Server der System Center 2012-Konfigurations-Manager installiert ist.</p></td>
    </tr>
    </tbody>
    </table>



5.  Überprüfen Sie auf der Seite **Zusammenfassung** die Features, die hinzugefügt werden sollen.

    **Hinweis:**  
    Wenn Sie ein Windows PowerShell-Skript der soeben erstellten Einträge erstellen möchten, klicken Sie auf **PowerShell-Skript exportieren** , und speichern Sie das Skript.



6.  Klicken Sie auf **Hinzufügen** , um dem Server das Configuration Manager-Integrations Feature hinzuzufügen, und klicken Sie dann auf **Schließen**.



## Verwandte Themen


[Konfigurieren der MBAM 2.5-Serverfunktionen](configuring-the-mbam-25-server-features.md)

[Überprüfen der Konfiguration von MBAM 2.5 Serverfunktionen](validating-the-mbam-25-server-feature-configuration.md)


## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






