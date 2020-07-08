---
title: So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.0 für einen bestimmten Benutzer
description: So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.0 für einen bestimmten Benutzer
ms.assetid: dad25992-3c75-4b7d-b4c6-c2edf43baaea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a17d9dad11092a4c8356983b70bea3c18da1be04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805306"
---
# So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.0 für einen bestimmten Benutzer

*Hinweis:** App-V 4,6 hat den Mainstream-Support verlassen.

Gehen Sie wie folgt vor, um mit App-V erstellte Pakete mithilfe der Benutzerkonfigurationsdatei zu migrieren.

**So konvertieren Sie ein Paket**

1. Suchen Sie die Benutzerkonfigurationsdatei für das Paket, das Sie konvertieren möchten. Um die Richtlinie festzulegen, führen Sie die folgenden Updates im **userConfiguration** -Abschnitt aus: **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; Paket-ID &gt; **.

   Der folgende Code ist ein Beispiel für eine Benutzerkonfigurationsdatei:

   &lt;? XML-Version = "1.0"?&gt;

   &lt;UserConfiguration &lt; -Paket-ID = Paket-ID &gt; Display &lt; Name = Name des Pakets&gt;

   xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"

   PackageName = &lt; Paket-ID&gt;

   &lt;/UserConfiguration&gt;

2. Zum Hinzufügen des App-V 5,0-Pakets geben Sie Folgendes in einer erhöhten PowerShell-Eingabeaufforderung ein:

   PS &gt; **$pkg = Add-AppvClientPackage – Pfad** &lt; zum Paketspeicherort&gt;

   PS &gt; **Publish-AppVClientPackage $pkg-DynamicUserConfiguration** &lt; Pfad zur Benutzerkonfigurationsdatei&gt;

3. Öffnen Sie die Anwendung jetzt über FTA oder Verknüpfungen. Die Anwendung sollte mit App-V 5,0 geöffnet werden.

   Das App-v SP2-Paket und das konvertierte App-v 5,0-Paket werden für den Benutzer veröffentlicht, aber die FTA-und Tastenkombinationen für die Anwendungen wurden vom APP-v 5,0-Paket übernommen.

   Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.0](operations-for-app-v-50.md)

 

 





