---
title: So stellen Sie einen MED-V-Arbeitsbereich in ein Windows 7-Image bereit
description: So stellen Sie einen MED-V-Arbeitsbereich in ein Windows 7-Image bereit
author: dansimp
ms.assetid: a83aba4e-8681-4906-9872-f431c0bb15f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49dd796d6f6af425b9000b595a0d828c3cb0035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812262"
---
# So stellen Sie einen MED-V-Arbeitsbereich in ein Windows 7-Image bereit


Sie können alle MED-V-Komponenten in einem Windows 7-Abbild installieren, das Sie in Ihrem Unternehmen genauso wie bei jeder neuen Installation von Windows 7 verteilen. Der Endbenutzer beendet dann die Installation des Med-v-Arbeitsbereichs, indem er auf eine **Start** Menü Verknüpfung klickt, die Sie zum Starten von Med-v konfiguriert haben. Das erstmalige Setup wird gestartet, und der Endbenutzer befolgt die Anweisungen, um die Konfiguration abzuschließen.

Der folgende Abschnitt enthält Informationen und Anweisungen, die Ihnen bei der Bereitstellung des MED-V-Arbeitsbereichs in Ihrem Unternehmen helfen, indem Sie ein Windows 7-Abbild verwenden.

**So stellen Sie einen MED-V-Arbeitsbereich in einem Windows 7-Abbild bereit**

1.  Erstellen Sie ein Standardbild von Windows 7. Weitere Informationen finden Sie unter [Erstellen eines Standard Abbilds von Windows 7: Schritt-für-Schritt-Anleitung](https://go.microsoft.com/fwlink/?LinkId=204843) ( https://go.microsoft.com/fwlink/?LinkId=204843) .

2.  Installieren Sie im Windows 7-Abbild Windows Virtual PC und die Windows Virtual PC-Updates. Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.

3.  Installieren Sie den Med-v-Host-Agent mithilfe der Installationsdatei Med-v \ _HostAgent \ _setup. Weitere Informationen finden Sie unter [Manuelles Installieren des MED-V-Host-Agents](how-to-manually-install-the-med-v-host-agent.md).

    **Warnung**  Internet Explorer muss geschlossen werden, bevor Sie den MED-V-Host-Agent installieren, andernfalls können Konflikte später bei der URL-Umleitung auftreten. Sie können dies auch tun, indem Sie während einer Verteilung einen Neustart des Computers angeben.

     

4.  Kopieren Sie die MED-V Workspace-Paketdateien in das Windows 7-Abbild. Die Med-v Workspace-Paketdateien sind das Med-v Workspace-Installationsprogramm, die medv-Datei und setup.exe Datei, die Sie mithilfe des **Med-v-Arbeitsbereichs-Packagers**erstellt haben.

    **Wichtig**  Die medv-und die setup.exe-Datei müssen sich im gleichen Ordner wie das MED-V Workspace-Installationsprogramm befinden. Installieren Sie dann den MED-V-Arbeitsbereich, indem Sie setup.exe ausführen.

     

5.  Konfigurieren Sie eine Verknüpfung im Menü " **Start** ", um die Installation des MED-V-Arbeitsbereichs Pakets zu öffnen.

    Erstellen Sie eine Verknüpfung im **Startmenü** mit der setup.exe-Datei, über die der Endbenutzer eine MED-V-Installation nach Bedarf starten kann.

6.  Verteilen Sie das Windows 7-Abbild mithilfe des standardmäßigen Bild Bereitstellungsprozesses Ihres Unternehmens an Computer in Ihrem Unternehmen, für die MED-V erforderlich ist.

Wenn der Endbenutzer auf eine im Med-v-Arbeitsbereich veröffentlichte Anwendung zugreifen muss, kann er auf die Verknüpfung **Start** Menü klicken, um den Med-v-Arbeitsbereich zu installieren. Dadurch wird automatisch die erstmalige Einrichtung gestartet und die Konfiguration von MED-V abgeschlossen. Nach Abschluss der erstmaligen Einrichtung kann der Endbenutzer im **Startmenü** auf die MED-V-Anwendungen zugreifen.

## Verwandte Themen


[Übersicht über die Bereitstellung von MED-V 2.0](med-v-20-deployment-overview.md)

[So stellen Sie einen MED-V-Arbeitsbereich über eines elektronischen Softwareverteilungssystem bereit](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

 

 





