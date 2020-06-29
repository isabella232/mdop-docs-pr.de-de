---
title: Informationen zum Veröffentlichen und Aufheben der Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich
description: Informationen zum Veröffentlichen und Aufheben der Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich
author: dansimp
ms.assetid: fd5a62e9-0577-44d2-ae17-61c0aef78ce8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc8f9579d800aa0e5da0d67e0cd71bcae5e912a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812046"
---
# Informationen zum Veröffentlichen und Aufheben der Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich


Obwohl eine Anwendung in einem MED-V-Arbeitsbereich installiert ist, müssen Sie möglicherweise auch die Anwendung veröffentlichen, bevor Sie für den Endbenutzer verfügbar wird. Standardmäßig werden die meisten Anwendungen zu dem Zeitpunkt veröffentlicht, zu dem Sie installiert sind, und Verknüpfungen werden erstellt und aktiviert.

In einigen Fällen möchten Sie möglicherweise Anwendungen im MED-V-Arbeitsbereich installieren, ohne Sie für den Endbenutzer verfügbar zu machen, beispielsweise für die Virenscanner-Software. Es gibt auch Situationen, in denen Sie eine Anwendung veröffentlichen möchten, die auf dem MED-V-Arbeitsbereich installiert ist, die dem Endbenutzer zuvor nicht zur Verfügung stand. Möglicherweise müssen Sie eine installierte Anwendung veröffentlichen, wenn die Installation im **Startmenü** nicht automatisch eine Verknüpfung erstellt hat.

**Wichtig**  Wenn Sie eine Anwendung veröffentlichen, die keine UNC-Pfade unterstützt, empfehlen wir, die Anwendung einem Laufwerk zuzuordnen.

 

Sie können Anwendungen in einem bereitgestellten MED-V-Arbeitsbereich veröffentlichen oder deren Veröffentlichung aufheben, indem Sie eine der folgenden Aufgaben ausführen:

**Veröffentlichen oder Aufheben der Veröffentlichung einer installierten Anwendung**

1.  Wenn Sie eine Anwendung in einem bereitgestellten MED-V-Arbeitsbereich veröffentlichen möchten, kopieren Sie eine Verknüpfung für diese Anwendung in den folgenden Ordner auf dem virtuellen Computer:

    C:\\Dokumente und Einstellungen\\All Users\\Start Menü

    Verwenden Sie bei Bedarf Gruppenrichtlinien oder ein ESD-System, um ein Skript bereitzustellen, das die Verknüpfung für diese Anwendung in den Ordner "All Users\\Start" kopiert.

2.  Wenn Sie die Veröffentlichung einer Anwendung in einem bereitgestellten MED-V-Arbeitsbereich aufheben möchten, löschen Sie die Verknüpfung für diese Anwendung aus dem folgenden Ordner auf dem virtuellen Computer:

    C:\\Dokumente und Einstellungen\\All Users\\Start Menü

    Verwenden Sie bei Bedarf Gruppenrichtlinien oder ein ESD-System, um ein Skript bereitzustellen, das die Verknüpfung für diese Anwendung aus dem Menü Ordner alle Users\\Start löscht.

    **Hinweis**  Häufig wird die Verknüpfung automatisch aus dem **Startmenü** des Hostcomputers gelöscht, wenn Sie die Anwendung deinstallieren. In einigen Fällen, beispielsweise für einen MED-V-Arbeitsbereich, der für alle Benutzer eines freigegebenen Computers konfiguriert ist, müssen Sie möglicherweise die Verknüpfung im **Startmenü** nach der Deinstallation der Anwendung manuell löschen. Der Endbenutzer kann dies tun, indem Sie mit der rechten Maustaste auf die Verknüpfung klicken und dann **Löschen**auswählen.

     

Um zu testen, ob die Anwendung veröffentlicht oder nicht veröffentlicht wurde, überprüfen Sie im MED-V-Arbeitsbereich, ob die entsprechende Verknüpfung verfügbar ist.

