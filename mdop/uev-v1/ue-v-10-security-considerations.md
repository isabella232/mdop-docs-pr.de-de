---
title: Sicherheitsüberlegungen für UE-V 1.0
description: Sicherheitsüberlegungen für UE-V 1.0
author: dansimp
ms.assetid: c5cdf9ff-dc96-4491-98e9-0eada898ffe0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b503028ae327f92759fe0f64f33fe0cffc62b05c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810291"
---
# <span data-ttu-id="9982d-103">Sicherheitsüberlegungen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="9982d-103">UE-V 1.0 Security Considerations</span></span>


<span data-ttu-id="9982d-104">Dieses Thema enthält eine kurze Übersicht über Konten und Gruppen, Protokolldateien und andere sicherheitsrelevante Überlegungen für Microsoft User Experience Virtualization (UE-V).</span><span class="sxs-lookup"><span data-stu-id="9982d-104">This topic contains a brief overview of accounts and groups, log files, and other security-related considerations for Microsoft User Experience Virtualization (UE-V).</span></span> <span data-ttu-id="9982d-105">Wenn Sie weitere Informationen wünschen, folgen Sie den Links, die hier bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9982d-105">For more information, follow the links that are provided here.</span></span>

## <span data-ttu-id="9982d-106">Sicherheitsüberlegungen für die UE-V-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="9982d-106">Security considerations for UE-V configuration</span></span>


**<span data-ttu-id="9982d-107">Wenn Sie die Speicherfreigabe für Einstellungen erstellen, beschränken Sie den Freigabe Zugriff auf Benutzer, die Zugriff benötigen.</span><span class="sxs-lookup"><span data-stu-id="9982d-107">When you create the settings storage share, limit the share access to users that need access.</span></span>**

<span data-ttu-id="9982d-108">Da Einstellungs Pakete personenbezogene Informationen enthalten können, sollten Sie darauf achten, diese so gut wie möglich zu schützen.</span><span class="sxs-lookup"><span data-stu-id="9982d-108">Because settings packages may contain personal information, you should take care to protect them as well as possible.</span></span> <span data-ttu-id="9982d-109">Gehen Sie im Allgemeinen wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="9982d-109">In general, do the following:</span></span>

-   <span data-ttu-id="9982d-110">Beschränken Sie die Freigabe auf die Benutzer, die Zugriff benötigen.</span><span class="sxs-lookup"><span data-stu-id="9982d-110">Restrict the share to only the users that need access.</span></span> <span data-ttu-id="9982d-111">Erstellen Sie eine Sicherheitsgruppe für Benutzer, die Ordner auf einer bestimmten Freigabe umgeleitet haben, und beschränken Sie den Zugriff auf diese Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9982d-111">Create a security group for users that have redirected folders on a particular share, and limit access to only those users.</span></span>

-   <span data-ttu-id="9982d-112">Wenn Sie die Freigabe erstellen, blenden Sie die Freigabe aus, indem Sie einen $ hinter den Freigabenamen setzen.</span><span class="sxs-lookup"><span data-stu-id="9982d-112">When you create the share, hide the share by putting a $ after the share name.</span></span> <span data-ttu-id="9982d-113">Dadurch wird die Freigabe aus beiläufigen Browsern ausgeblendet, und die Freigabe wird in "meine Netzwerkumgebung" nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9982d-113">This will hide the share from casual browsers, and the share will not be visible in My Network Places.</span></span>

-   <span data-ttu-id="9982d-114">Gewähren Sie Benutzern nur die Mindestberechtigungen, die erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9982d-114">Only give users the minimum amount of permissions needed.</span></span> <span data-ttu-id="9982d-115">Die erforderlichen Berechtigungen werden in den folgenden Tabellen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9982d-115">The permissions needed are shown in the tables below.</span></span>

    1.  <span data-ttu-id="9982d-116">Legen Sie die folgenden SMB-Berechtigungen (Freigabeebene) für den Ordner für die Einstellung des Speicherorts fest:</span><span class="sxs-lookup"><span data-stu-id="9982d-116">Set the following share-level (SMB) permissions for the setting storage location folder:</span></span>

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><span data-ttu-id="9982d-117">Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="9982d-117">User account</span></span></th>
        <th align="left"><span data-ttu-id="9982d-118">Empfohlene Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="9982d-118">Recommended permissions</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="9982d-119">Jeder</span><span class="sxs-lookup"><span data-stu-id="9982d-119">Everyone</span></span></p></td>
        <td align="left"><p><span data-ttu-id="9982d-120">Keine Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="9982d-120">No Permissions</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="9982d-121">Sicherheitsgruppe UE-V</span><span class="sxs-lookup"><span data-stu-id="9982d-121">Security group of UE-V</span></span></p></td>
        <td align="left"><p><span data-ttu-id="9982d-122">Vollzugriff</span><span class="sxs-lookup"><span data-stu-id="9982d-122">Full Control</span></span></p></td>
        </tr>
        </tbody>
        </table>



