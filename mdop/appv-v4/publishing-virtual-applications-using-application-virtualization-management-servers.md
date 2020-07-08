---
title: Veröffentlichen von virtuellen Anwendungen mit Application Virtualization Management-Servern
description: Veröffentlichen von virtuellen Anwendungen mit Application Virtualization Management-Servern
author: dansimp
ms.assetid: f3d79284-3f82-4ca3-b741-1a80b61490da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01b85d73ed0a6a8bf723be381e947fbbc003bf6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806439"
---
# Veröffentlichen von virtuellen Anwendungen mit Application Virtualization Management-Servern


In einer auf Application Virtualization Server basierenden Bereitstellung werden virtuelle Anwendungspakete, die sequenziert, getestet und bereitgestellt wurden, in die Hauptinhalts Freigabe kopiert, die vom Application Virtualization Management Server verwendet werden soll. Nachdem die Pakete auf dem Application Virtualization-Verwaltungs Server importiert wurden, können Sie für die Endbenutzer veröffentlicht werden.

**Hinweis**  Die Inhaltsfreigabe sollte sich auf dem angeschlossenen Datenträgerspeicher des Servers befinden. Die Verwendung eines Netzwerkspeicher Geräts wie einem SAN oder einer DFS-Freigabe sollte aufgrund der Auswirkungen auf das Netzwerk sorgfältig berücksichtigt werden.

 

Anwendungen werden in Active Directory-Gruppen bereitgestellt. In der Regel erstellt der Application Virtualization-Administrator Active Directory-Gruppen für jede virtuelle Anwendung, die veröffentlicht werden soll, und fügt dann die entsprechenden Benutzer zu diesen Gruppen hinzu. Wenn sich die Benutzer an ihren Arbeitsstationen anmelden, führt der Application Virtualization-Client standardmäßig eine Veröffentlichungsaktualisierung mithilfe der Anmeldeinformationen des angemeldeten Benutzers durch. Der Benutzer kann dann Anwendungen von überall aus starten, wo die Verknüpfungen gespeichert wurden. Der Application Virtualization-Administrator bestimmt, wo und wie viele Tastenkombinationen sich während der Sequenzierung der Anwendung auf dem Clientsystem befinden.

**Hinweis**  Bei einer *Veröffentlichungsaktualisierung* handelt es sich um einen Anruf an den Application Virtualization Server, der auf dem Application Virtualization-Client definiert ist, um zu ermitteln, welche virtuellen Anwendungsverknüpfungen für die Verwendung durch den Endbenutzer an den Client gesendet werden.

 

## Verwandte Themen


[Application Virtualization Server-basiertes Szenario](application-virtualization-server-based-scenario.md)

[So veröffentlichen Sie eine virtuelle Anwendung auf dem Client](how-to-publish-a-virtual-application-on-the-client.md)

[Übersicht über die Application Virtualization-Systemkomponenten](overview-of-the-application-virtualization-system-components.md)

[Planen Ihrer Streaming-Lösung in einer Anwendung Virtualisierung Server-basierten-Implementierung](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

 

 





