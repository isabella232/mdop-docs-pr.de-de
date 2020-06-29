---
title: Aktualisieren von MED-V 2.0
description: Aktualisieren von MED-V 2.0
author: dansimp
ms.assetid: beea2f54-42d7-4a17-98e0-d243a8562265
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 62e8987ec511783422b8dd336dd4f3be2008c9b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810132"
---
# Aktualisieren von MED-V 2.0


Helfen Sie, Ihr System zu sichern, indem Sie die entsprechenden Sicherheitsupdates für Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 anwenden.

## Aktualisieren von MED-V


Sie können MED-V interaktiv, vom Endbenutzer oder im Hintergrund mithilfe eines elektronischen Softwareverteilungssystems aktualisieren. Bei der Installation des Med-v-Host-Agents wird der Med-v-Host-Agent aktualisiert, und anschließend wird der Med-v-Arbeitsbereich aktualisiert, falls erforderlich. Der MED-V-Host-Agent und Gast-Agent bleiben synchron. Wenn Anwendungen vom Med-v-Arbeitsbereich ausgeführt werden, während der Med-v-Host-Agent aktualisiert wird, ist ein Neustart des Hostcomputers erforderlich, um das Update abzuschließen. Wenn keine Anwendungen ausgeführt werden, wird MED-V automatisch neu gestartet, und das Upgrade wird ohne einen Neustart des Hostcomputers durchgeführt.

Wenn Sie MED-V mithilfe eines elektronischen Softwareverteilungssystems aktualisieren, können Sie das Neustartverhalten steuern. Unterdrücken Sie dazu den Neustart, indem Sie bei der Installation von MED-V\_HostAgent\_Setup.exe an der Eingabeaufforderung **Reboot = "ReallySuppress"** eingeben. Konfigurieren Sie dann das elektronische Softwareverteilungssystem, um den 3010-Rückgabecode zu erfassen (der signalisiert, dass ein Neustart erforderlich ist), und führen Sie das Verhalten für das Festlegen des Neustarts aus.

## Verwandte Themen


[Technische Referenz für MED-V](technical-reference-for-med-v.md)

 

 





