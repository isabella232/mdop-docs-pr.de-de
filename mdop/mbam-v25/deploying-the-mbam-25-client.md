---
title: Bereitstellen des MBAM 2.5-Clients
description: Bereitstellen des MBAM 2.5-Clients
author: dansimp
ms.assetid: 0a96a0ee-f280-49d9-a244-88f4147fe9fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 375af8966c8e66a58baec5065d065891187899fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811659"
---
# Bereitstellen des MBAM 2.5-Clients


Die Microsoft BitLocker-Client Software für die Verwaltung und Überwachung (MBAM) ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen. Der BitLocker-Client kann in eine Organisation integriert werden, indem der Client über ein elektronisches Softwareverteilungssystem, wie etwa Active Directory-Domänendienste, bereitgestellt wird, oder indem die Clientcomputer im Rahmen des anfänglichen Imaging-Prozesses direkt verschlüsselt werden.

Je nachdem, ob Sie die Microsoft BitLocker-Verwaltungs-und-Überwachungs Client Software bereitstellen, können Sie die BitLocker-Laufwerkverschlüsselung auf einem Computer in Ihrer Organisation aktivieren, bevor der Endbenutzer den Computer empfängt, oder anschließend, indem Sie die Gruppenrichtlinie konfigurieren und die MBAM-Client Software mithilfe eines Enterprise-Software Bereitstellungssystems bereitstellen.

## Bereitstellen des MBAM-Clients auf Desktop-oder Laptopcomputern


Nachdem Sie die Gruppenrichtlinieneinstellungen konfiguriert haben, können Sie ein Produkt des Enterprise-Software Bereitstellungssystems wie MicrosoftSystemCenter2012 ConfigurationManager oder Active Directory-Domänendienste verwenden, um die Windows Installer-Dateien für die MBAM-Client Installation auf Zielcomputern bereitzustellen. Sie können entweder die 32-Bit-oder 64-Bit-MbamClientSetup.exe Dateien oder die 32-Bit-oder 64-Bit-MBAMClient.msi Dateien verwenden, die mit der MBAM-Client Software bereitgestellt werden. Weitere Informationen zum Bereitstellen von MBAM-Gruppenrichtlinieneinstellungen finden Sie unter [Bereitstellen von MBAM 2,5-Gruppenrichtlinienobjekten](deploying-mbam-25-group-policy-objects.md).

**Hinweis**  Ab MBAM 2,5 SP1 ist eine separate MSI-Version nicht mehr im MBAM-Produkt enthalten. Sie können die MSI-Datei jedoch aus der ausführbaren Datei (. exe) extrahieren, die im Lieferumfang des Produkts enthalten ist.

 

[So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25.md)

## Bereitstellen des MBAM-Clients als Teil einer Windows-Bereitstellung


In Organisationen, in denen Computer zentral empfangen und konfiguriert werden, können Sie den MBAM-Client installieren, um die BitLocker-Laufwerkverschlüsselung auf jedem Computer zu verwalten, bevor Benutzerdaten darin geschrieben werden. Der Vorteil dieses Prozesses liegt darin, dass jeder Computer dann mit der BitLocker-Laufwerkverschlüsselung kompatibel ist. Diese Methode ist nicht auf Benutzeraktionen angewiesen, da der Administrator den Computer bereits verschlüsselt hat. Eine wichtige Annahme für dieses Szenario ist, dass die Richtlinie des Unternehmens ein Windows-Abbild des Unternehmens installiert, bevor der Computer für den Benutzer bereitgestellt wird. Wenn die Gruppenrichtlinieneinstellungen so konfiguriert sind, dass eine PIN erforderlich ist, werden die Benutzer aufgefordert, eine PIN festzulegen, nachdem Sie die Richtlinie erhalten haben.

[So aktivieren Sie BitLocker im Rahmen einer Windows-Bereitstellung mithilfe von MBAM](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

## Bereitstellen des MBAM-Clients mithilfe einer Befehlszeile


In diesem Abschnitt wird erläutert, wie Sie den MBAM-Client mithilfe einer Befehlszeile installieren.

[So stellen Sie den MBAM-Client über eine Befehlszeile bereit](how-to-deploy-the-mbam-client-by-using-a-command-line.md)

## Weitere Ressourcen für die Bereitstellung des MBAM-Clients


[Bereitstellen von MBAM 2.5](deploying-mbam-25.md)



## Verwandte Themen


[Bereitstellen von MBAM 2.5](deploying-mbam-25.md)

[Planen von MBAM 2.5](planning-for-mbam-25.md)

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





