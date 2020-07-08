---
title: MED-V-TrimTransfer-Technologie
description: MED-V-TrimTransfer-Technologie
author: dansimp
ms.assetid: 2744e855-a486-4028-9606-f0084794ec65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa11c8036954070bbff465a6ad78992fdd52f3a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811605"
---
# MED-V-TrimTransfer-Technologie


## <a href="" id="bkmk-medvtrimtransfertechnology"></a>


Die Med-v Advanced Trim Transfer-Deduplizierungs-Technologie beschleunigt den Download von anfänglichen und aktualisierten virtuellen Computerbildern über das LAN oder WAN, wodurch die Netzwerkbandbreite verringert wird, die für den Transport eines virtuellen Computers mit einem Med-v-Arbeitsbereich an mehrere Endbenutzer erforderlich ist.

Diese bahnbrechende Technologie verwendet vorhandene lokale Daten, um das Bild des virtuellen Computers zu erstellen, und nutzt dabei die Tatsache, dass in vielen Fällen ein Großteil des virtuellen Computers (beispielsweise System-und Anwendungsdateien) auf dem Datenträger des Endbenutzers bereits vorhanden ist. Wenn beispielsweise ein virtueller Computer, der WindowsXP enthält, an einen Client mit einer lokalen Kopie von WindowsXP übermittelt wird, entfernt MED-V automatisch die redundanten WindowsXP-Elemente aus der Übertragung. Um einen gültigen und funktionsfähigen Arbeitsbereich zu gewährleisten, überprüft der MED-V-Client die Integrität lokaler Daten vor der Verwendung kryptografisch, und gewährleistet, dass die lokalen Datenblöcke absolut identisch mit denen im Bild des gewünschten virtuellen Computers sind. Blöcke, die nicht übereinstimmen, werden nicht verwendet.

Der Prozess ist bandbreiteneffizient und transparent, und Übertragungen werden im Hintergrund ausgeführt, wobei ungenutzte Netzwerk-und CPU-Ressourcen verwendet werden.

Beim Aktualisieren auf eine neue Bildversion (beispielsweise wenn Administratoren eine neue Anwendung oder einen neuen Patch verteilen möchten) werden nur die geänderten Elemente ("Deltas") heruntergeladen, und nicht die gesamte virtuelle Maschine, wodurch die erforderliche Netzwerkbandbreite und die erforderliche Lieferzeit erheblich reduziert werden.

Sie können konfigurieren, welche Ordner auf dem Host als Teil des Trim-Übertragungsprotokolls basierend auf dem Hostbetriebssystem indiziert werden. Diese Einstellungen werden in der *ClientSettings.xml* -Datei konfiguriert, die im Ordner **Servers\\Configuration Server\\** zu finden ist.

Bei der Anwendung neuer Einstellungen muss der Dienst neu gestartet werden.

```xml
<HostIndexingXP type="System.String[]"> 
- <ArrayOfString>
<string>%WINDIR%</string> 
<string>%ProgramFiles%\Common Files</string> 
<string>%ProgramFiles%\Internet Explorer</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
<string>%ProgramFiles%\Windows NT</string> 
<string>%ProgramFiles%\Messenger</string> 
<string>%ProgramFiles%\Adobe</string> 
<string>%ProgramFiles%\Outlook Express</string> 
</ArrayOfString> 
</HostIndexingXP> 
- <HostIndexingVista type="System.String[]"> 
- <ArrayOfString> 
<string>%WINDIR%\MSAgent</string> 
<string>%WINDIR%\winsxs</string> 
<string>%WINDIR%\system</string> 
<string>%WINDIR%\system32</string> 
<string>%WINDIR%\Microsoft.NET</string> 
<string>%WINDIR%\SoftwareDistribution</string> 
<string>%WINDIR%\L2Schemas</string> 
<string>%WINDIR%\Cursors</string> 
<string>%WINDIR%\Boot</string> 
<string>%WINDIR%\Help</string> 
<string>%WINDIR%\assembly</string> 
<string>%WINDIR%\inf</string> 
<string>%WINDIR%\fonts</string> 
<string>%WINDIR%\Installer</string> 
<string>%WINDIR%\IME</string> 
<string>%WINDIR%\Resources</string> 
<string>%WINDIR%\servicing</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
</ArrayOfString> 
</HostIndexingVista>
```

 

 





