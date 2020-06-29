---
title: So erstellen oder bearbeiten Sie MOF-Dateien
description: So erstellen oder bearbeiten Sie MOF-Dateien
author: dansimp
ms.assetid: 4d19d707-b90f-4057-a6e9-e4221a607190
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5f59e9133dd25ecf45d16a5cb704d6ea00923d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811086"
---
# So erstellen oder bearbeiten Sie MOF-Dateien


Bevor Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit Configuration Manager installieren, müssen Sie die Datei "Configuration. mof" bearbeiten. Je nachdem, welche Version von Configuration Manager Sie verwenden, müssen Sie auch die SMS \ _def. MOF-Datei bearbeiten oder erstellen.

## Bearbeiten der Datei „Configuration.mof“


Damit die Clientcomputer BitLocker-Kompatibilitätsdetails über die MBAM-Konfigurations-Manager-Berichte melden können, müssen Sie die Datei "Configuration. mof" für Microsoft System Center Configuration Manager 2007 und SystemCenter2012 ConfigurationManager bearbeiten.

[Bearbeiten der Datei „Configuration.mof“](edit-the-configurationmof-file.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a>Erstellen oder Bearbeiten der SMS \ _def. MOF-Datei


Damit die Clientcomputer BitLocker-Kompatibilitätsdetails in den MBAM-Configuration Manager-Berichten melden können, müssen Sie die SMS \ _def. MOF-Datei erstellen oder bearbeiten. In Configuration Manager 2007 ist die Datei bereits vorhanden, daher müssen Sie die vorhandene Datei bearbeiten, aber nicht überschreiben. Wenn Sie SystemCenter2012 ConfigurationManager verwenden, müssen Sie die Datei erstellen.

[Erstellen oder Bearbeiten der SMS \ _def. MOF-Datei](create-or-edit-the-sms-defmof-file.md)

## Verwandte Themen


[Bereitstellen von MBAM mit dem Konfigurations-Manager](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





