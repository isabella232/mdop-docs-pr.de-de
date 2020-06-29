---
title: So fügen Sie ein Paket hinzu
description: So fügen Sie ein Paket hinzu
author: dansimp
ms.assetid: 5407fdbe-e658-44f6-a9b8-a566b81dedce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c580d7d131017c52e278adda0208ffcb2e86ccf2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808731"
---
# So fügen Sie ein Paket hinzu


Sie können ein Paket aus der Application Virtualization Server-Verwaltungskonsole wie folgt hinzufügen:

-   Importieren Sie eine Anwendung, die das Paket automatisch im Prozess erstellt.

-   Manuelles Hinzufügen eines Pakets

Es wird empfohlen, dass Sie Anwendungen importieren, anstatt Sie manuell hinzuzufügen. Weitere Informationen zum Importieren von Anwendungen finden Sie unter [so wird es gemacht: Importieren einer Anwendung](how-to-import-an-applicationserver.md).

**So fügen Sie ein Paket manuell hinzu**

1.  Klicken Sie in der Application Virtualization Server-Verwaltungskonsole im linken Bereich mit der rechten Maustaste auf den Knoten **Pakete** , und wählen Sie **neues Paket**aus.

2.  Geben Sie im Dialogfeld **neues Paket** einen Namen in das Feld **Paketname** ein.

3.  Suchen oder geben Sie im Feld **Vollständiger Pfad für Paketdatei** einen Pfadnamen ein. Hierbei muss es sich um eine SFT-Datei handeln.

    **Hinweis**  Wenn Sie die SFT-Datei durchsuchen, ersetzen Sie den lokalen Pfad (wie c:\\Programme Files\\User\ _Apps \\virtual\ _App \ _Server \\content) durch den statischen Hostnamen oder die IP-Adresse des Servers. Bei Verwendung der Variablen *% SFT \ _SOFTGRIDSERVER%* ist die Konfiguration pro Clientcomputer erforderlich.

    In Dialogfeldern, die auf virtuelle Anwendungsserver verweisen, müssen Sie einen Netzwerkspeicherort verwenden, beispielsweise den statischen Hostnamen oder die IP-Adresse des Servers, auf den Ihre Benutzer zugreifen können. Die OSD-Datei (Open Software Descriptor) der Anwendung kann die Platzhaltervariable *% SFT \ _SOFTGRIDSERER%* durch den statischen Hostnamen oder die IP-Adresse des Servers ersetzen. Wenn Sie die Platzhaltervariable beibehalten, müssen Sie diese Variable auf jedem Clientcomputer, der auf diesen Server zugreifen soll, festzulegen. Setzen Sie einen Benutzer oder eine System Variable auf jedem Computer für SFT \ _SOFTGRIDSERVER. Der Variablenwert muss der statische Hostname oder die IP-Adresse des Servers sein. Wenn Sie eine Variable festzulegen, beenden Sie die Client Sitzung, melden Sie sich bei Microsoft Windows ab und wieder an, und starten Sie die Sitzung auf jedem Computer neu, auf dem eine Sitzung ausgeführt wurde und für die die Variable festgesetzt wurde.

     

4.  Klicken Sie auf **Weiter**.

5.  Im Dialogfeld " **Zusammenfassung** " wird der Speicherort der Datei angezeigt, und Sie werden aufgefordert, die Datei an den Speicherort zu kopieren, wenn dies noch nicht geschehen ist. Klicken Sie auf **Fertig stellen** , nachdem Sie die Informationen überprüft haben.

    **Hinweis**  Wenn Sie Anwendungen auf einem Remoteserver verwalten, geben Sie im nächsten Dialogfeld nur den Pfad der Datei relativ zum Inhaltsstamm des Servers ein.

     

## Verwandte Themen


[So importieren Sie eine Anwendung](how-to-import-an-applicationserver.md)

[So verwalten Sie die Pakete in der Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 