~~~
2.  Set the following NTFS permissions for the settings storage location folder:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Folder</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Admins</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Security group of UE-V users</p></td>
    <td align="left"><p>List Folder/Read Data, Create Folders/Append Data</p></td>
    <td align="left"><p>This Folder Only</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>Remove all Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    </tbody>
    </table>



3.  Set the following share-level (SMB) permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommend permissions</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>Read Permission Levels</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Read/Write Permission Levels</p></td>
    </tr>
    </tbody>
    </table>



4.  Set the following NTFS permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Apply to</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>List Folder Contents and Read</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    </tbody>
    </table>
~~~



### <span data-ttu-id="9982d-123">Verwenden von Servern mit Windows Server 2003 oder höher zum Hosten umgeleiteter Dateifreigaben</span><span class="sxs-lookup"><span data-stu-id="9982d-123">Use Windows Server 2003 or later servers to host redirected file shares</span></span>

<span data-ttu-id="9982d-124">Benutzereinstellungen-Paketdateien enthalten persönliche Informationen, die zwischen dem Clientcomputer und dem Server, auf dem die Einstellungs Pakete gespeichert sind, übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="9982d-124">User settings package files contain personal information that is transferred between the client computer and the server that stores the settings packages.</span></span> <span data-ttu-id="9982d-125">Aus diesem Grund sollten Sie sicherstellen, dass die Daten geschützt sind, während Sie über das Netzwerk transportiert werden.</span><span class="sxs-lookup"><span data-stu-id="9982d-125">Because of this, you should ensure that the data is protected while it travels over the network.</span></span>

<span data-ttu-id="9982d-126">Benutzereinstellungsdaten sind anfällig für diese potenziellen Bedrohungen: Abfangen der Daten, die über das Netzwerk geleitet werden. Manipulation der Daten bei der über das Netzwerk übertragenen Daten; und Spoofing des Servers, der die Daten hostet.</span><span class="sxs-lookup"><span data-stu-id="9982d-126">User settings data is vulnerable to these potential threats: interception of the data as it passes over the network; tampering with the data as it passes over the network; and spoofing of the server that hosts the data.</span></span>

<span data-ttu-id="9982d-127">Verschiedene Features von Windows Server 2003 und höher können dazu beitragen, Benutzerdaten zu schützen:</span><span class="sxs-lookup"><span data-stu-id="9982d-127">Several features of Windows Server 2003 and above can help to secure user data:</span></span>

-   <span data-ttu-id="9982d-128">**Kerberos** -Kerberos ist in allen Versionen von Windows 2000 und Windows Server 2003 und höher Standard.</span><span class="sxs-lookup"><span data-stu-id="9982d-128">**Kerberos** - Kerberos is standard on all versions of Windows 2000 and Windows Server 2003 and later.</span></span> <span data-ttu-id="9982d-129">Kerberos gewährleistet die höchste Sicherheitsstufe für Netzwerkressourcen.</span><span class="sxs-lookup"><span data-stu-id="9982d-129">Kerberos ensures the highest level of security to network resources.</span></span> <span data-ttu-id="9982d-130">NTLM authentifiziert nur den Client; Kerberos authentifiziert den Server und den Client.</span><span class="sxs-lookup"><span data-stu-id="9982d-130">NTLM authenticates the client only; Kerberos authenticates the server and the client.</span></span> <span data-ttu-id="9982d-131">Wenn NTLM verwendet wird, weiß der Client nicht, ob der Server gültig ist.</span><span class="sxs-lookup"><span data-stu-id="9982d-131">When NTLM is used, the client does not know whether the server is valid.</span></span> <span data-ttu-id="9982d-132">Dies ist besonders wichtig, wenn der Client persönliche Dateien mit dem Server austauscht, wie dies bei Roaming-Profilen der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="9982d-132">This is particularly important if the client is exchanging personal files with the server, as is the case with Roaming Profiles.</span></span> <span data-ttu-id="9982d-133">Kerberos bietet eine bessere Sicherheit als NTLM.</span><span class="sxs-lookup"><span data-stu-id="9982d-133">Kerberos provides better security than NTLM.</span></span> <span data-ttu-id="9982d-134">Kerberos steht unter Windows NT, Version 4,0 oder früheren Betriebssystemen, nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9982d-134">Kerberos is not available on Windows NT version 4.0 or earlier operating systems.</span></span>

