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
# Unterstützung für Clientberichterstellung über HTTP


Version 4,6 des App-V-Clients unterstützt jetzt die Verwendung der HTTP-Kommunikation beim Senden von Client Berichterstattungsdaten an den Veröffentlichungsserver. Dieses Feature unterstützt Szenarien, in denen ein Kunde einen benutzerdefinierten HTTP (S)-Veröffentlichungsserver implementiert hat, der zum Sammeln und Verarbeiten von Client Daten konfiguriert ist.

Weitere Informationen zu http-Veröffentlichungsservern finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=157426>

## Client Berichterstattung über http


Der Client beginnt mit dem Sammeln von Daten, wenn ein "Reporting =" true ""-Attribut im XML-Veröffentlichungs Antwort-XML vom Veröffentlichungsserver empfangen wird. Wenn dieses Attribut empfangen wird, sendet der Client alle akkumulierten Daten an den Veröffentlichungsserver, der die Veröffentlichungsaktualisierung gesendet hat. Die Details dieses Prozesses lauten wie folgt:

-   Der Client sendet eine HTTP GET-Anforderung an den Veröffentlichungsserver für eine Veröffentlichungsaktualisierung. Die Kopfzeile dieser Nachricht enthält einen benutzerdefinierten Header "AppV-op: Refresh", den der benutzerdefinierte HTTP (S)-Veröffentlichungsserver verwendet, um den Nachrichtentyp zu identifizieren.

-   Der Veröffentlichungsserver sendet dann das XML für die Veröffentlichungs Aktualisierungs Antwort, das einen "Reporting =" true ""-Wert enthält.

-   Der Client sendet dann eine HTTP POST-Anforderung an den Veröffentlichungsserver zusammen mit den Berichterstattungsdaten, die seit der vorherigen Aktualisierung gesammelt wurden. Die Kopfzeile dieser Nachricht enthält einen benutzerdefinierten "AppV-op: Report"-Header, den der benutzerdefinierte HTTP (S)-Veröffentlichungsserver verwendet, um den Nachrichtentyp zu identifizieren.

Das folgende Schema gibt bestimmte Details des Pakets und die Anwendungsdaten an, die an den Server gesendet werden.

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

 

 





