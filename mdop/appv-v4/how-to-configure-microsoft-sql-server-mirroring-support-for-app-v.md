---
title: So konfigurieren Sie die Unterstützung von Microsoft SQL Server-Spiegelungen für App-V
description: So konfigurieren Sie die Unterstützung von Microsoft SQL Server-Spiegelungen für App-V
author: dansimp
ms.assetid: 6d069eb5-109f-460a-836a-de49473b7035
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fb572442cd12bb32fc9406de65f05a3bf061f946
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807304"
---
# So konfigurieren Sie die Unterstützung von Microsoft SQL Server-Spiegelungen für App-V


Mit dem folgenden Verfahren können Sie Ihre Microsoft Application Virtualization-Umgebung (App-V) für die Verwendung der Microsoft SQL Server-Datenbankspiegelung konfigurieren. Das Konfigurieren der Datenbankspiegelung kann bei Disaster Recovery-und Failover-Szenarien helfen. App-V 4,5 SP2 unterstützt alle Modi der Datenbankspiegelung, die derzeit für Microsoft SQL Server 2005 und SQL Server 2008 verfügbar sind.

**Hinweis:**  
Dieses Verfahren wurde für Administratoren geschrieben, die mit dem Einrichten und Konfigurieren von SQL Server-Datenbanken und der Datenbankspiegelung mit Microsoft SQL Server vertraut sind, und umfasst daher nur die spezifischen Konfigurationseinstellungen, die für App-V eindeutig sind.



**So konfigurieren Sie Ihre App-V-Umgebung für die Verwendung der Microsoft SQL Server-Datenbankspiegelung**

