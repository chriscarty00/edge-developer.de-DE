---
title: Simulieren von reduzierter Bewegung mithilfe von Entwicklertools (CSS bevorzugt reduzierte Bewegung)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: f1bf90de4ac1832fff07e9ac963c26f92adeea2c
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843984"
---
# Reduzierte Bewegungs Simulation  

Animationen in Webprodukten sind möglicherweise ein Problem mit der Barrierefreiheit.  Betriebssysteme befassen sich mit dem Problem, indem Sie eine Option zum Deaktivieren von Animationen verwenden, um Benutzer Verwirrungen und mögliche gesundheitliche Probleme wie das Auslösen von Anfällen zu vermeiden.  Im Web können Sie die CSS-medienabfrage " [bevorzugt-reduzierte Bewegung][MDNPrefersReducedMotion] " verwenden, um festzustellen, ob Benutzer keine Animationen sehen möchten.  In Ihrem Produkt können Sie den Animations Code in einen Test einschließen, um zu vermeiden, dass Animationen für die betroffenen Benutzer angezeigt werden.  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

Mithilfe des [Microsoft Edge-devtools][DevtoolsGuideChromiumMain]können Sie diese reduzierte Bewegungs Einstellung simulieren, ohne Ihr Betriebssystem ändern zu müssen.  

1.  Öffnen des **Befehlsmenüs**  
    1.  Drücken Sie `Control` + `Shift` + `P` Windows oder `Command` + `Shift` + `P` Mac OS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Das **Befehlsmenü**  
        :::image-end:::   
        
1.  Geben `reduced` Sie an, um die Simulation ein-und auszuschalten.  Wählen Sie die Option aus, und drücken Sie `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Aktivieren oder Deaktivieren der Einstellung "reduzierte Bewegung bevorzugt" im Befehlsmenü" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Aktivieren oder Deaktivieren der Einstellung " **reduzierte Bewegung bevorzugt** " im **Befehlsmenü**  
    :::image-end:::  
    
1.  Aktualisieren Sie die aktuelle Seite, um zu testen, ob Ihre Animationen deaktiviert oder sichtbar sind.  
    
<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-rendering.msft.png "Abbildung 1: das Befehlsmenü"  
[ImageToggleReducedMotionFromCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png "Abbildung 2: Umschalten der reduzierten Bewegung von der befehlspalette"

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools Microsoft | Microsoft docs"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion "bevorzugt-reduzierte-Motion | MDN"  
