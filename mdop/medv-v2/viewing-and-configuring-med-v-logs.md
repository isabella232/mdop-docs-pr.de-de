---
title: Anzeigen und Konfigurieren von MED-V-Protokollen
description: Anzeigen und Konfigurieren von MED-V-Protokollen
author: dansimp
ms.assetid: a15537ce-981d-4f55-9c3c-e7fbf94b8fe5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7984cec072827136db9ea52a535c0ea44c6bc2c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810129"
---
# Anzeigen und Konfigurieren von MED-V-Protokollen


Wenn Sie Probleme und Probleme mit Med-v beheben, finden Sie es möglicherweise hilfreich oder notwendig, auf die Med-v-Ereignisprotokolle zuzugreifen. Mit dem MED-V Administration Toolkit können Sie die Ereignisanzeige für den Hostcomputer und den virtuellen Gastcomputer öffnen. Sie können auch das Med-v-Administrations-Toolkit verwenden, um den Protokolliergrad festzulegen, auf dem die Med-v-Ereignisprotokolle Bericht Med-v-Ereignisse protokollieren.

Informationen zum Öffnen des Med-v-Administrations-Toolkits finden Sie unter [Problembehandlung bei Med-v mit dem Administrations-Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).

## Anzeigen von MED-V-Ereignisprotokollen


Klicken Sie im Fenster **MED-V Administration Toolkit** auf **Host Ereignisse** , um die Ereignisanzeige für den Hostcomputer zu öffnen. Oder klicken Sie auf **gastereignisse** , um die Ereignisanzeige für den virtuellen Gastcomputer zu öffnen.

Die Ereignisanzeige wird geöffnet und zeigt die entsprechenden Ereignisprotokolle an, mit denen Sie die Probleme behandeln können, die beim Bereitstellen oder Verwalten von MED-V auftreten können. Standardmäßig werden nur Fehler und Warnungen angezeigt. Weitere Informationen zu bestimmten Ereignis-IDs und Nachrichten finden Sie unter [MED-V-Ereignisprotokollmeldungen](med-v-event-log-messages.md).

**Hinweis**  Endbenutzer können Ereignisprotokolldateien nur im Gast speichern, wenn Sie über Administratorberechtigungen verfügen.

 

### So öffnen Sie die Ereignisanzeige auf dem Hostcomputer manuell

1.  Klicken Sie auf **Start**, klicken Sie auf **System**Steuerung, und klicken Sie dann auf **Verwaltungs Tools**.

2.  Doppelklicken Sie auf **Ereignisanzeige**, und klicken Sie dann auf **Anwendungen und Dienstprotokolle**.

3.  Doppelklicken Sie auf **MEDV**.

## Konfigurieren von MED-V-Ereignisprotokollen


Sie können die Med-v-Ereignisprotokollierungsstufe angeben, indem Sie das entsprechende Optionsfeld im Med-v-Administrations-Toolkit auswählen. Sie können entscheiden, ob die Ereignisprotokollierung nur Fehler, Fehler und Warnungen sowie Fehler, Warnungen und Informationsmeldungen enthält. Der angegebene ereignisprotokollierungsgrad wird sowohl für den Hostcomputer als auch für den virtuellen Gastcomputer festgelegt.

Sie können auch die Ereignisprotokollierungsstufe angeben, indem Sie den Registrierungswert EventLogLevel bearbeiten. Weitere Informationen finden Sie unter [Verwalten von MED-V Workspace-Konfigurationseinstellungen](managing-med-v-workspace-configuration-settings.md).

**Hinweis**  Die Ebene, die Sie im Fenster **Med-v-Administrations-Toolkit** angeben, bezieht sich auf die zukünftige Med-v-Ereignisprotokollierung. Wenn Sie die Ebene so festzulegen, dass alle Fehler, Warnungen und Informationsmeldungen erfasst werden, werden die Ereignisprotokolle schneller gefüllt, und ältere Ereignisse werden entfernt.

 

## Verwandte Themen


[Neu starten und das Zurücksetzen eines MED-V-Arbeitsbereichs](restarting-and-resetting-a-med-v-workspace.md)

[Anzeigen von MED-V-Arbeitsbereichskonfigurationen](viewing-med-v-workspace-configurations.md)

 

 





