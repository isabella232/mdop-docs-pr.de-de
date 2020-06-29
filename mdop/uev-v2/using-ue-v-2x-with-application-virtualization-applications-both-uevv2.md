---
title: Verwenden von UE-V 2. x mit Application Virtualization-Anwendungen
description: Verwenden von UE-V 2. x mit Application Virtualization-Anwendungen
author: dansimp
ms.assetid: 4644b810-fc48-4fd0-96e4-2fc6cd64d8ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221d21c5815b36b57a04a0299352e5fe64f657c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812256"
---
# Verwenden von UE-V 2. x mit Application Virtualization-Anwendungen


Microsoft User Experience Virtualization (UE-v) 2,0, 2,1 und 2,1 SP1 unterstützen Microsoft Application Virtualization (app-v)-Anwendungen ohne erforderliche Änderungen am APP-v-Paket oder der UE-v-Vorlage. Ein weiterer Schritt ist jedoch erforderlich, da Sie den UE-v-Generator nicht direkt in einer virtualisierten App-v-Anwendung ausführen können. Stattdessen müssen Sie die Anwendung lokal installieren, die Vorlage generieren und dann die Vorlage auf die virtualisierte Anwendung anwenden. UE-v unterstützt App-v 4,5, App-v 4,6 und App-v 5,0-Pakete.

## Synchronisierung der UE-v-Einstellungen für App-v-Anwendungen


UE-v überwacht, wenn eine Anwendung durch den Programmnamen und optional durch Dateiversionsnummern und Produktversionsnummern geöffnet wird, unabhängig davon, ob die Anwendung lokal oder virtuell mithilfe von App-v installiert wird. Wenn die Anwendung gestartet wird, überwacht UE-v den App-v-Prozess, wendet alle Einstellungen an, die im Einstellungsspeicher Pfad des Benutzers gespeichert sind, und ermöglicht dann, dass die Anwendung normal gestartet wird. UE-v überwacht App-v-Anwendungen und übersetzt die relevanten Datei-und Registrierungspfade automatisch an den virtualisierten Speicherort, anstatt an den physikalischen Standort außerhalb der APP-v-Computerumgebung.

 **So implementieren Sie die Synchronisierung von Einstellungen für eine virtualisierte Anwendung**

1.  Führen Sie den UE-V-Generator aus, um die Einstellungen der lokal installierten Anwendung zu erfassen, deren Einstellungen Sie zwischen Computern synchronisieren möchten. Durch diesen Vorgang wird eine Vorlage für Einstellungs Speicherort erstellt. Wenn Sie eine integrierte Vorlage wie die Vorlage Microsoft Office 2010 verwenden, überspringen Sie diesen Schritt. Weitere Informationen zum Ausführen des UE-v-Generators finden Sie unter [Bereitstellen von UE-v 2. x für benutzerdefinierte Anwendungen](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).

2.  Installieren Sie das App-V-Anwendungspaket, wenn dies noch nicht geschehen ist.

3.  Veröffentlichen Sie die Vorlage am Speicherort des Vorlagen Katalogs für Einstellungen, oder installieren Sie die Vorlage manuell mithilfe des `Register-UEVTemplate` Windows PowerShell-Cmdlets.

    **Hinweis**  Wenn Sie die neu erstellte Vorlage im Vorlagenkatalog für Einstellungen veröffentlichen, erhält der Client die Vorlage erst, nachdem der Synchronisierungsanbieter die Einstellungen aktualisiert hat. Wenn Sie diesen Vorgang manuell starten möchten, öffnen Sie den **Aufgabenplaner**, erweitern Sie **Aufgabenplanungsbibliothek**, erweitern Sie **Microsoft**, und erweitern Sie **UE-V**. Klicken Sie im Ergebnisbereich mit der rechten Maustaste auf **Vorlage Auto Update**, und klicken Sie dann auf **Ausführen**.

     

4.  Starten Sie das App-V-Paket.






## Verwandte Themen


[Verwalten von UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

 

 





