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
# <span data-ttu-id="d64d0-104">Verschieben von Benutzern aus dem Internet Explorer nach Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d64d0-104">Moving users to Microsoft Edge from Internet Explorer</span></span>  

<span data-ttu-id="d64d0-105">Viele moderne Websites verfügen über Designs, die mit Internet Explorer \ (IE \) nicht kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="d64d0-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="d64d0-106">Wenn ein IE-Benutzer eine inkompatible öffentliche Website besucht, erhält der Benutzer möglicherweise eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d64d0-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="d64d0-107">In der Meldung wird angegeben, dass die Website mit dem Browser nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="d64d0-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="d64d0-108">Nachdem die Nachricht angezeigt wurde, wird erwartet, dass der Benutzer manuell zu einem modernen Browser wechselt.</span><span class="sxs-lookup"><span data-stu-id="d64d0-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="d64d0-109">Um Unterbrechungen zu minimieren, beginnend mit Version 84, unterstützt Microsoft Edge eine neue Funktion, die Benutzer automatisch umleitet.</span><span class="sxs-lookup"><span data-stu-id="d64d0-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="d64d0-110">Wenn ein IE-Benutzer zu einer Website navigiert, die mit IE nicht kompatibel ist, leitet Windows den Benutzer automatisch an Microsoft Edge um.</span><span class="sxs-lookup"><span data-stu-id="d64d0-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="d64d0-111">Wenn Sie die Websites in der Liste überprüfen möchten, navigieren Sie zu [benötigen Sie Microsoft Edge-Liste][MicrosoftEdgeNeededgeV1].</span><span class="sxs-lookup"><span data-stu-id="d64d0-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="d64d0-112">In diesem Artikel werden die folgenden Konzepte beschrieben:</span><span class="sxs-lookup"><span data-stu-id="d64d0-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="d64d0-113">Gründe für das Hinzufügen einer Website zur Liste</span><span class="sxs-lookup"><span data-stu-id="d64d0-113">Why a website is added to the list</span></span>  
*   <span data-ttu-id="d64d0-114">Die Benutzeroberfläche für die Umleitung</span><span class="sxs-lookup"><span data-stu-id="d64d0-114">The user experience for redirection</span></span>  
*   <span data-ttu-id="d64d0-115">Anfordern eines Updates für die Liste</span><span class="sxs-lookup"><span data-stu-id="d64d0-115">Request an update to the list</span></span>  
    
## <span data-ttu-id="d64d0-116">Warum wird eine Website zur IE-Kompatibilitätsliste hinzugefügt?</span><span class="sxs-lookup"><span data-stu-id="d64d0-116">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="d64d0-117">Die IE-Kompatibilitätsliste fügt nur dann eine Website hinzu, wenn die folgenden Aktionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d64d0-117">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="d64d0-118">Zeigt einem IE-Benutzer eine Nachricht, die darauf hinweist, dass der Benutzer aus Kompatibilitätsgründen einen anderen Browser verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="d64d0-118">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="d64d0-119">Besitzer Anforderungen zum Hinzufügen der Website zur IE-Kompatibilitätsliste.</span><span class="sxs-lookup"><span data-stu-id="d64d0-119">Owner requests to add the website to the IE compatibility list.</span></span>  

## <span data-ttu-id="d64d0-120">Umleitungserfahrung</span><span class="sxs-lookup"><span data-stu-id="d64d0-120">Redirection experience</span></span>

<span data-ttu-id="d64d0-121">Bei der Umleitung zu Microsoft Edge wird dem Benutzer das einmalige Dialogfeld im nächsten Screenshot angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d64d0-121">On redirection to Microsoft Edge, the user is shown the one-time dialog in the next screenshot.</span></span>  <span data-ttu-id="d64d0-122">Das Dialogfeld bietet dem Benutzer die folgenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="d64d0-122">The dialog provides the user with the following information.</span></span>  

