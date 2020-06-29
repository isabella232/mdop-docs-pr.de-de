---
title: Unterstützung für Clientberichterstellung über HTTP
description: Unterstützung für Clientberichterstellung über HTTP
author: dansimp
ms.assetid: 4a26ac80-1fb5-4c05-83de-4d06793f7bf2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4e1759bb4df39ac403e2837c4083275a8b3436f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806247"
---
# <span data-ttu-id="51566-103">Unterstützung für Clientberichterstellung über HTTP</span><span class="sxs-lookup"><span data-stu-id="51566-103">Support for Client Reporting over HTTP</span></span>


<span data-ttu-id="51566-104">Version 4,6 des App-V-Clients unterstützt jetzt die Verwendung der HTTP-Kommunikation beim Senden von Client Berichterstattungsdaten an den Veröffentlichungsserver.</span><span class="sxs-lookup"><span data-stu-id="51566-104">Version 4.6 of the App-V client now supports the use of HTTP communication when sending client reporting data to the publishing server.</span></span> <span data-ttu-id="51566-105">Dieses Feature unterstützt Szenarien, in denen ein Kunde einen benutzerdefinierten HTTP (S)-Veröffentlichungsserver implementiert hat, der zum Sammeln und Verarbeiten von Client Daten konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="51566-105">This feature supports scenarios where a customer has implemented a custom HTTP(S) publishing server that is configured to collect and process client data.</span></span>

<span data-ttu-id="51566-106">Weitere Informationen zu http-Veröffentlichungsservern finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="51566-106">For more information on HTTP publishing servers, see</span></span> <https://go.microsoft.com/fwlink/?LinkId=157426>

## <span data-ttu-id="51566-107">Client Berichterstattung über http</span><span class="sxs-lookup"><span data-stu-id="51566-107">Client Reporting over HTTP</span></span>


<span data-ttu-id="51566-108">Der Client beginnt mit dem Sammeln von Daten, wenn ein "Reporting =" true ""-Attribut im XML-Veröffentlichungs Antwort-XML vom Veröffentlichungsserver empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="51566-108">The client starts collecting data when it receives a “REPORTING=”TRUE””attribute in the publishing refresh response XML from the publishing server.</span></span> <span data-ttu-id="51566-109">Wenn dieses Attribut empfangen wird, sendet der Client alle akkumulierten Daten an den Veröffentlichungsserver, der die Veröffentlichungsaktualisierung gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="51566-109">When this attribute is received, the client sends any accumulated data to the publishing server that sent the publishing refresh.</span></span> <span data-ttu-id="51566-110">Die Details dieses Prozesses lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="51566-110">The details of this process are as follows:</span></span>

-   <span data-ttu-id="51566-111">Der Client sendet eine HTTP GET-Anforderung an den Veröffentlichungsserver für eine Veröffentlichungsaktualisierung.</span><span class="sxs-lookup"><span data-stu-id="51566-111">The client sends an HTTP GET request to the publishing server for a publishing refresh.</span></span> <span data-ttu-id="51566-112">Die Kopfzeile dieser Nachricht enthält einen benutzerdefinierten Header "AppV-op: Refresh", den der benutzerdefinierte HTTP (S)-Veröffentlichungsserver verwendet, um den Nachrichtentyp zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="51566-112">The header of this message contains an “AppV-Op:Refresh” custom header that the custom HTTP(S) publishing server uses to identify the message type.</span></span>

-   <span data-ttu-id="51566-113">Der Veröffentlichungsserver sendet dann das XML für die Veröffentlichungs Aktualisierungs Antwort, das einen "Reporting =" true ""-Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="51566-113">The publishing server then sends the publishing refresh response XML that contains a “REPORTING=”TRUE”” value.</span></span>

-   <span data-ttu-id="51566-114">Der Client sendet dann eine HTTP POST-Anforderung an den Veröffentlichungsserver zusammen mit den Berichterstattungsdaten, die seit der vorherigen Aktualisierung gesammelt wurden.</span><span class="sxs-lookup"><span data-stu-id="51566-114">The client then sends an HTTP POST request to the publishing server along with the reporting data that has been gathered since the previous refresh.</span></span> <span data-ttu-id="51566-115">Die Kopfzeile dieser Nachricht enthält einen benutzerdefinierten "AppV-op: Report"-Header, den der benutzerdefinierte HTTP (S)-Veröffentlichungsserver verwendet, um den Nachrichtentyp zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="51566-115">The header of this message contains an “AppV-Op:Report” custom header that the custom HTTP(S) publishing server uses to identify the message type.</span></span>

<span data-ttu-id="51566-116">Das folgende Schema gibt bestimmte Details des Pakets und die Anwendungsdaten an, die an den Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="51566-116">The following schema gives specific details of the package and the application data that is sent to the server.</span></span>

```xml
<?xml version="1.0"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:element name="CLIENT_DATA">
        <xs:complexType>
            <xs:all>
                <xs:element ref="PKG_LIST" minOccurs="1" maxOccurs="1"/>
                <xs:element ref="APP_RECORDS" minOccurs="1" maxOccurs="1"/>
            </xs:all>
            <!-- no regex for Ver because we want to allow tags like "Beta" -->
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Host" type="xs:token" use="required"/>
            <xs:attribute name="CacheSize" type="xs:nonNegativeInteger" use="required"/>
            <xs:attribute name="CacheUsed" type="xs:nonNegativeInteger" use="required"/>
        </xs:complexType>
    </xs:element>

    <xs:element name="PKG_LIST">
        <xs:complexType>
            <xs:choice>
                <xs:element ref="PKG_DATA" minOccurs="0" maxOccurs="unbounded"/>
            </xs:choice>
        </xs:complexType>
    </xs:element>

    <xs:element name="PKG_DATA">
        <xs:complexType>
            <xs:attribute name="Name" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Guid" type="xs:token" use="required"/>
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="VerGuid" type="xs:token" use="required"/>
            <xs:attribute name="Source" type="xs:normalizedString" use="required"/>
            <xs:attribute name="PctCached" use="required">
                <xs:simpleType>
                    <xs:restriction base="xs:nonNegativeInteger">
                        <xs:minInclusive value="0"/>
                        <xs:maxInclusive value="100"/>
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:complexType>
    </xs:element>

    <xs:element name="APP_RECORDS">
         <xs:complexType>
            <xs:choice>
                <xs:element ref="APP_RECORD" minOccurs="0" maxOccurs="unbounded"/>
            </xs:choice>
        </xs:complexType>
   </xs:element>

    <xs:element name="APP_RECORD">
            <xs:attribute name="Name" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Server" type="xs:normalizedString" use="required"/>
            <xs:attribute name="User" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Launched" type="xs:dateTime" use="required"/>
            <xs:attribute name="Shutdown" type="xs:dateTime" use="optional"/>
    </xs:element>

</xs:schema>
```

 

 





