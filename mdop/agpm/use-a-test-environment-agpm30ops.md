---
title: Verwenden einer Testumgebung
description: Verwenden einer Testumgebung
author: dansimp
ms.assetid: 86295084-b39e-4040-bb3f-15c3c1e99b1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1264d9fe6f922a7e61bcd069581c7bd5e39b7787
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807427"
---
# <span data-ttu-id="acef2-103">Verwenden einer Testumgebung</span><span class="sxs-lookup"><span data-stu-id="acef2-103">Use a Test Environment</span></span>


<span data-ttu-id="acef2-104">Wenn Sie eine Testorganisationseinheit (Organizational Unit, OU) zum Testen von Gruppenrichtlinienobjekten (GPOs) vor der Bereitstellung in der Produktionsumgebung verwenden, müssen Sie über die erforderlichen Berechtigungen für den Zugriff auf die Testorganisationseinheit verfügen.</span><span class="sxs-lookup"><span data-stu-id="acef2-104">If you use a testing organizational unit (OU) to test Group Policy Objects (GPOs) before deployment to the production environment, you must have the necessary permissions to access the test OU.</span></span> <span data-ttu-id="acef2-105">Die Verwendung einer Testorganisationseinheit ist optional.</span><span class="sxs-lookup"><span data-stu-id="acef2-105">The use of a test OU is optional.</span></span>

**<span data-ttu-id="acef2-106">So verwenden Sie eine Testorganisationseinheit</span><span class="sxs-lookup"><span data-stu-id="acef2-106">To use a test OU</span></span>**

1.  <span data-ttu-id="acef2-107">Wenn Sie das Gruppenrichtlinienobjekt zur Bearbeitung ausgecheckt haben, klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten.</span><span class="sxs-lookup"><span data-stu-id="acef2-107">While you have the GPO checked out for editing, in the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you are managing GPOs.</span></span>

2.  <span data-ttu-id="acef2-108">Klicken Sie auf die ausgecheckte Kopie des zu testenden Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="acef2-108">Click the checked out copy of the GPO to be tested.</span></span> <span data-ttu-id="acef2-109">Dem Namen wird **\ [ausgecheckt \]** vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="acef2-109">The name will be preceded with **\[Checked Out\]**.</span></span> <span data-ttu-id="acef2-110">(Wenn Sie nicht aufgeführt ist, klicken Sie auf **Aktion**und dann auf **Aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="acef2-110">(If it is not listed, click **Action**, then **Refresh**.</span></span> <span data-ttu-id="acef2-111">Sortieren Sie die Namen alphabetisch, und **\ [ausgecheckt \]** GPOs werden in der Regel oben in der Liste angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="acef2-111">Sort the names alphabetically, and **\[Checked Out\]** GPOs will typically appear at the top of the list.)</span></span>

3.  <span data-ttu-id="acef2-112">Ziehen Sie das Gruppenrichtlinienobjekt in die Testorganisationseinheit, und legen Sie es ab.</span><span class="sxs-lookup"><span data-stu-id="acef2-112">Drag and drop the GPO to the test OU.</span></span>

4.  <span data-ttu-id="acef2-113">Klicken Sie im Dialogfeld, in dem Sie gefragt werden, ob Sie einen Link zu einem GPO in der Testorganisationseinheit erstellen möchten, auf **OK** .</span><span class="sxs-lookup"><span data-stu-id="acef2-113">Click **OK** in the dialog box asking whether to create a link to the GPO in the test OU.</span></span>

### <span data-ttu-id="acef2-114">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="acef2-114">Additional considerations</span></span>

-   <span data-ttu-id="acef2-115">Nach Abschluss der Prüfung löscht das Einchecken des Gruppenrichtlinienobjekts automatisch den Link zu der ausgecheckten Kopie des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="acef2-115">When testing is complete, checking in the GPO automatically deletes the link to the checked-out copy of the GPO.</span></span>

### <span data-ttu-id="acef2-116">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="acef2-116">Additional references</span></span>

-   [<span data-ttu-id="acef2-117">Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="acef2-117">Editing a GPO</span></span>](editing-a-gpo-agpm30ops.md)

 

 





