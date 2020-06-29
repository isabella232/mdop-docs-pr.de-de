---
title: So installieren Sie MED-V-Client
description: So installieren Sie MED-V-Client
author: dansimp
ms.assetid: bfac6de7-d96d-4b3e-bd8b-183e051e53c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2e4468b15c0c196bf605b1b5d129ab38678ec74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812208"
---
# <span data-ttu-id="bb2bb-103">So installieren Sie MED-V-Client</span><span class="sxs-lookup"><span data-stu-id="bb2bb-103">How to Install MED-V Client</span></span>


<span data-ttu-id="bb2bb-104">In einem Bereitstellungspaket basierten Szenario ist die MED-V-Clientinstallation im Bereitstellungspaket enthalten und direkt aus dem Paket installiert.</span><span class="sxs-lookup"><span data-stu-id="bb2bb-104">In a deployment package-based scenario, the MED-V client installation is included in the deployment package and installed directly from the package.</span></span>

**<span data-ttu-id="bb2bb-105">Wichtig</span><span class="sxs-lookup"><span data-stu-id="bb2bb-105">Important</span></span>**  
<span data-ttu-id="bb2bb-106">Wenn Sie ein Bereitstellungspaket verwenden, das kein Bild enthält, stellen Sie sicher, dass das Bild vor der Installation des Bereitstellungspakets in das Web hochgeladen oder in den Ordner Pre-stage verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="bb2bb-106">When using a deployment package that does not include an image, ensure that the image is uploaded to the Web or pushed to the pre-stage folder prior to installing the deployment package.</span></span>



**<span data-ttu-id="bb2bb-107">So installieren Sie ein Bereitstellungspaket</span><span class="sxs-lookup"><span data-stu-id="bb2bb-107">To install a deployment package</span></span>**

1.  <span data-ttu-id="bb2bb-108">Führen Sie eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="bb2bb-108">Do one of the following:</span></span>

    -   <span data-ttu-id="bb2bb-109">Laden Sie das MED-V-Paket aus dem Web herunter.</span><span class="sxs-lookup"><span data-stu-id="bb2bb-109">Download the MED-V package from the Web.</span></span>

    -   <span data-ttu-id="bb2bb-110">Legen Sie die Bereitstellung USB oder DVD in das Hostlaufwerk ein.</span><span class="sxs-lookup"><span data-stu-id="bb2bb-110">Insert the deployment USB or DVD into the host drive.</span></span>

2.  <span data-ttu-id="bb2bb-111">Wenn MED-V nicht automatisch gestartet wird, doppelklicken Sie auf MED-VAutoInstaller.exe.</span><span class="sxs-lookup"><span data-stu-id="bb2bb-111">If MED-V does not launch automatically, double-click MED-VAutoInstaller.exe.</span></span>

    <span data-ttu-id="bb2bb-112">Es wird ein Dialogfeld angezeigt, in dem die Komponenten aufgelistet sind, die bereits installiert sind und die derzeit installiert sind.</span><span class="sxs-lookup"><span data-stu-id="bb2bb-112">A dialog box appears listing the components that are already installed and those that are currently being installed.</span></span>

    **<span data-ttu-id="bb2bb-113">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="bb2bb-113">Note</span></span>**  
    <span data-ttu-id="bb2bb-114">Wenn eine Version des Microsoft Virtual PC, die nicht unterstützt wird, auf dem Hostcomputer vorhanden ist, wird eine Meldung angezeigt, in der Sie darüber informiert werden, dass die vorhandene Version deinstalliert und das Installationsprogramm erneut ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb2bb-114">If a version of the Microsoft Virtual PC that is not supported exists on the host computer, a message will appear telling you to uninstall the existing version and run the installer again.</span></span>



~~~
**Note**  
If an older version of the MED-V client exists, it will prompt you asking whether you want to upgrade.



Depending on the components that have been installed, you might need to reboot. If rebooting is necessary, a message appears notifying you that you must reboot.
~~~

3. <span data-ttu-id="bb2bb-115">Falls erforderlich, starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="bb2bb-115">If necessary, reboot the computer.</span></span>

   <span data-ttu-id="bb2bb-116">Nach Abschluss der Installation wird MED-V gestartet, und es wird eine Meldung angezeigt, in der Sie darüber informiert werden, dass die Installation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="bb2bb-116">When the installation is complete, MED-V starts and a message appears notifying you that the installation is complete.</span></span>

4. <span data-ttu-id="bb2bb-117">Melden Sie sich bei MED-V mit dem folgenden Benutzernamen und Kennwort an:</span><span class="sxs-lookup"><span data-stu-id="bb2bb-117">Log in to MED-V using the following user name and password:</span></span>

   -   <span data-ttu-id="bb2bb-118">Geben Sie den Domänennamen und den Benutzernamen gefolgt vom Kennwort des Domänenbenutzers ein, der mit MED-V arbeiten darf.</span><span class="sxs-lookup"><span data-stu-id="bb2bb-118">Type in the domain name and user name followed by the password of the domain user who is permitted to work with MED-V.</span></span>

       <span data-ttu-id="bb2bb-119">Beispiel: "Domäne \ _name \\user\ _name"; "Kennwort"</span><span class="sxs-lookup"><span data-stu-id="bb2bb-119">Example: "domain\_name\\user\_name", "password"</span></span>

## <span data-ttu-id="bb2bb-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="bb2bb-120">Related topics</span></span>


[<span data-ttu-id="bb2bb-121">So konfigurieren Sie ein Bereitstellungspaket</span><span class="sxs-lookup"><span data-stu-id="bb2bb-121">How to Configure a Deployment Package</span></span>](how-to-configure-a-deployment-package.md)

[<span data-ttu-id="bb2bb-122">So laden Sie ein MED-V-Bild auf den Server hoch</span><span class="sxs-lookup"><span data-stu-id="bb2bb-122">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)

[<span data-ttu-id="bb2bb-123">Befehlszeilenreferenz für die Clientinstallation</span><span class="sxs-lookup"><span data-stu-id="bb2bb-123">Client Installation Command Line Reference</span></span>](client-installation-command-line-reference.md)









