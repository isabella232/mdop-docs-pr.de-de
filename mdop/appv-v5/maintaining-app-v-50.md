---
title: Warten von App-V 5.0
description: Warten von App-V 5.0
author: dansimp
ms.assetid: 66851ec3-c674-493b-ad6d-db8fcbf1956c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3445bfe00ba7703a66fa3da2f9d7089990dd3854
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805111"
---
# Warten von App-V 5.0


Nachdem Sie die erforderliche Planung abgeschlossen und dann App-v 5,0 bereitgestellt haben, können Sie die folgenden Informationen zum Verwalten der APP-v 5,0-Infrastruktur verwenden.

## <a href="" id="move-the-app-v-5-0-server-"></a>Verschieben des App-V 5,0-Servers


Der APP-v 5,0-Server stellt eine Verbindung mit der APP-v 5,0-Datenbank her. Daher können Sie die Verwaltungskomponente auf einem beliebigen Computer im Netzwerk installieren und dann mit der App-V 5,0-Datenbank verbinden.

[So verschieben Sie den App-V-Server auf einen anderen Computer](how-to-move-the-app-v-server-to-another-computer.md)

## <a href="" id="determine-if-an-app-v-5-0-application-is-running-virtualized-"></a>Ermitteln, ob eine App-V 5,0-Anwendung virtualisiert ausgeführt wird


Unabhängige Softwareanbieter (Independent Software Vendors, ISV), die ermitteln möchten, ob eine Anwendung mit App-V 5,0 oder höher virtualisiert ausgeführt wird, sollten im Standardnamespace ein benanntes Objekt namens **AppVVirtual- &lt; PID &gt; ** öffnen. So kann beispielsweise die Windows-API **GetCurrentProcessId ()** verwendet werden, um die ID des aktuellen Prozesses zu erhalten, beispielsweise 4052, und dann, wenn ein benanntes Ereignisobjekt namens **AppVVirtual-4052** erfolgreich mit **OpenEvent ()** im Standardnamespace für Lesezugriff geöffnet werden kann, ist die Anwendung virtuell. Wenn der **OpenEvent ()** -Aufruf fehlschlägt, ist die Anwendung nicht virtuell.

Darüber hinaus können ISV-Benutzer, die Aufrufe mit App-V 5,0 und höher für bestimmte APIs explizit virtualisieren oder nicht virtualisieren möchten, die **VirtualizeCurrentThread ()** -und **CurrentThreadIsVirtualized ()** -Funktionen verwenden, die im AppEntSubsystems32.dll-Modul implementiert sind. Diese stellen eine Möglichkeit dar, auf eine Downstream-Komponente zu deuten, dass der Anruf virtualisiert werden soll oder nicht.






## Weitere Ressourcen für die Verwaltung von App-V 5,0


[Vorgänge für App-V 5.0](operations-for-app-v-50.md)

 

 





