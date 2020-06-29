---
title: In die Domäne eingebundene und keiner Domäne beigetretene Clients
description: In die Domäne eingebundene und keiner Domäne beigetretene Clients
author: dansimp
ms.assetid: a935dc98-de60-45f3-ab74-2444ce082e88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4385ab3f26bb867dd649fe768e1500c9d015ffa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808872"
---
# In die Domäne eingebundene und keiner Domäne beigetretene Clients


Der App-V-Desktop Client kann so konfiguriert werden, dass die Verbindung zu einem Netzwerk ermöglicht wird, unabhängig davon, ob der Client einer Domäne beigetreten ist oder nicht der Domäne beigetreten ist.

## Mit der Domäne verbundene Clients


Clients, die Domänen verbunden sind, aber außerhalb des internen Netzwerks, können über eine VPN-Verbindung mit der App-V-Infrastruktur kommunizieren. Wenn Sie Benutzern die Möglichkeit geben möchten, das interne Netzwerk zu belassen, aber dennoch in einer App-V-Infrastruktur zu kommunizieren, erfordert Ihre Umgebung nur sehr wenig Setup. Da die Benutzer bereits Teil der Domäne sind, müssen Sie einfach sicherstellen, dass zwischengespeicherte Anmeldeinformationen auf dem Client unterstützt werden. Dies ist die Standardkonfiguration, und alle Änderungen an dieser Einstellung können über Gruppenrichtlinien erfolgen.

Wie im Leitfaden zur APP-v-Sicherheit für bewährte Methoden beschrieben, wird der Benutzer versuchen, sein Benutzerticket zur Authentifizierung an die APP-v-Infrastruktur zu senden. Wenn das Ticket abgelaufen ist, wird es auf die Verwendung von NTLM und die zwischengespeicherten Anmeldeinformationen auf dem Computer zurückgesetzt. Um Roaming zu ermöglichen, müssen Administratoren sicherstellen, dass der Veröffentlichungsserver, auf den intern zugegriffen wird, mit dem gleichen Namen extern verfügbar ist, damit die Namen ordnungsgemäß aufgelöst werden können.

## Nicht mit der Domäne verbundene Clients


Clients, die nicht der Domäne beigetreten sind, aber in der APP-v-Infrastruktur kommunizieren müssen, müssen so konfiguriert werden, dass sichergestellt ist, dass die Authentifizierung für die APP-v-Infrastruktur erfolgreich ist. Der APP-v-Desktop Client lässt keine Eingabeaufforderung für den Veröffentlichungs Aktualisierungsvorgang zu, sodass der Client so konfiguriert sein muss, dass er die richtigen Anmeldeinformationen für den App-V-Verwaltungs Server bereitstellt.

Der Veröffentlichungsserver, der für die Veröffentlichungsaktualisierung vom nicht für die Domäne verbundenen Client konfiguriert ist, erfordert, dass der externe Name, auf den Clients zugreifen, als allgemeiner Name oder als alternativer Subjektname (Subject Alternate Name, San) auf dem Zertifikat des Veröffentlichungsservers konfiguriert ist.

## Verwandte Themen


[So weisen Sie die richtigen Anmeldeinformationen für Windows Vista zu](how-to-assign--the-proper-credentials-for-windows-vista.md)

[So weisen Sie die richtigen Anmeldeinformationen für Windows XP zu](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





