---
title: Migrieren von einer früheren Version
description: Migrieren von einer früheren Version
author: dansimp
ms.assetid: a13cd353-b22a-48f7-af1e-5d54ede2a7e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a05bbd498cdb77a1ddf694b1aab6aeb42124775b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805066"
---
# <span data-ttu-id="762fe-103">Migrieren von einer früheren Version</span><span class="sxs-lookup"><span data-stu-id="762fe-103">Migrating from a Previous Version</span></span>


<span data-ttu-id="762fe-104">Mit App-v 5,0 können Sie Ihre vorhandene App-v 4,6-Infrastruktur auf die flexiblere, integrierte und einfacher zu verwaltende App-v 5,0-Infrastruktur migrieren.</span><span class="sxs-lookup"><span data-stu-id="762fe-104">With App-V 5.0 you can migrate your existing App-V 4.6 infrastructure to the more flexible, integrated, and easier to manage App-V 5.0 infrastructure.</span></span>

<span data-ttu-id="762fe-105">Wenn Sie Ihre Migrationsstrategie planen, sollten Sie die folgenden Abschnitte in Frage stellen:</span><span class="sxs-lookup"><span data-stu-id="762fe-105">Consider the following sections when you plan your migration strategy:</span></span>

<span data-ttu-id="762fe-106">**Hinweis**  Weitere Informationen zu den Unterschieden zwischen App-v 4,6 und App-v 5,0 finden Sie unter **Unterschiede zwischen App-v 4,6 und App-v 5,0 im Abschnitt** [über APP-v 5,0](about-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="762fe-106">**Note** For more information about the differences between App-V 4.6 and App-V 5.0, see the **Differences between App-V 4.6 and App-V 5.0 section** of [About App-V 5.0](about-app-v-50.md).</span></span>

 

## <span data-ttu-id="762fe-107">Konvertieren von Paketen, die mit einer früheren Version von App-V erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="762fe-107">Converting packages created using a prior version of App-V</span></span>


<span data-ttu-id="762fe-108">Verwenden Sie das Paket Konverter-Dienstprogramm, um virtuelle Anwendungspakete zu aktualisieren, die mit früheren Versionen von App-V erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="762fe-108">Use the package converter utility to upgrade virtual application packages created using previous versions of App-V.</span></span> <span data-ttu-id="762fe-109">Der Paket Konverter verwendet PowerShell zum Konvertieren von Paketen und kann die Automatisierung des Prozesses unterstützen, wenn viele Pakete vorhanden sind, für die eine Konvertierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="762fe-109">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

<span data-ttu-id="762fe-110">**Wichtig**  Nachdem Sie ein vorhandenes Paket konvertiert haben, sollten Sie das Paket vor der Bereitstellung des Pakets testen, um sicherzustellen, dass der Konvertierungsvorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="762fe-110">**Important** After you convert an existing package you should test the package prior to deploying the package to ensure the conversion process was successful.</span></span>

 

**<span data-ttu-id="762fe-111">Was Sie wissen müssen, bevor Sie vorhandene Pakete konvertieren</span><span class="sxs-lookup"><span data-stu-id="762fe-111">What to know before you convert existing packages</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="762fe-112">Problem</span><span class="sxs-lookup"><span data-stu-id="762fe-112">Issue</span></span></th>
<th align="left"><span data-ttu-id="762fe-113">Problemumgehung</span><span class="sxs-lookup"><span data-stu-id="762fe-113">Workaround</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="762fe-114">Paket Skripts werden nicht konvertiert.</span><span class="sxs-lookup"><span data-stu-id="762fe-114">Package scripts are not converted.</span></span></p></td>
<td align="left"><p><span data-ttu-id="762fe-115">Testen Sie das konvertierte Paket.</span><span class="sxs-lookup"><span data-stu-id="762fe-115">Test the converted package.</span></span> <span data-ttu-id="762fe-116">Falls erforderlich, konvertieren Sie das Skript.</span><span class="sxs-lookup"><span data-stu-id="762fe-116">If necessary convert the script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="762fe-117">Überschreibungen für die Paket Registrierungseinstellung werden nicht konvertiert.</span><span class="sxs-lookup"><span data-stu-id="762fe-117">Package registry setting overrides are not converted.</span></span></p></td>
<td align="left"><p><span data-ttu-id="762fe-118">Testen Sie das konvertierte Paket.</span><span class="sxs-lookup"><span data-stu-id="762fe-118">Test the converted package.</span></span> <span data-ttu-id="762fe-119">Fügen Sie bei Bedarf Registrierungs Überschreibungen erneut hinzu.</span><span class="sxs-lookup"><span data-stu-id="762fe-119">If necessary, re-add registry overrides.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="762fe-120">Virtuelle Pakete, die DSC verwenden, werden nach der Konvertierung nicht verknüpft.</span><span class="sxs-lookup"><span data-stu-id="762fe-120">Virtual packages using DSC are not linked after conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="762fe-121">Verknüpfen Sie die Pakete mithilfe von Verbindungsgruppen.</span><span class="sxs-lookup"><span data-stu-id="762fe-121">Link the packages using connection groups.</span></span> <span data-ttu-id="762fe-122">Siehe <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)"> Verwalten von Verbindungsgruppen </a> .</span><span class="sxs-lookup"><span data-stu-id="762fe-122">See <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)">Managing Connection Groups</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="762fe-123">Während der Konvertierung werden Umgebungsvariablen Konflikte erkannt.</span><span class="sxs-lookup"><span data-stu-id="762fe-123">Environment variable conflicts are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="762fe-124">Beheben Sie alle Konflikte in der zugehörigen <strong> OSD- </strong> Datei.</span><span class="sxs-lookup"><span data-stu-id="762fe-124">Resolve any conflicts in the associated <strong>.osd</strong> file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="762fe-125">Während der Konvertierung werden hart codierte Pfade erkannt.</span><span class="sxs-lookup"><span data-stu-id="762fe-125">Hard-coded paths are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="762fe-126">Hart codierte Pfade sind schwierig, richtig zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="762fe-126">Hard-coded paths are difficult to convert correctly.</span></span> <span data-ttu-id="762fe-127">Der Paket Konverter erkennt Pakete mit Dateien, die hart codierte Pfade enthalten, und gibt diese zurück.</span><span class="sxs-lookup"><span data-stu-id="762fe-127">The package converter will detect and return packages with files that contain hard-coded paths.</span></span> <span data-ttu-id="762fe-128">Zeigen Sie die Datei mit dem hartcodierten Pfad an, und ermitteln Sie, ob das Paket die Datei erfordert.</span><span class="sxs-lookup"><span data-stu-id="762fe-128">View the file with the hard-coded path, and determine whether the package requires the file.</span></span> <span data-ttu-id="762fe-129">Wenn dies der Fall ist, empfiehlt es sich, das Paket neu zu sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="762fe-129">If so, it is recommended to re-sequence the package.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="762fe-130">Beim Konvertieren einer Paketprüfung auf fehlerhafte Dateien oder Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="762fe-130">When converting a package check for failing files or shortcuts.</span></span> <span data-ttu-id="762fe-131">Suchen Sie das Element in App-V 4,6-Paket.</span><span class="sxs-lookup"><span data-stu-id="762fe-131">Locate the item in App-V 4.6 package.</span></span> <span data-ttu-id="762fe-132">Möglicherweise ist es ein hartcodierter Pfad.</span><span class="sxs-lookup"><span data-stu-id="762fe-132">It could possibly be hard-coded path.</span></span> <span data-ttu-id="762fe-133">Konvertieren Sie den Pfad.</span><span class="sxs-lookup"><span data-stu-id="762fe-133">Convert the path.</span></span>

