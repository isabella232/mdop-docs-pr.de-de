---
title: Vorbereiten der Umgebung für UE-V
description: Vorbereiten der Umgebung für UE-V
author: dansimp
ms.assetid: c93d3b33-e032-451a-9e1b-8534e1625396
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8f806f3c326bad5204a7f1ee69e11b61177e3cce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810681"
---
# Vorbereiten der Umgebung für UE-V


Microsoft User Experience Virtualization (UE-V) durchstreift die Einstellungen zwischen Computern durch die Verwendung eines Einstellungsspeicher Orts. Der Speicherort der Einstellungen ist eine Dateifreigabe und sollte während der Bereitstellung des UE-V-Agents konfiguriert werden. Sie muss entweder als Speicherort für Einstellungen oder als Active Directory-Basisverzeichnis definiert werden. Darüber hinaus sollte der Administrator einen Zeitserver konfigurieren, um eine konsistente Synchronisierung zu unterstützen. Wenn Sie Ihre Umgebung für UE-V vorbereiten möchten, sollten Sie Folgendes berücksichtigen:

-   [Speicher für UE-V-Einstellungen](#bkmk-uevsettingsstorage):

    -   [Definieren eines Speicherorts für Einstellungen](#bkmk-definingsettingsstoragelocation)

    -   [Verwenden des Active Directory-Basisverzeichnisses mit UE-V](#bkmk-usingactivedirectoryhomedirectory)

-   [Synchronisieren von Computer Uhren für die Synchronisierung von UE-V-Einstellungen](#bkmk-synchronizecomputerclocks)

-   [Leistungs-und Kapazitätsplanung](#bkmk-performancecapacityplanning)

Weitere Informationen zu den Anforderungen an das Betriebssystem und den Computer finden Sie unter [unterstützte Konfigurationen für UE-V 1,0](supported-configurations-for-ue-v-10.md).

## <a href="" id="bkmk-uevsettingsstorage"></a>Speicher für UE-V-Einstellungen


Sie können den Speicher der Benutzeroberflächen-Virtualisierungs-Einstellungen in einer von zwei Konfigurationen definieren: einem Einstellungs Speicherort oder einem Active Directory-Basisverzeichnis.

### <a href="" id="bkmk-definingsettingsstoragelocation"></a>Definieren eines Speicherorts für Einstellungen

Der Speicherort der UE-v-Einstellungen ist eine standardmäßige Netzwerkfreigabe, auf die UE-v-Benutzer zugreifen können. Vor dem Definieren des Speicherorts für Einstellungen müssen Sie ein Stammverzeichnis erstellen. Benutzer, die Einstellungen für die Freigabe speichern, müssen über Lese-/Schreibzugriff für den Speicherort verfügen. Der UE-V-Agent erstellt benutzerspezifische Ordner unter diesem Stammverzeichnis. Der Speicherort des Einstellungs Speichers wird durch Festlegen der **SettingsStoragePath** -Konfigurationsoption definiert. Diese Option kann wie folgt konfiguriert werden:

-   Während der Installation des UE-V-Agents über einen Befehlszeilenparameter oder in einem Batchskript.

-   Verwenden von Gruppenrichtlinien

-   Nach der Installation mithilfe von PowerShell oder WMI.

Der Pfad muss sich im UNC-Pfad (Universal Naming Convention) des Servers und der Freigabe befinden. Beispiel: **\\\\server\\settingsshare\\**. Diese Konfigurationsoption unterstützt die Verwendung von Variablen, um bestimmte Roaming-Szenarien zu ermöglichen.

Sie können die `%username%` Variable mit dem UNC-Pfad des Servers und der Freigabe verwenden. Dadurch werden die gleichen Einstellungen für alle Computer oder Sitzungen bereitgestellt, bei denen sich ein Benutzer anmeldet. Bedenken Sie diese Konfiguration für die folgenden Szenarien:

1.  Benutzer im Unternehmen verfügen über mehrere, ähnlich konfigurierte physische Computer, und die Einstellungen jedes Benutzers sollten auf allen Computern gleich sein.

2.  Benutzer im Unternehmen verwenden VPN-Pools (Virtual Desktop Infrastructure), in denen die Einstellungen für die VDI-Sitzungen jedes Benutzers beibehalten werden sollen.

3.  Benutzer im Unternehmen verfügen über einen physikalischen Computer und verwenden zusätzlich eine VDI. Die Einstellungen der einzelnen Benutzer sollten unabhängig davon sein, ob Sie den physikalischen Computer oder die VDI-Sitzung verwenden.

4.  Mehrere Enterprise-Computer werden von mehreren Benutzern verwendet. Die Einstellungen des jeweiligen Benutzers sollten auf allen Computern gleich sein.

Sie können die **%username%\\%Computername%** -Variablen mit dem UNC-Pfad des Servers und der Freigabe verwenden. Dadurch bleibt die Einstellungen für die einzelnen Computer erhalten. Bedenken Sie diese Konfiguration für die folgenden Szenarien:

1.  Benutzer im Unternehmen verfügen über mehrere physische Computer, und Sie möchten die Einstellungen für die einzelnen Computer beibehalten.

2.  Die Enterprise-Computer werden von mehreren Benutzern verwendet. Die Einstellungen sollten für jeden Computer beibehalten werden, in dem sich der Benutzer anmeldet.

Der UE-v-Agent erstellt dynamisch den benutzerspezifischen Einstellungsspeicher Pfad basierend auf einer UE-v- `SettingsStoragePath` Konfigurationseinstellung und den definierten Variablen.

Der UE-V-Agent erstellt dynamisch einen versteckten Systemordner `SettingsPackages` , der innerhalb jedes benutzerspezifischen Speicherorts benannt ist. Der UE-v-Agent liest und schreibt Einstellungen an diesen Speicherort, wie Sie von den registrierten UE-v-Einstellungen für Standort Vorlagen definiert werden.

Wenn der Speicherort der Einstellungen für einen Satz verwalteter Computer eines Benutzers identisch ist, werden die entsprechenden UE-V-Einstellungen durch die Regel "letzte Write WINS" bestimmt. Der Agent, der auf einem Computer ausgeführt wird, liest und schreibt unabhängig von Agents, die auf anderen Computern ausgeführt werden, an den Speicherort der Einstellungen. Die zuletzt geschriebenen Einstellungen und Werte sind die Einstellungen, die angewendet werden, wenn der nächste Agent vom Speicherort für Einstellungen liest. Weitere Informationen finden Sie unter [Bereitstellen des Speicherorts für Einstellungen für UE-V 1,0](deploying-the-settings-storage-location-for-ue-v-10.md).

### <a href="" id="bkmk-usingactivedirectoryhomedirectory"></a>Verwenden des Active Directory-Basisverzeichnisses mit UE-V

Wenn für UE-V kein Speicherplatz für Einstellungen konfiguriert ist, wenn der Agent bereitgestellt wird, wird das Active Directory-Basisverzeichnis (AD) des Benutzers zum Speichern von Einstellungen für Standort Pakete verwendet. Der UE-V-Agent erstellt dynamisch den Einstellungsspeicher Ordner unter dem Stammverzeichnis des AD Home-Verzeichnisses jedes Benutzers. Der Agent verwendet nur das Active Directory-Basisverzeichnis, wenn ein Settings-Speicherort (SettingsStoragePath) nicht anderweitig definiert ist.

## <a href="" id="bkmk-synchronizecomputerclocks"></a>Synchronisieren von Computeruhren für die Synchronisierung von UE-V-Einstellungen


Computer, auf denen der UE-V-Agent zum Synchronisieren von Einstellungen ausgeführt wird, müssen einen Zeitserver verwenden. Zeitstempel werden verwendet, um festzustellen, ob die Einstellungen vom Speicherort der Einstellungen synchronisiert werden müssen. Wenn die Uhrzeit des Computers falsch ist, können ältere Einstellungen neuere Einstellungen überschreiben, oder die neuen Einstellungen werden möglicherweise nicht am Speicherort des Einstellungs Speichers gespeichert. Die Verwendung eines Zeitservers ermöglicht es UE-V, eine konsistente Einstellungen zu gewährleisten.

## <a href="" id="bkmk-performancecapacityplanning"></a>Leistungs-und Kapazitätsplanung


Die Kapazitätsanforderungen für UE-V können mithilfe der standardmäßigen Festplattenkapazität und der Netzwerkstatusüberwachung bestimmt werden. UE-V verwendet eine SMB-Freigabe (Server Message Block) für die Speicherung von Einstellungspaketen. Die Größe der Einstellungs Pakete variiert je nach den Einstellungsinformationen für eine bestimmte Anwendung. Während die meisten Einstellungs Pakete klein sind, kann die Synchronisierung von potenziell umfangreichen Dateien, wie etwa Desktop Bildern, zu einer schlechten Leistung führen, insbesondere bei langsameren Netzwerken. Um Probleme mit der Netzwerklatenz zu minimieren, sollten Sie die Speicherorte für Einstellungen in denselben lokalen Netzwerken erstellen, in denen sich die Computer der Benutzer befinden.

Standardmäßig wird die UE-V-Synchronisierung nach 2 Sekunden ablaufen, wenn das Netzwerk langsam ist oder das Einstellungspaket groß ist. Sie können das Timeout mit Gruppenrichtlinien konfigurieren. Weitere Informationen zum Festlegen des Timeouts finden Sie unter [Konfigurieren von UE-V mit Gruppenrichtlinienobjekten](configuring-ue-v-with-group-policy-objects.md).

## Verwandte Themen


[Microsoft-User Experience Virtualization (UE-V) 1.0](index.md)

[Planen für UE-V 1.0](planning-for-ue-v-10.md)

[Unterstützte Konfigurationen für UE-V 1.0](supported-configurations-for-ue-v-10.md)

 

 





