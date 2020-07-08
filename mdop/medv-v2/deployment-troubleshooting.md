---
title: Problembehandlung bei der Bereitstellung
description: Problembehandlung bei der Bereitstellung
author: dansimp
ms.assetid: 9ee980f2-4e77-4020-9f0e-8c2ffdc390ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe9677175c9538bc070d2adea17a96351397d9a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809631"
---
# Problembehandlung bei der Bereitstellung


Dieses Thema enthält Informationen, die Sie bei der Behandlung von Bereitstellungsproblemen in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 unterstützen.

## Behandeln von Problemen bei der MED-V-Bereitstellung


Das folgende Problem kann auftreten, wenn Sie MED-V bereitstellen. Die Lösung hilft bei der Behebung dieses Problems.

**Probleme treten auf, wenn Sie nur MED-V für den aktuellen Benutzer installieren.** Med-v unterstützt nur die Installation des Med-v-Arbeitsbereichs Pakets, des Med-v-Host-Agents und des Med-v-Arbeitsbereichs für alle Benutzer. Die Installation für den aktuellen Benutzer verursacht nur Fehler bei der Installation der Komponenten und beim Einrichten des MED-V-Arbeitsbereichs.

**Lösung**

Verwenden Sie bei der Installation der MED-V-Komponenten niemals die Option **ALLUSERS = ""** .

**Für MED-V ist eine exklusive Verwendung des Virtualisierungs-Stacks erforderlich.** Auf einem Computer kann jeweils nur ein Virtualisierungs-Stack ausgeführt werden. Windows Virtual PC muss den virtuellen Stapel verwenden, und MED-V ist von Windows Virtual PC abhängig. Wenn Sie also versuchen, Med-v bereitzustellen oder zu verwenden, wenn andere Anwendungen ausgeführt werden, die den virtuellen Stapel verwenden, kann Med-v nicht ausgeführt oder erfolgreich installiert werden.

**Lösung**

Schließen Sie alle Anwendungen, die ausgeführt werden, die den Virtualisierungs-Stack verwenden, bevor Sie MED-V installieren oder ausführen.

**Verknüpfungen bleiben nach der Deinstallation erhalten.** Standardmäßig werden beim Deinstallieren von MED-V Verknüpfungen im **Startmenü** des Endbenutzers entfernt. In bestimmten Situationen wie beispielsweise für Endbenutzer, die Server gespeicherte Profile ausführen, bleiben Verknüpfungen zu den veröffentlichten MED-V-Anwendungen im **Startmenü** des Endbenutzers erhalten.

**Lösung**

Wenn Sie die restlichen Verknüpfungen im **Startmenü** manuell löschen möchten, klicken Sie mit der rechten Maustaste auf die Verknüpfungen, und klicken Sie dann auf **Entfernen**.

**Deaktivieren Sie die Gruppenrichtlinieneinstellung für Anmeldenachrichten im MED-V-Arbeitsbereich.** Wenn die Windows XP-Anmeldenachricht im Med-v-Arbeitsbereich aktiviert ist, muss sich der Endbenutzer jedes Mal anmelden, wenn er eine virtuelle Med-v-Anwendung öffnen möchte. Dadurch entsteht eine schlechte Benutzererfahrung.

**Lösung**

Deaktivieren Sie die folgenden Gruppenrichtlinieneinstellungen auf dem MED-V-virtuellen Computer:

**Interaktive Anmeldung: Nachricht für Benutzer, die sich anmelden wollen**

**Interaktive Anmeldung: Nachrichtentitel für Benutzer, die sich anmelden wollen**

## Verwandte Themen


[Problembehandlung bei Vorgängen](operations-troubleshooting-medv2.md)

 

 





