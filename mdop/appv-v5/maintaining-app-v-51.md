---
title: Warten von App-V 5.1
description: Warten von App-V 5.1
author: dansimp
ms.assetid: 5abd17d3-e8af-4261-b914-741ae116b0e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 431ad65507a5699358159c73eaf9f3cf0dee33b7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805108"
---
# Warten von App-V 5.1


Nachdem Sie die erforderliche Planung abgeschlossen und dann App-v 5,1 bereitgestellt haben, können Sie die folgenden Informationen zum Verwalten der APP-v 5,1-Infrastruktur verwenden.

## <a href="" id="move-the-app-v-5-1-server-"></a>Verschieben des App-V 5,1-Servers


Der APP-v 5,1-Server stellt eine Verbindung mit der APP-v 5,1-Datenbank her. Daher können Sie die Verwaltungskomponente auf einem beliebigen Computer im Netzwerk installieren und dann mit der App-V 5,1-Datenbank verbinden.

[So verschieben Sie den App-V-Server auf einen anderen Computer](how-to-move-the-app-v-server-to-another-computer51.md)

## <a href="" id="determine-if-an-app-v-5-1-application-is-running-virtualized-"></a>Ermitteln, ob eine App-V 5,1-Anwendung virtualisiert ausgeführt wird


Unabhängige Softwareanbieter (Independent Software Vendors, ISV), die ermitteln möchten, ob eine Anwendung mit App-V 5,1 oder höher virtualisiert ausgeführt wird, sollten im Standardnamespace ein benanntes Objekt namens **AppVVirtual- &lt; PID &gt; ** öffnen. So kann beispielsweise die Windows-API **GetCurrentProcessId ()** verwendet werden, um die ID des aktuellen Prozesses zu erhalten, beispielsweise 4052, und dann, wenn ein benanntes Ereignisobjekt namens **AppVVirtual-4052** erfolgreich mit **OpenEvent ()** im Standardnamespace für Lesezugriff geöffnet werden kann, ist die Anwendung virtuell. Wenn der **OpenEvent ()** -Aufruf fehlschlägt, ist die Anwendung nicht virtuell.

Darüber hinaus können ISV-Benutzer, die Aufrufe mit App-V 5,1 und höher für bestimmte APIs explizit virtualisieren oder nicht virtualisieren möchten, die **VirtualizeCurrentThread ()** -und **CurrentThreadIsVirtualized ()** -Funktionen verwenden, die im AppEntSubsystems32.dll-Modul implementiert sind. Diese stellen eine Möglichkeit dar, auf eine Downstream-Komponente zu deuten, dass der Anruf virtualisiert werden soll oder nicht.






## Weitere Ressourcen für die Verwaltung von App-V 5,1


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)

 

 





