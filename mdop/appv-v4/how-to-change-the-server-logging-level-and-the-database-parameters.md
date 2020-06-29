---
title: So ändern Sie die Serverebene für die Protokollierung und die Datenbankparameter
description: So ändern Sie die Serverebene für die Protokollierung und die Datenbankparameter
author: dansimp
ms.assetid: e3ebaee5-6c4c-4aa8-9766-c5aeb00f477a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bb35ac09c5e23f4847662171b68284f868e66dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807344"
---
# <span data-ttu-id="b473b-103">So ändern Sie die Serverebene für die Protokollierung und die Datenbankparameter</span><span class="sxs-lookup"><span data-stu-id="b473b-103">How to Change the Server Logging Level and the Database Parameters</span></span>


<span data-ttu-id="b473b-104">Mit den folgenden Verfahren können Sie den Protokolliergrad und die Datenbankprotokoll Parameter aus der Application Virtualization Server-Verwaltungskonsole ändern.</span><span class="sxs-lookup"><span data-stu-id="b473b-104">You can use the following procedures to change the logging level and the database log parameters from the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="b473b-105">Die folgenden Protokollierungsstufen stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="b473b-105">The following logging levels are available:</span></span>

-   <span data-ttu-id="b473b-106">Nur Transaktion</span><span class="sxs-lookup"><span data-stu-id="b473b-106">Transaction Only</span></span>

-   <span data-ttu-id="b473b-107">Schwerwiegende Fehler</span><span class="sxs-lookup"><span data-stu-id="b473b-107">Fatal Errors</span></span>

-   <span data-ttu-id="b473b-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="b473b-108">Errors</span></span>

-   <span data-ttu-id="b473b-109">Warnungen/Fehler</span><span class="sxs-lookup"><span data-stu-id="b473b-109">Warnings/Errors</span></span>

-   <span data-ttu-id="b473b-110">Informationen/Warnungen/Fehler</span><span class="sxs-lookup"><span data-stu-id="b473b-110">Info/Warnings/Errors</span></span>

-   <span data-ttu-id="b473b-111">Ausführliche</span><span class="sxs-lookup"><span data-stu-id="b473b-111">Verbose</span></span>

<span data-ttu-id="b473b-112">**Hinweis**  Aufgrund der Größe der Protokolldatei, die bei Verwendung des **verbose** -Modus erzeugt wird, empfehlen wir, dass Sie keine Produktionsserver mit dieser Protokollierungsstufe ausführen.</span><span class="sxs-lookup"><span data-stu-id="b473b-112">**Note** Because of the size of the log file produced when you use **Verbose** mode, the recommendation is that you do not run production servers with this level of logging set.</span></span>

 

<span data-ttu-id="b473b-113">Die Daten Bank Protokollierungsparameter legen den Daten Bank Treibertyp, die Zugriffsanmeldeinformationen und den Speicherort der Protokollierungsdatenbank fest.</span><span class="sxs-lookup"><span data-stu-id="b473b-113">The database logging parameters determine the database driver type, access credentials, and location of the logging database.</span></span>

**<span data-ttu-id="b473b-114">So ändern Sie den Protokolliergrad für Verwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="b473b-114">To change the logging level for Management Servers</span></span>**

1.  <span data-ttu-id="b473b-115">Klicken Sie auf den Knoten **Servergruppen** , um die Servergruppen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b473b-115">Click the **Server Groups** node to display the server groups.</span></span>

2.  <span data-ttu-id="b473b-116">Klicken Sie mit der rechten Maustaste auf die Servergruppe, und wählen Sie **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="b473b-116">Right-click the server group, and select **Properties**.</span></span>

3.  <span data-ttu-id="b473b-117">Wählen Sie im Dialogfeld **Eigenschaften** die Registerkarte **Protokollierung** aus.</span><span class="sxs-lookup"><span data-stu-id="b473b-117">In the **Properties** dialog box, select the **Logging** tab.</span></span>

4.  <span data-ttu-id="b473b-118">Wählen Sie im Dialogfeld **Servergruppeneigenschaften** den Server aus, und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="b473b-118">In the **Server Group Properties** dialog box, select the server and then click **Edit**.</span></span>

5.  <span data-ttu-id="b473b-119">Wählen Sie im Dialogfeld **Protokollmodul hinzufügen/bearbeiten** den Protokolliergrad in der Dropdownliste **Ereignistyp** aus.</span><span class="sxs-lookup"><span data-stu-id="b473b-119">In the **Add/Edit Log Module** dialog box, select the logging level from the **Event Type** drop-down list.</span></span>

6.  <span data-ttu-id="b473b-120">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="b473b-120">Click **OK**.</span></span>

7.  <span data-ttu-id="b473b-121">Klicken Sie im Dialogfeld **Server Gruppeneigenschaften** auf **OK** oder auf über **nehmen**.</span><span class="sxs-lookup"><span data-stu-id="b473b-121">In the **Server Group Properties** dialog box, click **OK** or **Apply**.</span></span>

**<span data-ttu-id="b473b-122">So ändern Sie den Protokolliergrad für Streamingserver</span><span class="sxs-lookup"><span data-stu-id="b473b-122">To change the logging level for Streaming Servers</span></span>**

