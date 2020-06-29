---
title: Installieren der App-V-Datenbanken und Konvertieren der zugehörigen Sicherheitsbezeichner mithilfe von PowerShell
description: Installieren der App-V-Datenbanken und Konvertieren der zugehörigen Sicherheitsbezeichner mithilfe von PowerShell
author: dansimp
ms.assetid: 2be6fb72-f3a6-4550-bba1-6defa78ca08a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39651df4d62971e39c4228ffce665386d5c9769d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805426"
---
# <span data-ttu-id="ec0c4-103">Installieren der App-V-Datenbanken und Konvertieren der zugehörigen Sicherheitsbezeichner mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="ec0c4-103">How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell</span></span>

<span data-ttu-id="ec0c4-104">Verwenden Sie das folgende PowerShell-Verfahren, um eine beliebige Anzahl von Active Directory-Domänendiensten (AD DS)-Benutzer-oder-Computerkonten in formatierte Sicherheits-IDs (SIDs) sowohl im Standardformat als auch im Hexadezimalformat zu konvertieren, das von Microsoft SQL Server bei der Ausführung von SQL-Skripts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ec0c4-104">Use the following PowerShell procedure to convert any number of Active Directory Domain Services (AD DS) user or machine accounts into formatted Security Identifiers (SIDs) both in the standard format and in the hexadecimal format used by Microsoft SQL Server when running SQL scripts.</span></span>

<span data-ttu-id="ec0c4-105">Bevor Sie diesen Vorgang ausführen, sollten Sie die in der folgenden Liste angezeigten Informationen und Beispiele lesen und verstehen:</span><span class="sxs-lookup"><span data-stu-id="ec0c4-105">Before attempting this procedure, you should read and understand the information and examples displayed in the following list:</span></span>

- <span data-ttu-id="ec0c4-106">**. Eingaben** – die Konten, die zum Konvertieren in das SID-Format verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec0c4-106">**.INPUTS** – The account or accounts used to convert to SID format.</span></span> <span data-ttu-id="ec0c4-107">Hierbei kann es sich um einen einzelnen Kontonamen oder ein Array von Kontonamen handeln.</span><span class="sxs-lookup"><span data-stu-id="ec0c4-107">This can be a single account name or an array of account names.</span></span>

- <span data-ttu-id="ec0c4-108">**. Outputs** – eine Liste von Kontonamen mit der entsprechenden sid in Standard-und hexadezimal Formaten.</span><span class="sxs-lookup"><span data-stu-id="ec0c4-108">**.OUTPUTS** - A list of account names with the corresponding SID in standard and hexadecimal formats.</span></span>

- <span data-ttu-id="ec0c4-109">**Beispiele** -</span><span class="sxs-lookup"><span data-stu-id="ec0c4-109">**Examples** -</span></span>

    <span data-ttu-id="ec0c4-110">**.\\ConvertToSID.ps1 DOMAIN\\user\ _account1 DOMAIN\\machine\ _account1 $ DOMAIN\\user\ _account2 | Format – Liste**.</span><span class="sxs-lookup"><span data-stu-id="ec0c4-110">**.\\ConvertToSID.ps1 DOMAIN\\user\_account1 DOMAIN\\machine\_account1$ DOMAIN\\user\_account2 | Format-List**.</span></span>

    **<span data-ttu-id="ec0c4-111">$accountsArray = @ ("DOMAIN\\user\ _account1"; "DOMAIN\\machine\ _account1 $"; "Domäne \ _User \ _account2")</span><span class="sxs-lookup"><span data-stu-id="ec0c4-111">$accountsArray = @("DOMAIN\\user\_account1", "DOMAIN\\machine\_account1$", "DOMAIN\_user\_account2")</span></span>**

    **<span data-ttu-id="ec0c4-112">.\\ConvertToSID.ps1 $accountsArray | Write-Output-filepath .\\SIDs.txt-Width 200</span><span class="sxs-lookup"><span data-stu-id="ec0c4-112">.\\ConvertToSID.ps1 $accountsArray | Write-Output -FilePath .\\SIDs.txt -Width 200</span></span>**

