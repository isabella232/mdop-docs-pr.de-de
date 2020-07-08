---
title: So lokalisieren Sie „HelpdeskURL“ für das Self-Service-Portal
description: So lokalisieren Sie „HelpdeskURL“ für das Self-Service-Portal
author: dansimp
ms.assetid: 86798460-077b-459b-8d54-4b605e07d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0d7ec4ce87bbe5aab56e9fa877ced5f51625a5dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811917"
---
# So lokalisieren Sie „HelpdeskURL“ für das Self-Service-Portal


Sie können eine lokalisierte Version der Self-Service-Portal-URL so konfigurieren, dass Sie Endbenutzern standardmäßig angezeigt wird. Die URL des Self-Service-Portals wird durch den Parameter **HelpdeskURL**dargestellt.

Wenn Sie eine lokalisierte Version erstellen, wie in den folgenden Anleitungen beschrieben, findet und zeigt die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) die lokalisierte Version an. Wenn MBAM keine lokalisierte Version findet, wird die für den Parameter **HelpDeskURL**konfigurierte URL angezeigt.

**Hinweis**  In den folgenden Anleitungen ist *Selfservice* der Standardname für das virtuelle Verzeichnis für das Self-Service-Portal. Wenn Sie das Self-Service-Portal konfiguriert haben, haben Sie möglicherweise einen anderen Namen verwendet.

 

**So lokalisieren Sie die Self-Service-Portal-URL**

1.  Navigieren Sie auf dem Server, auf dem Sie das Self-Service-Portal konfiguriert haben, zu **Websites** &gt; **Microsoft BitLocker-Verwaltung und überwachen** von &gt; **Selfservice** - &gt; **Anwendungseinstellungen**.

2.  Klicken Sie im Bereich **Aktionen** auf **Hinzufügen** , um das Dialogfeld **Anwendungseinstellung hinzufügen** zu öffnen.

3.  Geben Sie im Feld **Name den Namen** **HelpdeskURL**\ _ &lt; *Language*ein &gt; , wobei &lt; *Sprache* &gt; der geeignete Sprachcode für die URL ist.

    Wenn Sie beispielsweise eine lokalisierte Version des `HelpdeskURL` Werts in Spanisch erstellen möchten, benennen Sie den Parameter **HelpdeskURL \ _ES-es**.

    Der Name des Sprach Ordners kann auch der sprachneutrale Name **es** anstelle von **es-es**sein. Wenn der Browser des Endbenutzers auf **es-es** festgelegt ist und dieser Ordner nicht vorhanden ist, wird das übergeordnete Gebietsschema (wie in .net definiert) rekursiv abgerufen und überprüft, und es wird in &lt; MBAM Self-Service-Installationsverzeichnis &gt;\\SelfServiceWebsite\\es\\Notice.txt, bevor es endgültig zur Standard Notice.txt Datei wird. Dieser rekursiven Fallback imitiert die Load-Regeln für .NET-Ressourcen.

    Eine Liste der gültigen Sprachcodes, die Sie verwenden können, finden Sie unter [National Language Support (NLS)-API-Referenz](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  Geben Sie im Feld **Wert** die lokalisierte Version des Werts ein, der `HelpdeskURL` Endbenutzern angezeigt werden soll.



## Verwandte Themen


[Anpassen des Self-Service-Portals für Ihre Organisation](customizing-the-self-service-portal-for-your-organization.md)

 

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




