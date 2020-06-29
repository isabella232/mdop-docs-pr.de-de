---
title: Planen der Administratorrollen für MBAM 2.0
description: Planen der Administratorrollen für MBAM 2.0
author: dansimp
ms.assetid: 6f813297-6479-42d3-a21b-896d54466b5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a89a04c0ef074407dc3cd081d351d44023e65e70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810828"
---
# Planen der Administratorrollen für MBAM 2.0


In diesem Thema werden die verfügbaren Administratorrollen aufgelistet und beschrieben, die in Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) sowie die Serverspeicherorte, an denen die lokalen Gruppen erstellt werden, verfügbar sind.

## MBAM-Administrator Rollen


<a href="" id="---------------mbam-system-administrators"></a> **MBAM-System Administratoren**  
Administratoren in dieser Rolle haben Zugriff auf alle Features der Microsoft BitLocker-Verwaltung und-Überwachung. Die lokale Gruppe für diese Rolle ist auf dem Verwaltungs-und Überwachungs Server installiert.

<a href="" id="---------------mbam-helpdesk-users"></a> **MBAM Helpdesk-Benutzer**  
Administratoren in dieser Rolle haben Zugriff auf die Helpdesk-Features von MBAM. Die lokale Gruppe für diese Rolle ist auf dem Verwaltungs-und Überwachungs Server installiert.

<a href="" id="---------------mbam-report-users"></a> **MBAM-Berichtsbenutzer**  
Administratoren in dieser Rolle haben Zugriff auf die Konformitäts-und Überwachungsberichte von MBAM. Die lokale Gruppe für diese Rolle ist auf der Verwaltungs-und Überwachungsserver-, Konformitäts-und Überwachungsdatenbank sowie auf dem Server installiert, auf dem die Konformitäts-und Überwachungsberichte gehostet werden.

<a href="" id="---------------mbam-advanced-helpdesk-users"></a> **MBAM Advanced Helpdesk-Benutzer**  
Administratoren in dieser Rolle haben erhöhten Zugriff auf die Helpdesk-Features von MBAM. Die lokale Gruppe für diese Rolle ist auf dem Verwaltungs-und Überwachungs Server installiert. Wenn ein Benutzer Mitglied sowohl von MBAM Helpdesk-Benutzern als auch von MBAM Advanced Helpdesk-Benutzern ist, überschreibt die MBAM Advanced Helpdesk-Benutzerberechtigungen die Benutzerberechtigungen des MBAM-Helpdesks.

**Wichtig**  Damit Berichte angezeigt werden können, muss ein Administrator ein Mitglied der Sicherheitsgruppe **MBAM-Berichtsbenutzer** in den Verwaltungs-und Überwachungsserver-, Konformitäts-und Überwachungsdatenbanken sowie auf dem Server sein, der das Feature Konformitäts-und Überwachungsberichte hostet. Als bewährte Methode können Sie eine Sicherheitsgruppe in Active Directory-Domänendiensten mit Rechten für die Sicherheitsgruppe **MBAM-Berichtsbenutzer** auf dem Verwaltungs-und Überwachungsserver und dem Server erstellen, auf dem die Konformitäts-und Überwachungsberichte gehostet werden.

 

## Verwandte Themen


[Vorbereiten der Umgebung für MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md)

 

 