-   <span data-ttu-id="9982d-135">**IPSec** – das IP-Sicherheitsprotokoll (IPSec) bietet Authentifizierung auf Netzwerkebene, Datenintegrität und Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="9982d-135">**IPsec** - The IP Security Protocol (IPsec) provides network-level authentication, data integrity, and encryption.</span></span> <span data-ttu-id="9982d-136">IPSec stellt Folgendes sicher:</span><span class="sxs-lookup"><span data-stu-id="9982d-136">IPsec ensures the following:</span></span>

    -   <span data-ttu-id="9982d-137">Roaming-Daten sind während der Weiterleitung sicher vor Datenänderungen.</span><span class="sxs-lookup"><span data-stu-id="9982d-137">Roamed data is safe from data modification while en route.</span></span>

    -   <span data-ttu-id="9982d-138">Roaming-Daten sind sicher vor dem Abfangen, anzeigen oder kopieren.</span><span class="sxs-lookup"><span data-stu-id="9982d-138">Roamed data is safe from interception, viewing, or copying.</span></span>

    -   <span data-ttu-id="9982d-139">Auf Roaming-Daten kann nicht authentifizierte Personen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9982d-139">Roamed data is safe from being accessed by unauthenticated parties.</span></span>

-   <span data-ttu-id="9982d-140">**SMB-Signierung** : das SMB-Authentifizierungsprotokoll (Server Message Block) unterstützt die Nachrichtenauthentifizierung, die eine aktive Nachricht und "man-in-the-Middle"-Angriffe verhindert.</span><span class="sxs-lookup"><span data-stu-id="9982d-140">**SMB Signing** - The Server Message Block (SMB) authentication protocol supports message authentication which prevents active message and "man-in-the-middle" attacks.</span></span> <span data-ttu-id="9982d-141">Die SMB-Signierung bietet diese Authentifizierung, indem eine digitale Signatur in jedem SMB platziert wird.</span><span class="sxs-lookup"><span data-stu-id="9982d-141">SMB signing provides this authentication by placing a digital signature into each SMB.</span></span> <span data-ttu-id="9982d-142">Die digitale Signatur wird dann sowohl vom Client als auch vom Server überprüft.</span><span class="sxs-lookup"><span data-stu-id="9982d-142">The digital signature is then verified by both the client and the server.</span></span> <span data-ttu-id="9982d-143">Um die SMB-Signierung verwenden zu können, müssen Sie Sie zuerst entweder aktivieren oder auf dem SMB-Client und dem SMB-Server anfordern.</span><span class="sxs-lookup"><span data-stu-id="9982d-143">In order to use SMB signing, you must first either enable it or require it on both the SMB client and the SMB server.</span></span> <span data-ttu-id="9982d-144">Beachten Sie, dass bei der SMB-Signierung eine Leistungs Verhängung erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="9982d-144">Note that the SMB signing imposes a performance penalty.</span></span> <span data-ttu-id="9982d-145">Sie verbraucht keine Netzwerkbandbreite, beansprucht aber mehr CPU-Zyklen auf Client-und Serverseite.</span><span class="sxs-lookup"><span data-stu-id="9982d-145">It does not consume any more network bandwidth, but it uses more CPU cycles on the client and server side.</span></span>

### <span data-ttu-id="9982d-146">Verwenden Sie immer das NTFS-Dateisystem für Volumes, in denen Benutzerdaten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="9982d-146">Always use the NTFS File system for volumes holding users data</span></span>

