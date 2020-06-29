---
title: Anwenden von Netzwerkeinstellungen auf einen MED-V-Arbeitsbereich
description: Anwenden von Netzwerkeinstellungen auf einen MED-V-Arbeitsbereich
author: dansimp
ms.assetid: 641f46b3-a56f-478a-823b-1d90aa1716b3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a13227518945e74be9e4b3772af97eadbce3fc4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811803"
---
# <span data-ttu-id="095c6-103">Anwenden von Netzwerkeinstellungen auf einen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="095c6-103">How to Apply Network Settings to a MED-V Workspace</span></span>


<span data-ttu-id="095c6-104">Administratoren können die Netzwerkeinstellungen für jeden MED-V-Arbeitsbereich definieren.</span><span class="sxs-lookup"><span data-stu-id="095c6-104">Administrators can define the network settings for each MED-V workspace.</span></span>

<span data-ttu-id="095c6-105">Alle Netzwerkeinstellungen sind im **Richtlinien** Modul auf der Registerkarte **Netzwerk** konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="095c6-105">All network settings are configured in the **Policy** module, on the **Network** tab.</span></span>

**<span data-ttu-id="095c6-106">So wenden Sie Netzwerkeinstellungen auf einen MED-V-Arbeitsbereich an</span><span class="sxs-lookup"><span data-stu-id="095c6-106">To apply network settings to a MED-V workspace</span></span>**

1.  <span data-ttu-id="095c6-107">Klicken Sie auf den MED-V-Arbeitsbereich, den Sie konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="095c6-107">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="095c6-108">Konfigurieren Sie im Bereich " **Netzwerk** " die Einstellungen, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="095c6-108">In the **Network** pane, configure the settings as described in the following table.</span></span>

