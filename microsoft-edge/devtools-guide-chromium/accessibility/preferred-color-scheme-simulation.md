---
description: Erzwingen Microsoft Edge DevTools in den Vorschaumodus des Farbschemas.
title: Erzwingen Microsoft Edge DevTools in den Farbschemavorschaumodus (CSS bevorzugt Farbschema)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 1cdc9601e9e6fea1f6921c6cc40a1ed8232a0da8
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519149"
---
# <a name="dark-or-light-color-scheme-simulation"></a><span data-ttu-id="b7faf-104">Simulation des dunklen oder hellen Farbschemas</span><span class="sxs-lookup"><span data-stu-id="b7faf-104">Dark or Light Color Scheme simulation</span></span>  

<span data-ttu-id="b7faf-105">Betriebssysteme können jede Anwendung in dunkleren oder helleren Farben anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b7faf-105">Operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="b7faf-106">Ein Webprodukt mit einem hellen Design in einem Betriebssystem im dunklen Modus ist Gitter und kann für einige Benutzer ein Problem mit der Barrierefreiheit sein.</span><span class="sxs-lookup"><span data-stu-id="b7faf-106">Having a web product that has a light theme in a dark mode operating system is grating and can be an accessibility issue for some users.</span></span>  <span data-ttu-id="b7faf-107">Im Web können Sie die CSS-Medienabfrage mit dem [Bevorzugt-Farbschema][MDNPrefersColorScheme] verwenden, um zu ermitteln, ob Benutzer Ihr Produkt lieber in einem dunkleren oder helleren Farbschema anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="b7faf-107">On the web, you may use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect if users prefer to display your product in a darker or lighter colour scheme.</span></span>  <span data-ttu-id="b7faf-108">Verwenden [Microsoft Edge DevTools,][DevtoolsIndex] um eine Änderung vom Dunklen in den Hellmodus zu simulieren, ohne das gesamte Betriebssystem ändern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="b7faf-108">Use [Microsoft Edge DevTools][DevtoolsIndex] to simulate a change from dark to light mode without having to change the entire operating system.</span></span>  

1.  <span data-ttu-id="b7faf-109">Öffnen Sie das **Befehlsmenü**.</span><span class="sxs-lookup"><span data-stu-id="b7faf-109">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="b7faf-110">Wählen `Ctrl` + `Shift` + `P` Sie \(Windows/Linux\) oder `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="b7faf-110">Select `Ctrl`+`Shift`+`P` \(Windows/Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="b7faf-112">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="b7faf-112">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="b7faf-113">Geben Sie ein, wählen Sie entweder `emulate color` **CSS prefers-color-scheme** emulieren aus: dunkel oder **Emulieren von CSS prefers-color-scheme: light,** und wählen Sie dann `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="b7faf-113">Type `emulate color`, choose either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Farbschemaoption aus dem Befehlsmenü" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="b7faf-115">Farbschemaoption aus **dem Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="b7faf-115">Color scheme option from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="b7faf-116">Geben Sie einfach ein oder zeigt nicht das richtige Tool an, da es auch eine Möglichkeit gibt, ein Design für `dark` `light` [DevTools zu wählen.][DevtoolsCustomizeDarkTheme]</span><span class="sxs-lookup"><span data-stu-id="b7faf-116">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsCustomizeDarkTheme].</span></span>  <span data-ttu-id="b7faf-117">Wenn Sie sich fragen, was Sie wählen sollten, stellen Sie sicher, dass Sie ein **Renderingmenüelement** und kein **Darstellungsmenüelement** auswählen.</span><span class="sxs-lookup"><span data-stu-id="b7faf-117">If you are wondering what to choose, make sure that you are choosing a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="b7faf-118">Nachdem Sie ein Farbschema aktiviert haben, aktualisieren Sie das aktuelle Dokument, um den simulierten Modus anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="b7faf-118">After you choose a color scheme, refresh the current document to display the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Simulierter Lichtmodus innerhalb Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="b7faf-120">Simulierter Lichtmodus innerhalb Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b7faf-120">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="b7faf-121">Zeigen Sie Ihre CSS wie jede andere Webseite an, und ändern Sie sie.</span><span class="sxs-lookup"><span data-stu-id="b7faf-121">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="b7faf-122">Weitere Informationen finden Sie unter [Erste Schritte Mit Anzeigen und][DevtoolsCssIndex]Ändern von CSS .</span><span class="sxs-lookup"><span data-stu-id="b7faf-122">For more information, navigate to [Get Started With Viewing And Changing CSS][DevtoolsCssIndex].</span></span>  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Aktivieren des dunklen Designs in Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCssIndex]: ../css/index.md "Erste Schritte Mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
