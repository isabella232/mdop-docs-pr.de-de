---
title: Planen der Clientbereitstellung für MBAM 2.0
description: Planen der Clientbereitstellung für MBAM 2.0
author: dansimp
ms.assetid: 3a92cf29-092f-4cad-bdfa-d5f6aafe554b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c3a7383188d4064247d8e493c8e6125fc24a1d2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804364"
---
# Planen der Clientbereitstellung für MBAM 2.0


Je nachdem, wann Sie den Microsoft BitLocker-Verwaltungs-und-Überwachungs Client (MBAM) bereitstellen, können Sie die BitLocker-Laufwerkverschlüsselung auf einem Computer in Ihrer Organisation aktivieren, bevor der Endbenutzer den Computer oder anschließend empfängt. Sowohl für die eigenständige MBAM als auch für die Configuration Manager-Topologien müssen Sie die Gruppenrichtlinieneinstellungen für MBAM konfigurieren.

Wenn Sie die eigenständige MBAM-Topologie verwenden, empfiehlt es sich, ein Enterprise-Software Bereitstellungssystem zu verwenden, um die MBAM-Client Software auf Endbenutzercomputern bereitzustellen.

Wenn Sie MBAM mit der Configuration Manager-Topologie bereitstellen, können Sie mithilfe von Configuration Manager die MBAM-Client Software auf Endbenutzercomputern bereitstellen. In Configuration Manager erstellt die MBAM-Installation eine Sammlung von Computern, die von MBAM verwaltet werden können. Diese Sammlung umfasst Workstations und Geräte, die nicht über ein Trusted Platform Module (TPM) verfügen, aber unter Windows 8 ausgeführt werden.

**Hinweis**  Windows to go wird für integrierte Configuration Manager-Installationen von MBAM nicht unterstützt, wenn Sie Configuration Manager 2007 verwenden.

 

## Bereitstellen des MBAM-Clients zum Aktivieren der BitLocker-Verschlüsselung nach der Computer Verteilung an Endbenutzer


Nachdem Sie die Gruppenrichtlinie konfiguriert haben, können Sie ein Produkt des Enterprise-Software Bereitstellungssystems wie Microsoft System Center Configuration Manager oder Active Directory-Domänendienste (AD DS) verwenden, um die Windows Installer-Dateien der MBAM-Client Installation auf Zielcomputern bereitzustellen. Zum Bereitstellen des MBAM-Clients können Sie entweder die 32-oder 64-Bit-MbamClientSetup.exe Dateien oder MBAMClient.msi Dateien verwenden, die mit der MBAM-Software bereitgestellt werden.

Wenn Sie den MBAM-Client nach dem Verteilen von Computern an Client Computer bereitstellen, werden Endbenutzer aufgefordert, Ihren Computer zu verschlüsseln. Dadurch kann MBAM die Daten sammeln, die die PIN und das Kennwort enthalten, und dann den Verschlüsselungsprozess beginnen.

**Hinweis**  Bei dieser Vorgehensweise werden Benutzer, die über Computer mit einem TPM-Chip verfügen, aufgefordert, den TPM-Chip zu aktivieren und zu initialisieren, wenn der Chip zuvor nicht aktiviert wurde.

 

## Verwenden des MBAM-Clients zum Aktivieren der BitLocker-Verschlüsselung vor der Computer Verteilung an Endbenutzer


In Organisationen, in denen Computer zentral empfangen und konfiguriert werden und Computer über einen kompatiblen TPM-Chip verfügen, können Sie den MBAM-Client installieren, um die BitLocker-Verschlüsselung auf jedem Computer zu verwalten, bevor Benutzerdaten darin geschrieben werden. Der Vorteil dieses Prozesses liegt darin, dass jeder Computer dann BitLocker-Verschlüsselungs kompatibel ist. Diese Methode ist nicht auf Benutzeraktionen angewiesen, da der Administrator den Computer bereits verschlüsselt hat. Eine wichtige Annahme für dieses Szenario ist, dass die Richtlinie des Unternehmens ein Windows-Abbild des Unternehmens installiert, bevor der Computer für den Benutzer bereitgestellt wird.

Wenn Ihre Organisation den TPM-Chip zum Verschlüsseln von Computern verwenden möchte, fügt der Administrator die TPM-Beschützer hinzu, um das Betriebssystem Volumen des Computers zu verschlüsseln. Wenn Ihre Organisation den TPM-Chip und eine PIN-Schutzkomponente verwenden möchte, verschlüsselt der Administrator das Betriebssystemvolume mit dem TPM-Schutz, und dann wählen Benutzer eine PIN aus, wenn Sie sich zum ersten Mal anmelden. Wenn Ihre Organisation entscheidet, nur die PIN-Beschützer zu verwenden, muss der Administrator das Volume nicht zuerst verschlüsseln. Wenn Benutzer sich anmelden, werden Sie von der Microsoft BitLocker-Verwaltung und-Überwachung aufgefordert, eine PIN oder eine PIN und ein Kennwort anzugeben, die für spätere Computerneustarts verwendet werden.

**Hinweis**  Die TPM-Schutzoption setzt voraus, dass der Administrator die BIOS-Eingabeaufforderung akzeptiert, um das TPM zu aktivieren und zu initialisieren, bevor der Computer an den Benutzer übermittelt wird.

 

## Verwandte Themen


[Planen der Bereitstellung von MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Bereitstellen des MBAM 2.0-Clients](deploying-the-mbam-20-client-mbam-2.md)

 

 





