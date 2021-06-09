---
description: Überprüfen Sie, ob Webseiten mit deaktivierter BENUTZERoberflächenanimation (reduzierte Bewegung) mithilfe des Css-Medienfeatures "Emulieren" der Dropdownliste "Bevorzugt reduzierte Bewegung" im Renderingtool verwendet werden können.
title: Stellen Sie sicher, dass die Seite mit deaktivierter UI-Animation verwendet werden kann
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: ec30925b706b4b1c6dfaaa6ce66a38fab8759ac2
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597414"
---
# <a name="verify-that-the-page-is-usable-with-ui-animation-turned-off"></a>Stellen Sie sicher, dass die Seite mit deaktivierter UI-Animation verwendet werden kann

Eine Webseite sollte einem Benutzer, der Animationen im Betriebssystem deaktiviert hat, keine Animationen anzeigen.  Animationen können zur Benutzerfreundlichkeit eines Produkts beitragen, können aber auch Ablenkungen, Verwirrung oder Verwirrung verursachen.

Um zu überprüfen, ob eine Webseite mit deaktivierter BENUTZERoberflächenanimation (reduzierte Bewegung) verwendet werden kann, verwenden Sie im **Renderingtool** die Dropdownliste zum **Emulieren von CSS-Medienfeatures mit vorzuziehenden Bewegungen.**

Wenn Sie auf der Demowebseite für Barrierefreiheitstests Animationen im Betriebssystem deaktivieren oder diese Einstellungen mit DevTools emulieren, verwendet die Webseite keinen reibungslosen Bildlauf, wenn Sie die Links des Navigationsmenüs auf der Seitenleiste auswählen.  Dies wird erreicht, indem die Einstellung für den gleichmäßigen Bildlauf in CSS in einer Medienabfrage umgebrochen und dann das **Renderingtool** zum Emulieren der Betriebssystemeinstellung für reduzierte Animationen verwendet wird.

So überprüfen Sie, ob die Seite mit deaktivierten Animationen verwendet werden kann:

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.

1.  Wählen Sie oben in DevTools das **Tool "Quellen"** aus, und wählen Sie dann im **Navigationsbereich** auf der linken Seite die Option `styles.css` aus.  Die CSS-Datei wird im **Editorbereich** angezeigt.

1.  Wählen Sie **STRG+F** unter Windows/Linux oder **Befehl+F** unter macOS aus, und geben Sie dann `@media` ein.  Die folgende CSS-Medienabfrage wird angezeigt, die bestätigt, dass sie auf der Webseite verwendet wird.

    ```css
    @media (prefers-reduced-motion: no-preference) {
      html {
        scroll-behavior: smooth;
      }
    }
    ```

    Emulieren Sie als Nächstes die Einstellung des Betriebssystems, um die Animation wie folgt zu reduzieren.

1.  Wählen Sie **Esc** aus, um die Schublade am unteren Rand von DevTools zu öffnen.  Wählen Sie oben in der Schublade die Schaltfläche **Weitere Tools** ( **+** ) aus, um die Liste der Tools anzuzeigen, und wählen Sie dann **Rendering**aus.  

1.  Wählen Sie in der Dropdownliste **"Emulate CSS media feature prefers-reduced-motion"** die Option **"prefers-reduced-motion: reduced"** aus.

    :::image type="complex" source="../media/a11y-testing-simulating-reduced-motion.msft.png" alt-text="Simulieren von reduzierter Bewegung und css, die sicherstellen, dass ein gleichmäßiger Bildlauf nur erfolgt, wenn der Benutzer dies möchte" lightbox="../media/a11y-testing-simulating-reduced-motion.msft.png":::
        Simulieren von reduzierter Bewegung und css, die sicherstellen, dass ein gleichmäßiger Bildlauf nur erfolgt, wenn der Benutzer dies möchte
    :::image-end:::

1.  Wählen Sie auf der Webseite die blauen Menüelemente aus, **z. B. "Käufe"** oder **"Doppelklicken".**  Jetzt führt die Webseite sofort einen Bildlauf zum ausgewählten Abschnitt durch, anstatt die Animation für den gleichmäßigen Bildlauf zu verwenden.

1.  Wählen Sie im **Renderingtool** unter dem **Emulieren der CSS-Medienfunktion "Prefers-reduced-motion"** die Option **"Keine Emulation"** aus, um diese Einstellung zu entfernen.
   
Beachten Sie, dass die Demowebseite auch mit den oben genannten Medienabfrage- und Emulationseinstellungen weiterhin die folgenden Animationen ausführt. Stellen Sie beim Erstellen Ihres Webprodukts sicher, dass Sie alle ähnlichen Animationen beheben.  
*  Animation der blauen Menüelemente, wenn Sie mit dem Mauszeiger darauf zeigen.
*  Animation der Kreise auf den **Links "Mehr",** wenn Sie mit dem Mauszeiger darauf zeigen.



## <a name="see-also"></a>Weitere Informationen:

*  [Simulation reduzierter Bewegungen](reduced-motion-simulation.md)
*  [Übersicht über Barrierefreiheitstests mit DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
