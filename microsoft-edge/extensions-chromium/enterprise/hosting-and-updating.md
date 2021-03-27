---
description: Hosten und Veröffentlichen von Erweiterungen im Unternehmen für Microsoft Edge (Chromium).
title: Veröffentlichen und Aktualisieren von Erweiterungen im Microsoft Edge-Add-Ons-Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 2249462b0a2dac86efa4b775171e2a3229a34431
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461220"
---
# <a name="publish-and-update-extensions-in-the-microsoft-edge-add-ons-store"></a><span data-ttu-id="3af58-104">Veröffentlichen und Aktualisieren von Erweiterungen im Microsoft Edge-Add-Ons-Store</span><span class="sxs-lookup"><span data-stu-id="3af58-104">Publish and update extensions in the Microsoft Edge Add-ons store</span></span>  

<span data-ttu-id="3af58-105">Die meisten Erweiterungen werden im [Microsoft Edge-Add-Ons-Speicher][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] veröffentlicht, um Benutzer vor schädlichen Erweiterungen zu schützen.</span><span class="sxs-lookup"><span data-stu-id="3af58-105">Most extensions are published to the [Microsoft Edge Add-ons store][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] to protect users from malicious extensions.</span></span>  

## <a name="publish-options-for-extensions"></a><span data-ttu-id="3af58-106">Veröffentlichen von Optionen für Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="3af58-106">Publish options for extensions</span></span>  

<span data-ttu-id="3af58-107">Alle Erweiterungen werden als spezielle Archivdatei \( \) mit `.zip` einem Suffix an Benutzer `.crx` verteilt.</span><span class="sxs-lookup"><span data-stu-id="3af58-107">All extensions are distributed to users as a special archive \(`.zip`\) file with a `.crx` suffix.</span></span>  <span data-ttu-id="3af58-108">Im Microsoft Edge-Add-Ons-Speicher veröffentlichte Erweiterungen werden als Dateien `.zip` hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="3af58-108">Extensions published to the Microsoft Edge Add-ons store are uploaded as `.zip` files.</span></span>  <span data-ttu-id="3af58-109">Beim Veröffentlichungsprozess wird die Datei `.zip` automatisch in eine Datei `.crx` konvertiert.</span><span class="sxs-lookup"><span data-stu-id="3af58-109">The publishing process automatically converts the `.zip` file into a `.crx` file.</span></span>  

<span data-ttu-id="3af58-110">In den folgenden beiden Szenarien müssen Sie Ihre Erweiterung nicht im Microsoft Edge-Add-Ons-Speicher veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="3af58-110">The following two scenarios don't require you to publish your extension in the Microsoft Edge Add-ons store.</span></span>  

*   <span data-ttu-id="3af58-111">Erweiterungen, die mithilfe der Enterprise-Richtlinie verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="3af58-111">Extensions distributed using Enterprise policy.</span></span>  
*   <span data-ttu-id="3af58-112">Verwenden von auspackten Erweiterungsverzeichnissen auf einem lokalen Computer, wenn sich Microsoft Edge im Entwicklermodus befindet.</span><span class="sxs-lookup"><span data-stu-id="3af58-112">Using unpacked extension directories on a local machine when Microsoft Edge is in developer mode.</span></span>  

## <a name="updates-to-extensions"></a><span data-ttu-id="3af58-113">Updates für Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="3af58-113">Updates to extensions</span></span>

<span data-ttu-id="3af58-114">Der Microsoft Edge-Browser sucht automatisch nach neuen Versionen installierter Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="3af58-114">The Microsoft Edge browser automatically checks for new versions of installed Extensions.</span></span> <span data-ttu-id="3af58-115">Updates werden ohne Benutzereingriff installiert.</span><span class="sxs-lookup"><span data-stu-id="3af58-115">Updates are installed without user intervention.</span></span>  


<!-- image links -->

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Erweiterungen – Microsoft Edge Insider Addons | Microsoft"  

> [!NOTE]
> <span data-ttu-id="3af58-117">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3af58-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3af58-118">Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/hosting).</span><span class="sxs-lookup"><span data-stu-id="3af58-118">The original page is found [here](https://developer.chrome.com/extensions/hosting).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="3af58-120">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3af58-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
