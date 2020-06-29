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
# <span data-ttu-id="48231-103">Informationen zur Problembehandlung für Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="48231-103">Troubleshooting Information for the Application Virtualization Server</span></span>


<span data-ttu-id="48231-104">Dieses Thema enthält Informationen, die Sie zur Behebung verschiedener Probleme auf den Application Virtualization (App-V)-Servern verwenden können.</span><span class="sxs-lookup"><span data-stu-id="48231-104">This topic includes information that you can use to troubleshoot various issues on the Application Virtualization (App-V) Servers.</span></span>

## <span data-ttu-id="48231-105">Warnungsmeldung 25017 im Setup Protokoll nach der Installation des Servers</span><span class="sxs-lookup"><span data-stu-id="48231-105">Warning Message 25017 in Setup Log After Installing the Server</span></span>


<span data-ttu-id="48231-106">Nach der Installation finden Sie möglicherweise die folgende Meldung im Server Setup-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="48231-106">You might find the following message in the server setup log after installation.</span></span>

*<span data-ttu-id="48231-107">Warnung 25017.</span><span class="sxs-lookup"><span data-stu-id="48231-107">Warning 25017.</span></span> <span data-ttu-id="48231-108">Das Installationsprogramm konnte das Active Directory-Markierungsobjekt für den Server nicht erstellen.</span><span class="sxs-lookup"><span data-stu-id="48231-108">The installation Program could not create the Active Directory marker object for the server.</span></span> <span data-ttu-id="48231-109">Das für die Installation verwendete Konto hatte nicht genügend Rechte zum Schreiben in Active Directory oder Active Directory war nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="48231-109">The account used to install did not have the sufficient rights to write to Active Directory or Active Directory was unavailable.</span></span>*

<span data-ttu-id="48231-110">Das Installationsprogramm für App-V Management oder Streaming Server erstellt einen Dienstverbindungspunkt Eintrag unter dem Computerobjekt in den Active Directory-Domänendiensten (Adds), der dem Computer entspricht, auf dem der Server installiert ist, wenn das zum Ausführen des Installationsprogramms verwendete Konto über die entsprechenden Rechte verfügt.</span><span class="sxs-lookup"><span data-stu-id="48231-110">The App-V Management or Streaming Server installer creates a Service Connection Point entry under the Computer object in Active Directory Domain Services (ADDS) that corresponds to the computer on which the server is installed if the account used to run the installer has the appropriate rights.</span></span> <span data-ttu-id="48231-111">Wenn Sie diesen Eintrag nicht erstellen, kann die Installation nicht fehlschlagen, was sonst die Funktionsweise des Produkts beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="48231-111">Failure to create this entry will not cause the install to fail and this should not otherwise affect the functioning of the product.</span></span> <span data-ttu-id="48231-112">Der wahrscheinlichste Grund für einen Fehler besteht darin, dass das zum Ausführen der Installation verwendete Benutzerkonto nicht über die erforderlichen Rechte zum Schreiben in Adds verfügt.</span><span class="sxs-lookup"><span data-stu-id="48231-112">The likely cause of any failure is that the user account used to run the install did not have sufficient rights to write to ADDS.</span></span> <span data-ttu-id="48231-113">Obwohl das Registrieren des App-v-Servers in Adds optional ist, ist es in einem solchen Fall für zentralisierte Verwaltungstools möglich, den App-v-Server für Inventar-und Verwaltungszwecke zu finden.</span><span class="sxs-lookup"><span data-stu-id="48231-113">Although registering the App-V server in ADDS is optional, one benefit of doing so enables centralized management tools to locate the App-V server for inventory and management purposes.</span></span>

## <span data-ttu-id="48231-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="48231-114">Related topics</span></span>


[<span data-ttu-id="48231-115">Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="48231-115">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





