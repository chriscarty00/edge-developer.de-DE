---
title: Emulieren von Sehstörungen in Microsoft Edge devtools (Farbenblindheit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: b70499fa189d162fa7589966bab183f4c12f68f7
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843921"
---
# <span data-ttu-id="fd807-103">Emulieren von Sehstörungen</span><span class="sxs-lookup"><span data-stu-id="fd807-103">Emulate vision deficiencies</span></span>

<span data-ttu-id="fd807-104">Um die Anforderungen Ihrer Benutzer mit [farbsehstörungen][ColorblindawarenessMain] zu erfüllen \ (Farbenblindheit \), können Sie mit [Microsoft Edge devtools][MicrosoftEdgeDevTools] bestimmte farbsehstörungen simulieren.</span><span class="sxs-lookup"><span data-stu-id="fd807-104">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\), [Microsoft Edge DevTools][MicrosoftEdgeDevTools] enable you to simulate specific color vision deficiencies.</span></span>  <span data-ttu-id="fd807-105">Das Tool zum **emulieren von Sehstörungen** simuliert die folgenden Kategorien.</span><span class="sxs-lookup"><span data-stu-id="fd807-105">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="fd807-106">Farbsehstörungen</span><span class="sxs-lookup"><span data-stu-id="fd807-106">Color vision deficiency</span></span> | <span data-ttu-id="fd807-107">Details</span><span class="sxs-lookup"><span data-stu-id="fd807-107">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="fd807-108">Verschwommenes Sehvermögen</span><span class="sxs-lookup"><span data-stu-id="fd807-108">Blurred vision</span></span> | <span data-ttu-id="fd807-109">Der Benutzer hat Schwierigkeiten, sich auf feine Details zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="fd807-109">The user has difficulty focusing on fine details.</span></span> |   
| <span data-ttu-id="fd807-110">Protanopie</span><span class="sxs-lookup"><span data-stu-id="fd807-110">Protanopia</span></span> | <span data-ttu-id="fd807-111">Der Benutzer kann keine rote Leuchte erkennen.</span><span class="sxs-lookup"><span data-stu-id="fd807-111">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="fd807-112">Deuteranopie</span><span class="sxs-lookup"><span data-stu-id="fd807-112">Deuteranopia</span></span> | <span data-ttu-id="fd807-113">Der Benutzer kann kein grünes Licht erkennen.</span><span class="sxs-lookup"><span data-stu-id="fd807-113">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="fd807-114">Tritanopie</span><span class="sxs-lookup"><span data-stu-id="fd807-114">Tritanopia</span></span> | <span data-ttu-id="fd807-115">Der Benutzer kann keine blauen Lichter erkennen.</span><span class="sxs-lookup"><span data-stu-id="fd807-115">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="fd807-116">Achromatopsie</span><span class="sxs-lookup"><span data-stu-id="fd807-116">Achromatopsia</span></span> | <span data-ttu-id="fd807-117">Der Benutzer kann keine Farbe wahrnehmen, wodurch alle Farben auf eine Grauschattierung reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="fd807-117">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  

## <span data-ttu-id="fd807-118">Navigieren zu den Render-Tools</span><span class="sxs-lookup"><span data-stu-id="fd807-118">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="fd807-119">Um einen Sehstörungen zu simulieren, der für Ihr Web-Produkt angewendet wird, öffnen Sie die [Rendering-Tools][RenderingTools].</span><span class="sxs-lookup"><span data-stu-id="fd807-119">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][RenderingTools].</span></span>  

