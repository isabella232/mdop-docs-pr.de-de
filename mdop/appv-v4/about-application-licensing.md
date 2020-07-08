---
title: Informationen zur Anwendungslizenzierung
description: Informationen zur Anwendungslizenzierung
author: dansimp
ms.assetid: 6b487641-1627-4e91-b829-04f001008176
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546bc630b95fe52f960c7bdfb771d3e2561f9318
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808171"
---
# Informationen zur Anwendungslizenzierung


Sie können Anwendungslizenzen direkt in der Application Virtualization Server-Verwaltungskonsole verwalten.

## Lizenztypen


Das System Center Application Virtualization-System unterstützt derzeit die folgenden Lizenztypen:

-   **Unbegrenzte Lizenz**– ermöglicht den Zugriff auf die Anwendung durch eine beliebige Anzahl von gleichzeitigen Benutzern. Diese Lizenzierungsmethode ist geeignet, wenn Sie einer Anwendung eine unternehmensweite Lizenz zuweisen möchten.

-   **Concurrent License**– ermöglicht Ihnen, die maximale Anzahl von gleichzeitigen Benutzern zu definieren, die die Anwendung verwenden dürfen.

-   **Benannte Lizenz**– ermöglicht Ihnen, einem einzelnen Benutzer eine Lizenz zuzuweisen. Eine benannte Lizenz kann verwendet werden, um sicherzustellen, dass ein bestimmter Benutzer immer in der Lage ist, die Anwendung auszuführen.

Sie können gleichzeitige und benannte Lizenzen für dieselbe Anwendung kombinieren.

Die Lizenzierung ist standardmäßig deaktiviert, kann aber über die Registerkarte **Anbieter Pipeline** im Dialogfeld **Anbietereigenschaften** aktiviert werden. Details zum Aktivieren und Deaktivieren der Lizenzierung finden Sie unter [so wird es gemacht: Einrichten oder Deaktivieren der Anwendungslizenzierung](how-to-set-up-or-disable-application-licensing.md).

## Anbieterrichtlinien


Für das ASP-Modell (Application Service Provider) wurden Anbieterrichtlinien entwickelt. In diesem Modell kann eine einzelne ASP-Anwendung ein einzelnes Application Virtualization-System für mehrere Clients hosten, wobei jeder Client isoliert bleiben muss. Clients haben möglicherweise unterschiedliche Anforderungen – beispielsweise kann ein Client eine Authentifizierung erfordern, während eine andere nicht. Sie können Anbieterrichtlinien verwenden, um Berechtigungen für Clients zuzuordnen, damit nur die genehmigten Benutzer auf die einzelnen virtuellen Anwendungen oder virtuellen Anwendungspakete zugreifen können.

Für den Unternehmenskunden können Sie dieses Feature verwenden, wenn Sie über strenge Lizenzierungsanforderungen für eine oder mehrere Anwendungen verfügen. In diesem Fall ist die Lizenzierungskomponente auf der Registerkarte **Anbieter Pipeline** im Dialogfeld **Anbietereigenschaften** deaktiviert.

Die Registerkarte **Anbieter Pipeline** enthält ebenfalls Kontrollkästchen zum Aktivieren der Authentifizierung, Autorisierung (**Zugriffsberechtigungseinstellungen erzwingen**) und Dosierung (**Protokoll Nutzungsinformationen**). Wenn Ihre Konfiguration besondere Anforderungen hat, können Sie Ihre eigenen Pipelinekomponenten schreiben und dem System hinzufügen, indem Sie auf die Schaltfläche **erweitert** klicken.

## Konto Verwaltungen


Die Konto Berechtigung ist die Domäne, in der der Application Virtualization Server installiert ist. Wenn Sie die Server Installation durchlaufen, werden Sie aufgefordert, einen Domänennamen anzugeben. die Domäne, in der der Computer installiert ist, wird standardmäßig erkannt und verwendet. Wenn Benutzer versuchen, sich beim System anzumelden, werden Sie aufgefordert, Ihre Anmeldeinformationen einzugeben, bevor Sie auf diese Domäne zugreifen können.

Das Application Virtualization System unterstützt mehrere Domänen. Sie können Anwendungszugriff auf Benutzergruppen in anderen Domänen gewähren, wenn zwischen Domänen eine Vertrauensstellung hergestellt wird. Benutzer müssen Anmeldeinformationen angeben, die von jeder Domäne erkannt werden.

In der Application Virtualization Server-Verwaltungskonsole können Sie die primäre Domäne (Kontoautorität) und die Anmeldeinformationen ändern, die für den Zugriff verwendet werden.

## Authentifizierung


Authentifizierung ist der Mechanismus, der zum Bestätigen der Identität eines Benutzers verwendet wird. Jeder Benutzer mit einem anerkannten Benutzernamen und Kennwort hat Zugriff.

Im Application Virtualization System können Sie die Authentifizierung über ein Kontrollkästchen auf der Registerkarte **Anbieter Pipeline** aktivieren oder deaktivieren. Standardmäßig ist die Windows-Authentifizierung aktiviert.

## Autorisierung


Autorisierung ist der Prozess, der zum Bestätigen der Identität eines Benutzers verwendet wird. Nach der Bestätigung der Identität des Benutzers ermittelt das System, ob dem Benutzer Zugriff auf das System gewährt wurde und welchen Anwendungen der Benutzer Zugriff gewährt wurde. Die Application Virtualization Server-Verwaltungskonsole verfügt über das Kontrollkästchen **Zugriffsberechtigungseinstellungen erzwingen** auf der Registerkarte **Anbieter Pipeline** , um die Autorisierung zu aktivieren oder zu deaktivieren.

Im Application Virtualization System wird der Zugriff nur einer Benutzergruppe und nicht einzelnen Benutzern gewährt.

## Verwandte Themen


[So verwalten Sie Anwendungslizenzen in der Server Management Console](how-to-manage-application-licenses-in-the-server-management-console.md)

[So richten Sie die Anwendungslizenzierung ein oder deaktivieren Sie sie](how-to-set-up-or-disable-application-licensing.md)

[Server Management Console: Knoten „Anbieterrichtlinien“](server-management-console-provider-policies-node.md)

 

 