*   <span data-ttu-id="d64d0-123">Es wird erläutert, warum die Website umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="d64d0-123">It explains why the website is being redirected.</span></span>  
*   <span data-ttu-id="d64d0-124">Sie fordert den Benutzer zur Genehmigung auf, Daten und Einstellungen für das Browsen von IE zu Microsoft Edge zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="d64d0-124">It prompts the user for consent to copy browsing data and preferences from IE to Microsoft Edge.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d64d0-125">Die folgenden Browserdaten werden importiert.</span><span class="sxs-lookup"><span data-stu-id="d64d0-125">The following browsing data is imported.</span></span>  
      
      *   <span data-ttu-id="d64d0-126">Favoriten</span><span class="sxs-lookup"><span data-stu-id="d64d0-126">Favorites</span></span>  
      *   <span data-ttu-id="d64d0-127">Kennwörter</span><span class="sxs-lookup"><span data-stu-id="d64d0-127">Passwords</span></span>  
      *   <span data-ttu-id="d64d0-128">Suchmaschinen</span><span class="sxs-lookup"><span data-stu-id="d64d0-128">Search engines</span></span>  
      *   <span data-ttu-id="d64d0-129">Offene Registerkarten</span><span class="sxs-lookup"><span data-stu-id="d64d0-129">Open tabs</span></span>  
      *   <span data-ttu-id="d64d0-130">Verlauf</span><span class="sxs-lookup"><span data-stu-id="d64d0-130">History</span></span>  
      *   <span data-ttu-id="d64d0-131">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d64d0-131">Settings</span></span>  
      *   <span data-ttu-id="d64d0-132">Cookies</span><span class="sxs-lookup"><span data-stu-id="d64d0-132">Cookies</span></span>  
      *   <span data-ttu-id="d64d0-133">Die Startseite</span><span class="sxs-lookup"><span data-stu-id="d64d0-133">The Home Page</span></span>  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Durchsuchen der Benachrichtigung und Aufforderung zum Importieren von Daten und Einstellungen" lightbox="../media/neededge-dialog1.msft.png":::
         <span data-ttu-id="d64d0-135">Durchsuchen der Benachrichtigung und Aufforderung zum Importieren von Daten und Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d64d0-135">Browsing notification and prompt to import data and preferences</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="d64d0-136">Wenn der Benutzer nicht einverstanden ist, indem er das Kontrollkästchen **immer über meine Browserdaten und-Einstellungen aus Internet Explorer über** tragen auswählt, kann der Benutzer " **Continue Browsing**" auswählen,   um die Browsersitzung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="d64d0-136">If the user does not consent by choosing the **Always bring over my browsing data and preferences from Internet Explorer** checkbox, the user may choose **Continue browsing** to continue the browsing session.</span></span>  

<span data-ttu-id="d64d0-137">Schließlich wird für jede Umleitung unter der Adressleiste eine Website-Inkompatibilitäts-Banner angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d64d0-137">Finally, a website incompatibility banner is displayed under the address bar for each redirection.</span></span>  <span data-ttu-id="d64d0-138">Ein Beispiel für ein Website-Inkompatibilitäts-Banner wird in der folgenden Abbildung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d64d0-138">An example of a website incompatibility banner is displayed in following figure.</span></span>

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Benachrichtigung über moderne Websites und Aufforderung zum Festlegen von Microsoft Edge als Standardbrowser oder erkunden von Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   <span data-ttu-id="d64d0-140">Benachrichtigung über moderne Websites und Aufforderung zum Festlegen von Microsoft Edge als Standardbrowser oder erkunden von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d64d0-140">Notification about modern sites and prompt to set Microsoft Edge as default browser or explore Microsoft Edge</span></span>  
:::image-end:::

<span data-ttu-id="d64d0-141">Das Banner "Website-Inkompatibilität" bietet dem Benutzer die folgenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="d64d0-141">The website incompatibility banner provides the following details to the user.</span></span>  

*   <span data-ttu-id="d64d0-142">Empfiehlt dem Benutzer, zu Microsoft Edge zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="d64d0-142">Recommends that the user to switch to Microsoft Edge.</span></span>  
*   <span data-ttu-id="d64d0-143">Bietet an, Microsoft Edge als Standardbrowser einzurichten.</span><span class="sxs-lookup"><span data-stu-id="d64d0-143">Offers to set Microsoft Edge as the default browser.</span></span>  
*   <span data-ttu-id="d64d0-144">Bietet dem Benutzer die Möglichkeit, Microsoft Edge zu erkunden.</span><span class="sxs-lookup"><span data-stu-id="d64d0-144">Gives the user the option to explore Microsoft Edge.</span></span>    
    
