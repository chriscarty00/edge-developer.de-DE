---
title: Erzwingen des Microsoft Edge-devtools in den Vorschaumodus für Farbschemas (CSS bevorzugt Farbschema)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: a83284b676ad388114a4a0ddb7ebdf2203ebcb90
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758082"
---
# Simulation eines dunklen oder hellen Farbschemas  

Betriebssysteme weisen eine Möglichkeit auf, jede Anwendung in dunklerer oder heller Farbe anzuzeigen.  Wenn Sie ein Webprodukt mit einem hellen Design in einem Betriebssystem im dunklen Modus haben, können Sie es mit einem Problem der Barrierefreiheit bei einigen Benutzern erreichen.  Im Internet können Sie die CSS-medienabfrage " [bevorzugt-Farbschema][MDNPrefersColorScheme] " verwenden, um festzustellen, ob Benutzer Ihr Produkt lieber in einem dunkleren oder helleren Farbschema sehen möchten.  Verwenden Sie [Microsoft Edge devtools][DevtoolsGuideChromiumMain] , um eine Änderung vom dunkel-in hellen Modus zu simulieren, ohne das gesamte Betriebssystem ändern zu müssen.  

1.  Öffnen des **Befehlsmenüs**  
    1.  Drücken Sie `Control` + `Shift` + `P` Windows oder `Command` + `Shift` + `P` Mac OS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Das **Befehlsmenü**  
        :::image-end:::   
        
1.  Typ `emulate color` , wählen Sie entweder **emulieren von CSS bevorzugt-Farbschema: dunkel** oder **emulieren Sie CSS bevorzugt-Farbschema: Licht**  , und drücken Sie dann `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       Auswahl des Farbschemas im **Befehls** Menü  
    :::image-end:::  
    
    > [!IMPORTANT]
    > Sie können `dark` `light` das richtige Tool einfach eingeben oder nicht anzeigen, da es auch eine Möglichkeit zum [Auswählen eines Designs für devtools][DevtoolsGuideChromiumCustomizeDarkTheme]gibt.  Wenn Sie sich Fragen, was Sie auswählen sollen, stellen Sie sicher, dass Sie ein Menüelement für die wieder **Gabe** auswählen, kein Menüelement " **Darstellung** ".  

1.  Nachdem Sie ein Farbschema ausgewählt haben, laden Sie das aktuelle Dokument erneut, um den simulierten Modus anzuzeigen.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       Simulierter Licht Modus in Microsoft Edge devtools  
    :::image-end:::  
    
    Sie können Ihr CSS wie jede andere Webseite anzeigen und ändern.  Weitere Informationen finden Sie unter [Erste Schritte mit dem anzeigen und Ändern von CSS][DevtoolsGuideChromiumCssIndex].  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools Microsoft | Microsoft docs"  
[DevtoolsGuideChromiumCustomizeDarkTheme]: ../customize/dark-theme.md "Aktivieren des dunklen Designs in Microsoft Edge devtools | Microsoft docs"
[DevtoolsGuideChromiumCssIndex]: ../css/index.md "Erste Schritte mit dem anzeigen und Ändern von CSS | Microsoft docs"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "bevorzugt-Farbschema | MDN"  
