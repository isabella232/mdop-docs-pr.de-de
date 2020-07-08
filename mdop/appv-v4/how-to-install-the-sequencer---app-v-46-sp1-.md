---
title: Installieren des Sequencer (App-V 4,6 SP1)
description: Installieren des Sequencer (App-V 4,6 SP1)
author: dansimp
ms.assetid: fe8eb876-28fb-46ae-b592-da055107e639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 611564e861d65dcd357c58732fb60dab21c05abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807040"
---
# Installieren des Sequencer (App-V 4,6 SP1)


Der Microsoft Application Virtualization (App-V)-Sequenzer überwacht und zeichnet den Installations-und Einrichtungsprozess für Anwendungen auf, damit die Anwendung als virtuelle Anwendung ausgeführt werden kann. Installieren Sie den App-V-Sequencer auf einem Computer, auf dem nur das Betriebssystem installiert ist. Alternativ können Sie den Sequencer auf einem Computer installieren, der in einer virtuellen Umgebung ausgeführt wird, beispielsweise einem virtuellen Computer. Diese Methode ist hilfreich, da es einfacher ist, eine saubere Sequenz Umgebung beizubehalten, die Sie mit minimaler zusätzlicher Konfiguration wieder verwenden können.

Sie müssen über Administratorrechte auf dem Computer verfügen, den Sie zum Sequenzieren der Anwendung verwenden, und auf dem Computer darf keine Version von App-V Client ausgeführt werden. Das Erstellen einer virtuellen Anwendung mit dem App-V-Sequencer erfordert mehrere Vorgänge, daher ist es wichtig, dass Sie den Sequencer auf einem Computer installieren, der die [Hardware-und Software Anforderungen für Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md)erfüllt oder überschreitet.

**Hinweis:**  
Das Ausführen des App-V-Sequencers im abgesicherten Modus wird nicht unterstützt.



**So installieren Sie den Microsoft Application Virtualization Sequencer**

1.  Kopieren Sie die Installationsdateien von Microsoft Application Virtualization Sequencer auf den Computer, auf dem Sie Sie installieren möchten.

2.  Doppelklicken Sie auf **Setup.exe**, um den Installations-Assistenten für Microsoft Application Virtualization Sequencer zu starten. Wenn das **Microsoft Visual C++ SP1 Redistributable Package (x86)** vor der Installation nicht erkannt wird, klicken Sie auf **Installieren** , um die erforderliche Voraussetzung zu installieren.

3.  Klicken Sie auf der Seite **Willkommen** auf **weiter**, um die Installation fortzusetzen.

4.  Klicken Sie auf der Seite **Lizenzvertrag** auf **Ich stimme den Bedingungen**des Lizenzvertrags zu, um die Bedingungen des Lizenzvertrags zu akzeptieren, und klicken Sie dann auf **weiter**.

5.  Klicken Sie auf der Seite **Zielordner** auf **weiter**, um den Standardinstallationsordner zu übernehmen. Wenn Sie einen anderen Zielordner angeben möchten, klicken Sie auf **ändern** , und geben Sie den Installationsordner an, der für die Installation verwendet wird. Klicken Sie auf **Weiter**.

6.  Klicken Sie auf der Seite **virtuelles Laufwerk** auf **weiter**, um das Standardlaufwerk **Q:\\** (Standard) für Application Virtualization als das Laufwerk zu konfigurieren, von dem alle sequenzierten Anwendungen ausgeführt werden. Wenn Sie einen anderen Laufwerkbuchstaben angeben möchten, verwenden Sie die Liste, und wählen Sie den Laufwerkbuchstaben aus, den Sie verwenden möchten, indem Sie den entsprechenden Laufwerkbuchstaben auswählen, und klicken Sie dann auf **weiter**.

    **Wichtig**  
    Der mit diesem Schritt angegebene Application Virtualization-Laufwerkbuchstabe ist der Laufwerkbuchstabe, auf dem virtuelle Anwendungen auf Zielcomputern ausgeführt werden. Der angegebene Laufwerkbuchstabe muss verfügbar sein und auf den Computern, auf denen der App-V-Client ausgeführt wird, derzeit nicht verwendet werden. Wenn das angegebene Laufwerk bereits verwendet wird, schlägt die virtuelle Anwendung auf dem Zielcomputer fehl.



7.  Klicken Sie auf der Seite **bereit zum Installieren des Programms** auf **Installieren**, um die Installation zu starten.

8.  Klicken Sie auf der Seite **abgeschlossen des InstallShield-Assistenten** auf **Fertig stellen**, um den Installations-Assistenten zu schließen und den App-V-Sequenzer zu öffnen. Wenn Sie den Installations-Assistenten schließen möchten, ohne den Sequencer zu öffnen, deaktivieren Sie **das Programm starten**, und klicken Sie dann auf **Fertig stellen**.

    **Hinweis:**  
    Wenn Sie den App-V-Sequencer auf einem Computer mit einer virtuellen Umgebung, beispielsweise einem virtuellen Computer, installiert haben, müssen Sie jetzt einen Schnappschuss erstellen. Nachdem Sie eine Anwendung sequenziert haben, können Sie zu diesem Bild zurückkehren, sodass Sie die nächste Anwendung sequenzieren können.



~~~
When you uninstall the Sequencer, the following registry keys are not removed from the computer that the Sequencer was installed on. Additionally, you must restart the computer after you have uninstalled the Sequencer so that all associated drivers can be stopped and the operation can be completed.

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey**
~~~

## Verwandte Themen


[Konfigurieren von Application Virtualization Sequencer (App-V 4.6 SP1)](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)









