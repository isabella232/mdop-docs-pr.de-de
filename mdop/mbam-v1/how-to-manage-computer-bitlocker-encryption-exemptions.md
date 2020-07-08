---
title: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Computer
description: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Computer
author: dansimp
ms.assetid: d4400a0d-b36b-4cf5-a294-1f53ec47f9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51b93061468508900eaee7fce8a7827e2db61d19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811299"
---
# So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Computer


Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) kann verwendet werden, um bestimmte Computer vom BitLocker-Schutz zu befreien. Beispielsweise kann eine Organisation beschließen, die BitLocker-Ausnahmeregelung auf Computer-für-Computer-Basis zu steuern.

Wenn Sie einen Computer von der BitLocker-Verschlüsselung ausschließen möchten, müssen Sie den Computer zu einer Sicherheitsgruppe in ActiveDirectoryDomainServices hinzufügen, um alle computerbasierten BitLocker-Schutzregeln zu umgehen.

**Hinweis**  Wenn der Computer bereits mit BitLocker geschützt ist, hat die Richtlinie für den Computer Ausschluss keine Auswirkungen.

 

**So nehmen Sie einen Computer von der BitLocker-Verschlüsselung frei**

1.  Fügen Sie in ActiveDirectoryDomainServices das Computerkonto hinzu, das für eine Sicherheitsgruppe freigestellt werden soll. Auf diese Weise können Sie alle computerbasierten BitLocker-Schutzregeln umgehen.

2.  Erstellen Sie ein Gruppenrichtlinienobjekt mithilfe der MBAM-Gruppenrichtlinienvorlage, und ordnen Sie dann das Gruppenrichtlinienobjekt der Active Directory-Gruppe zu, die Sie im vorherigen Schritt erstellt haben. Weitere Informationen zum Erstellen der erforderlichen Gruppenrichtlinienobjekte finden Sie unter [Bereitstellen von MBAM 1,0-Gruppenrichtlinienobjekten](deploying-mbam-10-group-policy-objects.md).

3.  Wenn ein ausgenommener Computer gestartet wird, überprüft der MBAM-Client die Einstellungen für die Computer Freistellungs Richtlinie und unterbricht den Schutz, je nachdem, ob der Computer Bestandteil der BitLocker-Ausnahme Sicherheitsgruppe ist.

## Verwandte Themen


[Verwalten von MBAM 1.0-Funktionen](administering-mbam-10-features.md)

 

 





