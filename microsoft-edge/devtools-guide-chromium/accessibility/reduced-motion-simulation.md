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
# <a name="reduced-motion-simulation"></a>Reduzierte Bewegungssimulation  

Animation in Webprodukten kann ein Problem mit der Barrierefreiheit sein.  Betriebssysteme lösen das Problem, indem sie eine Option zum Deaktivieren von Animationen enthalten, um Benutzerverwechslungen und potenzielle Gesundheitsprobleme wie das Auslösen von Anfällen zu vermeiden.  Im Web können Sie die CSS-Medienabfrage [prefers-reduced-motion][MDNPrefersReducedMotion] verwenden, um zu erkennen, ob Benutzer keine Animationen ausführen oder anzeigen möchten.  In Ihrem Produkt können Sie Ihren Animationscode in einen Test umschließen, um zu vermeiden, dass Animationen für die betroffenen Benutzer angezeigt werden.  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

Mithilfe der [Microsoft Edge DevTools][DevtoolsIndex]können Sie diese Einstellung für reduzierte Bewegungen simulieren, ohne Ihr Betriebssystem ändern zu müssen.  

1.  Öffnen Sie das **Befehlsmenü**.  
    1.  Wählen `Control` + `Shift` + `P` Sie unter Windows/Linux oder `Command` + `Shift` + `P` unter macOS aus.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Das **Befehlsmenü**  
        :::image-end:::  
        
1.  Geben `reduced` Sie ein, um die Simulation ein- und auszuschalten.  Wählen Sie die Option aus, und wählen Sie `Enter` aus.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Aktivieren oder Deaktivieren der Einstellung für reduzierte Bewegungen im Befehlsmenü" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Aktivieren oder Deaktivieren der **Einstellung für reduzierte Bewegungen** im **Befehlsmenü**  
    :::image-end:::  
    
1.  Aktualisieren Sie die aktuelle Seite, um zu testen, ob Ihre Animationen deaktiviert oder sichtbar sind.  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "bevorzugt eine reduzierte Bewegungserkennung | MDN"  
