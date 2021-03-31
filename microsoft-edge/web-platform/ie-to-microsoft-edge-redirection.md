---
description: Verschieben von Benutzern von Internet Explorer zu Microsoft Edge
title: Verschieben von Benutzern von Internet Explorer zu Microsoft Edge
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
# <a name="moving-users-to-microsoft-edge-from-internet-explorer"></a><span data-ttu-id="7aae5-104">Verschieben von Benutzern von Internet Explorer zu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7aae5-104">Moving users to Microsoft Edge from Internet Explorer</span></span>  

<span data-ttu-id="7aae5-105">Viele moderne Websites verfügen über Designs, die nicht mit Internet Explorer \(IE\) kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="7aae5-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="7aae5-106">Wenn ein IE-Benutzer eine inkompatible öffentliche Website besucht, wird dem Benutzer möglicherweise eine Nachricht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7aae5-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="7aae5-107">Die Meldung besagt, dass die Website nicht mit dem Browser kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="7aae5-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="7aae5-108">Nachdem die Nachricht angezeigt wurde, wird erwartet, dass der Benutzer manuell zu einem modernen Browser wechselt.</span><span class="sxs-lookup"><span data-stu-id="7aae5-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="7aae5-109">Um Unterbrechungen zu minimieren, unterstützt Microsoft Edge ab Version 84 eine neue Funktion, mit der Benutzer automatisch umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="7aae5-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="7aae5-110">Wenn ein IE-Benutzer zu einer Website navigiert, die mit IE nicht kompatibel ist, leitet Windows den Benutzer automatisch zu Microsoft Edge um.</span><span class="sxs-lookup"><span data-stu-id="7aae5-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="7aae5-111">Um die Websites in der Liste zu überprüfen, navigieren Sie zu [Microsoft Edge-Liste benötigen.][MicrosoftEdgeNeededgeV1]</span><span class="sxs-lookup"><span data-stu-id="7aae5-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="7aae5-112">In diesem Artikel werden die folgenden Konzepte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7aae5-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="7aae5-113">Warum eine Website zur Liste hinzugefügt wird</span><span class="sxs-lookup"><span data-stu-id="7aae5-113">Why a website is added to the list</span></span>  
*   <span data-ttu-id="7aae5-114">Die Benutzeroberfläche für die Umleitung</span><span class="sxs-lookup"><span data-stu-id="7aae5-114">The user experience for redirection</span></span>  
*   <span data-ttu-id="7aae5-115">Anfordern eines Updates für die Liste</span><span class="sxs-lookup"><span data-stu-id="7aae5-115">Request an update to the list</span></span>  
    
## <a name="why-is-a-website-added-to-the-ie-compatibility-list"></a><span data-ttu-id="7aae5-116">Warum wird der IE-Kompatibilitätsliste eine Website hinzugefügt?</span><span class="sxs-lookup"><span data-stu-id="7aae5-116">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="7aae5-117">Die IE-Kompatibilitätsliste fügt nur dann eine Website hinzu, wenn die folgenden Aktionen auftreten.</span><span class="sxs-lookup"><span data-stu-id="7aae5-117">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="7aae5-118">Zeigt einem IE-Benutzer eine Meldung an, in der der Benutzer einen anderen Browser aus Kompatibilitätsgründen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="7aae5-118">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="7aae5-119">Besitzer fordert an, die Website der IE-Kompatibilitätsliste hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7aae5-119">Owner requests to add the website to the IE compatibility list.</span></span>  

## <a name="redirection-experience"></a><span data-ttu-id="7aae5-120">Umleitungserfahrung</span><span class="sxs-lookup"><span data-stu-id="7aae5-120">Redirection experience</span></span>

<span data-ttu-id="7aae5-121">Bei der Umleitung zu Microsoft Edge wird dem Benutzer das einmalige Dialogfeld im nächsten Screenshot angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7aae5-121">On redirection to Microsoft Edge, the user is shown the one-time dialog in the next screenshot.</span></span>  <span data-ttu-id="7aae5-122">Das Dialogfeld stellt dem Benutzer die folgenden Informationen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7aae5-122">The dialog provides the user with the following information.</span></span>  

