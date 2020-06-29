---
title: So konfigurieren Sie Webeinstellungen für einen MED-V-Arbeitsbereich
description: So konfigurieren Sie Webeinstellungen für einen MED-V-Arbeitsbereich
author: dansimp
ms.assetid: 9a6cd28f-7e4f-468f-830a-7b1d9abd3af3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 770d3fa9a03c9754db86ca348390d0b916de6d5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812133"
---
# <span data-ttu-id="41316-103">So konfigurieren Sie Webeinstellungen für einen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="41316-103">How to Configure Web Settings for a MED-V Workspace</span></span>


<span data-ttu-id="41316-104">Websites, die nur in älteren Versionen von Internet Explorer angezeigt werden können und die nicht im Hostbetriebssystem vorhanden sind, können in älteren Versionen von Internet Explorer innerhalb des MED-V-Arbeitsbereichs angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="41316-104">Web sites that can only be displayed in older versions of Internet Explorer and that do not exist in the host operating system can be viewed in older versions of Internet Explorer within the MED-V workspace.</span></span> <span data-ttu-id="41316-105">Der Benutzer muss im MED-V-Arbeitsbereich keinen Browser öffnen, um die angegebenen Websites anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="41316-105">The user does not need to open a browser in the MED-V workspace to view the specified Web sites.</span></span> <span data-ttu-id="41316-106">Der Benutzer kann einen Browser auf dem Host öffnen und automatisch an den MED-V-Arbeitsbereich weitergeleitet werden und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="41316-106">The user can open a browser on the host and automatically be redirected to the MED-V workspace and vice versa.</span></span>

<span data-ttu-id="41316-107">In den folgenden Verfahren wird beschrieben, wie Sie eine Liste von Webbrowsing-Regeln für einen MED-V-Arbeitsbereich einrichten können.</span><span class="sxs-lookup"><span data-stu-id="41316-107">The following procedures describe how you can set a list of Web browsing rules for a MED-V workspace.</span></span> <span data-ttu-id="41316-108">Alle in den Regeln enthaltenen Websites können im MED-V-Arbeitsbereich oder auf dem Host durchsucht werden, wie vom Administrator definiert.</span><span class="sxs-lookup"><span data-stu-id="41316-108">All sites included in the rules can be browsed either in the MED-V workspace or on the host, as defined by the administrator.</span></span> <span data-ttu-id="41316-109">Alle Websites, die nicht in den Regeln definiert sind, werden von der Umgebung aus durchsucht, in der Sie angefordert wurden.</span><span class="sxs-lookup"><span data-stu-id="41316-109">All sites not defined within the rules are browsed from the environment in which they were requested.</span></span> <span data-ttu-id="41316-110">Sie können Sie jedoch auch als Gruppe konfigurieren, um im MED-V-Arbeitsbereich oder auf dem Host durchsucht zu werden.</span><span class="sxs-lookup"><span data-stu-id="41316-110">However, you can configure them as a group as well, to be browsed in the MED-V workspace or the host.</span></span>

**<span data-ttu-id="41316-111">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="41316-111">Note</span></span>**  
<span data-ttu-id="41316-112">Web-Einstellungen gelten nur für Internet Explorer und keine anderen Browser.</span><span class="sxs-lookup"><span data-stu-id="41316-112">Web settings are applied only to Internet Explorer and to no other browsers.</span></span>



<span data-ttu-id="41316-113">Alle Web-Einstellungen werden im **Richtlinien** Modul auf der Registerkarte **Web** konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="41316-113">All Web settings are configured in the **Policy** module, on the **Web** tab.</span></span>

## <span data-ttu-id="41316-114">Konfigurieren von Webeinstellungen für den MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="41316-114">How to Configure Web Settings for the MED-V Workspace</span></span>


**<span data-ttu-id="41316-115">So konfigurieren Sie Webeinstellungen für den MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="41316-115">To configure Web settings for the MED-V workspace</span></span>**

