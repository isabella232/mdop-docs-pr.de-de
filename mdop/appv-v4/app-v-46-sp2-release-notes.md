---
title: App-V 4.6 SP2 – Versionshinweise
description: App-V 4.6 SP2 – Versionshinweise
author: dansimp
ms.assetid: abb536f0-e187-4c5b-952a-f837abd10ad2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cf36a6361e6f49c2b868c6752e1b2eb379cc9a31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809298"
---
# App-V 4.6 SP2 – Versionshinweise


**Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.**

Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft Application Virtualization (App-V) 4.6 SP2 installieren.

Diese Anmerkungen zu dieser Version enthalten Informationen, die zur erfolgreichen Installation von Application Virtualization 4,6 SP2 erforderlich sind. Die Anmerkungen zu dieser Version enthalten auch Informationen, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es einen Unterschied zwischen diesen Versionshinweisen und einer anderen APP-v 4.6 SP2-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## Informationen zur Produktdokumentation


Weitere Informationen zur Dokumentation für App-V finden Sie auf der Seite [Application Virtualization](https://go.microsoft.com/fwlink/?LinkID=232982) auf Microsoft TechNet.

## Abgeben von Feedback


Wir sind an Ihrem Feedback zu app-v 4.6 SP2 interessiert. Sie können Ihr Feedback an senden <mdopdocs@microsoft.com> .

**Hinweis**  Diese e-Mail-Adresse ist kein Supportkanal, aber Ihr Feedback wird uns helfen, zukünftige Änderungen für unsere Dokumentation und Produktversionen zu planen.

 

Die neuesten Informationen zu MDOP und weiteren Lernressourcen finden Sie auf der Seite [MDOP-Informationen](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Wenn Sie weitere Informationen zu neuen Updates oder Feedback geben möchten, folgen Sie uns auf [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) oder [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## <a href="" id="known-issues-with-app-v-4-6-sp2-"></a>Bekannte Probleme mit App-v 4.6 SP2


### Die Unterstützung für kurze Dateinamen ist für physikalische Laufwerke ohne System deaktiviert, wenn Sie eine Sequenz

Wenn Sie eine Sequenz unter Windows 8 oder Windows Server 2012 ablaufen, ist die Unterstützung für kurze Dateinamen (8,3) standardmäßig für physikalische Laufwerke ohne System deaktiviert.

Das dem primären virtuellen Anwendungsverzeichnis zugeordnete physikalische Laufwerk (beispielsweise "Q:\\appname") auf der Sequenz Station muss eine Unterstützung für kurze Dateinamen (8,3) bereitstellen, damit der APP-v 4.6 SP2-Sequenzer beim Erstellen von virtuellen Anwendungspaketen kurze Dateinamen generiert. Die Unterstützung für kurze Dateinamen (8,3) ist standardmäßig für physikalische Laufwerke ohne System unter Windows 8 oder Windows Server 2012 deaktiviert.

**Problemumgehung:** Aktivieren Sie die Unterstützung für kurze Dateinamen (8,3) auf nicht-System physikalischen Laufwerken. Sie können den folgenden Befehl verwenden, um eine kurze Dateinamen Unterstützung unter Windows 8 oder Windows Server 2012 zu aktivieren.

``` syntax
fsutil 8dot3name set <virtual drive letter>:
```

Verwenden Sie beispielsweise den folgenden Befehl, wenn der Laufwerkbuchstabe "Q:" lautet:

``` syntax
fsutil 8dot3name set Q: 0
```

**Hinweis**  Sie müssen diese Einstellung auf dem App-v-Client nicht ändern, da das App-v-Dateisystem in Windows 8 oder Windows Server 2012 kurze Pfade richtig verarbeitet.

 

### <a href="" id="-------------app-v-does-not-override-the-default-handler-for-file-type-or-protocol-associations-on-windows-8"></a> App-V überschreibt den Standardhandler für Dateityp-oder Protokollzuordnungen unter Windows 8 nicht

Wenn Sie mithilfe von **Standardprogrammen** in der **System** Steuerung unter Windows 8 eine Standardanwendung auswählen, werden die zugeordneten Dateitypzuordnungen für diese Anwendung nicht von App-V überschrieben.

**Problemumgehung:** Keine.

### Virtualisierte Outlook 2010 wird nicht als Option für mailto-klickable-Links unter Windows 8 angeboten

Die mailto-Shell-Erweiterung bietet keine virtualisierten Outlook 2010 unter Windows 8. Wenn Sie beispielsweise auf eine mailto:-Verknüpfung von virtualisierten Outlook 2010 klicken, die unter Windows 8 ausgeführt wird, wird kein neues e-Mail-Fenster erstellt. Diese Option funktioniert unter Windows 7 und früheren Versionen des Windows-Betriebssystems ordnungsgemäß.

**Problemumgehung:** Keine.

### <a href="" id="-------------application-virtualization-4-6-sp2-update-is-not-offered-on-all-locales-that-use-microsoft-update"></a> Application Virtualization 4,6 SP2-Update wird nicht in allen Gebietsschemas angeboten, die Microsoft Update verwenden

Wenn Sie Microsoft Update verwenden, steht das Update für App-v 4.6 SP2 für die folgenden Sprachgebietsschemas nicht zur Verfügung:

-   Kasachisch

-   Hindi

-   Serbisch-Kyrillisch

**Problemumgehung:** Wenn Sie Microsoft Windows Server Update Services (WSUS) verwenden, verwenden Sie die englische Version des Updates, oder laden Sie das Update aus dem Microsoft Update-Katalog herunter.

## Anmerkungen zu dieser Version Copyright-Informationen


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune und WindowsPowerShell sind Marken der Microsoft-Unternehmensgruppe. Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.



## Verwandte Themen


[Informationen zu Microsoft Application Virtualization 4.6SP2](about-microsoft-application-virtualization-46-sp2.md)

 

 