<span data-ttu-id="d64d0-145">Wenn eine Website von Internet Explorer zu Microsoft Edge umgeleitet wird, erfolgt eine der folgenden Aktionen.</span><span class="sxs-lookup"><span data-stu-id="d64d0-145">When a website is redirected from Internet Explorer to Microsoft Edge, one of the following actions occurs.</span></span>

*   <span data-ttu-id="d64d0-146">Wenn die aktive IE-Registerkarte keinen vorherigen Inhalt aufweist, wird Sie geschlossen.</span><span class="sxs-lookup"><span data-stu-id="d64d0-146">If the active IE tab had no prior content, it is closed.</span></span>  
*   <span data-ttu-id="d64d0-147">Wenn die aktive IE-Registerkarte vorherigen Inhalt aufweist, navigiert Sie zur [Microsoft-Support Seite, in der erläutert wird, warum die Website an Microsoft Edge umgeleitet wurde][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].</span><span class="sxs-lookup"><span data-stu-id="d64d0-147">If the active IE tab had prior content, it navigates to the [Microsoft support page that explains why the website was redirected to Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].</span></span>  

> [!NOTE]
> <span data-ttu-id="d64d0-148">Nach einer Umleitung können Benutzer IE weiterhin für Websites verwenden, die nicht in der IE-Kompatibilitätsliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d64d0-148">After a redirection, users may continue to use IE for websites that are not on the IE compatibility list.</span></span>  

## <span data-ttu-id="d64d0-149">Anfordern eines Updates für die IE-Kompatibilitätsliste</span><span class="sxs-lookup"><span data-stu-id="d64d0-149">Request an update to the IE compatibility list</span></span>  

<span data-ttu-id="d64d0-150">Die IE-Kompatibilitätsliste ist eine XML-Datei auf [Microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="d64d0-150">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="d64d0-151">Die Liste wird regelmäßig als Antwort auf Benutzer-und Websiteentwickler Anforderungen aktualisiert, damit Websites hinzugefügt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d64d0-151">The list is regularly updated in response to user and website developer requests to have websites added or removed.</span></span>  <span data-ttu-id="d64d0-152">Aktualisierungen der Liste werden automatisch auf Benutzer Computer heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="d64d0-152">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="d64d0-153">Senden Sie die folgenden Informationen an [ietoedge@Microsoft.com][MailtoMicrosoftIetoedge] , damit Ihre Website aus der IE-Kompatibilitätsliste hinzugefügt oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d64d0-153">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="d64d0-154">Name des Besitzers</span><span class="sxs-lookup"><span data-stu-id="d64d0-154">Owner name</span></span>  
*   <span data-ttu-id="d64d0-155">Unternehmens Titel</span><span class="sxs-lookup"><span data-stu-id="d64d0-155">Corporate title</span></span>  
*   <span data-ttu-id="d64d0-156">E-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="d64d0-156">Email address</span></span>  
*   <span data-ttu-id="d64d0-157">Name des Unternehmens</span><span class="sxs-lookup"><span data-stu-id="d64d0-157">Company name</span></span>  
*   <span data-ttu-id="d64d0-158">Straße</span><span class="sxs-lookup"><span data-stu-id="d64d0-158">Street address</span></span>  
*   <span data-ttu-id="d64d0-159">Website Adresse</span><span class="sxs-lookup"><span data-stu-id="d64d0-159">Website address</span></span>  
    
> [!NOTE]
> <span data-ttu-id="d64d0-160">Die IE-Kompatibilitätsliste ist für die Zusammenarbeit mit öffentlichen Websites vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="d64d0-160">The IE compatibility list is designed to work with public sites only.</span></span>  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Senden einer e-Mail an ietoedge@Microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Microsoft Official Home"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Benötigen Sie Microsoft Edge List v1 XML | Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "Die Website, die Sie erreichen wollten, funktioniert nicht mit Internet Explorer | Microsoft Office-Support"  
