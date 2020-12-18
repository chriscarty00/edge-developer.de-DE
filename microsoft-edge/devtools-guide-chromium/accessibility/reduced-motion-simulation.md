---
description: Simulieren von reduzierter Bewegung mithilfe von Entwicklertools
title: Simulieren von reduzierter Bewegung mithilfe von Entwicklertools (CSS bevorzugt reduzierte Bewegung)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 0e5243e01ca6c9344dceffb0bf004dadccc3d4d7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230789"
---
# <span data-ttu-id="c258d-104">Reduzierte Bewegungs Simulation</span><span class="sxs-lookup"><span data-stu-id="c258d-104">Reduced Motion Simulation</span></span>  

<span data-ttu-id="c258d-105">Animationen in Webprodukten sind möglicherweise ein Problem mit der Barrierefreiheit.</span><span class="sxs-lookup"><span data-stu-id="c258d-105">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="c258d-106">Betriebssysteme befassen sich mit dem Problem, indem Sie eine Option zum Deaktivieren von Animationen verwenden, um Benutzer Verwirrungen und mögliche gesundheitliche Probleme wie das Auslösen von Anfällen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="c258d-106">Operating Systems deal with the problem by including an option to turn off animations to avoid user confusion and potential health related problems such as triggering seizures.</span></span>  <span data-ttu-id="c258d-107">Im Web können Sie die CSS-medienabfrage " [bevorzugt-reduzierte Bewegung][MDNPrefersReducedMotion] " verwenden, um festzustellen, ob Benutzer keine Animationen sehen möchten.</span><span class="sxs-lookup"><span data-stu-id="c258d-107">On the web, you may use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS Media Query to detect if users prefer to not see any animations.</span></span>  <span data-ttu-id="c258d-108">In Ihrem Produkt können Sie den Animations Code in einen Test einschließen, um zu vermeiden, dass Animationen für die betroffenen Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c258d-108">In your product, you may wrap your animation code in a test to avoid animations showing up for the affected users.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="c258d-109">Mithilfe des [Microsoft Edge-devtools][DevtoolsIndex]können Sie diese reduzierte Bewegungs Einstellung simulieren, ohne Ihr Betriebssystem ändern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="c258d-109">Using the [Microsoft Edge DevTools][DevtoolsIndex], you may simulate this reduced motion setting without having to change your operating system.</span></span>  

1.  <span data-ttu-id="c258d-110">Öffnen des **Befehlsmenüs**</span><span class="sxs-lookup"><span data-stu-id="c258d-110">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="c258d-111">Wählen Sie `Control` + `Shift` + `P` unter Windows/Linux oder `Command` + `Shift` + `P` unter macOS aus.</span><span class="sxs-lookup"><span data-stu-id="c258d-111">Select `Control`+`Shift`+`P` on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="c258d-113">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="c258d-113">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="c258d-114">Geben `reduced` Sie an, um die Simulation ein-und auszuschalten.</span><span class="sxs-lookup"><span data-stu-id="c258d-114">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="c258d-115">Wählen Sie die Option aus, und wählen Sie aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c258d-115">Choose the option and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Aktivieren oder Deaktivieren der Einstellung "reduzierte Bewegung bevorzugt" im Befehlsmenü" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="c258d-117">Aktivieren oder Deaktivieren der Einstellung " **reduzierte Bewegung bevorzugt** " im **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="c258d-117">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c258d-118">Aktualisieren Sie die aktuelle Seite, um zu testen, ob Ihre Animationen deaktiviert oder sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="c258d-118">Refresh the current page to test whether your animations are turned off or visible.</span></span>  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "bevorzugt-reduzierte-Motion | MDN"  
