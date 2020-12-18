---
description: Emulieren von Sehstörungen in Microsoft Edge devtools
title: Emulieren von Sehstörungen in Microsoft Edge devtools (Farbenblindheit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 5343d32992880f8c60501a86db6cb3a92f417331
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230824"
---
# <span data-ttu-id="3728c-104">Emulieren von Sehstörungen</span><span class="sxs-lookup"><span data-stu-id="3728c-104">Emulate vision deficiencies</span></span>

<span data-ttu-id="3728c-105">Um die Anforderungen Ihrer Benutzer mit [farbsehstörungen][ColorblindawarenessMain] zu erfüllen \ (Farbenblindheit \), können Sie mit [Microsoft Edge devtools][DevtoolsIndex] bestimmte farbsehstörungen simulieren.</span><span class="sxs-lookup"><span data-stu-id="3728c-105">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\), [Microsoft Edge DevTools][DevtoolsIndex] enable you to simulate specific color vision deficiencies.</span></span>  <span data-ttu-id="3728c-106">Das Tool zum **emulieren von Sehstörungen** simuliert die folgenden Kategorien.</span><span class="sxs-lookup"><span data-stu-id="3728c-106">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="3728c-107">Farbsehstörungen</span><span class="sxs-lookup"><span data-stu-id="3728c-107">Color vision deficiency</span></span> | <span data-ttu-id="3728c-108">Details</span><span class="sxs-lookup"><span data-stu-id="3728c-108">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="3728c-109">Verschwommenes Sehvermögen</span><span class="sxs-lookup"><span data-stu-id="3728c-109">Blurred vision</span></span> | <span data-ttu-id="3728c-110">Der Benutzer hat Schwierigkeiten, sich auf feine Details zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="3728c-110">The user has difficulty focusing on fine details.</span></span> |   
| <span data-ttu-id="3728c-111">Protanopie</span><span class="sxs-lookup"><span data-stu-id="3728c-111">Protanopia</span></span> | <span data-ttu-id="3728c-112">Der Benutzer kann keine rote Leuchte erkennen.</span><span class="sxs-lookup"><span data-stu-id="3728c-112">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="3728c-113">Deuteranopie</span><span class="sxs-lookup"><span data-stu-id="3728c-113">Deuteranopia</span></span> | <span data-ttu-id="3728c-114">Der Benutzer kann kein grünes Licht erkennen.</span><span class="sxs-lookup"><span data-stu-id="3728c-114">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="3728c-115">Tritanopie</span><span class="sxs-lookup"><span data-stu-id="3728c-115">Tritanopia</span></span> | <span data-ttu-id="3728c-116">Der Benutzer kann keine blauen Lichter erkennen.</span><span class="sxs-lookup"><span data-stu-id="3728c-116">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="3728c-117">Achromatopsie</span><span class="sxs-lookup"><span data-stu-id="3728c-117">Achromatopsia</span></span> | <span data-ttu-id="3728c-118">Der Benutzer kann keine Farbe wahrnehmen, wodurch alle Farben auf eine Grauschattierung reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="3728c-118">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  

## <span data-ttu-id="3728c-119">Navigieren zu den Render-Tools</span><span class="sxs-lookup"><span data-stu-id="3728c-119">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="3728c-120">Um einen Sehstörungen zu simulieren, der für Ihr Web-Produkt angewendet wird, öffnen Sie die [Rendering-Tools][DevtoolsRenderingToolsIndex].</span><span class="sxs-lookup"><span data-stu-id="3728c-120">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][DevtoolsRenderingToolsIndex].</span></span>  

