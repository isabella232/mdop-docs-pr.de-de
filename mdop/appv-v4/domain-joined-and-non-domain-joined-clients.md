---
title: In die Domäne eingebundene und keiner Domäne beigetretene Clients
description: In die Domäne eingebundene und keiner Domäne beigetretene Clients
author: dansimp
ms.assetid: a935dc98-de60-45f3-ab74-2444ce082e88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4385ab3f26bb867dd649fe768e1500c9d015ffa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808872"
---
# <span data-ttu-id="1f4fa-103">In die Domäne eingebundene und keiner Domäne beigetretene Clients</span><span class="sxs-lookup"><span data-stu-id="1f4fa-103">Domain-Joined and Non-Domain-Joined Clients</span></span>


<span data-ttu-id="1f4fa-104">Der App-V-Desktop Client kann so konfiguriert werden, dass die Verbindung zu einem Netzwerk ermöglicht wird, unabhängig davon, ob der Client einer Domäne beigetreten ist oder nicht der Domäne beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1f4fa-104">The App-V Desktop Client can be configured to allow connection to a network regardless of whether the client is domain joined or non-domain joined.</span></span>

## <span data-ttu-id="1f4fa-105">Mit der Domäne verbundene Clients</span><span class="sxs-lookup"><span data-stu-id="1f4fa-105">Domain-Joined Clients</span></span>


<span data-ttu-id="1f4fa-106">Clients, die Domänen verbunden sind, aber außerhalb des internen Netzwerks, können über eine VPN-Verbindung mit der App-V-Infrastruktur kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1f4fa-106">Clients that are domain joined, but outside the internal network, can communicate with the App-V infrastructure by using a VPN connection.</span></span> <span data-ttu-id="1f4fa-107">Wenn Sie Benutzern die Möglichkeit geben möchten, das interne Netzwerk zu belassen, aber dennoch in einer App-V-Infrastruktur zu kommunizieren, erfordert Ihre Umgebung nur sehr wenig Setup.</span><span class="sxs-lookup"><span data-stu-id="1f4fa-107">When you want to provide users the ability to leave the internal network but still communicate in an App-V infrastructure, your environment requires very little setup.</span></span> <span data-ttu-id="1f4fa-108">Da die Benutzer bereits Teil der Domäne sind, müssen Sie einfach sicherstellen, dass zwischengespeicherte Anmeldeinformationen auf dem Client unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1f4fa-108">Because the users are already part of the domain, you simply need to ensure that Cached Credentials are supported on the client.</span></span> <span data-ttu-id="1f4fa-109">Dies ist die Standardkonfiguration, und alle Änderungen an dieser Einstellung können über Gruppenrichtlinien erfolgen.</span><span class="sxs-lookup"><span data-stu-id="1f4fa-109">This is the default configuration, and any changes to this setting can be accomplished from Group Policies.</span></span>

<span data-ttu-id="1f4fa-110">Wie im Leitfaden zur APP-v-Sicherheit für bewährte Methoden beschrieben, wird der Benutzer versuchen, sein Benutzerticket zur Authentifizierung an die APP-v-Infrastruktur zu senden.</span><span class="sxs-lookup"><span data-stu-id="1f4fa-110">As mentioned in the App-V Security Best Practices Guide, the user will attempt to send their user ticket to the App-V infrastructure for authentication.</span></span> <span data-ttu-id="1f4fa-111">Wenn das Ticket abgelaufen ist, wird es auf die Verwendung von NTLM und die zwischengespeicherten Anmeldeinformationen auf dem Computer zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1f4fa-111">If the ticket is expired, it will revert to using NTLM and the cached credentials on the computer.</span></span> <span data-ttu-id="1f4fa-112">Um Roaming zu ermöglichen, müssen Administratoren sicherstellen, dass der Veröffentlichungsserver, auf den intern zugegriffen wird, mit dem gleichen Namen extern verfügbar ist, damit die Namen ordnungsgemäß aufgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="1f4fa-112">To allow roaming, administrators must ensure that the publishing server being accessed internally is available at the same name externally for the names to resolve properly.</span></span>

## <span data-ttu-id="1f4fa-113">Nicht mit der Domäne verbundene Clients</span><span class="sxs-lookup"><span data-stu-id="1f4fa-113">Non-Domain-Joined Clients</span></span>


<span data-ttu-id="1f4fa-114">Clients, die nicht der Domäne beigetreten sind, aber in der APP-v-Infrastruktur kommunizieren müssen, müssen so konfiguriert werden, dass sichergestellt ist, dass die Authentifizierung für die APP-v-Infrastruktur erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="1f4fa-114">Clients that are non-domain joined but need to communicate in the App-V infrastructure must be configured to ensure that authentication to the App-V infrastructure is successful.</span></span> <span data-ttu-id="1f4fa-115">Der APP-v-Desktop Client lässt keine Eingabeaufforderung für den Veröffentlichungs Aktualisierungsvorgang zu, sodass der Client so konfiguriert sein muss, dass er die richtigen Anmeldeinformationen für den App-V-Verwaltungs Server bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="1f4fa-115">The App-V Desktop Client does not permit prompting for the publishing refresh process, so the client must be configured to present the proper credentials to the App-V Management Server.</span></span>

<span data-ttu-id="1f4fa-116">Der Veröffentlichungsserver, der für die Veröffentlichungsaktualisierung vom nicht für die Domäne verbundenen Client konfiguriert ist, erfordert, dass der externe Name, auf den Clients zugreifen, als allgemeiner Name oder als alternativer Subjektname (Subject Alternate Name, San) auf dem Zertifikat des Veröffentlichungsservers konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="1f4fa-116">The publishing server, which is configured for publishing refresh from the non-domain joined client, requires that the external name that clients access is configured as the common name or a subject alternate name (SAN) on the publishing server’s certificate.</span></span>

## <span data-ttu-id="1f4fa-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1f4fa-117">Related topics</span></span>


[<span data-ttu-id="1f4fa-118">So weisen Sie die richtigen Anmeldeinformationen für Windows Vista zu</span><span class="sxs-lookup"><span data-stu-id="1f4fa-118">How to Assign the Proper Credentials for Windows Vista</span></span>](how-to-assign--the-proper-credentials-for-windows-vista.md)

[<span data-ttu-id="1f4fa-119">So weisen Sie die richtigen Anmeldeinformationen für Windows XP zu</span><span class="sxs-lookup"><span data-stu-id="1f4fa-119">How to Assign the Proper Credentials for Windows XP</span></span>](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





