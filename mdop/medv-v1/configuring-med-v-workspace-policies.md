---
title: Konfigurieren von MED-V-Arbeitsbereichsrichtlinien
description: Konfigurieren von MED-V-Arbeitsbereichsrichtlinien
author: dansimp
ms.assetid: 0eaed981-cbf3-4b16-a4b7-4705c5705dc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84bdae38b1c801e2c2be2a3dd1d12dd2ca7d932d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810807"
---
# Konfigurieren von MED-V-Arbeitsbereichsrichtlinien


Eine MED-V-Arbeitsbereichs Richtlinie ist eine Gruppe von konfigurierbaren Einstellungen, die definieren, wie die virtualisierte Umgebung und Anwendungen auf dem Hostcomputer ausgeführt werden. In den Themen in diesem Abschnitt werden alle konfigurierbaren Einstellungen in der Med-v-Arbeitsbereichs Richtlinie sowie die Auswirkungen dieser Einstellungen auf den Med-v-Arbeitsbereich beschrieben.

Die folgenden MED-V-Arbeitsbereichstypen sind verfügbar:

-   **Persistent**– in einem beständigen Med-v-Arbeitsbereich werden alle Änderungen und Ergänzungen, die der Benutzer am Med-v-Arbeitsbereich vornimmt, im Med-v-Arbeitsbereich zwischen Sitzungen gespeichert. Darüber hinaus wird ein beständiger MED-V-Arbeitsbereich in der Regel in einer Domänenumgebung verwendet.

-   **Revertible**– in einem Revertible Med-v-Arbeitsbereich wird nach Abschluss jeder Sitzung (d. h., wenn der Med-v-Arbeitsbereich beendet wird) der Med-v-Arbeitsbereich während der Bereitstellung in seinen ursprünglichen Zustand zurückgesetzt. Keine Änderungen oder Ergänzungen, die der Benutzer vorgenommen hat, werden im MED-V-Arbeitsbereich zwischen Sitzungen gespeichert. Ein revertible MED-V-Arbeitsbereich kann in einer Domänenumgebung nicht verwendet werden.

Es ist wichtig, dass Sie sich für den Typ des Med-v-Arbeitsbereichs entscheiden, den Sie vor der Bereitstellung des Med-v-Arbeitsbereichs erstellen, da es nicht empfehlenswert ist, den Typ des Med-v-Arbeitsbereichs neu zu konfigurieren, nachdem eine Richtlinie für die Benutzer bereitgestellt wurde.

**Hinweis**  Beim Konfigurieren einer Richtlinie wird neben obligatorischen Feldern, die nicht ausgefüllt sind, ein Warnsymbol angezeigt. Wenn ein Pflichtfeld nicht ausgefüllt ist, wird das Symbol ebenfalls auf der Registerkarte angezeigt.

 

## Inhalt dieses Abschnitts


<a href="" id="how-to-apply-general-settings-to-a-med-v-workspace"></a>[So wenden Sie allgemeine Einstellungen auf einen MED-V-Arbeitsbereich an](how-to-apply-general-settings-to-a-med-v-workspace.md)  
Beschreibt die allgemeinen Einstellungen eines MED-V-Arbeitsbereichs und erläutert, wie Sie auf eine Richtlinie angewendet werden.

<a href="" id="how-to-apply-virtual-machine-settings-to-a-med-v-workspace"></a>[So wenden Sie die Einstellungen des virtuellen Computers auf einen MED-V-Arbeitsbereich an](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)  
Beschreibt die Einstellungen für den virtuellen Computer für einen MED-V-Arbeitsbereich und erläutert, wie Sie auf eine Richtlinie angewendet werden.

<a href="" id="how-to-configure-a-domain-user-or-group"></a>[So konfigurieren Sie einen Domänenbenutzer oder eine Gruppe](how-to-configure-a-domain-user-or-groupmedvv2.md)  
Beschreibt, wie Domänenbenutzer und-Gruppen konfiguriert werden.

<a href="" id="how-to-configure-published-applications"></a>[So konfigurieren Sie veröffentlichte Anwendungen](how-to-configure-published-applicationsmedvv2.md)  
Beschreibt veröffentlichte Anwendungen und Menüs sowie Informationen dazu, wie Sie auf eine Richtlinie angewendet werden.

<a href="" id="how-to-configure-web-settings-for-a-med-v-workspace"></a>[So konfigurieren Sie Webeinstellungen für einen MED-V-Arbeitsbereich](how-to-configure-web-settings-for-a-med-v-workspace.md)  
Beschreibt die Webeinstellungen, die für einen MED-V-Arbeitsbereich verfügbar sind, und erläutert, wie Sie auf eine Richtlinie angewendet werden.

<a href="" id="how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace"></a>[So konfigurieren Sie die Einrichtung des virtuellen Computer für einen MED-V-Arbeitsbereich](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace.md)  
Beschreibt das Einrichten eines virtuellen Computers für einen MED-V-Arbeitsbereich und die Anwendung auf eine Richtlinie.

<a href="" id="how-to-apply-network-settings-to-a-med-v-workspace"></a>[Anwenden von Netzwerkeinstellungen auf einen MED-V-Arbeitsbereich](how-to-apply-network-settings-to-a-med-v-workspace.md)  
Beschreibt die Netzwerkeinstellungen eines MED-V-Arbeitsbereichs und erläutert, wie Sie auf eine Richtlinie angewendet werden.

<a href="" id="how-to-apply-performance-settings-to-a-med-v-workspace"></a>[So wenden Sie Leistungseinstellungen auf einen MED-V-Arbeitsbereich an](how-to-apply-performance-settings-to-a-med-v-workspace.md)  
Beschreibt die Leistungseinstellungen eines MED-V-Arbeitsbereichs und erläutert, wie Sie auf eine Richtlinie angewendet werden.

<a href="" id="how-to-import-and-export-a-policy"></a>[Importieren und Exportieren einer Richtlinie](how-to-import-and-export-a-policy.md)  
Beschreibt, wie Sie eine Richtlinie importieren und exportieren.

 

 





