---
title: Emulieren von Sehstörungen in Microsoft Edge devtools (Farbenblindheit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 0b608f5fe67724eee81aeb993577ee9b45cbca09
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758083"
---
# <span data-ttu-id="897ea-103">Emulieren von Sehstörungen</span><span class="sxs-lookup"><span data-stu-id="897ea-103">Emulate vision deficiencies</span></span>

<span data-ttu-id="897ea-104">Weltweit haben etwa 8% der Männer und 0,5% der Frauen einen [farbsehstörungen-Mangel][ColorblindawarenessMain] , der gemeinhin als "Farbenblindheit" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="897ea-104">Worldwide approximately 8% of men and 0.5% of women have a [color vision deficiency][ColorblindawarenessMain] commonly named "Color Blindness".</span></span>  <span data-ttu-id="897ea-105">[Microsoft Edge devtools][MicrosoftEdgeDevTools] ermöglicht es Ihnen, verschiedene bekannte Mängel zu emulieren und eine Vorschau Ihres Produkts zur Verfügung zu stellen, die Sie überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="897ea-105">[Microsoft Edge DevTools][MicrosoftEdgeDevTools] enables you to emulate various known deficiencies and provide a preview of your product for you to review.</span></span>  

| <span data-ttu-id="897ea-106">Farb Mangel</span><span class="sxs-lookup"><span data-stu-id="897ea-106">Color Deficiency</span></span> | <span data-ttu-id="897ea-107">Details</span><span class="sxs-lookup"><span data-stu-id="897ea-107">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="897ea-108">Verschwommenes Sehvermögen</span><span class="sxs-lookup"><span data-stu-id="897ea-108">Blurred vision</span></span> |  |   
| <span data-ttu-id="897ea-109">Protanopie</span><span class="sxs-lookup"><span data-stu-id="897ea-109">Protanopia</span></span> | <span data-ttu-id="897ea-110">Die Unfähigkeit, jedes rote Licht wahrzunehmen.</span><span class="sxs-lookup"><span data-stu-id="897ea-110">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="897ea-111">Deuteranopie</span><span class="sxs-lookup"><span data-stu-id="897ea-111">Deuteranopia</span></span> | <span data-ttu-id="897ea-112">Die Unfähigkeit, grünes Licht wahrzunehmen.</span><span class="sxs-lookup"><span data-stu-id="897ea-112">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="897ea-113">Tritanopie</span><span class="sxs-lookup"><span data-stu-id="897ea-113">Tritanopia</span></span> | <span data-ttu-id="897ea-114">Die Unfähigkeit, ein blaues Licht wahrzunehmen.</span><span class="sxs-lookup"><span data-stu-id="897ea-114">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="897ea-115">Achromatopsie</span><span class="sxs-lookup"><span data-stu-id="897ea-115">Achromatopsia</span></span> | <span data-ttu-id="897ea-116">Die Unfähigkeit, eine beliebige Farbe wahrzunehmen, mit Ausnahme von Grautönen.</span><span class="sxs-lookup"><span data-stu-id="897ea-116">The inability to perceive any color, except for shades of grey.</span></span> |  

## <span data-ttu-id="897ea-117">Navigieren zu den Render-Tools</span><span class="sxs-lookup"><span data-stu-id="897ea-117">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="897ea-118">Wenn Sie Ihr Aktuelles Web-Produkt nach Farbmängeln testen möchten, öffnen Sie die [Rendering-Tools][RenderingTools].</span><span class="sxs-lookup"><span data-stu-id="897ea-118">To test your current web product for color deficiencies, open the [Rendering Tools][RenderingTools].</span></span>  

1.  <span data-ttu-id="897ea-119">Öffnen der Rendering-Tools durch Auswählen des `...` Menüelements in der Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="897ea-119">Open the Rendering Tools by selecting the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="897ea-120">Auswählen</span><span class="sxs-lookup"><span data-stu-id="897ea-120">Select</span></span> `More tools`  
1.  <span data-ttu-id="897ea-121">Auswählen</span><span class="sxs-lookup"><span data-stu-id="897ea-121">Select</span></span> `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Öffnen der Rendering-Tools" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="897ea-123">Öffnen der **Rendering-Tools**</span><span class="sxs-lookup"><span data-stu-id="897ea-123">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="897ea-124">Das **Rendering** -Menü wird in der unteren Hälfte des devtools angezeigt.</span><span class="sxs-lookup"><span data-stu-id="897ea-124">The **Rendering** menu appears in the bottom half of the DevTools.</span></span>  

1.  <span data-ttu-id="897ea-125">Scrollen Sie nach unten zum `Emulate Vision deficiencies` Menüelement, und wählen Sie eine der Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="897ea-125">Scroll down to the `Emulate Vision deficiencies` menu item and select from the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Das Menü "Sehstörungen emulieren" der Rendering-Tools" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="897ea-127">Das Menü " **Sehstörungen emulieren** " der **Rendering** -Tools</span><span class="sxs-lookup"><span data-stu-id="897ea-127">The **Emulate Vision Deficiencies** menu of the **Rendering** tools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="897ea-128">Wählen Sie eine der Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="897ea-128">Choose any of the options</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Menü Optionen für das Emulieren von Sehstörungen" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="897ea-130">Menü Optionen für das **emulieren von Sehstörungen**</span><span class="sxs-lookup"><span data-stu-id="897ea-130">The **Emulate Vision Deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="897ea-131">Die aktuelle Seite wird in einer Simulation angezeigt, wie Sie für einen Benutzer mit dem ausgewählten Mangel aussehen kann.</span><span class="sxs-lookup"><span data-stu-id="897ea-131">The current page is displayed in a simulation of how it may appear to a user with the chosen deficiency.</span></span>  

    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Dokumentation zu Microsoft Edge-Entwickler Tools in verschwommener Vision-Emulation" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="897ea-133">Wird mithilfe einer **verschwommenen Bild** Emulation angezeigt</span><span class="sxs-lookup"><span data-stu-id="897ea-133">Displayed using **Blurred Vision** emulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Dokumentation zu Microsoft Edge-Entwickler Tools in Achromatopsie-Vision-Emulation" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="897ea-135">Anzeige mithilfe der **Achromatopsie-Vision** -Emulation</span><span class="sxs-lookup"><span data-stu-id="897ea-135">Display using **Achromatopsia Vision** emulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="897ea-136">Verwenden des Befehlsmenüs</span><span class="sxs-lookup"><span data-stu-id="897ea-136">Using the command menu</span></span>  

<span data-ttu-id="897ea-137">Sie können die verschiedenen Emulationen auch erreichen, ohne die verschiedenen Menüs über das **Befehlsmenü**zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="897ea-137">You may also reach the different emulations without going through the various menus using the **Command Menu**.</span></span>  

1.  <span data-ttu-id="897ea-138">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="897ea-138">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="897ea-140">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="897ea-140">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="897ea-141">Geben Sie ein `emulate` , was Sie simulieren möchten, und drücken Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="897ea-141">Type `emulate`, choose what you want to simulate and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Die verschiedenen im Befehlsmenü verfügbaren Emulationsoptionen" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="897ea-143">Die verschiedenen im **Befehlsmenü** verfügbaren Emulationsoptionen</span><span class="sxs-lookup"><span data-stu-id="897ea-143">The different emulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="897ea-144">Die Emulations Tools sind näherungsweise, wie eine Person mit jedem Mangel Ihr Produkt sehen kann.</span><span class="sxs-lookup"><span data-stu-id="897ea-144">The emulation tools are approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="897ea-145">Die einzelnen Personen sind unterschiedlich, daher variieren Sehstörungen in Schweregraden von Person zu Person.</span><span class="sxs-lookup"><span data-stu-id="897ea-145">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="897ea-146">Um die Anforderungen Ihrer Benutzer besser erfüllen zu können, sollten Sie keine Farbkombinationen verwenden, die möglicherweise ein Problem sind.</span><span class="sxs-lookup"><span data-stu-id="897ea-146">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="897ea-147">Bei den Emulations Tools handelt es sich nicht um eine vollständige Bewertung der Barrierefreiheit Ihres Produkts, doch sollten Sie einen guten ersten Schritt zur Vermeidung der größten Mängel haben.</span><span class="sxs-lookup"><span data-stu-id="897ea-147">The emulation tools are not a full assessment of the accessibility of your product, but you should have a good first step towards avoiding the biggest deficiencies.</span></span>  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "Die Organisation der farbenblinden Sensibilisierung"  
[AmfcbMain]: https://www.amfcb.org "Die amerikanische Stiftung für das Farben Blind (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Microsoft Edge (Chrom)-Rendering-Tools"  
