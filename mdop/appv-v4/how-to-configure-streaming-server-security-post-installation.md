---
title: So konfigurieren Sie die Streaming Server Security-Nachinstallation
description: So konfigurieren Sie die Streaming Server Security-Nachinstallation
author: dansimp
ms.assetid: 9bde3677-d1aa-4dcc-904e-bb49a268d748
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1945b38da5dd50c0bd2fb0c741bd92012e78586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807292"
---
# So konfigurieren Sie die Streaming Server Security-Nachinstallation


Konfigurieren Sie den App-V-Streamingserver für erhöhte Sicherheit über die Registrierung. Wie beim App-V-Verwaltungsserver muss ein Zertifikat ordnungsgemäß mit dem richtigen EKU-Bezeichner für die Server Authentifizierung bereitgestellt werden, bevor Sie das folgende Verfahren nach der Installation ausführen.

**So konfigurieren Sie die Streaming Server-Sicherheit nach der Installation**

1.  Erstellen Sie eine MMC, fügen **Sie das** Zertifikat-Snap-in hinzu, und wählen Sie den **Zertifikatspeicher für den lokalen Computer**aus.

2.  Öffnen Sie die **persönlichen** Zertifikate für den Computer, und öffnen Sie das Zertifikat, das für App-V bereitgestellt wurde.

3.  Scrollen Sie auf der Registerkarte **Details** nach unten zum Fingerabdruck, und kopieren Sie den Hash im Detailbereich.

4.  Öffnen Sie den Registrierungs-Editor, und navigieren Sie zu `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server` .

5.  Bearbeiten `X509CertHash` Sie den Wert, fügen Sie den Fingerabdruck Hash in das Feld Wert ein, und entfernen Sie alle Leerzeichen. Klicken Sie auf **OK** , um die Bearbeitung zu übernehmen.

6.  Navigieren Sie im Registrierungs-Editor zu `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts` .

7.  Erstellen Sie einen neuen **DWORD** -Wert mit dem Namen "322", und geben Sie dann den Dezimalwert als 322 oder den Hexadezimalwert als 142 ein.

8.  Starten Sie den Streamingdienst neu.

## Verwandte Themen


[So konfigurieren Sie Management Server Security-Nachinstallation](how-to-configure-management-server-security-post-installation.md)

[Behandeln von Problemen mit Zertifikatberechtigungen](troubleshooting-certificate-permission-issues.md)

 

 