1.  <span data-ttu-id="41316-116">Klicken Sie auf den zu konfigurierbaren MED-V-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="41316-116">Click the MED-V workspace to be configured.</span></span>

2.  <span data-ttu-id="41316-117">Aktivieren Sie das Kontrollkästchen **Durchsuchen der Liste der URLs, die in der folgenden Tabelle definiert** sind, um den Benutzer zu einem Browser im MED-V-Arbeitsbereich oder-Host umzuleiten, wenn der Benutzer zu einer URL sucht, die den angegebenen Web Rules entspricht.</span><span class="sxs-lookup"><span data-stu-id="41316-117">Select the **Browse the list of URLs defined in the following table** check box to redirect the user to a browser within the MED-V workspace or host, when the user browses to a URL that conforms to the Web rules specified.</span></span>

3.  <span data-ttu-id="41316-118">Klicken Sie auf eine der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="41316-118">Click one of the following:</span></span>

    -   <span data-ttu-id="41316-119">**Im Arbeitsbereich**: Umleiten zu einem Browser im MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="41316-119">**In the Workspace**—Redirect to a browser in the MED-V workspace.</span></span>

    -   <span data-ttu-id="41316-120">**Im Host**: Umleiten zu einem Browser auf dem Host.</span><span class="sxs-lookup"><span data-stu-id="41316-120">**In the host**—Redirect to a browser on the host.</span></span>

4.  <span data-ttu-id="41316-121">Aktivieren Sie das Kontrollkästchen **alle anderen URLs durchsuchen** , um alle URLs, die von den webregeln ausgeschlossen sind, an den Host-oder MED-V-Arbeitsbereich umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="41316-121">Select the **Browse all other URLs** check box to redirect all URLs excluded from the Web rules to the host or MED-V workspace.</span></span>

5.  <span data-ttu-id="41316-122">Klicken Sie auf eine der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="41316-122">Click one of the following:</span></span>

    -   <span data-ttu-id="41316-123">**Im Arbeitsbereich**: leiten Sie alle anderen URLs zu einem Browser im MED-V-Arbeitsbereich um.</span><span class="sxs-lookup"><span data-stu-id="41316-123">**In the Workspace**—Redirect all other URLs to a browser in the MED-V workspace.</span></span>

    -   <span data-ttu-id="41316-124">**Im Host**: Umleiten aller anderen URLs zu einem Browser auf dem Host.</span><span class="sxs-lookup"><span data-stu-id="41316-124">**In the host**—Redirect all other URLs to a browser on the host.</span></span>

6.  <span data-ttu-id="41316-125">Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.</span><span class="sxs-lookup"><span data-stu-id="41316-125">On the **Policy** menu, select **Commit**.</span></span>

## <span data-ttu-id="41316-126">So fügen Sie eine Web-Regel hinzu</span><span class="sxs-lookup"><span data-stu-id="41316-126">How to Add a Web Rule</span></span>


**<span data-ttu-id="41316-127">So fügen Sie eine Web-Regel hinzu</span><span class="sxs-lookup"><span data-stu-id="41316-127">To add a Web rule</span></span>**

1.  <span data-ttu-id="41316-128">Aktivieren Sie das Kontrollkästchen **Liste der in der folgenden Tabelle definierten URLs durchsuchen** , um die Webbrowser Regeln für das Internet zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="41316-128">Select the **Browse the list of URLs defined in the following table** check box to enable the Web browsing rules.</span></span>

2.  <span data-ttu-id="41316-129">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="41316-129">Click **Add**.</span></span>

    <span data-ttu-id="41316-130">Eine neue webregel wird hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="41316-130">A new Web rule is added.</span></span>

3.  <span data-ttu-id="41316-131">Konfigurieren Sie die webregel Eigenschaften wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="41316-131">Configure the Web rule properties as described in the following table.</span></span>

