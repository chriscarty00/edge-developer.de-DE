---
description: Erzwingen Microsoft Edge DevTools in den Vorschaumodus für Farbschemas.
title: Erzwingen Microsoft Edge DevTools in den Vorschaumodus für Farbschemas (CSS bevorzugt Farbschema)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: dc2911ce7a7fcbeef7763099541822b5cd6cf053
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597068"
---
# <a name="dark-or-light-color-scheme-simulation"></a>Simulation von dunklen oder hellen Farbschemas  

Viele Betriebssysteme haben eine Möglichkeit, jede Anwendung in dunkleren oder helleren Farben anzuzeigen.  Ein Webprodukt, das ein helles Design in einem Betriebssystem im dunklen Modus aufweist, ist riebend und kann für einige Benutzer ein Problem mit der Barrierefreiheit sein.  

Für eine Webseite können Sie die [CSS-Medienabfrage "prefers-color-scheme"][MDNPrefersColorScheme] verwenden, um zu ermitteln, ob der Benutzer ihr Produkt lieber in einem dunkleren oder helleren Farbschema anzeigen möchte.  Verwenden Sie dann zum Testen des Ergebnisses [Microsoft Edge DevTools,][DevtoolsIndex] um einen Wechsel vom dunklen in den hellen Modus zu simulieren, ohne die Einstellung für das gesamte Betriebssystem ändern zu müssen.  

**So emulieren Sie dunkles oder helles Design:**

1.  Öffnen Sie das **Befehlsmenü**.  
    1.  Wählen Sie `Ctrl` + `Shift` + `P` \(Windows/Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Das **Befehlsmenü**  
        :::image-end:::  
        
1.  Geben `emulate color` Sie ein, wählen Sie entweder **Emulate CSS prefers-color-scheme: dark** oder **Emulate CSS prefers-color-scheme: light** and then select `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Farbschemaoption im Befehlsmenü" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       Farbschemaoption im **Befehlsmenü**  
    :::image-end:::  
    
    > [!IMPORTANT]
    > Einfach eingeben `dark` oder zeigt nicht das richtige Tool `light` an, da es auch eine Möglichkeit gibt, [ein Design für DevTools auszuwählen.][DevtoolsCustomizeDarkTheme]  Wenn Sie sich fragen, was Sie auswählen sollten, stellen Sie sicher, dass Sie ein **Renderingmenüelement** und kein **Darstellungsmenüelement** auswählen.  

1.  Nachdem Sie ein Farbschema ausgewählt haben, aktualisieren Sie das aktuelle Dokument, um den simulierten Modus anzuzeigen.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Simulierter Lichtmodus innerhalb Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       Simulierter Lichtmodus innerhalb Microsoft Edge DevTools  
    :::image-end:::  
    
    Zeigen Sie Ihre CSS wie jede andere Webseite an, und ändern Sie sie.  Weitere Informationen finden Sie unter ["Erste Schritte mit dem Anzeigen und Ändern von CSS".][DevtoolsCssIndex]  


## <a name="see-also"></a>Weitere Informationen:

* [Überprüfen Sie auf Kontrastprobleme mit dunklem Design und hellem Design](test-dark-mode.md)


<!-- links -->  
[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Aktivieren des dunklen Designs in Microsoft Edge DevTools-| Microsoft-Dokumente"
[DevtoolsCssIndex]: ../css/index.md "Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft-Dokumente"  
<!-- external links -->
[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | Mdn"  
