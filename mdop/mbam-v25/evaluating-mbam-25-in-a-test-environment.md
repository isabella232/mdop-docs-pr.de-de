---
title: Auswerten von MBAM 2.5 in einer Testumgebung
description: Auswerten von MBAM 2.5 in einer Testumgebung
author: dansimp
ms.assetid: 72959b7a-e55f-4797-91b3-5be23c8c2844
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d7ba8a62f5ddecf85fe56e04fc16a6bae374ba9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809784"
---
# Auswerten von MBAM 2.5 in einer Testumgebung


In diesem Thema wird beschrieben, wie Sie eine Testumgebung einrichten können, um die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 in der eigenständigen oder System Center Configuration Manager-Integrations Topologie auszuwerten.

## Auswerten von MBAM 2,5 mithilfe der eigenständigen Topologie


Zum Auswerten von MBAM mithilfe der eigenständigen Topologie verwenden Sie die Informationen in den folgenden Tabellen, um die MBAM-Server Software zu installieren, und konfigurieren Sie dann die MBAM-Server Features in Ihrer Testumgebung.

**So evaluieren Sie MBAM 2,5 mithilfe der eigenständigen Topologie**

1. Bevor Sie MBAM installieren, gehen Sie folgendermaßen vor:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Aufgabe</th>
   <th align="left">Wo erhalte ich Anweisungen?</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Stellen Sie sicher, dass Sie alle erforderlichen Software installiert haben.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Überprüfen Sie die erforderlichen Hardware-, RAM-und anderen Spezifikationen.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Von MBAM 2.5 unterstützte Konfigurationen</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Überprüfen Sie die Voraussetzungen für die Verwendung von Windows PowerShell, wenn Sie die Cmdlets zum Konfigurieren von MBAM verwenden möchten.</p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</a></p></td>
   </tr>
   </tbody>
   </table>



2. Installieren Sie die MBAM-Server Software, und konfigurieren Sie dann die gewünschten Features.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Aufgabe</th>
   <th align="left">Wo erhalte ich Anweisungen?</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren möchten.</p></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installieren der MBAM 2.5-Serversoftware</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Konfigurieren Sie die Datenbank für Compliance und Audit sowie die Wiederherstellungsdatenbank.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">So konfigurieren Sie die MBAM 2.5-Datenbanken</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Konfigurieren Sie das Feature Berichte.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">So konfigurieren Sie die MBAM 2.5-Berichte</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Konfigurieren Sie die Webanwendungen.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">So konfigurieren Sie die MBAM 2.5-Webanwendungen</a></p></td>
   </tr>
   </tbody>
   </table>



3. Gehen Sie auf einem Clientcomputer wie folgt vor:

   1.  Installieren Sie den MBAM-Client auf einem Clientcomputer.

   2.  Wenden Sie die MBAM-Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) auf den Computer an.

   3.  Legen Sie die folgenden Registrierungsschlüssel fest, um zu erzwingen, dass der MBAM-Client schneller und in regelmäßigen Abständen aktiviert wird:

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Hinweis:**  
       Da diese Tasten den MBAM-Client pro Minute reaktivieren, empfehlen wir, diese Registrierungsschlüsseleinstellungen nur in einer Testumgebung zu verwenden.



   4.  Starten Sie den **BitLocker-Verwaltungs Client Dienst**erneut.

## Auswerten von MBAM 2,5 mithilfe der Configuration Manager-Integrations Topologie von System Center 2012


Zum Auswerten von MBAM mithilfe der Configuration Manager-Integrations Topologie verwenden Sie die Informationen in den folgenden Tabellen, um die MBAM-Server Software zu installieren, und konfigurieren Sie dann die MBAM-Server Features in Ihrer Testumgebung. Nachdem Sie den MBAM-Client auf einem Clientcomputer installiert haben, führen Sie weitere Schritte durch, um zu erzwingen, dass der MBAM-Client den Status des Computers an MBAM schneller meldet.