*   <span data-ttu-id="7aae5-123">Es wird erläutert, warum die Website umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="7aae5-123">It explains why the website is being redirected.</span></span>  
*   <span data-ttu-id="7aae5-124">Er fordert den Benutzer zur Zustimmung auf, Browserdaten und -einstellungen von IE in Microsoft Edge zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="7aae5-124">It prompts the user for consent to copy browsing data and preferences from IE to Microsoft Edge.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7aae5-125">Die folgenden Browserdaten werden importiert.</span><span class="sxs-lookup"><span data-stu-id="7aae5-125">The following browsing data is imported.</span></span>  
      
      *   <span data-ttu-id="7aae5-126">Favoriten</span><span class="sxs-lookup"><span data-stu-id="7aae5-126">Favorites</span></span>  
      *   <span data-ttu-id="7aae5-127">Kennwörter</span><span class="sxs-lookup"><span data-stu-id="7aae5-127">Passwords</span></span>  
      *   <span data-ttu-id="7aae5-128">Suchmaschinen</span><span class="sxs-lookup"><span data-stu-id="7aae5-128">Search engines</span></span>  
      *   <span data-ttu-id="7aae5-129">Offene Registerkarten</span><span class="sxs-lookup"><span data-stu-id="7aae5-129">Open tabs</span></span>  
      *   <span data-ttu-id="7aae5-130">Verlauf</span><span class="sxs-lookup"><span data-stu-id="7aae5-130">History</span></span>  
      *   <span data-ttu-id="7aae5-131">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="7aae5-131">Settings</span></span>  
      *   <span data-ttu-id="7aae5-132">Cookies</span><span class="sxs-lookup"><span data-stu-id="7aae5-132">Cookies</span></span>  
      *   <span data-ttu-id="7aae5-133">Die Homepage</span><span class="sxs-lookup"><span data-stu-id="7aae5-133">The Home Page</span></span>  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Browserbenachrichtigung und Eingabeaufforderung zum Importieren von Daten und Einstellungen" lightbox="../media/neededge-dialog1.msft.png":::
         <span data-ttu-id="7aae5-135">Browserbenachrichtigung und Eingabeaufforderung zum Importieren von Daten und Einstellungen</span><span class="sxs-lookup"><span data-stu-id="7aae5-135">Browsing notification and prompt to import data and preferences</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="7aae5-136">Wenn der Benutzer nicht zuwilligt, indem er das Kontrollkästchen Meine Browserdaten und -einstellungen immer über **Internet Explorer** übertragen aus aktivieren, kann der Benutzer Weiter browsen auswählen, um die   Browsersitzung fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="7aae5-136">If the user does not consent by choosing the **Always bring over my browsing data and preferences from Internet Explorer** checkbox, the user may choose **Continue browsing** to continue the browsing session.</span></span>  

<span data-ttu-id="7aae5-137">Schließlich wird unter der Adressleiste für jede Umleitung ein Inkompatibilitätsbanner der Website angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7aae5-137">Finally, a website incompatibility banner is displayed under the address bar for each redirection.</span></span>  <span data-ttu-id="7aae5-138">Ein Beispiel für ein Website-Inkompatibilitätsbanner wird in der folgenden Abbildung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7aae5-138">An example of a website incompatibility banner is displayed in following figure.</span></span>

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Benachrichtigung über moderne Websites und Aufforderung zum Festlegen von Microsoft Edge als Standardbrowser oder Erkunden von Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   <span data-ttu-id="7aae5-140">Benachrichtigung über moderne Websites und Aufforderung zum Festlegen von Microsoft Edge als Standardbrowser oder Erkunden von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7aae5-140">Notification about modern sites and prompt to set Microsoft Edge as default browser or explore Microsoft Edge</span></span>  
:::image-end:::

<span data-ttu-id="7aae5-141">Das Inkompatibilitätsbanner der Website enthält die folgenden Details für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7aae5-141">The website incompatibility banner provides the following details to the user.</span></span>  

*   <span data-ttu-id="7aae5-142">Empfiehlt dem Benutzer, zu Microsoft Edge zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="7aae5-142">Recommends that the user to switch to Microsoft Edge.</span></span>  
*   <span data-ttu-id="7aae5-143">Bietet an, Microsoft Edge als Standardbrowser zu setzen.</span><span class="sxs-lookup"><span data-stu-id="7aae5-143">Offers to set Microsoft Edge as the default browser.</span></span>  
*   <span data-ttu-id="7aae5-144">Gibt dem Benutzer die Möglichkeit, Microsoft Edge zu erkunden.</span><span class="sxs-lookup"><span data-stu-id="7aae5-144">Gives the user the option to explore Microsoft Edge.</span></span>    
    
