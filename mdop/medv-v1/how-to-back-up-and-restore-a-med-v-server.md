---
title: So sichern Sie einen MED-V-Server und stellen ihn wieder her
description: So sichern Sie einen MED-V-Server und stellen ihn wieder her
author: dansimp
ms.assetid: 8d05e3a4-279b-4ce6-a319-8a09e7a30c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d51cfe3727896ed68a1fd67441174a294a1073cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809745"
---
# <span data-ttu-id="9f5e9-103">So sichern Sie einen MED-V-Server und stellen ihn wieder her</span><span class="sxs-lookup"><span data-stu-id="9f5e9-103">How to Back Up and Restore a MED-V Server</span></span>


<span data-ttu-id="9f5e9-104">XML-Dateien, die sich auf dem Server befinden, können gesichert und dann wiederhergestellt werden, wenn Daten auf dem Server verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="9f5e9-104">XML files located on the server can be backed up and then restored in case of loss of data on the server.</span></span>

**<span data-ttu-id="9f5e9-105">So sichern Sie einen MED-V-Server</span><span class="sxs-lookup"><span data-stu-id="9f5e9-105">To back up a MED-V server</span></span>**

-   <span data-ttu-id="9f5e9-106">Sichern Sie die folgenden Dateien in \* &lt; INSTALLDIR &gt; \\Servers\\ConfigurationServer\*:</span><span class="sxs-lookup"><span data-stu-id="9f5e9-106">Back up the following files, located in *&lt;InstallDir&gt;\\Servers\\ConfigurationServer*:</span></span>

    <span data-ttu-id="9f5e9-107">**Hinweis**  Wenn die Konfiguration von der Standardeinstellung geändert wurde, werden die Dateien möglicherweise an einem anderen Speicherort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9f5e9-107">**Note** If the configuration has been changed from the default, the files might be stored in a different location.</span></span>

     

    -   <span data-ttu-id="9f5e9-108">ClientPolicy.xml</span><span class="sxs-lookup"><span data-stu-id="9f5e9-108">ClientPolicy.xml</span></span>

    -   <span data-ttu-id="9f5e9-109">ClientSettings.xml</span><span class="sxs-lookup"><span data-stu-id="9f5e9-109">ClientSettings.xml</span></span>

    -   <span data-ttu-id="9f5e9-110">ConfigurationFiles.xml</span><span class="sxs-lookup"><span data-stu-id="9f5e9-110">ConfigurationFiles.xml</span></span>

    -   <span data-ttu-id="9f5e9-111">OrganizationPolicy.xml</span><span class="sxs-lookup"><span data-stu-id="9f5e9-111">OrganizationPolicy.xml</span></span>

    -   <span data-ttu-id="9f5e9-112">WorkspaceKeys.xml</span><span class="sxs-lookup"><span data-stu-id="9f5e9-112">WorkspaceKeys.xml</span></span>

    <span data-ttu-id="9f5e9-113">**Hinweis**  Die ServerSettings.xml-Datei kann ebenfalls gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="9f5e9-113">**Note** The ServerSettings.xml file can be backed up as well.</span></span> <span data-ttu-id="9f5e9-114">Wenn jedoch eine bestimmte Konfiguration geändert wurde (beispielsweise auf dem ursprünglichen Server befindet sich das MED-V VMS-Verzeichnis in "*C:\\Vms*", und ein solches Verzeichnis ist auf dem neuen Server nicht vorhanden), kann dies zu einem Fehler führen.</span><span class="sxs-lookup"><span data-stu-id="9f5e9-114">However, if a specific configuration has been changed (for example, on the original server, the MED-V VMS directory is located in "*C:\\Vms*" and such a directory does not exist on the new server), it can cause an error.</span></span>

     

**<span data-ttu-id="9f5e9-115">So stellen Sie einen MED-V-Server wieder her</span><span class="sxs-lookup"><span data-stu-id="9f5e9-115">To restore a MED-V server</span></span>**

1.  <span data-ttu-id="9f5e9-116">Installieren Sie einen neuen MED-V-Server.</span><span class="sxs-lookup"><span data-stu-id="9f5e9-116">Install a new MED-V server.</span></span>

2.  <span data-ttu-id="9f5e9-117">Kopieren Sie die Sicherungsdateien in das folgende Verzeichnis:</span><span class="sxs-lookup"><span data-stu-id="9f5e9-117">Copy the backup files to the following directory:</span></span>

    *<span data-ttu-id="9f5e9-118">&lt;INSTALLDIR &gt; \\Servers\\ConfigurationServer</span><span class="sxs-lookup"><span data-stu-id="9f5e9-118">&lt;InstallDir&gt;\\Servers\\ConfigurationServer</span></span>*

3.  <span data-ttu-id="9f5e9-119">Starten Sie den MED-V-Dienst erneut.</span><span class="sxs-lookup"><span data-stu-id="9f5e9-119">Restart the MED-V service.</span></span>

 

 





