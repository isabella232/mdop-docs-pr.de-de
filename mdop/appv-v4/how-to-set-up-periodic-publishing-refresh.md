---
title: So richten Sie regelmäßige Veröffentlichungsaktualisierungen ein
description: So richten Sie regelmäßige Veröffentlichungsaktualisierungen ein
author: dansimp
ms.assetid: c358c765-cb88-4881-b4e7-0a2e87304870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5bbea1c661d6cb5a78f0bb9de29538e0222cda6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806752"
---
# So richten Sie regelmäßige Veröffentlichungsaktualisierungen ein


Mit dem folgenden Verfahren können Sie den Client so konfigurieren, dass die Veröffentlichungsinformationen in regelmäßigen Abständen von den App-V-Servern aktualisiert werden. Nachdem der Client konfiguriert wurde, ist der Aktualisierungsvorgang automatisch. Mit diesen Einstellungen werden die Standardeinstellungen für den Client so konfiguriert, dass alle Benutzer auf diesem Computer dieselben Einstellungen sehen.

**Hinweis**  Nachdem Sie diese Schritte ausgeführt haben, werden die Veröffentlichungsinformationen gemäß den neuen Einstellungen nach der ersten Aktualisierung bei der Anmeldung aktualisiert. Wenn diese erste Aktualisierung erfolgt, kann der Server je nach Konfiguration die Computereinstellungen mit unterschiedlichen Einstellungen außer Kraft setzen. Auf der Registerkarte " **Aktualisieren** " im Dialogfeld " **Eigenschaften** " werden die lokal konfigurierten Clientcomputereinstellungen sowie alle Einstellungen angezeigt, die möglicherweise vom Veröffentlichungsserver für den Benutzer konfiguriert wurden.

 

**So aktualisieren Sie die Veröffentlichungsinformationen in regelmäßigen Abständen von den Application Virtualization-Servern**

1.  Klicken Sie **im Bereich Bereich** auf **Veröffentlichungsserver** .

2.  Klicken Sie im **Ergebnis** Bereich mit der rechten Maustaste auf den gewünschten Server, und wählen Sie im Popup-Menü **Eigenschaften** aus.

3.  Aktivieren Sie im Dialogfeld **Eigenschaften** auf der Registerkarte **Aktualisieren** das Kontrollkästchen **Konfiguration aktualisieren alle** , und geben Sie eine Zahl ein, die die Häufigkeit im Feld darstellt. Wählen Sie dann im Dropdownmenü die Option **Minuten**, **Stunden**und **Tage** aus.

    **Hinweis**  Diese Einstellung bewirkt, dass der Client die Veröffentlichungsinformationen jedes Mal aktualisiert, wenn der konfigurierte Zeitraum abgelaufen ist. Wenn der Benutzer nicht angemeldet ist, wenn es Zeit ist, eine Aktualisierung durchführen zu lassen, wird die Aktualisierung durchgeführt, wenn sich der Benutzer beim nächsten Mal anmeldet. Der Timer wird dann für den nächsten Zeitraum erneut gestartet.

     

4.  Klicken Sie auf über **nehmen** , um die Konfiguration zu ändern.

5.  Wenn Sie die Konfiguration des Servers abgeschlossen haben, klicken Sie auf **OK** , um das Dialogfeld zu schließen und zur Application Virtualization Client Management Console zurückzukehren.

## Verwandte Themen


[So konfigurieren Sie den Client in der Application Virtualization Client Management Console](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

 

 





