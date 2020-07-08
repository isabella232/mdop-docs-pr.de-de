---
title: Bereitstellen des MBAM 1.0-Clients
description: Bereitstellen des MBAM 1.0-Clients
author: dansimp
ms.assetid: f7ca233f-5035-4ff9-ab3a-f2453b4929d1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dee8c2f4a9b398c9f0797ada35e4c36610c755b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809634"
---
# Bereitstellen des MBAM 1.0-Clients


Der Client für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen. Der BitLocker-Client kann in eine Organisation integriert werden, indem der Client mithilfe von Tools wie Active Directory-Domänendiensten oder durch direkte Verschlüsselung der Clientcomputer im Rahmen des anfänglichen Imaging-Prozesses bereitgestellt wird.

Je nachdem, ob Sie den MBAM-Client bereitstellen, können Sie die BitLocker-Verschlüsselung auf einem Computer in Ihrer Organisation aktivieren, bevor oder nachdem der Endbenutzer den Computer empfängt. Um diesen Zeitpunkt zu steuern, konfigurieren Sie Gruppenrichtlinien und stellen die MBAM-Client Software mithilfe eines Enterprise-Software Bereitstellungssystems bereit.

Sie können eine oder beide dieser Methoden in Ihrer Organisation verwenden. Wenn Sie beide Methoden verwenden, können Sie Compliance, Berichterstellung und Unterstützung für die Schlüsselwiederherstellung verbessern.

## Bereitstellen des MBAM-Clients auf Desktop-oder Laptopcomputern


Nachdem Sie die Gruppenrichtlinie konfiguriert haben, können Sie die Windows Installer-Dateien für die MBAM-Client Installation auf Zielcomputern bereitstellen. Dazu können Sie ein Produkt des Enterprise-Software Bereitstellungssystems wie Microsoft System Center 2012 Configuration Manager oder Active Directory-Domänendienste verwenden. Die beiden verfügbaren Windows Installer-Dateien für die MBAM-Client Installation sind MBAMClient-64bit.msi und MBAMClient-32bit.msi. Diese Dateien werden mit der MBAM-Software bereitgestellt. Weitere Informationen zum Bereitstellen von MBAM-Gruppenrichtlinienobjekten finden Sie unter [Bereitstellen von MBAM 1,0-Gruppenrichtlinienobjekten](deploying-mbam-10-group-policy-objects.md).

[So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-1.md)

## Bereitstellen des MBAM-Clients als Teil einer Windows-Bereitstellung


In einigen Organisationen werden neue Computer zentral empfangen und konfiguriert. In dieser Situation können Administratoren den MBAM-Client installieren, um die BitLocker-Verschlüsselung auf jedem Computer zu verwalten, bevor Benutzerdaten auf den Computer geschrieben werden. Dieser Ansatz trägt dazu bei, sicherzustellen, dass Computer ordnungsgemäß verschlüsselt sind, da der Administrator die Aktion ausführt, ohne auf die Endbenutzer Aktion Vertrauen zu müssen. Eine wichtige Annahme für dieses Szenario ist, dass die Richtlinie des Unternehmens ein Windows-Abbild des Unternehmens installiert, bevor der Computer für den Benutzer bereitgestellt wird.

[So stellen Sie den MBAM-Client im Rahmen einer Windows-Bereitstellung bereit](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-1.md)

## Weitere Ressourcen für die Bereitstellung des MBAM-Clients


[Bereitstellen von MBAM 1.0](deploying-mbam-10.md)

[Planen der Clientbereitstellung für MBAM 1.0](planning-for-mbam-10-client-deployment.md)

 

 





