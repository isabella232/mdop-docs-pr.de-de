---
title: So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit
description: So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit
author: dansimp
ms.assetid: 8704bf33-535d-41da-b9b2-45b60754367e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a63311bcc93d84472ceff5c80c9222fefd5445c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810840"
---
# So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit


Der Client für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen. Der BitLocker-Client kann in eine Organisation integriert werden, indem die BitLocker-Verwaltung und-Verschlüsselung auf Client Computern während des Computer Imaging-und Windows-Bereitstellungsprozesses aktiviert wird.

**Hinweis:**  
Informationen zum Überprüfen der MBAM-Client Systemanforderungen finden Sie unter [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).



Die Verschlüsselung von Clientcomputern mit BitLocker während der anfänglichen Abbild Erstellungsphase einer Windows-Bereitstellung kann den Verwaltungsaufwand für die MBAM-Implementierung senken. Durch diesen Ansatz wird auch sichergestellt, dass alle bereitgestellten Computer bereits BitLocker ausführen und ordnungsgemäß konfiguriert sind.

**Warnung**  
In diesem Thema wird beschrieben, wie Sie die Windows-Registrierung mit dem Registrierungs-Editor ändern. Wenn Sie die Windows-Registrierung falsch ändern, können Sie zu schwerwiegenden Problemen führen, bei denen Sie möglicherweise eine Neuinstallation von Windows erforderlich machen. Bevor Sie die Registrierung ändern, sollten Sie eine Sicherungskopie der Registrierungsdateien (System. dat und User. dat) erstellen. Microsoft kann nicht garantieren, dass die Probleme, die beim Ändern der Registrierung auftreten, behoben werden können. Ändern Sie die Registrierung auf Ihr eigenes Risiko.



**So verschlüsseln Sie einen Computer als Teil der Windows-Bereitstellung**

1.  Wenn Ihre Organisation die Verwendung des TPM-Beschützers (Trusted Platform Module) oder der TPM + PIN Protector-Optionen in BitLocker plant, müssen Sie den TPM-Chip vor der anfänglichen Bereitstellung von MBAM aktivieren. Wenn Sie den TPM-Chip aktivieren, vermeiden Sie später einen Neustart des Prozesses, und Sie stellen sicher, dass die TPM-Chips entsprechend den Anforderungen Ihrer Organisation ordnungsgemäß konfiguriert sind. Sie müssen den TPM-Chip manuell im BIOS des Computers aktivieren. Weitere Informationen zum Konfigurieren des TPM-Chips finden Sie in der Herstellerdokumentation.

2.  Installieren Sie den MBAM-Client-Agent.

3.  Wir empfehlen, dass Sie den Computer einer Domäne hinzufügen...

    -   Wenn der Computer nicht zu einer Domäne gehört, wird das Wiederherstellungskennwort nicht im MBAM-Schlüssel Wiederherstellungs Dienst gespeichert. Standardmäßig lässt MBAM keine Verschlüsselung zu, es sei denn, der Wiederherstellungsschlüssel kann gespeichert werden.

    -   Wenn ein Computer im Wiederherstellungsmodus gestartet wird, bevor der Wiederherstellungsschlüssel auf dem MBAM-Server gespeichert wird, muss der Computer erneut abgespielt werden. Es steht keine Wiederherstellungsmethode zur Verfügung.

4.  Öffnen Sie eine Eingabeaufforderung als Administrator, beenden Sie den MBAM-Dienst, und setzen Sie den Dienst auf **manuell** oder **bei Bedarf**. Führen Sie dann die folgende Befehle aus:

    **NET STOP mbamagent**

    **SC config mbamagent Start = Demand**

5.  Festlegen der Registrierungseinstellungen für den MBAM-Agent zum Ignorieren von Gruppenrichtlinien und Ausführen der Verschlüsselung für das TPM nur für das **Betriebssystem** , um dies zu tun, führen Sie **Regedit**aus, und importieren Sie dann die Registrierungsschlüssel Vorlage aus c:\\Programme Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

6.  Wechseln Sie in regedit zu HKLM\\SOFTWARE\\Microsoft\\MBAM, und konfigurieren Sie die Einstellungen, die in der folgenden Tabelle aufgeführt sind.

    Registrierungseintrag

    Konfigurationseinstellungen

    Bereitstellung

    0 = aus

    1 = Verwenden von Bereitstellungszeit Richtlinieneinstellungen (Standard)

    UseKeyRecoveryService

    0 = Schlüssel Escrow nicht verwenden (die nächsten beiden Registrierungseinträge sind in diesem Fall nicht erforderlich.)

    1 = Verwenden des Schlüssels Escrow in Key Recovery System (Standard)

    Empfohlen: der Computer muss mit dem Schlüssel Wiederherstellungs Dienst kommunizieren können. Vergewissern Sie sich, dass der Computer mit dem Dienst kommunizieren kann, bevor Sie fortfahren.

    Keyrecoveryoptions

    0 = nur Wiederherstellungsschlüssel hochladen

    1 = Upload-Wiederherstellungsschlüssel und Schlüssel Wiederherstellungs Paket (Standard)

    KeyRecoveryServiceEndPoint

    Setzen Sie diesen Wert auf die URL für den Key Recovery Web Server.

    Beispiel: http:// &lt; Computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.



~~~
**Note**  
MBAM policy or registry values can be set here to override the previously set values.
~~~



7. Der MBAM-Agent startet das System während der MBAM-Clientbereitstellung neu. Wenn Sie für diesen Neustart bereit sind, führen Sie den folgenden Befehl an einer Eingabeaufforderung als Administrator aus:

   **NET Start mbamagent**

8. Wenn die Computer neu gestartet werden und das BIOS Sie auffordert, eine TPM-Änderung zu akzeptieren, übernehmen Sie die Änderung.

9. Starten Sie während des Windows-Client-Betriebssystem-Imaging-Prozesses den MBAM-Agentdienst neu, wenn Sie bereit sind, die Verschlüsselung zu starten. Öffnen Sie dann zum Einrichten von Start auf **automatisch**eine Eingabeaufforderung als Administrator, und führen Sie die folgenden Befehle aus:

   **SC config mbamagent Start = automatisch**

   **NET Start mbamagent**

10. Entfernen Sie die Registrierungswerte umgehen. Führen Sie dazu Regedit aus, navigieren Sie zum Registrierungseintrag HKLM\\SOFTWARE\\Microsoft, klicken Sie mit der rechten Maustaste auf den **MBAM** -Knoten, und klicken Sie dann auf **Löschen**.

## Verwandte Themen


[Bereitstellen des MBAM 1.0-Clients](deploying-the-mbam-10-client.md)