3.  <span data-ttu-id="095c6-109">Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.</span><span class="sxs-lookup"><span data-stu-id="095c6-109">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="095c6-110">MED-V Workspace-Netzwerkeigenschaften</span><span class="sxs-lookup"><span data-stu-id="095c6-110">MED-V Workspace Network Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="095c6-111">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="095c6-111">Property</span></span></th>
<th align="left"><span data-ttu-id="095c6-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="095c6-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="095c6-113">TCP/IP-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="095c6-113">TCP/IP Properties</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="095c6-114">Verwenden Sie die IP-Adresse (NAT) </strong> des Hosts – der Arbeitsbereich verwendet NAT, um die IP-Adresse des Hosts für ausgehenden Datenverkehr freizugeben.</span><span class="sxs-lookup"><span data-stu-id="095c6-114">Use host's IP address (NAT)</strong>—The workspace will use NAT to share the host's IP for outgoing traffic.</span></span></p></li>
<li><p><strong><span data-ttu-id="095c6-115">Verwenden Sie eine andere IP-Adresse als Host (Bridge) </strong> – der MED-V-Arbeitsbereich hat eine eigene Netzwerkadresse, die normalerweise über DHCP abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="095c6-115">Use different IP address than host (Bridge)</strong>—The MED-V workspace will have its own network address, usually obtained via DHCP.</span></span></p></li>
</ul>
<p><span data-ttu-id="095c6-116">Aktivieren Sie das <strong> Kontrollkästchen mehrere Adapter in den Arbeitsbereich zuordnen </strong> , wenn auf dem Hostcomputer mehrere Adapter vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="095c6-116">Select the <strong>Map multiple adapters into Workspace</strong> check box when the host computer has multiple adapters.</span></span> <span data-ttu-id="095c6-117">Es wird empfohlen, diese Konfiguration zu verwenden, wenn der Host zwischen verschiedenen Netzwerken mit unterschiedlichen Adaptern wechselt.</span><span class="sxs-lookup"><span data-stu-id="095c6-117">It is recommended to use this configuration when the host moves between different networks using different adapters.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="095c6-118">DNS-Server</span><span class="sxs-lookup"><span data-stu-id="095c6-118">DNS Server</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="095c6-119">Nicht ändern </strong> – die DNS-Einstellungen, die auf dem virtuellen Computer mit dem MED-V Workspace festgesetzt werden, werden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="095c6-119">Don't change</strong>—DNS settings that are set within the MED-V workspace virtual machine will not be changed.</span></span></p></li>
<li><p><strong><span data-ttu-id="095c6-120">Verwenden der Host-DNS-Adresse </strong> – die DNS-Einstellungen für den MED-V-Arbeitsbereich werden so synchronisiert, dass Sie den Einstellungen des Hosts entsprechen.</span><span class="sxs-lookup"><span data-stu-id="095c6-120">Use Host's DNS address</strong>—MED-V workspace DNS settings will be synchronized to match the host's settings.</span></span> <span data-ttu-id="095c6-121">Die DNS-Synchronisierung ist dynamisch.</span><span class="sxs-lookup"><span data-stu-id="095c6-121">The DNS synchronization is dynamic.</span></span> <span data-ttu-id="095c6-122">Sie wird in regelmäßigen Abständen mit dem Host synchronisiert, sodass Sie im MED-V-Arbeitsbereich dynamisch geändert wird, wenn Sie auf dem Host geändert wird.</span><span class="sxs-lookup"><span data-stu-id="095c6-122">It is synchronized periodically with the host so that if it is changed on the host, it will change dynamically in the MED-V workspace.</span></span></p></li>
<li><p><strong><span data-ttu-id="095c6-123">Verwenden bestimmter DNS-Adressen </strong> – der MED-V-Arbeitsbereich verwendet ein bestimmtes DNS, wie angegeben.</span><span class="sxs-lookup"><span data-stu-id="095c6-123">Use specific DNS addresses</strong>—The MED-V workspace will use a specific DNS, as specified.</span></span></p>
<p><span data-ttu-id="095c6-124"><strong> </strong> Geben Sie in den Feldern Primär und <strong> Sekundär </strong> die primären und sekundären DNS-Adressen ein.</span><span class="sxs-lookup"><span data-stu-id="095c6-124">In the <strong>Primary</strong> and <strong>Secondary</strong> fields, enter the primary and secondary DNS addresses.</span></span></p>
<p><span data-ttu-id="095c6-125">Aktivieren Sie das <strong> Kontrollkästchen Host-DNS-Adressen anfügen </strong> , um den Host an die konfigurierten DNS-Adressen anzufügen.</span><span class="sxs-lookup"><span data-stu-id="095c6-125">Select the <strong>Append Host's DNS addresses</strong> check box to append the host to the configured DNS addresses.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="095c6-126">Zuweisen von DNS-Suffixen</span><span class="sxs-lookup"><span data-stu-id="095c6-126">Assign DNS Suffixes</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="095c6-127">Weisen Sie die folgenden Suffixe </strong> zu: Aktivieren Sie dieses Kontrollkästchen, um bestimmte DNS-Suffixe zuzuweisen; geben Sie im Feld ein Suffix oder mehrere Suffixe durch Kommas getrennt ein.</span><span class="sxs-lookup"><span data-stu-id="095c6-127">Assign the following suffixes</strong>—Select this check box to assign specific DNS suffixes; in the box, enter a suffix or multiple suffixes separated by commas.</span></span></p></li>
<li><p><strong><span data-ttu-id="095c6-128">Anfügen von Host Suffixen </strong> – Aktivieren Sie dieses Kontrollkästchen, um die Host Suffixe an die DNS-Adresse anzufügen.</span><span class="sxs-lookup"><span data-stu-id="095c6-128">Append host suffixes</strong>—Select this check box to append the host suffixes to the DNS address.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="095c6-129">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="095c6-129">Related topics</span></span>


[<span data-ttu-id="095c6-130">Erstellen eines MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="095c6-130">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="095c6-131">Über die Benutzeroberfläche der MED-V-Management-Konsole</span><span class="sxs-lookup"><span data-stu-id="095c6-131">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

 

 





