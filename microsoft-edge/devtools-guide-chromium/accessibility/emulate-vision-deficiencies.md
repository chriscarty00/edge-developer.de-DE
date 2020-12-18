---
description: Emulieren von Sehstörungen in Microsoft Edge devtools
title: Emulieren von Sehstörungen in Microsoft Edge devtools (Farbenblindheit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 5343d32992880f8c60501a86db6cb3a92f417331
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230824"
---
# Emulieren von Sehstörungen

Um die Anforderungen Ihrer Benutzer mit [farbsehstörungen][ColorblindawarenessMain] zu erfüllen \ (Farbenblindheit \), können Sie mit [Microsoft Edge devtools][DevtoolsIndex] bestimmte farbsehstörungen simulieren.  Das Tool zum **emulieren von Sehstörungen** simuliert die folgenden Kategorien.  

| Farbsehstörungen | Details |  
|:--- |:--- |  
| Verschwommenes Sehvermögen | Der Benutzer hat Schwierigkeiten, sich auf feine Details zu konzentrieren. |   
| Protanopie | Der Benutzer kann keine rote Leuchte erkennen. |  
| Deuteranopie | Der Benutzer kann kein grünes Licht erkennen. |  
| Tritanopie | Der Benutzer kann keine blauen Lichter erkennen. |  
| Achromatopsie | Der Benutzer kann keine Farbe wahrnehmen, wodurch alle Farben auf eine Grauschattierung reduziert werden. |  

## Navigieren zu den Render-Tools  

Um einen Sehstörungen zu simulieren, der für Ihr Web-Produkt angewendet wird, öffnen Sie die [Rendering-Tools][DevtoolsRenderingToolsIndex].  

1.  So öffnen Sie die Rendering-Tools, indem Sie das `...` Menüelement in der Symbolleiste auswählen  
1.  Auswählen `More tools`  
1.  Auswählen `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Öffnen der Rendering-Tools" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Öffnen der **Rendering-Tools**  
    :::image-end:::  

Das **Rendering** -Menü wird im Einzug angezeigt.  

1.  Scrollen Sie nach unten zum `Emulate vision deficiencies` Menüelement, und wählen Sie das Dropdownmenü aus, um die Optionen anzuzeigen.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Das Menü "Sehstörungen emulieren" auf der Rendering-Schublade" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
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

1.  Wählen Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das **Befehlsmenü**zu öffnen.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
1.  Geben Sie ein `emulate` , was Sie simulieren und auswählen möchten `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Die verschiedenen Simulationsoptionen, die im Befehlsmenü zur Verfügung stehen" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Die verschiedenen Simulationsoptionen, die im **Befehlsmenü** zur Verfügung stehen  
    :::image-end:::  
    
> [!IMPORTANT]
> Die Tools zum **emulieren von Sehvermögen-Mängeln** simulieren Näherungswerte, wie eine Person mit jedem Mangel Ihr Produkt sehen kann.  Die einzelnen Personen sind unterschiedlich, daher variieren Sehstörungen in Schweregraden von Person zu Person.  Um die Anforderungen Ihrer Benutzer besser erfüllen zu können, sollten Sie keine Farbkombinationen verwenden, die möglicherweise ein Problem sind.  Die Tools zum **emulieren von Sehstörungen** sind keine vollständige Beurteilung der Barrierefreiheit Ihres Produkts.  Stattdessen sollten die Tools zum **emulieren von Sehstörungen** ein guter erster Schritt sein, um Probleme zu vermeiden.  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analysieren der Laufzeitleistung | Microsoft docs"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "Die Organisation der farbenblinden Sensibilisierung"  

[AmfcbMain]: https://www.amfcb.org "Die amerikanische Stiftung für das Farben Blind (AFCB)"  

