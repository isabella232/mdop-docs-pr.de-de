---
title: Bereitstellen des MBAM 2.0-Clients
description: Bereitstellen des MBAM 2.0-Clients
author: dansimp
ms.assetid: 3dd584fe-2a54-40f0-9bab-13ea74040b01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa42c8ab3adc273f0e00ba56a59f487deba89c6f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809961"
---
# Bereitstellen des MBAM 2.0-Clients


Der Client für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen. Der BitLocker-Client kann in eine Organisation integriert werden, indem der Client über ein elektronisches Softwareverteilungssystem, wie etwa Active Directory-Domänendienste, bereitgestellt wird, oder indem die Clientcomputer im Rahmen des anfänglichen Imaging-Prozesses direkt verschlüsselt werden.

Je nachdem, ob Sie den Microsoft BitLocker-Verwaltungs-und Überwachungs Client bereitstellen, können Sie die BitLocker-Verschlüsselung auf einem Computer in Ihrer Organisation aktivieren, bevor der Endbenutzer den Computer empfängt, oder anschließend, indem Sie die Gruppenrichtlinie konfigurieren und die MBAM-Client Software mithilfe eines Enterprise-Software Bereitstellungssystems bereitstellen.

## Bereitstellen des MBAM-Clients auf Desktop-oder Laptop Computern


Nachdem Sie die Gruppenrichtlinie konfiguriert haben, können Sie ein Produkt des Enterprise-Software Bereitstellungssystems wie Microsoft System Center Configuration Manager 2012 oder Active Directory-Domänendienste verwenden, um die Windows Installer-Dateien für die MBAM-Client Installation auf Zielcomputern bereitzustellen. Sie können den Client entweder mithilfe der 32-oder 64-Bit-MbamClientSetup.exe Dateien oder der 32-Bit-oder 64-Bit-MBAMClient.msi Dateien bereitstellen, die mit der MBAM-Software bereitgestellt werden. Weitere Informationen zum Bereitstellen von MBAM-Gruppenrichtlinienobjekten finden Sie unter [Bereitstellen von MBAM 2,0-Gruppenrichtlinienobjekten](deploying-mbam-20-group-policy-objects-mbam-2.md).

[So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-2.md)

## Bereitstellen des MBAM-Clients als Teil einer Windows-Bereitstellung


In Organisationen, in denen Computer zentral empfangen und konfiguriert werden, können Sie den MBAM-Client installieren, um die BitLocker-Verschlüsselung auf jedem Computer zu verwalten, bevor Benutzerdaten darin geschrieben werden. Der Vorteil dieses Prozesses liegt darin, dass jeder Computer dann BitLocker-Verschlüsselungs kompatibel ist. Diese Methode ist nicht auf Benutzeraktionen angewiesen, da der Administrator den Computer bereits verschlüsselt hat. Eine wichtige Annahme für dieses Szenario ist, dass die Richtlinie des Unternehmens ein Windows-Abbild des Unternehmens installiert, bevor der Computer für den Benutzer bereitgestellt wird. Wenn die Gruppenrichtlinie so konfiguriert ist, dass eine PIN erforderlich ist, werden die Benutzer aufgefordert, eine PIN festzulegen, nachdem Sie die Gruppenrichtlinie empfangen haben.

[So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-2.md)

## So verwenden Sie eine Befehlszeile zum Installieren des MBAM-Clients


In diesem Abschnitt wird erläutert, wie Sie den MBAM-Client mithilfe einer Befehlszeile installieren.

[So verwenden Sie eine Befehlszeile zum Installieren des MBAM-Clients](how-to-use-a-command-line-to-install-the-mbam-client.md)

## Weitere Ressourcen für die Bereitstellung des MBAM-Clients


[Bereitstellen von MBAM 2,0](deploying-mbam-20-mbam-2.md)[Planung für MBAM 2,0-Client Bereitstellung](planning-for-mbam-20-client-deployment-mbam-2.md)

 

 