**So evaluieren Sie MBAM 2,5 mithilfe der Configuration Manager-Integrations Topologie von System Center 2012**

1. Überprüfen Sie vor der Installation von MBAM die erforderliche Software und die unterstützte Konfiguration.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Aufgabe</th>
   <th align="left">Wo erhalte ich Anweisungen?</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Stellen Sie sicher, dass Sie alle erforderlichen Software installiert haben.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Überprüfen Sie die erforderlichen Hardware-, RAM-und anderen Spezifikationen.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Von MBAM 2.5 unterstützte Konfigurationen</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Überprüfen Sie die Voraussetzungen für die Verwendung von Windows PowerShell, wenn Sie die Cmdlets zum Konfigurieren von MBAM verwenden möchten.</p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Erstellen oder bearbeiten Sie die MOF-Dateien.</p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)">Bearbeiten der Datei „Configuration.mof“</a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)">Erstellen oder Bearbeiten der Datei „Sms_def.mof“</a></p></td>
   </tr>
   </tbody>
   </table>



2. Installieren Sie die MBAM-Server Software, und konfigurieren Sie dann die gewünschten Features.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Aufgabe</th>
   <th align="left">Wo erhalte ich Anweisungen?</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren möchten.</p>
   <div class="alert">
   <strong>Hinweis:</strong><br/><p>Sie können die Datenbanken auf einem SQL Server-Remotecomputer mit Windows PowerShell oder einem exportierten Data-tier Application (DAC)-Paket installieren. Weitere Informationen zu DAC-Paketen finden Sie unter <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> Datenebenen-Anwendungen </a> .</p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installieren der MBAM 2.5-Serversoftware</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Konfigurieren Sie die Datenbank für Compliance und Audit sowie die Wiederherstellungsdatenbank.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">So konfigurieren Sie die MBAM 2.5-Datenbanken</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Konfigurieren Sie das Feature Berichte.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">So konfigurieren Sie die MBAM 2.5-Berichte</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Konfigurieren Sie die Webanwendungen.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">So konfigurieren Sie die MBAM 2.5-Webanwendungen</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Konfigurieren Sie den System Center-Konfigurations-Manager, um die Configuration Manager-Objekte zu installieren.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">So konfigurieren Sie die Integration von MBAM 2.5 in System Center Configuration Manager</a></p></td>
   </tr>
   </tbody>
   </table>



3. Gehen Sie auf einem Clientcomputer wie folgt vor:

   1.  Installieren Sie den MBAM-Client und den Configuration Manager-Client auf einem Clientcomputer.

   2.  Wenden Sie die MBAM-Gruppenrichtlinienobjekte auf den Computer an.

   3.  Legen Sie die folgenden Registrierungsschlüssel fest, um zu erzwingen, dass der MBAM-Client schneller und in regelmäßigen Abständen aktiviert wird:

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Hinweis:**  
       Da diese Tasten den MBAM-Client pro Minute reaktivieren, empfehlen wir, diese Registrierungsschlüsseleinstellungen nur in einer Testumgebung zu verwenden.



   4.  Starten Sie den **BitLocker-Verwaltungs Client Dienst**erneut.

   5.  Öffnen Sie in der Systemsteuerung **Configuration Manager**, und klicken Sie dann auf die Registerkarte **Aktionen** .

   6.  Wählen Sie **Hardware Inventurzyklus**aus, und klicken Sie dann auf **jetzt ausführen**. Dieser Schritt führt die Hardwareinventur mithilfe der neuen Klassen aus, die Sie in Ihre MOF-Dateien importiert haben, und sendet die Daten dann an den Configuration Manager-Server.

   7.  Wählen Sie **Computerrichtlinienabruf & Evaluierungszyklus**aus, und klicken Sie dann auf **jetzt ausführen** , um die Gruppenrichtlinienobjekte anzuwenden, die für diesen Clientcomputer relevant sind.



