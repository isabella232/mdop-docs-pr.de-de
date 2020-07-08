---
title: Registerkarte ' Allgemeine Eigenschaften von Application Virtualization '
description: Registerkarte ' Allgemeine Eigenschaften von Application Virtualization '
author: dansimp
ms.assetid: be7449d9-171a-4a11-9382-83b7008ccbdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ee00bfc7f70ee7b17da42aad61356540a7a0be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808007"
---
# Application Virtualization-Eigenschaften: Registerkarte "Allgemein"


Verwenden Sie die Registerkarte **Allgemein** im Dialogfeld **Eigenschaften von Application Virtualization** , um Protokolleinstellungen und Datenspeicherorte zu ändern.

Diese Registerkarte enthält die folgenden Elemente.

<a href="" id="log-level"></a>**Protokollebene**  
Wählen Sie die Ebene in der Dropdownliste aus. Die Standardebene ist " **Informationen**".

<a href="" id="reset-log"></a>**Protokoll zurücksetzen**  
Klicken Sie auf diese Schaltfläche, um die aktuelle Protokolldatei zu sichern und sofort eine neue Protokolldatei zu starten.

<a href="" id="location"></a>**Pfad**  
Geben Sie den Speicherort ein, an dem die Protokolldatei sftlog.txt gespeichert werden soll, oder navigieren Sie zu ihm. Die Standardspeicherorte lauten wie folgt:

-   Für WindowsXP, Windows Server2003 –*c:\\Dokumente und Einstellungen\\All Users\\Application Data\\Microsoft\\Application-Virtualisierungs-Client*

-   Für Windows Vista, Windows 7, Windows Server2008 –*C:\\ProgramData\\Microsoft\\Application Virtualization Client*

<a href="" id="system-log-level"></a>**System Protokollebene**  
Wählen Sie die Ebene in der Dropdownliste aus. Die Standardstufe ist **Warning**.

**Hinweis**  Die Einstellung **Systemprotokollebene** steuert die Ebene der Nachrichten, die an das Systemereignisprotokoll gesendet werden. Die protokollierten Nachrichten sind identisch mit den Nachrichten, die im Clientereignisprotokoll protokolliert werden, aber Sie werden an einem anderen Speicherort gespeichert, der nicht die Speicherplatzeinschränkungen des Clientereignisprotokolls aufweist. Da das Systemereignisprotokoll keine Speicherplatzeinschränkungen aufweist, eignet es sich hervorragend für Situationen, in denen eine ausführliche Protokollierung erforderlich ist.

 

<a href="" id="global-data-directory"></a>**Globales Datenverzeichnis**  
Geben Sie den Speicherort des Verzeichnisses der Protokolldatei ein, oder suchen Sie nach ihm. Die Standardspeicherorte lauten wie folgt:

-   Für WindowsXP, Windows Server2003 –*c:\\Dokumente und Einstellungen\\All Users\\Application Data\\Microsoft\\Application-Virtualisierungs-Client*

-   Für Windows Vista, Windows 7, Windows Server2008 –*C:\\ProgramData\\Microsoft\\Application Virtualization Client*

<a href="" id="user-data-directory"></a>**Benutzerdatenverzeichnis**  
Geben Sie den Speicherort des Verzeichnisses ein, in dem benutzerspezifische Daten gespeichert sind, oder suchen Sie nach ihm. Der Standardwert ist% APPDATA%. Dieser Pfad muss eine gültige Umgebungsvariable auf dem Clientcomputer sein.

## Verwandte Themen


[Client Management Console: Application Virtualization-Eigenschaften](client-management-console-application-virtualization-properties.md)

 

 





