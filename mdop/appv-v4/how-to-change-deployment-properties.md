---
title: So ändern Sie die Bereitstellungseigenschaften
description: So ändern Sie die Bereitstellungseigenschaften
author: dansimp
ms.assetid: 0a214a7a-cc83-4d04-89f9-5727153be918
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfb42962d41159479db61da9c3beb3771ef35502
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807356"
---
# So ändern Sie die Bereitstellungseigenschaften


Mit den folgenden Verfahren können Sie die Informationen zur **Bereitstellungs** Registerkarte für eine von Ihnen sequenzierte Anwendung ändern, einschließlich der Application Virtualization Server-URL, der für die virtualisierten Anwendungen erforderlichen Betriebssysteme und der Ausgabeoptionen für die zu installierende virtuelle Anwendung.

**So ändern Sie die Server-URL**

1.  Wählen Sie das Streaming-Protokoll aus dem Dropdown-Listenfeld aus.

2.  Geben Sie den Hostnamen des Virtual Application Servers oder des Load Balancer der Servergruppe ein. Sie können den tatsächlichen Hostnamen oder die IP-Adresse verwenden.

3.  Geben Sie die Portnummer an, auf der der Virtual Application Server oder Load Balancer auf eine Application Virtualization Desktop Client-Anforderung für die gestreamte Anwendung wartet.

4.  Geben Sie den relativen Pfad auf dem virtuellen Anwendungsserver an, auf dem das Softwarepaket gespeichert ist.

**So ändern Sie die Anforderungen der Anwendungs Betriebssysteme**

1.  Wenn Sie das erforderliche Betriebssystem (en) hinzufügen möchten, wählen Sie es in der Liste **Verfügbare** aus, und klicken Sie auf die Pfeilschaltfläche, die auf das **ausgewählte** Betriebssystem Listen-Steuerelement zeigt.

2.  Wenn Sie ein Betriebssystem entfernen möchten, wählen Sie es im **ausgewählten** Listensteuerelement aus, und klicken Sie auf die Pfeilschaltfläche, die auf das Listensteuerelement **Verfügbare** Betriebssysteme zeigt.

**So ändern Sie die Optionen für die Anwendungsausgabe**

1.  Wählen Sie in der Dropdownliste **Komprimierungsalgorithmus** die Komprimierungsmethode aus, die beim Streaming der Anwendung verwendet werden soll.

2.  Aktivieren Sie das Kontrollkästchen **Sicherheitsdeskriptoren erzwingen** , um sicherzustellen, dass Sicherheitsbeschreibungen der verpackten Anwendungen bei der Bereitstellung erzwungen werden.

3.  Wählen Sie **Differenzdatei generieren** aus, um eine Differenzdatei für die Anwendung aus der vorherigen sequenzierten Version zu generieren.

4.  Wählen Sie **Microsoft Windows Installer-Paket (MSI) generieren** aus, um ein Installationsprogrammpaket zu erstellen.

## Verwandte Themen


[Informationen zur Registerkarte „Bereitstellung“](about-the-deployment-tab.md)

[Sequencer Console](sequencer-console.md)

 

 





