---
title: Entfernen von MBAM-Serverfunktionen oder -software
description: Entfernen von MBAM-Serverfunktionen oder -software
author: dansimp
ms.assetid: 5212ba3f-124d-43c5-824a-608e9a192e86
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e6e57c3d2a62a4e01242ade7a82a7bfa551da83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810879"
---
# Entfernen von MBAM-Serverfunktionen oder -software


In diesen Anweisungen wird erläutert, wie Software und Features aus der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) entfernt werden. Wenn Sie die MBAM-Server Features entfernen, werden nur die konfigurierten Features vom Server entfernt, nicht die MBAM-Server Software. Wenn Sie die MBAM-Server Software entfernen, werden die Software und alle MBAM-Server Features, die Sie auf diesem Server konfiguriert haben, entfernt.

**Hinweis**  Um zu verhindern, dass Daten versehentlich entfernt werden, bietet MBAM keinen Mechanismus zum Entfernen der Datenbanken. Sie müssen dies manuell tun.

 

## <a href="" id="bkmk-removeserverfeatures"></a>Entfernen von MBAM-Server Features


Sie können eine der folgenden Methoden verwenden, um von Ihnen konfigurierte MBAM-Server Features zu entfernen:

-   MBAM-Serverkonfigurations-Assistent

-   Windows PowerShell-Cmdlets

### Verwenden des MBAM-Serverkonfigurations-Assistenten zum Entfernen von Features

Befolgen Sie diese Anweisungen, um den MBAM-Serverkonfigurations-Assistenten zu verwenden, um konfigurierte MBAM-Server Features von einem Server zu entfernen.

**So entfernen Sie MBAM-Features mithilfe des Assistenten**

1.  Wählen Sie auf dem Server, auf dem Sie Features entfernen möchten, die Option **MBAM Server Configuration** aus, um den Konfigurations-Assistenten zu öffnen.

2.  Klicken Sie auf **Features entfernen**, wählen Sie die zu entfernenden Features aus, und klicken Sie dann auf **weiter**. Auf einer **Zusammenfassungs** Seite werden die Features angezeigt, die Sie zum Entfernen ausgewählt haben.

3.  Klicken Sie auf **Entfernen** , um das Entfernen der Features zu starten, und klicken Sie dann auf **Schließen**.

### Verwenden von Windows PowerShell zum Entfernen von Features

Führen Sie die folgenden Schritte als allgemeine Anleitung zum Entfernen von MBAM-Server Features mithilfe von Windows PowerShell-Cmdlets aus.

**So entfernen Sie MBAM-Features mithilfe von Windows PowerShell**

1.  Bevor Sie Features entfernen, lesen Sie [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) zum Überprüfen der Voraussetzungen für die Verwendung von Windows PowerShell.

2.  Verwenden Sie die folgenden Cmdlets, um die MBAM-Server Features zu entfernen:

    -   Deaktivieren-MbamReport

    -   Deaktivieren-MbamWebApplication

    -   Deaktivieren-MbamCMIntegration

    Wenn Sie Hilfe zu Windows PowerShell-Cmdlets erhalten möchten, geben Sie **Get-Help-** &lt; *Cmdlet* ein, &gt; oder lesen Sie die Seite [Automatisierung des Microsoft-Desktop Optimierungs Pakets mit Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) für die MBAM Windows PowerShell-Cmdlets.

## Entfernen der MBAM-Server Software


Führen Sie die folgenden Schritte aus, um die MBAM-Server Software und alle MBAM-Server Features zu entfernen, die Sie auf diesem Server konfiguriert haben.

**So entfernen Sie die MBAM-Server Software**

1.  Führen Sie auf dem Server, auf dem Sie die MBAM-Server Software deinstallieren möchten, **MBAMserversetup.exe** aus, um den Setup-Assistenten für Microsoft BitLocker-Verwaltung und-Überwachung zu starten.

2.  Wählen Sie **deinstallieren**aus, und folgen Sie den restlichen Eingabeaufforderungen, um den Vorgang der Deinstallation der MBAM-Server Software abzuschließen.



## Verwandte Themen


[Bereitstellen von MBAM 2.5](deploying-mbam-25.md)

 

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



