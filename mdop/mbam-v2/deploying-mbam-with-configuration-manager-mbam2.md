---
title: Bereitstellen von MBAM mit dem Konfigurations-Manager
description: Bereitstellen von MBAM mit dem Konfigurations-Manager
author: dansimp
ms.assetid: 89d03e29-457a-471d-b893-e0b74a83ec50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c6cffc1cf51a26aeaa94fcb265199c19f0f34abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809964"
---
# Bereitstellen von MBAM mit dem Konfigurations-Manager


In den folgenden Verfahren wird beschrieben, wie Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit Microsoft System Center Configuration Manager 2007 oder MicrosoftSystemCenter2012 ConfigurationManager durch usingthe Empfohlene Konfiguration bereitstellen, die unter [Erste Schritte bei der Verwendung von MBAM mit Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)beschrieben wird. Die empfohlene Konfiguration besteht darin, die Verwaltungs-und Überwachungsfeatures auf einem oder mehreren Microsoft BitLocker-Verwaltungs-und-Überwachungs Servern zu installieren und Microsoft System Center Configuration Manager 2007 oder MicrosoftSystemCenter2012 ConfigurationManager auf einem separaten Server zu installieren.

Bevor Sie mit der Installation beginnen, stellen Sie sicher, dass Sie die Voraussetzungen und Hardware-und Softwareanforderungen für die Installation von MBAM mit Configuration Manager erfüllt haben, indem Sie [Planen zum Bereitstellen von MBAM mit Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md)überprüfen.

Wenn Sie MBAM mit der Configuration Manager-Topologie erneut installieren müssen, müssen Sie zuerst bestimmte Configuration Manager-Objekte entfernen. Lesen Sie den [Knowledge Base-Artikel](https://go.microsoft.com/fwlink/?LinkId=286306) , um weitere Informationen zu erhalten.

Die Schritte zum Installieren von MBAM mit Configuration Manager sind in die folgenden Kategorien unterteilt. Führen Sie die Schritte für jede Kategorie aus, um die Installation abzuschließen.

## So erstellen oder bearbeiten Sie MOF-Dateien


Damit die Clientcomputer BitLocker-Konformitätsdetails über die MBAM-Konfigurations-Manager-Berichte melden können, müssen Sie die Datei " **Configuration. MOF** " Bearbeiten und entweder die SMS \ _def. MOF-Datei bearbeiten oder erstellen, je nachdem, welche Version von Configuration Manager Sie verwenden.

[So erstellen oder bearbeiten Sie MOF-Dateien](how-to-create-or-edit-the-mof-files.md)

## So installieren Sie MBAM mit dem Konfigurations-Manager


In diesem Abschnitt finden Sie eine schrittweise Anleitung zum Installieren der folgenden Schritte: MBAM auf dem Configuration Manager-Server; die Wiederherstellungs-und Überwachungsdatenbanken auf dem Daten Bank Server; und die Verwaltungs-und Überwachungsserver Features auf dem Verwaltungs-und Überwachungsserver.

[So installieren Sie MBAM mit dem Konfigurations-Manager](how-to-install-mbam-with-configuration-manager.md)

## Überprüfen der MBAM Server-Feature-Installation auf dem Configuration Manager-Server


Wenn die Microsoft BitLocker-Administrator-und-überwachungsinstallation abgeschlossen ist, überprüfen Sie, ob die Installation alle erforderlichen MBAM-Features erfolgreich eingerichtet hat, die für den Configuration Manager-Server erforderlich sind.

[So überprüfen Sie die MBAM-Installation mit dem Konfigurations-Manager](how-to-validate-the-mbam-installation-with-configuration-manager.md)

## Verwandte Themen


[Verwenden von MBAM mit dem Konfigurations-Manager](using-mbam-with-configuration-manager.md)

 

 





