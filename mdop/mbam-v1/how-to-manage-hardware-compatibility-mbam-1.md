---
title: So verwalten Sie Hardwarekompatibilität
description: So verwalten Sie Hardwarekompatibilität
author: dansimp
ms.assetid: c74b96b9-8161-49bc-b5bb-4838734e7df5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf9e2c5b2b33ea93d9834a81700bd2be8a9b9757
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804637"
---
# So verwalten Sie Hardwarekompatibilität


Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) kann Informationen zum Hersteller und Modell von Clientcomputern sammeln, nachdem Sie die Gruppenrichtlinie Hardware Kompatibilitätsüberprüfung zulassen bereitgestellt haben. Wenn Sie diese Richtlinie konfigurieren, meldet der MBAM-Agent dem MBAM-Server die Informationen zum Erstellen und modellieren des Computers, wenn der MBAM-Client auf einem Clientcomputer bereitgestellt wird.

Das Hardware Kompatibilitätsfeature ist hilfreich, wenn Ihre Organisation über ältere Computer Hardware oder Computer verfügt, die TPM-Chips (Trusted Platform Module) nicht unterstützen. In diesen Fällen können Sie das Hardware Kompatibilitätsfeature verwenden, um sicherzustellen, dass die BitLocker-Verschlüsselung nur auf Computermodelle angewendet wird, die Sie unterstützen. Wenn alle Computer in Ihrer Organisation BitLocker unterstützen, müssen Sie das Hardware Kompatibilitätsfeature nicht verwenden.

**Hinweis**  Standardmäßig ist das MBAM-Hardware Kompatibilitätsfeature nicht aktiviert. Um Sie zu aktivieren, wählen Sie das **Hardware Kompatibilitäts** Feature während der Installation unter dem **Server Feature Verwaltung und Überwachung** aus. Weitere Informationen zum Einrichten und Konfigurieren der Hardware Kompatibilität finden Sie unter [Bereitstellen der MBAM 1,0-Server Infrastruktur](deploying-the-mbam-10-server-infrastructure.md).

 

Das Hardware Kompatibilitätsfeature funktioniert wie folgt:

****

1.  Der MBAM-Client-Agent ermittelt grundlegende Computer Informationen wie Hersteller, Modell, BIOS Maker, BIOS-Version, TPM-Hersteller und TPM-Version und übergibt diese Informationen an den MBAM-Server.

2.  Der MBAM-Server generiert eine Liste der Clientcomputer Marken und-Modelle, mit denen Sie zwischen denjenigen unterscheiden können, die BitLocker unterstützen können.

3.  Die im Unternehmen bereitgestellten MBAM-Client-Agents aktualisieren diese Liste automatisch mit allen neuen Computermarken und-Modellen, die mit einem **unbekannten**Zustand gefunden werden. Ein Administrator kann dann die MBAM-Verwaltungswebsite zum Ändern von Listeneinträgen verwenden, um einen bestimmten Computer als **kompatibel** oder **inkompatibel**festzulegen.

4.  Bevor der MBAM-Client-Agent mit der Verschlüsselung eines Laufwerks beginnt, überprüft der Agent zuerst die BitLocker-Verschlüsselungs Kompatibilität der Hardware, auf der er ausgeführt wird.

    -   Wenn die Hardware als kompatibel markiert ist, wird der BitLocker-Verschlüsselungsprozess gestartet. MBAM wird auch den Hardware Kompatibilitätsstatus des Computers einmal pro Tag erneut überprüfen.

    -   Wenn die Hardware als nicht kompatibel gekennzeichnet ist, protokolliert der Agent ein Ereignis und übergibt den Status "Hardware ausgenommen" als Teil der Konformitäts Berichterstattung. Der Agent überprüft alle sieben Tage, ob der Status in "kompatibel" geändert wurde.

    -   Wenn die Hardware als unbekannt markiert ist, wird der BitLocker-Verschlüsselungsprozess nicht gestartet. Der MBAM-Client-Agent überprüft den Hardware Kompatibilitätsstatus des Computers einmal pro Tag erneut.

**Warnung**  Wenn der MBAM-Client-Agent versucht, einen Computer zu verschlüsseln, der die BitLocker-Laufwerkverschlüsselung nicht unterstützt, besteht die Möglichkeit, dass der Computer beschädigt wird. Stellen Sie sicher, dass das Hardware Kompatibilitätsfeature richtig konfiguriert ist, wenn Ihre Organisation über eine ältere Hardware verfügt, die BitLocker nicht unterstützt.

 

**So verwalten Sie die Hardwarekompatibilität**

1.  Öffnen Sie einen Webbrowser, und navigieren Sie zur Website Microsoft BitLocker-Verwaltung und-Überwachung. Wählen Sie in der linken Menüleiste **Hardware** aus.

2.  Klicken Sie im rechten Bereich auf **Erweiterte Suche**und dann auf Filtern, um eine Liste aller Computermodelle anzuzeigen, die einen **Funktions** Status **unbekannt**aufweisen. Eine Liste der Computermodelle, die den Suchkriterien entsprechen, wird angezeigt. Administratoren können auf dieser Seite neue Computertypen hinzufügen, bearbeiten oder entfernen.

3.  Überprüfen Sie jede unbekannte Hardwarekonfiguration, um zu ermitteln, ob die Konfiguration auf **kompatibel** oder nicht **kompatibel**festgelegt werden soll.

4.  Wählen Sie eine oder mehrere Zeilen aus, und klicken Sie dann entweder auf **kompatibel festlegen** oder auf nicht **kompatibel** festlegen, um die BitLocker-Kompatibilität entsprechend den ausgewählten Computermodellen zu definieren. Wenn Sie auf **kompatibel**festzulegen, versucht BitLocker, die Richtlinien für die Laufwerkverschlüsselung auf Computern zu erzwingen, die dem unterstützten Modell entsprechen. Wenn Sie auf **inkompatibel**festzulegen, wird von BitLocker keine Laufwerk Verschlüsselungsrichtlinie auf diesen Computern erzwungen.

    **Hinweis**  Nachdem Sie ein Computermodell als kompatibel festgesetzt haben, kann es mehr als vierundzwanzig Stunden dauern, bis der MBAM-Client die BitLocker-Verschlüsselung auf den Computern beginnt, die diesem Hardwaremodell entsprechen.

     

5.  Administratoren sollten die Hardwarekompatibilitätsliste regelmäßig überwachen, um neue Modelle zu überprüfen, die vom MBAM-Agent erkannt werden, und dann Ihre Kompatibilitätseinstellung auf **kompatibel** oder **inkompatibel** aktualisieren.

## Verwandte Themen


[Verwalten von MBAM 1.0-Funktionen](administering-mbam-10-features.md)

 

 