4. Gehen Sie in der Configuration Manager-Konsole wie folgt vor:

   1.  Klicken Sie im Navigationsbereich mit der rechten Maustaste auf **MBAM unterstützte Computer**, klicken Sie auf **Mitgliedschaft aktualisieren**, und klicken Sie dann auf **Ja** , um den Clientcomputer zu zwingen, seine Mitgliedschaft sofort zu melden.

   2.  Klicken Sie im Navigationsbereich auf von **MBAM unterstützte Computer** , um zu überprüfen, ob der Clientcomputer in der Sammlung angezeigt wird.

5. Öffnen Sie **Configuration Manager** auf dem Clientcomputer in der Systemsteuerung erneut, und gehen Sie folgendermaßen vor:

   1.  Klicken Sie auf die Registerkarte **Aktionen** , und führen Sie dann den **Computerrichtlinienabruf & Evaluierungszyklus**erneut aus.

   2.  Klicken Sie auf die Registerkarte **Konfigurationen** , wählen Sie den BitLocker-Basisplan aus, und klicken Sie dann auf **bewerten**.

6. Überprüfen Sie in der Configuration Manager-Konsole, ob der Clientcomputer im Enterprise-Konformitätsbericht wie folgt angezeigt wird:

   1.  Wählen Sie im Navigationsbereich den Arbeitsbereich **Überwachung** aus.

   2.  Erweitern Sie in der Konsolenstruktur **Übersicht** &gt; **Bericht Erstellungs** &gt; **Berichte** &gt; **MBAM**.

   3.  Wählen Sie den Ordner aus, der die Sprache darstellt, in der Sie Berichte anzeigen möchten, und wählen Sie dann den Bericht im Bereich Ergebnisse aus.

## Auswerten von MBAM 2,5 mithilfe der System Center Configuration Manager 2007-Integrations Topologie


Wenn Sie MBAM mithilfe der Configuration Manager-Integrations Topologie auswerten möchten, führen Sie die gleichen Schritte aus, um MBAM in Ihrer Testumgebung während der Verwendung in einer Produktionsumgebung zu installieren und zu konfigurieren. Nachdem Sie den MBAM-Client auf einem Clientcomputer installiert haben, führen Sie die zusätzlichen Schritte in diesem Thema aus, um dem MBAM-Client zu ermöglichen, den Status des Computers an MBAM schneller zu melden.

**So evaluieren Sie MBAM mithilfe der Configuration Manager 2007-Integrations Topologie**

1. Bevor Sie MBAM installieren, gehen Sie folgendermaßen vor:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Aufgabe</th>
   <th align="left">Wo erhalte ich Anweisungen?</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Stellen Sie sicher, dass Sie alle erforderlichen Software installiert haben.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Überprüfen Sie die erforderlichen Hardware-, RAM-und anderen Spezifikationen.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Von MBAM 2.5 unterstützte Konfigurationen</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Erstellen oder bearbeiten Sie die MOF-Dateien.</p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)">Bearbeiten der Datei „Configuration.mof“</a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)">Erstellen oder Bearbeiten der Datei „Sms_def.mof“</a></p></td>
   </tr>
   </tbody>
   </table>



2. Installieren Sie die MBAM-Server Software, und konfigurieren Sie dann die gewünschten Features.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Aufgabe</th>
   <th align="left">Wo erhalte ich Anweisungen?</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren möchten.</p>
   <div class="alert">
   <strong>Hinweis:</strong><br/><p>Sie können die Datenbanken auf einem SQL Server-Remotecomputer mit Windows PowerShell oder einem exportierten Data-tier Application (DAC)-Paket installieren. Weitere Informationen zu DAC-Paketen finden Sie unter <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> Datenebenen-Anwendungen </a> .</p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installieren der MBAM 2.5-Serversoftware</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Konfigurieren Sie die Datenbank für Compliance und Audit sowie die Wiederherstellungsdatenbank.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">So konfigurieren Sie die MBAM 2.5-Datenbanken</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Konfigurieren Sie das Feature Berichte.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">So konfigurieren Sie die MBAM 2.5-Berichte</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Konfigurieren Sie die Webanwendungen.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">So konfigurieren Sie die MBAM 2.5-Webanwendungen</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Konfigurieren Sie den System Center-Konfigurations-Manager, um die Configuration Manager-Objekte zu installieren.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">So konfigurieren Sie die Integration von MBAM 2.5 in System Center Configuration Manager</a></p></td>
   </tr>
   </tbody>
   </table>



