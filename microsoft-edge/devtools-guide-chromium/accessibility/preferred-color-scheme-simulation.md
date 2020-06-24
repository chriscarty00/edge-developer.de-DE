---
title: Erzwingen des Microsoft Edge-devtools in den Vorschaumodus für Farbschemas (CSS bevorzugt Farbschema)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: a83284b676ad388114a4a0ddb7ebdf2203ebcb90
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758082"
---
# <span data-ttu-id="89de5-103">Simulation eines dunklen oder hellen Farbschemas</span><span class="sxs-lookup"><span data-stu-id="89de5-103">Dark or Light Color Scheme simulation</span></span>  

<span data-ttu-id="89de5-104">Betriebssysteme weisen eine Möglichkeit auf, jede Anwendung in dunklerer oder heller Farbe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="89de5-104">Operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="89de5-105">Wenn Sie ein Webprodukt mit einem hellen Design in einem Betriebssystem im dunklen Modus haben, können Sie es mit einem Problem der Barrierefreiheit bei einigen Benutzern erreichen.</span><span class="sxs-lookup"><span data-stu-id="89de5-105">Having a web product that has a light theme in a dark mode operating system is grating and can be an accessibility issue for some users.</span></span>  <span data-ttu-id="89de5-106">Im Internet können Sie die CSS-medienabfrage " [bevorzugt-Farbschema][MDNPrefersColorScheme] " verwenden, um festzustellen, ob Benutzer Ihr Produkt lieber in einem dunkleren oder helleren Farbschema sehen möchten.</span><span class="sxs-lookup"><span data-stu-id="89de5-106">On the web, you may use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect if users prefer to see your product in a darker or lighter colour scheme.</span></span>  <span data-ttu-id="89de5-107">Verwenden Sie [Microsoft Edge devtools][DevtoolsGuideChromiumMain] , um eine Änderung vom dunkel-in hellen Modus zu simulieren, ohne das gesamte Betriebssystem ändern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="89de5-107">Use [Microsoft Edge DevTools][DevtoolsGuideChromiumMain] to simulate a change from dark to light mode without having to change the entire operating system.</span></span>  

1.  <span data-ttu-id="89de5-108">Öffnen des **Befehlsmenüs**</span><span class="sxs-lookup"><span data-stu-id="89de5-108">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="89de5-109">Drücken Sie `Control` + `Shift` + `P` Windows oder `Command` + `Shift` + `P` Mac OS.</span><span class="sxs-lookup"><span data-stu-id="89de5-109">Press `Control`+`Shift`+`P`  on Windows or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="89de5-111">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="89de5-111">The **Command Menu**</span></span>  
        :::image-end:::   
        
1.  <span data-ttu-id="89de5-112">Typ `emulate color` , wählen Sie entweder **emulieren von CSS bevorzugt-Farbschema: dunkel** oder **emulieren Sie CSS bevorzugt-Farbschema: Licht** , und drücken Sie dann `Enter` .</span><span class="sxs-lookup"><span data-stu-id="89de5-112">Type `emulate color`, select either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light**  and then press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Auswahl des Farbschemas im Befehlsmenü" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="89de5-114">Auswahl des Farbschemas im **Befehls** Menü</span><span class="sxs-lookup"><span data-stu-id="89de5-114">Color scheme selection from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="89de5-115">Sie können `dark` `light` das richtige Tool einfach eingeben oder nicht anzeigen, da es auch eine Möglichkeit zum [Auswählen eines Designs für devtools][DevtoolsGuideChromiumCustomizeDarkTheme]gibt.</span><span class="sxs-lookup"><span data-stu-id="89de5-115">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsGuideChromiumCustomizeDarkTheme].</span></span>  <span data-ttu-id="89de5-116">Wenn Sie sich Fragen, was Sie auswählen sollen, stellen Sie sicher, dass Sie ein Menüelement für die wieder **Gabe** auswählen, kein Menüelement " **Darstellung** ".</span><span class="sxs-lookup"><span data-stu-id="89de5-116">If you are wondering what to choose, make sure that you are selecting a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="89de5-117">Nachdem Sie ein Farbschema ausgewählt haben, laden Sie das aktuelle Dokument erneut, um den simulierten Modus anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="89de5-117">After you select a color scheme, reload the current document to see the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Simulierter Licht Modus in Microsoft Edge devtools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="89de5-119">Simulierter Licht Modus in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="89de5-119">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="89de5-120">Sie können Ihr CSS wie jede andere Webseite anzeigen und ändern.</span><span class="sxs-lookup"><span data-stu-id="89de5-120">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="89de5-121">Weitere Informationen finden Sie unter [Erste Schritte mit dem anzeigen und Ändern von CSS][DevtoolsGuideChromiumCssIndex].</span><span class="sxs-lookup"><span data-stu-id="89de5-121">For more information, see [Get Started With Viewing And Changing CSS][DevtoolsGuideChromiumCssIndex].</span></span>  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools Microsoft | Microsoft docs"  
[DevtoolsGuideChromiumCustomizeDarkTheme]: ../customize/dark-theme.md "Aktivieren des dunklen Designs in Microsoft Edge devtools | Microsoft docs"
[DevtoolsGuideChromiumCssIndex]: ../css/index.md "Erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "bevorzugt-Farbschema | MDN"  
