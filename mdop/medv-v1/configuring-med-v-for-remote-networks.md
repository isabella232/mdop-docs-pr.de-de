---
title: Konfigurieren von MED-V für Remote-Netzwerke
description: Konfigurieren von MED-V für Remote-Netzwerke
author: dansimp
ms.assetid: 4d2f0081-622f-4a6f-8d73-f8c2108036e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328376046ee5213f3d5bb09be7adf8c81f8508b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811926"
---
# <span data-ttu-id="e18f3-103">Konfigurieren von MED-V für Remote-Netzwerke</span><span class="sxs-lookup"><span data-stu-id="e18f3-103">Configuring MED-V for Remote Networks</span></span>


<span data-ttu-id="e18f3-104">Sie können MED-V so konfigurieren, dass Sie in einem Netzwerk, Remote oder sowohl aus dem Netzwerk als auch aus der Ferne aus arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e18f3-104">You can configure MED-V to work from inside a network, remotely, or both from inside the network and remotely.</span></span>

## <a href="" id="bkmk-howtoconfiguremedvtoworkfrominsideanetworkorremotely"></a>


**<span data-ttu-id="e18f3-105">So konfigurieren Sie MED-V für die Arbeit in einem Netzwerk</span><span class="sxs-lookup"><span data-stu-id="e18f3-105">To configure MED-V to work from inside a network</span></span>**

-   <span data-ttu-id="e18f3-106">Konfigurieren Sie einen MED-V-Server und die Bildverteilung innerhalb des Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="e18f3-106">Configure a MED-V server and image distribution inside the network.</span></span>

**<span data-ttu-id="e18f3-107">So konfigurieren Sie MED-V für die Remote Arbeit</span><span class="sxs-lookup"><span data-stu-id="e18f3-107">To configure MED-V to work remotely</span></span>**

1.  <span data-ttu-id="e18f3-108">Konfigurieren Sie einen MED-V-Server und einen Bildverteilungsserver, auf die über das Internet zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e18f3-108">Configure a MED-V server and an image distribution server that are accessible from the Internet.</span></span>

2.  <span data-ttu-id="e18f3-109">Konfigurieren Sie bei Bedarf ein Umkreisnetzwerk (auch als DMZ bezeichnet) Reverse-Proxy.</span><span class="sxs-lookup"><span data-stu-id="e18f3-109">If needed, configure a perimeter network (also called a DMZ) reverse proxy.</span></span>

3.  <span data-ttu-id="e18f3-110">Legen Sie die Authentifizierungsmethode in der *ClientSettings.xml* -Datei fest, die im Ordner **Servers\\Configuration Server\\** zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="e18f3-110">Set the authentication method, in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

**<span data-ttu-id="e18f3-111">So konfigurieren Sie MED-V für die Arbeit in einem Netzwerk und Remote</span><span class="sxs-lookup"><span data-stu-id="e18f3-111">To configure MED-V to work both from inside a network and remotely</span></span>**

1.  <span data-ttu-id="e18f3-112">Konfigurieren Sie einen MED-V-Server und einen Bildverteilungsserver im Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e18f3-112">Configure a MED-V server and image distribution server inside the network.</span></span>

2.  <span data-ttu-id="e18f3-113">Stellen Sie sicher, dass auf die Server über das Internet zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e18f3-113">Ensure that the servers are accessible from the Internet.</span></span>

3.  <span data-ttu-id="e18f3-114">Konfigurieren Sie die DNS-Auflösung so, dass Sie, wenn der Client versucht, eine Verbindung mit einem Server herzustellen, automatisch eine Verbindung mit dem richtigen Server (im Netzwerk oder über das Internet) herstellt, der auf dem Clientstandort basiert.</span><span class="sxs-lookup"><span data-stu-id="e18f3-114">Configure the DNS resolution so that when the client attempts to connect to a server, it automatically connects to the correct server (within the network or over the Internet) based on the client location.</span></span>

4.  <span data-ttu-id="e18f3-115">Konfigurieren Sie bei Bedarf einen Reverse-Proxy für Umkreisnetzwerke.</span><span class="sxs-lookup"><span data-stu-id="e18f3-115">If needed, configure a perimeter network reverse proxy.</span></span>

5.  <span data-ttu-id="e18f3-116">Legen Sie die Authentifizierungsmethode in der *ClientSettings.xml* -Datei fest, die im Ordner **Servers\\Configuration Server\\** zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="e18f3-116">Set the authentication method, in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

<span data-ttu-id="e18f3-117">**Hinweis**  Bei der Anwendung neuer Einstellungen muss der Dienst neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="e18f3-117">**Note** When applying new settings, the service must be restarted.</span></span>

 

-   <span data-ttu-id="e18f3-118">Sie können das IIS-Authentifizierungsschema auf eine der folgenden Optionen ändern: Basic, Digest, NTLM oder Negotiate.</span><span class="sxs-lookup"><span data-stu-id="e18f3-118">You can change the IIS authentication scheme to one of the following: BASIC, DIGEST, NTLM, or NEGOTIATE.</span></span> <span data-ttu-id="e18f3-119">Der Standardwert ist Negotiate und verwendet den folgenden Eintrag:</span><span class="sxs-lookup"><span data-stu-id="e18f3-119">The default is NEGOTIATE and uses the following entry:</span></span>

    ```xml
    <ImageDistribution>
    <!-- The authentication used for image download. Basic and digest authentication should be used only under SSL.-->
       <!-- The line below can be one of the following: -->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_BASIC</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_DIGEST</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NTLM</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME-->
       <Authentication type="Kidaro.Foundation.Bits.BG_AUTH_SCHEME">
          <BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME>
       </Authentication>
    </ImageDistribution>
    ```

## <span data-ttu-id="e18f3-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e18f3-120">Related topics</span></span>


[<span data-ttu-id="e18f3-121">Planen und Entwerfen der MED-V-Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="e18f3-121">MED-V Infrastructure Planning and Design</span></span>](med-v-infrastructure-planning-and-design.md)

 

 





