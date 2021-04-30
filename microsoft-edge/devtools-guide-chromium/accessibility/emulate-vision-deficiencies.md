---
description: Emulieren von Sehschwächen in Microsoft Edge DevTools.
title: Emulieren von Sehschwächen in Microsoft Edge DevTools (Farbblindheit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 8c3f3a34c441692117906f51c3d8430e79fd72b1
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519170"
---
# <a name="emulate-vision-deficiencies"></a><span data-ttu-id="3a004-104">Emulieren von Sehstörungen</span><span class="sxs-lookup"><span data-stu-id="3a004-104">Emulate vision deficiencies</span></span>

<span data-ttu-id="3a004-105">Um die Anforderungen Ihrer Benutzer [][ColorblindawarenessMain] mit Farbsichtschwäche \(Farbblindheit\) besser zu erfüllen, können Sie mit [Microsoft Edge DevTools][DevtoolsIndex] bestimmte Farbsichtschwächen simulieren.</span><span class="sxs-lookup"><span data-stu-id="3a004-105">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\), [Microsoft Edge DevTools][DevtoolsIndex] allow you to simulate specific color vision deficiencies.</span></span>  <span data-ttu-id="3a004-106">Das **Tool Zum Emulieren von Sehschwächen** simuliert die folgenden Kategorien.</span><span class="sxs-lookup"><span data-stu-id="3a004-106">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="3a004-107">Mangel an Farbsicht</span><span class="sxs-lookup"><span data-stu-id="3a004-107">Color vision deficiency</span></span> | <span data-ttu-id="3a004-108">Details</span><span class="sxs-lookup"><span data-stu-id="3a004-108">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="3a004-109">Verschwommenes Sehen</span><span class="sxs-lookup"><span data-stu-id="3a004-109">Blurred vision</span></span> | <span data-ttu-id="3a004-110">Der Benutzer hat Schwierigkeiten, sich auf feine Details zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="3a004-110">The user has difficulty focusing on fine details.</span></span> |  
| <span data-ttu-id="3a004-111">Protanopia</span><span class="sxs-lookup"><span data-stu-id="3a004-111">Protanopia</span></span> | <span data-ttu-id="3a004-112">Der Benutzer kann kein rotes Licht wahrnehmen.</span><span class="sxs-lookup"><span data-stu-id="3a004-112">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="3a004-113">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="3a004-113">Deuteranopia</span></span> | <span data-ttu-id="3a004-114">Der Benutzer kann kein grünes Licht wahrnehmen.</span><span class="sxs-lookup"><span data-stu-id="3a004-114">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="3a004-115">Tritanopie</span><span class="sxs-lookup"><span data-stu-id="3a004-115">Tritanopia</span></span> | <span data-ttu-id="3a004-116">Der Benutzer kann kein blaues Licht wahrnehmen.</span><span class="sxs-lookup"><span data-stu-id="3a004-116">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="3a004-117">Achromatopsie</span><span class="sxs-lookup"><span data-stu-id="3a004-117">Achromatopsia</span></span> | <span data-ttu-id="3a004-118">Der Benutzer kann keine Farbe wahrnehmen, wodurch alle Farben auf einen Grauton reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="3a004-118">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  

## <a name="navigate-to-the-rendering-tools"></a><span data-ttu-id="3a004-119">Navigieren zu den Renderingtools</span><span class="sxs-lookup"><span data-stu-id="3a004-119">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="3a004-120">Um einen Sehschwächenmangel zu simulieren, der für Ihr Webprodukt angewendet wird, öffnen Sie die [Renderingtools][DevtoolsRenderingToolsIndex].</span><span class="sxs-lookup"><span data-stu-id="3a004-120">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][DevtoolsRenderingToolsIndex].</span></span>  

