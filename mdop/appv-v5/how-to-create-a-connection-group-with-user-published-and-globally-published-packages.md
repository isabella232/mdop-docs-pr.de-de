---
title: So erstellen Sie eine Verbindungsgruppe mit von Benutzern und global veröffentlichten Paketen
description: So erstellen Sie eine Verbindungsgruppe mit von Benutzern und global veröffentlichten Paketen
author: dansimp
ms.assetid: 82f7ea7f-7b14-4506-8940-fdcd6c3e117f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: c98981180133881909db17d19cb42771f94bd66a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805663"
---
# So erstellen Sie eine Verbindungsgruppe mit von Benutzern und global veröffentlichten Paketen
Mit einer der folgenden Methoden können Sie Benutzer berechtigte Verbindungsgruppen erstellen, die sowohl von Benutzern veröffentlichte als auch Global veröffentlichte Pakete enthalten:

-   [Verwenden von PowerShell-Cmdlets zum Erstellen der Benutzer berechtigten Verbindungsgruppen](#bkmk-posh-userentitled-cg)

-   [Verwenden des App-V-Servers zum Erstellen der Benutzer berechtigten Verbindungsgruppen](#bkmk-appvserver-userentitled-cg)

**Was Sie wissen sollten, bevor Sie beginnen:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nicht unterstützte Szenarien und potenzielle Probleme</th>
<th align="left">Ergebnis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Sie können keine von Benutzern veröffentlichten Pakete in Global berechtigte Verbindungsgruppen einbeziehen.</p></td>
<td align="left"><p>Bei der Verbindungsgruppe tritt ein Fehler auf.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Wenn Sie ein Paket auf globaler Ebene veröffentlichen und dann eine von Benutzern veröffentlichte Verbindungsgruppe erstellen, in der Sie dieses Paket nicht optional erstellt haben, können Sie weiterhin <strong> die Veröffentlichung von "Publish-AppvClientPackage &lt; Package-Global" ausführen, &gt; </strong> um die Veröffentlichung des Pakets aufzuheben, auch wenn dieses Paket in einer anderen Verbindungsgruppe verwendet wird.</p></td>
<td align="left"><p>Wenn das Paket von anderen Verbindungsgruppen verwendet wird, schlägt das Paket in diesen Verbindungsgruppen fehl.</p>
<p>Um die Veröffentlichung eines nicht optionalen Pakets, das in einer anderen Verbindungsgruppe verwendet wird, unbeabsichtigt zu verhindern, empfehlen wir, dass Sie die Verbindungsgruppen nachvollziehen, in denen Sie ein nicht optionales Paket verwendet haben.</p></td>
</tr>
</tbody>
</table>

 
<a href="" id="bkmk-posh-userentitled-cg"></a>**Verwenden von PowerShell-Cmdlets zum Erstellen von Benutzer berechtigten Verbindungsgruppen**

1.  Verwenden Sie die folgenden Befehle, um Pakete hinzuzufügen und zu veröffentlichen:

    **Add-AppvClientPackage package1 \ _AppV \ _File \ _Path**

    **Add-AppvClientPackage Package2 \ _AppV \ _File \ _Path**

    **Publish-AppvClientPackage-Package-package1 \ _ID-Version package1 \ _Version ID – Global**

    **Publish-AppvClientPackage-Package-Package2 \ _ID-VersionIdPackage2 \ _ID**

2.  Erstellen Sie die XML-Datei der Verbindungsgruppe. Weitere Informationen finden Sie unter [Informationen zur Verbindungsgruppen Datei](about-the-connection-group-file.md).

3.  Fügen Sie die Verbindungsgruppe mithilfe der folgenden Befehle hinzu, und veröffentlichen Sie Sie:

    **Add-AppvClientConnectionGroup Connection \ _Group \ _XML \ _File \ _Path**

    **Aktivieren-AppvClientConnectionGroup-Gruppen-CG \ _Group \ _ID-Version-Nr CG \ _Version \ _ID**

<a href="" id="bkmk-appvserver-userentitled-cg"></a>**Verwenden des App-V-Servers zum Erstellen von Benutzer berechtigten Verbindungsgruppen**

1.  Öffnen Sie die App-V 5,0-Verwaltungskonsole.

2.  Befolgen Sie die Anweisungen unter [Veröffentlichen eines Pakets mithilfe der Verwaltungskonsole](how-to-publish-a-package-by-using-the-management-console-50.md) , um Pakete Global und für den Benutzer zu veröffentlichen.

3.  Befolgen Sie die Anweisungen unter [Erstellen einer Verbindungsgruppe](how-to-create-a-connection-group.md) , um die Verbindungsgruppe zu erstellen, und fügen Sie die von Benutzern veröffentlichten und Global veröffentlichten Pakete hinzu.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Verwalten von Verbindungsgruppen](managing-connection-groups.md)

[So verwenden Sie optionale Pakete in Verbindungsgruppen](how-to-use-optional-packages-in-connection-groups.md)

 

 





