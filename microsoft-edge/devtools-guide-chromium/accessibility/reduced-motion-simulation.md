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

Mithilfe des [Microsoft Edge-devtools][DevtoolsIndex]können Sie diese reduzierte Bewegungs Einstellung simulieren, ohne Ihr Betriebssystem ändern zu müssen.  

1.  Öffnen des **Befehlsmenüs**  
    1.  Wählen Sie `Control` + `Shift` + `P` unter Windows/Linux oder `Command` + `Shift` + `P` unter macOS aus.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Das **Befehlsmenü**  
        :::image-end:::  
        
1.  Geben `reduced` Sie an, um die Simulation ein-und auszuschalten.  Wählen Sie die Option aus, und wählen Sie aus `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Aktivieren oder Deaktivieren der Einstellung "reduzierte Bewegung bevorzugt" im Befehlsmenü" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Aktivieren oder Deaktivieren der Einstellung " **reduzierte Bewegung bevorzugt** " im **Befehlsmenü**  
    :::image-end:::  
    
1.  Aktualisieren Sie die aktuelle Seite, um zu testen, ob Ihre Animationen deaktiviert oder sichtbar sind.  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "bevorzugt-reduzierte-Motion | MDN"  
