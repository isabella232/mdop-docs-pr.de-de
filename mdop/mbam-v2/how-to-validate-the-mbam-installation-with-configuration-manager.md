---
title: So überprüfen Sie die MBAM-Installation mit dem Konfigurations-Manager
description: So überprüfen Sie die MBAM-Installation mit dem Konfigurations-Manager
author: dansimp
ms.assetid: 8e268539-91c3-4e8a-baae-faf3605da818
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 500c6f6ee5138b5677bf1fa20e2627a56981df1f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809475"
---
# So überprüfen Sie die MBAM-Installation mit dem Konfigurations-Manager


Nachdem Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit Configuration Manager installiert haben, überprüfen Sie, ob die Installation alle erforderlichen Features für MBAM erfolgreich eingerichtet hat, indem Sie die folgenden Schritte ausführen.

**So überprüfen Sie die MBAM Server-Feature-Installation mit Configuration Manager**

1.  Öffnen Sie auf dem Server, auf dem System Center Configuration Manager bereitgestellt wird, die **Systemsteuerung.** Wählen Sie das Programm aus, das zum Deinstallieren oder Ändern eines Programms verwendet wird. Überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** in der Liste der Programme und Funktionen angezeigt wird.

    **Hinweis**  Um die Installation zu überprüfen, müssen Sie ein Domänenkonto verwenden, das über lokale Computeradministrator Anmeldeinformationen auf jedem Server verfügt.

     

2.  Überprüfen Sie mithilfe der Configuration Manager-Konsole, ob eine neue Sammlung mit dem Namen "MBAM-unterstützte Computer" angezeigt wird.

    So zeigen Sie die Sammlung mit Configuration Manager 2007 an: Klicken Sie auf **Website Datenbank** ( &lt; **SiteCode** &gt;  -  &lt; **Servername** &gt; , &lt; **Sitename** &gt; ), **Computer Verwaltung**.

    So zeigen Sie die Sammlung mit SystemCenter2012 ConfigurationManager an: Klicken Sie auf den Arbeitsbereich **Ressourcen und Kompatibilität** , **gerätesammlungen**.

3.  Verwenden Sie die Configuration Manager-Konsole, um zu überprüfen, ob die folgenden Berichte im **MBAM** -Ordner aufgeführt sind:

    -   BitLocker-Computer Konformität

    -   BitLocker Enterprise Compliance-Dashboard

    -   Details zur BitLocker-Unternehmenskonformität

    -   Zusammenfassung der BitLocker-Unternehmenskonformität

    So zeigen Sie die Berichte mit Configuration Manager 2007 an: Klicken Sie auf Bericht **Erstellung**, **Reporting Services**, \ \ \ \ &lt; **Servername** &gt; , **Berichtsordner**

    So zeigen Sie die Berichte mit SystemCenter2012 ConfigurationManager an: Klicken Sie auf den Arbeitsbereich **Überwachung** , **Berichterstellung**, **Berichte**.

4.  Verwenden Sie die Configuration Manager-Konsole, um zu bestätigen, dass der Konfigurations Basisplan "BitLocker-Schutz" aufgeführt ist.

    So zeigen Sie die Konfigurationsbasislinien mit Configuration Manager 2007 an: Klicken Sie auf **gewünschte Konfigurationsverwaltung**, **Konfigurationsbasislinien**.

    So zeigen Sie die Konfigurationsbasislinien mit SystemCenter2012 ConfigurationManager an: Klicken Sie auf den Arbeitsbereich **Ressourcen und Kompatibilität** , **Konformitäts Einstellungen**, **Konfigurationsbasislinien**.

5.  Überprüfen Sie mithilfe der Configuration Manager-Konsole, ob die folgenden neuen Konfigurationselemente angezeigt werden:

    -   BitLocker-Datenlaufwerke mit fester Datensicherheit

    -   BitLocker-Betriebs System-Laufwerkschutz

    So zeigen Sie die Konfigurationselemente mit Configuration Manager 2007 an: Klicken Sie auf **gewünschte Konfigurationsverwaltung**, **Konfigurationselemente**.

    So zeigen Sie die Konfigurationselemente mit SystemCenter2012 ConfigurationManager an: Klicken Sie auf den Arbeitsbereich **Ressourcen und Kompatibilität** , **Konformitäts Einstellungen**, **Konfigurationselemente**.

## Verwandte Themen


[Bereitstellen von MBAM mit dem Konfigurations-Manager](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





