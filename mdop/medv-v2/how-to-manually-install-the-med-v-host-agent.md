---
title: So installieren Sie den MED-V-Host-Agent manuell
description: So installieren Sie den MED-V-Host-Agent manuell
author: dansimp
ms.assetid: 4becc90b-6481-4e1f-a4d3-aec74c8821ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a7fb44b23a390cf394af2331152955afc2d8eba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804571"
---
# So installieren Sie den MED-V-Host-Agent manuell


Es gibt zwei getrennte, aber verwandte Komponenten für die Microsoft Enterprise Desktop Virtualization (Med-v) 2,0-Lösung: den Med-v-Host-Agent und den Gast-Agent. Der Host-Agent befindet sich auf dem Hostcomputer (dem Computer eines Benutzers, auf dem Windows 7 ausgeführt wird) und stellt einen Kanal für die Kommunikation mit dem Med-v-Gast bereit (dem virtuellen Med-v-Computer, der auf dem Hostcomputer ausgeführt wird). Darüber hinaus bietet es bestimmte MED-V-verwandte Funktionen, wie etwa die Anwendungsveröffentlichung.

In der Regel stellen und installieren Sie den MED-V-Host-Agent unter Verwendung der bevorzugten Software Bereitstellungsmethode Ihres Unternehmens. Vor der Bereitstellung von MED-V im gesamten Unternehmen empfiehlt es sich jedoch, den Host-Agent lokal für Tests zu installieren. In diesem Abschnitt finden Sie Schritt-für-Schritt-Anweisungen für die manuelle Installation des MED-V-Host-Agents.

**Hinweis**  Der MED-V-Gast-Agent wird während der erstmaligen Einrichtung automatisch installiert.

 

**Wichtig**  Schließen Sie Internet Explorer, bevor Sie den MED-V-Host-Agent installieren, andernfalls können Konflikte später bei der URL-Umleitung auftreten. Sie können dies auch tun, indem Sie während einer Verteilung einen Neustart des Computers angeben.

 

**So installieren Sie den MED-V-Host-Agent**

1.  Suchen Sie die MED-V-Installationsdateien, die Sie im Rahmen des Software Downloads erhalten haben.

2.  Doppelklicken Sie auf die MED-V \ _HostAgent \ _setup Installationsdatei.

    Der **Microsoft Enterprise Desktop Virtualization (MED-V)-Setup-** Assistent wird geöffnet. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

3.  Akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie dann auf **weiter**.

4.  Wählen Sie den Zielordner für die Installation des MED-V-Host-Agents aus. Klicken Sie auf **Weiter**.

5.  Klicken Sie auf **Installieren**, um mit der Installation des Host-Agents zu beginnen.

6.  Nachdem die Installation erfolgreich abgeschlossen wurde, klicken Sie auf **Fertig stellen** , um den Assistenten zu schließen.

    Um zu überprüfen, ob die Installation des Host-Agents erfolgreich war, klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Enterprise Desktop Virtualization**, und klicken Sie dann auf **MED-V-Host-Agent**.

**Hinweis**  Bis ein Med-v-Arbeitsbereich installiert ist, kann der Med-v-Host-Agent gestartet und ausgeführt werden, bietet jedoch keine Funktionalität.

 

## Verwandte Themen


[So stellen Sie die MED-V-Komponenten über ein elektronisches Softwareverteilungssystem bereit](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md)

[So installieren Sie den Arbeitsbereichs-Packager für MED-V](how-to-install-the-med-v-workspace-packager.md)

[So deinstallieren Sie die MED-V-Komponenten](how-to-uninstall-the-med-v-components.md)

 

 





