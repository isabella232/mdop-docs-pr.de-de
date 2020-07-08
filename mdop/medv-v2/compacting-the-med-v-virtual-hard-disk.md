---
title: Komprimieren der virtuellen MED-V-Festplatte
description: Komprimieren der virtuellen MED-V-Festplatte
author: dansimp
ms.assetid: 5e6122d1-9847-4b33-adab-594919eec3c5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f71aefb1e4e901078b4d0a421065b7bd5acdf0ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809859"
---
# Komprimieren der virtuellen MED-V-Festplatte


Obwohl es optional ist, können Sie die virtuelle Festplatte (VHD) komprimieren, um leeren Speicherplatz freizugeben und die Größe der VHD zu verringern, bevor Sie das Windows Virtual PC-Abbild konfigurieren.

**Wichtig**  Bevor Sie fortfahren, erstellen Sie eine Sicherungskopie Ihres Windows XP-Abbilds.

 

**Vorbereiten der virtuellen Festplatte**

1.  Öffnen Sie Ihr Windows XP-Abbild.

    Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Windows Virtual PC**, klicken Sie auf **Windows Virtual PC**, und doppelklicken Sie dann auf Ihr Windows XP-Abbild.

2.  Löschen Sie den dll-Cache.

    1.  Geben Sie an einer Eingabeaufforderung auf dem virtuellen Computer **sfc/CacheSize = 1**ein.

    2.  Starten Sie den virtuellen Computer neu.

    3.  Geben Sie an einer Eingabeaufforderung auf dem virtuellen Computer **sfc/PURGECACHE**.

3.  Löschen Sie nicht benötigte Dateien wie Deinstallationsprogramme, temporäre Dateien, Protokolldateien, Seiten Dateien, freigegebene Ordner usw.

4.  Deaktivieren Sie die System Wiederherstellung. Sie können diesen Schritt auch in der Datei "Sysprep. inf" angeben.

    1.  Doppelklicken **Sie in der Systemsteuerung auf** **System**, und wählen Sie dann die Registerkarte **Systemwiederherstellung** aus.

    2.  Wählen Sie **System Wiederherstellung deaktivieren**aus, und klicken Sie dann auf **OK**.

5.  Setzen Sie die maximale Größe des Ereignisprotokolls, und löschen Sie alle Ereignisse.

    1.  Öffnen Sie die Ereignisanzeige.

        Klicken Sie auf **Start**, klicken Sie auf **System**Steuerung, doppelklicken Sie auf **Verwaltung**, und doppelklicken Sie dann auf **Ereignisanzeige**.

    2.  Klicken Sie mit der rechten Maustaste auf **Anwendung**, und klicken Sie auf **Eigenschaften**.

    3.  Legen Sie im Bereich **Log Size** die **Maximale Protokollgröße** auf 512 KB und wählen Sie dann **Ereignisse nach Bedarf überschreiben**aus.

    4.  Klicken Sie auf **Protokoll löschen**. Klicken Sie im daraufhin angezeigten Dialogfeld **Ereignisanzeige** auf **Nein**.

    5.  Klicken Sie im **Eigenschaften** Fenster auf **OK**.

    6.  Wiederholen Sie die Schritte a bis e für die **Sicherheits** -und **System** Protokolle.

6.  Führen Sie das Tool Datenträgerbereinigung aus.

    Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Zubehör**, klicken Sie auf **System Tools**, und klicken Sie dann auf **Datenträgerbereinigung**.

7.  Konfigurieren Sie Ihre Seitendatei nach Bedarf für Ihre Anwendungen.

    1.  Doppelklicken **Sie in der Systemsteuerung auf** **System**, und wählen Sie dann die Registerkarte **erweitert** aus.

    2.  Klicken Sie im Bereich " **Leistung** " auf " **Einstellungen**".

    3.  Klicken Sie im Bereich **virtueller Speicher** auf **ändern**.

    4.  Konfigurieren Sie Ihre Seitendatei Einstellungen.

8.  Fahren Sie das Windows XP-Abbild herunter.

**Defragmentieren und vorkomprimieren der virtuellen Festplatte**

1.  Klicken Sie in der **System** Steuerung auf dem Hostcomputer unter Windows 7 auf **Verwaltungs Tools**, doppelklicken Sie auf **Computerverwaltung**, und klicken Sie dann auf **Datenträgerverwaltung**.

2.  Wenn Sie die Datenträger-Verwaltungskonsole verwenden, fügen Sie die virtuelle Festplatte an (mounten), und Defragmentieren Sie die Festplatte.

3.  Extrahieren Sie mithilfe eines ISO-Extraktionstools die Datei "precompact. ISO", die sich im Ordner \\Program Files\\Windows Virtual PC\\Integration Components befindet.

4.  Verwenden Sie das precompact.exe-Programm, um die virtuelle Windows XP-Festplatte zu komprimieren.

5.  Trennen Sie die virtuelle Festplatte mithilfe der Datenträgerverwaltungskonsole.

**Komprimieren der virtuellen Festplatte**

1.  Öffnen Sie Windows Virtual PC.

    Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Windows Virtual PC**, und klicken Sie dann auf **Windows Virtual PC**.

2.  Klicken Sie mit der rechten Maustaste auf Ihr Windows XP-Bild, und wählen Sie **Einstellungen**aus.

3.  Klicken Sie auf die **Festplatte** für diejenige, die Ihrem Windows XP-Abbild entspricht, und klicken Sie dann auf **ändern**.

4.  Klicken Sie auf **virtuelle Festplatte komprimieren**.

5.  Klicken Sie auf **komprimieren** , und klicken Sie dann auf **OK**.

Erstellen Sie eine Sicherungskopie Ihrer komprimierten virtuellen Festplatte.

## Verwandte Themen


[Konfigurieren eines virtuellen Windows-PC-Images für MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md)

[Technische Referenz für MED-V](technical-reference-for-med-v.md)

 

 