<span data-ttu-id="762fe-134">**Hinweis**  Es wird empfohlen, den App-V 5,0-Sequenzer zum Konvertieren kritischer Anwendungen oder Anwendungen zu verwenden, die Features nutzen müssen.</span><span class="sxs-lookup"><span data-stu-id="762fe-134">**Note** It is recommended that you use the App-V 5.0 sequencer for converting critical applications or applications that need to take advantage of features.</span></span> <span data-ttu-id="762fe-135">Lesen Sie, [wie Sie eine neue Anwendung mit App-V 5,0 Sequenzieren](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="762fe-135">See, [How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).</span></span>

<span data-ttu-id="762fe-136">Wenn ein konvertiertes Paket nicht geöffnet wird, nachdem Sie es konvertiert haben, empfiehlt es sich auch, die Anwendung mithilfe des App-V 5,0-Sequencers neu zu sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="762fe-136">If a converted package does not open after you convert it, it is also recommended that you re-sequence the application using the App-V 5.0 sequencer.</span></span>

 

[<span data-ttu-id="762fe-137">So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="762fe-137">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

## <span data-ttu-id="762fe-138">Migrieren von Clients</span><span class="sxs-lookup"><span data-stu-id="762fe-138">Migrating Clients</span></span>


<span data-ttu-id="762fe-139">In der folgenden Tabelle wird die empfohlene Methode zum Aktualisieren von Clients angezeigt.</span><span class="sxs-lookup"><span data-stu-id="762fe-139">The following table displays the recommended method for upgrading clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="762fe-140">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="762fe-140">Task</span></span></th>
<th align="left"><span data-ttu-id="762fe-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="762fe-141">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="762fe-142">Aktualisieren Ihrer Umgebung auf App-v 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="762fe-142">Upgrade your environment to App-V4.6SP2</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="762fe-143">Überlegungen zur Implementierung und zum Upgrade von Application Virtualization </a></span><span class="sxs-lookup"><span data-stu-id="762fe-143">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="762fe-144">Installieren Sie den App-V 5,0-Client mit aktivierter Koexistenz.</span><span class="sxs-lookup"><span data-stu-id="762fe-144">Install the App-V 5.0 client with co-existence enabled.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)"><span data-ttu-id="762fe-145">Bereitstellen der APP-v 4,6 und des App-v 5,0-Clients auf </a> demselben Computer</span><span class="sxs-lookup"><span data-stu-id="762fe-145">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="762fe-146">Sequenzieren und Rollout von App-V 5,0-Paketen.</span><span class="sxs-lookup"><span data-stu-id="762fe-146">Sequence and roll out App-V 5.0 packages.</span></span> <span data-ttu-id="762fe-147">Bei Bedarf können Sie die Veröffentlichung von App-V 4,6-Paketen aufheben.</span><span class="sxs-lookup"><span data-stu-id="762fe-147">As needed, unpublish App-V 4.6 packages.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)"><span data-ttu-id="762fe-148">So wird es gemacht: Sequenzierung einer neuen Anwendung mit APP- </a> V 5,0</span><span class="sxs-lookup"><span data-stu-id="762fe-148">How to Sequence a New Application with App-V 5.0</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="762fe-149">**Wichtig**  Sie müssen App-v 4.6 SP3 ausführen, um den Koexistenzmodus verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="762fe-149">**Important** You must be running App-V4.6SP3 to use coexistence mode.</span></span> <span data-ttu-id="762fe-150">Wenn Sie ein Paket sequenzieren, müssen Sie außerdem die Einstellung für die Verwaltungsautorität konfigurieren, die sich in der **Benutzerkonfiguration** befindet, die sich im Abschnitt **Benutzerkonfiguration** befindet.</span><span class="sxs-lookup"><span data-stu-id="762fe-150">Additionally, when you sequence a package, you must configure the Managing Authority setting, which is in the **User Configuration** is located in the **User Configuration** section.</span></span>

 

## <span data-ttu-id="762fe-151">Migrieren der vollständigen Infrastruktur des App-V 5,0-Servers</span><span class="sxs-lookup"><span data-stu-id="762fe-151">Migrating the App-V 5.0 Server Full Infrastructure</span></span>


<span data-ttu-id="762fe-152">Es gibt keine direkte Methode zum Upgrade auf eine vollständige App-V 5,0-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="762fe-152">There is no direct method to upgrade to a full App-V 5.0 infrastructure.</span></span> <span data-ttu-id="762fe-153">Verwenden Sie die Informationen im folgenden Abschnitt, um Informationen zum Upgrade des App-V-Servers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="762fe-153">Use the information in the following section for information about upgrading the App-V server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="762fe-154">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="762fe-154">Task</span></span></th>
<th align="left"><span data-ttu-id="762fe-155">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="762fe-155">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="762fe-156">Aktualisieren Sie Ihre Umgebung auf App-v 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="762fe-156">Upgrade your environment to App-V4.6SP3.</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="762fe-157">Überlegungen zur Implementierung und zum Upgrade von Application Virtualization </a></span><span class="sxs-lookup"><span data-stu-id="762fe-157">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="762fe-158">Bereitstellen der App-V 5,0-Version des Clients</span><span class="sxs-lookup"><span data-stu-id="762fe-158">Deploy App-V 5.0 version of the client.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"><span data-ttu-id="762fe-159">Bereitstellen des App-V </a> -Clients</span><span class="sxs-lookup"><span data-stu-id="762fe-159">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="762fe-160">Installieren Sie den App-V 5,0-Server.</span><span class="sxs-lookup"><span data-stu-id="762fe-160">Install App-V 5.0 server.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"><span data-ttu-id="762fe-161">Bereitstellen des App-V 5,0 </a> -Servers</span><span class="sxs-lookup"><span data-stu-id="762fe-161">How to Deploy the App-V 5.0 Server</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="762fe-162">Migrieren vorhandener Pakete</span><span class="sxs-lookup"><span data-stu-id="762fe-162">Migrate existing packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="762fe-163">Weitere Informationen finden Sie unter <strong> Konvertieren von Paketen, die mit einer früheren Version von App-V </strong> in diesem Artikel erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="762fe-163">See the <strong>Converting packages created using a prior version of App-V</strong> section of this article.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="762fe-164">Zusätzliche Migrationsaufgaben</span><span class="sxs-lookup"><span data-stu-id="762fe-164">Additional Migration tasks</span></span>


<span data-ttu-id="762fe-165">Sie können auch zusätzliche Migrationsaufgaben wie die Neukonfiguration von Endpunkten und das Öffnen eines Pakets ausführen, das mit einer früheren Version auf einem Computer mit dem App-V 5,0-Client erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="762fe-165">You can also perform additional migration tasks such as reconfiguring end points as well as opening a package created using a prior version on a computer running the App-V 5.0 client.</span></span> <span data-ttu-id="762fe-166">Die folgenden Links enthalten weitere Informationen zum Ausführen dieser Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="762fe-166">The following links provide more information about performing these tasks.</span></span>

[<span data-ttu-id="762fe-167">So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu einem konvertierten App-V 5.0-Paket für alle Benutzer eines bestimmten Computers</span><span class="sxs-lookup"><span data-stu-id="762fe-167">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="762fe-168">So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.0 für einen bestimmten Benutzer</span><span class="sxs-lookup"><span data-stu-id="762fe-168">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

[<span data-ttu-id="762fe-169">So setzen Sie Erweiterungspunkte von einem App-V 5.0-Paket auf ein App-V 4.6-Paket für alle Benutzer eines bestimmten Computers zurück</span><span class="sxs-lookup"><span data-stu-id="762fe-169">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="762fe-170">So setzen Sie Erweiterungspunkte von einem App-V 5.0-Paket auf ein App-V 4.6-Paket für einen bestimmten Benutzer zurück</span><span class="sxs-lookup"><span data-stu-id="762fe-170">How to Revert Extension Points From an App-V 5.0 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-a-specific-user.md)







## <span data-ttu-id="762fe-171">Weitere Ressourcen für die Ausführung von App-V-Migrationsaufgaben</span><span class="sxs-lookup"><span data-stu-id="762fe-171">Other resources for performing App-V migration tasks</span></span>


[<span data-ttu-id="762fe-172">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="762fe-172">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="762fe-173">Ein vereinfachtes Upgrade-Verfahren für Microsoft App-V 5,1-Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="762fe-173">A simplified Microsoft App-V 5.1 Management Server upgrade procedure</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





