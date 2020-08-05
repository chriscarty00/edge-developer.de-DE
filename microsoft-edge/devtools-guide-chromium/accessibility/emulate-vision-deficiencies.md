---
title: Emulieren von Sehstörungen in Microsoft Edge devtools (Farbenblindheit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: b70499fa189d162fa7589966bab183f4c12f68f7
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843921"
---
# Emulieren von Sehstörungen

Um die Anforderungen Ihrer Benutzer mit [farbsehstörungen][ColorblindawarenessMain] zu erfüllen \ (Farbenblindheit \), können Sie mit [Microsoft Edge devtools][MicrosoftEdgeDevTools] bestimmte farbsehstörungen simulieren.  Das Tool zum **emulieren von Sehstörungen** simuliert die folgenden Kategorien.  

| Farbsehstörungen | Details |  
|:--- |:--- |  
| Verschwommenes Sehvermögen | Der Benutzer hat Schwierigkeiten, sich auf feine Details zu konzentrieren. |   
| Protanopie | Der Benutzer kann keine rote Leuchte erkennen. |  
| Deuteranopie | Der Benutzer kann kein grünes Licht erkennen. |  
| Tritanopie | Der Benutzer kann keine blauen Lichter erkennen. |  
| Achromatopsie | Der Benutzer kann keine Farbe wahrnehmen, wodurch alle Farben auf eine Grauschattierung reduziert werden. |  

## Navigieren zu den Render-Tools  

Um einen Sehstörungen zu simulieren, der für Ihr Web-Produkt angewendet wird, öffnen Sie die [Rendering-Tools][RenderingTools].  

1.  Öffnen der Rendering-Tools durch Auswählen des `...` Menüelements in der Symbolleiste  
1.  Auswählen `More tools`  
1.  Auswählen `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Öffnen der Rendering-Tools" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Öffnen der **Rendering-Tools**  
    :::image-end:::  

Das **Rendering** -Menü wird im Einzug angezeigt.  

1.  Scrollen Sie nach unten zum `Emulate vision deficiencies` Menüelement, und wählen Sie das Dropdownmenü aus, um die Optionen anzuzeigen.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Das Menü Sehstörungen emulieren auf der Rendering-Schublade" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       Das Menü " **Sehstörungen emulieren** " auf der **Rendering** -Schublade  
    :::image-end:::  
    
1.  Wählen Sie eine Option aus.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Menü Optionen für das Emulieren von Sehstörungen" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Menü Optionen für das **emulieren von Sehstörungen**  
    :::image-end:::  
    
1.  Das Hauptfenster zeigt die Simulation der ausgewählten Option an, die auf die aktuelle Seite angewendet wurde.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Anzeige mit * * verschwommener Sehkraft * *-Simulation" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Anzeige mithilfe einer **verschwommenen Bild** Simulation  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Anzeige mit * * Achromatopsie * *-Simulation" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Anzeigen mithilfe der **Achromatopsie** -Simulation :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## Verwenden des Befehlsmenüs  

Sie können auch das **Befehlsmenü** verwenden, um auf die verschiedenen Simulationen zuzugreifen.  

1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
1.  Geben Sie ein `emulate` , was Sie simulieren möchten, und drücken Sie `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Die verschiedenen Simulationsoptionen, die im Befehlsmenü zur Verfügung stehen" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Die verschiedenen Simulationsoptionen, die im **Befehlsmenü** zur Verfügung stehen  
    :::image-end:::  
    
> [!IMPORTANT]
> Die Tools zum **emulieren von Sehvermögen-Mängeln** simulieren Näherungswerte, wie eine Person mit jedem Mangel Ihr Produkt sehen kann.  Die einzelnen Personen sind unterschiedlich, daher variieren Sehstörungen in Schweregraden von Person zu Person.  Um die Anforderungen Ihrer Benutzer besser erfüllen zu können, sollten Sie keine Farbkombinationen verwenden, die möglicherweise ein Problem sind.  Die Tools zum **emulieren von Sehstörungen** sind keine vollständige Beurteilung der Barrierefreiheit Ihres Produkts.  Stattdessen sollten die Tools zum **emulieren von Sehstörungen** ein guter erster Schritt sein, um Probleme zu vermeiden.  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "Die Organisation der farbenblinden Sensibilisierung"  
[AmfcbMain]: https://www.amfcb.org "Die amerikanische Stiftung für das Farben Blind (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Microsoft Edge (Chrom)-Rendering-Tools"  
