---
title: So konfigurieren Sie Windows Server 2008 Firewall für App-V
description: So konfigurieren Sie Windows Server 2008 Firewall für App-V
author: dansimp
ms.assetid: 57f4ed17-0651-4a3c-be1e-29d9520c6aeb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 19e4cda9ac3b908f68e4f69b9663033d8a21ae41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807219"
---
# <span data-ttu-id="abe05-103">So konfigurieren Sie Windows Server 2008 Firewall für App-V</span><span class="sxs-lookup"><span data-stu-id="abe05-103">How to Configure Windows Server 2008 Firewall for App-V</span></span>


<span data-ttu-id="abe05-104">Mit der Einführung von Windows Server2008 wurden die Firewall-und IPSec-Komponenten zu einem einzigen Dienst zusammengeführt, und die Funktionen dieses Diensts wurden verbessert.</span><span class="sxs-lookup"><span data-stu-id="abe05-104">With the introduction of Windows Server2008, the firewall and IPsec components were merged into one service, and the capabilities of this service were enhanced.</span></span> <span data-ttu-id="abe05-105">Der neue Firewalldienst unterstützt eine eingehende und ausgehende Stateful-Prüfung.</span><span class="sxs-lookup"><span data-stu-id="abe05-105">The new firewall service supports incoming and outgoing stateful inspection.</span></span> <span data-ttu-id="abe05-106">Darüber hinaus können Sie mithilfe von Gruppenrichtlinien bestimmte Firewallregeln und IPSec-Richtlinien konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="abe05-106">Also, you can configure specific firewall rules and IPsec policies through group policies.</span></span> <span data-ttu-id="abe05-107">Weitere Informationen zur Windows-Firewall in Windows Server2008 finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=151980> .</span><span class="sxs-lookup"><span data-stu-id="abe05-107">For additional information about the Windows firewall in Windows Server2008, see <https://go.microsoft.com/fwlink/?LinkId=151980>.</span></span>

<span data-ttu-id="abe05-108">Das folgende Verfahren beinhaltet nicht das Hinzufügen einer Ausnahme für die ICO-und OSD-Veröffentlichung über SMB oder http/https.</span><span class="sxs-lookup"><span data-stu-id="abe05-108">The following procedure does not include adding an exception for ICO and OSD publishing through SMB or HTTP/HTTPS.</span></span> <span data-ttu-id="abe05-109">Diese Ausnahmen werden automatisch basierend auf dem Netzwerkprofil und den Rollen hinzugefügt, die auf der Windows Server 2008-Firewall installiert sind.</span><span class="sxs-lookup"><span data-stu-id="abe05-109">Those exceptions are automatically added based on the network profile and roles installed on the Windows Server 2008 firewall.</span></span>

<span data-ttu-id="abe05-110">**Hinweis**  Wenn der Verwaltungs Server für die Verwendung von RTSP konfiguriert ist, wiederholen Sie diesen Vorgang, um das `sghwsvr.exe` Programm als Ausnahme hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="abe05-110">**Note** If the Management Server is configured to use RTSP, repeat this procedure to add the `sghwsvr.exe` program as an exception.</span></span>

<span data-ttu-id="abe05-111">Der App-V Streaming Server erfordert die Programmausnahme `sglwdsptr.exe` für die RTSPS-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="abe05-111">The App-V Streaming Server requires the program exception `sglwdsptr.exe` for RTSPS communication.</span></span> <span data-ttu-id="abe05-112">Ein App-V-Streamingserver, der RTSP für die Kommunikation verwendet, erfordert auch eine Programmausnahme für `sglwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="abe05-112">An App-V Streaming Server that uses RTSP for communication also requires a program exception for `sglwsvr.exe`.</span></span>

 

**<span data-ttu-id="abe05-113">So konfigurieren Sie die Windows Server2008-Firewall für App-V</span><span class="sxs-lookup"><span data-stu-id="abe05-113">To configure Windows Server2008 firewall for App-V</span></span>**

1.  <span data-ttu-id="abe05-114">Öffnen Sie die **Windows-Firewall mit Advanced Security** Management Console über die Systemsteuerung oder durch Eingabe `wf.msc` in der Zeile ausführen.</span><span class="sxs-lookup"><span data-stu-id="abe05-114">Open the **Windows Firewall with Advanced Security** management console through the Control Panel or by typing `wf.msc` on the Run line.</span></span>

2.  <span data-ttu-id="abe05-115">Erstellen Sie eine neue eingehende Regel, und wählen Sie **Programm**aus.</span><span class="sxs-lookup"><span data-stu-id="abe05-115">Create a new inbound rule, and select **Program**.</span></span>

3.  <span data-ttu-id="abe05-116">Wählen Sie den Programmpfad aus, und navigieren Sie zu `sghwdsptr.exe` , der standardmäßig unter gespeichert ist `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .</span><span class="sxs-lookup"><span data-stu-id="abe05-116">Select the program path, and browse to `sghwdsptr.exe`, which is located by default at `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin`.</span></span>

4.  <span data-ttu-id="abe05-117">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="abe05-117">Click **Next**.</span></span>

5.  <span data-ttu-id="abe05-118">Wählen Sie **Action** auf der Seite Aktion **die Option Verbindung zulassen**aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="abe05-118">On the **Action** page, select **Allow the connection**, and then click **Next**.</span></span>

6.  <span data-ttu-id="abe05-119">Wählen Sie die geeigneten **profile** aus, die auf die eingehende Regel angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="abe05-119">Select the appropriate **Profiles** to apply to the inbound rule.</span></span>

7.  <span data-ttu-id="abe05-120">Geben Sie einen Namen und eine Beschreibung für die Regel ein, und klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="abe05-120">Provide a name and description for the rule, and click **Finish**.</span></span>

## <span data-ttu-id="abe05-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="abe05-121">Related topics</span></span>


[<span data-ttu-id="abe05-122">So konfigurieren Sie Windows Server 2003 Firewall für App-V</span><span class="sxs-lookup"><span data-stu-id="abe05-122">How to Configure Windows Server 2003 Firewall for App-V</span></span>](how-to-configure-windows-server-2003-firewall-for-app-v.md)

 

 