<span data-ttu-id="9982d-147">Konfigurieren Sie für die sicherste Konfiguration Server, die die UE-V-Einstellungsdateien hosten, um das NTFS-Datei System zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9982d-147">For the most secure configuration, configure servers that host the UE-V settings files to use the NTFS File System.</span></span> <span data-ttu-id="9982d-148">Im Gegensatz zu FAT unterstützt NTFS Discretionary Access Control Lists (DACLs) und System Access Control Lists (SACLs).</span><span class="sxs-lookup"><span data-stu-id="9982d-148">Unlike FAT, NTFS supports Discretionary access control lists (DACLs) and system access control lists (SACLs).</span></span> <span data-ttu-id="9982d-149">DACLs und SACLs steuern, wer Vorgänge für eine Datei ausführen kann und welche Ereignisse die Protokollierung von Aktionen auslösen, die für eine Datei ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9982d-149">DACLs and SACLs control who can perform operations on a file and what events will trigger the logging of actions performed on a file.</span></span>

### <a href="" id="do-not-rely-on-efs-to-encrypt-users--files-when-transmitted-over-the-network"></a><span data-ttu-id="9982d-150">Verlassen Sie sich nicht auf EFS, um die Dateien von Benutzern zu verschlüsseln, wenn Sie über das Netzwerk gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9982d-150">Do not rely on EFS to encrypt users’ files when transmitted over the network</span></span>

<span data-ttu-id="9982d-151">Wenn Sie EFS (Encrypting File System) zum Verschlüsseln von Dateien auf einem Remoteserver verwenden, werden die verschlüsselten Daten während der Übertragung über das Netzwerk nicht verschlüsselt. Sie wird nur verschlüsselt, wenn Sie auf einem Datenträger gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9982d-151">When you use Encrypting File System (EFS) to encrypt files on a remote server, the encrypted data is not encrypted during transit over the network; It only becomes encrypted when stored on disk.</span></span>

<span data-ttu-id="9982d-152">Die Ausnahmen sind, wenn Ihr System IPSec (Internet Protocol Security) oder WebDAV (Web Distributed Authoring and Versioning) umfasst.</span><span class="sxs-lookup"><span data-stu-id="9982d-152">The exceptions to this are when your system includes Internet Protocol security (IPsec) or Web Distributed Authoring and Versioning (WebDAV).</span></span> <span data-ttu-id="9982d-153">IPSec verschlüsselt Daten, während Sie über ein TCP/IP-Netzwerk transportiert werden.</span><span class="sxs-lookup"><span data-stu-id="9982d-153">IPsec encrypts data while it is transported over a TCP/IP network.</span></span> <span data-ttu-id="9982d-154">Wenn die Datei verschlüsselt ist, bevor Sie kopiert oder in einen WebDAV-Ordner auf einem Server verschoben wird, bleibt Sie während der Übertragung verschlüsselt und wird auf dem Server gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9982d-154">If the file is encrypted before being copied or moved to a WebDAV folder on a server, it will remain encrypted during the transmission and while it is stored on the server.</span></span>

### <span data-ttu-id="9982d-155">Verschlüsseln des Offline Dateicaches</span><span class="sxs-lookup"><span data-stu-id="9982d-155">Encrypt the Offline Files cache</span></span>

<span data-ttu-id="9982d-156">Standardmäßig ist der Cache für Offline Dateien durch ACLs auf NTFS-Partitionen geschützt, aber durch die Verschlüsselung des Caches wird die Sicherheit auf einem lokalen Computer weiter verbessert.</span><span class="sxs-lookup"><span data-stu-id="9982d-156">By default, the Offline Files cache is protected on NTFS partitions by ACLs, but encrypting the cache further enhances security on a local computer.</span></span> <span data-ttu-id="9982d-157">Standardmäßig ist der Cache auf dem lokalen Computer nicht verschlüsselt, sodass alle im Netzwerk zwischengespeicherten verschlüsselten Dateien auf dem lokalen Computer nicht verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="9982d-157">By default, the cache on the local computer is not encrypted, so any encrypted files cached from the network will not be encrypted on the local computer.</span></span> <span data-ttu-id="9982d-158">Dies kann in einigen Umgebungen ein Sicherheitsrisiko darstellen.</span><span class="sxs-lookup"><span data-stu-id="9982d-158">This may pose a security risk in some environments.</span></span>

