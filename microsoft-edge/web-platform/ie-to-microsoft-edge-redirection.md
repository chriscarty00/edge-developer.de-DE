---
description: Verschieben von Benutzern aus dem Internet Explorer nach Microsoft Edge
title: Verschieben von Benutzern aus dem Internet Explorer nach Microsoft Edge
author: MSEdgeTeam
ms.date: 11/06/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: Microsoft Edge, Kompatibilität, Web-Plattform, Internet Explorer
ms.openlocfilehash: 2e1488359e405247e290ad8f6300c480a7e20af6
ms.sourcegitcommit: 6ef48c8cda392c6bf8217cff5f696ac620d10739
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2020
ms.locfileid: "11163206"
---
# Verschieben von Benutzern aus dem Internet Explorer nach Microsoft Edge 

Viele moderne Websites verfügen über Designs, die mit Internet Explorer \ (IE \) nicht kompatibel sind.  Wenn ein IE-Benutzer eine inkompatible öffentliche Website besucht, erhält der Benutzer möglicherweise eine Nachricht.  In der Meldung wird angegeben, dass die Website mit dem Browser nicht kompatibel ist.  Nachdem die Nachricht angezeigt wurde, wird erwartet, dass der Benutzer manuell zu einem modernen Browser wechselt.  Um Unterbrechungen zu minimieren, beginnend mit Version 84, unterstützt Microsoft Edge eine neue Funktion, die Benutzer automatisch umleitet.  Wenn ein IE-Benutzer zu einer Website navigiert, die mit IE nicht kompatibel ist, leitet Windows den Benutzer automatisch an Microsoft Edge um.  Wenn Sie die Websites in der Liste überprüfen möchten, navigieren Sie zu [benötigen Sie Microsoft Edge-Liste][MicrosoftEdgeNeededgeV1].

In diesem Artikel werden die folgenden Konzepte beschrieben:  

*   Die Benutzeroberfläche für die Umleitung  
*   Anfordern eines Updates für die Liste  
    
## Warum wird eine Website zur IE-Kompatibilitätsliste hinzugefügt?  

Die IE-Kompatibilitätsliste fügt nur dann eine Website hinzu, wenn die folgenden Aktionen ausgeführt werden.  

*   Zeigt einem IE-Benutzer eine Nachricht, die darauf hinweist, dass der Benutzer aus Kompatibilitätsgründen einen anderen Browser verwenden soll.  
*   Besitzer Anforderungen zum Hinzufügen der Website zur IE-Kompatibilitätsliste.  
    
## Aktualisieren der IE-Kompatibilitätsliste  

Die IE-Kompatibilitätsliste ist eine XML-Datei auf [Microsoft.com][MicrosoftOfficialHome].  Die Liste wird regelmäßig als Antwort auf Benutzer-und Websiteentwickler Anforderungen aktualisiert, damit Websites hinzugefügt oder entfernt werden.  Aktualisierungen der Liste werden automatisch auf Benutzer Computer heruntergeladen.  

Senden Sie die folgenden Informationen an [ietoedge@Microsoft.com][MailtoMicrosoftIetoedge] , damit Ihre Website aus der IE-Kompatibilitätsliste hinzugefügt oder entfernt wird.    

*   Name des Besitzers  
*   Unternehmens Titel  
*   E-Mail-Adresse  
*   Name des Unternehmens  
*   Straße  
*   Website Adresse  
    
> [!NOTE]
> Die IE-Kompatibilitätsliste ist für die Zusammenarbeit mit öffentlichen Websites vorgesehen.  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Senden einer e-Mail an ietoedge@Microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Microsoft Official Home"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Benötigen Sie Microsoft Edge List v1 XML | Microsoft Edge"  
