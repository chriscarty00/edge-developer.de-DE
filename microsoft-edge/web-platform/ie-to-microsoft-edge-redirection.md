---
description: Verschieben von Benutzern zu Microsoft Edge aus Internet Explorer
title: Verschieben von Benutzern zu Microsoft Edge aus Internet Explorer
author: MSEdgeTeam
ms.date: 11/13/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: microsoft edge, compatibility, web platform, internet explorer
ms.openlocfilehash: c2106955ed79bd28dc1f847dee220944bb014689
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461136"
---
# <a name="moving-users-to-microsoft-edge-from-internet-explorer"></a>Verschieben von Benutzern zu Microsoft Edge aus Internet Explorer  

Viele moderne Websites verfügen über Designs, die nicht mit Internet Explorer \(IE\) kompatibel sind.  Wenn ein IE-Benutzer eine inkompatible öffentliche Website besucht, wird dem Benutzer möglicherweise eine Nachricht angezeigt.  Die Meldung besagt, dass die Website nicht mit dem Browser kompatibel ist.  Nachdem die Nachricht angezeigt wurde, wird erwartet, dass der Benutzer manuell zu einem modernen Browser wechselt.  Um Unterbrechungen zu minimieren, unterstützt Microsoft Edge ab Version 84 eine neue Funktion, die Benutzer automatisch umleite.  Wenn ein IE-Benutzer zu einer Website navigiert, die mit IE nicht kompatibel ist, leitet Windows Benutzer automatisch an Microsoft Edge.  Navigieren Sie zum Überprüfen der Websites in der Liste zu [Microsoft Edge Liste .][MicrosoftEdgeNeededgeV1]

In diesem Artikel werden die folgenden Konzepte beschrieben.  

*   Warum eine Website zur Liste hinzugefügt wird  
*   Die Benutzeroberfläche für die Umleitung  
*   Anfordern eines Updates für die Liste  
    
## <a name="why-is-a-website-added-to-the-ie-compatibility-list"></a>Warum wird der IE-Kompatibilitätsliste eine Website hinzugefügt?  

Die IE-Kompatibilitätsliste fügt nur dann eine Website hinzu, wenn die folgenden Aktionen auftreten.  

*   Zeigt einem IE-Benutzer eine Meldung an, in der der Benutzer einen anderen Browser aus Kompatibilitätsgründen verwenden soll.  
*   Besitzer fordert an, die Website der IE-Kompatibilitätsliste hinzuzufügen.  

## <a name="redirection-experience"></a>Umleitungserfahrung

Bei der Umleitung Microsoft Edge wird dem Benutzer das Einmaldialogfeld im nächsten Screenshot angezeigt.  Das Dialogfeld stellt dem Benutzer die folgenden Informationen zur Verfügung.  

*   Es wird erläutert, warum die Website umgeleitet wird.  
*   Der Benutzer wird aufgefordert, die Zustimmung zum Kopieren von Browserdaten und -einstellungen aus IE in Microsoft Edge.  

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
      *   Die Homepage  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Browserbenachrichtigung und Eingabeaufforderung zum Importieren von Daten und Einstellungen" lightbox="../media/neededge-dialog1.msft.png":::
         Browserbenachrichtigung und Eingabeaufforderung zum Importieren von Daten und Einstellungen  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Wenn der Benutzer nicht zuwilligt, indem er das Kontrollkästchen Meine Browserdaten und ****-einstellungen immer über **Internet Explorer** übertragen aus aktivieren, kann der Benutzer Weiter browsen auswählen, um die   Browsersitzung fortzufahren.  

Schließlich wird unter der Adressleiste für jede Umleitung ein Inkompatibilitätsbanner der Website angezeigt.  Ein Beispiel für ein Website-Inkompatibilitätsbanner wird in der folgenden Abbildung angezeigt.

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Benachrichtigung über moderne Websites und Aufforderung zum Festlegen Microsoft Edge als Standardbrowser oder Erkunden Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   Benachrichtigung über moderne Websites und Aufforderung zum Festlegen Microsoft Edge als Standardbrowser oder Erkunden Microsoft Edge  
:::image-end:::

Das Inkompatibilitätsbanner der Website enthält die folgenden Details für den Benutzer.  

*   Empfiehlt dem Benutzer, zu Microsoft Edge.  
*   Bietet an, Microsoft Edge als Standardbrowser festlegen.  
*   Gibt dem Benutzer die Möglichkeit, die Microsoft Edge.    
    
Wenn eine Website von Internet Explorer zu Microsoft Edge umgeleitet wird, tritt eine der folgenden Aktionen auf.

*   Wenn die aktive IE-Registerkarte keinen vorherigen Inhalt hatte, wird sie geschlossen.  
*   Wenn die aktive IE-Registerkarte zuvor Inhalte hatte, navigiert sie zur Microsoft-Supportseite, auf der erläutert wird, warum die Website zu [Microsoft Edge umgeleitet wurde.][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]  

> [!NOTE]
> Nach einer Umleitung können Benutzer IE für Websites verwenden, die nicht in der IE-Kompatibilitätsliste enthalten sind.  

## <a name="request-an-update-to-the-ie-compatibility-list"></a>Anfordern eines Updates für die IE-Kompatibilitätsliste  

Die IE-Kompatibilitätsliste ist eine XML-Datei auf [microsoft.com.][MicrosoftOfficialHome]  Die Liste wird regelmäßig als Reaktion auf Benutzer- und Websiteentwickleranforderungen aktualisiert, um Websites hinzufügen oder entfernen zu lassen.  Aktualisierungen der Liste werden automatisch auf Benutzerautomaten heruntergeladen.  

Senden Sie die folgenden Informationen [ietoedge@microsoft.com,][MailtoMicrosoftIetoedge] damit Ihre Website hinzugefügt oder aus der IE-Kompatibilitätsliste entfernt wird.    

*   Besitzername  
*   Unternehmenstitel  
*   E-Mail-Adresse  
*   Name des Unternehmens  
*   Straße  
*   Websiteadresse  
    
Die IE-Kompatibilitätsliste wird innerhalb einer Woche aktualisiert.

> [!NOTE]
> Die IE-Kompatibilitätsliste ist nur für die Arbeit mit öffentlichen Websites konzipiert.  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Senden einer E-Mail an ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Microsoft Official Home"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Benötigen Microsoft Edge v1-Xml-| Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "Die Website, die Sie erreichen wollten, funktioniert nicht mit Internet Explorer | Microsoft Office Support"  