<span data-ttu-id="7aae5-145">Wenn eine Website von Internet Explorer zu Microsoft Edge umgeleitet wird, tritt eine der folgenden Aktionen auf.</span><span class="sxs-lookup"><span data-stu-id="7aae5-145">When a website is redirected from Internet Explorer to Microsoft Edge, one of the following actions occurs.</span></span>

*   <span data-ttu-id="7aae5-146">Wenn die aktive IE-Registerkarte keinen vorherigen Inhalt hatte, wird sie geschlossen.</span><span class="sxs-lookup"><span data-stu-id="7aae5-146">If the active IE tab had no prior content, it is closed.</span></span>  
*   <span data-ttu-id="7aae5-147">Wenn die aktive IE-Registerkarte zuvor Inhalte hatte, navigiert sie zur Microsoft-Supportseite, auf der erläutert wird, warum die Website zu [Microsoft Edge umgeleitet wurde.][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]</span><span class="sxs-lookup"><span data-stu-id="7aae5-147">If the active IE tab had prior content, it navigates to the [Microsoft support page that explains why the website was redirected to Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].</span></span>  

> [!NOTE]
> <span data-ttu-id="7aae5-148">Nach einer Umleitung können Benutzer IE für Websites verwenden, die nicht in der IE-Kompatibilitätsliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7aae5-148">After a redirection, users may continue to use IE for websites that are not on the IE compatibility list.</span></span>  

## <a name="request-an-update-to-the-ie-compatibility-list"></a><span data-ttu-id="7aae5-149">Anfordern eines Updates für die IE-Kompatibilitätsliste</span><span class="sxs-lookup"><span data-stu-id="7aae5-149">Request an update to the IE compatibility list</span></span>  

<span data-ttu-id="7aae5-150">Die IE-Kompatibilitätsliste ist eine XML-Datei auf [microsoft.com.][MicrosoftOfficialHome]</span><span class="sxs-lookup"><span data-stu-id="7aae5-150">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="7aae5-151">Die Liste wird regelmäßig als Reaktion auf Benutzer- und Websiteentwickleranforderungen aktualisiert, um Websites hinzufügen oder entfernen zu lassen.</span><span class="sxs-lookup"><span data-stu-id="7aae5-151">The list is regularly updated in response to user and website developer requests to have websites added or removed.</span></span>  <span data-ttu-id="7aae5-152">Aktualisierungen der Liste werden automatisch auf Benutzerautomaten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="7aae5-152">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="7aae5-153">Senden Sie die folgenden Informationen [ietoedge@microsoft.com,][MailtoMicrosoftIetoedge] damit Ihre Website hinzugefügt oder aus der IE-Kompatibilitätsliste entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7aae5-153">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="7aae5-154">Besitzername</span><span class="sxs-lookup"><span data-stu-id="7aae5-154">Owner name</span></span>  
*   <span data-ttu-id="7aae5-155">Unternehmenstitel</span><span class="sxs-lookup"><span data-stu-id="7aae5-155">Corporate title</span></span>  
*   <span data-ttu-id="7aae5-156">E-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="7aae5-156">Email address</span></span>  
*   <span data-ttu-id="7aae5-157">Name des Unternehmens</span><span class="sxs-lookup"><span data-stu-id="7aae5-157">Company name</span></span>  
*   <span data-ttu-id="7aae5-158">Straße</span><span class="sxs-lookup"><span data-stu-id="7aae5-158">Street address</span></span>  
*   <span data-ttu-id="7aae5-159">Websiteadresse</span><span class="sxs-lookup"><span data-stu-id="7aae5-159">Website address</span></span>  
    
<span data-ttu-id="7aae5-160">Die IE-Kompatibilitätsliste wird innerhalb einer Woche aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7aae5-160">The IE compatibility list is updated within a week.</span></span>

> [!NOTE]
> <span data-ttu-id="7aae5-161">Die IE-Kompatibilitätsliste ist nur für die Arbeit mit öffentlichen Websites konzipiert.</span><span class="sxs-lookup"><span data-stu-id="7aae5-161">The IE compatibility list is designed to work with public sites only.</span></span>  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Senden einer E-Mail an ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Microsoft Official Home"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Microsoft Edge List v1 xml | Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "Die Website, die Sie erreichen wollten, funktioniert nicht mit Internet Explorer | Microsoft Office Support"  
