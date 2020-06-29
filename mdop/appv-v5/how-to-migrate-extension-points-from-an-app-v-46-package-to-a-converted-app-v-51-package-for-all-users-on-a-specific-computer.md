---
title: So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu einem konvertierten App-V 5.1-Paket für alle Benutzer eines bestimmten Computers
description: So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu einem konvertierten App-V 5.1-Paket für alle Benutzer eines bestimmten Computers
author: dansimp
ms.assetid: 4ef823a5-3106-44c5-aecc-29edf69c2fbb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 7bac244804b46309a0e0a75cb3742dfe22e92e8f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805309"
---
# So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu einem konvertierten App-V 5.1-Paket für alle Benutzer eines bestimmten Computers


Gehen Sie wie folgt vor, um Erweiterungspunkte aus einem App-v 4.6-Paket zu einem App-v 5,1-Paket unter Verwendung der Bereitstellungs Konfigurationsdatei zu migrieren.

**Hinweis**  Bei diesem Verfahren wird davon ausgegangen, dass Sie die neueste Version von App-V 4,6 ausführen.  
Für das folgende Verfahren ist kein App-V 5,1-Verwaltungsserver erforderlich.

 

**So migrieren Sie Erweiterungspunkte aus einem Paket aus einem App-v 4.6-Paket zu einem konvertierten App-v 5,1-Paket unter Verwendung der Konfigurationsdatei für die Bereitstellung**

1. Suchen Sie das Verzeichnis, das die Bereitstellungs Konfigurationsdatei für das Paket enthält, das Sie migrieren möchten. Um die Richtlinie einzurichten, führen Sie das folgende Update für den **userConfiguration** -Abschnitt aus:

   **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; Paket-ID&gt;**

   Der folgende Code ist ein Beispiel für Inhalte aus einer Konfigurationsdatei für die Bereitstellung:

   &lt;? XML-Version = "1.0"?&gt;

   &lt;DeploymentConfiguration

   xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration> " Paket &lt; -ID = Paket-ID &gt; Display &lt; Name = Anzeige Name&gt;

   &lt;MachineConfiguration/&gt;

   &lt;UserConfiguration&gt;

   &lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true"

   PackageName = &lt; Paket-ID&gt;

   &lt;/UserConfiguration&gt;

   &lt;/DeploymentConfiguration&gt;

2. Um das App-V 5,1-Paket hinzuzufügen, geben Sie in einer erhöhten PowerShell-Eingabeaufforderung Folgendes ein:

   PS &gt; **$pkg = Add-AppvClientPackage** **–** Path &lt; path to Package Location &gt;  - **DynamicDeploymentConfiguration** &lt; path to the Deployment Configuration File&gt;

   PS &gt; **Publish-AppVClientPackage $pkg**

3. Um die Migration zu testen, öffnen Sie die virtuelle Anwendung mithilfe zugehöriger Freihandelsabkommen oder Verknüpfungen. Die Anwendung wird mit App-V 5,1 geöffnet. Sowohl das App-v 4,6-Paket als auch das konvertierte App-v 5,1-Paket werden für den Benutzer veröffentlicht, aber die FTA-und Tastenkombinationen für die Anwendungen wurden vom APP-v 5,1-Paket übernommen.

   Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[So setzen Sie Erweiterungspunkte von einem App-V 5.1-Paket auf ein App-V 4.6-Paket für alle Benutzer eines bestimmten Computers zurück](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Vorgänge für App-V 5.1](operations-for-app-v-51.md)

 

 





