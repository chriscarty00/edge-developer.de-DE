---
description: Hosten und Veröffentlichen von Erweiterungen im Unternehmen für Microsoft Edge (Chromium).
title: Veröffentlichen und Aktualisieren von Erweiterungen im Microsoft Edge-Add-Ons-Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 91fdd5c2f625890653085e8999da3e513b072348
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327687"
---
# <span data-ttu-id="0d039-104">Veröffentlichen und Aktualisieren von Erweiterungen im Microsoft Edge-Add-Ons-Store</span><span class="sxs-lookup"><span data-stu-id="0d039-104">Publish and update extensions in the Microsoft Edge Add-ons store</span></span>  

<span data-ttu-id="0d039-105">Die meisten Erweiterungen werden im [Microsoft Edge-Add-Ons-Store][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] veröffentlicht, um Benutzer vor bösartigen Erweiterungen zu schützen.</span><span class="sxs-lookup"><span data-stu-id="0d039-105">Most extensions are published to the [Microsoft Edge Add-ons store][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] to protect users from malicious extensions.</span></span>  

## <span data-ttu-id="0d039-106">Veröffentlichungsoptionen für Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="0d039-106">Publish options for extensions</span></span>  

<span data-ttu-id="0d039-107">Alle Erweiterungen werden als spezielle Archivdatei \( \) mit einem Suffix `.zip` an Die Benutzer `.crx` verteilt.</span><span class="sxs-lookup"><span data-stu-id="0d039-107">All extensions are distributed to users as a special archive \(`.zip`\) file with a `.crx` suffix.</span></span>  <span data-ttu-id="0d039-108">Im Microsoft Edge-Add-Ons-Speicher veröffentlichte Erweiterungen werden als Dateien `.zip` hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="0d039-108">Extensions published to the Microsoft Edge Add-ons store are uploaded as `.zip` files.</span></span>  <span data-ttu-id="0d039-109">Beim Veröffentlichungsprozess wird die Datei `.zip` automatisch in eine Datei `.crx` konvertiert.</span><span class="sxs-lookup"><span data-stu-id="0d039-109">The publishing process automatically converts the `.zip` file into a `.crx` file.</span></span>  

<span data-ttu-id="0d039-110">In den folgenden beiden Szenarien müssen Sie Ihre Erweiterung nicht im Microsoft Edge-Add-Ons-Store veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0d039-110">The following two scenarios don't require you to publish your extension in the Microsoft Edge Add-ons store.</span></span>  

*   <span data-ttu-id="0d039-111">Erweiterungen, die mithilfe der Unternehmensrichtlinie verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="0d039-111">Extensions distributed using Enterprise policy.</span></span>  
*   <span data-ttu-id="0d039-112">Verwenden von entpackten Erweiterungsverzeichnissen auf einem lokalen Computer, wenn sich Microsoft Edge im Entwicklermodus befindet.</span><span class="sxs-lookup"><span data-stu-id="0d039-112">Using unpacked extension directories on a local machine when Microsoft Edge is in developer mode.</span></span>  

## <span data-ttu-id="0d039-113">Updates für Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="0d039-113">Updates to extensions</span></span>

<span data-ttu-id="0d039-114">Der Microsoft Edge Browser sucht regelmäßig nach neuen Versionen installierter Erweiterungen und aktualisiert diese ohne Benutzereingriff.</span><span class="sxs-lookup"><span data-stu-id="0d039-114">The Microsoft Edge browser periodically checks for new versions of installed extensions and updates each without user intervention.</span></span>  

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Erweiterungen – Microsoft Edge Insider Addons | Microsoft"  

> [!NOTE]
> <span data-ttu-id="0d039-116">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d039-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0d039-117">Die ursprüngliche Seite finden Sie [hier.](https://developer.chrome.com/extensions/hosting)</span><span class="sxs-lookup"><span data-stu-id="0d039-117">The original page is found [here](https://developer.chrome.com/extensions/hosting).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="0d039-119">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0d039-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
