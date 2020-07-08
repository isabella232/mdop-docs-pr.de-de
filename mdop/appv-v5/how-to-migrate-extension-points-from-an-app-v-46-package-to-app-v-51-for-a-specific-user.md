---
title: So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.1 für einen bestimmten Benutzer
description: So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.1 für einen bestimmten Benutzer
author: dansimp
ms.assetid: 19da3776-5ebe-41e1-9890-12b84ef3c1c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: e2166b0f280153ad62709b21bb3477d0c4277fcd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805300"
---
# So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.1 für einen bestimmten Benutzer


Gehen Sie wie folgt vor, um mit App-V erstellte Pakete mithilfe der Benutzerkonfigurationsdatei zu migrieren.

**Hinweis**  Bei diesem Verfahren wird davon ausgegangen, dass Sie die neueste Version von App-V 4,6 ausführen.

**So konvertieren Sie ein Paket**

1. Suchen Sie die Benutzerkonfigurationsdatei für das Paket, das Sie konvertieren möchten. Um die Richtlinie festzulegen, führen Sie die folgenden Updates im **userConfiguration** -Abschnitt aus: **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; Paket-ID &gt; **.

   Der folgende Code ist ein Beispiel für eine Benutzerkonfigurationsdatei:

   &lt;? XML-Version = "1.0"?&gt;

   &lt;UserConfiguration &lt; -Paket-ID = Paket-ID &gt; Display &lt; Name = Name des Pakets&gt;

   xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"

   PackageName = &lt; Paket-ID&gt;

   &lt;/UserConfiguration&gt;

2. Zum Hinzufügen des App-V 5,1-Pakets geben Sie Folgendes in ein erweitertes PowerShell-Eingabeaufforderungsfenster ein:

   PS &gt; **$pkg = Add-AppvClientPackage – Pfad** &lt; zum Paketspeicherort&gt;

   PS &gt; **Publish-AppVClientPackage $pkg-DynamicUserConfiguration** &lt; Pfad zur Benutzerkonfigurationsdatei&gt;

3. Öffnen Sie die Anwendung jetzt über FTA oder Verknüpfungen. Die Anwendung sollte mit App-V 5,1 geöffnet werden.

   Das App-v 4,6-Paket und das konvertierte App-v 5,1-Paket werden für den Benutzer veröffentlicht, aber die FTA-und Tastenkombinationen für die Anwendungen wurden vom APP-v 5,1-Paket übernommen.

   Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)

[So setzen Sie Erweiterungspunkte von einem App-V 5.1-Paket auf ein App-V 4.6-Paket für einen bestimmten Benutzer zurück](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)

 

 





