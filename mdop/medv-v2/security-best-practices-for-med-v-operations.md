---
title: Bewährte Sicherheitsmethoden für MED-V-Vorgänge
description: Bewährte Sicherheitsmethoden für MED-V-Vorgänge
author: dansimp
ms.assetid: 231e2b9a-8b49-42fe-93b5-2ef12fe17bac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4353a15c756dba8cf44f530c2077546e3f9288cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811131"
---
# Bewährte Sicherheitsmethoden für MED-V-Vorgänge


Als autorisierter Administrator sind Sie dafür verantwortlich, die Informationen der Benutzer zu schützen und die Sicherheit Ihrer Organisation während und nach der Bereitstellung von MED-V-Arbeitsbereichen zu gewährleisten. Bedenken Sie insbesondere die folgenden Probleme.

**Anpassen von Internet Explorer im MED-V-Arbeitsbereich** Frühere Versionen des Windows-Betriebssystems und von Internet Explorer sind nicht so sicher wie aktuelle Versionen. Daher ist Internet Explorer im MED-V-Arbeitsbereich so konfiguriert, dass das Browsen und andere Aktivitäten, die Sicherheitsrisiken darstellen können, verhindert werden. Darüber hinaus ist die Einstellung für Internet-Sicherheitszone für Internet Explorer im MED-V-Arbeitsbereich auf die höchste Ebene festgelegt. Standardmäßig werden beide Konfigurationen beim Erstellen Ihres Med-v-Arbeitsbereichs Pakets im Med-v-Arbeitsbereich-Paketer eingestellt.

Durch die Verwendung von Internet Explorer Administration Kit (IEAK) oder durch Ändern der Standardeinstellungen im Med-v Workspace-Paketer können Sie Internet Explorer im Med-v-Arbeitsbereich anpassen. Beachten Sie jedoch, dass Sie, wenn Sie Internet Explorer im MED-V-Arbeitsbereich so anpassen, dass Sie nicht so sicher sind, dass Sie Ihre Organisation für die Sicherheitsrisiken verfügbar machen können, die in älteren Versionen von Internet Explorer vorhanden sind.

Aus Sicherheitsgesichtspunkten sind bewährte Methoden für die Verwaltung von Internet Explorer im MED-V-Arbeitsbereich wie folgt:

-   Lassen Sie beim Erstellen Ihres Med-v-Arbeitsbereichs Pakets die Standardeinstellungen so festlegen, dass Internet Explorer im Med-v-Arbeitsbereich so konfiguriert ist, dass das Browsen und andere Aktivitäten, die Sicherheitsrisiken darstellen können, verhindert werden.

-   Wenn Sie Ihr MED-V-Arbeitsbereichs Paket erstellen, beließen Sie die Standardeinstellungen so, dass die Sicherheitseinstellung für das Internet sicherheitsgebiet auf der höchsten Ebene verbleibt.

-   Konfigurieren Sie Ihren Unternehmens Proxy oder Internet Explorer-Inhaltsratgeber so, dass Domänen außerhalb des Intranets Ihres Unternehmens blockiert werden.

**Konfigurieren eines MED-V-Arbeitsbereichs für alle Benutzer auf einem freigegebenen Computer** Wenn Sie einen MED-V-Arbeitsbereich so konfigurieren, dass alle Benutzer auf einem freigegebenen Computer darauf zugreifen können, stellen Sie fest, dass die virtuelle Gastmaschine (Virtual Machine, VHD) an einem Speicherort abgelegt wird, der allen Benutzern in diesem System Lese-und Schreibzugriff gewährt.

**Konfigurieren eines Proxykontos für die Domänenmitgliedschaft** Wenn Sie ein Proxykonto für die Teilnahme an virtuellen Computern zur Domäne konfigurieren, müssen Sie wissen, dass es möglich ist, dass ein Endbenutzer die Anmeldeinformationen für das Proxykonto erhält. Daher müssen erforderliche Vorkehrungen getroffen werden, beispielsweise das Einschränken von Konto Benutzerrechten, um zu verhindern, dass ein Endbenutzer die Anmeldeinformationen verwendet, um Schäden zu verursachen.

**Sysprep-Konfiguration.** Obwohl die Datei "Sysprep. inf" standardmäßig verschlüsselt ist, kann Ihr Inhalt von einem bestimmten Endbenutzer entschlüsselt und gelesen werden, der sich erfolgreich beim virtuellen Computer anmelden kann. Dies wirft Sicherheitsbedenken auf, da die Datei "Sysprep. inf" zusätzlich zu einem Windows-Product Key Anmeldeinformationen enthalten kann.

Sie können dieses Risiko verringern, indem Sie ein Konto mit Einschränkungen für die Teilnahme an virtuellen Computern an der Domäne einrichten und die Anmeldeinformationen für dieses Konto bei der Konfiguration von Sysprep angeben. Alternativ können Sie auch Sysprep und das erstmalige Einrichten so konfigurieren, dass Sie im **beaufsichtigten** Modus ausgeführt werden, und die Endbenutzer müssen Ihre Anmeldeinformationen für die Teilnahme am virtuellen Computer zur Domäne angeben.

In einem MED-V-bewährten Verfahren wird angegeben, dass FtsCompletion.exe unter einem Konto ausgeführt wird, das den Endbenutzern die Berechtigung zum Herstellen einer Verbindung mit dem Gast über den Remote Desktop Verbindung-Client (RDC) gewährt.

**Endbenutzer Authentifizierung.** Das Aktivieren der Zwischenspeicherung von Anmeldeinformationen für Endbenutzer bietet die beste Benutzerfreundlichkeit von MED-V, schafft aber das Potenzial, dass jemand Zugriff auf die Anmeldeinformationen des Endbenutzers erhält. Die einzige Möglichkeit, dieses Risiko zu verringern, besteht darin, dass für den **MED-V-Arbeitsbereichs-Packager** angegeben wird, dass keine Endbenutzeranmeldeinformationen gespeichert werden. Weitere Informationen zur Authentifizierung von Endbenutzern finden Sie unter [Authentifizierung von MED-V-Endbenutzern](authentication-of-med-v-end-users.md).

## Verwandte Themen


[Problembehandlung bei Vorgängen](operations-troubleshooting-medv2.md)

[Microsoft Enterprise Desktop Virtualization 2,0](index.md)

 

 





