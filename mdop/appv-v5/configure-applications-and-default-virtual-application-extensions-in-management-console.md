---
title: Konfigurieren von Anwendungen und Standard-Erweiterungen für virtuelle Anwendungen in der Verwaltungskonsole
description: So zeigen Sie mithilfe der Verwaltungskonsole Anwendungen und virtuelle Standardanwendungserweiterungen an und konfigurieren sie
author: dansimp
ms.assetid: 1e1941d3-fb22-4077-8ec6-7a0cb80335d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2019
ms.openlocfilehash: 7c29ba0e40cf1adbc2b2297124cfb245a65a7ffe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805927"
---
#   Konfigurieren von Anwendungen und Standard-Erweiterungen für virtuelle Anwendungen in der Verwaltungskonsole

Gehen Sie wie folgt vor, um Standardpaket Erweiterungen *anzuzeigen* und zu *Konfigurieren* .

**So können Sie die Standarderweiterungen für virtuelle Anwendungen anzeigen und konfigurieren**

1.  Um das Paket anzuzeigen, das Sie konfigurieren möchten, öffnen Sie die App-V 5,1-Verwaltungskonsole. Wählen Sie das Paket aus, das Sie konfigurieren möchten, klicken Sie mit der rechten Maustaste auf den Paketnamen, und wählen Sie **Standardkonfiguration bearbeiten**aus.

2.  Wenn Sie die im angegebenen Paket enthaltenen Anwendungen anzeigen möchten, klicken Sie im Bereich **Standardkonfiguration** auf **Anwendungen**. Wenn Sie die Tastenkombinationen für dieses Paket anzeigen möchten, klicken Sie auf **Tastenkombinationen**. Wenn Sie die Dateitypzuordnungen für dieses Paket anzeigen möchten, klicken Sie auf **Dateitypen**.

3.  Wenn Sie die Anwendungserweiterungen aktivieren möchten, wählen Sie **aktivieren**aus.

    Wenn Sie Tastenkombinationen aktivieren möchten, wählen Sie **Tastenkombinationen aktivieren**aus. Wenn Sie eine neue Verknüpfung für die ausgewählte Anwendung hinzufügen möchten, klicken Sie im Bereich " **Verknüpfungen** " mit der rechten Maustaste auf die Anwendung, und wählen Sie **neue Verknüpfung hinzufügen**aus. Um eine Verknüpfung zu entfernen, klicken Sie im Bereich " **Verknüpfungen** " mit der rechten Maustaste auf die Anwendung, und wählen Sie **Verknüpfung entfernen**aus. Wenn Sie eine vorhandene Verknüpfung bearbeiten möchten, klicken Sie mit der rechten Maustaste auf die Anwendung, und wählen Sie **Verknüpfung bearbeiten**aus.

4.  Wenn Sie weitere Anwendungserweiterungen anzeigen möchten, klicken Sie auf **erweitert** , und klicken Sie dann auf **Konfiguration exportieren**. Geben Sie einen Dateinamen ein, und klicken Sie auf **Speichern**. Mit der Konfigurationsdatei können Sie alle Anwendungserweiterungen anzeigen, die dem Paket zugeordnet sind.

5.  Wenn Sie andere Anwendungserweiterungen bearbeiten möchten, ändern Sie die Konfigurationsdatei, und klicken Sie auf **importieren, und überschreiben Sie diese Konfiguration**. Wählen Sie die geänderte Datei aus, und klicken Sie auf **Öffnen**. Klicken Sie im Dialogfeld auf über **Schreiben** , um den Vorgang abzuschließen.

>**Hinweis** Wenn der Upload fehlschlägt und die Größe Ihrer Konfigurationsdatei über 4MB liegt, müssen Sie die vom Server zulässige maximale Dateigröße erhöhen. Dies kann durch Hinzufügen des maxRequestLength-Attributs mit einem Wert erfolgen, der größer als die Größe Ihrer Konfigurationsdatei (in KB) dem httpRuntime-Element in Zeile 26 von ist `C:\Program Files\Microsoft Application Virtualization Server\ManagementService\Web.config` .  
Wenn Sie beispielsweise `<httpRuntime targetFramework="4.5"/>` auf ändern, `<httpRuntime targetFramework="4.5" maxRequestLength="8192"/>` wird die maximale Größe auf 8MB erhöht.


Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.1](operations-for-app-v-51.md)

 

 





