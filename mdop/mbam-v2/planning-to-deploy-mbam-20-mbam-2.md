---
title: Planen der Bereitstellung von MBAM 2.0
description: Planen der Bereitstellung von MBAM 2.0
author: dansimp
ms.assetid: 2dc05fcd-aed9-4315-aeaf-92aaa9e0e955
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c7f065e52655212261dfe8b6b3f081f697142473
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811272"
---
# Planen der Bereitstellung von MBAM 2.0


Sie sollten eine Reihe unterschiedlicher Bereitstellungskonfigurationen und Voraussetzungen berücksichtigen, bevor Sie Ihren Bereitstellungsplan für Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) erstellen. Dieser Abschnitt enthält Informationen, die Ihnen beim Sammeln der erforderlichen Informationen helfen können, um einen Bereitstellungsplan zu formulieren, der Ihren geschäftlichen Anforderungen am besten entspricht. Wenn Sie MBAM mit der Configuration Manager-Topologie installieren, lesen Sie [Planen der Bereitstellung von MBAM mit Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) für zusätzliche Planungsinformationen.

## Überprüfen der von MBAM 2,0 unterstützten Konfigurationen


Stellen Sie nach dem Vorbereiten Ihrer Computerumgebung für die MBAM-Server-und-Client Feature-Installation sicher, dass Sie die unterstützten Konfigurationen überprüfen, um zu bestätigen, dass die Computer, auf denen Sie die Installation durchführen, die Mindestanforderungen für Hardware und Betriebssystem MBAM erfüllen. Weitere Informationen zu den Voraussetzungen für die MBAM-Bereitstellung finden Sie unter [MBAM 2,0-Bereitstellungsvoraussetzungen](mbam-20-deployment-prerequisites-mbam-2.md).

[Von MBAM 2.0 unterstützte Konfigurationen](mbam-20-supported-configurations-mbam-2.md)

## Planen der MBAM 2,0-Server-und-Client Bereitstellung


Die MBAM-Serverinfrastruktur hängt von einer Reihe von Server Features ab, die basierend auf den Anforderungen des Unternehmens auf einem oder mehreren Server Computern installiert werden können. Diese Features können in einer verteilten Konfiguration auf mehreren Servern installiert werden.

**Hinweis**  Eine MBAM-Installation auf einem einzelnen Server wird nur für Lab-Umgebungen empfohlen.

 

Der MBAM-Client ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen. Der BitLocker-Client kann in eine Organisation integriert werden, indem der Client über ein Enterprise-Software Bereitstellungssystem bereitgestellt oder der Client-Agent auf Clientcomputern als Teil des anfänglichen Imaging-Prozesses installiert wird.

Mit MBAM können Sie einen Computer in Ihrer Organisation verschlüsseln, entweder bevor der Endbenutzer den Computer empfängt, oder anschließend mithilfe von Gruppenrichtlinien.

[Planen der Serverbereitstellung für MBAM 2.0](planning-for-mbam-20-server-deployment-mbam-2.md)

[Planen der Clientbereitstellung für MBAM 2.0](planning-for-mbam-20-client-deployment-mbam-2.md)

## <a href="" id="other-resources-for-mbam-planning-"></a>Weitere Ressourcen für die Planung von MBAM


[Planen von MBAM 2.0](planning-for-mbam-20-mbam-2.md)

 

 





