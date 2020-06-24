---
title: Erzwingen des Microsoft Edge-devtools in den Vorschaumodus für Farbschemas (CSS bevorzugt Farbschema)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 94c5369f0eb35059933be7f6202a4f64450629cd
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758078"
---
# <span data-ttu-id="59cd4-103">Reduzierte Bewegungs Simulation</span><span class="sxs-lookup"><span data-stu-id="59cd4-103">Reduced Motion Simulation</span></span>  

<span data-ttu-id="59cd4-104">Animationen in Webprodukten sind möglicherweise ein Problem mit der Barrierefreiheit.</span><span class="sxs-lookup"><span data-stu-id="59cd4-104">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="59cd4-105">Betriebssysteme befassen sich mit dem Problem, indem Sie eine Option zum Deaktivieren von Animationen verwenden, um Benutzer Verwirrungen und mögliche gesundheitliche Probleme wie das Auslösen von Anfällen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="59cd4-105">Operating Systems deal with the problem by including an option to turn off animations to avoid user confusion and potential health related problems such as triggering seizures.</span></span>  <span data-ttu-id="59cd4-106">Im Web können Sie die CSS-medienabfrage " [bevorzugt-reduzierte Bewegung][MDNPrefersReducedMotion] " verwenden, um festzustellen, ob Benutzer keine Animationen sehen möchten.</span><span class="sxs-lookup"><span data-stu-id="59cd4-106">On the web, you may use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS Media Query to detect if users prefer to not see any animations.</span></span>  <span data-ttu-id="59cd4-107">In Ihrem Produkt können Sie den Animations Code in einen Test einschließen, um zu vermeiden, dass Animationen für die betroffenen Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="59cd4-107">In your product, you may wrap your animation code in a test to avoid animations showing up for the affected users.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
  animation: none;
  }
}
```  

<span data-ttu-id="59cd4-108">Mithilfe des [Microsoft Edge-devtools][DevtoolsGuideChromiumMain]können Sie diese reduzierte Bewegungs Einstellung simulieren, ohne Ihr Betriebssystem ändern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="59cd4-108">Using the [Microsoft Edge DevTools][DevtoolsGuideChromiumMain], you may simulate this reduced motion setting without having to change your operating system.</span></span>  

1.  <span data-ttu-id="59cd4-109">Öffnen des **Befehlsmenüs**</span><span class="sxs-lookup"><span data-stu-id="59cd4-109">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="59cd4-110">Drücken Sie `Control` + `Shift` + `P` Windows oder `Command` + `Shift` + `P` Mac OS.</span><span class="sxs-lookup"><span data-stu-id="59cd4-110">Press `Control`+`Shift`+`P`  on Windows or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="59cd4-112">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="59cd4-112">The **Command Menu**</span></span>  
        :::image-end:::   
        
1.  <span data-ttu-id="59cd4-113">Geben `reduced` Sie an, um die Simulation ein-und auszuschalten.</span><span class="sxs-lookup"><span data-stu-id="59cd4-113">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="59cd4-114">Wählen Sie die Option aus, und drücken Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="59cd4-114">Select the option and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Aktivieren oder Deaktivieren der Einstellung "reduzierte Bewegung bevorzugt" im Befehlsmenü" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="59cd4-116">Aktivieren oder Deaktivieren der Einstellung " **reduzierte Bewegung bevorzugt** " im **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="59cd4-116">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="59cd4-117">Aktualisieren Sie die aktuelle Seite, um zu testen, ob Ihre Animationen deaktiviert oder sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="59cd4-117">Refresh the current page to test whether your animations are turned off or visible.</span></span>  
    
<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-rendering.msft.png "Abbildung 1: das Befehlsmenü"  
[ImageToggleReducedMotionFromCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png "Abbildung 2: Umschalten der reduzierten Bewegung von der befehlspalette"

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools Microsoft | Microsoft docs"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion "bevorzugt-reduzierte-Motion | MDN"  