---
title: So lokalisieren Sie die HelpdeskText-Anweisung, mit der Benutzer auf weitere Informationen zum Self-Service-Portal verwiesen werden
description: So lokalisieren Sie die HelpdeskText-Anweisung, mit der Benutzer auf weitere Informationen zum Self-Service-Portal verwiesen werden
author: dansimp
ms.assetid: 09ba2a07-3186-45d9-adef-4034c70ae7cf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2367424185da813a46fa52f3614c03083864f75f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809946"
---
# So lokalisieren Sie die HelpdeskText-Anweisung, mit der Benutzer auf weitere Informationen zum Self-Service-Portal verwiesen werden


Sie können eine lokalisierte Version der Self-Service-Portal-"HelpdeskText"-Anweisung konfigurieren, die Endbenutzer darüber informiert, wie Sie bei Verwendung des Self-Service-Portals zusätzliche Hilfe erhalten. Wenn Sie lokalisierten Text für die Anweisung konfigurieren, wie in den folgenden Anleitungen beschrieben, zeigt MBAM die lokalisierte Version an. Wenn MBAM die lokalisierte Version nicht findet, wird der Wert im **HelpdeskText** -Parameter angezeigt.

**Hinweis**  In den folgenden Anleitungen ist *Selfservice* der Standardname für das virtuelle Verzeichnis für das Self-Service-Portal. Wenn Sie das Self-Service-Portal konfiguriert haben, haben Sie möglicherweise einen anderen Namen verwendet.

 

**So zeigen Sie eine lokalisierte Version der HelpdeskText-Anweisung an**

1.  Navigieren Sie auf dem Server, auf dem Sie das Self-Service-Portal konfiguriert haben, zu **Websites** &gt; **Microsoft BitLocker-Verwaltung und überwachen** von &gt; **Selfservice** - &gt; **Anwendungseinstellungen**.

2.  Klicken Sie im Bereich **Aktionen** auf **Hinzufügen** , um das Dialogfeld **Anwendungseinstellung hinzufügen** zu öffnen.

3.  Geben Sie im Feld **Name den Namen** **HelpdeskText**\ _ &lt; *Language*ein &gt; , wobei &lt; *Sprache* &gt; der für den Text geeignete Sprachcode ist.

    Um beispielsweise eine lokalisierte HelpdeskText-Anweisung in Spanisch zu erstellen, benennen Sie den Parameter **HelpdeskText \ _ES-es**.

    Der Name des Sprach Ordners kann auch der sprachneutrale Name **es** anstelle von **es-es**sein. Wenn der Browser des Endbenutzers auf **es-es** festgelegt ist und dieser Ordner nicht vorhanden ist, wird das übergeordnete Gebietsschema (wie in .net definiert) rekursiv abgerufen und überprüft, und es wird in &lt; MBAM Self-Service-Installationsverzeichnis &gt;\\SelfServiceWebsite\\es\\Notice.txt, bevor es endgültig zur Standard Notice.txt Datei wird. Dieser rekursiven Fallback imitiert die Load-Regeln für .NET-Ressourcen.

    Eine Liste der gültigen Sprachcodes, die Sie verwenden können, finden Sie unter [National Language Support (NLS)-API-Referenz](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  Geben Sie im Feld **Wert** den lokalisierten Text ein, der Endbenutzern angezeigt werden soll.



## Verwandte Themen


[Anpassen des Self-Service-Portals für Ihre Organisation](customizing-the-self-service-portal-for-your-organization.md)

 

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



