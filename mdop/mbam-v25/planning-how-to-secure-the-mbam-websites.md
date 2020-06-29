---
title: Planen der Sicherung von MBAM-Websites
description: Planen der Sicherung von MBAM-Websites
author: dansimp
ms.assetid: aea1d137-62cf-4da4-9989-541e0b5ad8d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 223c9397ad7933e11051c289c3dbcab63940fbc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810906"
---
# <span data-ttu-id="c2844-103">Planen der Sicherung von MBAM-Websites</span><span class="sxs-lookup"><span data-stu-id="c2844-103">Planning How to Secure the MBAM Websites</span></span>


<span data-ttu-id="c2844-104">In diesem Thema werden die folgenden Methoden zum Sichern der Microsoft BitLocker-Verwaltungs-und-Überwachungs Website (MBAM) 2,5-Website und des Self-Service-Portals beschrieben:</span><span class="sxs-lookup"><span data-stu-id="c2844-104">This topic describes the following methods for securing the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Administration and Monitoring Website and Self-Service Portal:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2844-105">Methode</span><span class="sxs-lookup"><span data-stu-id="c2844-105">Method</span></span></th>
<th align="left"><span data-ttu-id="c2844-106">Erforderlich oder optional?</span><span class="sxs-lookup"><span data-stu-id="c2844-106">Required or optional?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2844-107">Verwenden von Zertifikaten zum Sichern von MBAM-Websites</span><span class="sxs-lookup"><span data-stu-id="c2844-107">Using certificates to secure MBAM websites</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2844-108">Optional, aber sehr empfehlenswert</span><span class="sxs-lookup"><span data-stu-id="c2844-108">Optional, but highly recommended</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2844-109">Registrieren von Dienstprinzipalnamen (Service Principal Names, SPN) für das Anwendungspoolkonto</span><span class="sxs-lookup"><span data-stu-id="c2844-109">Registering Service Principal Names (SPN) for the application pool account</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2844-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c2844-110">Required</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="c2844-111">Weitere Informationen zum Sichern Ihrer MBAM-Bereitstellung finden Sie unter [Sicherheitsüberlegungen zu MBAM 2,5](mbam-25-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="c2844-111">For more information about how to secure your MBAM deployment, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md).</span></span>

## <span data-ttu-id="c2844-112">Verwenden von Zertifikaten zum Sichern von MBAM-Websites</span><span class="sxs-lookup"><span data-stu-id="c2844-112">Using certificates to secure MBAM websites</span></span>


<span data-ttu-id="c2844-113">Wir empfehlen, dass Sie ein Zertifikat verwenden, um die Kommunikation zwischen den folgenden zu sichern:</span><span class="sxs-lookup"><span data-stu-id="c2844-113">We recommend that you use a certificate to secure the communication between the:</span></span>

-   <span data-ttu-id="c2844-114">MBAM-Client und die Webdienste</span><span class="sxs-lookup"><span data-stu-id="c2844-114">MBAM Client and the web services</span></span>

-   <span data-ttu-id="c2844-115">Browser und die Website "Verwaltung und Überwachung" sowie die Websites des Self-Service-Portals</span><span class="sxs-lookup"><span data-stu-id="c2844-115">Browser and the Administration and Monitoring Website and the Self-Service Portal websites</span></span>

