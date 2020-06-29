---
title: So installieren Sie den App-V-Client mithilfe von Setup.exe
description: So installieren Sie den App-V-Client mithilfe von Setup.exe
author: dansimp
ms.assetid: 106a5d97-b5f6-4a16-bf52-a84f4d558c74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60f79a2d2f74848ab121ba13cdf8c215088d54db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807067"
---
# So installieren Sie den App-V-Client mithilfe von Setup.exe


In diesem Thema wird beschrieben, wie Sie den App-V-Client mit dem setup.exe-Programm installieren. Wenn Sie den App-V-Client mit dem setup.exe-Programm installieren, ermittelt das Installationsprogramm, welche erforderliche Software erforderlich ist, und installiert sie automatisch, bevor der Client installiert wird.

**So installieren Sie den Application Virtualization-Client mithilfe von Setup.exe**

1.  Stellen Sie sicher, dass Sie mit einem Konto angemeldet sind, das über Administratorrechte auf dem Computer verfügt.

2.  Öffnen Sie ein Eingabeaufforderungsfenster, und ändern Sie das Verzeichnis in den Ordner, in dem die Setupdateien enthalten sind. Wenn Sie Version 4.6 oder eine neuere Version des App-V-Clients installieren, müssen Sie das richtige Installationsprogramm für das Betriebssystem des Computers, 32-Bit oder 64-Bit verwenden. Bei der Installation tritt ein Fehler auf, und es wird eine Fehlermeldung angezeigt, wenn Sie das falsche Installationsprogramm verwenden.

3.  Geben Sie die Befehlszeichenfolge für den Installationsbefehl an der Eingabeaufforderung ein. Alternativ können Sie eine Befehlsdatei erstellen und diese über die Eingabeaufforderung ausführen. Sie können auch eine Skriptsprache wie VBScript oder Windows PowerShell verwenden, um den Befehl auszuführen.

4.  Das folgende Befehlszeilenbeispiel zeigt, wie setup.exe mit einer Reihe optionaler Parameter verwendet werden kann. Weitere Informationen zu diesen Parametern finden Sie unter [Befehlszeilenparameter für Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md).

    **"setup.exe"/s/v "/qn SWICACHESIZE = \ \" 10240 \ \ "SWIPUBSVRDISPLAY = \ \" Production System\\ "SWIPUBSVRTYPE = \ \" http/secure\\ "SWIPUBSVRHOST = \ \" PRODSYS\\ "SWIPUBSVRPORT = \ \" 443 \ \ "SWIPUBSVRPATH = \ \"/AppVirt/appsntype.xml \ \ "SWIPUBSVRREFRESH = \ \" on\\ "SWIGLOBALDATA = \ \" D:\\AppVirt\\Global\\ "SWIUSERDATA = \ \" ^% LocalAppData ^%\\Windows\\Application Virtualization Client\\ "SWIFSDRIVE = \ \" Q\\ ""**

    **Wichtig**  
    -   Die Anführungszeichen, die im Abschnitt "**/v**" angezeigt werden, müssen als Sonderzeichen behandelt und mit einem vorangehenden "" eingegeben werden **\\** . Die Anführungszeichen sind nur erforderlich, wenn der Wert ein Leerzeichen enthält. aus Gründen der Konsistenz werden jedoch alle Instanzen im vorherigen Beispiel als Anführungszeichen angezeigt.

    -   Dem "" " **%** -Zeichen in"**% HOMEDRIVE%**"muss das Escapezeichen" "vorangestellt werden **^** . Andernfalls legt die Windows-Befehlsshell den Wert auf den Wert des Benutzers fest, der die Installation ausführt.

    -   Die **InstallShield** -Schalter **/s** und **/QN** sind erforderlich, um eine unbeaufsichtigte Installation zu ermöglichen. Der **/QN** -Schalter muss dem **/v** -Schalter folgen, getrennt durch ein Anführungszeichen ohne dazwischen liegende Leerzeichen.

    -   Der im **SWIGLOBALDATA** -Wert angegebene Ordner muss bereits vorhanden sein.

     

5.  Wenn die Installation abgeschlossen ist, empfehlen wir, dass Sie einen Microsoft Update-Scan ausführen, um sicherzustellen, dass die neuesten Updates installiert sind.

## Verwandte Themen


[So installieren Sie den Client über die Befehlszeile](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