1.  <span data-ttu-id="b473b-123">Bearbeiten Sie den folgenden Registrierungsschlüsselwert, um den Protokolliergrad zu ändern:</span><span class="sxs-lookup"><span data-stu-id="b473b-123">Edit the following registry key value to change the logging level:</span></span>

    -   <span data-ttu-id="b473b-124">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\distributionserver\\loglevel</span><span class="sxs-lookup"><span data-stu-id="b473b-124">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel</span></span>

2.  <span data-ttu-id="b473b-125">Wählen Sie einen der folgenden Werte aus, um den Protokolliergrad einzustellen.</span><span class="sxs-lookup"><span data-stu-id="b473b-125">Select one of the following values to set the logging level.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="b473b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b473b-126">Value</span></span></th>
    <th align="left"><span data-ttu-id="b473b-127">Protokollierungsstufe</span><span class="sxs-lookup"><span data-stu-id="b473b-127">Logging Level</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b473b-128">0</span><span class="sxs-lookup"><span data-stu-id="b473b-128">0</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b473b-129">Nur Transaktionen</span><span class="sxs-lookup"><span data-stu-id="b473b-129">Transactions Only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b473b-130">1</span><span class="sxs-lookup"><span data-stu-id="b473b-130">1</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b473b-131">Schwerwiegende Fehler</span><span class="sxs-lookup"><span data-stu-id="b473b-131">Fatal Errors</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b473b-132">2</span><span class="sxs-lookup"><span data-stu-id="b473b-132">2</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b473b-133">Fehler</span><span class="sxs-lookup"><span data-stu-id="b473b-133">Errors</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b473b-134">3</span><span class="sxs-lookup"><span data-stu-id="b473b-134">3</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b473b-135">Warnungen/Fehler</span><span class="sxs-lookup"><span data-stu-id="b473b-135">Warnings/Errors</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b473b-136">4</span><span class="sxs-lookup"><span data-stu-id="b473b-136">4</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b473b-137">Informationen/Warnungen/Fehler</span><span class="sxs-lookup"><span data-stu-id="b473b-137">Information/ Warnings/Errors</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b473b-138">5</span><span class="sxs-lookup"><span data-stu-id="b473b-138">5</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b473b-139">Ausführliche</span><span class="sxs-lookup"><span data-stu-id="b473b-139">Verbose</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="b473b-140">So ändern Sie Datenbankprotokoll Parameter</span><span class="sxs-lookup"><span data-stu-id="b473b-140">To change database log parameters</span></span>**

1.  <span data-ttu-id="b473b-141">Klicken Sie auf den Knoten **Servergruppen** , um die Servergruppen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b473b-141">Click the **Server Groups** node to display the server groups.</span></span>

2.  <span data-ttu-id="b473b-142">Klicken Sie mit der rechten Maustaste auf die Servergruppe, und wählen Sie **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="b473b-142">Right-click the server group, and select **Properties**.</span></span>

3.  <span data-ttu-id="b473b-143">Wählen Sie im Dialogfeld **Eigenschaften** die Registerkarte **Protokollierung** aus.</span><span class="sxs-lookup"><span data-stu-id="b473b-143">In the **Properties** dialog box, select the **Logging** tab.</span></span>

4.  <span data-ttu-id="b473b-144">Wählen Sie im Dialogfeld **Servergruppeneigenschaften** den Server aus, und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="b473b-144">In the **Server Group Properties** dialog box, select the server and then click **Edit**.</span></span>

5.  <span data-ttu-id="b473b-145">Wählen Sie im Dialogfeld **Protokollmodul hinzufügen/bearbeiten** in der Dropdownliste **Datenbanktreiber** einen Datenbanktreiber aus.</span><span class="sxs-lookup"><span data-stu-id="b473b-145">In the **Add/Edit Log Module** dialog box, select a database driver from the **Database Driver** drop-down list.</span></span>

6.  <span data-ttu-id="b473b-146">Geben Sie einen **DNS-Hostnamen**ein.</span><span class="sxs-lookup"><span data-stu-id="b473b-146">Enter a **DNS Host Name**.</span></span>

7.  <span data-ttu-id="b473b-147">Klicken Sie auf das Kontrollkästchen **Port dynamisch bestimmen** , oder geben Sie eine Portnummer in das Feld **Port** ein.</span><span class="sxs-lookup"><span data-stu-id="b473b-147">Click the **Dynamically Determine Port** check box, or enter a port number in the **Port** field.</span></span>

8.  <span data-ttu-id="b473b-148">Geben Sie einen **Dienstnamen** in das entsprechende Feld ein.</span><span class="sxs-lookup"><span data-stu-id="b473b-148">Enter a **Service Name** in the corresponding field.</span></span>

9.  <span data-ttu-id="b473b-149">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="b473b-149">Click **OK**.</span></span>

10. <span data-ttu-id="b473b-150">Klicken Sie im Dialogfeld **Server Gruppeneigenschaften** auf **OK** oder auf über **nehmen**.</span><span class="sxs-lookup"><span data-stu-id="b473b-150">On the **Server Group Properties** dialog box, click **OK** or **Apply**.</span></span>

## <span data-ttu-id="b473b-151">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b473b-151">Related topics</span></span>


[<span data-ttu-id="b473b-152">So passen Sie ein Application Virtualization System in der Server Management Console an</span><span class="sxs-lookup"><span data-stu-id="b473b-152">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

 

 





