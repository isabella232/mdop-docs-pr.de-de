---
title: MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten
description: MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten
author: dansimp
ms.assetid: 74180d8d-7b0f-460f-b301-53595cde8381
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9b89e1a1383997d6ebc92f8e034fbf2945823f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804322"
---
# MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten


Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 mithilfe des System Center Configuration Manager-Integrationsfeatures installieren, müssen Sie die in diesem Thema beschriebenen Voraussetzungen zusätzlich zu den in [MBAM 2,5-Server Voraussetzungen für eigenständige und Configuration Manager-Integrations Topologien](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)ausführen. Sie müssen auch MOF-Dateien erstellen oder ändern, die für die Configuration Manager-Integrations Topologie erforderlich sind.

## Voraussetzungen für das Configuration Manager-Integrationsfeature


Wenn Sie MBAM mit der System Center Configuration Manager-Integrations Topologie konfigurieren, müssen Sie weitere Voraussetzungen erfüllen, die für Configuration Manager erforderlich sind.

[Voraussetzungen für das Configuration Manager-Integrationsfeature](prerequisites-for-the-configuration-manager-integration-feature.md)

## Bearbeiten der Datei "Configuration. mof"


Damit die Clientcomputer BitLocker-Kompatibilitätsdetails über die MBAM-Konfigurations-Manager-Berichte melden können, müssen Sie die Datei "Configuration. mof" für SystemCenter2012 ConfigurationManager und Microsoft System Center Configuration Manager 2007 bearbeiten.

[Bearbeiten der Datei „Configuration.mof“](edit-the-configurationmof-file-mbam-25.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a>Erstellen oder Bearbeiten der SMS \ _def. MOF-Datei


Damit die Clientcomputer BitLocker-Kompatibilitätsdetails in den MBAM-Configuration Manager-Berichten melden können, müssen Sie die SMS \ _def. MOF-Datei erstellen oder bearbeiten. Wenn Sie SystemCenter2012 ConfigurationManager verwenden, müssen Sie die Datei erstellen. In Configuration Manager 2007 ist die Datei bereits vorhanden, daher müssen Sie die vorhandene Datei bearbeiten, aber nicht überschreiben.

[Erstellen oder Bearbeiten der SMS \ _def. MOF-Datei](create-or-edit-the-sms-defmof-file-mbam-25.md)


## Verwandte Themen


[Vorbereiten der Umgebung für MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Von MBAM 2.5 unterstützte Konfigurationen](mbam-25-supported-configurations.md)

[Planen der Bereitstellung von MBAM 2.5](planning-to-deploy-mbam-25.md)

 

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




