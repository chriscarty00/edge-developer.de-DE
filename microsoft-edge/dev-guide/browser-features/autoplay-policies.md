---
description: Sicherstellen, dass sich der Medieninhalt auf Ihrer Website wie vorgesehen verhält
title: Dev Guide – Richtlinien für die automatische Wiedergabe
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 9/17/2018
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Medien, Video, Audio, automatische Wiedergabe
ms.custom: seodec18
ms.openlocfilehash: 397c6f0a22359dbfab7c44370b0429147b7c9834
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566768"
---
# <span data-ttu-id="1565c-104">Richtlinien für die automatische Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="1565c-104">Autoplay Policies</span></span>

<span data-ttu-id="1565c-105">Microsoft Edge bietet Kunden die Möglichkeit, Ihre Browsereinstellungen auf Websites zu personalisieren, die Medien mit Sound wiedergeben, um Ablenkungen im Internet zu minimieren und die Bandbreite zu sparen.</span><span class="sxs-lookup"><span data-stu-id="1565c-105">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span> <span data-ttu-id="1565c-106">Darüber hinaus unterdrückt Microsoft Edge automatisch die automatische Wiedergabe von Medien in Hintergrundregisterkarten.</span><span class="sxs-lookup"><span data-stu-id="1565c-106">Additionaly, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>

