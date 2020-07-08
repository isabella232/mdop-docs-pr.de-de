---
title: So generieren Sie MBAM-Berichte
description: So generieren Sie MBAM-Berichte
author: dansimp
ms.assetid: 083550cb-8c3f-49b3-a30e-97d85374d2f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ccdc1a2cd69d8cc2e2c2823827f5ea43ad867a78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810348"
---
# So generieren Sie MBAM-Berichte


Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit der eigenständigen Topologie installieren, können Sie unterschiedliche Berichte erstellen, um die BitLocker-Verschlüsselungs Nutzung und-Kompatibilität zu überwachen. In den Verfahren in diesem Thema wird beschrieben, wie Sie die Website "Verwaltung und Überwachung" und die erforderlichen Schritte zum Generieren von Microsoft BitLocker-Verwaltungs-und-Überwachungsberichten zu Unternehmenskonformität, einzelnen Computern und wichtigen Wiederherstellungsaktivitäten öffnen. Detaillierte Informationen zum Verständnis von MBAM-Berichten finden Sie unter [Grundlegendes zu MBAM-Berichten](understanding-mbam-reports-mbam-2.md).

**Hinweis**  Um die Berichte ausführen zu können, müssen Sie Mitglied der **Rolle "Berichtsbenutzer** " auf den Computern sein, auf denen die Verwaltungs-und Überwachungs Server Features, die Kompatibilitäts-und Überwachungsdatenbank sowie die Kompatibilitäts-und Überwachungsberichte installiert sind.

 

**So öffnen Sie die Website "Verwaltung und Überwachung"**