<span data-ttu-id="9982d-159">Wenn die Verschlüsselung aktiviert ist, werden alle Dateien im Offline Dateicache verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="9982d-159">When encryption is enabled, all files in the Offline Files cache are encrypted.</span></span> <span data-ttu-id="9982d-160">Dies umfasst das Verschlüsseln vorhandener Dateien sowie von Dateien, die später hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9982d-160">This includes encrypting existing files as well as files that are added later.</span></span> <span data-ttu-id="9982d-161">Die zwischengespeicherte Kopie auf dem lokalen Computer ist betroffen, die zugehörige Netzwerkkopie jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="9982d-161">The cached copy on the local computer is affected, but the associated network copy is not.</span></span>

<span data-ttu-id="9982d-162">Der Cache kann auf eine von zwei Arten verschlüsselt werden:</span><span class="sxs-lookup"><span data-stu-id="9982d-162">The cache can be encrypted in one of two ways:</span></span>

1.  <span data-ttu-id="9982d-163">Über Gruppenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="9982d-163">Via Group Policy.</span></span> <span data-ttu-id="9982d-164">– Aktivieren Sie im Gruppenrichtlinien-Editor die Einstellung **Offline Datei-Cache verschlüsseln** , die sich auf Computer Configuration\\Administrative Templates\\Network\\Offline-Dateien befindet.</span><span class="sxs-lookup"><span data-stu-id="9982d-164">- Enable the **Encrypt the Offline Files Cache** setting, located at Computer Configuration\\Administrative Templates\\Network\\Offline Files, in the Group Policy editor.</span></span>

2.  <span data-ttu-id="9982d-165">Manuell.</span><span class="sxs-lookup"><span data-stu-id="9982d-165">Manually.</span></span> <span data-ttu-id="9982d-166">– Wählen Sie im Windows-Explorer im Befehlsmenü Extras und dann Ordneroptionen aus.</span><span class="sxs-lookup"><span data-stu-id="9982d-166">- Select Tools and then Folder Options in the command menu of Windows Explorer.</span></span> <span data-ttu-id="9982d-167">Wählen Sie die Registerkarte Offlinedateien aus, und aktivieren Sie dann das Kontrollkästchen **Offlinedateien zum Sichern von Daten verschlüsseln** .</span><span class="sxs-lookup"><span data-stu-id="9982d-167">Select the Offline Files tab, and then select the **Encrypt offline files to secure data** check box.</span></span>

### <span data-ttu-id="9982d-168">Der UE-V-Agent soll Ordner für jeden Benutzer erstellen</span><span class="sxs-lookup"><span data-stu-id="9982d-168">Let the UE-V Agent create folders for each user</span></span>

<span data-ttu-id="9982d-169">Um sicherzustellen, dass UE-v optimal funktioniert, erstellen Sie nur die Stammfreigabe auf dem Server, und lassen Sie den UE-v-Agent die Ordner für jeden Benutzer erstellen.</span><span class="sxs-lookup"><span data-stu-id="9982d-169">To ensure that UE-V works optimally, create only the root share on the server, and let the UE-V Agent create the folders for each user.</span></span> <span data-ttu-id="9982d-170">In UE-V werden diese Benutzerordner mit der entsprechenden Sicherheit erstellt.</span><span class="sxs-lookup"><span data-stu-id="9982d-170">UE-V will create these user folders with the appropriate security.</span></span>

<span data-ttu-id="9982d-171">Diese Berechtigungskonfiguration ermöglicht Benutzern das Erstellen von Ordnern für den Einstellungsspeicher.</span><span class="sxs-lookup"><span data-stu-id="9982d-171">This permission configuration allows users to create folders for settings storage.</span></span> <span data-ttu-id="9982d-172">Der UE-V-Agent erstellt und sichert einen settingspackage-Ordner, während er im Kontext des Benutzers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9982d-172">The UE-V agent creates and secures a settingspackage folder while running in the context of the user.</span></span> <span data-ttu-id="9982d-173">Der Benutzer erhält Vollzugriff auf seinen settingspackage-Ordner.</span><span class="sxs-lookup"><span data-stu-id="9982d-173">The user receives full control to their settingspackage folder.</span></span> <span data-ttu-id="9982d-174">Andere Benutzer erben keinen Zugriff auf diesen Ordner.</span><span class="sxs-lookup"><span data-stu-id="9982d-174">Other users do not inherit access to this folder.</span></span> <span data-ttu-id="9982d-175">Es ist nicht erforderlich, einzelne Benutzerverzeichnisse zu erstellen und zu sichern.</span><span class="sxs-lookup"><span data-stu-id="9982d-175">You do not need to create and secure individual user directories.</span></span> <span data-ttu-id="9982d-176">Dies erfolgt automatisch durch den Agenten, der im Kontext des Benutzers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9982d-176">This will be done automatically by the agent that runs in the context of the user.</span></span>