<span data-ttu-id="1565c-107">Benutzer können das Medienverhalten mit den Steuerelementen für die automatische Wiedergabe auf [globaler](#global-media-autoplay-settings) und [pro Website](#per-site-media-autoplay-settings) anpassen, die die folgenden Optionen bieten:</span><span class="sxs-lookup"><span data-stu-id="1565c-107">Users can customize media behavior with both [global](#global-media-autoplay-settings) and [per-site](#per-site-media-autoplay-settings) autoplay controls, which provide the following options:</span></span>

- <span data-ttu-id="1565c-108">" **Zulassen** " ist die Standardeinstellung, und die Wiedergabe von Videos wird fortgesetzt, wenn eine Registerkarte zuerst im Vordergrund angezeigt wird, nach Ermessen der Website.</span><span class="sxs-lookup"><span data-stu-id="1565c-108">**Allow**  is the default and will continue to play videos when a tab is first viewed in the foreground, at the site’s discretion.</span></span>

- <span data-ttu-id="1565c-109">**Limit** schränkt die automatische Wiedergabe nur dann ein, wenn Videos stumm geschaltet sind, sodass die Benutzer nie von Sound überrascht werden.</span><span class="sxs-lookup"><span data-stu-id="1565c-109">**Limit** will restrict autoplay to only work when videos are muted, so users are never surprised by sound.</span></span> <span data-ttu-id="1565c-110">Nachdem der Benutzer auf eine beliebige Stelle auf der Seite geklickt hat, ist die automatische Wiedergabe wieder aktiviert und wird weiterhin innerhalb dieser Domäne auf dieser Registerkarte zugelassen.</span><span class="sxs-lookup"><span data-stu-id="1565c-110">Once the user clicks anywhere on the page, autoplay is re-enabled, and will continue to be allowed within that domain in that tab.</span></span>

- <span data-ttu-id="1565c-111">**Blockieren** verhindert die automatische Wiedergabe auf allen Websites, bis Benutzer direkt mit dem Medieninhalt interagieren.</span><span class="sxs-lookup"><span data-stu-id="1565c-111">**Block** will prevent autoplay on all sites until users directly interact with the media content.</span></span>

## <span data-ttu-id="1565c-112">Einstellungen für die automatische Wiedergabe globaler Medien</span><span class="sxs-lookup"><span data-stu-id="1565c-112">Global media autoplay settings</span></span>

<span data-ttu-id="1565c-113">Benutzer können das Standardverhalten für die automatische Wiedergabe für alle Websites unter **Erweiterte Einstellung**  >  **Medien Automatik**steuern.</span><span class="sxs-lookup"><span data-stu-id="1565c-113">Users can control the default autoplay behavior for all sites under **Advanced Setting** > **Media autoplay**.</span></span>

![Einstellungen für die automatische Wiedergabe globaler Medien](../media/autoplay_global.png)

## <span data-ttu-id="1565c-115">Einstellungen für die automatische Wiedergabe von Medien pro Website</span><span class="sxs-lookup"><span data-stu-id="1565c-115">Per-site media autoplay settings</span></span>

<span data-ttu-id="1565c-116">Benutzer können das Verhalten der automatischen Wiedergabe pro Website unter dem Abschnitt " **Websiteberechtigungen** " im Bereich "Website Informationen" steuern.</span><span class="sxs-lookup"><span data-stu-id="1565c-116">Users can control autoplay behavior on a per-site basis under the **Website permissions** section of the website information pane.</span></span> <span data-ttu-id="1565c-117">Diese Einstellung finden Sie, indem Sie auf das Symbol "Informationen" oder das Symbol "Sperren" auf der linken Seite der Adressleiste klicken und dann auf "Einstellungen für die Wiedergabe von Medien" klicken, um zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="1565c-117">This setting can be found by clicking the information icon or lock icon on the left side of the address bar and clicking on “Media autoplay settings” to get started.</span></span>

<span data-ttu-id="1565c-118">Einstellungen pro Website überschreiben die globale Einstellung.</span><span class="sxs-lookup"><span data-stu-id="1565c-118">Per-site settings override the global setting.</span></span> <span data-ttu-id="1565c-119">Wenn ein Benutzer beispielsweise seine globale Einstellung auf "zulassen" festgelegt hat, aber eine Einstellung pro Website auf "blockieren" ändert, wird die automatische Wiedergabe für diese Website blockiert.</span><span class="sxs-lookup"><span data-stu-id="1565c-119">For example, if a user has their global setting set to “Allow” but changes a per-site setting to “Block”, autoplay will be blocked for that site.</span></span>

![Einstellungen für die automatische Wiedergabe von Medien pro Website](../media/autoplay_per-site.png)
 
## <span data-ttu-id="1565c-121">Bewährte Methoden für Web-Entwickler</span><span class="sxs-lookup"><span data-stu-id="1565c-121">Best Practices for Web Developers</span></span>

<span data-ttu-id="1565c-122">Hier erfahren Sie, wie Sie eine gute Benutzerfreundlichkeit mit auf Ihrer Website gehosteten Medien gewährleisten:</span><span class="sxs-lookup"><span data-stu-id="1565c-122">Here's how to ensure a good user experience with media hosted on your site:</span></span>

- <span data-ttu-id="1565c-123">Davon ausgehen, dass für jede Verwendung eines Medienelements Wil eine Benutzergeste erforderlich ist, um die Wiedergabe zu starten (da Benutzer die automatische Wiedergabe zu einem beliebigen Zeitpunkt blockieren können) und entsprechend planen.</span><span class="sxs-lookup"><span data-stu-id="1565c-123">Assume  each use of a media element wil require a user gesture to start the playback (as users can block autoplay at any point in time) and plan accordingly.</span></span>  <span data-ttu-id="1565c-124">Global-und pro-Site-AutoPlay-Richtlinien gelten für alle `<audio>` und `<video>` Elemente, unabhängig davon, wie Sie auf Ihrer Website verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1565c-124">Global and per-site autoplay policies apply to all `<audio>` and `<video>` elements, regardless of how they are used on your site</span></span>

- <span data-ttu-id="1565c-125">Stellen Sie sicher, dass mediensteuerelemente immer auf dem Website Medium und dem Anzeigeninhalt vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="1565c-125">Ensure that media controls are always present on both site media and ad content.</span></span> <span data-ttu-id="1565c-126">Dadurch können Benutzer die Wiedergabe neu starten, wenn die automatische Wiedergabe auf der Seite blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="1565c-126">This will give users the ability to restart playback if autoplay is blocked on the page.</span></span>

- <span data-ttu-id="1565c-127">Bewerten Sie, wie die automatische Wiedergabe die Benutzerfreundlichkeit auf Ihrer Website beeinträchtigen kann, und verwenden Sie die automatische Wiedergabe auf eine Weise, die unerwünschte Medienwiedergabe minimiert.</span><span class="sxs-lookup"><span data-stu-id="1565c-127">Evaluate how autoplay may affect users’ experience on your website and consider using autoplay in a way that minimizes unwanted media playback.</span></span> <span data-ttu-id="1565c-128">Wenn die automatische Wiedergabe ein entscheidender Bestandteil ihrer Erfahrung ist, sollten Sie die Verwendung von stummgeschaltetem Inhalt verwenden, damit der Benutzer die Stummschaltung aufheben kann.</span><span class="sxs-lookup"><span data-stu-id="1565c-128">If autoplay is a crucial part of your experience, consider using muted content to start and allowing the user to unmute it.</span></span> <span data-ttu-id="1565c-129">Für stummgeschaltete Inhalte muss die Audioquelle entweder explizit stumm geschaltet oder nicht eingestellt sein.</span><span class="sxs-lookup"><span data-stu-id="1565c-129">For muted content to autoplay, the audio source must be either explicitly muted or not be set.</span></span> <span data-ttu-id="1565c-130">Andernfalls wird das Element nicht als stumm geschaltet angesehen.</span><span class="sxs-lookup"><span data-stu-id="1565c-130">Otherwise the element will not be considered as muted.</span></span>

- <span data-ttu-id="1565c-131">Verwenden Sie die systemeigenen Browsersteuerelemente für die Medienwiedergabe, sofern dies nicht unbedingt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1565c-131">Unless absolutely necessary to do otherwise, use the native browser controls for media playback.</span></span> <span data-ttu-id="1565c-132">Dadurch wird eine konsistente Benutzeroberfläche gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="1565c-132">This will ensure a consistent experience for users.</span></span> <span data-ttu-id="1565c-133">Wenn Sie stattdessen benutzerdefinierte Steuerelemente erstellen, stellen Sie sicher, dass die mediensteuerelemente immer vorhanden sind und dass Ihre Steuerelemente auf die Unterdrückung der automatischen Wiedergabe reagieren.</span><span class="sxs-lookup"><span data-stu-id="1565c-133">If you are building custom controls instead, ensure that media controls are always present and that your controls properly react to autoplay suppression.</span></span>

### <span data-ttu-id="1565c-134">Iframe-Delegierung</span><span class="sxs-lookup"><span data-stu-id="1565c-134">Iframe delegation</span></span>

<span data-ttu-id="1565c-135">Die automatische Wiedergabe in einer `<iframe>` erbt die Berechtigung "AutoPlay" von der übergeordneten Seite unabhängig vom Inhalts Ursprung.</span><span class="sxs-lookup"><span data-stu-id="1565c-135">Autoplay in an `<iframe>` will inherit the autoplay permission from the parent page regardless of content origin.</span></span> <span data-ttu-id="1565c-136">In einem Wiedergabelisten Szenario, in dem jede Mediendatei von einem separaten IFrame gehostet wird, muss der Benutzer die Wiedergabe nur einmal für die gesamte Wiedergabeliste initiieren.</span><span class="sxs-lookup"><span data-stu-id="1565c-136">In a playlist scenario where each media file is hosted by a separate iframe, the user would only need to initiate playback once for the entire playlist.</span></span>

### <span data-ttu-id="1565c-137">Erkennen, wenn die automatische Wiedergabe zulässig ist</span><span class="sxs-lookup"><span data-stu-id="1565c-137">Detecting when autoplay is allowed</span></span>

<span data-ttu-id="1565c-138">Sie können die Wiedergabesteuerelemente so anpassen, dass der richtige Zustand angezeigt wird, wenn die automatische Wiedergabe blockiert wird, indem Sie die von der `play()` Funktion für das Medienelement zurückgegebene Versprechung untersuchen:</span><span class="sxs-lookup"><span data-stu-id="1565c-138">You can adjust your playback controls to display the correct state when autoplay is blocked by examining the promise returned by the `play()` function on the media element:</span></span>

```Javascript

var promise = document.querySelector('video').play();

if (promise !== undefined) { 
    promise.catch(_error => { 
        // Autoplay was blocked
        // Show user media controls to manually start playback
    }).then(() => { 
        // Autoplay started
    }); 
}

```
