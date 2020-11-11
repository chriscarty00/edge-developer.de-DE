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
# <span data-ttu-id="616ee-104">Verschieben von Benutzern aus dem Internet Explorer nach Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="616ee-104">Moving users to Microsoft Edge from Internet Explorer</span></span> 

<span data-ttu-id="616ee-105">Viele moderne Websites verfügen über Designs, die mit Internet Explorer \ (IE \) nicht kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="616ee-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="616ee-106">Wenn ein IE-Benutzer eine inkompatible öffentliche Website besucht, erhält der Benutzer möglicherweise eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="616ee-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="616ee-107">In der Meldung wird angegeben, dass die Website mit dem Browser nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="616ee-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="616ee-108">Nachdem die Nachricht angezeigt wurde, wird erwartet, dass der Benutzer manuell zu einem modernen Browser wechselt.</span><span class="sxs-lookup"><span data-stu-id="616ee-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="616ee-109">Um Unterbrechungen zu minimieren, beginnend mit Version 84, unterstützt Microsoft Edge eine neue Funktion, die Benutzer automatisch umleitet.</span><span class="sxs-lookup"><span data-stu-id="616ee-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="616ee-110">Wenn ein IE-Benutzer zu einer Website navigiert, die mit IE nicht kompatibel ist, leitet Windows den Benutzer automatisch an Microsoft Edge um.</span><span class="sxs-lookup"><span data-stu-id="616ee-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="616ee-111">Wenn Sie die Websites in der Liste überprüfen möchten, navigieren Sie zu [benötigen Sie Microsoft Edge-Liste][MicrosoftEdgeNeededgeV1].</span><span class="sxs-lookup"><span data-stu-id="616ee-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="616ee-112">In diesem Artikel werden die folgenden Konzepte beschrieben:</span><span class="sxs-lookup"><span data-stu-id="616ee-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="616ee-113">Die Benutzeroberfläche für die Umleitung</span><span class="sxs-lookup"><span data-stu-id="616ee-113">The user experience for redirection</span></span>  
*   <span data-ttu-id="616ee-114">Anfordern eines Updates für die Liste</span><span class="sxs-lookup"><span data-stu-id="616ee-114">How to request an update to the list</span></span>  
    
## <span data-ttu-id="616ee-115">Warum wird eine Website zur IE-Kompatibilitätsliste hinzugefügt?</span><span class="sxs-lookup"><span data-stu-id="616ee-115">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="616ee-116">Die IE-Kompatibilitätsliste fügt nur dann eine Website hinzu, wenn die folgenden Aktionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="616ee-116">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="616ee-117">Zeigt einem IE-Benutzer eine Nachricht, die darauf hinweist, dass der Benutzer aus Kompatibilitätsgründen einen anderen Browser verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="616ee-117">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="616ee-118">Besitzer Anforderungen zum Hinzufügen der Website zur IE-Kompatibilitätsliste.</span><span class="sxs-lookup"><span data-stu-id="616ee-118">Owner requests to add the website to the IE compatibility list.</span></span>  
    
## <span data-ttu-id="616ee-119">Aktualisieren der IE-Kompatibilitätsliste</span><span class="sxs-lookup"><span data-stu-id="616ee-119">Update the IE compatibility list</span></span>  

<span data-ttu-id="616ee-120">Die IE-Kompatibilitätsliste ist eine XML-Datei auf [Microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="616ee-120">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="616ee-121">Die Liste wird regelmäßig als Antwort auf Benutzer-und Websiteentwickler Anforderungen aktualisiert, damit Websites hinzugefügt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="616ee-121">The list is regularly updated in response to user and website developer requests to have websites added or removed.</span></span>  <span data-ttu-id="616ee-122">Aktualisierungen der Liste werden automatisch auf Benutzer Computer heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="616ee-122">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="616ee-123">Senden Sie die folgenden Informationen an [ietoedge@Microsoft.com][MailtoMicrosoftIetoedge] , damit Ihre Website aus der IE-Kompatibilitätsliste hinzugefügt oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="616ee-123">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="616ee-124">Name des Besitzers</span><span class="sxs-lookup"><span data-stu-id="616ee-124">Owner name</span></span>  
*   <span data-ttu-id="616ee-125">Unternehmens Titel</span><span class="sxs-lookup"><span data-stu-id="616ee-125">Corporate title</span></span>  
*   <span data-ttu-id="616ee-126">E-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="616ee-126">Email address</span></span>  
*   <span data-ttu-id="616ee-127">Name des Unternehmens</span><span class="sxs-lookup"><span data-stu-id="616ee-127">Company name</span></span>  
*   <span data-ttu-id="616ee-128">Straße</span><span class="sxs-lookup"><span data-stu-id="616ee-128">Street address</span></span>  
*   <span data-ttu-id="616ee-129">Website Adresse</span><span class="sxs-lookup"><span data-stu-id="616ee-129">Website address</span></span>  
    
> [!NOTE]
> <span data-ttu-id="616ee-130">Die IE-Kompatibilitätsliste ist für die Zusammenarbeit mit öffentlichen Websites vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="616ee-130">The IE compatibility list is designed to work with public sites only.</span></span>  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Senden einer e-Mail an ietoedge@Microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Microsoft Official Home"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Benötigen Sie Microsoft Edge List v1 XML | Microsoft Edge"  