1.  <span data-ttu-id="fd807-120">Öffnen der Rendering-Tools durch Auswählen des `...` Menüelements in der Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="fd807-120">Open the Rendering Tools by selecting the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="fd807-121">Auswählen</span><span class="sxs-lookup"><span data-stu-id="fd807-121">Select</span></span> `More tools`  
1.  <span data-ttu-id="fd807-122">Auswählen</span><span class="sxs-lookup"><span data-stu-id="fd807-122">Select</span></span> `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Öffnen der Rendering-Tools" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="fd807-124">Öffnen der **Rendering-Tools**</span><span class="sxs-lookup"><span data-stu-id="fd807-124">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="fd807-125">Das **Rendering** -Menü wird im Einzug angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fd807-125">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="fd807-126">Scrollen Sie nach unten zum `Emulate vision deficiencies` Menüelement, und wählen Sie das Dropdownmenü aus, um die Optionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fd807-126">Scroll down to the `Emulate vision deficiencies` menu item and select the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Das Menü "Sehstörungen emulieren" auf der Rendering-Schublade" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="fd807-128">Das Menü " **Sehstörungen emulieren** " auf der **Rendering** -Schublade</span><span class="sxs-lookup"><span data-stu-id="fd807-128">The **Emulate vision deficiencies** menu on the **Rendering** drawer</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fd807-129">Wählen Sie eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="fd807-129">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Menü Optionen für das Emulieren von Sehstörungen" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="fd807-131">Menü Optionen für das **emulieren von Sehstörungen**</span><span class="sxs-lookup"><span data-stu-id="fd807-131">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fd807-132">Das Hauptfenster zeigt die Simulation der ausgewählten Option an, die auf die aktuelle Seite angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fd807-132">The main windows displays the simulation of your selected option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Anzeige mit \* \* verschwommener Sehkraft \* \*-Simulation" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="fd807-134">Anzeige mithilfe einer **verschwommenen Bild** Simulation</span><span class="sxs-lookup"><span data-stu-id="fd807-134">Display using **Blurred Vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Anzeige mit \* \* Achromatopsie \* \*-Simulation" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="fd807-136">Anzeigen mithilfe der **Achromatopsie** -Simulation</span><span class="sxs-lookup"><span data-stu-id="fd807-136">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="fd807-137">Verwenden des Befehlsmenüs</span><span class="sxs-lookup"><span data-stu-id="fd807-137">Use the Command Menu</span></span>  

<span data-ttu-id="fd807-138">Sie können auch das **Befehlsmenü** verwenden, um auf die verschiedenen Simulationen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="fd807-138">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="fd807-139">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fd807-139">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="fd807-141">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="fd807-141">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fd807-142">Geben Sie ein `emulate` , was Sie simulieren möchten, und drücken Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="fd807-142">Type `emulate`, choose what you want to simulate and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Die verschiedenen Simulationsoptionen, die im Befehlsmenü zur Verfügung stehen" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="fd807-144">Die verschiedenen Simulationsoptionen, die im **Befehlsmenü** zur Verfügung stehen</span><span class="sxs-lookup"><span data-stu-id="fd807-144">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="fd807-145">Die Tools zum **emulieren von Sehvermögen-Mängeln** simulieren Näherungswerte, wie eine Person mit jedem Mangel Ihr Produkt sehen kann.</span><span class="sxs-lookup"><span data-stu-id="fd807-145">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="fd807-146">Die einzelnen Personen sind unterschiedlich, daher variieren Sehstörungen in Schweregraden von Person zu Person.</span><span class="sxs-lookup"><span data-stu-id="fd807-146">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="fd807-147">Um die Anforderungen Ihrer Benutzer besser erfüllen zu können, sollten Sie keine Farbkombinationen verwenden, die möglicherweise ein Problem sind.</span><span class="sxs-lookup"><span data-stu-id="fd807-147">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="fd807-148">Die Tools zum **emulieren von Sehstörungen** sind keine vollständige Beurteilung der Barrierefreiheit Ihres Produkts.</span><span class="sxs-lookup"><span data-stu-id="fd807-148">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="fd807-149">Stattdessen sollten die Tools zum **emulieren von Sehstörungen** ein guter erster Schritt sein, um Probleme zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="fd807-149">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "Die Organisation der farbenblinden Sensibilisierung"  
[AmfcbMain]: https://www.amfcb.org "Die amerikanische Stiftung für das Farben Blind (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Microsoft Edge (Chrom)-Rendering-Tools"  