1.  <span data-ttu-id="3728c-121">So öffnen Sie die Rendering-Tools, indem Sie das `...` Menüelement in der Symbolleiste auswählen</span><span class="sxs-lookup"><span data-stu-id="3728c-121">To open the Rendering Tools, by choose the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="3728c-122">Auswählen</span><span class="sxs-lookup"><span data-stu-id="3728c-122">Choose</span></span> `More tools`  
1.  <span data-ttu-id="3728c-123">Auswählen</span><span class="sxs-lookup"><span data-stu-id="3728c-123">Choose</span></span> `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Öffnen der Rendering-Tools" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="3728c-125">Öffnen der **Rendering-Tools**</span><span class="sxs-lookup"><span data-stu-id="3728c-125">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="3728c-126">Das **Rendering** -Menü wird im Einzug angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3728c-126">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="3728c-127">Scrollen Sie nach unten zum `Emulate vision deficiencies` Menüelement, und wählen Sie das Dropdownmenü aus, um die Optionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3728c-127">Scroll down to the `Emulate vision deficiencies` menu item and choose the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Das Menü "Sehstörungen emulieren" auf der Rendering-Schublade" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="3728c-129">Das Menü " **Sehstörungen emulieren** " auf der **Rendering** -Schublade</span><span class="sxs-lookup"><span data-stu-id="3728c-129">The **Emulate vision deficiencies** menu on the **Rendering** drawer</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3728c-130">Wählen Sie eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="3728c-130">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Menü Optionen für das Emulieren von Sehstörungen" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="3728c-132">Menü Optionen für das **emulieren von Sehstörungen**</span><span class="sxs-lookup"><span data-stu-id="3728c-132">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3728c-133">Das Hauptfenster zeigt die Simulation der ausgewählten Option an, die auf die aktuelle Seite angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3728c-133">The main windows displays the simulation of your chosen option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Anzeige mit \* \* verschwommener Sehkraft \* \*-Simulation" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="3728c-135">Anzeige mithilfe einer **verschwommenen Bild** Simulation</span><span class="sxs-lookup"><span data-stu-id="3728c-135">Display using **Blurred Vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Anzeige mit \* \* Achromatopsie \* \*-Simulation" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="3728c-137">Anzeigen mithilfe der **Achromatopsie** -Simulation</span><span class="sxs-lookup"><span data-stu-id="3728c-137">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="3728c-138">Verwenden des Befehlsmenüs</span><span class="sxs-lookup"><span data-stu-id="3728c-138">Use the Command Menu</span></span>  

<span data-ttu-id="3728c-139">Sie können auch das **Befehlsmenü** verwenden, um auf die verschiedenen Simulationen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="3728c-139">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="3728c-140">Wählen Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3728c-140">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="3728c-142">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="3728c-142">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3728c-143">Geben Sie ein `emulate` , was Sie simulieren und auswählen möchten `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3728c-143">Type `emulate`, choose what you want to simulate and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Die verschiedenen Simulationsoptionen, die im Befehlsmenü zur Verfügung stehen" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="3728c-145">Die verschiedenen Simulationsoptionen, die im **Befehlsmenü** zur Verfügung stehen</span><span class="sxs-lookup"><span data-stu-id="3728c-145">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="3728c-146">Die Tools zum **emulieren von Sehvermögen-Mängeln** simulieren Näherungswerte, wie eine Person mit jedem Mangel Ihr Produkt sehen kann.</span><span class="sxs-lookup"><span data-stu-id="3728c-146">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="3728c-147">Die einzelnen Personen sind unterschiedlich, daher variieren Sehstörungen in Schweregraden von Person zu Person.</span><span class="sxs-lookup"><span data-stu-id="3728c-147">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="3728c-148">Um die Anforderungen Ihrer Benutzer besser erfüllen zu können, sollten Sie keine Farbkombinationen verwenden, die möglicherweise ein Problem sind.</span><span class="sxs-lookup"><span data-stu-id="3728c-148">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="3728c-149">Die Tools zum **emulieren von Sehstörungen** sind keine vollständige Beurteilung der Barrierefreiheit Ihres Produkts.</span><span class="sxs-lookup"><span data-stu-id="3728c-149">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="3728c-150">Stattdessen sollten die Tools zum **emulieren von Sehstörungen** ein guter erster Schritt sein, um Probleme zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="3728c-150">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analysieren der Laufzeitleistung | Microsoft docs"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "Die Organisation der farbenblinden Sensibilisierung"  

[AmfcbMain]: https://www.amfcb.org "Die amerikanische Stiftung für das Farben Blind (AFCB)"  

