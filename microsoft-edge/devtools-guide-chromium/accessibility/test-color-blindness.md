---
description: Überprüfen Sie, ob Webseiten von Personen mit Farbenblindheit verwendet werden können, indem Sie die Dropdownliste "Sehschwächen emulieren" im Renderingtool verwenden.
title: Stellen Sie sicher, dass die Seite von Personen mit Farbblindheit verwendet werden kann
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 54cd7230f0402bfeb4b5ee28d2bcd0947794676f
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597448"
---
# <a name="verify-that-the-page-is-usable-by-people-with-color-blindness"></a>Stellen Sie sicher, dass die Seite von Personen mit Farbblindheit verwendet werden kann

<!-- Rendering tool: Emulate vision deficiencies: Protanopia -->

Um zu überprüfen, ob eine Webseite von Personen mit Farbenblindheit verwendet werden kann, verwenden Sie im **Renderingtool** die Dropdownliste **"Sehschwächen emulieren".**

Auf der Demo-Webseite für Barrierefreiheitstests verwenden die verschiedenen Schenkungszustände Farbe als einzige Möglichkeit zur Differenzierung.
*  Grün bedeutet, dass eine große Menge von Schenkungen empfangen wurde.
*  Gelb bedeutet, dass eine mittlere Menge von Schenkungen empfangen wurde.
*  Rot bedeutet, dass eine geringe Menge von Käufen empfangen wurde.

Sie können jedoch nicht erwarten, dass alle Ihre Benutzer diese Farben wie gewünscht sehen.  Indem Sie das Feature **"Sehschwächen emulieren"** des **Rendering-Tools** verwenden, können Sie feststellen, dass dieses Design nicht gut genug ist, indem Sie simulieren, wie Personen mit einer anderen Vision Ihr Design wahrnehmen würden.


So überprüfen Sie, ob eine Webseite von Personen mit Farbenblindheit verwendet werden kann:

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.

1.  Wählen Sie **Esc** aus, um die Schublade am unteren Rand von DevTools zu öffnen.  Wählen Sie das **+** Symbol oben in der Schublade aus, um die Liste der Tools anzuzeigen, und wählen Sie dann **Rendern**aus.  

1.  Wählen Sie in der Dropdownliste **"Sehschwächen emulieren"** die Option **"Protanopia"** aus.  _Protanopia_ ist eine reduzierte Empfindlichkeit gegenüber rotem Licht, wodurch es schwierig ist, Grün, Rot und Gelb zu unterscheiden.

    :::image type="complex" source="../media/a11y-testing-simulating-protanopia.msft.png" alt-text="Anzeigen des Dokuments als jemand mit Protanopie würde es sehen" lightbox="../media/a11y-testing-simulating-protanopia.msft.png":::
        Anzeigen des Dokuments als jemand mit Protanopie würde es sehen
    :::image-end:::
    
1.  Wählen Sie im **Renderingtool** unterhalb **von Emulieren von Sehschwächen** **"Keine Emulation"** aus, um die Simulation zu entfernen.


## <a name="see-also"></a>Weitere Informationen:

*  [Emulieren von Sehschwächen][DevToolsVisionDeficiencies] – Definiert die Elemente in der Dropdownliste **"Sehschwächen emulieren",** einschließlich Protanopia, Deuteranopia, Tritanopia und Aopsia.
*  [Übersicht über Barrierefreiheitstests mit DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsVisionDeficiencies]: ./emulate-vision-deficiencies.md "Emulieren von Sehschwächen | Microsoft-Dokumente"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
