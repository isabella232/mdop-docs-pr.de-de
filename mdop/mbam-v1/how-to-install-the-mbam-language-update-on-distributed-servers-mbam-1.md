---
title: So installieren Sie das MBAM-Sprachupdate auf verteilten Servern
description: So installieren Sie das MBAM-Sprachupdate auf verteilten Servern
author: dansimp
ms.assetid: 5ddc64c6-0417-4a04-843e-b5e18d9f1a52
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6758463c6fc038c4d6ea86c0d49804f29bb543d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811311"
---
# So installieren Sie das MBAM-Sprachupdate auf verteilten Servern


Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) umfasst vier Serverrollen, die auf einem oder mehreren Computern ausgeführt werden können. Allerdings erfordern nur zwei MBAM-Server Features das Update, um die Installation der MBAM 1,0-Sprachversion und der MBAM-Richtlinienvorlage zu unterstützen. In Konfigurationen mit den MBAM-Server Features, die auf mehreren Computern installiert sind, müssen nur die folgenden Server Features aktualisiert werden:

-   Die MBAM-Konformitäts-und Überwachungsberichte

-   Der MBAM-Verwaltungs-und-Überwachungs Server

**Wichtig**  Die MBAM-Server Features müssen in dieser Reihenfolge aktualisiert werden: zuerst Konformitäts-und Überwachungsberichte und dann den Server für Verwaltung und Überwachung. Die MBAM-Gruppenrichtlinienvorlagen können jederzeit ohne Rücksicht auf die Reihenfolge aktualisiert werden.

 

**So installieren Sie das MBAM-sprach Update auf der MBAM-Konformitäts-und Überwachungsberichts Server Funktion**

1.  Suchen Sie auf dem Computer, auf dem das Feature MBAM-Konformitäts-und Überwachungsbericht ausgeführt wird, den MBAM-Setup-Assistenten für Sprach Updates (MBAMsetup.exe).

2.  Führen Sie den Assistenten für Konformitäts-und Überwachungsberichte aus, und schließen Sie dann den Assistenten.

**So installieren Sie das MBAM-sprach Update auf dem MBAM-Server Feature "Verwaltung und Überwachung"**

1.  Öffnen Sie auf dem Computer, auf dem das Feature MBAM-Verwaltung und-Überwachung ausgeführt wird, die IIS-Verwaltungskonsole (Internet Informationsdienste), wechseln Sie zu **Websites**, und schließen Sie dann die Website Microsoft BitLocker-Verwaltung und-Überwachung.

2.  Wählen Sie aus, um die Bindungen für die MBAM-Website zu bearbeiten, und ändern Sie dann die Bindungen der Website. Ändern Sie beispielsweise den Port von 443 in 9443.

3.  Suchen Sie den Setup-Assistenten für MBAM-sprach Updates (MBAMsetup.exe), und führen Sie ihn aus. Führen Sie den Assistenten für das Feature Verwaltung und Monitoring Server aus, und schließen Sie dann den Assistenten.

4.  Nachdem Sie die Server Datenbank aktualisiert haben, öffnen Sie die IIS-Verwaltungskonsole, und überprüfen Sie die Bindungen der Website Microsoft BitLocker-Verwaltung und-Überwachung.

5.  Löschen Sie die alte Bindung, und stellen Sie sicher, dass die verbleibende Bindung den richtigen Hostnamen, das Zertifikat und die Portnummer für die MBAM Enterprise-Konfiguration aufweist.

6.  Starten Sie die MBAM-Website neu.

7.  Testen Sie die Funktionalität der MBAM-Website:

    -   Öffnen Sie die MBAM-Weboberfläche, und stellen Sie sicher, dass Sie einen Wiederherstellungsschlüssel für einen Client abrufen können.

    -   Erzwingen der Verschlüsselung eines neuen oder manuell entschlüsselten Clientcomputers

        **Hinweis**  Der MBAM-Client wird nur geöffnet, wenn er mit der Wiederherstellungs-und Hardware Datenbank kommunizieren kann.

         

## Verwandte Themen


[Bereitstellen des Sprachrelease-Updates für MBAM 1.0](deploying-the-mbam-10-language-release-update.md)

 

 





