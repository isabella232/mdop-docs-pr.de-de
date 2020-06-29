---
title: So generieren Sie MBAM-Berichte
description: So generieren Sie MBAM-Berichte
author: dansimp
ms.assetid: cdf4ae76-040c-447c-8736-c9e57068d221
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f0b5a4e984d7a609eab7204e67f46042992f586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810609"
---
# So generieren Sie MBAM-Berichte


Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) generiert verschiedene Berichte, um die BitLocker-Verschlüsselungs Nutzung und-Kompatibilität zu überwachen. In diesem Thema wird beschrieben, wie Sie die MBAM-Verwaltungswebsite öffnen und wie Sie MBAM-Berichte zu Unternehmenskonformität, einzelnen Computern, Hardwarekompatibilität und wichtigen Wiederherstellungsaktivitäten generieren. Weitere Informationen zu MBAM-Berichten finden Sie unter [Grundlegendes zu MBAM-Berichten](understanding-mbam-reports-mbam-1.md).

**Hinweis**  Damit Sie die Berichte ausführen können, müssen Sie Mitglied der Rolle " **Berichtsbenutzer** " auf den Computern sein, auf denen Sie die Verwaltungs-und Überwachungs Server Features, die Kompatibilitäts-und Überwachungsdatenbank sowie Compliance-und Überwachungsberichte installiert haben.

 

**So öffnen Sie die MBAM-Verwaltungswebsite**

1.  Öffnen Sie einen Webbrowser, und navigieren Sie zur MBAM-Website. Die Standard-URL für die Website lautet *http:// &lt; Computer &gt; Name* des Microsoft BitLocker-Verwaltungs-und-Überwachungsservers.

    **Hinweis**  Wenn die MBAMadministration-Website auf einem anderen Port als Port 80 installiert wurde, müssen Sie diese Portnummer in der URL angeben. Beispiel * &lt; : http://Computername &gt; : &lt; Port &gt; *. Wenn Sie während der Installation einen Hostnamen für die MBAMadministration-Website angegeben haben, lautet die *URL &lt; http:// &gt; Hostname*.

     

2.  Klicken Sie im Navigationsbereich auf **Berichte**. Klicken Sie im Hauptbereich auf die Registerkarte für Ihren Berichtstyp: **Enterprise-Konformitätsbericht**, **Computer Kompatibilitätsbericht**, **Hardware Überwachungsbericht**oder **Wiederherstellungs Überwachungsbericht**.

    **Hinweis**  Historische MBAM-Client Daten werden in der Kompatibilitätsdatenbank aufbewahrt. Diese aufbewahrten Daten sind möglicherweise erforderlich, wenn ein Computer verloren geht oder gestohlen wird. Wenn Sie Unternehmensberichte ausführen, sollten Sie geeignete Anfangs-und Endtermine verwenden, um die Zeiträume für die Berichte von ein bis zwei Wochen zu bereichern, um die Genauigkeit der Berichtsdaten zu erhöhen.

     

**So erstellen Sie einen Enterprise-Konformitätsbericht**

1.  Klicken Sie auf der MBAMadministration-Website im Navigationsbereich auf **Berichte** , und klicken Sie dann auf die Registerkarte **Enterprise-Konformitätsbericht** , und wählen Sie die entsprechenden Filter für den Bericht aus. Für den Enterprise-Konformitätsbericht können Sie die folgenden Filter einrichten.

    -   **Kompatibilitäts Status** Verwenden Sie diesen Filter, um die Kompatibilitätsstatus Typen (beispielsweise kompatibel oder nicht kompatibel) anzugeben, die in den Bericht aufgenommen werden sollen.

    -   **Fehlerzustand**. Verwenden Sie diesen Filter, um die Fehlerzustands Typen wie keinen Fehler oder Fehler anzugeben, die in den Bericht aufgenommen werden sollen.

2.  Klicken Sie auf **Bericht anzeigen** , um den angegebenen Bericht anzuzeigen.

    Die Berichtsergebnisse können in einem der verschiedenen verfügbaren Dateiformate wie HTML, Microsoft Word und Microsoft Excel gespeichert werden.

    **Hinweis**  Der Enterprise-Konformitätsbericht wird von einem SQL-Auftrag generiert, der alle sechs Stunden ausgeführt wird. Wenn Sie den Bericht zum ersten Mal anzeigen, stellen Sie möglicherweise fest, dass einige Daten fehlen.

     

3.  Wenn Sie Informationen zu einem Computer im Computer Kompatibilitätsbericht anzeigen möchten, wählen Sie den Computernamen aus.

4.  Wählen Sie das Pluszeichen (+) neben dem Computernamen aus, um Informationen zu den Volumes auf dem Computer anzuzeigen.