1.  <span data-ttu-id="3a004-121">Um die Renderingtools zu öffnen, wählen Sie das `...` Menüelement in der Symbolleiste aus.</span><span class="sxs-lookup"><span data-stu-id="3a004-121">To open the Rendering Tools, choose the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="3a004-122">Weitere **Tools auswählen**</span><span class="sxs-lookup"><span data-stu-id="3a004-122">Choose **More tools**</span></span>  
1.  <span data-ttu-id="3a004-123">Rendern **auswählen**</span><span class="sxs-lookup"><span data-stu-id="3a004-123">Choose **Rendering**</span></span>  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Öffnen der Renderingtools" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="3a004-125">Öffnen der **Renderingtools**</span><span class="sxs-lookup"><span data-stu-id="3a004-125">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="3a004-126">Das **Menü Rendering** wird in der Schublade angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3a004-126">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="3a004-127">Scrollen Sie nach unten `Emulate vision deficiencies` zum Menüelement, und wählen Sie das Dropdownmenü aus, um die Optionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3a004-127">Scroll down to the `Emulate vision deficiencies` menu item and choose the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Das Menü Sehschwächen emulieren in der Renderschubschubleiste" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="3a004-129">Das **Menü Visionsmangel emulieren** in der **Renderschubleiste**</span><span class="sxs-lookup"><span data-stu-id="3a004-129">The **Emulate vision deficiencies** menu on the **Rendering** drawer</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3a004-130">Wählen Sie eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="3a004-130">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Menüoptionen Visionsmangel emulieren" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="3a004-132">Menüoptionen **zum Emulieren von Sehschwächen**</span><span class="sxs-lookup"><span data-stu-id="3a004-132">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3a004-133">In den Hauptfenstern wird die Simulation der ausgewählten Option angezeigt, die auf die aktuelle Seite angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3a004-133">The main windows displays the simulation of your chosen option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Anzeigen mithilfe der Simulation **Blurred Vision**" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="3a004-135">Anzeigen mithilfe einer **Simulation mit verschwommener** Vision</span><span class="sxs-lookup"><span data-stu-id="3a004-135">Display using **Blurred Vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Anzeigen mithilfe der **Achromatopsia**-Simulation" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="3a004-137">Anzeigen mithilfe **der Achromatopsia-Simulation**</span><span class="sxs-lookup"><span data-stu-id="3a004-137">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <a name="use-the-command-menu"></a><span data-ttu-id="3a004-138">Verwenden des Befehlsmenüs</span><span class="sxs-lookup"><span data-stu-id="3a004-138">Use the Command Menu</span></span>  

<span data-ttu-id="3a004-139">Sie können auch das **Befehlsmenü verwenden,** um auf die verschiedenen Simulationen zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="3a004-139">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="3a004-140">Wählen `Ctrl` + `Shift` + `P` Sie \(Windows/Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü zu öffnen.**</span><span class="sxs-lookup"><span data-stu-id="3a004-140">Select `Ctrl`+`Shift`+`P` \(Windows/Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="3a004-142">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="3a004-142">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3a004-143">Geben `emulate` Sie ein, wählen Sie aus, was Sie simulieren möchten, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="3a004-143">Type `emulate`, choose what you want to simulate and choose `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Die verschiedenen Simulationsoptionen, die im Befehlsmenü verfügbar sind" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="3a004-145">Die verschiedenen Simulationsoptionen, die im **Befehlsmenü verfügbar sind**</span><span class="sxs-lookup"><span data-stu-id="3a004-145">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="3a004-146">Die **Tools zum Emulieren** von Sehschwächen simulieren Näherungen darüber, wie eine Person mit jedem Mangel Ihr Produkt sehen kann.</span><span class="sxs-lookup"><span data-stu-id="3a004-146">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="3a004-147">Jede Person ist unterschiedlich, daher variieren Sehschwächen im Schweregrad von Person zu Person.</span><span class="sxs-lookup"><span data-stu-id="3a004-147">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="3a004-148">Um die Anforderungen Ihrer Benutzer besser zu erfüllen, vermeiden Sie jede Farbkombination, die ein Problem sein kann.</span><span class="sxs-lookup"><span data-stu-id="3a004-148">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="3a004-149">Die **Emulate vision deficiencies tools** sind keine vollständige Barrierefreiheitsbewertung Ihres Produkts.</span><span class="sxs-lookup"><span data-stu-id="3a004-149">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="3a004-150">Stattdessen sollten Sie mit **den Tools zum** Emulieren von Sehschwächen einen guten ersten Schritt zur Vermeidung von Problemen finden.</span><span class="sxs-lookup"><span data-stu-id="3a004-150">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  

<!-- links -->  

[DevToolsIndex]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analysieren der Laufzeitleistung | Microsoft Docs"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "Die Organisation &quot;Farbblindheit&quot;"  

[AmfcbMain]: https://www.amfcb.org "The American Foundation for the Color Blind (AFCB)"  
