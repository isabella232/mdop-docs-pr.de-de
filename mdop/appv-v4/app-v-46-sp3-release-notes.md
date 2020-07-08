---
title: App-V 4.6 SP3 – Versionshinweise
description: App-V 4.6 SP3 – Versionshinweise
author: dansimp
ms.assetid: 206fadeb-59cc-47b4-836f-191ab1c27ff8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: dd0b82c5e12cbe161066a7f4a4e0932cb92cca42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808048"
---
# App-V 4.6 SP3 – Versionshinweise


Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.

Lesen Sie diese Versionshinweise gründlich, bevor Sie das Microsoft Application Virtualization (App-V)-Verwaltungs System installieren. Diese Anmerkungen zu dieser Version enthalten Informationen, die Ihnen bei der erfolgreichen Installation von Application Virtualization (App-V) 4.6 SP3 helfen. Dieses Dokument enthält Informationen, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es einen Unterschied zwischen diesen Anmerkungen zu dieser Version und einer anderen App-V-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## Schutz vor Sicherheitsrisiken und Viren


Zum Schutz vor Sicherheitsrisiken und Viren ist es wichtig, die neuesten verfügbaren Sicherheitsupdates für jede neue Software zu installieren, die installiert wird. Weitere Informationen finden Sie auf der [Microsoft-Sicherheitswebsite](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Bekannte Probleme mit Application Virtualization 4.6 SP3


In diesem Abschnitt finden Sie die neuesten Informationen zu Problemen mit Microsoft Application Virtualization (App-V) 4.6 SP3. Diese Probleme werden in der Produktdokumentation nicht angezeigt und können in einigen Fällen der vorhandenen Produktdokumentation widersprechen. Wenn dies möglich ist, werden diese Probleme in späteren Versionen behoben.

### In der virtuellen Umgebung können keine Links mit Internet Explorer11 auf Microsoft Windows 8,1 geöffnet werden

Der Versuch, Hyperlinks innerhalb einer virtuellen Umgebung zu öffnen, schlägt in Windows 8,1 mit Internet Explorer 11 fehl. Der Grund dafür ist, dass Internet Explorer 11 nun standardmäßig mit aktiviertem erweiterten Schutzmodus (EPM) ausgeliefert wird und App-V nicht in der Lage ist, auf erforderliche Registrierungsschlüssel, Dateien und Kommunikations Port Objekte zuzugreifen.

Problemumgehung: Deaktivieren Sie EPM in Internet Explorer11, bevor Sie ein App-V-Paket öffnen. Auf diese Weise können Sie Internet Explorer in der virtuellen Umgebung öffnen.

## Verwandte Themen


[Informationen zu Microsoft Application Virtualization 4.6SP3](about-microsoft-application-virtualization-46-sp3.md)

 

 