**So generieren Sie den Bericht zur Computer Konformität**

1.  Wählen Sie auf der MBAMadministration-Website im Navigationsbereich den Knoten **Bericht** aus, und wählen Sie dann den **Bericht Computer Compliance**aus. Verwenden Sie den Bericht zur Computer Konformität, um nach **Benutzername** oder **Computername**zu suchen.

2.  Klicken Sie auf **Bericht anzeigen** , um den computerbericht anzuzeigen.

    Ergebnisse können in einem der verschiedenen verfügbaren Dateiformate wie HTML, Microsoft Word und Microsoft Excel gespeichert werden.

3.  Wenn Sie weitere Informationen zu einem Computer im Computer Kompatibilitätsbericht anzeigen möchten, wählen Sie den Computernamen aus.

4.  Wählen Sie das Pluszeichen (+) neben dem Computernamen aus, um Informationen zu den Volumes auf dem Computer anzuzeigen.

    **Hinweis**  Ein MBAM-Client Computer gilt als kompatibel, wenn der Computer den Anforderungen der MBAM-Richtlinieneinstellungen entspricht oder das Hardwaremodell des Computers auf inkompatibel eingestellt ist. Wenn Sie detaillierte Informationen zu den mit dem Computer verknüpften Datenträger-Volumes anzeigen, können Computer, die aufgrund der Hardwarekompatibilität von der BitLocker-Verschlüsselung ausgenommen sind, als kompatibel angezeigt werden, obwohl der Verschlüsselungsstatus für den Laufwerk Datenträger als nicht kompatibel angezeigt wird.

     

**So generieren Sie den Hardware Kompatibilitäts Überwachungsbericht**

1.  Wählen Sie auf der MBAMadministration-Website im Navigationsbereich den Knoten **Bericht** aus, und wählen Sie dann den **Hardware Überwachungsbericht**aus. Wählen Sie die entsprechenden Filter für Ihren Hardware Überwachungsbericht aus. Der Hardware Überwachungsbericht bietet die folgenden verfügbaren Filter:

    -   **Benutzer (Domain\\User)**. Gibt den Namen des Benutzers an, der eine Änderung vorgenommen hat.

    -   **Ändern**Sie den Typ. Gibt den Typ der gesuchten Änderungen an.

    -   **Anfangstermin**. Gibt den Anfangstermin Teil des Datumsbereichs an, für den Sie einen Bericht erstellen möchten.

    -   **Enddatum**. Gibt den Endtermin des Datumsbereichs an, zu dem Sie einen Bericht erstatten möchten.

2.  Klicken Sie auf **Bericht anzeigen** , um den Bericht anzuzeigen.

    Ergebnisse können in verschiedenen verfügbaren Dateiformaten wie HTML, Microsoft Word und Microsoft Excel gespeichert werden.

**So generieren Sie den Wiederherstellungsschlüssel-Überwachungsbericht**

1.  Wählen Sie auf der MBAMadministration-Website den Knoten **Bericht** im Navigationsbereich aus, und wählen Sie dann den **Wiederherstellungs Überwachungsbericht**aus. Wählen Sie die Filter für Ihren Wiederherstellungsschlüssel-Überwachungsbericht aus. Die verfügbaren Filter für Wiederherstellungsschlüssel Audits lauten wie folgt:

    -   **Requestor**. Gibt den Benutzernamen des Requestors an. Der Anforderer ist die Person im Helpdesk, die im Auftrag eines Benutzers auf den Schlüssel zugegriffen hat.

    -   **Anfordernder**. Gibt den Benutzernamen des Antragstellers an. Der Antragsteller ist die Person, die den Helpdesk aufgerufen hat, um einen Wiederherstellungsschlüssel zu erhalten.

    -   **Ergebnis anfordern** Gibt die Abfrageergebnistypen an, beispielsweise: Erfolg oder Fehler. So können Sie beispielsweise versuchen, fehlgeschlagene Zugriffsversuche auf Schlüssel anzuzeigen.

    -   **Key-Typ**. Gibt den Schlüsseltyp an, beispielsweise: Kennwort für Wiederherstellungsschlüssel oder TPM-Kenn Wort Hash.

    -   **Anfangstermin**. Gibt den Anfangstermin Teil des Datumsbereichs an.

    -   **Enddatum**. Gibt den Endtermin des Datumsbereichs an.

2.  Klicken Sie auf **Bericht anzeigen** , um den Bericht anzuzeigen.

    Ergebnisse können in verschiedenen verfügbaren Dateiformaten wie HTML, Microsoft Word und Microsoft Excel gespeichert werden.

## Verwandte Themen


[BitLocker-Kompatibilitätsüberwachung und -berichterstellung mit MBAM 1.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





