---
description: Auf dieser Seite finden Sie eine Übersicht über die Neuerungen in EdgeHTML 13.
title: Neue Features und APIs in EdgeHTML 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2119e576a637d5f78e073f49a3cb1868a7ce1ca4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234232"
---
# <span data-ttu-id="e76ec-104">Neuerungen in EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="e76ec-104">What's new in EdgeHTML 13</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="e76ec-105">Hier sind die Änderungen, die im Lieferumfang von EdgeHTML 13 enthalten sind, dem Modul, das den Microsoft Edge-Browser im [ersten wichtigen Update](https://blogs.windows.com/windowsexperience/2015/11/12) für Windows 10 (11/2015, Build 10586 \) einmacht.</span><span class="sxs-lookup"><span data-stu-id="e76ec-105">Here are the changes shipped with EdgeHTML 13, the engine powering the Microsoft Edge browser in the [first major update](https://blogs.windows.com/windowsexperience/2015/11/12) for Windows 10 \(11/2015, Build 10586\).</span></span>  <span data-ttu-id="e76ec-106">Eine Übersicht über Änderungen am gesamten Microsoft Edge-Browser finden Sie unter [Introducing EdgeHTML 13, unser erstes Platt Form Update für Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16).</span><span class="sxs-lookup"><span data-stu-id="e76ec-106">For an overview of changes to the overall Microsoft Edge browser, see [Introducing EdgeHTML 13, our first platform update for Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16).</span></span>  

<span data-ttu-id="e76ec-107">Hier ist der Permalink für die folgende Liste der  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md) Änderungen:</span><span class="sxs-lookup"><span data-stu-id="e76ec-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md).</span></span>  

## <span data-ttu-id="e76ec-108">Features</span><span class="sxs-lookup"><span data-stu-id="e76ec-108">Features</span></span>  

### <span data-ttu-id="e76ec-109">CSS</span><span class="sxs-lookup"><span data-stu-id="e76ec-109">CSS</span></span>  

<span data-ttu-id="e76ec-110">EdgeHTML 13 unterstützt neue CSS-Features, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="e76ec-110">EdgeHTML 13 supports new CSS features, including:</span></span>  

*   [<span data-ttu-id="e76ec-111">Pseudo Klassen für CSS-Veränderlichkeit</span><span class="sxs-lookup"><span data-stu-id="e76ec-111">CSS Mutability Pseudo-classes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/cssmutabilitypseudoclasses)  
*   [<span data-ttu-id="e76ec-112">Pseudo Klassen für CSS-Bereich</span><span class="sxs-lookup"><span data-stu-id="e76ec-112">CSS Range Pseudo-classes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/cssrangepseudoclasses)  
*   <span data-ttu-id="e76ec-113">CSS- [anfangs](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) -und [unset](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue) -Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e76ec-113">CSS [initial](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) and [unset](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue) keywords</span></span>  

### <span data-ttu-id="e76ec-114">Verschlüsselte Medienerweiterungen</span><span class="sxs-lookup"><span data-stu-id="e76ec-114">Encrypted Media Extensions</span></span>  

