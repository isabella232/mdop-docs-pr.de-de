---
title: Liste auszuschließender Anwendungen für virtuelle Windows-PCs
description: Liste auszuschließender Anwendungen für virtuelle Windows-PCs
author: dansimp
ms.assetid: 7715f198-f5ed-421e-8740-0cec2ca4ece3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/28/2017
ms.openlocfilehash: 190049ce99865ef237d8d26e14a8279def7da521
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810108"
---
# Liste auszuschließender Anwendungen für virtuelle Windows-PCs


In einigen Fällen möchten Sie möglicherweise nicht, dass im MED-V-Arbeitsbereich installierte Anwendungen im **Startmenü** des Hostcomputers veröffentlicht werden. Sie können die Veröffentlichung dieser Anwendungen aufheben, indem Sie die Anweisungen unter Veröffentlichen und Aufheben der [Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)befolgen. Wenn das Programm allerdings immer automatisch aktualisiert wird, wird es möglicherweise auch automatisch erneut veröffentlicht. Dies führt dazu, dass Sie die Veröffentlichung der Anwendung erneut aufheben müssen.

Windows Virtual PC enthält ein Feature, das als "Ausschlussliste" bezeichnet wird, mit der Sie bestimmte installierte Anwendungen angeben können, die nicht **im Startmenü des Hosts veröffentlicht** werden sollen. Die "Ausschlussliste" befindet sich in der gastregistrierung im HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList-Schlüssel und listet die Anwendungen auf, die nicht im **Start** Menü des Hosts veröffentlicht werden. Sie können sich die "Ausschlussliste" als permanente Aufhebung der Veröffentlichung der angegebenen Anwendungen vorstellen, da automatische Updates für die aufgelisteten Anwendungen nicht dazu führen, dass Sie automatisch erneut veröffentlicht werden.

## Verwalten von Anwendungen mithilfe der Ausschlussliste in Windows Virtual PC


****

1.  Öffnen Sie den Arbeitsbereich MED-V im Vollbildmodus.

    Informationen zum Öffnen des Med-v-Arbeitsbereichs im Vollbildmodus mithilfe des Med-v-Administrations-Toolkits finden Sie unter [Anzeigen von Med-v-Arbeitsbereichskonfigurationen](viewing-med-v-workspace-configurations.md#bkmk-fullscreen). Sie können Sie aber auch manuell im Vollbildmodus öffnen, indem Sie auf **Start**, dann auf **Alle Programme**, auf **Windows Virtual PC**, auf **Windows Virtual PC**und dann auf den MED-V-Arbeitsbereich doppelklicken.

2.  Öffnen Sie im Windows Virtual PC-Fenster des MED-V Workspace den Registrierungs-Editor.

    Klicken Sie auf **Start**, klicken Sie auf **Ausführen**, und geben Sie dann regedit ein. Klicken Sie dann auf **OK**.

3.  Suchen Sie im Registrierungs-Editor den Registrierungsschlüssel HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList.

4.  Erstellen Sie einen neuen Registrierungswert für die installierte Anwendung, die nicht im **Startmenü** des Hostcomputers veröffentlicht werden soll. Wenn Sie beispielsweise die Veröffentlichung des automatisch veröffentlichten Programms Microsoft Silverlight aufheben möchten, führen Sie die folgenden Schritte aus:

    1.  Klicken Sie mit hervorgehobenem VPCVAppExcludeList-Registrierungsschlüssel auf **Bearbeiten**, klicken Sie auf **neu**, und klicken Sie dann auf **Zeichenfolgenwert**.

    2.  Geben Sie den Namen für den neuen Registrierungswert ein. Für Microsoft Silverlight können Sie beispielsweise sllauncher.exe eingeben.

    3.  Doppelklicken Sie auf den neuen Registrierungswert, und geben Sie die Wertdaten ein.

        Die Wertdaten sind der vollständige Pfad für den Befehl, dessen Veröffentlichung Sie aufheben möchten. Sie können den vollständigen Pfad finden, indem Sie mit der rechten Maustaste auf die Verknüpfung im **Startmenü** für die Anwendung klicken, die nicht veröffentlicht werden soll, und dann auf **Eigenschaften**klicken. Der vollständige Pfad wird auf der Registerkarte **Verknüpfung** unter **Ziel**angezeigt.

        Für das Programm Microsoft Silverlight kann der vollständige Pfad beispielsweise "c:\\Programme c:\\Programme\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe" sein.

        **Wichtig**  Falls zutreffend, entfernen Sie die Anführungszeichen aus dem vollständigen Pfad, wenn Sie Sie in das Datenfeld "Wert" eingeben.

         

5.  Schließen Sie den Registrierungs-Editor, und starten Sie den virtuellen Computer mit dem MED-V Workspace neu.

    Die Anwendung ist weiterhin im MED-V-Arbeitsbereich installiert, wird aber jetzt aus dem **Startmenü** des Hostcomputers entfernt.

Sie können auch eine ausgeschlossene Anwendung im **Startmenü** des Hosts erneut veröffentlichen, indem Sie den entsprechenden Wert aus dem VPCVAppExcludeList-Schlüssel löschen. Wenn Sie beispielsweise Microsoft Silverlight erneut veröffentlichen möchten, klicken Sie mit der rechten Maustaste auf den Registrierungswert sllauncher.exe, und wählen Sie **Löschen**aus.

## Verwandte Themen


[Technische Referenz für MED-V](technical-reference-for-med-v.md)

[Informationen zum Veröffentlichen und Aufheben der Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





