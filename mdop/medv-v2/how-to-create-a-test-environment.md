---
title: So erstellen Sie eine Testumgebung
description: So erstellen Sie eine Testumgebung
author: dansimp
ms.assetid: a0db2299-16f3-4516-8769-7d55ca4a1e98
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ee2ab131f6003b56cce7a60ffea1cd00b067fae3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812265"
---
# So erstellen Sie eine Testumgebung


Im folgenden finden Sie einige Schritte und Anweisungen, die Sie beim Erstellen einer Testumgebung unterstützen, die Sie verwenden können, um Ihr MED-V Workspace-Paket lokal zu testen, bevor Sie es im gesamten Unternehmen bereitstellen. Dieser Abschnitt enthält Anleitungen zum Erstellen einer Testumgebung, entweder manuell oder mithilfe eines elektronischen Softwareverteilungssystems.

**So erstellen Sie eine Testumgebung mithilfe eines ESD**

1.  Verwenden Sie die Methode des Unternehmens zur Bereitstellung von Software im gesamten Unternehmen, um die folgenden erforderlichen Komponenten auf einem Testcomputer bereitzustellen. Installieren Sie Sie in der folgenden Reihenfolge:

    -   **Windows Virtual PC** – Falls noch nicht installiert. Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.

    -   **Windows Virtual PC-Ergänzungen und-Updates**– Falls noch nicht installiert. Weitere Informationen finden Sie unter [Konfigurieren der Voraussetzungen](configure-installation-prerequisites.md)für die Installation.

    -   **Installationsdatei des Med-v-Host-Agents** – installiert den Host-Agent (Med-v \ _HostAgent \ _setup Installationsdatei). Weitere Informationen finden Sie unter [Manuelles Installieren des MED-V-Host-Agents](how-to-manually-install-the-med-v-host-agent.md).

    -   Das **Med-v Workspace-Installationsprogramm, die VHD und die Setup-Datei** , die im **Med-v-Arbeitsbereichs Paket**erstellt wurde. Weitere Informationen finden Sie unter [Erstellen eines MED-V-Arbeitsbereichs Pakets](create-a-med-v-workspace-package.md).

        **Wichtig**  Das ausführbare Programm für VHD und Setup muss sich im gleichen Ordner wie das MED-V Workspace-Installationsprogramm befinden. Installieren Sie dann das MED-V Workspace-Installationsprogramm, indem Sie setup.exe ausführen.

         

2.  Nachdem alle Komponenten auf dem Testcomputer installiert wurden, führen Sie den MED-V-Host-Agent aus, um die erstmalige Einrichtung zu starten.

    Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Enterprise Desktop Virtualization**, und klicken Sie dann auf **MED-V-Host-Agent**.

    **Hinweis**  Wenn Sie den MED-V-Host-Agent nicht physisch auf dem Testcomputer ausführen können, wird das erstmalige Setup beim nächsten Neustart des Computers automatisch gestartet.

     

Das erstmalige Setup wird gestartet, und es kann zehn Minuten oder mehr dauern, bis der Vorgang abgeschlossen ist.

Informationen zum Testen Ihrer Konfigurationseinstellungen bei der erstmaligen Einrichtung von Setup finden Sie unter [Überprüfen der Einstellungen für die erstmalige Einrichtung](how-to-verify-first-time-setup-settings.md).

**So erstellen Sie eine Testumgebung manuell**

1.  Installieren Sie den Med-v-Host-Agent in einer lokalen Testumgebung, die Med-v-Voraussetzungen enthält, beispielsweise Windows Virtual PC mit Ergänzungen und Updates. Informationen finden Sie unter [Manuelles Installieren des MED-V-Host-Agents](how-to-manually-install-the-med-v-host-agent.md).

2.  Kopieren Sie die MED-V Workspace-Dateien in Ihre Testumgebung. Die Med-v-Arbeitsbereichsdateien befinden sich im Zielordner, den Sie im **Med-v Workspace-Paketer**angegeben haben.

    **Wichtig**  Das ausführbare Programm für VHD und Setup muss sich im gleichen Ordner wie das MED-V Workspace-Installationsprogramm in Ihrer Testumgebung befinden.

     

3.  Installieren Sie den MED-V-Arbeitsbereich, indem Sie setup.exe ausführen.

4.  Starten Sie die erstmalige Einrichtung, indem Sie den MED-V-Host-Agent ausführen.

    Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft Enterprise Desktop Virtualization**, und klicken Sie dann auf **MED-V-Host-Agent**.

Das erstmalige Setup wird gestartet, und je nach Größe der festgelegten VHD kann es einige Minuten dauern.

Nun können Sie die verschiedenen Einstellungen für Konfiguration, Anwendungsveröffentlichung und URL-Umleitung testen, die Sie für Ihren MED-V-Arbeitsbereich angegeben haben.

**Hinweis**  Standardmäßig überschreibt MED-V die Richtlinie für die Bildschirmsperre im Gast. Dies stellt jedoch kein Sicherheitsproblem dar, da der Hostcomputer weiterhin die Richtlinie für die Bildschirmsperre berücksichtigt.

 

## Verwandte Themen


[So überprüfen Sie erstmalige Einstellungen für das Setup](how-to-verify-first-time-setup-settings.md)

[So testen Sie die Anwendungsveröffentlichung](how-to-test-application-publishing.md)

[So testen Sie die URL-Umleitung](how-to-test-url-redirection.md)

 

 





