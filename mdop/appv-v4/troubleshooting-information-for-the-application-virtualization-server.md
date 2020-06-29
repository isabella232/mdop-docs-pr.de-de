---
title: Informationen zur Problembehandlung für Application Virtualization Server
description: Informationen zur Problembehandlung für Application Virtualization Server
author: dansimp
ms.assetid: e9d43d9b-84f2-4d1b-bb90-a13740151e0c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c98ad42a00e20900263d0598822a6381e2df1ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806207"
---
# Informationen zur Problembehandlung für Application Virtualization Server


Dieses Thema enthält Informationen, die Sie zur Behebung verschiedener Probleme auf den Application Virtualization (App-V)-Servern verwenden können.

## Warnungsmeldung 25017 im Setup Protokoll nach der Installation des Servers


Nach der Installation finden Sie möglicherweise die folgende Meldung im Server Setup-Protokoll.

*Warnung 25017. Das Installationsprogramm konnte das Active Directory-Markierungsobjekt für den Server nicht erstellen. Das für die Installation verwendete Konto hatte nicht genügend Rechte zum Schreiben in Active Directory oder Active Directory war nicht verfügbar.*

Das Installationsprogramm für App-V Management oder Streaming Server erstellt einen Dienstverbindungspunkt Eintrag unter dem Computerobjekt in den Active Directory-Domänendiensten (Adds), der dem Computer entspricht, auf dem der Server installiert ist, wenn das zum Ausführen des Installationsprogramms verwendete Konto über die entsprechenden Rechte verfügt. Wenn Sie diesen Eintrag nicht erstellen, kann die Installation nicht fehlschlagen, was sonst die Funktionsweise des Produkts beeinträchtigt. Der wahrscheinlichste Grund für einen Fehler besteht darin, dass das zum Ausführen der Installation verwendete Benutzerkonto nicht über die erforderlichen Rechte zum Schreiben in Adds verfügt. Obwohl das Registrieren des App-v-Servers in Adds optional ist, ist es in einem solchen Fall für zentralisierte Verwaltungstools möglich, den App-v-Server für Inventar-und Verwaltungszwecke zu finden.

## Verwandte Themen


[Application Virtualization Server](application-virtualization-server.md)

 

 





