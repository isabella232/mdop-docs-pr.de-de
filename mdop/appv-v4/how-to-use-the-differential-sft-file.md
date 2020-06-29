---
title: So verwenden Sie die differenzielle SFT-Datei
description: So verwenden Sie die differenzielle SFT-Datei
author: dansimp
ms.assetid: 607e30fd-2f0e-4e2f-b669-0b3f010aebb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 85cc45f9665569d77fcf275db6dbc080eb919229
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806687"
---
# <span data-ttu-id="62986-103">So verwenden Sie die differenzielle SFT-Datei</span><span class="sxs-lookup"><span data-stu-id="62986-103">How to Use the Differential SFT File</span></span>


<span data-ttu-id="62986-104">Beim Sequenzieren einer Anwendung erstellt der Microsoft Application Virtualization (App-V)-Sequenzer SFT-Dateien (. SFT), um alle Dateien der virtuellen Anwendung und die Konfigurationsinformationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="62986-104">When sequencing an application, the Microsoft Application Virtualization (App-V) Sequencer creates SFT files (.sft) to store all of the virtual application’s files content and configuration information.</span></span> <span data-ttu-id="62986-105">In Version 4.5 von App-V wurde die differenzielle SFT-Datei (. dsft) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="62986-105">In version4.5 of App-V, the Differential SFT (.dsft) file has been introduced.</span></span> <span data-ttu-id="62986-106">Nachdem Sie den Sequencer zum Erstellen eines Upgrades für ein vorhandenes Paket verwendet haben, können Sie diese Datei generieren, um nur die Unterschiede zwischen dem ursprünglichen sequenzierten Anwendungspaket und der neuen Version zu speichern.</span><span class="sxs-lookup"><span data-stu-id="62986-106">After using the Sequencer to create an upgrade for an existing package, you can choose to generate this file to store only the differences between the original sequenced application package and the new version.</span></span> <span data-ttu-id="62986-107">Sie ist daher deutlich kleiner als die vollständige SFT-Datei für die neue Version der Anwendung und reduziert die Auswirkungen des Sendens von Paket Updates über Netzwerkverbindungen mit niedriger Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="62986-107">It is therefore much smaller than the full SFT file would be for the new version of the application and reduces the impact of sending package updates over low-bandwidth network connections.</span></span> <span data-ttu-id="62986-108">Die Verwendung wird jedoch nur in bestimmten eingeschränkten Situationen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="62986-108">However, its use is supported only in certain restricted situations.</span></span> <span data-ttu-id="62986-109">Dieses Feature sollte speziell verwendet werden, wenn Sie ein ESD-System (Electronic Software Distribution) verwenden, um eine Gruppe von Benutzern mit einem lokalen Dateiserver über eine Verbindung mit niedriger Bandbreite zu verwalten, und Sie keine App-V-Streaming-Server verwenden.</span><span class="sxs-lookup"><span data-stu-id="62986-109">This feature was intended to be used specifically where you are using an electronic software distribution (ESD) system to manage a group of users with a local file server over a low-bandwidth connection and you are not using App-V streaming servers.</span></span>

<span data-ttu-id="62986-110">Sie müssen die differenzielle SFT-Datei nicht verwenden, wenn Sie die Konfigurations Manager2007 verwenden, um die Benutzer zu verwalten, da Configuration Manager Unterstützung für Bereitstellungen mit niedriger Bandbreite bietet, die bereits integriert sind.</span><span class="sxs-lookup"><span data-stu-id="62986-110">You do not need to use the Differential SFT file if you are using Configuration Manager2007 to manage the users, because Configuration Manager has support for low-bandwidth deployments already built in.</span></span> <span data-ttu-id="62986-111">Darüber hinaus ist es nicht erforderlich, wenn Sie Application Virtualization (App-V)-Verwaltungs-oder Streamingserver mit aktivem Upgrade verwenden, da der Client nur die Unterschiede zwischen den alten und den neuen Paketversionen abruft.</span><span class="sxs-lookup"><span data-stu-id="62986-111">It is also not required if you are using Application Virtualization (App-V) Management or Streaming Servers with Active Upgrade because the client will retrieve only the differences between the old and new package versions.</span></span>

<span data-ttu-id="62986-112">Das folgende Verfahren zeigt, wie Sie die mkdiffpkg.exe verwenden, die in der Sequencer-Installation enthalten ist, um die differenzielle SFT-Datei nach Abschluss des Upgrades des virtuellen Anwendungspakets zu erstellen und die differenzielle SFT-Datei bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="62986-112">The following procedure shows how to use the mkdiffpkg.exe that is included in the Sequencer installation to create the Differential SFT file, after completing the upgrade of the virtual application package, and to deploy the Differential SFT file.</span></span> <span data-ttu-id="62986-113">Wenn Sie dieses Verfahren durchführen, können Sie sicherstellen, dass der Client, wenn das Paket auf dem Clientcomputer irgendwie entladen wird, beim nächsten Versuch des Benutzers, die Anwendung auszuführen, auf die Außerkraftsetzungs-URL zurückgreift, die für das Streamen des vollständigen Pakets v2. SFT aus der lokalen Dateifreigabe festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="62986-113">Completing this procedure helps ensure that if the package is somehow unloaded from the client computer, the next time the user tries to run the application, the client will fall back to the override URL, which is set to stream the full package V2.sft from the local file share.</span></span> <span data-ttu-id="62986-114">Dadurch wird verhindert, dass der Benutzer beim Starten der Anwendung fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="62986-114">This will avoid any failure for the user when starting the application.</span></span> <span data-ttu-id="62986-115">Wenn der gesamte Client beschädigt wird oder deinstalliert wird, empfiehlt es sich, das ESD-System so zu konfigurieren, dass die Vollversion des aktualisierten Pakets, v2. SFT, für den Client bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="62986-115">If the entire client becomes corrupted or is uninstalled, it is recommended that the ESD system be configured to deploy the full version of the upgraded package, V2.sft, to the client.</span></span>

