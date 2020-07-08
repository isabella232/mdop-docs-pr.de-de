---
title: Planen der Administratorrollen für MBAM 1.0
description: Planen der Administratorrollen für MBAM 1.0
author: dansimp
ms.assetid: 95be0eb4-25e9-43ca-a8e7-27373d35544d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 104d650824330ea990881c520a7811511f496dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811425"
---
# Planen der Administratorrollen für MBAM 1.0


Dieses Thema enthält und beschreibt die Administratorrollen, die in Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) verfügbar sind, sowie die Serverspeicherorte, an denen die lokalen Gruppen erstellt werden.

## MBAM-Administrator Rollen


<a href="" id="---------------mbam-system-administrators"></a> **MBAM-System Administratoren**  
Administratoren in dieser Rolle haben Zugriff auf alle MBAM-Features. Die lokale Gruppe für diese Rolle ist auf dem Verwaltungs-und Überwachungs Server installiert.

<a href="" id="---------------mbam-hardware-users"></a> **MBAM-Hardware Benutzer**  
Administratoren in dieser Rolle haben Zugriff auf die Features der Hardware Funktion von MBAM. Die lokale Gruppe für diese Rolle ist auf dem Verwaltungs-und Überwachungs Server installiert.

<a href="" id="---------------mbam-helpdesk-users"></a> **MBAM Helpdesk-Benutzer**  
Administratoren in dieser Rolle haben Zugriff auf die Helpdesk-Features von MBAM. Die lokale Gruppe für diese Rolle ist auf dem Verwaltungs-und Überwachungs Server installiert.

<a href="" id="---------------mbam--report-users"></a> **MBAM-Berichtsbenutzer**  
Administratoren in dieser Rolle haben Zugriff auf das Feature Konformitäts-und Überwachungsberichte von MBAM. Die lokale Gruppe für diese Rolle ist auf der Verwaltungs-und Überwachungsserver-, Konformitäts-und Überwachungsdatenbank sowie auf dem Server installiert, auf dem die Konformitäts-und Überwachungsberichte gehostet werden.

<a href="" id="---------------mbam--advanced-helpdesk-users"></a> **MBAM Advanced Helpdesk-Benutzer**  
Administratoren in dieser Rolle haben erhöhten Zugriff auf die Helpdesk-Features von MBAM. Die lokale Gruppe für diese Rolle ist auf dem Verwaltungs-und Überwachungs Server installiert. Wenn ein Benutzer Mitglied sowohl von MBAM Helpdesk-Benutzern als auch von MBAM Advanced Helpdesk-Benutzern ist, überschreibt die Berechtigung MBAM Advanced Helpdesk-Benutzer die Berechtigungen des MBAM-Helpdesk-Benutzers.

**Wichtig**  Damit die Berichte angezeigt werden können, muss ein Administrator ein Mitglied der Sicherheitsgruppe **MBAM-Berichtsbenutzer** in den Verwaltungs-und Überwachungs Servern, der Kompatibilitäts-und Überwachungsdatenbank sowie auf dem Server sein, der das Feature Compliance und Berichte hostet. Als bewährte Methode können Sie eine Sicherheitsgruppe in Active Directory mit Rechten für die lokale **MBAM-Berichtsbenutzer** -Sicherheitsgruppe sowohl auf dem Verwaltungs-und Überwachungsserver als auch auf dem Server erstellen, auf dem die Konformität und die Berichte gehostet werden.

 

## Verwandte Themen


[Vorbereiten der Umgebung für MBAM 1.0](preparing-your-environment-for-mbam-10.md)

 

 





