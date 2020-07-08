---
title: Konfigurieren der Installationsvoraussetzungen
description: Konfigurieren der Installationsvoraussetzungen
author: dansimp
ms.assetid: ff9cf28a-3eac-4b6c-8ce9-bfc202f57947
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6cd9379804c45a2025064a6eecf363c010980369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807855"
---
# Konfigurieren der Installationsvoraussetzungen


Die folgenden Anweisungen sind Voraussetzungen für die Installation und Verwendung von Microsoft Enterprise Desktop Virtualization (MED-V) 2,0:

[Windows Virtual PC](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7)

[Windows Virtual PC-Aktualisierung](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update)

[Antivirus/Backup Software-Konfiguration](#bkmk-antivirusbackupsoftwareconfiguration)

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7"></a>Installieren und Konfigurieren von Windows Virtual PC


**Wichtig**  Wenn bereits eine Version von Virtual PC für Windows auf dem Hostcomputer vorhanden ist, müssen Sie Sie deinstallieren, bevor Sie Windows Virtual PC installieren.

 

**So installieren Sie Windows Virtual PC**

1.  Laden Sie [Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=195918) aus dem Microsoft Download Center herunter ( https://go.microsoft.com/fwlink/?LinkId=195918) .

2.  Führen Sie die Installationsdatei auf dem Hostcomputer aus, und führen Sie die Schritte im Assistenten aus.

**Wichtig**  Windows Virtual PC enthält das Integrationskomponentenpaket, das Features bereitstellt, die die Interaktion zwischen der virtuellen Umgebung und dem physikalischen Computer verbessern. So können Sie beispielsweise die Maus zwischen dem Host und den Gastcomputern bewegen. Für MED-V ist die Installation des Integrationskomponentenpakets erforderlich.

 

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update"></a>Installieren und Konfigurieren des Windows Virtual PC-Updates


Das Microsoft-Update, das dem Artikel KB977206 zugeordnet ist, aktiviert den Windows XP-Modus für Computer ohne Hardware unterstützte Virtualisierungs-Technologie (HAV). Wir empfehlen, dieses Update zu installieren, da einige Integrationsfeatures möglicherweise nicht ordnungsgemäß funktionieren, wenn das Integrationskomponentenpaket im Gastbetriebssystem nicht mit der Version von Windows Virtual PC übereinstimmt, die auf dem Hostcomputer installiert ist.

**Wichtig**  Sie müssen dieses Update nicht installieren, wenn Sie MED-V auf Hostcomputern installieren, auf denen Windows 7 mit Service Pack 1 ausgeführt wird.

 

**Tipp**  Neben dem hier aufgelisteten Update empfehlen wir, dass Sie alle verfügbaren Windows Virtual PC-Updates überprüfen und diese Updates anwenden, die für Ihre Umgebung geeignet oder erforderlich sind.

 

**So installieren Sie das Windows Virtual PC-Update**

1.  Laden Sie das erforderliche Windows Virtual PC-Update aus dem Microsoft Download Center herunter.

    [32-Bit-Update](https://go.microsoft.com/fwlink/?LinkId=195919) ( https://go.microsoft.com/fwlink/?LinkId=195919) .

    [64-Bit-Update](https://go.microsoft.com/fwlink/?LinkId=195920) ( https://go.microsoft.com/fwlink/?LinkId=195920) .

2.  Führen Sie die Installationsdatei auf dem Hostcomputer im erweiterten Modus aus, und führen Sie die Schritte im Assistenten aus.

    Weitere Informationen zum Hotfix-Paket für Windows Virtual PC finden Sie im [Artikel 977206](https://go.microsoft.com/fwlink/?LinkId=195921) ( https://go.microsoft.com/fwlink/?LinkId=195921) .

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a>So konfigurieren Sie Antivirus/Sicherungs Software


Um zu verhindern, dass Antivirus-Aktivitäten die Leistung des virtuellen Desktops beeinträchtigen, empfehlen wir, wo Sie können, die folgenden Typen von virtuellen Maschinen von einem beliebigen Antivirus-oder Sicherungsprozess auszuschließen, der auf dem Hostcomputer ausgeführt wird:

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. VHD

## Verwandte Themen


[Konfigurieren der Umgebungsvoraussetzungen](configure-environment-prerequisites.md)

[High-Level-Architektur](high-level-architecturemedv2.md)

[Von MED 2.0 unterstützte Konfigurationen](med-v-20-supported-configurations.md)

 

 





