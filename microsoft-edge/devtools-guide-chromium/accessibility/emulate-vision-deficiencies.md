---
title: Emulieren von Sehstörungen in Microsoft Edge devtools (Farbenblindheit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 0b608f5fe67724eee81aeb993577ee9b45cbca09
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758083"
---
# Emulieren von Sehstörungen

Weltweit haben etwa 8% der Männer und 0,5% der Frauen einen [farbsehstörungen-Mangel][ColorblindawarenessMain] , der gemeinhin als "Farbenblindheit" bezeichnet wird.  [Microsoft Edge devtools][MicrosoftEdgeDevTools] ermöglicht es Ihnen, verschiedene bekannte Mängel zu emulieren und eine Vorschau Ihres Produkts zur Verfügung zu stellen, die Sie überprüfen können.  

| Farb Mangel | Details |  
|:--- |:--- |  
| Verschwommenes Sehvermögen |  |   
| Protanopie | Die Unfähigkeit, jedes rote Licht wahrzunehmen. |  
| Deuteranopie | Die Unfähigkeit, grünes Licht wahrzunehmen. |  
| Tritanopie | Die Unfähigkeit, ein blaues Licht wahrzunehmen. |  
| Achromatopsie | Die Unfähigkeit, eine beliebige Farbe wahrzunehmen, mit Ausnahme von Grautönen. |  

## Navigieren zu den Render-Tools  

Wenn Sie Ihr Aktuelles Web-Produkt nach Farbmängeln testen möchten, öffnen Sie die [Rendering-Tools][RenderingTools].  

1.  Öffnen der Rendering-Tools durch Auswählen des `...` Menüelements in der Symbolleiste  
1.  Auswählen `More tools`  
1.  Auswählen `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Öffnen der Rendering-Tools" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Öffnen der **Rendering-Tools**  
    :::image-end:::  

Das **Rendering** -Menü wird in der unteren Hälfte des devtools angezeigt.  

1.  Scrollen Sie nach unten zum `Emulate Vision deficiencies` Menüelement, und wählen Sie eine der Optionen aus.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Das Menü "Sehstörungen emulieren" der Rendering-Tools" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       Das Menü " **Sehstörungen emulieren** " der **Rendering** -Tools  
    :::image-end:::  
    
1.  Wählen Sie eine der Optionen aus.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Menü Optionen für das Emulieren von Sehstörungen" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Menü Optionen für das **emulieren von Sehstörungen**  
    :::image-end:::  
    
1.  Die aktuelle Seite wird in einer Simulation angezeigt, wie Sie für einen Benutzer mit dem ausgewählten Mangel aussehen kann.  

    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Dokumentation zu Microsoft Edge-Entwickler Tools in verschwommener Vision-Emulation" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Wird mithilfe einer **verschwommenen Bild** Emulation angezeigt  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Dokumentation zu Microsoft Edge-Entwickler Tools in Achromatopsie-Vision-Emulation" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Anzeige mithilfe der **Achromatopsie-Vision** -Emulation :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## Verwenden des Befehlsmenüs  

Sie können die verschiedenen Emulationen auch erreichen, ohne die verschiedenen Menüs über das **Befehlsmenü**zu durchlaufen.  

1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
1.  Geben Sie ein `emulate` , was Sie simulieren möchten, und drücken Sie `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Die verschiedenen im Befehlsmenü verfügbaren Emulationsoptionen" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Die verschiedenen im **Befehlsmenü** verfügbaren Emulationsoptionen  
    :::image-end:::  
    
> [!IMPORTANT]
> Die Emulations Tools sind näherungsweise, wie eine Person mit jedem Mangel Ihr Produkt sehen kann.  Die einzelnen Personen sind unterschiedlich, daher variieren Sehstörungen in Schweregraden von Person zu Person.  Um die Anforderungen Ihrer Benutzer besser erfüllen zu können, sollten Sie keine Farbkombinationen verwenden, die möglicherweise ein Problem sind.  Bei den Emulations Tools handelt es sich nicht um eine vollständige Bewertung der Barrierefreiheit Ihres Produkts, doch sollten Sie einen guten ersten Schritt zur Vermeidung der größten Mängel haben.  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "Die Organisation der farbenblinden Sensibilisierung"  
[AmfcbMain]: https://www.amfcb.org "Die amerikanische Stiftung für das Farben Blind (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Microsoft Edge (Chrom)-Rendering-Tools"  