3. Gehen Sie auf einem Clientcomputer wie folgt vor:

   1.  Installieren Sie den MBAM-Client auf einem Clientcomputer.

   2.  Wenden Sie die MBAM-Gruppenrichtlinienobjekte auf den Computer an.

   3.  Setzen Sie die folgenden Registrierungsschlüssel, um zu erzwingen, dass der MBAM-Client schneller und in schnelleren Intervallen aufwacht:

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Hinweis:**  
       Da diese Tasten den MBAM-Client pro Minute reaktivieren, empfehlen wir, diese Registrierungsschlüsseleinstellungen nur in einer Evaluierungsumgebung zu verwenden.



   4.  Starten Sie den **BitLocker-Verwaltungs Client Dienst**erneut.

   5.  Öffnen Sie in der Systemsteuerung **Configuration Manager**, und klicken Sie dann auf die Registerkarte **Aktionen** .

   6.  Wählen Sie **Computerrichtlinienabruf & Evaluierungszyklus**aus, und klicken Sie dann auf **jetzt ausführen** , um die Gruppenrichtlinienobjekte anzuwenden, die für diesen Clientcomputer relevant sind.

   7.  Wählen Sie **Hardware Inventurzyklus**aus, und klicken Sie dann auf **jetzt ausführen**. Dieser Schritt führt die Hardwareinventur mithilfe der neuen Klassen aus, die Sie in Ihre MOF-Dateien importiert haben, und sendet die Daten dann an den Configuration Manager-Server.

4. Gehen Sie in der Configuration Manager-Konsole wie folgt vor:

   1.  Klicken Sie im Navigationsbereich mit der rechten Maustaste auf **MBAM unterstützte Computer**, klicken Sie auf **Mitgliedschaft aktualisieren**, und klicken Sie dann auf **Ja** , um den Clientcomputer zu zwingen, seine Mitgliedschaft sofort zu melden.

   2.  Klicken Sie im Navigationsbereich auf von **MBAM unterstützte Computer** , um zu überprüfen, ob der Clientcomputer in der Sammlung angezeigt wird.

5. Öffnen Sie **Configuration Manager** auf dem Clientcomputer in der Systemsteuerung erneut, und gehen Sie folgendermaßen vor:

   1.  Klicken Sie auf die Registerkarte **Aktionen** , und führen Sie dann den **Computerrichtlinienabruf & Evaluierungszyklus**erneut aus.

   2.  Klicken Sie auf die Registerkarte **Konfigurationen** , wählen Sie den BitLocker-Basisplan aus, und klicken Sie auf **bewerten**.

6. Überprüfen Sie in der Configuration Manager-Konsole, ob der Clientcomputer im Enterprise-Konformitätsbericht wie folgt angezeigt wird:

   1.  Erweitern Sie im Navigationsbereich **Computer Management** &gt; **Reporting** &gt; **Reporting Services** - &gt; ** &lt; Servername &gt; MBAM**.

   2.  Wählen Sie im Knoten **MBAM** den Ordner aus, der die Sprache darstellt, in der Sie Berichte anzeigen möchten, und wählen Sie dann den Bericht im Bereich Ergebnisse aus.


## Verwandte Themen


[Erste Schritte mit MBAM 2.5](getting-started-with-mbam-25.md)


## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).