**Hinweis**  Anwendungen, die in Windows XP SP3 enthalten sind und sich im Start Menü Ordner des virtuellen Computers befinden, werden nicht automatisch auf dem Host veröffentlicht. Sie werden von Registrierungseinstellungen gesteuert, die die automatische Veröffentlichung blockieren. Weitere Informationen finden Sie unter [Ausschlussliste für Windows Virtual PC-Anwendung](windows-virtual-pc-application-exclude-list.md).

 

**So veröffentlichen Sie Elemente in der Systemsteuerung**

1.  Erstellen Sie eine Verknüpfung auf dem virtuellen Computer, wobei das Ziel der Name des Elements ist, beispielsweise C:\\WINDOWS\\system32\\appwiz.cpl.

    Die Verknüpfung muss entweder erstellt oder in den Ordner "%ALLUSERSPROFILE%\\Start Menu\\" oder einen der Unterordner verschoben werden.

    Das Element wird auf dem Hostcomputer an der entsprechenden Stelle im Start Menü Ordner des Hosts veröffentlicht.

2.  Starten Sie die Verknüpfung für das Element im Host.

**Vorsicht**  Wenn Sie die Verknüpfung erstellen, geben Sie% systemroot% \\control.exe nicht an. Diese Anwendung wird nicht veröffentlicht, da Sie in den Registrierungseinstellungen enthalten ist, die die automatische Veröffentlichung blockieren.

 

**So behandelt MED-V die automatische Anwendungsveröffentlichung**

1.  Während der Anwendungsveröffentlichung kopiert MED-V die Verknüpfungen vom virtuellen Gastcomputer auf den Hostcomputer, indem er versucht, die im Gast vorhandene Ordnerhierarchie zu vergleichen. Auf diese Weise kopiert MED-V mithilfe der folgenden Schritte Verknüpfungen aus dem Gast an den Host:

    1.  MED-V versucht, einen Ordner unter Start Menu\\Programs auf dem Hostcomputer zu finden, der mit dem Ordner in dem Gast identisch ist, in dem sich die Verknüpfung befindet.

    2.  Wenn kein übereinstimmender Ordner vorhanden ist, versucht MED-V dann, einen Ordner im Start Menü Ordner des Hosts zu finden, der mit dem Ordner in dem Gast identisch ist, in dem sich die Verknüpfung befindet.

    3.  Wenn kein übereinstimmender Ordner vorhanden ist, kopiert MED-V die Verknüpfung in den Standardordner auf dem Host, den Ordner Start Menu\\Programs.

2.  Beispiel für den Anwendungs Veröffentlichungsprozess:

    1.  Wenn eine Anwendungsverknüpfung im Ordner Start Menu\\Programs\\AppShortcuts des Gastes veröffentlicht wird, sucht MED-V auf dem Hostcomputer nach einem Ordner Start Menu\\Programs\\ AppShortcuts, und wenn gefunden, wird die Verknüpfung in diesen Ordner kopiert.

    2.  Wenn der Ordner nicht gefunden wird, sucht MED-V auf dem Hostcomputer nach einem Start Menu\\AppShortcuts-Ordner, und wenn gefunden, wird die Verknüpfung in diesen Ordner kopiert.

    3.  Wenn der Ordner nicht gefunden wird, kopiert MED-V die Verknüpfung in den Ordner Start Menu\\Programs.

**Hinweis**  Ein Ordner muss bereits im Start Menü Ordner des Hostcomputers für MED-V vorhanden sein, um die Verknüpfung dort zu kopieren. MED-V erstellt den Ordner nicht, wenn er noch nicht vorhanden ist.

 

## Verwandte Themen


[Installieren und Entfernen einer Anwendung im MED-V-Arbeitsbereich](installing-and-removing-an-application-on-the-med-v-workspace.md)

[Verwalten von Softwareupdates für MED-V-Arbeitsbereiche](managing-software-updates-for-med-v-workspaces.md)

[Liste auszuschließender Anwendungen für virtuelle Windows-PCs](windows-virtual-pc-application-exclude-list.md)

 

 





