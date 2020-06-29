---
title: Verwalten von MED-V-Arbeitsbereichseinstellungen mit dem MED-V-Arbeitsbereichs-Packager
description: Verwalten von MED-V-Arbeitsbereichseinstellungen mit dem MED-V-Arbeitsbereichs-Packager
author: dansimp
ms.assetid: e4b2c516-b9f8-44f9-9eae-caac6c2af3e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9905c8da0f1f0678cce9587296526e8f04493c20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811566"
---
# Verwalten von MED-V-Arbeitsbereichseinstellungen mit dem MED-V-Arbeitsbereichs-Packager


Sie können den Med-v Workspace-Paketer verwenden, um bestimmte Einstellungen im Med-v-Arbeitsbereich zu verwalten.

**So verwalten Sie die Einstellungen in einem MED-V-Arbeitsbereich**

1. Klicken Sie zum Öffnen des **Med-v Workspace-Pakets**auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Enterprise Desktop Virtualization**, und klicken Sie dann auf **Med-v Workspace Packager**.

2. Klicken Sie im Hauptbereich des **MED-V Workspace-Pakets** auf **Einstellungen verwalten**.

3. Im Fenster **Einstellungen verwalten** können Sie die folgenden MED-V Workspace-Einstellungen konfigurieren:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Starten des MED-V-Arbeitsbereichs</strong></p></td>
   <td align="left"><p>Wählen Sie aus, ob der Med-v-Arbeitsbereich bei der Benutzeranmeldung bei der ersten Verwendung gestartet oder der Endbenutzer entscheiden soll, wann der Med-v-Arbeitsbereich gestartet wird.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>Der Arbeitsbereich Med-v beginnt auf eine von zwei Arten: entweder beim Anmelden des Endbenutzers oder beim ersten Ausführen einer Aktion, die Med-v erfordert, beispielsweise das Öffnen einer veröffentlichten Anwendung oder das Eingeben einer URL, die eine Umleitung erfordert.</p>
   <p>Sie können diese Einstellung für den Endbenutzer definieren oder zulassen, dass der Endbenutzer steuert, wie MED-V gestartet wird.</p>
   <div class="alert">
   <strong>Hinweis:</strong><br/><p>Wenn Sie angeben, dass der Endbenutzer entscheidet, besteht das Standardverhalten darin, dass der MED-V-Arbeitsbereich bei der Anmeldung gestartet wird. Sie können die Standardeinstellung ändern, indem Sie mit der rechten Maustaste auf das Med-v-Symbol im Infobereich klicken und dann <strong> Med-v-Benutzereinstellungen auswählen </strong> . Wenn Sie diese Einstellung für den Endbenutzer definieren, können Sie die Art und Weise, in der MED-V gestartet wird, nicht ändern.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Networking</strong></p></td>
   <td align="left"><p>Wählen <strong> Sie </strong> <strong> </strong> für Ihre Netzwerkeinstellung freigegeben oder überbrückt aus. Der Standardwert ist <strong> Shared </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong>Shared </strong> - der MED-V Workspace verwendet die Netzwerkadressübersetzung (Network Address Translation, NAT), um die IP-Adresse des Host-&#39;für ausgehenden Datenverkehr freizugeben.</p>
   <p><strong>Überbrückt </strong> - der MED-V-Arbeitsbereich verfügt über eine eigene Netzwerkadresse, die in der Regel über DHCP abgerufen wird.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Speichern von Anmeldeinformationen</strong></p></td>
   <td align="left"><p>Wählen Sie aus, ob die Endbenutzeranmeldeinformationen gespeichert werden sollen.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>Das Standardverhalten ist, dass die Speicherung von Anmeldeinformationen deaktiviert ist, damit der Endbenutzer bei jeder Anmeldung authentifiziert werden muss.</p>
   <div class="alert">
   <strong>Wichtig</strong><br/><p>Auch wenn die Zwischenspeicherung der Anmeldeinformationen des Endbenutzers die beste Benutzererfahrung bietet, sollten Sie sich mit den damit verbundenen Risiken vertraut machen.</p>
   <p>Die Domänenanmeldeinformationen des Endbenutzers werden in einem reversiblen Format im Windows-Anmelde Informations-Manager gespeichert. Ein Angreifer kann ein Programm schreiben, das das Kennwort abruft und so Zugriff auf die Anmeldeinformationen des Benutzers erhält. Sie können dieses Risiko nur verringern, indem Sie die Speicherung der Anmeldeinformationen des Endbenutzers deaktivieren.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



4. Klicken Sie auf **Speichern unter...** , um die aktualisierten Konfigurationseinstellungen im angegebenen Ordner zu speichern. MED-V erstellt eine Registrierungsdatei, die die aktualisierten Einstellungen enthält. Bereitstellen der aktualisierten Registrierungsdatei mithilfe von Gruppenrichtlinien Weitere Informationen zum Verwenden von Gruppenrichtlinien finden Sie unter [Gruppenrichtlinien-Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

   MED-V erstellt auch ein Windows PowerShell-Skript im angegebenen Ordner, mit dem Sie diese aktualisierte Registrierungsdatei erneut erstellen können.

## Verwandte Themen


[Verwalten von Konfigurationseinstellungen für MED-V-Arbeitsbereiche](managing-med-v-workspace-configuration-settings.md)

[Verwalten von MED-V-Arbeitsbereichseinstellungen](manage-med-v-workspace-settings.md)









