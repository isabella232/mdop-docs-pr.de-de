---
title: Problembehandlung bei Advanced Group Policy Management
description: Problembehandlung bei Advanced Group Policy Management
author: dansimp
ms.assetid: f58849cf-6c5b-44d8-b356-0ed7a5b24cee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c22b9a0983b26252ee0d9c8d99b63cd4ab5dc2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807432"
---
# Problembehandlung bei Advanced Group Policy Management


In diesem Abschnitt werden einige häufige Probleme aufgeführt, die bei der Verwendung der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) zum Verwalten von Gruppenrichtlinienobjekten auftreten können.

## Welche Probleme haben Sie?


-   [Ich kann nicht auf ein Archiv zugreifen](#bkmk-access-an-archive)

-   [Der GPO-Status variiert für verschiedene Gruppenrichtlinienadministratoren](#bkmk-state-varies)

-   [Ich kann die AGPM-Server Verbindung nicht ändern](#bkmk-modify-archive-location)

-   [Ich kann die Standardvorlage oder das anzeigen, erstellen, bearbeiten, umbenennen, bereitstellen oder Löschen von GPOs nicht ändern.](#bkmk-perform-task)

-   [Ich kann einen bestimmten GPO-Namen nicht verwenden](#bkmk-use-particular-name)

-   [Ich erhalte keine AGPM-e-Mail-Benachrichtigungen](#bkmk-email)

-   [Ich kann Port 4600 für den AGPM-Dienst nicht verwenden](#bkmk-port)

-   [Der AGPM-Dienst wird nicht gestartet](#bkmk-not-start)

-   [Software Installation für Gruppenrichtlinien kann nicht installiert werden](#bkmk-software-installation)

### <a href="" id="bkmk-access-an-archive"></a>Ich kann nicht auf ein Archiv zugreifen

-   **Ursache**: Sie haben nicht den richtigen Server und Port für das Archiv ausgewählt.

-   **Lösung**:

    -   Wenn Sie ein AGPM-Administrator sind, lesen Sie [Konfigurieren der AGPM-Server Verbindung](configure-the-agpm-server-connection.md).

    -   Wenn Sie kein AGPM-Administrator sind: fordern Sie die Verbindungsdetails für den AGPM-Server von einem AGPM-Administrator an. Informationen finden Sie unter [Konfigurieren der AGPM-Server Verbindung](configure-the-agpm-server-connection-reviewer.md).

-   **Ursache**: der erweiterte Gruppenrichtlinien-Verwaltungsdienst wird nicht ausgeführt.

-   **Lösung**:

    -   Wenn Sie ein AGPM-Administrator sind: Starten Sie den AGPM-Dienst. Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service.md).

    -   Wenn Sie kein AGPM-Administrator sind: wenden Sie sich an einen AGPM-Administrator, um Hilfe zu erhalten.

### <a href="" id="bkmk-state-varies"></a>Der GPO-Status variiert für verschiedene Gruppenrichtlinienadministratoren

-   **Ursache**: verschiedene Gruppenrichtlinienadministratoren haben verschiedene AGPM-Server für dasselbe Archiv ausgewählt.

-   **Lösung**:

    -   Wenn Sie ein AGPM-Administrator sind, lesen Sie [Konfigurieren der AGPM-Server Verbindung](configure-the-agpm-server-connection.md).

    -   Wenn Sie kein AGPM-Administrator sind: fordern Sie die Verbindungsdetails für den AGPM-Server von einem AGPM-Administrator an. Informationen finden Sie unter [Konfigurieren der AGPM-Server Verbindung](configure-the-agpm-server-connection-reviewer.md).

### <a href="" id="bkmk-modify-archive-location"></a>Ich kann die AGPM-Server Verbindung nicht ändern

-   **Ursache**: Wenn die Einstellungen auf der Registerkarte **AGPM-Server** nicht verfügbar sind, wurde der AGPM-Server mithilfe einer administrativen Vorlage zentral konfiguriert.

-   **Lösung**:

    -   Wenn Sie ein AGPM-Administrator sind: Wenn die Einstellungen auf der Registerkarte **AGPM-Server** nicht verfügbar sind, lesen Sie [Konfigurieren der AGPM-Serververbindung](configure-the-agpm-server-connection.md).

    -   Wenn Sie kein AGPM-Administrator sind: Wenn die Einstellungen auf der Registerkarte **AGPM-Server** nicht verfügbar sind, müssen Sie den AGPM-Server nicht ändern.

### <a href="" id="bkmk-perform-task"></a>Ich kann die Standardvorlage oder das anzeigen, erstellen, bearbeiten, umbenennen, bereitstellen oder Löschen von GPOs nicht ändern.

-   **Ursache**: Ihnen wurde keine Rolle mit den Berechtigungen zugewiesen, die zum Ausführen der Aufgabe oder Aufgaben erforderlich sind.

-   **Lösung**:

    -   Wenn Sie ein AGPM-Administrator sind, lesen Sie Delegieren des Zugriffs auf [Domänenebene](delegate-domain-level-access.md) und [Delegieren des Zugriffs auf ein einzelnes Gruppenrichtlinienobjekt](delegate-access-to-an-individual-gpo.md). AGPM-Berechtigungen werden von der Domäne zu allen GPOs, die sich derzeit im Archiv befinden, kaskadiert. Wenn neue Gruppenrichtlinienadministratoren auf Domänenebene hinzugefügt werden, müssen Ihre Berechtigungen so festgesetzt sein, dass Sie auf **dieses Objekt und verschachtelte Objekte**angewendet werden. Informationen dazu, welche Rollen eine Aufgabe ausführen können und welche Berechtigungen für die Ausführung einer Aufgabe erforderlich sind, finden Sie in der Hilfe zu dieser Aufgabe.

    -   Wenn Sie kein AGPM-Administrator sind und zusätzliche Rollen oder Berechtigungen benötigen: wenden Sie sich an einen AGPM-Administrator, um Hilfe zu erhalten. Beachten Sie, dass Sie, wenn Sie ein Editor sind, den Vorgang des Erstellens eines GPO, der Bereitstellungeines Gruppenrichtlinienobjekts oder des Löschens eines Gruppenrichtlinienobjekts aus der Produktionsumgebung beginnen können, aber eine genehmigende Person oder ein AGPM-Administrator Ihre Anforderung genehmigen muss.

### <a href="" id="bkmk-use-particular-name"></a>Ich kann einen bestimmten GPO-Namen nicht verwenden

-   **Ursache**: entweder der GPO-Name wird bereits verwendet, oder Sie haben keine Berechtigung, das Gruppenrichtlinienobjekt aufzulisten.

-   **Lösung**:

    -   Wenn der Name des Gruppenrichtlinienobjekts auf der Registerkarte **gesteuert**, **unkontrolliert**oder **Ausstehend** angezeigt wird, wählen Sie einen anderen Namen aus. Wenn ein bereitgestelltes GPO umbenannt, aber noch nicht erneut bereitgestellt wurde, wird es unter seinem alten Namen in der Produktionsumgebung angezeigt, daher wird der alte Name noch verwendet. Stellen Sie das Gruppenrichtlinienobjekt erneut bereit, um dessen Namen in der Produktionsumgebung zu aktualisieren und diesen Namen für die Verwendung durch ein anderes GPO freizugeben.

    -   Wenn der GPO-Name nicht auf der Registerkarte **gesteuert**, **unkontrolliert**oder **Ausstehend** angezeigt wird, ist möglicherweise keine Berechtigung zum Auflisten des Gruppenrichtlinienobjekts vorhanden. Wenden Sie sich an einen AGPM-Administrator, um die Berechtigung anzufordern.

### <a href="" id="bkmk-email"></a>Ich erhalte keine AGPM-e-Mail-Benachrichtigungen

-   **Ursache**: Es wurde kein gültiger SMTP-e-Mail-Server und keine e-Mail-Adresse bereitgestellt, oder es wurde keine Aktion durchgeführt, die eine e-Mail-Benachrichtigung generiert.

-   **Lösung**:

    -   Wenn Sie ein AGPM-Administrator sind: Wenn e-Mail-Benachrichtigungen über ausstehende Aktionen von AGPM gesendet werden sollen, muss ein AGPM-Administrator auf der Registerkarte **Domänendelegierung** einen gültigen SMTP-e-Mail-Server und e-Mail-Adressen für genehmigende Personen bereitstellen. Weitere Informationen finden Sie unter [Konfigurieren von e-Mail-Benachrichtigungen](configure-e-mail-notification.md).

    -   E-Mail-Benachrichtigungen werden nur generiert, wenn ein Bearbeiter, Prüfer oder ein anderer Gruppenrichtlinienadministrator, der über die zum Erstellen, bereitstellen oder Löschen eines Gruppenrichtlinienobjekts erforderliche Berechtigung verfügt, eine Anforderung für eine dieser Aktionen übermittelt. Es erfolgt keine automatische Benachrichtigung über die Genehmigung oder Ablehnung einer Anfrage.

### <a href="" id="bkmk-port"></a>Ich kann Port 4600 für den AGPM-Dienst nicht verwenden

-   **Ursache**: Standardmäßig ist der Port, auf dem der AGPM-Dienst lauscht, Port 4600.

-   **Lösung**: Wenn Port 4600 für den AGPM-Dienst nicht verfügbar ist, ändern Sie die einzelnen Archiv Indexdateien so, dass Sie einen anderen Port verwenden, und aktualisieren Sie dann den AGPM-Server für alle Gruppenrichtlinienadministratoren. Weitere Informationen finden Sie unter [Ändern des Ports, auf den der AGPM-Dienst lauscht](modify-the-port-on-which-the-agpm-service-listens.md).

### <a href="" id="bkmk-not-start"></a>Der AGPM-Dienst wird nicht gestartet

-   **Ursache**: Sie haben die Einstellungen für den AGPM-Dienst im Betriebssystemunter **Administrative Tools** und **Dienste**geändert.

-   **Lösung**: Ändern Sie die Einstellungen für **Microsoft Advanced Group Policy Management-Server** unter **Software**. Weitere Informationen finden Sie unter [Ändern des AGPM-Dienstkontos](modify-the-agpm-service-account.md).

### <a href="" id="bkmk-software-installation"></a>Software Installation für Gruppenrichtlinien kann nicht installiert werden

-   **Ursache**: AGPM erhält die Integrität von Gruppenrichtlinien-Software Installationspaketen. Obwohl GPOs offline bearbeitet werden, bleiben Verknüpfungen zwischen Paketen und zwischengespeicherten Clientinformationen erhalten. Dies ist entwurfsbedingt.

-   **Lösung**: Wenn Sie ein Gruppenrichtlinienobjekt offline mit AGPM bearbeiten, konfigurieren Sie ein Upgrade für die Gruppenrichtlinien-Software Installation eines Pakets in einem anderen Gruppenrichtlinienobjekt, um auf das bereitgestellte GPO zu verweisen, nicht auf die ausgecheckte Kopie. Der Editor muss über die Berechtigung " **Lesen** " für das bereitgestellte Gruppenrichtlinienobjekt verfügen.

 

 





