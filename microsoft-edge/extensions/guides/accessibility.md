---
ms.assetid: c4544a19-de78-4c69-a042-c0415726548f
description: Wenn Sie sicherstellen möchten, dass das Symbol ihrer Erweiterung im hellen und im dunklen Modus angezeigt wird, folgen Sie dem Leitfaden zur Barrierefreiheit.
title: Barrierefreiheits Erweiterungen (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: 60e794467c6d054e390ce61c40559afa3a110c21
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882793"
---
# <span data-ttu-id="9be1b-104">Barrierefreiheits Erweiterungen (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="9be1b-104">Accessibility - Extensions (EdgeHTML)</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <span data-ttu-id="9be1b-105">Erstellen von barrierefreien Erweiterungssymbolen für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9be1b-105">Creating accessible extension icons for Microsoft Edge</span></span>

<span data-ttu-id="9be1b-106">Entwickler von Drittanbieter-Erweiterungen werden ermutigt, Bildressourcen zu verwenden, die den strengen Barrierefreiheitsanforderungen von Microsoft entsprechen, damit Symbole für helle und dunkle Designs deutlich sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="9be1b-106">Third-party extension developers are encouraged to use image assets that meet Microsoft’s strict accessibility requirements so that icons are clearly visible for both light and dark themes.</span></span> <span data-ttu-id="9be1b-107">Wir empfehlen, dass alle Erweiterungssymbole ein 14:1-Verhältnis zwischen der Hintergrundfarbe des Symbols und der dominierenden Farbe des Symbols selbst aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9be1b-107">We recommend that all extension icons have a 14:1 ratio between the icon’s background color and the dominant color of the icon itself.</span></span>


<span data-ttu-id="9be1b-108">Von Microsoft entwickelte First-Party-Erweiterungen wenden eine visuelle Behandlung mit "Aufklebern" an, um diese Anforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="9be1b-108">First-party extensions developed by Microsoft apply a “stickering” visual treatment to satisfy these requirements.</span></span>

### <span data-ttu-id="9be1b-109">Beispiele für "Aufkleber"</span><span class="sxs-lookup"><span data-stu-id="9be1b-109">Examples of the "stickering"</span></span>

<span data-ttu-id="9be1b-110">Das Hauptziel von "Aufklebern" besteht darin, das Symbol visuell auf jeder Hintergrundfarbe zugänglich zu machen.</span><span class="sxs-lookup"><span data-stu-id="9be1b-110">The main goal of “stickering” is to make the icon visually accessible on any background color.</span></span> <span data-ttu-id="9be1b-111">Das empfohlene Farb Verhältnis zwischen dem weißen äußeren Strich und dem Symbol sollte 14:1 sein, um die hohen Kontrast Anforderungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9be1b-111">The recommended color ratio between the white outer stroke and your icon should be 14:1 to support the high contrast requirements.</span></span>

#### <span data-ttu-id="9be1b-112">Gutes Symbol</span><span class="sxs-lookup"><span data-stu-id="9be1b-112">Good icon</span></span>
<span data-ttu-id="9be1b-113">Mit Aufklebern bleibt ein in erster Linie dunkleres Symbol auf jeder Hintergrundfarbe sichtbar.</span><span class="sxs-lookup"><span data-stu-id="9be1b-113">With stickering, a primarily dark icon will remain visible on any background color.</span></span>


![Abbildung des Symbols, das auf einer beliebigen Hintergrundfarbe angezeigt wird](./../media/accessibility-light-to-dark-good.png)

#### <span data-ttu-id="9be1b-115">Ungültiges Symbol</span><span class="sxs-lookup"><span data-stu-id="9be1b-115">Bad icon</span></span>
<span data-ttu-id="9be1b-116">Ohne Aufkleber kann ein Symbol in den Hintergrund integriert werden, sodass es nicht mehr zu sehen ist.</span><span class="sxs-lookup"><span data-stu-id="9be1b-116">Without stickering, an icon could blend in with the background and become impossible to see.</span></span>


![Abbildung des Symbols, das in schwarzen Hintergrund verschmilzt](./../media/accessibility-light-to-dark-bad.png)

### <span data-ttu-id="9be1b-118">"Aufkleber" für Ihr Erweiterungssymbol</span><span class="sxs-lookup"><span data-stu-id="9be1b-118">"Stickering" your extension icon</span></span>

<span data-ttu-id="9be1b-119">In den folgenden fünf Schritten wird die vorgeschlagene Methode zum Erstellen eines Erweiterungssymbols erläutert, das den Barrierefreiheitsanforderungen von Microsoft entspricht:</span><span class="sxs-lookup"><span data-stu-id="9be1b-119">The following five steps outline the suggested method of creating an extension icon that meets Microsoft’s accessibility requirements:</span></span>


| <span data-ttu-id="9be1b-120">Schritt 1</span><span class="sxs-lookup"><span data-stu-id="9be1b-120">Step 1</span></span>                                       | <span data-ttu-id="9be1b-121">Schritt 2</span><span class="sxs-lookup"><span data-stu-id="9be1b-121">Step 2</span></span>                                       | <span data-ttu-id="9be1b-122">Schritt 3</span><span class="sxs-lookup"><span data-stu-id="9be1b-122">Step 3</span></span>                                                                                 | <span data-ttu-id="9be1b-123">Schritt 4</span><span class="sxs-lookup"><span data-stu-id="9be1b-123">Step 4</span></span>                                                                          | <span data-ttu-id="9be1b-124">Schritt 5</span><span class="sxs-lookup"><span data-stu-id="9be1b-124">Step 5</span></span>                                                       |
|:---------------------------------------------|:---------------------------------------------|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span data-ttu-id="9be1b-125">Setzen Sie das Symbol innerhalb des angegebenen Rasters.</span><span class="sxs-lookup"><span data-stu-id="9be1b-125">Set your icon within your specified grid.</span></span>    | <span data-ttu-id="9be1b-126">Verringern Sie die Größe des Symbols um 2 Pixel.</span><span class="sxs-lookup"><span data-stu-id="9be1b-126">Reduce your icon size by 2 pixels.</span></span>           | <span data-ttu-id="9be1b-127">Kopieren Sie das Symbol, und fügen Sie es ein.</span><span class="sxs-lookup"><span data-stu-id="9be1b-127">Copy your icon and paste in place.</span></span> <span data-ttu-id="9be1b-128">Erstellen Sie einen äußeren Strich mit 2 Pixeln mit abgerundeten Ecken.</span><span class="sxs-lookup"><span data-stu-id="9be1b-128">Create a 2 pixel outer stroke with rounded corners.</span></span> | <span data-ttu-id="9be1b-129">Skizzieren Sie den Strich, geben Sie den zusammengesetzten Pfad frei, und verbinden Sie die restlichen Shapes.</span><span class="sxs-lookup"><span data-stu-id="9be1b-129">Outline your stroke, release the compound path, and merge the remaining shapes.</span></span> | <span data-ttu-id="9be1b-130">Färben Sie den äußeren Strich weiß und das innere Symbol, wie Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="9be1b-130">Color the outer stroke white and the inner icon as you wish.</span></span> |
| ![step1](./../media/accessibility-step1.png) | ![step2](./../media/accessibility-step2.png) | ![step3](./../media/accessibility-step3.png)                                           | ![Schritt4](./../media/accessibility-step4.png)                                    | ![step5](./../media/accessibility-step5.png)                 |

