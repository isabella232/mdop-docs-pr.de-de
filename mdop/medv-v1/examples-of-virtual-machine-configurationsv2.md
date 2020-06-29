---
title: Beispiele für VM-Konfigurationen
description: Beispiele für VM-Konfigurationen
author: dansimp
ms.assetid: 5937601e-41ab-4ca2-8fa1-3c9154710cd6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b9fc7b1f88b2b30ea149fe73a387826fdbb2a66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810645"
---
# Beispiele für VM-Konfigurationen


Im folgenden finden Sie Beispiele für typische Konfigurationen virtueller Computer: eine in einem beständigen Med-v-Arbeitsbereich und eine in einem revertible Med-v-Arbeitsbereich.

**Hinweis**  Diese Beispiele sind nicht für die Verwendung in allen Umgebungen vorgesehen. Passen Sie die Konfiguration entsprechend Ihrer Umgebung an.

 

**So konfigurieren Sie eine typische Domänen Einrichtung in einem beständigen MED-V-Arbeitsbereich**

1.  Konfigurieren Sie Sysprep für das Basis Bild, um eine eindeutige SID zu erstellen. Weitere Informationen finden Sie unter [Erstellen eines virtuellen PC-Images für MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).

2.  Aktivieren Sie auf der Registerkarte **VM-Setup** das Kontrollkästchen **VM-Setup ausführen** .

3.  Konfigurieren Sie im Abschnitt **VM-Computer Namensmuster** das Muster für den Computerabbild Namen. Weitere Informationen finden Sie unter [Konfigurieren von Eigenschaften des VM-Computer namens Musters](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).

4.  Klicken Sie auf **Skript-Editor**, und konfigurieren Sie im Dialogfeld **VM-Setup-Skript-Editor** die folgenden Aktionen:

    1.  **Computer umbenennen**

    2.  **Windows neu starten**

    3.  **Überprüfen der Konnektivität**

    4.  **Domäne beitreten**

    5.  **Deaktivieren der automatischen Anmeldung**

    Weitere Informationen finden Sie unter [so wird es gemacht: Einrichten von Skriptaktionen](how-to-set-up-script-actions.md).

5.  Klicken Sie im Menü **Richtlinie** auf **Commit**.

**So konfigurieren Sie ein typisches Setup in einem revertible-Arbeitsbereich**

1.  Aktivieren Sie auf der Registerkarte **VM-Setup** das Kontrollkästchen VM auf der **Grundlage des Computernamens Musters umbenennen** .

2.  Konfigurieren Sie im Abschnitt **VM-Computer Namensmuster** das Muster für den Computerabbild Namen. Weitere Informationen finden Sie unter [Konfigurieren von Eigenschaften des VM-Computer namens Musters](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).

3.  Klicken Sie im Menü **Richtlinie** auf **Commit**.

## Verwandte Themen


[So konfigurieren Sie die Einrichtung des virtuellen Computer für einen MED-V-Arbeitsbereich](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[So konfigurieren Sie die Eigenschaften der Namensmuster virtueller Computer](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

[So richten Sie Skriptaktionen ein](how-to-set-up-script-actions.md)

 

 





