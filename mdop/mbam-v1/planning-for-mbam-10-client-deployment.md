---
title: Planen der Clientbereitstellung für MBAM 1.0
description: Planen der Clientbereitstellung für MBAM 1.0
author: dansimp
ms.assetid: 3af2e7f3-134b-4ab9-9847-b07474ca6ac3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d58d6420febd2da9ee9cd4074fc8b5870285b0b4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811419"
---
# Planen der Clientbereitstellung für MBAM 1.0


Je nachdem, wann Sie den Microsoft BitLocker-Verwaltungs-und-Überwachungs Client (MBAM) bereitstellen, können Sie die BitLocker-Verschlüsselung auf einem Computer in Ihrer Organisation aktivieren, bevor der Endbenutzer den Computer oder anschließend empfängt. Um die BitLocker-Verschlüsselung zu aktivieren, nachdem der Endbenutzer den Computer empfangen hat, konfigurieren Sie die Gruppenrichtlinie. Um die BitLocker-Verschlüsselung zu aktivieren, bevor der Endbenutzer den Computer empfängt, stellen Sie die MBAM-Client Software mithilfe eines Enterprise-Software Bereitstellungssystems bereit.

Sie können eine oder beide Methoden in Ihrer Organisation verwenden. Wenn Sie beide Methoden verwenden, können Sie Compliance, Berichterstellung und Unterstützung für die Schlüsselwiederherstellung verbessern.

**Hinweis**  Informationen zum Überprüfen der MBAM-Client Systemanforderungen finden Sie unter [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).

 

## Bereitstellen des MBAM-Clients zum Aktivieren der BitLocker-Verschlüsselung nach der Computer Verteilung an Endbenutzer


Nachdem Sie die Gruppenrichtlinie konfiguriert haben, können Sie ein Produkt des Enterprise-Software Bereitstellungssystems wie Microsoft System Center Configuration Manager 2012 oder Active Directory-Domänendienste verwenden, um die Windows Installer-Dateien für die MBAM-Client Installation auf den Zielcomputern bereitzustellen. Die beiden Windows Installer-Dateien für die MBAM-Client Installation sind MBAMClient-64bit.msi und MBAMClient-32bit.msi, die mit der MBAM-Software bereitgestellt werden. Weitere Informationen zum Bereitstellen von MBAM-Gruppenrichtlinienobjekten finden Sie unter [Bereitstellen von MBAM 1,0-Gruppenrichtlinienobjekten](deploying-mbam-10-group-policy-objects.md).

Wenn Sie den MBAM-Client bereitstellen, werden die Endbenutzer nach dem Verteilen der Computer an Endbenutzer aufgefordert, ihre Computer zu verschlüsseln. Damit können MBAM die Daten sammeln, die PIN und das Kennwort einbeziehen und dann den Verschlüsselungsprozess beginnen.

**Hinweis**  Bei dieser Vorgehensweise werden Benutzer aufgefordert, den TPM-Chip (Trusted Platform Module) zu aktivieren und zu initialisieren, wenn er zuvor nicht aktiviert wurde.

 

## Verwenden des MBAM-Clients zum Aktivieren der BitLocker-Verschlüsselung vor der Computer Verteilung an Endbenutzer


In Organisationen, in denen Computer zentral empfangen und konfiguriert werden, können Sie den MBAM-Client installieren, um die BitLocker-Verschlüsselung auf jedem Computer zu verwalten, bevor Benutzerdaten darauf geschrieben werden. Der Vorteil dieses Prozesses besteht darin, dass jeder Computer dann mit der BitLocker-Verschlüsselung kompatibel ist. Diese Methode ist nicht auf Benutzeraktionen angewiesen, da der Administrator den Computer bereits verschlüsselt hat. Eine wichtige Annahme für dieses Szenario ist, dass die Richtlinie des Unternehmens ein Windows-Abbild des Unternehmens installiert, bevor der Computer für den Benutzer bereitgestellt wird.

Wenn Ihre Organisation (TPM) zum Verschlüsseln von Computern verwenden möchte, muss der Administrator die Betriebssystem Lautstärke des Computers mit TPM-Protector verschlüsseln. Wenn Ihre Organisation den TPM-Chip und eine PIN-Schutzkomponente verwenden möchte, muss der Administrator das System Volume mit dem TPM-Schutz verschlüsseln, und die Benutzer wählen dann bei der ersten Anmeldung eine PIN aus. Wenn Ihre Organisation entscheidet, nur die PIN-Beschützer zu verwenden, muss der Administrator das Volume nicht zuerst verschlüsseln. Wenn Benutzer sich auf ihren Computern anmelden, fordert MBAM Sie auf, eine PIN oder eine PIN und ein Kennwort anzugeben, die Sie verwenden, wenn Sie Ihren Computer später erneut starten.

**Hinweis**  Die TPM-Schutzoption erfordert, dass der Administrator die BIOS-Eingabeaufforderung akzeptiert, um das TPM zu aktivieren und zu initialisieren, bevor der Computer an den Benutzer bereitgestellt wird.

 

## Verwandte Themen


[Planen der Bereitstellung von MBAM 1.0](planning-to-deploy-mbam-10.md)

[Bereitstellen des MBAM 1.0-Clients](deploying-the-mbam-10-client.md)

 

 





