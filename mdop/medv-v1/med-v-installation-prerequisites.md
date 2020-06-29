---
title: Erforderliche Komponenten MED-V-Installation
description: Erforderliche Komponenten MED-V-Installation
author: dansimp
ms.assetid: cf3c0906-23eb-4c4a-8951-a65741720f95
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2b432b8c2b06e171eb339aab6c7b15efb20d5919
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810873"
---
# Erforderliche Komponenten MED-V-Installation


Im folgenden sind die Voraussetzungen für die Installation von MED-V zu finden:

[Active Directory-Anforderungen](#bkmk-activedirectoryrequirements)

[Berichtsdatenbank](#bkmk-howtoinstallthereportdatabase)

[Antivirus/Backup Software-Konfiguration](#bkmk-antivirusbackupsoftwareconfiguration)

[Microsoft Virtual PC 2007 SP1](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1)

## <a href="" id="bkmk-activedirectoryrequirements"></a>Active Directory-Anforderungen


Wenn Benutzer nicht zur gleichen Domäne gehören, zu der der Server gehört, muss bei der Konfiguration des MED-V-Servers eine Vertrauensstellung zwischen den Domänen eingerichtet werden.

## <a href="" id="bkmk-howtoinstallthereportdatabase"></a>Installieren der Berichtsdatenbank


Die Berichtsdatenbank ist zum Speichern aller MED-V-Arbeitsbereichs Protokolle erforderlich. Die Protokolldatenbank wird dann zum Generieren von MED-V-Berichten verwendet. Informationen zu Berichten finden Sie unter [MED-V-Berichterstellung](med-v-reporting.md).

SQL Server kann auf dem gleichen Server wie der MED-V-Server oder auf einem Remoteserver installiert werden. Wenn Sie auf einem Remoteserver installieren, lesen Sie [Installieren von SQL Server auf einem Remote](#bkmk-installingsqlserveronaremoteserver)Server.

### <a href="" id="bkmk-installingsqlserveronaremoteserver"></a>Installieren von SQL Server auf einem Remote Server

**So installieren Sie SQL Server auf einem Remoteserver**

1.  Konfigurieren Sie auf dem Remoteserver Folgendes:

    -   Instanzname – Standardinstanz

    -   Authentifizierungsmodus – gemischter Modus

    -   Benutzer – der erstellte Standardbenutzer ist "SA"

    -   Kennwort – gewünschtes Kennwort

    -   Sortierungseinstellungen – Standard

    -   Fehler in den Verwendungsberichts Einstellungen – Standard

2.  Installieren Sie die folgenden Dateien auf dem MED-V-Server:

    -   Wenn Sie die Voraussetzungen für die Management Pack Objects-Sammlung für Microsoft SQL Server2008 installieren möchten, laden Sie [Microsoft SQL Server2008 Native Client](https://go.microsoft.com/fwlink/?LinkId=164039) aus dem Microsoft Download Center herunter.

    -   Wenn Sie die Voraussetzungen für die Management Pack Objects-Sammlung für Microsoft SQL Server2005 installieren möchten, laden Sie [Microsoft SQL Server2005 Native Client](https://go.microsoft.com/fwlink/?LinkId=164038) aus dem Microsoft Download Center herunter.

    -   Wenn Sie die erforderlichen dll-Dateien für Microsoft SQL Server2008 installieren möchten, laden Sie die [Microsoft SQL Server 2008 Management Objects-Sammlung](https://go.microsoft.com/fwlink/?LinkId=164041) aus dem Microsoft Download Center herunter.

    -   Wenn Sie die erforderlichen dll-Dateien für Microsoft SQL Server2005 installieren möchten, laden Sie [Microsoft SQL Server2005-Verwaltungsobjekte](https://go.microsoft.com/fwlink/?LinkId=164040) aus dem Microsoft Download Center herunter.

    -   Zum Installieren der eigenständigen Installationspakete, die zusätzlichen Nutzen für SQL Server2008 bieten, laden Sie das [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) aus dem Microsoft Download Center herunter.

    -   Zum Installieren der eigenständigen Installationspakete, die zusätzlichen Nutzen für SQL Server2005 bieten, laden Sie das [Feature Pack für Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) aus dem Microsoft Download Center herunter.

    Weitere Informationen zu diesen Dateien finden Sie unter [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) im Microsoft Download Center ( https://go.microsoft.com/fwlink/?LinkId=163960) oder im [Feature Pack für Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) im Microsoft Download Center ( https://go.microsoft.com/fwlink/?LinkId=163961) .

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a>Antivirus/Backup Software-Konfiguration


Um zu verhindern, dass Antivirenprogramme die Leistung des virtuellen Desktops beeinträchtigen, empfiehlt es sich, die folgenden virtuellen Computerdatei Typen von jeder Antivirus-oder Sicherungsverarbeitung auszuschließen, die auf dem Host ausgeführt wird:

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. CKM

-   \*. EVHD

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1"></a>Installieren und Konfigurieren von Microsoft Virtual PC2007 SP1


**Wichtig**  Wenn Virtual PC für Windows auf dem Hostcomputer vorhanden ist, deinstallieren Sie es vor der Installation von Virtual PC2007 SP1.

 

**So installieren Sie Microsoft Virtual PC2007 SP1**

1.  Laden Sie virtuelles PC2007 SP1 aus dem Microsoft Download Center [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994)herunter.

2.  Führen Sie die Installationsdatei auf dem Hostcomputer aus, und folgen Sie den Anweisungen des Assistenten.

3.  Installieren des Virtual PC2007 SP1-Updates auf dem Hostcomputer im erweiterten Modus

    Weitere Informationen finden Sie in [der Beschreibung des Hotfix-Pakets für Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).

    **Hinweis**  Das virtuelle PC2007 SP1-Update ist für die Ausführung von Virtual PC2007 SP1 erforderlich.

     

## Verwandte Themen


[Unterstützte Konfigurationen](supported-configurationsmedv-orientation.md)

 

 