<span data-ttu-id="c2844-116">Informationen zum Anfordern und Installieren eines Zertifikats finden Sie unter [Konfigurieren von Internet Server Zertifikaten](https://technet.microsoft.com/library/cc731977.aspx).</span><span class="sxs-lookup"><span data-stu-id="c2844-116">For information about requesting and installing a certificate, see [Configuring Internet Server Certificates](https://technet.microsoft.com/library/cc731977.aspx).</span></span>

**<span data-ttu-id="c2844-117">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="c2844-117">Note</span></span>**  
<span data-ttu-id="c2844-118">Sie können die Websites und Webdienste auf unterschiedlichen Servern nur konfigurieren, wenn Sie Windows PowerShell verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2844-118">You can configure the websites and web services on different servers only if you are using Windows PowerShell.</span></span> <span data-ttu-id="c2844-119">Wenn Sie den MBAM-Serverkonfigurations-Assistenten zum Konfigurieren der Websites verwenden, müssen Sie die Websites und die Webdienste auf demselben Server konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c2844-119">If you use the MBAM Server Configuration wizard to configure the websites, you must configure the websites and the web services on the same server.</span></span>



<span data-ttu-id="c2844-120">Um die Kommunikation zwischen den Webdiensten und den Datenbanken zu sichern, sollten Sie auch die Verschlüsselung in SQL Server erzwingen.</span><span class="sxs-lookup"><span data-stu-id="c2844-120">To secure the communication between the web services and the databases, we also recommend that you force encryption in SQL Server.</span></span> <span data-ttu-id="c2844-121">Informationen zum Sichern aller Verbindungen mit SQL Server, einschließlich der Kommunikation zwischen den Webdiensten und SQL Server, finden Sie unter [MBAM 2,5-Sicherheitsüberlegungen](mbam-25-security-considerations.md#bkmk-secure-databases).</span><span class="sxs-lookup"><span data-stu-id="c2844-121">For information about securing all connections to SQL Server, including communication between the web services and SQL Server, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-secure-databases).</span></span>

## <span data-ttu-id="c2844-122">Registrieren von SPNs für das Anwendungspoolkonto</span><span class="sxs-lookup"><span data-stu-id="c2844-122">Registering SPNs for the application pool account</span></span>


<span data-ttu-id="c2844-123">Damit die MBAM-Server die Kommunikation über die Verwaltungs-und Überwachungs Website und das Self-Service-Portal authentifizieren können, müssen Sie einen Dienstprinzipalnamen (Service Principal Name, SPN) für den Hostnamen unter dem Domänenkonto registrieren, das Sie für den Webanwendungspool verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2844-123">To enable the MBAM Servers to authenticate communication from the Administration and Monitoring Website and the Self-Service Portal, you must register a Service Principal Name (SPN) for the host name under the domain account that you are using for the web application pool.</span></span>

<span data-ttu-id="c2844-124">In diesem Thema finden Sie Anweisungen zum Registrieren von SPNs für die folgenden Typen von Host Namen:</span><span class="sxs-lookup"><span data-stu-id="c2844-124">This topic contains instructions on how to register SPNs for the following types of host names:</span></span>

-   <span data-ttu-id="c2844-125">Vollständig qualifizierter Domänenname</span><span class="sxs-lookup"><span data-stu-id="c2844-125">Fully qualified domain name</span></span>

-   <span data-ttu-id="c2844-126">NetBIOS-Name</span><span class="sxs-lookup"><span data-stu-id="c2844-126">NetBIOS name</span></span>

-   <span data-ttu-id="c2844-127">Virtueller Name</span><span class="sxs-lookup"><span data-stu-id="c2844-127">Virtual name</span></span>

### <span data-ttu-id="c2844-128">Vor dem Erstellen von SPNs für eine anfängliche MBAM-Installation</span><span class="sxs-lookup"><span data-stu-id="c2844-128">Before you create SPNs for an initial MBAM installation</span></span>

<span data-ttu-id="c2844-129">Überprüfen Sie die Informationen in der folgenden Tabelle, bevor Sie mit dem Erstellen von SPNs beginnen.</span><span class="sxs-lookup"><span data-stu-id="c2844-129">Review the information in the following table before you start creating SPNs.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2844-130">Aufgabe oder Element</span><span class="sxs-lookup"><span data-stu-id="c2844-130">Task or item</span></span></th>
<th align="left"><span data-ttu-id="c2844-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c2844-131">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2844-132">Erstellen Sie ein Dienstkonto in Active Directory-Domänendienste (AD DS).</span><span class="sxs-lookup"><span data-stu-id="c2844-132">Create a service account in Active Directory Domain Services (AD DS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2844-133">Das Dienstkonto ist ein Benutzerkonto, das Sie in AD DS erstellen, um Sicherheit für die MBAM-Websites bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c2844-133">The service account is a user account that you create in AD DS to provide security for the MBAM websites.</span></span> <span data-ttu-id="c2844-134">Die MBAM-Websites werden unter einem Anwendungspool ausgeführt, dessen Identität der Name des Dienstkontos ist.</span><span class="sxs-lookup"><span data-stu-id="c2844-134">The MBAM websites run under an application pool, whose identity is the name of the service account.</span></span> <span data-ttu-id="c2844-135">Die SPNs werden dann im Anwendungspoolkonto registriert.</span><span class="sxs-lookup"><span data-stu-id="c2844-135">The SPNs are then registered in the application pool account.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c2844-136">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="c2844-136">Note</span></span></strong><br/><p><span data-ttu-id="c2844-137">Sie müssen dasselbe Anwendungspoolkonto für alle Webserver verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2844-137">You must use the same application pool account for all web servers.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2844-138">Vergewissern Sie sich, dass entweder das IIS-IUSRS-Gruppenkonto oder das Anwendungspoolkonto über die erforderlichen Rechte verfügen.</span><span class="sxs-lookup"><span data-stu-id="c2844-138">Verify that either the IIS-IUSRS group account or the application pool account has been granted the necessary rights.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2844-139">Führen Sie die folgenden Schritte aus, um dies zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="c2844-139">To check this, follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="c2844-140">Öffnen Sie den <strong> lokalen Sicherheitsrichtlinien-Editor </strong> , und erweitern Sie den <strong> Knoten Lokale Richtlinien </strong> .</span><span class="sxs-lookup"><span data-stu-id="c2844-140">Open the <strong>Local Security Policy editor</strong> and expand the <strong>Local Policies</strong> node.</span></span></p></li>
<li><p><span data-ttu-id="c2844-141">Wählen Sie den <strong> Knoten Benutzerrechtezuweisung aus </strong> , und doppelklicken Sie <strong> im rechten Bereich auf die Gruppenrichtlinieneinstellungen für den Identitätswechsel eines Clients nach Authentifizierung </strong> und <strong> Anmeldung als Stapelverarbeitungsauftrag </strong> .</span><span class="sxs-lookup"><span data-stu-id="c2844-141">Select the <strong>User Rights Assignment</strong> node, and double-click the <strong>Impersonate a client after authentication</strong> and <strong>Log on as a batch job</strong> Group Policy settings in the right pane.</span></span></p></li>
</ol></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2844-142">Wenn Sie die MBAM-Websites mithilfe eines Domänenadministratorkontos konfigurieren, erstellt MBAM die SPNs für Sie.</span><span class="sxs-lookup"><span data-stu-id="c2844-142">If you configure the MBAM websites by using a domain administrative account, MBAM will create the SPNs for you.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2844-143">Wenn Sie die MBAM-Websites mithilfe eines Domänenadministratorkontos konfigurieren, führen Sie die Schritte in diesem Thema aus, um SPNs für den Typ des verwendeten Hostnamens manuell zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="c2844-143">If you configure the MBAM websites by using a domain administrative account, follow the steps in this topic to register SPNs manually for the type of host name that you are using.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="c2844-144">Registrieren von SPNs, wenn Sie einen vollqualifizierten Domänenhost Namen verwenden</span><span class="sxs-lookup"><span data-stu-id="c2844-144">Registering SPNs when you use a fully qualified domain host name</span></span>

<span data-ttu-id="c2844-145">Wenn Sie bei der Konfiguration von MBAM einen vollqualifizierten Domänenhost Namen verwenden, müssen Sie nur einen SPN registrieren, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c2844-145">If you use a fully qualified domain host name when you configure MBAM, you have to register only one SPN, as shown in the following example.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2844-146">Was Sie tun müssen</span><span class="sxs-lookup"><span data-stu-id="c2844-146">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="c2844-147">Beispiele und weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c2844-147">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2844-148">Registrieren Sie einen SPN für den vollqualifizierten Domänennamen.</span><span class="sxs-lookup"><span data-stu-id="c2844-148">Register an SPN for the fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mybitlockerrecovery.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="c2844-149">Der vollqualifizierte Hostname lautet <strong> mybitlockerrecovery.contoso.com </strong> , und das für den Webanwendungspool verwendete Domänenkonto ist <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="c2844-149">The fully qualified host name is <strong>mybitlockerrecovery.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2844-150">Konfigurieren Sie die beschränkte Delegierung für den SPN, den Sie für das Anwendungspoolkonto registrieren.</span><span class="sxs-lookup"><span data-stu-id="c2844-150">Configure constrained delegation for the SPN that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="c2844-151">Konfigurieren der beschränkten Delegierung</span><span class="sxs-lookup"><span data-stu-id="c2844-151">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="c2844-152">Diese Anforderung gilt nur für MBAM 2,5; in MBAM 2,5 SP1 ist dies nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c2844-152">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="c2844-153">Registrieren von SPNs bei Verwendung eines NetBIOS-Hostnamens</span><span class="sxs-lookup"><span data-stu-id="c2844-153">Registering SPNs when you use a NetBIOS host name</span></span>

<span data-ttu-id="c2844-154">Wenn Sie bei der Konfiguration von MBAM einen NetBIOS-Hostnamen verwenden, registrieren Sie einen SPN für den NetBIOS-Namen und einen weiteren SPN für den vollqualifizierten Domänennamen, wie in den folgenden Beispielen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c2844-154">If you use a NetBIOS host name when you configure MBAM, register one SPN for the NetBIOS name, and another SPN for the fully qualified domain name, as shown in the following examples.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2844-155">Was Sie tun müssen</span><span class="sxs-lookup"><span data-stu-id="c2844-155">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="c2844-156">Beispiele und weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c2844-156">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2844-157">Registrieren Sie einen SPN für den NetBIOS-Host Namen.</span><span class="sxs-lookup"><span data-stu-id="c2844-157">Register an SPN for the NetBIOS host name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/nbname01 contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="c2844-158">Der NetBIOS-Hostname lautet <strong> nbname01 </strong> , und das für den Webanwendungspool verwendete Domänenkonto ist <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="c2844-158">The NetBIOS host name is <strong>nbname01</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2844-159">Registrieren Sie einen SPN für den vollqualifizierten Domänennamen.</span><span class="sxs-lookup"><span data-stu-id="c2844-159">Register an SPN for the fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn –s http/nbname01.corp.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="c2844-160">Der vollqualifizierte Domänenname lautet <strong> nbname01.contoso.com </strong> , und das für den Webanwendungspool verwendete Domänenkonto ist <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="c2844-160">The fully qualified domain name is <strong>nbname01.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2844-161">Konfigurieren Sie die beschränkte Delegierung für die SPNs, die Sie für das Anwendungspoolkonto registrieren.</span><span class="sxs-lookup"><span data-stu-id="c2844-161">Configure constrained delegation for the SPNs that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="c2844-162">Konfigurieren der beschränkten Delegierung</span><span class="sxs-lookup"><span data-stu-id="c2844-162">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="c2844-163">Diese Anforderung gilt nur für MBAM 2,5; in MBAM 2,5 SP1 ist dies nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c2844-163">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-regvirtualspn"></a><span data-ttu-id="c2844-164">Registrieren von SPNs bei Verwendung eines virtuellen Hostnamens</span><span class="sxs-lookup"><span data-stu-id="c2844-164">Registering SPNs when you use a virtual host name</span></span>

<span data-ttu-id="c2844-165">Wenn Sie MBAM mit einem virtuellen Hostnamen konfigurieren, bei dem es sich um einen vollqualifizierten Domänennamen handelt, registrieren Sie nur einen SPN für den virtuellen Host Namen.</span><span class="sxs-lookup"><span data-stu-id="c2844-165">If you configure MBAM with a virtual host name that is a fully qualified domain name, register only one SPN for the virtual host name.</span></span> <span data-ttu-id="c2844-166">Wenn es sich bei dem von Ihnen konfigurierten virtuellen Host Namen nicht um einen vollqualifizierten Domänennamen handelt, müssen Sie einen zweiten SPN erstellen, der den vollqualifizierten Domänennamen angibt, wie in den folgenden Beispielen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c2844-166">If the virtual host name that you configure is not a fully qualified domain name, you must create a second SPN that specifies the fully qualified domain name, as described in the following examples.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2844-167">Was Sie tun müssen</span><span class="sxs-lookup"><span data-stu-id="c2844-167">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="c2844-168">Beispiele und weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c2844-168">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2844-169">Wenn der Name Ihres virtuellen Hosts ein vollständig qualifizierter Domänenname ist, wie in diesem Beispiel, registrieren Sie nur einen SPN.</span><span class="sxs-lookup"><span data-stu-id="c2844-169">If your virtual host name is a fully qualified domain name, as in this example, register only one SPN.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="c2844-170">Im Beispiel lautet der Name des virtuellen Hosts <strong> mbamvirtual.contoso.com </strong> , und das für den Webanwendungspool verwendete Domänenkonto ist <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="c2844-170">In the example, the virtual host name is <strong>mbamvirtual.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2844-171">Registrieren Sie diesen zusätzlichen SPN, wenn der Name Ihres virtuellen Hosts kein vollqualifizierter Domänenname ist.</span><span class="sxs-lookup"><span data-stu-id="c2844-171">Register this additional SPN if your virtual host name is not a fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="c2844-172">Im Beispiel lautet der Name des virtuellen Hosts <strong> mbamvirtual </strong> , und das für den Webanwendungspool verwendete Domänenkonto ist <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="c2844-172">In the example, the virtual host name is <strong>mbamvirtual</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2844-173">Registrieren Sie diesen zusätzlichen SPN, wenn der Name Ihres virtuellen Hosts kein vollqualifizierter Domänenname ist.</span><span class="sxs-lookup"><span data-stu-id="c2844-173">Register this additional SPN if your virtual host name is not a fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="c2844-174">Im Beispiel lautet der Name des virtuellen Hosts <strong> mbamvirtual.contoso.com </strong> , und das für den Webanwendungspool verwendete Domänenkonto ist <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="c2844-174">In the example, the virtual host name is <strong>mbamvirtual.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2844-175">Erstellen Sie auf dem Domain Nameserver (DNS)-Server einen "A Record" für den benutzerdefinierten Hostnamen, und verweisen Sie auf einen Webserver oder ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="c2844-175">On the Domain Name Server (DNS) server, create an “A record” for the custom host name and point it to a web server or a load balancer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2844-176">Weitere Informationen finden Sie im Abschnitt "so konfigurieren Sie einen DNS-Host für Datensätze" unter <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)"> Konfigurieren von DNS-Hosteinträgen </a> .</span><span class="sxs-lookup"><span data-stu-id="c2844-176">See the “To configure DNS Host A Records” section in <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)">Configure DNS Host Records</a>.</span></span></p>
<p><span data-ttu-id="c2844-177">Wir empfehlen, anstelle von CNAMEs Datensätze zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2844-177">We recommend that you use A records instead of CNAMES.</span></span> <span data-ttu-id="c2844-178">Wenn Sie CNAMEs verwenden, um auf die Domänenadresse zu verweisen, müssen Sie auch SPNs für den Webservernamen im Anwendungspoolkonto registrieren.</span><span class="sxs-lookup"><span data-stu-id="c2844-178">If you use CNAMES to point to the domain address, you must also register SPNs for the web server name in the application pool account.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2844-179">Konfigurieren Sie die beschränkte Delegierung für die SPNs, die Sie für das Anwendungspoolkonto registrieren.</span><span class="sxs-lookup"><span data-stu-id="c2844-179">Configure constrained delegation for the SPNs that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="c2844-180">Konfigurieren der beschränkten Delegierung</span><span class="sxs-lookup"><span data-stu-id="c2844-180">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="c2844-181">Diese Anforderung gilt nur für MBAM 2,5; in MBAM 2,5 SP1 ist dies nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c2844-181">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-registerspn"></a><span data-ttu-id="c2844-182">Registrieren eines SPN beim Upgrade von vorherigen Versionen von MBAM</span><span class="sxs-lookup"><span data-stu-id="c2844-182">Registering an SPN when you upgrade from previous versions of MBAM</span></span>

<span data-ttu-id="c2844-183">Führen Sie die Schritte in diesem Abschnitt nur aus, wenn Sie Folgendes tun möchten:</span><span class="sxs-lookup"><span data-stu-id="c2844-183">Complete the steps in this section only if you want to:</span></span>

-   <span data-ttu-id="c2844-184">Upgrade von einer früheren Version von MBAM.</span><span class="sxs-lookup"><span data-stu-id="c2844-184">Upgrade from a previous version of MBAM.</span></span>

-   <span data-ttu-id="c2844-185">Führen Sie die Websites in MBAM 2,5 in einer Lastenausgleichs-oder verteilten Konfiguration aus, und Sie werden derzeit in einer Konfiguration ausgeführt, die nicht Lastenausgleich ist.</span><span class="sxs-lookup"><span data-stu-id="c2844-185">Run the websites in MBAM 2.5 in a load-balanced or distributed configuration, and you are currently running in a configuration that is not load balanced.</span></span>

<span data-ttu-id="c2844-186">Wenn Sie SPNs bereits auf dem Computerkonto und nicht in einem Anwendungspoolkonto registriert haben, verwendet MBAM die vorhandenen SPNs, und Sie können die Websites nicht in einer Lastenausgleich-oder verteilten Konfiguration konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c2844-186">If you already registered SPNs on the machine account rather than in an application pool account, MBAM uses the existing SPNs, and you cannot configure the websites in a load-balanced or distributed configuration.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2844-187">Was Sie tun müssen</span><span class="sxs-lookup"><span data-stu-id="c2844-187">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="c2844-188">Beispiele und weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c2844-188">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2844-189">Erstellen Sie ein Anwendungspoolkonto in Active Directory-Domänendienste (AD DS).</span><span class="sxs-lookup"><span data-stu-id="c2844-189">Create an application pool account in Active Directory Domain Services (AD DS).</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2844-190">Entfernen Sie die aktuell installierten Websites und Webdienste.</span><span class="sxs-lookup"><span data-stu-id="c2844-190">Remove the currently installed websites and web services.</span></span></p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)"><span data-ttu-id="c2844-191">Entfernen von MBAM-Serverfunktionen oder -software</span><span class="sxs-lookup"><span data-stu-id="c2844-191">Removing MBAM Server Features or Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2844-192">Entfernen Sie SPNs aus dem Computerkonto.</span><span class="sxs-lookup"><span data-stu-id="c2844-192">Remove SPNs from the machine account.</span></span></p></td>
<td align="left"><p><code>Setspn –d http/mbamwebserver mbamwebserver</code></p>
<p><code>Setspn –d http/mbamwebserver.contoso.com mbamwebserver</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2844-193">Registrieren Sie SPNs im Anwendungspoolkonto.</span><span class="sxs-lookup"><span data-stu-id="c2844-193">Register SPNs in the application pool account.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2844-194">Führen Sie die Schritte zum <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)"> Registrieren von SPNs aus, wenn Sie einen virtuellen Hostnamen verwenden </a> .</span><span class="sxs-lookup"><span data-stu-id="c2844-194">Follow the steps for <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)">Registering SPNs when you use a virtual host name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2844-195">Konfigurieren Sie die Web Applications und Web Services neu.</span><span class="sxs-lookup"><span data-stu-id="c2844-195">Reconfigure the web applications and web services.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="c2844-196">So konfigurieren Sie die MBAM 2.5-Webanwendungen</span><span class="sxs-lookup"><span data-stu-id="c2844-196">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2844-197">Führen Sie je nach der für die Konfiguration verwendeten Methode eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="c2844-197">Do one of the following, depending on the method you use for the configuration:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2844-198">Methode</span><span class="sxs-lookup"><span data-stu-id="c2844-198">Method</span></span></th>
<th align="left"><span data-ttu-id="c2844-199">Details</span><span class="sxs-lookup"><span data-stu-id="c2844-199">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c2844-200">MBAM-Serverkonfigurations-Assistent</span><span class="sxs-lookup"><span data-stu-id="c2844-200">MBAM Server Configuration wizard</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c2844-201">Geben Sie das Anwendungspoolkonto im <strong> Feld "Domänenkonto" des Webdienst-Anwendungspools ein </strong> .</span><span class="sxs-lookup"><span data-stu-id="c2844-201">Enter the application pool account in the <strong>Web service application pool domain account</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><code>Enable-MbamWebApplication</code> <span data-ttu-id="c2844-202">Windows PowerShell-Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2844-202">Windows PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2844-203">Geben Sie das Konto in den <code>WebServiceApplicationPoolCredential</code> Parameter ein.</span><span class="sxs-lookup"><span data-stu-id="c2844-203">Enter the account in the <code>WebServiceApplicationPoolCredential</code> parameter.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="c2844-204">Wichtig</span><span class="sxs-lookup"><span data-stu-id="c2844-204">Important</span></span></strong><br/><p><span data-ttu-id="c2844-205">Der eingegebene Hostname muss mit dem Namen des virtuellen Hosts identisch sein, für den Sie die SPNs erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2844-205">The host name that you enter must be the same name as the virtual host name for which you are creating the SPNs.</span></span> <span data-ttu-id="c2844-206">Außerdem müssen die Hostnamen und die Anmeldeinformationen des Anwendungspools in Ihrer Webfarm auf jedem Server identisch sein, den Sie konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c2844-206">Also, in your web farm, the host names and the application pool credentials must be the same on every server that you are configuring.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="c2844-207">Wenn MBAM die Webanwendungen konfiguriert, versucht Sie, die SPNs für Sie zu registrieren, kann dies aber nur tun, wenn Sie über Domänenadministratorrechte auf dem Server verfügen, auf dem Sie MBAM installieren.</span><span class="sxs-lookup"><span data-stu-id="c2844-207">When MBAM configures the web applications, it will try to register the SPNs for you, but it can do so only if you have Domain Admin rights on the server on which you are installing MBAM.</span></span> <span data-ttu-id="c2844-208">Wenn Sie nicht über diese Rechte verfügen, können Sie die Konfiguration abschließen, aber Sie müssen die SPNs vor oder nach dem Konfigurieren von MBAM festlegen.</span><span class="sxs-lookup"><span data-stu-id="c2844-208">If you do not have these rights, you can complete the configuration, but you will have to set the SPNs before or after you configure MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="c2844-209">Erforderliche Filtereinstellungen für Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2844-209">Required Request Filtering Settings</span></span>

 <span data-ttu-id="c2844-210">"Nicht aufgelistete Dateinamenerweiterungen zulassen" ist erforderlich, damit die Anwendung wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c2844-210">'Allow unlisted file name extensions' is required for the application to operate as expected.</span></span>  <span data-ttu-id="c2844-211">Diese finden Sie unter "Microsoft BitLocker-Verwaltung und-Überwachung" – > Anforderungsfilterung – > Featureeinstellungen bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c2844-211">This can be found by navigating to the 'Microsoft BitLocker Administration and Monitoring' -> Request Filtering -> Edit Feature Settings.</span></span>


## <span data-ttu-id="c2844-212">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c2844-212">Related topics</span></span>


[<span data-ttu-id="c2844-213">Vorbereiten der Umgebung für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c2844-213">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="c2844-214">Bereitstellungsvoraussetzungen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c2844-214">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)





## <span data-ttu-id="c2844-215">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="c2844-215">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="c2844-216">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="c2844-216">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="c2844-217">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="c2844-217">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



