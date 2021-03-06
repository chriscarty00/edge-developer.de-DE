---
description: Erzwingen Sie Microsoft Edge DevTools in den Farbschemavorschaumodus.
title: Erzwingen von Microsoft Edge DevTools in den Farbschemavorschaumodus (CSS bevorzugt Farbschema)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 84f482605acd6edab6829e00d5fa31f927ebc032
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398301"
---
# <a name="dark-or-light-color-scheme-simulation"></a>Simulation des dunklen oder hellen Farbschemas  

Betriebssysteme können jede Anwendung in dunkleren oder helleren Farben anzeigen.  Ein Webprodukt mit einem hellen Design in einem Betriebssystem im dunklen Modus ist Gitter und kann für einige Benutzer ein Problem mit der Barrierefreiheit sein.  Im Web können Sie die CSS-Medienabfrage mit dem [Bevorzugt-Farbschema][MDNPrefersColorScheme] verwenden, um zu ermitteln, ob Benutzer Ihr Produkt lieber in einem dunkleren oder helleren Farbschema anzeigen möchten.  Verwenden [Sie Microsoft Edge DevTools,][DevtoolsIndex] um eine Änderung vom Dunklen in den Hellmodus zu simulieren, ohne das gesamte Betriebssystem ändern zu müssen.  

1.  Öffnen Sie das **Befehlsmenü**.  
    1.  Wählen `Control` + `Shift` + `P` Sie \(Windows/Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Das **Befehlsmenü**  
        :::image-end:::  
        
1.  Geben Sie ein, wählen Sie entweder `emulate color` **CSS prefers-color-scheme** emulieren aus: dunkel oder **Emulieren von CSS prefers-color-scheme: light,** und wählen Sie dann `Enter` aus.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Farbschemaoption aus dem Befehlsmenü" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       Farbschemaoption aus **dem Befehlsmenü**  
    :::image-end:::  
    
    > [!IMPORTANT]
    > Geben Sie einfach ein oder zeigt nicht das richtige Tool an, da es auch eine Möglichkeit gibt, ein Design für `dark` `light` [DevTools zu wählen.][DevtoolsCustomizeDarkTheme]  Wenn Sie sich fragen, was Sie wählen sollten, stellen Sie sicher, dass Sie ein **Renderingmenüelement** und kein **Darstellungsmenüelement** auswählen.  

1.  Nachdem Sie ein Farbschema aktiviert haben, aktualisieren Sie das aktuelle Dokument, um den simulierten Modus anzeigen zu können.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Simulierter Lichtmodus in Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       Simulierter Lichtmodus in Microsoft Edge DevTools  
    :::image-end:::  
    
    Zeigen Sie Ihre CSS wie jede andere Webseite an, und ändern Sie sie.  Weitere Informationen finden Sie unter [Erste Schritte mit dem Anzeigen und Ändern von CSS][DevtoolsCssIndex].  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Aktivieren des dunklen Designs in Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCssIndex]: ../css/index.md "Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft Docs"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
