---
title: Planen der Clientbereitstellung für MBAM 2.5
description: Planen der Clientbereitstellung für MBAM 2.5
author: dansimp
ms.assetid: 23c89976-af24-4753-9412-ce0ea42d1964
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ff03b58da0985b2f57308c99a9bc15f4a0554623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811488"
---
# Planen der Clientbereitstellung für MBAM 2.5


Je nachdem, wann Sie die Microsoft BitLocker-Verwaltungs-und Überwachungs-Client Software (MBAM) bereitstellen, können Sie die BitLocker-Laufwerkverschlüsselung auf einem Computer in Ihrer Organisation aktivieren, bevor der Endbenutzer den Computer oder anschließend empfängt. Für die MBAM eigenständige und die System Center Configuration Manager-Integrations Topologien müssen Sie die Gruppenrichtlinieneinstellungen für MBAM konfigurieren.

Wenn Sie die eigenständige MBAM-Topologie verwenden, empfiehlt es sich, ein Enterprise-Software Bereitstellungssystem zu verwenden, um die MBAM-Client Software auf Endbenutzercomputern bereitzustellen.

Wenn Sie MBAM mit der Configuration Manager-Integrations Topologie bereitstellen, können Sie mithilfe von Configuration Manager die MBAM-Client Software auf Endbenutzercomputern bereitstellen. In Configuration Manager erstellt die MBAM-Installation eine Sammlung von Computern, die von MBAM verwaltet werden können. Diese Sammlung umfasst Workstations und Geräte, die nicht über ein Trusted Platform Module (TPM) verfügen, aber unter Windows 8, Windows 8,1 oder Windows 10 ausgeführt werden.

**Hinweis**  Windows to go wird bei der Installation der Configuration Manager-Integrations Topologie nicht unterstützt, wenn Sie Configuration Manager 2007 verwenden.

 

## Bereitstellen des MBAM-Clients zum Aktivieren der BitLocker-Laufwerkverschlüsselung nach der Computer Verteilung an Endbenutzer


Nachdem Sie die Gruppenrichtlinie konfiguriert haben, können Sie ein Produkt des Enterprise-Software Bereitstellungssystems wie Microsoft System Center Configuration Manager oder Active Directory-Domänendienste (AD DS) verwenden, um die Windows Installer-Dateien der MBAM-Client Installation auf Zielcomputern bereitzustellen. Zum Bereitstellen des MBAM-Clients können Sie entweder die 32-oder 64-Bit-MbamClientSetup.exe Dateien oder MBAMClient.msi Dateien verwenden, die mit der MBAM-Client Software bereitgestellt werden.

**Hinweis**  Ab MBAM 2,5 SP1 ist eine separate MSI-Version nicht mehr im MBAM-Produkt enthalten. Sie können die MSI-Datei jedoch aus der ausführbaren Datei (. exe) extrahieren, die im Lieferumfang des Produkts enthalten ist.

 

Wenn Sie den MBAM-Client nach dem Verteilen von Computern an Client Computer bereitstellen, werden Endbenutzer aufgefordert, Ihren Computer zu verschlüsseln. Diese Aktion ermöglicht es MBAM, die Daten zu sammeln, einschließlich der PIN und des Kennworts (bei Bedarf nach Richtlinie), und dann den Verschlüsselungsprozess zu starten.

**Hinweis**  Bei dieser Vorgehensweise werden Endbenutzer, die über Computer mit einem TPM-Chip verfügen, aufgefordert, den TPM-Chip zu aktivieren und zu initialisieren, wenn der Chip zuvor nicht aktiviert wurde.

 

## Verwenden des MBAM-Clients zum Aktivieren der BitLocker-Laufwerkverschlüsselung vor der Computer Verteilung an Endbenutzer


In Organisationen, in denen Computer zentral empfangen und konfiguriert werden und Computer über einen kompatiblen TPM-Chip verfügen, können Sie den MBAM-Client verwenden, um die BitLocker-Laufwerkverschlüsselung auf jedem Computer zu verwalten, bevor Benutzerdaten darin geschrieben werden. Der Vorteil dieses Prozesses liegt darin, dass jeder Computer dann kompatibel ist. Diese Methode ist nicht auf Endbenutzeraktionen angewiesen, da der Administrator den Computer bereits verschlüsselt hat. Eine wichtige Voraussetzung für dieses Szenario ist, dass die Richtlinie des Unternehmens ein Windows-Abbild des Unternehmens installiert, bevor der Computer an den Endbenutzer übermittelt wird.

Wenn Ihre Organisation den TPM-Chip zum Verschlüsseln von Computern verwenden möchte, fügt der Administrator die TPM-Beschützer hinzu, um das Betriebssystem Volumen des Computers zu verschlüsseln. Wenn Ihre Organisation den TPM-Chip und eine PIN-Schutzkomponente verwenden möchte, verschlüsselt der Administrator das Betriebssystemvolume mit dem TPM-Schutz, und dann wählen Endbenutzer eine PIN aus, wenn Sie sich zum ersten Mal anmelden. Wenn Ihre Organisation entscheidet, nur die PIN-Beschützer zu verwenden, muss der Administrator das Volume nicht zuerst verschlüsseln. Wenn sich die Endbenutzer anmelden, werden Sie von der Microsoft BitLocker-Verwaltung und-Überwachung aufgefordert, eine PIN oder eine PIN und ein Kennwort anzugeben, die bei einem späteren Neustart des Computers verwendet werden sollen.

**Hinweis**  Die TPM-Schutzoption setzt voraus, dass der Administrator die BIOS-Eingabeaufforderung akzeptiert, um das TPM zu aktivieren und zu initialisieren, bevor der Computer an den Endbenutzer übermittelt wird.

 

## MBAM-Client Unterstützung für verschlüsselte Festplatten


MBAM unterstützt BitLocker auf verschlüsselten Festplatten, die die TCG-Spezifikationsanforderungen für Opal-und IEEE-1667-Standards erfüllen. Wenn BitLocker auf diesen Geräten aktiviert ist, generiert es Schlüssel und führt Verwaltungsfunktionen auf dem verschlüsselten Laufwerk aus. Weitere Informationen finden Sie unter [verschlüsselte Festplatte](https://technet.microsoft.com/library/hh831627.aspx) .


## Verwandte Themen


[Planen der Bereitstellung von MBAM 2.5](planning-to-deploy-mbam-25.md)

[Bereitstellen des MBAM 2.5-Clients](deploying-the-mbam-25-client.md)

 

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




