---
title: So konfigurieren Sie die Streaming Server Security-Nachinstallation
description: So konfigurieren Sie die Streaming Server Security-Nachinstallation
author: dansimp
ms.assetid: 9bde3677-d1aa-4dcc-904e-bb49a268d748
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1945b38da5dd50c0bd2fb0c741bd92012e78586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807292"
---
# <span data-ttu-id="2b0b5-103">So konfigurieren Sie die Streaming Server Security-Nachinstallation</span><span class="sxs-lookup"><span data-stu-id="2b0b5-103">How to Configure Streaming Server Security Post-Installation</span></span>


<span data-ttu-id="2b0b5-104">Konfigurieren Sie den App-V-Streamingserver für erhöhte Sicherheit über die Registrierung.</span><span class="sxs-lookup"><span data-stu-id="2b0b5-104">Configure the App-V Streaming Server for enhanced security through the registry.</span></span> <span data-ttu-id="2b0b5-105">Wie beim App-V-Verwaltungsserver muss ein Zertifikat ordnungsgemäß mit dem richtigen EKU-Bezeichner für die Server Authentifizierung bereitgestellt werden, bevor Sie das folgende Verfahren nach der Installation ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b0b5-105">As with the App-V Management Server, a certificate must be correctly provisioned with the correct EKU identifier for Server Authentication before you complete the following post-installation procedure.</span></span>

**<span data-ttu-id="2b0b5-106">So konfigurieren Sie die Streaming Server-Sicherheit nach der Installation</span><span class="sxs-lookup"><span data-stu-id="2b0b5-106">To configure Streaming Server security post-installation</span></span>**

1.  <span data-ttu-id="2b0b5-107">Erstellen Sie eine MMC, fügen **Sie das** Zertifikat-Snap-in hinzu, und wählen Sie den **Zertifikatspeicher für den lokalen Computer**aus.</span><span class="sxs-lookup"><span data-stu-id="2b0b5-107">Create an MMC, add the **Certificates** snap-in, and select **Local Machine certificate store**.</span></span>

2.  <span data-ttu-id="2b0b5-108">Öffnen Sie die **persönlichen** Zertifikate für den Computer, und öffnen Sie das Zertifikat, das für App-V bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2b0b5-108">Open the **Personal** certificates for the computer, and open the certificate provisioned for App-V.</span></span>

3.  <span data-ttu-id="2b0b5-109">Scrollen Sie auf der Registerkarte **Details** nach unten zum Fingerabdruck, und kopieren Sie den Hash im Detailbereich.</span><span class="sxs-lookup"><span data-stu-id="2b0b5-109">On the **Details** tab, scroll down to the thumbprint and copy the hash in the details pane.</span></span>

4.  <span data-ttu-id="2b0b5-110">Öffnen Sie den Registrierungs-Editor, und navigieren Sie zu `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server` .</span><span class="sxs-lookup"><span data-stu-id="2b0b5-110">Open the registry editor, and navigate to `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server`.</span></span>

5.  <span data-ttu-id="2b0b5-111">Bearbeiten `X509CertHash` Sie den Wert, fügen Sie den Fingerabdruck Hash in das Feld Wert ein, und entfernen Sie alle Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="2b0b5-111">Edit the `X509CertHash` value, paste the thumbprint hash in the value field, and remove all spaces.</span></span> <span data-ttu-id="2b0b5-112">Klicken Sie auf **OK** , um die Bearbeitung zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="2b0b5-112">Click **OK** to accept the edit.</span></span>

6.  <span data-ttu-id="2b0b5-113">Navigieren Sie im Registrierungs-Editor zu `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts` .</span><span class="sxs-lookup"><span data-stu-id="2b0b5-113">In the registry editor, navigate to `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts`.</span></span>

7.  <span data-ttu-id="2b0b5-114">Erstellen Sie einen neuen **DWORD** -Wert mit dem Namen "322", und geben Sie dann den Dezimalwert als 322 oder den Hexadezimalwert als 142 ein.</span><span class="sxs-lookup"><span data-stu-id="2b0b5-114">Create a new **DWORD** value named "322," and then enter the decimal value as 322 or the hexadecimal value as 142.</span></span>

8.  <span data-ttu-id="2b0b5-115">Starten Sie den Streamingdienst neu.</span><span class="sxs-lookup"><span data-stu-id="2b0b5-115">Restart the streaming service.</span></span>

## <span data-ttu-id="2b0b5-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2b0b5-116">Related topics</span></span>


[<span data-ttu-id="2b0b5-117">So konfigurieren Sie Management Server Security-Nachinstallation</span><span class="sxs-lookup"><span data-stu-id="2b0b5-117">How to Configure Management Server Security Post-Installation</span></span>](how-to-configure-management-server-security-post-installation.md)

[<span data-ttu-id="2b0b5-118">Behandeln von Problemen mit Zertifikatberechtigungen</span><span class="sxs-lookup"><span data-stu-id="2b0b5-118">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)

 

 