<span data-ttu-id="62986-116">Weitere Informationen zum Aktualisieren eines Pakets finden Sie unter "Aktualisieren einer vorhandenen virtuellen Anwendung" im App-v 4.5-Betriebshandbuch unter</span><span class="sxs-lookup"><span data-stu-id="62986-116">For more information about upgrading a package, see “How to Upgrade an Existing Virtual Application” in the App-V4.5 Operations Guide at</span></span> <https://go.microsoft.com/fwlink/?LinkId=133129>

<span data-ttu-id="62986-117">**Hinweis**  Voraussetzung ist, dass alle Benutzer Computer, für die das ESD-Ziel vorgesehen ist, die v1. SFT-Datei vollständig in den lokalen Cache geladen haben und das Dateistreaming auf allen Computern aktiviert sein muss.</span><span class="sxs-lookup"><span data-stu-id="62986-117">**Note** As a prerequisite, all user computers being targeted by the ESD must have the V1.sft file fully loaded into their local cache, and file streaming must be enabled on all computers.</span></span>

 

**<span data-ttu-id="62986-118">So verwenden Sie die differenzielle SFT-Datei</span><span class="sxs-lookup"><span data-stu-id="62986-118">To use the Differential SFT file</span></span>**

1.  <span data-ttu-id="62986-119">Melden Sie sich mit einem Konto mit Administratorrechten beim Sequencer-Computer an.</span><span class="sxs-lookup"><span data-stu-id="62986-119">Log on to the Sequencer computer by using an account with administrator rights.</span></span> <span data-ttu-id="62986-120">Öffnen Sie das ursprüngliche Paket (v1) für das Upgrade im Sequencer, und aktualisieren Sie dann das Paket auf die neue Version (v2), und speichern Sie es als neues v2. SFT.</span><span class="sxs-lookup"><span data-stu-id="62986-120">Open the original package (V1) for upgrade in the Sequencer, and then upgrade the package to the new version (V2) and save it as a new V2.sft.</span></span>

2.  <span data-ttu-id="62986-121">Öffnen Sie ein Befehlsfenster im App-v 4.5 Sequencer-Installationsordner, und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="62986-121">Open a command window in the App-V4.5 Sequencer installation folder, and run the following command:</span></span>

    `“mkdiffpkg.exe V2.sft V2.dsft”`

3.  <span data-ttu-id="62986-122">Kopieren Sie mithilfe des ESD-Systems oder eines anderen Dateikopiervorgangs die vollständige v2-Paketinhalts Datei v2. SFT in eine lokale Dateifreigabe, auf die die Benutzer Computer in einer gut verbundenen Netzwerkverbindung zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="62986-122">Using the ESD system or other file copy process, copy the full V2 package content file, V2.sft, to a local file share that is accessible to the user computers on a well-connected network connection.</span></span>

4.  <span data-ttu-id="62986-123">Legen Sie mithilfe des ESD-Systems eine Kopie der differenziellen SFT-Datei v2. dsft auf jedem Benutzer Computer ab.</span><span class="sxs-lookup"><span data-stu-id="62986-123">Using the ESD system, place a copy of the Differential SFT file, V2.dsft, on each user computer.</span></span>

5.  <span data-ttu-id="62986-124">Führen Sie zum Importieren der Datei v2. dsft den folgenden SFTMIME-Befehl auf jedem Benutzer Computer aus:</span><span class="sxs-lookup"><span data-stu-id="62986-124">To import the V2.dsft file, run the following SFTMIME command on each user computer:</span></span>

    `“SFTMIME load package:<package name> /SFTPATH <path to V2.dsft>”`

6.  <span data-ttu-id="62986-125">Führen Sie auf jedem Benutzer Computer den folgenden SFTMIME-Befehl aus, um die override-URL so festzulegen, dass Sie auf die v2. SFT-Datei verweist:</span><span class="sxs-lookup"><span data-stu-id="62986-125">Run the following SFTMIME command on each user computer to set the override URL to point to the V2.sft file:</span></span>

    `“SFTMIME configure package:<package name> /OverrideURL FILE://<network path to V2.sft>”`

**<span data-ttu-id="62986-126">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="62986-126">Note</span></span>**  
-   <span data-ttu-id="62986-127">Differenzielle SFT-Dateien müssen auf Clients in der richtigen Reihenfolge angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="62986-127">Differential SFT files must be applied to clients in the correct order.</span></span> <span data-ttu-id="62986-128">Beispielsweise muss v2. dsft auf eine v1-Anwendung angewendet werden, bevor v3. dsft angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="62986-128">For example, V2.dsft must be applied to a V1 application before V3.dsft is applied.</span></span>

-   <span data-ttu-id="62986-129">Die **Microsoft Windows Installer-Paketfunktion (MSI)** im Sequencer kann nicht mit der differenziellen SFT-Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62986-129">The **Generate Microsoft Windows Installer (MSI) Package** capability in the Sequencer cannot be used with the Differential SFT file.</span></span>

 

## <span data-ttu-id="62986-130">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="62986-130">Related topics</span></span>


[<span data-ttu-id="62986-131">Erstellen oder Aktualisieren virtueller Anwendungen mit dem App-V-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="62986-131">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