**<span data-ttu-id="9982d-177">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="9982d-177">Note</span></span>**  
<span data-ttu-id="9982d-178">Zusätzliche Sicherheit kann konfiguriert werden, wenn ein Windows-Server für die Speicherfreigabe "Einstellungen" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9982d-178">Additional security can be configured when a Windows server is utilized for the settings storage share.</span></span> <span data-ttu-id="9982d-179">UE-V kann so konfiguriert werden, dass entweder die Gruppe des lokalen Administrators oder der aktuelle Benutzer der Besitzer des Ordners ist, in dem die Einstellungs Pakete gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="9982d-179">UE-V can be configured to verify that either the local administrator's group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="9982d-180">Verwenden Sie den folgenden Befehl, um zusätzliche Sicherheit zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="9982d-180">To enable additional security use the following command:</span></span>

1.  <span data-ttu-id="9982d-181">Fügen Sie einen Registrierungsschlüssel "reg \ _DWORD" mit dem Namen "RepositoryOwnerCheckEnabled" hinzu `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="9982d-181">Add a REG\_DWORD registry key named "RepositoryOwnerCheckEnabled" to `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="9982d-182">Stellen Sie den Registrierungsschlüsselwert auf 1 ein.</span><span class="sxs-lookup"><span data-stu-id="9982d-182">Set registry key value to 1.</span></span>

<span data-ttu-id="9982d-183">Wenn diese Konfigurationseinstellung eingerichtet ist, überprüft der UE-V-Agent, ob die Gruppe des lokalen Administrators oder der aktuelle Benutzer der Besitzer des settingspackage-Ordners ist.</span><span class="sxs-lookup"><span data-stu-id="9982d-183">When this configuration setting is in place, the UE-V agent verifies that the local administrator’s group or current user is the owner of the settingspackage folder.</span></span> <span data-ttu-id="9982d-184">Wenn dies nicht der Fall ist, ermöglicht der UE-V-Agent keinen Zugriff auf den Ordner.</span><span class="sxs-lookup"><span data-stu-id="9982d-184">If not, then the UE-V agent will not allow access to the folder.</span></span>



<span data-ttu-id="9982d-185">Wenn Sie Ordner für die Benutzer erstellen müssen, und stellen Sie sicher, dass Sie die richtigen Berechtigungen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9982d-185">If you must create folders for the users and ensure that you have the correct permissions set.</span></span>

<span data-ttu-id="9982d-186">Wir empfehlen dringend, dass Sie keine Ordner vorerstellen und stattdessen dem UE-V-Agent das Erstellen des Ordners für den Benutzer gestatten.</span><span class="sxs-lookup"><span data-stu-id="9982d-186">We strongly recommend that you do not precreate folders and that instead, you allow the UE-V agent to create the folder for the user.</span></span>

### <a href="" id="ensure-that-correct-permissions-are-set-when-storing-ue-v-settings-in-a-user-s-home-directory"></a><span data-ttu-id="9982d-187">Sicherstellen, dass die richtigen Berechtigungen beim Speichern der UE-V-Einstellungen im Basisverzeichnis eines Benutzers festgesetzt werden</span><span class="sxs-lookup"><span data-stu-id="9982d-187">Ensure that correct permissions are set when storing UE-V settings in a user’s home directory</span></span>

<span data-ttu-id="9982d-188">Wenn Sie die UE-V-Einstellungen in das private Verzeichnis eines Benutzers umleiten, stellen Sie sicher, dass die Berechtigungen für das private Verzeichnis des Benutzers für Ihre Organisation entsprechend festgesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="9982d-188">If you redirect UE-V settings to a user’s home directory, be sure that the permissions on the user's home directory are set appropriately for your organization.</span></span>

## <span data-ttu-id="9982d-189">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9982d-189">Related topics</span></span>


[<span data-ttu-id="9982d-190">Sicherheit und Datenschutz für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="9982d-190">Security and Privacy for UE-V 1.0</span></span>](security-and-privacy-for-ue-v-10.md)