## <span data-ttu-id="ec0c4-113">So konvertieren Sie eine beliebige Anzahl von Active Directory-Domänendiensten (AD DS)-Benutzer-oder-Computerkonten in formatierte Sicherheits-IDs (SIDs)</span><span class="sxs-lookup"><span data-stu-id="ec0c4-113">To convert any number of Active Directory Domain Services (AD DS) user or machine accounts into formatted Security Identifiers (SIDs)</span></span>

1. <span data-ttu-id="ec0c4-114">Kopieren Sie das folgende Skript in einen Text-Editor, und speichern Sie es als PowerShell-Skriptdatei, beispielsweise **ConvertToSIDs.ps1**.</span><span class="sxs-lookup"><span data-stu-id="ec0c4-114">Copy the following script into a text editor and save it as a PowerShell script file, for example **ConvertToSIDs.ps1**.</span></span>
1. <span data-ttu-id="ec0c4-115">Klicken Sie auf **Start** , und geben Sie **PowerShell**ein, um eine PowerShell-Konsole zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ec0c4-115">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="ec0c4-116">Klicken Sie mit der rechten Maustaste auf **Windows PowerShell**, und wählen Sie **Als Administrator ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec0c4-116">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span>

   ```powershell
   <#
   .SYNOPSIS
   This PowerShell script will take an array of account names and try to convert each of them to the corresponding SID in standard and hexadecimal formats.
   .DESCRIPTION
   This is a PowerShell script that converts any number of Active Directory (AD) user or machine accounts into formatted Security Identifiers (SIDs) both in the standard format and in the hexadecimal format used by SQL server when running SQL scripts.
   .INPUTS
   The account(s) to convert to SID format. This can be a single account name or an array of account names. Please see examples below.
   .OUTPUTS
   A list of account names with the corresponding SID in standard and hexadecimal formats
   .EXAMPLE
   .\ConvertToSID.ps1 DOMAIN\user_account1 DOMAIN\machine_account1$ DOMAIN\user_account2 | Format-List
   .EXAMPLE
   $accountsArray = @("DOMAIN\user_account1", "DOMAIN\machine_account1$", "DOMAIN_user_account2")
   .\ConvertToSID.ps1 $accountsArray | Write-Output -FilePath .\SIDs.txt -Width 200
   #>

   function ConvertSIDToHexFormat
   {

      param([System.Security.Principal.SecurityIdentifier]$sidToConvert)

      $sb = New-Object System.Text.StringBuilder
      [int] $binLength = $sidToConvert.BinaryLength
      [Byte[]] $byteArray = New-Object Byte[] $binLength
      $sidToConvert.GetBinaryForm($byteArray, 0)
      foreach($byte in $byteArray)
      {
          $sb.Append($byte.ToString("X2")) |Out-Null
      }
      return $sb.ToString()
   }
    [string[]]$myArgs = $args
   if(($myArgs.Length -lt 1) -or ($myArgs[0].CompareTo("/?") -eq 0))
   {

    [string]::Format("{0}====== Description ======{0}{0}" +
                  "  Converts any number of user or machine account names to string and hexadecimal SIDs.{0}" +
                  "  Pass the account(s) as space separated command line parameters. (For example 'ConvertToSID.ps1 DOMAIN\Account1 DOMAIN\Account2 ...'){0}" +
                  "  The output is written to the console in the format 'Account name    SID as string   SID as hexadecimal'{0}" +
                  "  And can be written out to a file using standard PowerShell redirection{0}" +
                  "  Please specify user accounts in the format 'DOMAIN\username'{0}" +
                  "  Please specify machine accounts in the format 'DOMAIN\machinename$'{0}" +
                  "  For more help content, please run 'Get-Help ConvertToSID.ps1'{0}" +
                  "{0}====== Arguments ======{0}" +
                  "{0}  /?    Show this help message", [Environment]::NewLine)
   }
   else
   {
       #If an array was passed in, try to split it
       if($myArgs.Length -eq 1)
       {
           $myArgs = $myArgs.Split(' ')
       }

       #Parse the arguments for account names
       foreach($accountName in $myArgs)
       {
           [string[]] $splitString = $accountName.Split('\')  # We're looking for the format "DOMAIN\Account" so anything that does not match, we reject
           if($splitString.Length -ne 2)
           {
               $message = [string]::Format("{0} is not a valid account name. Expected format 'Domain\username' for user accounts or 'DOMAIN\machinename$' for machine accounts.", $accountName)
               Write-Error -Message $message
               continue
           }

           #Convert any account names to SIDs
           try
           {
               [System.Security.Principal.NTAccount] $account = New-Object System.Security.Principal.NTAccount($splitString[0], $splitString[1])
               [System.Security.Principal.SecurityIdentifier] $SID = [System.Security.Principal.SecurityIdentifier]($account.Translate([System.Security.Principal.SecurityIdentifier]))
           }
           catch [System.Security.Principal.IdentityNotMappedException]
           {
               $message = [string]::Format("Failed to translate account object '{0}' to a SID. Please verify that this is a valid user or machine account.", $account.ToString())
               Write-Error -Message $message
               continue
           }

           #Convert regular SID to binary format used by SQL
           $hexSIDString = ConvertSIDToHexFormat $SID

           $SIDs = New-Object PSObject
           $SIDs | Add-Member NoteProperty Account $accountName
           $SIDs | Add-Member NoteProperty SID $SID.ToString()
           $SIDs | Add-Member NoteProperty Hexadecimal $hexSIDString

           Write-Output $SIDs
       }
   }
   ```

