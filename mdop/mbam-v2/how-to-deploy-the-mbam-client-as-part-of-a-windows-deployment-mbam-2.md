---
title: So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit
description: So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit
author: dansimp
ms.assetid: 67387de7-8b02-4412-9850-3b8d8e5c18af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d75e5748167d2d4866f98e9d3611584067ecd418
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810666"
---
# So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit


Der Client für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen. Wenn Computer, die über einen TPM-Chip (Trusted Platform Module) verfügen, kann der BitLocker-Client in eine Organisation integriert werden, indem die BitLocker-Verwaltung und-Verschlüsselung auf Clientcomputern im Rahmen des Imaging-und Windows-Bereitstellungsprozesses aktiviert wird.

**Hinweis:**  
Informationen zum Überprüfen der Systemanforderungen für die Microsoft BitLocker-Verwaltung und-Überwachung finden Sie unter [unterstützte MBAM 2,0-Konfigurationen](mbam-20-supported-configurations-mbam-2.md).



Das Verschlüsseln von Clientcomputern mit BitLocker während der anfänglichen Abbild Erstellungsphase einer Windows-Bereitstellung kann den administrativen Overhead verringern, der für die Implementierung von MBAM in einer Organisation erforderlich ist. Außerdem wird sichergestellt, dass auf jedem bereitgestellten Computer bereits BitLocker ausgeführt wird und ordnungsgemäß konfiguriert ist.

**Hinweis:**  
Das Verfahren in diesem Thema beschreibt das Ändern der Windows-Registrierung. Wenn Sie den Registrierungs-Editor falsch verwenden, kann dies zu schwerwiegenden Problemen führen, die eine Neuinstallation von Windows erforderlich machen. Microsoft kann nicht garantieren, dass Probleme, die sich aus der fehlerhaften Verwendung des Registrierungs-Editors ergeben, behoben werden können. Verwenden Sie den Registrierungs-Editor auf eigenes Risiko.



**So verschlüsseln Sie einen Computer als Teil der Windows-Bereitstellung**

1.  Wenn Ihre Organisation die Verwendung des TPM-Beschützers (Trusted Platform Module) oder der TPM + PIN Protector-Optionen in BitLocker plant, müssen Sie den TPM-Chip vor der anfänglichen Bereitstellung von MBAM aktivieren. Wenn Sie den TPM-Chip aktivieren, vermeiden Sie später einen Neustart des Prozesses, und Sie stellen sicher, dass die TPM-Chips entsprechend den Anforderungen Ihrer Organisation ordnungsgemäß konfiguriert sind. Sie müssen den TPM-Chip manuell im BIOS des Computers aktivieren.

    **Hinweis:**  
    Einige Anbieter stellen Tools bereit, mit denen Sie den TPM-Chip im BIOS innerhalb des Betriebssystems aktivieren und aktivieren können. Weitere Informationen zum Konfigurieren des TPM-Chips finden Sie in der Herstellerdokumentation.



2.  Installieren Sie den Client-Agent für Microsoft BitLocker-Verwaltung und-Überwachung.

3.  Verbinden Sie den Computer mit einer Domäne (empfohlen).

    -   Wenn der Computer nicht der Domäne beigetreten ist, wird das Wiederherstellungskennwort nicht im MBAM-Schlüssel Wiederherstellungs Dienst gespeichert. Standardmäßig lässt MBAM keine Verschlüsselung zu, es sei denn, der Wiederherstellungsschlüssel kann gespeichert werden.

    -   Wenn ein Computer im Wiederherstellungsmodus gestartet wird, bevor der Wiederherstellungsschlüssel auf dem MBAM-Server gespeichert wird, muss der Computer erneut abgespielt werden. Es steht keine Wiederherstellungsmethode zur Verfügung.

4.  Führen Sie die Eingabeaufforderung als Administrator aus, beenden Sie den MBAM-Dienst, und legen Sie den Dienst auf **manuell** oder **bei Bedarf**, und beginnen Sie dann mit der Eingabe der folgenden Befehle:

    **NET STOP mbamagent**

    **SC config mbamagent Start = Demand**

5.  Festlegen der Registrierungseinstellungen für den MBAM-Agent, um Gruppenrichtlinien zu ignorieren und das TPM nur für das **Betriebssystem zu verschlüsseln** , indem Sie **Regedit**ausführen und dann die Registrierungsschlüssel Vorlage aus c:\\Programme Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg. importieren

6.  Wechseln Sie in regedit zu HKLM\\SOFTWARE\\Microsoft\\MBAM, und konfigurieren Sie die Einstellungen, die in der folgenden Tabelle aufgeführt sind.

    Registrierungseintrag

    Konfigurationseinstellungen

    Bereitstellung

    0 = aus

    1 = Verwenden von Bereitstellungszeit Richtlinieneinstellungen (Standard)

    UseKeyRecoveryService

    0 = Schlüssel Escrow nicht verwenden (die nächsten beiden Registrierungseinträge sind in diesem Fall nicht erforderlich)

    1 = Verwenden des Schlüssels Escrow in Key Recovery System (Standard)

    Empfohlen: der Computer muss mit dem Schlüssel Wiederherstellungs Dienst kommunizieren können. Vergewissern Sie sich, dass der Computer mit dem Dienst kommunizieren kann, bevor Sie fortfahren.

    Keyrecoveryoptions

    0 = nur Uploads des Wiederherstellungsschlüssels

    1 = Uploads-Wiederherstellungsschlüssel und Schlüssel Wiederherstellungs Paket (Standard)

    KeyRecoveryServiceEndPoint

    Setzen Sie diesen Wert auf die URL für den Key Recovery Web Server, beispielsweise http:// &lt; Computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.



~~~
**Note**  
MBAM policy or registry values can be set here to override previously set values.
~~~



7. Der MBAM-Agent startet das System während der MBAM-Clientbereitstellung neu. Wenn Sie für diesen Neustart bereit sind, führen Sie den folgenden Befehl an einer Eingabeaufforderung als Administrator aus:

   **NET Start mbamagent**

8. Wenn die Computer neu gestartet werden und das BIOS Sie auffordert, eine TPM-Änderung zu akzeptieren, übernehmen Sie die Änderung.

9. Wenn Sie während des Windows-Client-Betriebssystem-Imaging-Prozesses die Verschlüsselung starten möchten, starten Sie den MBAM-Agent-Dienst neu, und legen Sie Start to **Automatic** ab, indem Sie eine Eingabeaufforderung als Administrator ausführen und die folgenden Befehle eingeben:

   **SC config mbamagent Start = automatisch**

   **NET Start mbamagent**

10. Entfernen Sie die Registrierungswerte umgehen, indem Sie regedit ausführen, und wechseln Sie zum Registrierungseintrag HKLM\\SOFTWARE\\Microsoft. Um den **MBAM** -Knoten zu löschen, klicken Sie mit der rechten Maustaste auf den Knoten, und klicken Sie auf **Löschen**.

## Verwandte Themen


[Bereitstellen des MBAM 2.0-Clients](deploying-the-mbam-20-client-mbam-2.md)









