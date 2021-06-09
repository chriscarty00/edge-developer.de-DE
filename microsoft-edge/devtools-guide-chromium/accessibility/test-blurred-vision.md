---
description: Um zu überprüfen, ob eine Webseite mit verschwommener Sicht verwendet werden kann, verwenden Sie im Renderingtool die Dropdownliste "Sehschwächen emulieren".
title: Überprüfen Sie, ob die Seite mit verschwommener Sicht verwendet werden kann
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 2fc1a1cf7746591573fce07946c7fb11abf42705
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597450"
---
# <a name="verify-that-the-page-is-usable-with-blurred-vision"></a>Überprüfen Sie, ob die Seite mit verschwommener Sicht verwendet werden kann

<!-- Rendering tool: Emulate vision deficiencies: Blurred vision -->

Um verschwommenes Sehen zu simulieren, verwenden Sie im **Renderingtool** das Menü **"Sehschwächen emulieren".**  Wenn Sie dieses Feature mit der Demowebseite verwenden, können Sie sehen, dass der Schlagschatten des Texts im oberen Menü das Lesen der Menüelemente erschwert.

So überprüfen Sie, ob eine Webseite mit verschwommener Vision verwendet werden kann:

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.

1.  Wählen Sie **Esc** aus, um die Schublade am unteren Rand von DevTools zu öffnen.  Wählen Sie das **+** Symbol oben in der Schublade aus, um die Liste der Tools anzuzeigen, und wählen Sie dann **Rendern**aus.  

1.  Wählen Sie in der Dropdownliste **"Sehschwächen emulieren"** die Option **"Verschwommene Vision"** aus.

    :::image type="complex" source="../media/a11y-testing-simulating-blur.msft.png" alt-text="Simulieren einer verschwommenen Seite" lightbox="../media/a11y-testing-simulating-blur.msft.png":::
        Simulieren einer verschwommenen Seite
    :::image-end:::

    Beachten Sie, dass `text-shadow` die CSS-Eigenschaft den Text der Menüelemente im oberen Menü nur schwer lesen kann. Überprüfen Sie z. B. **"Home",** **"Adopt a Pet"** und andere Menüelemente.
    
1.  Wählen Sie im **Renderingtool** unter **"Sehschwäche emulieren"** die Option **"Keine Emulation"** aus, um die unscharfe Sehsimulation zu entfernen.


## <a name="see-also"></a>Weitere Informationen:

*  [Emulieren von Sehstörungen](emulate-vision-deficiencies.md)
*  [Übersicht über Barrierefreiheitstests mit DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
