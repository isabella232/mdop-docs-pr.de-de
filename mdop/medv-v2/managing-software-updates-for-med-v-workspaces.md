---
title: Verwalten von Softwareupdates für MED-V-Arbeitsbereiche
description: Verwalten von Softwareupdates für MED-V-Arbeitsbereiche
author: dansimp
ms.assetid: a28d6dcd-cb9f-46ba-8dac-1d990837a3a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 696238a2f5ad9b7e5120f75f6cd09d890d12519b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810780"
---
# Verwalten von Softwareupdates für MED-V-Arbeitsbereiche


Für die Bereitstellung von Softwareupdates für die Anwendungen im bereitgestellten MED-V-Arbeitsbereich stehen Ihnen verschiedene Optionen zur Verfügung.

**Hinweis**  Informationen dazu, wie Sie die Konfigurationseinstellungen angeben, die definieren, wie Med-v automatische Updates erhält, finden Sie unter [Verwalten von automatischen Updates für med-v-Arbeitsbereiche](managing-automatic-updates-for-med-v-workspaces.md).

 

**Aktualisieren von Software in einem MED-V-Arbeitsbereich**

1.  **Verwenden eines elektronischen Software Verteilungssystems**

    Wenn Ihr Unternehmen ein ESD-System (Electronic Software Distribution System) zum Bereitstellen von Software verwendet, können Sie es verwenden, um Softwareupdates für Anwendungen in MED-V-Arbeitsbereichen bereitzustellen, genauso wie Sie Updates für Anwendungen auf physischen Computern bereitstellen.

2.  **Verwenden von Gruppenrichtlinien**

    Wenn Ihre Organisation Software mithilfe von Gruppenrichtlinien bereitstellt, können Sie Sie verwenden, um Softwareupdates für Anwendungen in MED-V-Arbeitsbereichen bereitzustellen, genauso wie Sie Updates für Anwendungen auf physischen Computern bereitstellen.

3.  **Verwenden von Application Virtualization (App-V)**

    Wenn Sie Med-v zusammen mit App-v verwenden, können Sie Softwareupdates für Anwendungen im Med-v-Arbeitsbereich bereitstellen, indem Sie die Schritte ausführen, die für App-v zum Aktualisieren von Software erforderlich sind. Weitere Informationen finden Sie unter [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .

4.  **Aktualisieren der Software im Core-Abbild**

    Obwohl es sich nicht um eine MED-V-bewährte Methode handelt, können Sie Softwareupdates für Anwendungen im Core-Abbild installieren. Nachdem Sie die Updates installiert haben, können Sie den MED-V-Arbeitsbereich wieder in Ihrem Unternehmen bereitstellen, genauso wie Sie ihn ursprünglich bereitgestellt haben.

    **Wichtig**  Diese Methode zum Verwalten von Softwareupdates wird nicht empfohlen. Wenn Sie außerdem Software im kernbild aktualisieren und den MED-V-Arbeitsbereich wieder in Ihrem Unternehmen bereitstellen, muss das erstmalige Setup erneut ausgeführt werden, und alle auf dem virtuellen Computer gespeicherten Daten gehen verloren.

     

## Verwandte Themen


[Verwalten von automatischen Updates für MED-V-Arbeitsbereiche](managing-automatic-updates-for-med-v-workspaces.md)

[So testen Sie die Anwendungsveröffentlichung](how-to-test-application-publishing.md)

[Informationen zum Veröffentlichen und Aufheben der Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