1.  Richten Sie die SQL Server-Datenbankspiegelung der App-V-Datenbank nach Ihren Standard Geschäftsmethoden für die Datenbankspiegelung ein. Verwenden Sie die folgenden Links, um allgemeine Informationen zum Implementieren der Microsoft SQL Server-Datenbankspiegelung zu erhalten:

    -   **Microsoft SQL 2005**–[Einrichten der Datenbankspiegelung](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)

    -   **Microsoft SQL 2008**–[Einrichten der Datenbankspiegelung](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)

    Darüber hinaus finden Sie Informationen zu bewährten Methoden unter [bewährte Methoden für die Datenbankspiegelung und Leistungsüberlegungen](https://go.microsoft.com/fwlink/?LinkId=190270) ( https://go.microsoft.com/fwlink/?LinkId=190270) .

2.  Überprüfen Sie nach der Einrichtung der Spiegelung, ob die App-V-Datenbank den Status **(Prinzipal, synchronisiert)** aufweist, und die gespiegelte Datenbank zeigt den Status **(gespiegelt, synchronisiert/wiederherstellen)**. Beheben Sie alle Spiegelungs Probleme, bevor Sie mit dem nächsten Schritt fortfahren. Weitere Informationen zum Überwachen des Status finden Sie unter über [Wachen des Spiegelungsstatus](https://go.microsoft.com/fwlink/?LinkId=190279) ( https://go.microsoft.com/fwlink/?LinkId=190279) .

3.  Erstellen Sie auf dem SQL Server-Computer, der die Spiegelung der APP-v-Datenbank hostet, die SQL Server-Anmeldung für das Netzwerkdienstkonto des App-v-Verwaltungsservers unter Verwendung des ** &lt; Domänen &gt; \\ &lt; ManagementServerHostName &gt; $ **des Kontonamens.

4.  Installieren Sie den Microsoft SQL Server Native Client auf dem App-v-Verwaltungs Server und auf dem Computer mit dem App-v-Verwaltungs-Webdienst, wenn Sie auf einem anderen Computer installiert sind. Wenn Sie beabsichtigen, zusätzliche App-V-Verwaltungsserver zum Lastenausgleich mit der gespiegelten SQL-Datenbank zu verbinden, müssen Sie auch den Microsoft SQL Server Native Client auf diesen Computern installieren. Sie können den Microsoft SQL Server Native Client von der [Microsoft SQL Server 2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=187479) -Seite im Microsoft Download Center herunterladen ( https://go.microsoft.com/fwlink/?LinkId=187479) .

5.  Überprüfen Sie den Registrierungsschlüssel **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlservername** , und stellen Sie sicher, dass er nur den Hostnamen des SQL-Servers enthält. Wenn Sie einen Instanznamen enthält, beispielsweise *serverhostname\\instancename*, muss der Instanzname entfernt werden.

    **Wichtig**  
    Der App-V-Verwaltungs Server verwendet die TCP/IP-Netzwerkbibliothek, um mit dem SQL Server zu kommunizieren, wenn die Datenbankspiegelung aktiviert ist, und daher können keine Instanznamen verwendet werden. Die Portnummern müssen stattdessen in den Registrierungsschlüsseln angegeben werden.



6.  Überprüfen Sie den Registrierungsschlüssel **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlserverport** , und stellen Sie sicher, dass er die Portnummer enthält, die für SQL auf dem SQL Server-Computer verwendet wird. Wenn Sie eine benannte Instanz verwenden, muss dieser Schlüsselwert auf den Port festgesetzt werden, der für die benannte Instanz verwendet wird.

7.  Erstellen Sie den Registrierungsschlüssel **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverservername** als reg \ _SZ, und legen Sie dann den Wert auf den Hostnamen des SQL-Servers fest, der die Spiegelung hostet.

8.  Erstellen Sie den Registrierungsschlüssel **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverserverport** als DWORD, und legen Sie dann den Wert auf die Portnummer fest, die für SQL auf dem Computer verwendet wird, auf dem SQL Server ausgeführt wird, um die Spiegelung zu hosten. Wenn Sie eine benannte Instanz für die Spiegelung verwenden, muss dieser Schlüsselwert auf die Portnummer festgesetzt werden, die für die benannte Instanz verwendet wird.

9.  Konfigurieren Sie auf dem Computer, auf dem der App-V Management Web Service ausgeführt wird, die UDL-Textdatei (Universal Data Link). Doppelklicken Sie in dem Verzeichnis, in dem App-V installiert ist, auf **SftMgmt. udl** , und geben Sie die folgenden Werte an:

    -   Wählen Sie auf der Registerkarte **Anbieter** den OLE DB-Anbieter **SQL Server Native Client 10,0**aus.

    -   Klicken Sie auf **weiter** , um die Registerkarte **Verbindung** auszuwählen. Geben Sie im Feld **Servername** den Servernamen des SQL-Servers ein. Wählen Sie als nächstes **Windows NT Integrated Security verwenden**aus. Klicken Sie abschließend auf die Liste **Wählen Sie die Datenbank aus**, und wählen Sie dann den Namen der App-V-Datenbank aus.

    -   Klicken Sie auf die Registerkarte **alle** , und wählen Sie dann den Eintrag **Failover-Partner**aus. Klicken Sie auf **Wert bearbeiten**, und geben Sie dann den Servernamen des SQL Server-Failovers ein. Klicken Sie auf **OK**.

    **Wichtig**  
    Das App-V-System verwendet die Kerberos-Authentifizierung. Wenn Sie die SQL-Spiegelung so konfigurieren, dass die Kerberos-Authentifizierung auf dem SQL Server aktiviert ist und der SQL Server-Dienst unter einem Domänenbenutzerkonto ausgeführt wird, müssen Sie einen SPN manuell konfigurieren. Weitere Informationen finden Sie unter "Wenn der SQL-Dienstdomänen basiertes Konto verwendet" im Artikel [Konfigurieren der App-V-Verwaltung für eine verteilte Umgebung](https://go.microsoft.com/fwlink/?LinkId=203186) ( https://go.microsoft.com/fwlink/?LinkId=203186) .



10. Um zu überprüfen, ob die Datenbankspiegelung ordnungsgemäß ausgeführt wird, testen Sie das Failover, und vergewissern Sie sich, dass der App-V-Verwaltungs Server weiterhin ordnungsgemäß funktioniert.

    **Wichtig**  
    Gehen Sie mit Bedacht vor, und befolgen Sie Ihre standardmäßigen Geschäftsmethoden, um sicherzustellen, dass die Systemvorgänge bei einem Fehler nicht gestört werden.



~~~
After the failover has occurred successfully, as verified by using the SQL Server status monitoring information, right-click the **Applications** node in the App-V Management Console, and then select **Refresh**. The list of applications should display normally if the system is working correctly.
~~~

## Verwandte Themen


[So führen Sie Verwaltungsaufgaben in der Application Virtualization Server Management Console durch](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)