1. <span data-ttu-id="ec0c4-117">Führen Sie das Skript aus, das Sie in Schritt 1 dieses Verfahrens gespeichert haben, und übergeben Sie die Konten, um Sie als Argumente zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="ec0c4-117">Run the script you saved in step one of this procedure passing the accounts to convert as arguments.</span></span>

   <span data-ttu-id="ec0c4-118">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ec0c4-118">For example,</span></span>

   **<span data-ttu-id="ec0c4-119">.\\ConvertToSID.ps1 DOMAIN\\user\ _account1 DOMAIN\\machine\ _account1 $ DOMAIN\\user\ _account2 | Format – Liste</span><span class="sxs-lookup"><span data-stu-id="ec0c4-119">.\\ConvertToSID.ps1 DOMAIN\\user\_account1 DOMAIN\\machine\_account1$ DOMAIN\\user\_account2 | Format-List</span></span>**
   
   <span data-ttu-id="ec0c4-120">oder</span><span class="sxs-lookup"><span data-stu-id="ec0c4-120">or</span></span>
   
   <span data-ttu-id="ec0c4-121">**$accountsArray = @ ("DOMAIN\\user\ _account1"; "DOMAIN\\machine\ _account1 $"; "Domäne \ _User \ _account2")** 
    **.\\ConvertToSID.ps1 $accountsArray | Write-Output-filepath .\\SIDs.txt-Width 200**</span><span class="sxs-lookup"><span data-stu-id="ec0c4-121">**$accountsArray = @("DOMAIN\\user\_account1", "DOMAIN\\machine\_account1$", "DOMAIN\_user\_account2")**
 **.\\ConvertToSID.ps1 $accountsArray | Write-Output -FilePath .\\SIDs.txt -Width 200**</span></span>

**<span data-ttu-id="ec0c4-122">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="ec0c4-122">Got an App-V issue?</span></span>** <span data-ttu-id="ec0c4-123">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="ec0c4-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ec0c4-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ec0c4-124">Related topics</span></span>

[<span data-ttu-id="ec0c4-125">Verwalten von App-V 5.1 mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="ec0c4-125">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)
