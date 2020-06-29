---
title: So deinstallieren Sie App-V Client
description: So deinstallieren Sie App-V Client
author: dansimp
ms.assetid: 07591270-9651-4bb5-a5b3-e0fc009bd9e2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: acb3f53b42027ff2c1b84fd2ab2bdde3c52f96de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806740"
---
# So deinstallieren Sie App-V Client


Gehen Sie wie folgt vor, um den Application Virtualization-Client auf dem Computer zu deinstallieren.

**So deinstallieren Sie den Application Virtualization-Desktop Client**

1.  Doppelklicken Sie in der Systemsteuerung auf **Software** (oder in Windows Vista, **Programme und Funktionen**), und doppelklicken Sie dann auf **Microsoft Application Virtualization Desktop Client**.

2.  Klicken Sie im daraufhin angezeigten Dialogfeld auf **Ja** , um den Deinstallationsvorgang fortzusetzen.

    **Wichtig**  Der Deinstallationsprozess kann nicht abgebrochen oder unterbrochen werden.

     

3.  Wenn eine Meldung angezeigt wird, die besagt, dass die Microsoft Application Virtualization Client Tray-Anwendung geschlossen werden muss, bevor Sie fortfahren, klicken Sie mit der rechten Maustaste auf das App-V-Symbol im Infobereich, und wählen Sie **Beenden** aus, um die Anwendung zu schließen. Klicken Sie dann auf wieder **holen** , um den Deinstallationsvorgang fortzusetzen.

    **Wichtig**  Möglicherweise wird eine Meldung angezeigt, die besagt, dass eine oder mehrere virtuelle Anwendungen verwendet werden. Schließen Sie alle geöffneten Anwendungen, und speichern Sie Ihre Daten, bevor Sie fortfahren. Klicken Sie dann auf **OK** , um den Deinstallationsvorgang fortzusetzen.

     

4.  Eine Fortschrittsleiste zeigt die verbleibende Zeit an. Wenn dieser Schritt abgeschlossen ist, müssen Sie den Computer neu starten, damit alle zugehörigen Treiber beendet werden können, um den Deinstallationsvorgang abzuschließen.

    **Hinweis**  Die folgenden Registrierungsschlüssel bleiben nach Abschluss des Deinstallationsvorgangs erhalten:

    -   HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid

    -   HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid\\4.5

    -   HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid\\4.5\\systemguard "Client" = DWORD: 00000000

    -   HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid\\4.5\\systemguard\\seckey

     

## Verwandte Themen


[So installieren Sie den Client über die Befehlszeile](how-to-install-the-client-by-using-the-command-line-new.md)

[So installieren Sie Application Virtualization Client manuell](how-to-manually-install-the-application-virtualization-client.md)

[So veröffentlichen Sie eine virtuelle Anwendung auf dem Client](how-to-publish-a-virtual-application-on-the-client.md)

 

 