4.  <span data-ttu-id="41316-132">Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.</span><span class="sxs-lookup"><span data-stu-id="41316-132">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="41316-133">MED-V Workspace-Webeigenschaften</span><span class="sxs-lookup"><span data-stu-id="41316-133">MED-V Workspace Web Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="41316-134">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="41316-134">Property</span></span></th>
<th align="left"><span data-ttu-id="41316-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41316-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="41316-136">Typ</span><span class="sxs-lookup"><span data-stu-id="41316-136">Type</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="41316-137">Domänensuffix </strong> – Zugriff auf eine beliebige Hostadresse, die mit dem in der <strong> Value </strong> -Eigenschaft angegebenen Suffix endet und entsprechend der im Web Browsing festgelegten Option festgelegt ist <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="41316-137">Domain suffix</strong>—Access to any host address ending with the suffix specified in the <strong>Value</strong> property and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="41316-138">IP-Präfix </strong> : Zugriff auf eine vollständige oder teilweise IP-Adresse im Bereich des in der <strong> Value-Eigenschaft angegebenen Präfixes </strong> und wird entsprechend der im Web Browsing festgelegten Option festgelegt <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="41316-138">IP Prefix</strong>—Access to any full or partial IP address in the range of the prefix specified in the <strong>Value</strong> property and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="41316-139">Alle lokalen Adressen </strong> – Zugriff auf alle Adressen ohne &#39;. &#39; und wird entsprechend der im Web-Browsing festgelegten Option festgesetzt <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="41316-139">All Local Addresses</strong>—Access to all addresses without a &#39;.&#39; and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="41316-140">Wert</span><span class="sxs-lookup"><span data-stu-id="41316-140">Value</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="41316-141">Wenn <strong> Domänensuffix </strong> in der <strong> Type </strong> -Eigenschaft ausgewählt ist, geben Sie ein Domänensuffix ein.</span><span class="sxs-lookup"><span data-stu-id="41316-141">If <strong>Domain suffix</strong> is selected in the <strong>Type</strong> property, enter a domain suffix.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="41316-142">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="41316-142">Note</span></span></strong><br/><ul>
<li><p><span data-ttu-id="41316-143">Geben Sie nicht &quot; \* &quot; vor dem Suffix ein.</span><span class="sxs-lookup"><span data-stu-id="41316-143">Do not enter &quot;\*&quot; before the suffix.</span></span></p></li>
<li><p><span data-ttu-id="41316-144">Domänensuffixe unterstützen Aliase ebenfalls.</span><span class="sxs-lookup"><span data-stu-id="41316-144">Domain suffixes support aliases as well.</span></span></p></li>
</ul>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="41316-145">Wenn IP-Präfix in der <strong> Type </strong> -Eigenschaft ausgewählt ist, geben Sie eine vollständige oder teilweise IP-Adresse ein.</span><span class="sxs-lookup"><span data-stu-id="41316-145">If IP Prefix is selected in the <strong>Type</strong> property, enter a full or partial IP address.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="41316-146">So löschen Sie eine Web-Regel</span><span class="sxs-lookup"><span data-stu-id="41316-146">How to Delete a Web Rule</span></span>


**<span data-ttu-id="41316-147">So löschen Sie eine Web-Regel</span><span class="sxs-lookup"><span data-stu-id="41316-147">To delete a Web rule</span></span>**

1.  <span data-ttu-id="41316-148">Wählen Sie im Bereich **Web** die zu löschende Web-Regel aus.</span><span class="sxs-lookup"><span data-stu-id="41316-148">In the **Web** pane, select the Web rule to delete.</span></span>

2.  <span data-ttu-id="41316-149">Klicken Sie auf **Entfernen**.</span><span class="sxs-lookup"><span data-stu-id="41316-149">Click **Remove**.</span></span>

    <span data-ttu-id="41316-150">Die Web-Regel wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="41316-150">The Web rule is deleted.</span></span>

## <span data-ttu-id="41316-151">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="41316-151">Related topics</span></span>


[<span data-ttu-id="41316-152">Über die Benutzeroberfläche der MED-V-Management-Konsole</span><span class="sxs-lookup"><span data-stu-id="41316-152">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="41316-153">Erstellen eines MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="41316-153">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)









