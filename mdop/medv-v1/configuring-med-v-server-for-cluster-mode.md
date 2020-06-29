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
# <span data-ttu-id="c649f-103">Konfigurieren von MED-V-Server für den Clustermodus</span><span class="sxs-lookup"><span data-stu-id="c649f-103">Configuring MED-V Server for Cluster Mode</span></span>


<span data-ttu-id="c649f-104">Sie können den MED-V-Server im Clustermodus konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c649f-104">You can configure the MED-V server in cluster mode.</span></span> <span data-ttu-id="c649f-105">Im Clustermodus werden zwei Server verwendet, und alle Dateien, die als Gegenüberstellung zu beiden Servern identifiziert werden, werden in einem Dateisystemgespeichert.</span><span class="sxs-lookup"><span data-stu-id="c649f-105">In cluster mode, two servers are used and all files identified as mutual to both servers are placed on a file system.</span></span> <span data-ttu-id="c649f-106">Der Server greift auf die Dateien aus dem Dateisystem zu, anstatt die Dateien lokal zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c649f-106">The server accesses the files from the file system rather than storing the files locally.</span></span>

## <a href="" id="bkmk-howtoconfigurethemedvserverinclustermode"></a>


**<span data-ttu-id="c649f-107">So konfigurieren Sie den MED-V-Server im Clustermodus</span><span class="sxs-lookup"><span data-stu-id="c649f-107">To configure the MED-V server in cluster mode</span></span>**

1.  <span data-ttu-id="c649f-108">Installieren und konfigurieren Sie MED-V auf einem der Server.</span><span class="sxs-lookup"><span data-stu-id="c649f-108">Install and configure MED-V on one of the servers.</span></span>

2.  <span data-ttu-id="c649f-109">Erstellen Sie ein freigegebenes Netzwerk an einem zentralen Ort, an dem alle Server darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="c649f-109">Create a shared network in a central location where all of the servers can access it.</span></span>

3.  <span data-ttu-id="c649f-110">Kopieren Sie den Inhalt des \* &lt; INSTALLDIR &gt; /Servers/ConfigurationServer\* -Ordners in das freigegebene Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c649f-110">Copy the contents of the *&lt;InstallDir&gt;/Servers/ConfigurationServer* folder to the shared network.</span></span>

4.  <span data-ttu-id="c649f-111">Installieren Sie den MED-V-Server auf allen benannten Servern.</span><span class="sxs-lookup"><span data-stu-id="c649f-111">Install MED-V server on all designated servers.</span></span>

5.  <span data-ttu-id="c649f-112">Weisen Sie im freigegebenen Netzwerk vollständigen Zugriff auf alle MED-V Server-Systemkonten zu.</span><span class="sxs-lookup"><span data-stu-id="c649f-112">On the shared network, assign full access to all MED-V server system accounts.</span></span>

6.  <span data-ttu-id="c649f-113">Gehen Sie auf jedem Server wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="c649f-113">On each server, do the following:</span></span>

    1.  <span data-ttu-id="c649f-114">Legen Sie in der Datei \* &lt; INSTALLDIR &gt; /Server/ServerConfiguration.xml\* den Wert von \* &lt; storePath &gt; \* auf den freigegebenen Netzwerkpfad.</span><span class="sxs-lookup"><span data-stu-id="c649f-114">In the *&lt;InstallDir&gt;/Servers/ServerConfiguration.xml* file, set the value of *&lt;StorePath&gt;* to the shared network path.</span></span>

    2.  <span data-ttu-id="c649f-115">Kopieren Sie die \* &lt; InstsallDir- &gt; /Server/KeyPair.xml\* Datei vom ursprünglichen Server auf alle MED-V-Server.</span><span class="sxs-lookup"><span data-stu-id="c649f-115">Copy the *&lt;InstsallDir&gt;/Servers/KeyPair.xml* file from the original server to all MED-V servers.</span></span>

    3.  <span data-ttu-id="c649f-116">Starten Sie den MED-V-Dienst erneut.</span><span class="sxs-lookup"><span data-stu-id="c649f-116">Restart the MED-V service.</span></span>

<span data-ttu-id="c649f-117">**Hinweis**  Wenn alle Server über die gleichen lokalen Einstellungen verfügen (wie Abhör Anschlüsse, IIS-Server, Verwaltungsberechtigungen, Berichtsdatenbank usw.), können die \* &lt; INSTALLDIR- &gt; /Server/ServerSettings.xml\* auch von allen Servern freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c649f-117">**Note** If all servers have the same local settings (such as listening ports, IIS server, management permissions, report database, and so on), the *&lt;InstallDir&gt;/Servers/ServerSettings.xml* can be shared by all servers as well.</span></span>

 

## <span data-ttu-id="c649f-118">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c649f-118">Related topics</span></span>


[<span data-ttu-id="c649f-119">Planen und Entwerfen der MED-V-Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="c649f-119">MED-V Infrastructure Planning and Design</span></span>](med-v-infrastructure-planning-and-design.md)

 

 





