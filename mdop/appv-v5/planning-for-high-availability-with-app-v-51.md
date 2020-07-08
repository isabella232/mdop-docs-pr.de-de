---
title: Planen hoher Verfügbarkeit mit App-V 5.1
description: Planen hoher Verfügbarkeit mit App-V 5.1
author: dansimp
ms.assetid: 1f190a0e-10ee-4fbe-a602-7e807e943033
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5c8e0e684051859a4caa2c4ef983c040295bc6d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805009"
---
# Planen hoher Verfügbarkeit mit App-V 5.1


Microsoft Application Virtualization (App-V) 5,1-Systemkonfigurationen können die Vorteile von Optionen nutzen, die einen hohen verfügbaren Service gewährleisten.

Verwenden Sie die Informationen in den folgenden Abschnitten, damit Sie die Optionen für die Bereitstellung von App-V 5,1 in einer hoch verfügbaren Konfiguration verstehen können.

-   [Unterstützung für Microsoft SQL Server-Clustering](#bkmk-sqlcluster)

-   [Unterstützung für den IIS-Netzwerklastenausgleich](#bkmk-iisloadbal)

-   [Unterstützung von Cluster-Dateiservern beim Ausführen von (SCS)-Modus](#bkmk-clusterscsmode)

-   [Unterstützung für die Microsoft SQL Server-Spiegelung](#bkmk-sqlmirroring)

-   [Unterstützung für Microsoft SQL Server immer aktiviert](#bkmk-sqlalwayson)

## <a href="" id="bkmk-sqlcluster"></a>Unterstützung für Microsoft SQL Server-Clustering


Sie können die App-V-Verwaltungsdatenbank und die Berichtsdatenbank auf Computern ausführen, auf denen Microsoft SQL Server-Cluster ausgeführt werden. Sie müssen die Datenbanken jedoch mithilfe von Skripts installieren.

Anweisungen hierzu finden Sie unter [Bereitstellen der App-V-Datenbanken mithilfe von SQL-Skripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).

## <a href="" id="bkmk-iisloadbal"></a>Unterstützung für den IIS-Netzwerklastenausgleich


Sie können den Internet Informationsdienste (IIS)-Netzwerklastenausgleich verwenden, um eine hoch verfügbare Umgebung für Computer zu konfigurieren, auf denen die App-V 5. x-Verwaltungs-, Veröffentlichungs-und Reporting Services ausgeführt werden, die über IIS bereitgestellt werden.

Weitere Informationen zum Konfigurieren von IIS und Netzwerklastenausgleich für Computer mit Windows Server-Betriebssystemen finden Sie im folgenden:

-   Enthält Informationen zum Konfigurieren von Internet Informationsdienste (IIS) 7,0.

    [Erreichen von hoher Verfügbarkeit und Skalierbarkeit – arr und NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)

-   Konfigurieren von Microsoft Windows Server

    [Netzwerklastenausgleich](https://go.microsoft.com/fwlink/?LinkId=316370) ( https://go.microsoft.com/fwlink/?LinkId=316370) .

    Diese Informationen gelten auch für IIS-Netzwerklastenausgleichs-Cluster in Windows Server2008, Windows Server2008R2 oder Windows Server2012.

    **Hinweis**  Die IIS-Netzwerklastenausgleich-Funktion in Windows Server2012 ist in der Regel identisch mit der in Windows Server2008R2. Einige Aufgabendetails werden jedoch in Windows Server2012 geändert. Informationen zu neuen Methoden für Aufgaben finden Sie unter [allgemeine Verwaltungsaufgaben und Navigation in Windows Server 2012 R2 Preview und Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) ( https://go.microsoft.com/fwlink/?LinkId=316371) .

     

## <a href="" id="bkmk-clusterscsmode"></a>Unterstützung von Cluster-Dateiservern beim Ausführen von (SCS)-Modus


Das Ausführen von App-V 5,1 im Share Content Store (SCS)-Modus mit gruppierten Dateiservern wird unterstützt.

Die folgenden Schritte können verwendet werden, um diese Konfiguration zu aktivieren:

-   Konfigurieren Sie App-V 5,1, um im Client-SCS-Modus ausgeführt zu werden. Weitere Informationen zum Konfigurieren des App-v 5,1 SCS-Modus finden Sie unter so wird es [gemacht: Installieren des App-v 5,1-Clients für den freigegebenen Inhaltsspeicher Modus](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md).

-   Konfigurieren Sie den im Microsoft Server2012-Skalierungsmodus und im Pre **2012** -Modus konfigurierten Dateiservercluster mit einem virtuellen San.

Die folgenden Schritte können verwendet werden, um die Konfiguration zu überprüfen:

1.  Fügen Sie ein Paket auf dem Veröffentlichungsserver hinzu. Weitere Informationen zum Hinzufügen eines Pakets finden Sie unter so wird es [gemacht: Hinzufügen oder Aktualisieren von Paketen mithilfe der Verwaltungskonsole](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md).

2.  Führen Sie eine Veröffentlichungsaktualisierung auf dem Computer durch, auf dem der App-V 5,1-Client ausgeführt wird, und öffnen Sie eine Anwendung.

3.  Wechseln Sie die Clusterknoten in der Mitte des Veröffentlichungs Aktualisierungs-und Mid-Streaming, um sicherzustellen, dass ein Failover ordnungsgemäß funktioniert.

Weitere Informationen zum Konfigurieren von Windows Server-Failoverclustern finden Sie im folgenden:

-   [Prüfliste: Erstellen eines gruppierten Dateiservers](https://go.microsoft.com/fwlink/?LinkId=316372) ( https://go.microsoft.com/fwlink/?LinkId=316372) .

-   [Verwenden freigegebener Clustervolumes in einem Windows Server 2012-Failovercluster](https://go.microsoft.com/fwlink/?LinkId=316373) ( https://go.microsoft.com/fwlink/?LinkId=316373) .

## <a href="" id="bkmk-sqlmirroring"></a>Unterstützung für die Microsoft SQL Server-Spiegelung


Bei Verwendung der Microsoft SQL Server-Spiegelung, bei der die APP-v 5,1-Verwaltungsserver Datenbank mithilfe von zwei SQL Server-Instanzen gespiegelt wird, wird für App-v 5,1-Verwaltungsserver Datenbanken unterstützt.

Weitere Informationen zum Konfigurieren der Microsoft SQL Server-Spiegelung finden Sie im folgenden:

-   [Vorgehensweise: Vorbereiten einer Spiegeldatenbank für die Spiegelung (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)

-   [Einrichten einer Datenbankspiegelungssitzung mithilfe der Windows-Authentifizierung (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)

Die folgenden Schritte können verwendet werden, um die Konfiguration zu überprüfen:

1.  Initiieren Sie eine Microsoft SQL Server-Spiegelungssitzung.

2.  Wählen Sie **Failover** aus, um eine neue Master-Microsoft SQL Server-Instanz festzulegen.

3.  Überprüfen Sie, ob der App-V 5,1-Verwaltungsserver nach dem Failover weiterhin wie erwartet funktioniert.

Die Verbindungszeichenfolge auf dem Verwaltungsserver kann geändert werden, um **Failover-Partner &lt; = &gt; Server2**einzubeziehen. Dies hilft nur, wenn das primäre auf der Spiegelung auf das sekundäre Failover und der Computer, auf dem der App-V 5,1-Client ausgeführt wird, eine neue Verbindung ausführt (sagen wir nach einem Neustart).

Führen Sie die folgenden Schritte aus, um die Verbindungszeichenfolge so zu ändern, dass Sie **Failover-Partner = &lt; &gt; Server2**umfasst:

**Wichtig**  In diesem Thema wird beschrieben, wie Sie die Windows-Registrierung mit dem Registrierungs-Editor ändern. Wenn Sie die Windows-Registrierung falsch ändern, können Sie zu schwerwiegenden Problemen führen, bei denen Sie möglicherweise eine Neuinstallation von Windows erforderlich machen. Bevor Sie die Registrierung ändern, sollten Sie eine Sicherungskopie der Registrierungsdateien (System. dat und User. dat) erstellen. Microsoft kann nicht garantieren, dass die Probleme, die beim Ändern der Registrierung auftreten, behoben werden können. Ändern Sie die Registrierung auf Ihr eigenes Risiko.

 

1.  Melden Sie sich beim Verwaltungsserver an, und öffnen Sie **Regedit**.

2.  Navigieren Sie zu **HKEY \ _LOCAL \ _MACHINE**  \\  **Software**  \\  **Microsoft**  \\  **AppV**  \\  **Server**  \\  **Managementservice**.

3.  Ändern Sie die **Verwaltung \ _SQL \ _CONNECTION \ _STRING** Wert mit dem **Failover-Partner = &lt; Server2 &gt; **.

4.  Starten Sie den Verwaltungsdienst mithilfe der IIS-Konsole erneut.

    **Hinweis**  Die Datenbankspiegelung befindet sich in der Liste der veralteten Datenbankmodul Features für Microsoft SQL Server2012 aufgrund der in Microsoft SQL Server 2012 verfügbaren **AlwaysOn** -Funktion.

     

Klicken Sie auf einen der folgenden Links, um weitere Informationen zu erhalten:

-   [Vorgehensweise: Vorbereiten einer Spiegeldatenbank für die Spiegelung (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) ( https://go.microsoft.com/fwlink/?LinkId=394235) .

-   [Vorgehensweise: Konfigurieren einer Datenbankspiegelungssitzung (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) ( https://go.microsoft.com/fwlink/?LinkId=394236) .

-   [Einrichten einer Datenbankspiegelungssitzung mithilfe der Windows-Authentifizierung (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) ( https://go.microsoft.com/fwlink/?LinkId=394237) .

-   [Veraltete Datenbankmodul Features in SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) ( https://go.microsoft.com/fwlink/?LinkId=394238) .

## <a href="" id="bkmk-sqlalwayson"></a>Unterstützung für Microsoft SQL Server immer für die Konfiguration


Die App-V 5,1-Verwaltungsserver-Datenbank unterstützt Bereitstellungen auf Computern, auf denen Microsoft SQL Server ausgeführt wird, mit der **Always on** -Konfiguration.






## Verwandte Themen


[Planen der Bereitstellung von App-V](planning-to-deploy-app-v51.md)

 

 