<span data-ttu-id="e76ec-115">Microsoft Edge unterstützt jetzt die neuen APIs für [verschlüsselte Medienerweiterungen](https://w3.org/TR/encrypted-media) mit unpräfixen.</span><span class="sxs-lookup"><span data-stu-id="e76ec-115">Microsoft Edge now supports the new unprefixed [Encrypted Media Extensions](https://w3.org/TR/encrypted-media) APIs.</span></span>  <span data-ttu-id="e76ec-116">Verschlüsselte Medienerweiterungen \ (EME \) erweitert die Video-und Audioelemente, um DRM-geschützte Inhalte (Digital Rights Management) zu aktivieren, ohne Plug-ins zu verwenden.  Weitere Informationen finden Sie unter eme:  [verschlüsselte Medienerweiterungen](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API).</span><span class="sxs-lookup"><span data-stu-id="e76ec-116">Encrypted Media Extensions \(EME\) extends the video and audio elements to enable Digital Rights Management \(DRM\) protected content without using plug-ins.  Read more about EME:  [Encrypted Media Extensions](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API).</span></span>  

### <span data-ttu-id="e76ec-117">Grafiken</span><span class="sxs-lookup"><span data-stu-id="e76ec-117">Graphics</span></span>  

<span data-ttu-id="e76ec-118">EdgeHTML 13 stellt die folgenden Grafik Updates vor:</span><span class="sxs-lookup"><span data-stu-id="e76ec-118">EdgeHTML 13 introduces the following graphics updates:</span></span>  

*   [<span data-ttu-id="e76ec-119">Canvas-Ellipse</span><span class="sxs-lookup"><span data-stu-id="e76ec-119">Canvas ellipse</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/canvas2dellipse)  
*   [<span data-ttu-id="e76ec-120">Füllmethoden für Leinwand</span><span class="sxs-lookup"><span data-stu-id="e76ec-120">Canvas blending modes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/compositingandblendingincanvas2d)  
*   [<picture> <span data-ttu-id="e76ec-121">Element </span><span class="sxs-lookup"><span data-stu-id="e76ec-121">element</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/pictureelement)  
*   [<span data-ttu-id="e76ec-122">SVG-externer Inhalt</span><span class="sxs-lookup"><span data-stu-id="e76ec-122">SVG external content</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/svgexternalcontent)  

### <span data-ttu-id="e76ec-123">JavaScript</span><span class="sxs-lookup"><span data-stu-id="e76ec-123">JavaScript</span></span>  

<span data-ttu-id="e76ec-124">EdgeHTML 13 umfasst [wichtige Verbesserungen und die Unterstützung neuer Features in Chakra](https://blogs.windows.com/msedgedev/2015/09/30), dem JavaScript-Modul, das Microsoft Edge anbietet, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="e76ec-124">EdgeHTML 13 includes [major improvements and new feature support in Chakra](https://blogs.windows.com/msedgedev/2015/09/30), the JavaScript engine powering Microsoft Edge, including:</span></span>  

#### <span data-ttu-id="e76ec-125">Neue Funktionen</span><span class="sxs-lookup"><span data-stu-id="e76ec-125">New features</span></span>  

<span data-ttu-id="e76ec-126">Standardmäßig aktiviert</span><span class="sxs-lookup"><span data-stu-id="e76ec-126">On by default</span></span>  

*   <span data-ttu-id="e76ec-127">Standardmäßig aktiviert [asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) \ ([Blogbeitrag](https://blogs.windows.com/msedgedev/2015/11/10), [Demo](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)</span><span class="sxs-lookup"><span data-stu-id="e76ec-127">[asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) enabled by default \([blog post](https://blogs.windows.com/msedgedev/2015/11/10), [demo](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)</span></span>  
*   <span data-ttu-id="e76ec-128">[Classes](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \ (ES2015 \)</span><span class="sxs-lookup"><span data-stu-id="e76ec-128">[Classes](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \(ES2015\)</span></span>  

#### <span data-ttu-id="e76ec-129">Experimentelle JavaScript-Features</span><span class="sxs-lookup"><span data-stu-id="e76ec-129">Experimental JavaScript features</span></span>  

<span data-ttu-id="e76ec-130">Aktiviert mit</span><span class="sxs-lookup"><span data-stu-id="e76ec-130">Enabled with</span></span> `about:flags`  

*   <span data-ttu-id="e76ec-131">[Asynchrone Funktionen](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \ (ES2016 \)</span><span class="sxs-lookup"><span data-stu-id="e76ec-131">[Async functions](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \(ES2016\)</span></span>  
*   <span data-ttu-id="e76ec-132">[Potenz Operator](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \ (ES2016 \)</span><span class="sxs-lookup"><span data-stu-id="e76ec-132">[Exponentiation operator](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \(ES2016\)</span></span>  
*   <span data-ttu-id="e76ec-133">[Destrukturierung](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \ (ES2015 \)</span><span class="sxs-lookup"><span data-stu-id="e76ec-133">[Destructuring](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \(ES2015\)</span></span>  

### <span data-ttu-id="e76ec-134">Benutzereingabe</span><span class="sxs-lookup"><span data-stu-id="e76ec-134">User Input</span></span>  

<span data-ttu-id="e76ec-135">Die folgenden in EdgeHTML 13 eingeführten Features verbessern die Benutzereingabe:</span><span class="sxs-lookup"><span data-stu-id="e76ec-135">The following features introduced in EdgeHTML 13 improve user input:</span></span>  

*   [\<meter\> <span data-ttu-id="e76ec-136">Element </span><span class="sxs-lookup"><span data-stu-id="e76ec-136">element</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/meterelement)  
*   [<span data-ttu-id="e76ec-137">oninvalid-Ereignishandler für das Element Dokument und-Fenster</span><span class="sxs-lookup"><span data-stu-id="e76ec-137">oninvalid event handler for the element document and window</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/oninvalideventhandler)  

### <span data-ttu-id="e76ec-138">Zeiger Sperre</span><span class="sxs-lookup"><span data-stu-id="e76ec-138">Pointer Lock</span></span>  

<span data-ttu-id="e76ec-139">Microsoft Edge unterstützt jetzt die Pointer Lock-API \ (zuvor als "Maus Sperre" bezeichnet) für den Zugriff auf rohe Mausbewegungen, das Ziel von Mausereignissen auf ein einzelnes Element sperren, wodurch Grenzwerte für die Mausbewegung in einer einzelnen Richtung beseitigt werden und der Cursor aus der Ansicht entfernt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e76ec-139">Microsoft Edge now supports the Pointer Lock API \(previously called Mouse Lock\) for access to raw mouse movement, locking the target of mouse events to a single element, eliminating limits of how far mouse movement can go in a single direction, and removing the cursor from view.</span></span>  

## <span data-ttu-id="e76ec-140">Neue APIs in EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="e76ec-140">New APIs in EdgeHTML 13</span></span>  

<span data-ttu-id="e76ec-141">Hier finden Sie die vollständige Liste der neuen APIs in EdgeHTML 13.</span><span class="sxs-lookup"><span data-stu-id="e76ec-141">Here's the full list of new APIs in EdgeHTML 13.</span></span>  <span data-ttu-id="e76ec-142">Sie werden im Format von angezeigt `[interface name].[api name]` .</span><span class="sxs-lookup"><span data-stu-id="e76ec-142">They are listed in the format of `[interface name].[api name]`.</span></span>  

<iframe height='584' scrolling='no' title='<span data-ttu-id="e76ec-143">Neue APIs in EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="e76ec-143">New APIs in EdgeHTML 13</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/vmzxEY/?height=584&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width:  100%;'><span data-ttu-id="e76ec-144">Weitere Informationen finden Sie in den neuen APIs für Stifte <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'> in EdgeHTML 13 </a> von Microsoft Edge docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) auf <a href='http://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="e76ec-144">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'>New APIs in EdgeHTML 13</a> by Microsoft Edge Docs (<a href='http://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='http://codepen.io'>CodePen</a>.</span></span></iframe>  
