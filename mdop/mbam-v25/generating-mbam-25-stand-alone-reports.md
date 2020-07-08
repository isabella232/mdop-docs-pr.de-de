---
title: Generieren von eigenständigen MBAM 2.5-Berichten
description: Generieren von eigenständigen MBAM 2.5-Berichten
author: dansimp
ms.assetid: 0ec623ff-5155-4906-aef2-20cdc0f84667
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: e1c6b33de26cce5d9ad8d20461dbe0ea0f138c78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809766"
---
# Generieren von eigenständigen MBAM 2.5-Berichten


Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit der eigenständigen Topologie konfigurieren, können Sie Berichte zum Überwachen der BitLocker-Laufwerk Verschlüsselungs Nutzung und-Kompatibilität generieren. Dieses Thema enthält die folgenden Verfahren:

-   [So öffnen Sie die Website "Verwaltung und Überwachung"](#bkmk-openadmin)

-   [So erstellen Sie einen Enterprise-Konformitätsbericht](#bkmk-enterprise)

-   [So erstellen Sie einen Computer Kompatibilitätsbericht](#bkmk-computercomp)

-   [So generieren Sie einen Wiederherstellungsschlüssel-Überwachungsbericht](#bkmk-recoverykey)

Beschreibungen der eigenständigen Berichte finden Sie unter [Grundlegendes zu MBAM 2,5 eigenständige Berichte](understanding-mbam-25-stand-alone-reports.md).

**Hinweis**  Damit Sie die Berichte ausführen können, müssen Sie Mitglied der Gruppe **MBAM-Berichtsbenutzer** sein, die Sie in den Active Directory-Domänendiensten konfigurieren. Weitere Informationen finden Sie unter [Planen von MBAM 2,5-Gruppen und-Konten](planning-for-mbam-25-groups-and-accounts.md).

 

<a href="" id="bkmk-openadmin"></a>**So öffnen Sie die Website "Verwaltung und Überwachung"**

1.  Öffnen Sie einen Webbrowser, und navigieren Sie zur Website Verwaltung und Überwachung. Die Standard-URL für die Website Verwaltung und Überwachung lautet wie folgt:

    *http (s):// &lt; MBAMAdministrationServerName &gt; : &lt; Port &gt; /Helpdesk*

2.  Klicken Sie im linken Bereich auf **Berichte**. Wählen Sie in der oberen Menüleiste den Bericht aus, den Sie ausführen möchten.

    MBAM-Client Daten werden in der Compliance-und Audit-Datenbank für historische Bezüge aufbewahrt, falls ein Computer verloren geht oder gestohlen wird. Wenn Sie Unternehmensberichte ausführen, empfehlen wir, dass Sie geeignete Anfangs-und Endtermine verwenden, um die Zeiträume für die Berichte von ein bis zwei Wochen zu bereichern, um die Genauigkeit der Berichtsdaten zu erhöhen.

    Nachdem Sie einen Bericht erstellt haben, können Sie die Ergebnisse in verschiedenen Formaten wie HTML, Microsoft Word und Microsoft Excel speichern.

    **Hinweis**  Konfigurieren Sie SQL Server Reporting Services (SSRS) so, dass Secure Sockets Layer (SSL) verwendet wird, bevor Sie die Website Verwaltung und Überwachung konfigurieren. Wenn SSRS aus irgendeinem Grund nicht für die Verwendung von SSL konfiguriert ist, wird die URL für die Berichte bei der Konfiguration der Website Verwaltung und Überwachung auf http anstatt auf HTTPS festgelegt. Wenn Sie dann zur Website Verwaltung und Überwachung wechseln und einen Bericht auswählen, wird die folgende Meldung angezeigt: "nur sicherer Inhalt wird angezeigt." Klicken Sie auf **alle Inhalte anzeigen**, um den Bericht anzuzeigen.

     

<a href="" id="bkmk-enterprise"></a>**So erstellen Sie einen Enterprise-Konformitätsbericht**

1.  Wählen Sie auf der Website Verwaltung und Überwachung im linken Navigationsbereich den Knoten **Berichte** aus, wählen Sie **Enterprise-Konformitätsbericht**aus, und wählen Sie die Filter aus, die Sie verwenden möchten. Die verfügbaren Filter für den Enterprise Compliance-Bericht lauten:

    -   **Kompatibilitäts Status** Verwenden Sie diesen Filter, um die Kompatibilitätsstatus Typen des Berichts anzugeben (beispielsweise kompatibel oder nicht kompatibel).

    -   **Fehlerzustand**. Verwenden Sie diesen Filter, um die Fehlerzustands Typen des Berichts anzugeben (beispielsweise kein Fehler oder Fehler).

2.  Klicken Sie auf **Bericht anzeigen** , um den ausgewählten Bericht anzuzeigen.

3.  Wählen Sie einen Computernamen aus, um Informationen zum Computer im Bericht zur Computer Konformität anzuzeigen.

4.  Wählen Sie das Pluszeichen (+) neben dem Computernamen aus, um Informationen zu den Volumes auf dem Computer anzuzeigen.

<a href="" id="bkmk-computercomp"></a>**So erstellen Sie einen Computer Kompatibilitätsbericht**

1.  Wählen Sie auf der Website Verwaltung und Überwachung im linken Navigationsbereich den Knoten **Bericht** aus, und wählen Sie dann **Computer Kompatibilitätsbericht**aus. Verwenden Sie den Bericht zur Computer Konformität, um nach **Benutzername** oder **Computername**zu suchen.

2.  Klicken Sie auf **Bericht anzeigen** , um den Bericht zur Computer Konformität anzuzeigen.

3.  Wählen Sie einen Computernamen aus, um weitere Informationen zum Computer im Bericht zur Computer Konformität anzuzeigen.

4.  Wählen Sie das Pluszeichen (+) neben dem Computernamen aus, um Informationen zu den Volumes auf dem Computer anzuzeigen.

    **Hinweis**  Ein MBAM-Clientcomputer gilt als kompatibel, wenn der Computer die Anforderungen der MBAM-Gruppenrichtlinieneinstellungen erfüllt oder überschreitet.

<a href="" id="bkmk-recoverykey"></a>**So generieren Sie einen Wiederherstellungsschlüssel-Überwachungsbericht**

1.  Wählen Sie auf der Website Verwaltung und Überwachung im linken Navigationsbereich den Knoten **Bericht** aus, und wählen Sie dann **Wiederherstellungs Überwachungsbericht**aus. Wählen Sie die Filter für Ihren Wiederherstellungsschlüssel-Überwachungsbericht aus. Die verfügbaren Filter für Wiederherstellungsschlüssel Audits lauten wie folgt:

    -   **Helpdesk-Nutzer**. Dieser Filter ermöglicht Benutzern, den Benutzernamen des anfordernden Benutzers anzugeben. Der Anforderer ist die Person im Helpdesk, die im Auftrag eines Endbenutzers auf den Schlüssel zugegriffen hat.

    -   **Endbenutzer**. Mit diesem Filter können Benutzer den Benutzernamen des anfordernden angeben. Der anfordernde ist der Endbenutzer, der den Helpdesk aufgerufen hat, um einen Wiederherstellungsschlüssel zu erhalten.

    -   **Ergebnis anfordern**. Dieser Filter ermöglicht Benutzern, die anforderungsergebnis Typen (beispielsweise Erfolg oder Fehler) anzugeben, auf denen der Bericht basieren soll. Beispielsweise können Benutzer fehlgeschlagene Zugriffsversuche auf Schlüssel anzeigen anzeigen.

    -   **Key-Typ**. Dieser Filter ermöglicht Benutzern die Angabe des Schlüsseltyps (beispielsweise des Wiederherstellungsschlüssel Kennworts oder des TPM-Kennworthashs), auf dem der Bericht basieren soll.

    -   **Anfangstermin**. Dieser Filter wird verwendet, um den Anfangstermin Teil des Datumsbereichs zu definieren, über den der Benutzerbericht erstatten möchte.

    -   **Enddatum**. Dieser Filter wird verwendet, um den Enddatums Teil des Datumsbereichs zu definieren, über den die Benutzer Berichte erstellen möchten.

2.  Klicken Sie auf **Bericht anzeigen** , um den Bericht anzuzeigen.



## Verwandte Themen


[BitLocker-Kompatibilitätsüberwachung und -berichterstellung mit MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[Grundlegende Informationen zu eigenständigen MBAM 2.5-Berichten](understanding-mbam-25-stand-alone-reports.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