1.  Öffnen Sie einen Webbrowser, und navigieren Sie zur Websiteverwaltung und Überwachung. Die Standard-URL für die Websiteverwaltung und Überwachung lautet *http:// &lt; Computer &gt; Name*.

    **Hinweis**  Wenn Lebensarbeitszeit und die Überwachungs Website auf einem anderen Port als 80 installiert wurden, müssen Sie den Port in der URL angeben (beispielsweise *http:// &lt; Computername &gt; : &lt; Port &gt; *. Wenn Sie während der Installation einen Hostnamen für Lebensarbeitszeit-und Überwachungs Website angegeben haben, lautet die URL *http:// &lt; Hostname &gt; *.

     

2.  Klicken Sie im linken Bereich auf **Berichte** , und wählen Sie dann in der oberen Menüleiste den Bericht aus, den Sie ausführen möchten.

    Historische MBAM-Client Daten werden in der Kompatibilitätsdatenbank für historische Bezüge aufbewahrt, falls ein Computer verloren geht oder gestohlen wird. Wenn Sie Unternehmensberichte ausführen, empfehlen wir, dass Sie geeignete Anfangs-und Endtermine verwenden, um die Zeiträume für die Berichte von ein bis zwei Wochen zu bereichern, um die Genauigkeit der Berichtsdaten zu erhöhen.

    **Hinweis**  Wenn SSRS nicht für die Verwendung von Secure Socket Layer konfiguriert wurde, wird die URL für die Berichte bei der Installation des MBAM-Servers auf http anstatt auf HTTPS festgelegt. Wenn Sie dann zum Helpdesk-Portal wechseln und einen Bericht auswählen, wird die folgende Meldung angezeigt: "nur sicherer Inhalt wird angezeigt." Klicken Sie auf **alle Inhalte anzeigen**, um den Bericht anzuzeigen.

     

**So erstellen Sie einen Enterprise-Konformitätsbericht**

1.  Wählen Sie auf der Websiteverwaltung und Überwachung im linken Navigationsbereich den Knoten **Berichte** aus, wählen Sie **Enterprise-Konformitätsbericht**aus, und wählen Sie die Filter aus, die Sie verwenden möchten. Die verfügbaren Filter für den Enterprise Compliance-Bericht lauten wie folgt:

    -   **Kompatibilitäts Status** Verwenden Sie diesen Filter, um die Kompatibilitätsstatus Typen (beispielsweise kompatibel oder nicht kompatibel) des Berichts anzugeben.

    -   **Fehlerzustand**. Verwenden Sie diesen Filter, um die Fehlerzustands Typen (beispielsweise kein Fehler oder Fehler) des Berichts anzugeben.

2.  Klicken Sie auf **Bericht anzeigen** , um den ausgewählten Bericht anzuzeigen.

    Ergebnisse können in unterschiedlichen Formaten wie HTML, Microsoft Word und Microsoft Excel gespeichert werden.

    **Hinweis**  Der Enterprise-Konformitätsbericht wird von einem SQL-Auftrag generiert, der alle sechs Stunden ausgeführt wird. Wenn Sie den Bericht zum ersten Mal anzeigen, stellen Sie möglicherweise fest, dass einige Daten fehlen. Sie können aktualisierte Berichtsdaten mithilfe von SQL Management Studio manuell generieren. Erweitern Sie im Fenster **Objekt-Explorer** den Eintrag **SQL Server-Agent**, erweitern Sie **Aufträge**, klicken Sie mit der rechten Maustaste auf den **createcache** -Auftrag, und wählen Sie **Job bei Schritt starten** aus.

     

3.  Wählen Sie einen Computernamen aus, um Informationen zum Computer im Bericht zur Computer Konformität anzuzeigen.

4.  Wählen Sie das Pluszeichen (+) neben dem Computernamen aus, um Informationen zu den Volumes auf dem Computer anzuzeigen.

**So generieren Sie den Bericht zur Computer Konformität**

1.  Wählen Sie auf der Websiteverwaltung und Überwachung im linken Navigationsbereich den Knoten **Bericht** aus, und wählen Sie dann den **Bericht Computer Compliance**aus. Verwenden Sie den Bericht zur Computer Konformität, um nach **Benutzername** oder **Computername**zu suchen.

2.  Klicken Sie auf **Bericht anzeigen** , um den computerbericht anzuzeigen.

    Ergebnisse können in unterschiedlichen Formaten wie HTML, Microsoft Word und Microsoft Excel gespeichert werden.

3.  Wählen Sie einen Computernamen aus, um weitere Informationen zum Computer im Bericht zur Computer Konformität anzuzeigen.

4.  Wählen Sie das Pluszeichen (+) neben dem Computernamen aus, um Informationen zu den Volumes auf dem Computer anzuzeigen.

    **Hinweis**  Ein MBAM-Clientcomputer gilt als kompatibel, wenn der Computer den Anforderungen der MBAM-Richtlinieneinstellungen entspricht.

     

**So generieren Sie den Wiederherstellungsschlüssel-Überwachungsbericht**

1.  Wählen Sie auf der Websiteverwaltung und Überwachung im linken Navigationsbereich den Knoten **Bericht** aus, und wählen Sie dann den **Bericht Wiederherstellungs**Überwachung aus. Wählen Sie die Filter für Ihren Wiederherstellungsschlüssel-Überwachungsbericht aus. Die verfügbaren Filter für Wiederherstellungsschlüssel Audits lauten wie folgt:

    -   **Requestor**. Dieser Filter ermöglicht Benutzern, den Benutzernamen des anfordernden Benutzers anzugeben. Der anfordernde ist die Person im Helpdesk, die im Auftrag eines Benutzers auf den Schlüssel zugegriffen hat.

    -   **Anfordernder**. Mit diesem Filter können Benutzer den Benutzernamen des anfordernden angeben. Der Antragsteller ist die Person, die den Helpdesk aufgerufen hat, um einen Wiederherstellungsschlüssel zu erhalten.

    -   **Ergebnis anfordern**. Dieser Filter ermöglicht Benutzern, die anforderungsergebnis Typen (beispielsweise Erfolg oder Fehler) anzugeben, auf denen der Bericht basieren soll. Beispielsweise können Benutzer fehlgeschlagene Zugriffsversuche auf Schlüssel anzeigen anzeigen.

    -   **Key-Typ**. Dieser Filter ermöglicht Benutzern die Angabe des Schlüsseltyps (beispielsweise: Wiederherstellungsschlüssel Kennwort oder TPM-Kenn Wort Hash), auf dem der Bericht basieren soll.

    -   **Anfangstermin**. Dieser Filter wird verwendet, um den Anfangstermin Teil des Datumsbereichs zu definieren, über den der Benutzerbericht erstatten möchte.

    -   **Enddatum**. Dieser Filter wird verwendet, um den Enddatums Teil des Datumsbereichs zu definieren, über den die Benutzer Berichte erstellen möchten.

2.  Klicken Sie auf **Bericht anzeigen** , um den Bericht anzuzeigen.

    Ergebnisse können in unterschiedlichen Formaten wie HTML, Microsoft Word und Microsoft Excel gespeichert werden.

## Verwandte Themen


[BitLocker-Kompatibilitätsüberwachung und -berichterstellung mit MBAM 2.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





