---
title: So installieren Sie das MBAM-Sprachupdate auf einem einzelnen Server
description: So installieren Sie das MBAM-Sprachupdate auf einem einzelnen Server
author: dansimp
ms.assetid: e6fe59a3-a3e1-455c-a059-1f23ee083cf6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94814158335430aba433c180cdba83d0cf15b760
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810744"
---
# So installieren Sie das MBAM-Sprachupdate auf einem einzelnen Server


Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) umfasst vier Serverrollen, die auf einem oder mehreren Computern ausgeführt werden können. Allerdings erfordern nur zwei MBAM-Server Features das Update, um die Installation der MBAM 1,0-Sprachversion und der MBAM-Richtlinienvorlage zu unterstützen. Führen Sie die in diesem Thema beschriebenen Schritte aus, um alle drei erforderlichen MBAM-Features zu aktualisieren, die auf einem Computer installiert werden sollen.

**So installieren Sie das MBAM-sprach Update auf einem einzelnen Server**

1.  Öffnen Sie die Internet Informationsdienste (IIS)-Verwaltungskonsole, wechseln Sie zu **Websites**, und schließen Sie dann die Website für die Microsoft BitLocker-Verwaltung und-Überwachung.

2.  Bearbeiten Sie die Bindungen für die MBAM-Website, und ändern Sie dann temporär die Bindungen der Website. Ändern Sie beispielsweise den Port von 443 in 9443.

3.  Suchen Sie den MBAM-Setup-Assistenten (MBAMsetup.exe), und führen Sie ihn aus, und wählen Sie die folgenden drei Features aus:

    1.  Konformitäts-und Überwachungsberichte

    2.  Verwaltungs-und Überwachungs Server

    3.  Vorlagen für Gruppenrichtlinien

    **Wichtig**  Die MBAM-Server Features müssen in der folgenden Reihenfolge aktualisiert werden: zuerst Konformitäts-und Überwachungsberichte, dann Administration und Monitoring Server. Die Gruppenrichtlinienvorlagen können jederzeit ohne Rücksicht auf die Reihenfolge aktualisiert werden.

     

4.  Nachdem Sie die Server Datenbank aktualisiert haben, öffnen Sie die IIS-Verwaltungskonsole, und überprüfen Sie die Bindungen der Website Microsoft BitLocker-Verwaltung und-Überwachung.

5.  Löschen Sie eine der Bindungen, und stellen Sie sicher, dass die verbleibende Bindung den richtigen Hostnamen, das Zertifikat und die Portnummer für die MBAM Enterprise-Konfiguration aufweist.

6.  Starten Sie die MBAM-Website neu.

7.  Testen Sie die Funktionalität der MBAM-Website:

    -   Öffnen Sie die MBAM-Weboberfläche, und stellen Sie sicher, dass Sie einen Wiederherstellungsschlüssel für einen Client abrufen können.

    -   Erzwingen der Verschlüsselung eines neuen oder manuell entschlüsselten Clientcomputers

        **Hinweis**  Der MBAM-Client wird nur geöffnet, wenn er mit der Wiederherstellungs-und Hardware Datenbank kommunizieren kann.

         

## Verwandte Themen


[Bereitstellen des Sprachrelease-Updates für MBAM 1.0](deploying-the-mbam-10-language-release-update.md)

 

 





