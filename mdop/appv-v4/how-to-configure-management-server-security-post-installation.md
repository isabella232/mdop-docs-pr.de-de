---
title: So konfigurieren Sie Management Server Security-Nachinstallation
description: So konfigurieren Sie Management Server Security-Nachinstallation
author: dansimp
ms.assetid: 71979fa6-3d0b-4a8b-994e-cb728d013090
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 521e72ead78055a7d3261664ccb75d454c22e622
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807307"
---
# <span data-ttu-id="b54c3-103">So konfigurieren Sie Management Server Security-Nachinstallation</span><span class="sxs-lookup"><span data-stu-id="b54c3-103">How to Configure Management Server Security Post-Installation</span></span>


<span data-ttu-id="b54c3-104">Verwenden Sie die APP-v-Verwaltungskonsole, um das Zertifikat hinzuzufügen und den App-v-Verwaltungs Server für erhöhte Sicherheit zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b54c3-104">Use the App-V Management Console to add the certificate and configure the App-V Management Server for enhanced security.</span></span> <span data-ttu-id="b54c3-105">Mit dem folgenden Verfahren können Sie die Sicherheits nach Installation konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b54c3-105">You can use the following procedure to configure security post-installation.</span></span>

**<span data-ttu-id="b54c3-106">So konfigurieren Sie die nach Installation von Management Server-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="b54c3-106">To configure Management Server security post-installation</span></span>**

1.  <span data-ttu-id="b54c3-107">Öffnen Sie die APP-v-Verwaltungskonsole, und stellen Sie eine Verbindung mit dem **Verwaltungsdienst** mit App-v-Administratorprivilegien her.</span><span class="sxs-lookup"><span data-stu-id="b54c3-107">Open the App-V Management Console, and connect to the **Management Service** with App-V administrator privileges.</span></span>

2.  <span data-ttu-id="b54c3-108">Erweitern Sie den Server, erweitern Sie **Servergruppen**, und wählen Sie dann die entsprechende Servergruppe aus, für die der Verwaltungsserver registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="b54c3-108">Expand the server, expand **Server Groups**, and then select the appropriate server group with which the Management Server was registered.</span></span>

3.  <span data-ttu-id="b54c3-109">Klicken Sie mit der rechten Maustaste auf das Verwaltungs Server Objekt, und wählen Sie **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="b54c3-109">Right-click the Management Server object, and select **Properties**.</span></span>

4.  <span data-ttu-id="b54c3-110">Klicken Sie auf der Registerkarte **Ports** auf **Server Zertifikat** , und schließen Sie den Assistenten ab, um das ordnungsgemäß bereitgestellte Zertifikat auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="b54c3-110">On the **Ports** tab, click **Server Certificate** and complete the wizard to select the properly provisioned certificate.</span></span>

    <span data-ttu-id="b54c3-111">**Hinweis**  Wenn im Assistenten keine Zertifikate angezeigt werden, wurde kein Zertifikat bereitgestellt, oder das Zertifikat erfüllt die Anforderungen von App-V.</span><span class="sxs-lookup"><span data-stu-id="b54c3-111">**Note** If no certificates are displayed in the wizard, a certificate has not been provisioned or the certificate does meet the requirements of App-V.</span></span>

     

5.  <span data-ttu-id="b54c3-112">Klicken Sie auf **weiter** , um zur Seite **Willkommen beim Zertifikat-Assistenten** weiter zu gehen.</span><span class="sxs-lookup"><span data-stu-id="b54c3-112">Click **Next** to continue on to the **Welcome To Certificate Wizard** page.</span></span>

6.  <span data-ttu-id="b54c3-113">Wählen Sie im Bildschirm **Verfügbare Zertifikate** das richtige Zertifikat aus.</span><span class="sxs-lookup"><span data-stu-id="b54c3-113">Select the correct certificate in the **Available Certificates** screen.</span></span>

7.  <span data-ttu-id="b54c3-114">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="b54c3-114">Click **Finish**.</span></span>

8.  <span data-ttu-id="b54c3-115">Nachdem Sie den Assistenten abgeschlossen haben, löschen Sie **RTSP** als verfügbaren Abhör-Port.</span><span class="sxs-lookup"><span data-stu-id="b54c3-115">After completing the wizard, clear **RTSP** as an available listening port.</span></span> <span data-ttu-id="b54c3-116">Dadurch wird verhindert, dass Verbindungen über einen nicht sicheren Kommunikationskanal hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b54c3-116">This prevents connections from being made over a non-secure communication channel.</span></span>

9.  <span data-ttu-id="b54c3-117">Klicken Sie auf über **nehmen**, und starten Sie den **Microsoft Virtual Application Server** -Dienst erneut.</span><span class="sxs-lookup"><span data-stu-id="b54c3-117">Click **Apply**, and restart the **Microsoft Virtual Application Server** service.</span></span> <span data-ttu-id="b54c3-118">Verwenden Sie das MMC-Snap-in des Diensts, um diese Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b54c3-118">Use the service’s MMC snap-in to accomplish this task.</span></span>

## <span data-ttu-id="b54c3-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b54c3-119">Related topics</span></span>


[<span data-ttu-id="b54c3-120">So konfigurieren Sie die Streaming Server Security-Nachinstallation</span><span class="sxs-lookup"><span data-stu-id="b54c3-120">How to Configure Streaming Server Security Post-Installation</span></span>](how-to-configure-streaming-server-security-post-installation.md)

[<span data-ttu-id="b54c3-121">Behandeln von Problemen mit Zertifikatberechtigungen</span><span class="sxs-lookup"><span data-stu-id="b54c3-121">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)

 

 





