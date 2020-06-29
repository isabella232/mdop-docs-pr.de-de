---
title: Erste Schritte mit App-V 5.0
description: Erste Schritte mit App-V 5.0
author: dansimp
ms.assetid: 3e16eafb-ce95-4d06-b214-fe0f4b1b495f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a7979c81b7b57107f824b96d9fef8049a00c5b08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805813"
---
# Erste Schritte mit App-V 5.0


App-V 5,0 ermöglicht Administratoren das bereitstellen, aktualisieren und unterstützen von Anwendungen als Dienste in Echtzeit – bedarfsbasiert. Einzelne Anwendungen werden von lokal installierten Produkten in Zentral verwaltete Dienste transformiert und sind überall verfügbar, ohne Computer vorkonfigurieren oder Betriebssystemeinstellungen ändern zu müssen.

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
<li><p>Verfügt über eine auf Silverlight® basierende Verwaltungswebsite, über die Sie die App-V-Infrastruktur von einem beliebigen Computer aus konfigurieren können. Sie können Anwendungen hinzufügen und entfernen, Tastenkombinationen bearbeiten, Benutzern und Gruppen Zugriffsberechtigungen zuweisen und Verbindungsgruppen erstellen.</p></li>
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

 

Weitere Informationen zu diesen Elementen finden Sie unter [hochstufige Architektur für App-V 5,0](high-level-architecture-for-app-v-50.md).

Wenn Sie mit diesem Produkt noch nicht vertraut sind, empfehlen wir Ihnen, die Dokumentation gründlich zu lesen. Bevor Sie die Anwendung in einer Produktionsumgebung bereitstellen, empfehlen wir auch, den Bereitstellungsplan in einer Testnetzwerkumgebung zu überprüfen. Sie können auch erwägen, eine Klasse über relevante Technologien zu Unternehmen. Weitere Informationen zu Microsoft-Schulungsmöglichkeiten finden Sie in der Microsoft-Schulungsübersicht unter <https://go.microsoft.com/fwlink/p/?LinkId=80347> .

**Hinweis**  Eine herunterladbare Version des Administratorhandbuchs steht nicht zur Verfügung. Sie können sich jedoch mit einem speziellen Modus der TechNet-Bibliothek vertraut machen, der es Ihnen ermöglicht, Artikel auszuwählen, Sie in einer Sammlung zu gruppieren, zu drucken oder in eine Datei unter (zu exportieren <https://go.microsoft.com/fwlink/?LinkId=272491> https://go.microsoft.com/fwlink/?LinkId=272491) .

 

Dieser Abschnitt des App-v 5,0-Administrator Handbuchs enthält allgemeine Informationen zu app-v 5,0, um Ihnen ein grundlegendes Verständnis des Produkts zu vermitteln, bevor Sie mit der Bereitstellungsplanung beginnen.

## Erste Schritte mit App-V 5,0


-   [Informationen zu App-V 5.0](about-app-v-50.md)

    Bietet eine allgemeine Übersicht über App-V 5,0 und die Art und Weise, wie Sie in Ihrer Organisation verwendet werden kann.

-   [Informationen zu App-V 5.0 SP1](about-app-v-50-sp1.md)

    Bietet eine allgemeine Übersicht über App-V 5.0 SP1 und die Art und Weise, wie Sie in Ihrer Organisation verwendet werden kann.

-   [Informationen zu App-V 5.0 SP2](about-app-v-50-sp2.md)

    Bietet eine allgemeine Übersicht über App-V 5.0 SP2 und die Art und Weise, wie Sie in Ihrer Organisation verwendet werden kann.

-   [Informationen zu App-V 5.0 SP3](about-app-v-50-sp3.md)

    Bietet eine allgemeine Übersicht über App-V 5.0 SP2 und die Art und Weise, wie Sie in Ihrer Organisation verwendet werden kann.

-   [Evaluieren von App-V 5.0](evaluating-app-v-50.md)

    Bietet Informationen dazu, wie Sie App-V 5,0 für die Verwendung in Ihrer Organisation am besten auswerten können.

-   [High-Level-Architektur für App-V 5.0](high-level-architecture-for-app-v-50.md)

    Enthält eine Beschreibung der App-V 5,0-Features und ihrer Zusammenarbeit.

-   [Barrierefreiheit von App-V 5.0](accessibility-for-app-v-50.md)

    Bietet Informationen zu Features und Diensten, mit denen dieses Produkt und die zugehörige Dokumentation für Personen mit Behinderungen barrierefreier sind.

## <a href="" id="other-resources-for-this-product-"></a>Weitere Ressourcen für dieses Produkt


-   [Microsoft Application Virtualization 5,0-Administrator Handbuch](microsoft-application-virtualization-50-administrators-guide.md)

-   [Planen für App-V 5.0](planning-for-app-v-50-rc.md)

-   [Bereitstellen von App-V 5.0](deploying-app-v-50.md)

-   [Vorgänge für App-V 5.0](operations-for-app-v-50.md)

-   [Problembehandlung bei App-V 5.0](troubleshooting-app-v-50.md)






 

 





