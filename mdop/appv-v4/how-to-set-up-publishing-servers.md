---
title: So richten Sie Veröffentlichungsserver ein
description: So richten Sie Veröffentlichungsserver ein
author: dansimp
ms.assetid: 2111f079-c202-4c49-b2a6-f4237068b2dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f060d862fd1449f5240ad495b53a1fa4e97697f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806743"
---
# <span data-ttu-id="778d8-103">So richten Sie Veröffentlichungsserver ein</span><span class="sxs-lookup"><span data-stu-id="778d8-103">How to Set Up Publishing Servers</span></span>


<span data-ttu-id="778d8-104">Mit den folgenden Verfahren können Sie Application Virtualization Server direkt über die Client Verwaltungskonsole hinzufügen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="778d8-104">You can use the following procedures to add and configure Application Virtualization Servers directly from the Client Management Console.</span></span>

**<span data-ttu-id="778d8-105">So fügen Sie einen Anwendungsveröffentlichungsserver hinzu</span><span class="sxs-lookup"><span data-stu-id="778d8-105">To add an application publishing server</span></span>**

1.  <span data-ttu-id="778d8-106">Klicken Sie im **Ergebnis** Bereich mit der rechten Maustaste, und wählen Sie im Popupmenü den Eintrag neuer **Server** aus, um den Assistenten für neue Application Virtualization Server zu starten, oder klicken Sie alternativ mit der rechten Maustaste auf den Knoten **Publishing Server** , und wählen Sie dann im Popupmenü den Eintrag **neuer Server** aus.</span><span class="sxs-lookup"><span data-stu-id="778d8-106">In the **Results** pane, right-click and select **New Server** from the pop-up-menu to start the New Application Virtualization Server Wizard, or alternatively, right-click the **Publishing Server** node and select **New Server** from the pop-up-menu.</span></span>

2.  <span data-ttu-id="778d8-107">Geben Sie auf Seite 1 des Assistenten den Namen des Servers in das Feld **Anzeigename** ein, und wählen Sie in der Dropdownliste **Type** den Servertyp aus.</span><span class="sxs-lookup"><span data-stu-id="778d8-107">On page one of the wizard, enter the name of the server in the **Display Name** field and select the server type from the **Type** drop-down list.</span></span> <span data-ttu-id="778d8-108">In der Dropdownliste der Servertypen können Sie **Application Virtualization Server**, **Enhanced Security Application Virtualization Server**, **Standard HTTP Server**oder **Enhanced Security http Server** auswählen.</span><span class="sxs-lookup"><span data-stu-id="778d8-108">You can choose **Application Virtualization Server**, **Enhanced Security Application Virtualization Server**, **Standard HTTP Server**, or **Enhanced Security HTTP Server** from the drop-down list of server types.</span></span>

3.  <span data-ttu-id="778d8-109">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="778d8-109">Click **Next**.</span></span>

4.  <span data-ttu-id="778d8-110">Geben Sie auf Seite 2 des Assistenten die entsprechenden Informationen in die Felder **Hostname** und **Port** ein.</span><span class="sxs-lookup"><span data-stu-id="778d8-110">On page two of the wizard, type the appropriate information into the **Host Name** and **Port** fields.</span></span> <span data-ttu-id="778d8-111">Das Feld " **Pfad** " kann für Application Virtualization-Server nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="778d8-111">The **Path** field is not editable for Application Virtualization Servers.</span></span> <span data-ttu-id="778d8-112">Sie müssen einen Pfad für den Standard-HTTP-Server oder den erweiterten Security http-Server eingeben.</span><span class="sxs-lookup"><span data-stu-id="778d8-112">You must enter a path for Standard HTTP Server or Enhanced Security HTTP Server.</span></span>

5.  <span data-ttu-id="778d8-113">Klicken Sie auf **Fertig stellen** , um den Server hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="778d8-113">Click **Finish** to add the server.</span></span>

**<span data-ttu-id="778d8-114">So richten Sie einen Anwendungsveröffentlichungsserver ein</span><span class="sxs-lookup"><span data-stu-id="778d8-114">To set up an application publishing server</span></span>**

1.  <span data-ttu-id="778d8-115">Klicken Sie im **Ergebnis** Bereich mit der rechten Maustaste auf den gewünschten Server, und wählen Sie im Popupmenü **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="778d8-115">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="778d8-116">Klicken Sie auf die Registerkarte **Allgemein** , auf der Sie den Servernamen ändern, einen Typ aus der Dropdownliste der Servertypen auswählen und den Hostnamen und den Port angeben können.</span><span class="sxs-lookup"><span data-stu-id="778d8-116">Click the **General** tab, where you can change the server name, select a type from the drop-down list of server types, and specify the host name and port.</span></span> <span data-ttu-id="778d8-117">Wenn der Servertyp Standard-HTTP-Server oder Enhanced Security http Server ist, kann das Feld **path** ebenfalls bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="778d8-117">When the server type is Standard HTTP Server or Enhanced Security HTTP Server, the **Path** field is also editable.</span></span>

3.  <span data-ttu-id="778d8-118">Klicken Sie auf die Registerkarte **Aktualisieren** , auf der das Kontrollkästchen **Veröffentlichung bei Benutzeranmeldung aktualisieren** standardmäßig aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="778d8-118">Click the **Refresh** tab, where the **Refresh publishing on user login** check box is selected by default.</span></span> <span data-ttu-id="778d8-119">Wenn Sie die Aktualisierungsrate ändern möchten, aktivieren Sie das Kontrollkästchen **Veröffentlichungs alle aktualisieren** , und geben Sie eine Zahl ein, die die Häufigkeit im Feld darstellt.</span><span class="sxs-lookup"><span data-stu-id="778d8-119">To change the refresh rate, select the **Refresh publishing every** check box and enter a number that represents the frequency in the field.</span></span> <span data-ttu-id="778d8-120">Wählen Sie dann im Dropdownmenü die Option **Minuten**, **Stunden**und **Tage** aus.</span><span class="sxs-lookup"><span data-stu-id="778d8-120">Then select **Minutes**, **Hours**, **Days** from the drop-down menu.</span></span> <span data-ttu-id="778d8-121">(Die Mindestzeitdauer, die Sie eingeben können, beträgt 30 Minuten.)</span><span class="sxs-lookup"><span data-stu-id="778d8-121">(The minimum amount of time you can enter is 30 minutes.)</span></span>

4.  <span data-ttu-id="778d8-122">Klicken Sie auf über **nehmen** , um die Konfiguration zu ändern.</span><span class="sxs-lookup"><span data-stu-id="778d8-122">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="778d8-123">Wenn Sie die Veröffentlichung beendet haben, klicken Sie auf **OK** , um das Dialogfeld zu schließen und zur Client Verwaltungskonsole zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="778d8-123">When you are finished publishing, click **OK** to exit the dialog box and return to the Client Management Console.</span></span>

## <span data-ttu-id="778d8-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="778d8-124">Related topics</span></span>


[<span data-ttu-id="778d8-125">So deaktivieren oder ändern Sie Einstellungen für den unterbrochenen Betriebsmodus</span><span class="sxs-lookup"><span data-stu-id="778d8-125">How to Disable or Modify Disconnected Operation Mode Settings</span></span>](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





