---
title: So konfigurieren Sie Windows Server 2008 Firewall für App-V
description: So konfigurieren Sie Windows Server 2008 Firewall für App-V
author: dansimp
ms.assetid: 57f4ed17-0651-4a3c-be1e-29d9520c6aeb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 19e4cda9ac3b908f68e4f69b9663033d8a21ae41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807219"
---
# So konfigurieren Sie Windows Server 2008 Firewall für App-V


Mit der Einführung von Windows Server2008 wurden die Firewall-und IPSec-Komponenten zu einem einzigen Dienst zusammengeführt, und die Funktionen dieses Diensts wurden verbessert. Der neue Firewalldienst unterstützt eine eingehende und ausgehende Stateful-Prüfung. Darüber hinaus können Sie mithilfe von Gruppenrichtlinien bestimmte Firewallregeln und IPSec-Richtlinien konfigurieren. Weitere Informationen zur Windows-Firewall in Windows Server2008 finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=151980> .

Das folgende Verfahren beinhaltet nicht das Hinzufügen einer Ausnahme für die ICO-und OSD-Veröffentlichung über SMB oder http/https. Diese Ausnahmen werden automatisch basierend auf dem Netzwerkprofil und den Rollen hinzugefügt, die auf der Windows Server 2008-Firewall installiert sind.

**Hinweis**  Wenn der Verwaltungs Server für die Verwendung von RTSP konfiguriert ist, wiederholen Sie diesen Vorgang, um das `sghwsvr.exe` Programm als Ausnahme hinzuzufügen.

Der App-V Streaming Server erfordert die Programmausnahme `sglwdsptr.exe` für die RTSPS-Kommunikation. Ein App-V-Streamingserver, der RTSP für die Kommunikation verwendet, erfordert auch eine Programmausnahme für `sglwsvr.exe` .

 

**So konfigurieren Sie die Windows Server2008-Firewall für App-V**

1.  Öffnen Sie die **Windows-Firewall mit Advanced Security** Management Console über die Systemsteuerung oder durch Eingabe `wf.msc` in der Zeile ausführen.

2.  Erstellen Sie eine neue eingehende Regel, und wählen Sie **Programm**aus.

3.  Wählen Sie den Programmpfad aus, und navigieren Sie zu `sghwdsptr.exe` , der standardmäßig unter gespeichert ist `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .

4.  Klicken Sie auf **Weiter**.

5.  Wählen Sie **Action** auf der Seite Aktion **die Option Verbindung zulassen**aus, und klicken Sie dann auf **weiter**.

6.  Wählen Sie die geeigneten **profile** aus, die auf die eingehende Regel angewendet werden sollen.

7.  Geben Sie einen Namen und eine Beschreibung für die Regel ein, und klicken Sie auf **Fertig stellen**.

## Verwandte Themen


[So konfigurieren Sie Windows Server 2003 Firewall für App-V](how-to-configure-windows-server-2003-firewall-for-app-v.md)

 

 





