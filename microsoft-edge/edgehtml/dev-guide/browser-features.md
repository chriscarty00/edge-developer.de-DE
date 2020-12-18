---
ms.assetid: 4d3fa934-4fa8-4c02-b9b5-88506c76baac
description: Leitfäden für Browser Features in Microsoft Edge
title: Browser – Entwicklerhandbuch
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2579fad881496e2197f9f696bb2c12c47c7f723e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234115"
---
# <span data-ttu-id="52d50-104">Browser-Features</span><span class="sxs-lookup"><span data-stu-id="52d50-104">Browser features</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

## <span data-ttu-id="52d50-105">AutoPlay-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="52d50-105">Autoplay policies</span></span>  

 <span data-ttu-id="52d50-106">Microsoft Edge bietet Kunden die Möglichkeit, Ihre Browsereinstellungen auf Websites zu personalisieren, die Medien mit Sound wiedergeben, um Ablenkungen im Internet zu minimieren und die Bandbreite zu sparen.</span><span class="sxs-lookup"><span data-stu-id="52d50-106">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span>  <span data-ttu-id="52d50-107">Benutzer können das Medienverhalten mit den Steuerelementen für die automatische Wiedergabe auf globaler und pro Website anpassen.</span><span class="sxs-lookup"><span data-stu-id="52d50-107">Users can customize media behavior with both global and per-site autoplay controls.</span></span>  <span data-ttu-id="52d50-108">Darüber hinaus unterdrückt Microsoft Edge automatisch die automatische Wiedergabe von Medien in Hintergrundregisterkarten.</span><span class="sxs-lookup"><span data-stu-id="52d50-108">Additionally, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>  

<span data-ttu-id="52d50-109">Schauen Sie sich die [Richtlinien](./browser-features/autoplay-policies.md) für die automatische Wiedergabe an, um Details und bewährte Methoden für eine gute Benutzerfreundlichkeit mit auf Ihrer Website gehosteten Medien zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="52d50-109">Check out [Autoplay policies](./browser-features/autoplay-policies.md) for details and best practices to ensure a good user experience with media hosted on your site.</span></span>  

## <span data-ttu-id="52d50-110">Flash</span><span class="sxs-lookup"><span data-stu-id="52d50-110">Flash</span></span>  

<span data-ttu-id="52d50-111">Wenn Flash auf Ihrer Seite verwendet wird, der Benutzer ihn aber nicht aktiviert hat, zeigt Microsoft Edge in der Adressleiste normalerweise ein Puzzleteil Symbol an.</span><span class="sxs-lookup"><span data-stu-id="52d50-111">If Flash is used on your page but the user has not enabled it, Microsoft Edge will normally show a puzzle piece icon in the address bar.</span></span>  <span data-ttu-id="52d50-112">Wenn Sie das Flash-Steuerelement nach dem Laden der Seite dynamisch hinzufügen, wird das Symbol "Rätsel" möglicherweise nicht angezeigt, in diesem Fall sollten Sie [testen, ob Flash geladen wird, und eine anmutige Fallback-Erfahrung bereitstellen](./browser-features/flash.md) , wenn es nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="52d50-112">If you are dynamically adding the Flash control after the page is loaded, the puzzle icon may not display, in which case you'll want to [test if Flash is loaded and provide a graceful fallback experience](./browser-features/flash.md) if its not present.</span></span>  

## <span data-ttu-id="52d50-113">Leseansicht</span><span class="sxs-lookup"><span data-stu-id="52d50-113">Reading view</span></span>  

<span data-ttu-id="52d50-114">Microsoft Edge bietet eine [Leseansicht](./browser-features/reading-view.md) für eine optimierte, Buch ähnliche Leseerfahrung von Webseiten, ohne dass es sich um nicht verknüpfte oder andere sekundäre Inhalte auf der Seite handelt.</span><span class="sxs-lookup"><span data-stu-id="52d50-114">Microsoft Edge provides a [reading view](./browser-features/reading-view.md) for a more streamlined, book-like reading experience of webpages, without the distraction of unrelated or other secondary content on the page.</span></span>  <span data-ttu-id="52d50-115">Hier finden Sie Tipps, wie Sie eine hervorragende Leseansicht für Ihre Website und auch Anweisungen zum Deaktivieren der Leseansicht für Ihre Website sicherstellen können.</span><span class="sxs-lookup"><span data-stu-id="52d50-115">Here are tips on how to ensure a great reading view experience with your site and also instructions for opting your site out of reading view.</span></span>  

## <span data-ttu-id="52d50-116">Suchanbieterermittlung</span><span class="sxs-lookup"><span data-stu-id="52d50-116">Search provider discovery</span></span>  

<span data-ttu-id="52d50-117">Die Rich-Search-Integration ist in die Microsoft Edge-Adressleiste integriert, einschließlich Suchvorschlägen, Ergebnissen aus dem Internet, dem Browserverlauf und Favoriten.</span><span class="sxs-lookup"><span data-stu-id="52d50-117">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span>  <span data-ttu-id="52d50-118">[Hier finden Sie weitere Informationen für Suchanbieter](./browser-features/search-provider-discovery.md) , die Unterstützung für Microsoft Edge bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="52d50-118">[Here's more info for search providers](./browser-features/search-provider-discovery.md) looking to provide support for Microsoft Edge.</span></span>  
