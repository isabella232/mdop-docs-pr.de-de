---
title: So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile
description: So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile
author: dansimp
ms.assetid: 3e3d873f-13d2-402f-97b4-f62d0c399171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c424f39c8209ca641f6073838ebcb8726acc9e25
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807291"
---
# So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile


Nachdem der Application Virtualization (App-V)-Client während der Installation über die Befehlszeile bereitgestellt und konfiguriert wurde, ist es möglicherweise erforderlich, eine oder mehrere Clientkonfigurationseinstellungen zu ändern. Dies erfolgt durch Bearbeiten der entsprechenden Registrierungsschlüssel mithilfe einer der folgenden Methoden:

-   Direktes Verwenden des Registrierungs-Editors

-   Verwenden einer REG-Datei

-   Verwenden einer Skriptsprache wie VBScript oder Windows PowerShell

Es gibt auch eine ADM-Vorlage, die Sie verwenden können. Weitere Informationen zur ADM-Vorlage finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=121835> .

**Vorsicht**  Verwenden Sie beim Bearbeiten der Registrierung Vorsicht, da Fehler den Computer in einem unbrauchbaren Zustand belassen können. Befolgen Sie unbedingt Ihre Standard Geschäftsmethoden, die sich auf Registrierungsänderungen beziehen. Testen Sie alle vorgeschlagenen Änderungen in einer Testumgebung gründlich, bevor Sie Sie auf Produktionscomputern bereitstellen.

 

## Inhalt dieses Abschnitts


**Wichtig**  Auf einem 64-Bit-Computer finden Sie die in den folgenden Abschnitten beschriebenen Schlüssel und Werte unter HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid\\4.5\\client.

 

<a href="" id="how-to-reset-the-filesystem-cache"></a>[So setzen Sie den Dateisystemcache zurück](how-to-reset-the-filesystem-cache.md)  
Enthält die Informationen, die erforderlich sind, um den Dateisystemcache zurückzusetzen.

<a href="" id="how-to-change-the-size-of-the-filesystem-cache"></a>[So ändern Sie die Größe des Dateisystemcaches](how-to-change-the-size-of-the-filesystem-cache.md)  
Erläutert, wie Sie die Größe des Caches ändern können.

<a href="" id="how-to-use-the-cache-space-management-feature"></a>[So verwenden Sie das Verwaltungsfeature für den Cachespeicher](how-to-use-the-cache-space-management-feature.md)  
Beschreibt, wie Sie das Feature für die Cachespeicherverwaltung konfigurieren können.

<a href="" id="how-to-configure-the-client-log-file"></a>[So konfigurieren Sie die Clientprotokolldatei](how-to-configure-the-client-log-file.md)  
Beschreibt die verschiedenen Registrierungsschlüsselwerte, die die Clientprotokolldatei steuern, und wie Sie Sie ändern können.

<a href="" id="how-to-configure-user-permissions"></a>[So konfigurieren Sie Benutzerberechtigungen](how-to-configure-user-permissions.md)  
Identifiziert den Registrierungsschlüssel, der die Benutzerberechtigungen steuert, und gibt Beispiele dafür, wie Sie einige Berechtigungen ändern können.

<a href="" id="how-to-configure-the-client-for-application-package-retrieval"></a>[So konfigurieren Sie den Client für den Abruf von Anwendungspaketen](how-to-configure-the-client-for-application-package-retrieval.md)  
Es wird erläutert, wie Sie den Client so konfigurieren, dass Paketinhalte, Symbole und Dateitypzuordnungen aus unterschiedlichen Quellen abgerufen werden, und es werden mehrere Beispiele für das richtige Pfadformat bereitgestellt.

<a href="" id="how-to-configure-the-client-for-disconnected-operation-mode"></a>[So konfigurieren Sie den Client für den unterbrochenen Betriebsmodus](how-to-configure-the-client-for-disconnected-operation-mode.md)  
Enthält Informationen zum Konfigurieren der verschiedenen Einstellungen, die mit dem Modus für getrennte Vorgänge verbunden sind.

<a href="" id="how-to-configure-shortcut-and-file-type-association-behavior"></a>[So konfigurieren Sie das Verhalten von Verknüpfungen und Dateitypzuordnungen](how-to-configure-shortcut-and-file-type-association-behavior-46-only.md)  
Beschreibt die Registrierungsschlüsselwerte, die Tastenkombinationen und Dateitypzuordnungen im App-V-Client steuern, und enthält Details zur Konfiguration.

## Verwandte Themen


[Application Virtualization Client](application-virtualization-client.md)

 

 





