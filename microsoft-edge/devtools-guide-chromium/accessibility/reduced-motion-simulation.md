---
description: Simulieren sie reduzierte Bewegung mithilfe von Entwicklertools.
title: Simulieren von reduzierter Bewegung mithilfe von Entwicklertools (CSS bevorzugt reduzierte Bewegung)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 29cdbd7492665e819315910b3f743d444470cc12
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397867"
---
# <a name="reduced-motion-simulation"></a><span data-ttu-id="8c115-104">Reduzierte Bewegungssimulation</span><span class="sxs-lookup"><span data-stu-id="8c115-104">Reduced motion simulation</span></span>  

<span data-ttu-id="8c115-105">Animation in Webprodukten kann ein Problem mit der Barrierefreiheit sein.</span><span class="sxs-lookup"><span data-stu-id="8c115-105">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="8c115-106">Betriebssysteme lösen das Problem, indem sie eine Option zum Deaktivieren von Animationen enthalten, um Benutzerverwechslungen und potenzielle Gesundheitsprobleme wie das Auslösen von Anfällen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="8c115-106">Operating Systems deal with the problem by including an option to turn off animations to avoid user confusion and potential health related problems such as triggering seizures.</span></span>  <span data-ttu-id="8c115-107">Im Web können Sie die CSS-Medienabfrage [prefers-reduced-motion][MDNPrefersReducedMotion] verwenden, um zu erkennen, ob Benutzer keine Animationen ausführen oder anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="8c115-107">On the web, you may use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS Media Query to detect if users prefer to not run or display any animations.</span></span>  <span data-ttu-id="8c115-108">In Ihrem Produkt können Sie Ihren Animationscode in einen Test umschließen, um zu vermeiden, dass Animationen für die betroffenen Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8c115-108">In your product, you may wrap your animation code in a test to avoid animations showing up for the affected users.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="8c115-109">Mithilfe der [Microsoft Edge DevTools][DevtoolsIndex]können Sie diese Einstellung für reduzierte Bewegungen simulieren, ohne Ihr Betriebssystem ändern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="8c115-109">Using the [Microsoft Edge DevTools][DevtoolsIndex], you may simulate this reduced motion setting without having to change your operating system.</span></span>  

1.  <span data-ttu-id="8c115-110">Öffnen Sie das **Befehlsmenü**.</span><span class="sxs-lookup"><span data-stu-id="8c115-110">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="8c115-111">Wählen `Control` + `Shift` + `P` Sie unter Windows/Linux oder `Command` + `Shift` + `P` unter macOS aus.</span><span class="sxs-lookup"><span data-stu-id="8c115-111">Select `Control`+`Shift`+`P` on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="8c115-113">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="8c115-113">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="8c115-114">Geben `reduced` Sie ein, um die Simulation ein- und auszuschalten.</span><span class="sxs-lookup"><span data-stu-id="8c115-114">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="8c115-115">Wählen Sie die Option aus, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="8c115-115">Choose the option and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Aktivieren oder Deaktivieren der Einstellung für reduzierte Bewegungen im Befehlsmenü" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="8c115-117">Aktivieren oder Deaktivieren der **Einstellung für reduzierte Bewegungen** im **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="8c115-117">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8c115-118">Aktualisieren Sie die aktuelle Seite, um zu testen, ob Ihre Animationen deaktiviert oder sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="8c115-118">Refresh the current page to test whether your animations are turned off or visible.</span></span>  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "bevorzugt eine reduzierte Bewegungserkennung | MDN"  
