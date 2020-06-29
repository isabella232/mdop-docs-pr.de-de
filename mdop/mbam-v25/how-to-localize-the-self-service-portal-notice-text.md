---
title: So lokalisieren Sie den Hinweistext für das Self-Service-Portal
description: So lokalisieren Sie den Hinweistext für das Self-Service-Portal
author: dansimp
ms.assetid: a4c878b7-e5c8-45af-a537-761bb2991659
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a2385f6b00713e7373bd1707b02324b80f300c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811920"
---
# So lokalisieren Sie den Hinweistext für das Self-Service-Portal


Sie können lokalisierten Benachrichtigungstext so konfigurieren, dass er für Endbenutzer standardmäßig im Self-Service-Portal angezeigt wird. Die Notice.txt-Datei, die den Hinweistext anzeigt, befindet sich im folgenden Stammverzeichnis:

&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website\\

Wenn Sie lokalisierten Hinweistext anzeigen möchten, erstellen Sie eine lokalisierte Notice.txt Datei, und speichern Sie Sie dann unter einem bestimmten Sprachordner im folgenden Beispielverzeichnis:

&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website\\

**Hinweis**  Sie können den Pfad mithilfe des **NoticeTextPath** -Elements in den **Anwendungseinstellungen**konfigurieren.

 

MBAM zeigt den Hinweistext auf der Grundlage der folgenden Regeln an:

-   Wenn Sie eine lokalisierte **Notice.txt** Datei im entsprechenden Sprachordner erstellen, zeigt MBAM den lokalisierten Hinweistext an, wenn die Standard **Notice.txt** Datei vorhanden ist. Wenn die Standard **Notice.txt** Datei fehlt, wird eine Meldung angezeigt, die besagt, dass die Standarddatei nicht vorhanden ist.

-   Wenn MBAM keine lokalisierte Version der Notice.txt-Datei findet, wird der Text in der standardmäßigen Notice.txt Datei angezeigt.

-   Wenn MBAM keine Standard Notice.txt Datei findet, wird der Standardtext im Self-Service-Portal angezeigt.

**Hinweis**  Wenn der Browser eines Endbenutzers auf eine Sprache festgesetzt ist, die keinen entsprechenden Unterordner "Sprache" oder Notice.txt hat, wird der Text in der Notice.txt Datei im folgenden Stammverzeichnis angezeigt:

&lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website\\

 

**So erstellen Sie eine lokalisierte Notice.txt-Datei**

1.  Erstellen Sie auf dem Server, auf dem Sie das Self-Service-Portal konfiguriert haben, einen &lt; *sprach* &gt; Ordner im folgenden Beispielverzeichnis, wobei &lt; *Sprache* &gt; den Namen der lokalisierten Sprache darstellt:

    &lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website\\

    **Hinweis**  Da einige Sprachordner bereits vorhanden sind, müssen Sie möglicherweise keinen Ordner erstellen. Wenn Sie einen Sprachordner erstellen müssen, finden Sie unter [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) eine Liste der gültigen Namen, die Sie für den &lt; *sprach* &gt; Ordner verwenden können.

     

2.  Erstellen Sie eine Notice.txt-Datei, die den lokalisierten Benachrichtigungstext enthält.

3.  Speichern Sie die Notice.txt Datei im &lt; Ordner *Sprache* &gt; . Wenn Sie beispielsweise eine lokalisierte Notice.txt Datei in Spanisch erstellen möchten, speichern Sie die lokalisierte Notice.txt Datei im folgenden Beispielverzeichnis:

    &lt;*MBAM Self-Service-Installationsverzeichnis* &gt; \\Self-Dienst Website\\Es-es

    Der Name des Sprach Ordners kann auch der sprachneutrale Name **es** anstelle von **es-es**sein. Wenn der Browser des Endbenutzers auf **es-es** festgelegt ist und dieser Ordner nicht vorhanden ist, wird das übergeordnete Gebietsschema (wie in .net definiert) rekursiv abgerufen und überprüft, und es wird in &lt; MBAM Self-Service-Installationsverzeichnis &gt;\\SelfServiceWebsite\\es\\Notice.txt, bevor es endgültig zur Standard Notice.txt Datei wird. Dieser rekursiven Fallback imitiert die Load-Regeln für .NET-Ressourcen.



## Verwandte Themen


[Anpassen des Self-Service-Portals für Ihre Organisation](customizing-the-self-service-portal-for-your-organization.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





