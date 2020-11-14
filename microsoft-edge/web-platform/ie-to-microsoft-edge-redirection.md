---
description: Verschieben von Benutzern aus dem Internet Explorer nach Microsoft Edge
title: Verschieben von Benutzern aus dem Internet Explorer nach Microsoft Edge
author: MSEdgeTeam
ms.date: 11/13/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: Microsoft Edge, Kompatibilität, Web-Plattform, Internet Explorer
ms.openlocfilehash: 872bd5ec52f471e4958ef7354c046ec30f1ba72e
ms.sourcegitcommit: 62258ce0ef469948ca8af42141d02aa9719243f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2020
ms.locfileid: "11168365"
---
# Verschieben von Benutzern aus dem Internet Explorer nach Microsoft Edge  

Viele moderne Websites verfügen über Designs, die mit Internet Explorer \ (IE \) nicht kompatibel sind.  Wenn ein IE-Benutzer eine inkompatible öffentliche Website besucht, erhält der Benutzer möglicherweise eine Nachricht.  In der Meldung wird angegeben, dass die Website mit dem Browser nicht kompatibel ist.  Nachdem die Nachricht angezeigt wurde, wird erwartet, dass der Benutzer manuell zu einem modernen Browser wechselt.  Um Unterbrechungen zu minimieren, beginnend mit Version 84, unterstützt Microsoft Edge eine neue Funktion, die Benutzer automatisch umleitet.  Wenn ein IE-Benutzer zu einer Website navigiert, die mit IE nicht kompatibel ist, leitet Windows den Benutzer automatisch an Microsoft Edge um.  Wenn Sie die Websites in der Liste überprüfen möchten, navigieren Sie zu [benötigen Sie Microsoft Edge-Liste][MicrosoftEdgeNeededgeV1].

In diesem Artikel werden die folgenden Konzepte beschrieben:  

*   Gründe für das Hinzufügen einer Website zur Liste  
*   Die Benutzeroberfläche für die Umleitung  
*   Anfordern eines Updates für die Liste  
    
## Warum wird eine Website zur IE-Kompatibilitätsliste hinzugefügt?  

Die IE-Kompatibilitätsliste fügt nur dann eine Website hinzu, wenn die folgenden Aktionen ausgeführt werden.  

*   Zeigt einem IE-Benutzer eine Nachricht, die darauf hinweist, dass der Benutzer aus Kompatibilitätsgründen einen anderen Browser verwenden soll.  
*   Besitzer Anforderungen zum Hinzufügen der Website zur IE-Kompatibilitätsliste.  

## Umleitungserfahrung

Bei der Umleitung zu Microsoft Edge wird dem Benutzer das einmalige Dialogfeld im nächsten Screenshot angezeigt.  Das Dialogfeld bietet dem Benutzer die folgenden Informationen.  

*   Es wird erläutert, warum die Website umgeleitet wird.  
*   Sie fordert den Benutzer zur Genehmigung auf, Daten und Einstellungen für das Browsen von IE zu Microsoft Edge zu kopieren.  

:::row:::
   :::column span="":::
      Die folgenden Browserdaten werden importiert.  
      
      *   Favoriten  
      *   Kennwörter  
      *   Suchmaschinen  
      *   Offene Registerkarten  
      *   Verlauf  
      *   Einstellungen  
      *   Cookies  
      *   Die Startseite  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Durchsuchen der Benachrichtigung und Aufforderung zum Importieren von Daten und Einstellungen" lightbox="../media/neededge-dialog1.msft.png":::
         Durchsuchen der Benachrichtigung und Aufforderung zum Importieren von Daten und Einstellungen  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Wenn der Benutzer nicht einverstanden ist, indem er das Kontrollkästchen **immer über meine Browserdaten und-Einstellungen aus Internet Explorer über** tragen auswählt, kann der Benutzer " **Continue Browsing**" auswählen,   um die Browsersitzung fortzusetzen.  

Schließlich wird für jede Umleitung unter der Adressleiste eine Website-Inkompatibilitäts-Banner angezeigt.  Ein Beispiel für ein Website-Inkompatibilitäts-Banner wird in der folgenden Abbildung angezeigt.

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Benachrichtigung über moderne Websites und Aufforderung zum Festlegen von Microsoft Edge als Standardbrowser oder erkunden von Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   Benachrichtigung über moderne Websites und Aufforderung zum Festlegen von Microsoft Edge als Standardbrowser oder erkunden von Microsoft Edge  
:::image-end:::

Das Banner "Website-Inkompatibilität" bietet dem Benutzer die folgenden Informationen.  

*   Empfiehlt dem Benutzer, zu Microsoft Edge zu wechseln.  
*   Bietet an, Microsoft Edge als Standardbrowser einzurichten.  
*   Bietet dem Benutzer die Möglichkeit, Microsoft Edge zu erkunden.    
    
Wenn eine Website von Internet Explorer zu Microsoft Edge umgeleitet wird, erfolgt eine der folgenden Aktionen.

*   Wenn die aktive IE-Registerkarte keinen vorherigen Inhalt aufweist, wird Sie geschlossen.  
*   Wenn die aktive IE-Registerkarte vorherigen Inhalt aufweist, navigiert Sie zur [Microsoft-Support Seite, in der erläutert wird, warum die Website an Microsoft Edge umgeleitet wurde][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].  

> [!NOTE]
> Nach einer Umleitung können Benutzer IE weiterhin für Websites verwenden, die nicht in der IE-Kompatibilitätsliste enthalten sind.  

## Anfordern eines Updates für die IE-Kompatibilitätsliste  

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

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "Die Website, die Sie erreichen wollten, funktioniert nicht mit Internet Explorer | Microsoft Office-Support"  
