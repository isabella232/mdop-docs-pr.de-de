---
title: Konfigurieren von MED-V-Server für den Clustermodus
description: Konfigurieren von MED-V-Server für den Clustermodus
author: dansimp
ms.assetid: 41f0b2a3-4ce9-48e1-a6fb-4c13c4228515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddb7dd5af65d8a465c5c1884bb27a3027621bac1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811923"
---
# Konfigurieren von MED-V-Server für den Clustermodus


Sie können den MED-V-Server im Clustermodus konfigurieren. Im Clustermodus werden zwei Server verwendet, und alle Dateien, die als Gegenüberstellung zu beiden Servern identifiziert werden, werden in einem Dateisystemgespeichert. Der Server greift auf die Dateien aus dem Dateisystem zu, anstatt die Dateien lokal zu speichern.

## <a href="" id="bkmk-howtoconfigurethemedvserverinclustermode"></a>


**So konfigurieren Sie den MED-V-Server im Clustermodus**

1.  Installieren und konfigurieren Sie MED-V auf einem der Server.

2.  Erstellen Sie ein freigegebenes Netzwerk an einem zentralen Ort, an dem alle Server darauf zugreifen können.

3.  Kopieren Sie den Inhalt des * &lt; INSTALLDIR &gt; /Servers/ConfigurationServer* -Ordners in das freigegebene Netzwerk.

4.  Installieren Sie den MED-V-Server auf allen benannten Servern.

5.  Weisen Sie im freigegebenen Netzwerk vollständigen Zugriff auf alle MED-V Server-Systemkonten zu.

6.  Gehen Sie auf jedem Server wie folgt vor:

    1.  Legen Sie in der Datei * &lt; INSTALLDIR &gt; /Server/ServerConfiguration.xml* den Wert von * &lt; storePath &gt; * auf den freigegebenen Netzwerkpfad.

    2.  Kopieren Sie die * &lt; InstsallDir- &gt; /Server/KeyPair.xml* Datei vom ursprünglichen Server auf alle MED-V-Server.

    3.  Starten Sie den MED-V-Dienst erneut.

**Hinweis**  Wenn alle Server über die gleichen lokalen Einstellungen verfügen (wie Abhör Anschlüsse, IIS-Server, Verwaltungsberechtigungen, Berichtsdatenbank usw.), können die * &lt; INSTALLDIR- &gt; /Server/ServerSettings.xml* auch von allen Servern freigegeben werden.

 

## Verwandte Themen


[Planen und Entwerfen der MED-V-Infrastruktur](med-v-infrastructure-planning-and-design.md)

 

 





