---
title: High-Level-Architektur
description: High-Level-Architektur
author: dansimp
ms.assetid: a00edb9f-207b-4f32-9e8f-522ea2739d2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a5db4a56b2abfb0df19b0d6d86f4bf88380c2bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812268"
---
# High-Level-Architektur


In diesem Abschnitt werden die allgemeine Systemarchitektur und der Komponentenentwurf von Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 beschrieben.

## System Architektur


MED-V verbessert den Windows Virtual PC, um zwei Betriebssysteme auf einem Gerät auszuführen, wobei die Bereitstellung virtueller Bilder, die gruppenrichtlinienbasierte Bereitstellung und die zentralisierte Verwaltung hinzugefügt werden. Mithilfe von MED-V können Sie Windows Virtual PC-Images auf einem beliebigen Windows-basierten Desktop, auf dem Windows 7 Professional, Enterprise oder Windows 7 Ultimate ausgeführt wird, problemlos konfigurieren, bereitstellen und verwalten. Die MED-V-Lösung umfasst die folgenden Komponenten:

<a href="" id="---------------med-v-host"></a> **MED-V-Host**  
Eine Windows 7-Umgebung mit einem Med-v-Host-Agent, einem ESD-System (Electronic Software Distribution), einem Registrierungs Verwaltungssystem und einem Med-v-Gast. Der Med-v-Host interagiert mit dem Med-v-Gast, damit bestimmte Setup Funktionen und Systeminformationen verarbeitet werden können.

<a href="" id="-------------------med-v-host-agent"></a> **MED-V-Host-Agent**  
Die im Med-v-Host enthaltene Med-v-Software, die einen Kanal für die Kommunikation mit dem Med-v-Gast bereitstellt. Darüber hinaus bietet es Funktionen wie das erstmalige Einrichten und die Anwendungsveröffentlichung.

**Hinweis**  Nachdem Med-v und die erforderlichen Komponenten installiert sind, muss Med-v konfiguriert werden. Die Konfiguration von MED-V wird als erstmalige Einrichtung bezeichnet.

 

<a href="" id="esd-system"></a>**ESD-System**  
Ihre vorhandene Softwareverteilungsmethode, mit der Sie die von Med-v erstellten Med-v-Arbeitsbereichs Paketdateien bereitstellen und installieren können.

<a href="" id="registry-management-system"></a>**Registrierungs Verwaltungs System**  
Ihre vorhandene Methode zum Verwalten von Gruppenrichtlinieneinstellungen und-Einstellungen.

<a href="" id="windows-virtual-pc-image"></a>**Windows Virtual PC-Bild**  
Ein vom Administrator definierter virtueller Computer, der die folgenden Komponenten enthält:

<a href="" id="corporate-operating-system"></a>**Betriebs System des Unternehmens**  
Ihr Standard-Betriebssystem für Unternehmen.

<a href="" id="management-and-security-tools"></a>**Verwaltungs-und Sicherheits Tools**  
Ihre standardmäßigen Verwaltungs-und Sicherheitstools wie Virenschutz.

<a href="" id="-----------------------med-v-guest"></a> **MED-V-Gast**  
Eine Windows XP SP3-Umgebung als Teil eines Windows Virtual PC unter Windows 7 mit den folgenden Komponenten:

<a href="" id="---------------------------med-v-guest-agent"></a> **MED-V-Gast-Agent**  
Die im Med-v-Gast enthaltene Med-v-Software, die einen Kanal für die Kommunikation mit dem Med-v-Host bereitstellt. Darüber hinaus unterstützt der MED-V-Host-Agent Funktionen wie das Durchführen der erstmaligen Einrichtung.

**Hinweis**  Der MED-V-Gast-Agent wird während der erstmaligen Einrichtung automatisch installiert.

 

<a href="" id="esd-client"></a>**ESD-Client**  
Ein optionaler Teil Ihres ESD-Systems, mit dem Softwarepakete und Statusberichte für das ESD-System installiert werden.

## Verwandte Themen


[Planen der Betriebssystemkompatibilität der Anwendung](planning-for-application-operating-system-compatibility.md)

[Vorbereiten der Bereitstellungsumgebung für MED-V](prepare-the-deployment-environment-for-med-v.md)

 

 





