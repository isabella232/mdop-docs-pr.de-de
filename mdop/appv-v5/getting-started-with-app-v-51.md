---
title: Erste Schritte mit App-V 5.1
description: Erste Schritte mit App-V 5.1
author: dansimp
ms.assetid: 49a20e1f-0566-4e53-a417-1521393fc974
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff10f12bc672a24f2837f50bfb1f0033ede3e46f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805810"
---
# Erste Schritte mit App-V 5.1


Microsoft Application Virtualization (App-V) 5,1 ermöglicht Administratoren die Bereitstellung, Aktualisierung und Unterstützung von Anwendungen als Dienste in Echtzeit – bedarfsbasiert. Einzelne Anwendungen werden von lokal installierten Produkten in Zentral verwaltete Dienste transformiert und sind überall verfügbar, ohne Computer vorkonfigurieren oder Betriebssystemeinstellungen ändern zu müssen.

App-V umfasst die folgenden Elemente:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Element</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V-Verwaltungs Server</p></td>
<td align="left"><ul>
<li><p>Bietet einen zentralen Speicherort für die Verwaltung der APP-v-Infrastruktur, die virtuelle Anwendungen sowohl für den App-v-Desktop Client als auch für den Remote Desktop Dienste-Client (ehemals Terminal Dienste) bereitstellt.</p></li>
<li><p>Verwendet Microsoft SQL Server® für seinen Datenspeicher, in dem mindestens ein App-V-Verwaltungsserver einen einzelnen SQL Server-Datenspeicher freigeben kann.</p></li>
<li><p>Authentifiziert Anforderungen und bietet Sicherheit, Dosierung, Überwachung und Datenerfassung. Der Server verwendet Active Directory und unterstützende Tools zum Verwalten von Benutzern und Anwendungen.</p></li>
<li><p>Verfügt über eine Verwaltungswebsite, über die Sie die App-V-Infrastruktur von einem beliebigen Computer aus konfigurieren können. Sie können Anwendungen hinzufügen und entfernen, Tastenkombinationen bearbeiten, Benutzern und Gruppen Zugriffsberechtigungen zuweisen und Verbindungsgruppen erstellen.</p></li>
<li><p>Ermöglicht die Kommunikation zwischen der App-V Web Management Console und dem SQL Server-Datenspeicher. Diese Komponenten können je nach erforderlicher Systemarchitektur auf einem einzelnen Server Computer oder auf einem oder mehreren separaten Computern installiert werden.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>App-V-Veröffentlichungs Server</p></td>
<td align="left"><ul>
<li><p>Bietet App-V-Clients mit berechtigten Anwendungen für den jeweiligen Benutzer</p></li>
<li><p>Hostet das virtuelle Anwendungspaket für Streaming.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V-Desktop Client</p></td>
<td align="left"><ul>
<li><p>Ruft virtuelle Anwendungen ab</p></li>
<li><p>Veröffentlicht die Anwendungen auf den Clients</p></li>
<li><p>Richtet virtuelle Umgebungen zur Laufzeit automatisch auf Windows-Endpunkten ein und verwaltet Sie.</p></li>
<li><p>Speichert benutzerspezifische Einstellungen für virtuelle Anwendungen wie Registrierungs-und Dateiänderungen in den Profilen jedes Benutzers&#39;s.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>App-V Remote Desktop Dienste (RDS)-Client</p></td>
<td align="left"><p>Ermöglicht es Remote Desktop-Sitzungs Host Servern, die Funktionen des App-V-Desktop Clients für freigegebene Desktopsitzungen zu verwenden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V-Sequenzer</p></td>
<td align="left"><ul>
<li><p>Ist ein auf Assistenten basierendes Tool, mit dem Sie herkömmliche Anwendungen in virtuelle Anwendungen umwandeln können.</p></li>
<li><p>Erstellt die Anwendung "Package", die sich aus:</p>
<ol>
<li><p>eine sequenzierte Anwendungsdatei (APPV)</p></li>
<li><p>eine Windows Installer-Datei (MSI), die für Clients bereitgestellt werden kann, die für eigenständigen Betrieb konfiguriert sind</p></li>
<li><p>Mehrere XML-Dateien, einschließlich Report.XML, PackageName_DeploymentConfig.XML und PackageName_UserConfig.XML. Die XML-Dateien userconfig und DeploymentConfig werden verwendet, um benutzerdefinierte Änderungen am Standardverhalten des Pakets zu konfigurieren.</p></li>
</ol></li>
</ul></td>
</tr>
</tbody>
</table>

 

Weitere Informationen zu diesen Elementen finden Sie unter [hochstufige Architektur für App-V 5,1](high-level-architecture-for-app-v-51.md).

Wenn Sie mit diesem Produkt noch nicht vertraut sind, empfehlen wir Ihnen, die Dokumentation gründlich zu lesen. Bevor Sie die Anwendung in einer Produktionsumgebung bereitstellen, empfehlen wir auch, den Bereitstellungsplan in einer Testnetzwerkumgebung zu überprüfen. Sie können auch erwägen, eine Klasse über relevante Technologien zu Unternehmen. Weitere Informationen zu Microsoft-Schulungsmöglichkeiten finden Sie in der Microsoft-Schulungsübersicht unter <https://go.microsoft.com/fwlink/p/?LinkId=80347> .

**Hinweis**  Eine herunterladbare Version des Administratorhandbuchs steht nicht zur Verfügung. Sie können sich jedoch mit einem speziellen Modus der TechNet-Bibliothek vertraut machen, der es Ihnen ermöglicht, Artikel auszuwählen, Sie in einer Sammlung zu gruppieren, zu drucken oder in eine Datei unter (zu exportieren <https://go.microsoft.com/fwlink/?LinkId=272491> https://go.microsoft.com/fwlink/?LinkId=272491) .

 

Dieser Abschnitt des App-v 5,1-Administrator Handbuchs enthält allgemeine Informationen zu app-v 5,1, um Ihnen ein grundlegendes Verständnis des Produkts zu vermitteln, bevor Sie mit der Bereitstellungsplanung beginnen.

## Erste Schritte mit App-V 5,1


-   [Informationen zu App-V 5.1](about-app-v-51.md)

    Bietet eine allgemeine Übersicht über App-V 5,1 und die Art und Weise, wie Sie in Ihrer Organisation verwendet werden kann.

-   [Evaluieren von App-V 5.1](evaluating-app-v-51.md)

    Bietet Informationen dazu, wie Sie App-V 5,1 für die Verwendung in Ihrer Organisation am besten auswerten können.

-   [High-Level-Architektur für App-V 5.1](high-level-architecture-for-app-v-51.md)

    Enthält eine Beschreibung der App-V 5,1-Features und ihrer Zusammenarbeit.

-   [Barrierefreiheit von App-V 5.1](accessibility-for-app-v-51.md)

    Bietet Informationen zu Features und Diensten, mit denen dieses Produkt und die zugehörige Dokumentation für Personen mit Behinderungen barrierefreier sind.

## <a href="" id="other-resources-for-this-product-"></a>Weitere Ressourcen für dieses Produkt


-   [Microsoft Application Virtualization 5,1-Administrator Handbuch](microsoft-application-virtualization-51-administrators-guide.md)

-   [Planen von App-V 5.1](planning-for-app-v-51.md)

-   [Bereitstellen von App-V 5.1](deploying-app-v-51.md)

-   [Vorgänge für App-V 5.1](operations-for-app-v-51.md)

-   [Problembehandlung bei App-V 5.1](troubleshooting-app-v-51.md)

-   [Technische Referenz zu App-V 5.1](technical-reference-for-app-v-51.md)






 

 





