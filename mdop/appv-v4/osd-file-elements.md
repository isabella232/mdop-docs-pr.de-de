---
title: Elemente der OSD-Datei
description: Elemente der OSD-Datei
author: dansimp
ms.assetid: 8211b562-7549-4331-8321-144f52574e99
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8e3ebcf53ff39ecd2ef7ad0feec0bbbcae199db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806575"
---
# Elemente der OSD-Datei


Das Sequencer-Installationsverzeichnis enthält eine XML-Schemadatei, **Softricity. xsd**, die die gültige Struktur einer Open Software Descriptor-Datei (OSD) definiert. Im folgenden finden Sie einige der häufiger verwendeten OSD-Elemente.

<a href="" id="softpkg"></a>SOFTPKG  
Das Stammelement der OSD-Datei, die alle Elemente enthält, die das Softwarepaket definieren.

<a href="" id="codebase"></a>CodeBase  
Informationen zur SFT-Datei für dieses Paket, einschließlich der Attribute href, filename und GUID. Sie können das href-Attribut bearbeiten, wenn Sie den Verteilungspunkt dieses bestimmten Pakets ändern.

<a href="" id="os"></a>Betriebssystem  
Definiert, auf welchen Betriebssystemen diese Anwendung basierend auf Werten ausgeführt werden kann, die anfangs im Sequenz-Assistenten festgelegt sind. Dieser Wert kann nur die Werte enthalten, die in **Softricity. xsd**definiert sind.

<a href="" id="local-interaction-allowed"></a>lokal \ _INTERACTION \ _ALLOWED  
Auf true festgelegt, ermöglicht dies die Erstellung benannter Objekte (Ereignisse, Mutexe, Semaphoren, Dateizuordnungen und Mailslots) und COM-Objekte im globalen Namespace, anstatt innerhalb einer bestimmten virtuellen Umgebung isoliert zu werden, wodurch virtuellen Anwendungen die Interaktion mit den Anwendungen des Hostbetriebssystems ermöglicht wird.

Beispiel: &lt; SOFTPKG- &gt; &lt; Implementierung&gt;

&lt;VIRTUALENV- &gt; &lt; Richtlinien&gt;

&lt;LOCAL \ _INTERACTION \ _ALLOWED &gt; true

&lt;/LOCAL\ _INTERACTION \ _ALLOWED&gt;

&lt;/Policies &gt; &lt; /VIRTUALENV&gt;

&lt;/Implementation &gt; &lt; /SOFTPKG&gt;

<a href="" id="dependencies"></a>Abhängigkeiten  
Definiert die dynamische Suite-Komposition (Abhängigkeiten von anderen Paketen) mithilfe eines CodeBase-Tags aus einem anderen Paket.

Beispiel: &lt; Abhängigkeiten &gt; &lt; CodeBase href = "RTSPS://Server/Package.SFT" GUID = "7579F4DF-2461-4219-BD43-494E1FDC69E3" sysguarddatei = "pkg. 1 \ \ osguard. CP" size = "6572748" Mandatory = "falsch"/ &gt; &lt; /Dependencies&gt;

<a href="" id="package-name"></a>Paket Name  
Ein allgemeiner Name für das Paket, das in die **Paket Informations** Seite des Sequenz-Assistenten eingegeben wurde, mit der Sie einen einzelnen Namen für eine sequenzierte Anwendung mit mehreren Anwendungen angeben können.

<a href="" id="title"></a>Titel  
Optionaler beschreibender Name der Anwendung, die Sie sequenzieren.

<a href="" id="abstract"></a>Abstrakt  
Kurzbeschreibung des Softwarepakets, das im Feld " **Kommentare** " auf der **Paket Informations** Seite des Sequenz-Assistenten eingegeben wurde. Es empfiehlt sich, Informationen wie das Betriebssystem und die Service Pack-Ebene der Sequencer-Workstation, die Sequencer-Version und den Namen des Sequenzierungs Ingenieurs anzugeben.

<a href="" id="script"></a>Skript  
Definiert bestimmte Skriptereignisse, die beim Starten, Herunterfahren oder Streaming auftreten können.

<a href="" id="mgmt-shortcutlist"></a>Mgmt \ _SHORTCUTLIST  
Liste aller im Assistenten definierten Tastenkombinationen

<a href="" id="mgmt-fileassociations"></a>Mgmt \ _FILEASSOCIATIONS  
Liste der im Assistenten angegebenen Dateitypen.

## Verwandte Themen


[Informationen zur Registerkarte „OSD“](about-the-osd-tab.md)

 

 





