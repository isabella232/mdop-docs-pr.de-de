---
title: Installieren und Entfernen einer Anwendung im MED-V-Arbeitsbereich
description: Installieren und Entfernen einer Anwendung im MED-V-Arbeitsbereich
author: dansimp
ms.assetid: 24f32720-51ab-4385-adfe-4f5a65e45fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 22cb98c167b53b1b206b8b5be2ba18fc0fba4f06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812223"
---
# Installieren und Entfernen einer Anwendung im MED-V-Arbeitsbereich


Anwendungen, die mit dem Betriebssystem "Host" nicht kompatibel sind, können im Med-v-Arbeitsbereich ausgeführt und im Med-v-Arbeitsbereich auf die gleiche Weise wie auf dem Hostcomputer, im **Startmenü** oder mithilfe einer localhost-Verknüpfung geöffnet werden.

Nachdem Sie einen Med-v-Arbeitsbereich bereitgestellt haben, stehen Ihnen verschiedene Optionen zum Installieren und Entfernen von Anwendungen im Med-v-Arbeitsbereich zur Verfügung. Zu den folgenden Optionen gehören:

-   [Verwenden von Gruppenrichtlinien](#bkmk-grouppolicy)

-   [Verwenden eines elektronischen Software Verteilungssystems](#bkmk-esd)

-   [Verwenden von Application Virtualization (App-V)](#bkmk-appv)

-   [Aktualisieren des Kern Abbilds](#bkmk-coreimage)

**Wichtig**  Wenn Sie sicherstellen möchten, dass eine installierte Anwendung automatisch auf dem Host veröffentlicht wird, installieren Sie die Anwendung auf dem virtuellen Computer für **alle Benutzer**. Weitere Informationen zur Anwendungsveröffentlichung finden Sie unter [veröffentlichen und Aufheben der Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).

 

**Tipp**  Med-v unterstützt keine Gast-zu-Host-Umleitung für die Inhaltsbehandlung, wie das Doppelklicken auf ein Microsoft Word-Dokument in Internet Explorer im Med-v-Arbeitsbereich. Daher müssen die erforderlichen Anwendungen wie Microsoft Word in MED-V Workspace installiert werden, um die standardmäßige Inhalts Behandlungsfunktion bereitzustellen, die ein Endbenutzer möglicherweise erwartet.

 

## <a href="" id="bkmk-grouppolicy"></a> Hinzufügen und Entfernen von Anwendungen mithilfe von Gruppenrichtlinien


Sie können Gruppenrichtlinien-und Gruppenrichtlinienobjekte verwenden, um Anwendungen allen oder einigen MED-V-Arbeitsbereichen in Ihrem Unternehmen zuzuweisen oder zu veröffentlichen. Bei zugewiesenen Anwendungen wird die Anwendung im **Startmenü** angezeigt, wenn sich ein Endbenutzer bei seinem Computer anmeldet. Wenn Sie die neue Anwendung zum ersten Mal auswählen, wird die Anwendung installiert und kann verwendet werden. Für veröffentlichte Anwendungen wird die Anwendung nicht im **Startmenü** angezeigt. Sie steht nur für den Endbenutzer zur Verfügung, indem Sie in der **System** Steuerung **Software** verwenden oder eine Datei öffnen, die der Anwendung zugeordnet ist.

Sie können auch Gruppenrichtlinien-und Gruppenrichtlinienobjekte auf die gleiche Weise verwenden, um Anwendungen aus dem MED-V-Arbeitsbereich zu entfernen.

Weitere Informationen zum Hinzufügen und Entfernen von Anwendungen mithilfe von Gruppenrichtlinien finden Sie unter [Gruppenrichtlinien-Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

## <a href="" id="bkmk-esd"></a> Hinzufügen und Entfernen von Anwendungen mithilfe eines ESD-Systems


Ein ESD-System (Electronic Software Distribution) ist so konzipiert, dass Software und andere Informationen auf vielen verschiedenen Computern über Netzwerkverbindungen effizient bereitgestellt werden können. Wenn Ihre Organisation ein ESD-System zum Bereitstellen von Software verwendet, können Sie diese zum Hinzufügen und Entfernen von Anwendungen in MED-V-Arbeitsbereichen verwenden, genauso wie beim Hinzufügen und Entfernen von Anwendungen auf physischen Computern.

## <a href="" id="bkmk-appv"></a> Hinzufügen und Entfernen von Anwendungen mithilfe von App-V


Microsoft Application Virtualization (App-V) bietet die Verwaltungsfunktion, um Anwendungen für Endbenutzercomputer verfügbar zu machen, ohne die Anwendungen direkt auf diesen Computern installieren zu müssen. Möglicherweise möchten Sie Med-v und App-v zusammen verwenden, wenn Ihre Organisation beispielsweise Anwendungen aufweist, die Sie mit App-v in Windows XP sequenziert haben, und Sie durch eine erneute Sequenzierung Ihre Migration zu Windows 7 verzögern würden.

Sie können Med-v zusammen mit App-v verwenden, um virtuelle Anwendungen in einem bereitgestellten Med-v-Arbeitsbereich hinzuzufügen oder zu entfernen. Zum Verwalten von Anwendungen auf diese Weise müssen Sie zuerst den App-v-Agent auf dem Med-v-Gastbetriebssystem installieren. Sie können dann App-v im Med-v-Arbeitsbereich verwenden, um die virtuellen Anwendungen hinzuzufügen und zu entfernen.

Informationen zum Installieren und Verwenden von App-V finden Sie unter [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .

**Wichtig**  App-v-Anwendungen, die Sie im Med-v-Arbeitsbereich veröffentlichen, weisen Dateitypzuordnungen auf, die nicht vom Hostcomputer auf den virtuellen Gastcomputer umgeleitet werden können. Der Endbenutzer kann jedoch weiterhin auf diese Dateitypen zugreifen, indem Sie auf **Datei**und dann in der veröffentlichten App-V-Anwendung auf **Öffnen** klicken.

Wenn Sie die Umleitung dieser Dateitypzuordnungen erzwingen möchten, geben Sie App-V für zugeordnete Dateitypzuordnungen an, indem Sie Folgendes an einer Eingabeaufforderung auf dem virtuellen Gastcomputer eingeben: **SFTMIME/Query obj: Type**. Ordnen Sie dann diese Dateitypzuordnungen auf dem Hostcomputer zu.

 

## <a href="" id="bkmk-coreimage"></a> Hinzufügen und Entfernen von Anwendungen im Core-Abbild


Obwohl es sich nicht um ein MED-V-bewährtes Verfahren handelt, können Sie Anwendungen direkt im kernbild hinzufügen und entfernen. Nachdem Sie eine Anwendung hinzugefügt oder entfernt haben, können Sie den MED-V-Arbeitsbereich wieder in Ihrem Unternehmen bereitstellen, genauso wie Sie ihn ursprünglich bereitgestellt haben.

Weitere Informationen zum Hinzufügen oder Entfernen von Anwendungen für das kernbild finden Sie unter [Installieren von Anwendungen auf einem Windows Virtual PC-Abbild](installing-applications-on-a-windows-virtual-pc-image.md).

**Wichtig**  Diese Methode zum Verwalten von Anwendungen wird nicht empfohlen. Wenn Sie Anwendungen im kernbild hinzufügen oder entfernen und den MED-V-Arbeitsbereich wieder in Ihrem Unternehmen bereitstellen, muss das erstmalige Setup erneut ausgeführt werden, und alle auf dem virtuellen Computer gespeicherten Daten gehen verloren.

 

**Hinweis**  Obwohl eine Anwendung in einem MED-V-Arbeitsbereich installiert ist, müssen Sie möglicherweise auch die Anwendung veröffentlichen, bevor Sie für den Endbenutzer verfügbar wird. Möglicherweise müssen Sie eine installierte Anwendung veröffentlichen, wenn die Installation im **Startmenü** nicht automatisch eine Verknüpfung erstellt hat. Wenn Sie die Veröffentlichung einer Anwendung aufheben möchten, müssen Sie möglicherweise eine Verknüpfung manuell aus dem **Startmenü** entfernen.

Standardmäßig werden die meisten Anwendungen zu dem Zeitpunkt veröffentlicht, zu dem Sie installiert werden, wenn Verknüpfungen automatisch erstellt und aktiviert werden.

 

## Verwandte Themen


[So testen Sie die Anwendungsveröffentlichung](how-to-test-application-publishing.md)

[Informationen zum Veröffentlichen und Aufheben der Veröffentlichung einer Anwendung im MED-V-Arbeitsbereich](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





