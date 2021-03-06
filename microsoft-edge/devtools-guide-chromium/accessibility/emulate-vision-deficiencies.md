---
description: Emulieren von Sehschwächen in Microsoft Edge DevTools.
title: Emulieren von Sehschwächen in Microsoft Edge DevTools (Farbblindheit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: eec3c95bac93e600acf1887c8d31cea2173c6aee
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397874"
---
# <a name="emulate-vision-deficiencies"></a>Emulieren von Sehstörungen

Um die Anforderungen Ihrer Benutzer [][ColorblindawarenessMain] mit Farbsichtschwäche \(Farbblindheit\) besser zu erfüllen, können Sie mit [Microsoft Edge DevTools][DevtoolsIndex] bestimmte Farbsichtschwächen simulieren.  Das **Tool Zum Emulieren von Sehschwächen** simuliert die folgenden Kategorien.  

| Mangel an Farbsicht | Details |  
|:--- |:--- |  
| Verschwommenes Sehen | Der Benutzer hat Schwierigkeiten, sich auf feine Details zu konzentrieren. |  
| Protanopia | Der Benutzer kann kein rotes Licht wahrnehmen. |  
| Deuteranopia | Der Benutzer kann kein grünes Licht wahrnehmen. |  
| Tritanopie | Der Benutzer kann kein blaues Licht wahrnehmen. |  
| Achromatopsie | Der Benutzer kann keine Farbe wahrnehmen, wodurch alle Farben auf einen Grauton reduziert werden. |  

## <a name="navigate-to-the-rendering-tools"></a>Navigieren zu den Renderingtools  

Um einen Sehschwächenmangel zu simulieren, der für Ihr Webprodukt angewendet wird, öffnen Sie die [Renderingtools][DevtoolsRenderingToolsIndex].  

1.  Um die Renderingtools zu öffnen, wählen Sie das `...` Menüelement in der Symbolleiste aus.  
1.  Weitere **Tools auswählen**  
1.  Rendern **auswählen**  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Öffnen der Renderingtools" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Öffnen der **Renderingtools**  
    :::image-end:::  

Das **Menü Rendering** wird in der Schublade angezeigt.  

1.  Scrollen Sie nach unten `Emulate vision deficiencies` zum Menüelement, und wählen Sie das Dropdownmenü aus, um die Optionen anzuzeigen.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Das Menü Sehschwächen emulieren in der Renderschubschubleiste" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       Das **Menü Visionsmangel emulieren** in der **Renderschubleiste**  
    :::image-end:::  
    
1.  Wählen Sie eine Option aus.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Menüoptionen "Visionsmangel emulieren"" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Menüoptionen **zum Emulieren von Sehschwächen**  
    :::image-end:::  
    
1.  In den Hauptfenstern wird die Simulation der ausgewählten Option angezeigt, die auf die aktuelle Seite angewendet wurde.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Anzeigen mithilfe der Simulation **Blurred Vision**" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Anzeigen mithilfe einer **Simulation mit verschwommener** Vision  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Anzeigen mithilfe der **Achromatopsia**-Simulation" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Anzeigen mithilfe **der Achromatopsia-Simulation** :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <a name="use-the-command-menu"></a>Verwenden des Befehlsmenüs  

Sie können auch das **Befehlsmenü verwenden,** um auf die verschiedenen Simulationen zu zugreifen.  

1.  Wählen `Control` + `Shift` + `P` Sie \(Windows/Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü zu öffnen.**  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
1.  Geben `emulate` Sie ein, wählen Sie aus, was Sie simulieren möchten, und wählen Sie `Enter` aus.  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Die verschiedenen Simulationsoptionen, die im Befehlsmenü verfügbar sind" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Die verschiedenen Simulationsoptionen, die im **Befehlsmenü verfügbar sind**  
    :::image-end:::  
    
> [!IMPORTANT]
> Die **Tools zum Emulieren** von Sehschwächen simulieren Näherungen darüber, wie eine Person mit jedem Mangel Ihr Produkt sehen kann.  Jede Person ist unterschiedlich, daher variieren Sehschwächen im Schweregrad von Person zu Person.  Um die Anforderungen Ihrer Benutzer besser zu erfüllen, vermeiden Sie jede Farbkombination, die ein Problem sein kann.  Die **Emulate vision deficiencies tools** sind keine vollständige Barrierefreiheitsbewertung Ihres Produkts.  Stattdessen sollten Sie mit **den Tools zum** Emulieren von Sehschwächen einen guten ersten Schritt zur Vermeidung von Problemen finden.  

<!-- links -->  

[DevToolsIndex]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analysieren der Laufzeitleistung | Microsoft Docs"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "Die Organisation "Farbblindheit""  

[AmfcbMain]: https://www.amfcb.org "The American Foundation for the Color Blind (AFCB)"  
