---
description: Um die Aktivierreihenfolge der Abschnitte einer Seite schnell anzuzeigen, verwenden Sie die Quellreihenfolgeanzeige im Barrierefreiheitstool rechts neben der Registerkarte "Formatvorlagen".
title: Testen Sie die Tastaturunterstützung mithilfe des Source Order Viewers
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 7e90221b581280a6eb63cee4d073622a80871903
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597411"
---
# <a name="test-keyboard-support-using-the-source-order-viewer"></a>Testen Sie die Tastaturunterstützung mithilfe des Source Order Viewers

Die Quellreihenfolge eines Dokuments ist für die Hilfstechnologie wichtig und kann sich von der Reihenfolge unterscheiden, in der Elemente auf der gerenderten Seite angezeigt werden.  MitHILFE von CSS können Sie Seitenelemente visuell neu anordnen, was jedoch nicht bedeutet, dass Hilfstechnologien wie Sprachausgabe Seitenelemente in der gleichen Reihenfolge darstellen würden.  

Um sicherzustellen, dass das Dokument eine logische Reihenfolge aufweist, können Sie die **Quellreihenfolgeanzeige** verwenden, um unterschiedliche Seitenelemente mit Zahlen zu beschriften, die die Reihenfolge im Quellcode des Dokuments angeben.  Die **Quellreihenfolgeanzeige** befindet sich auf der Registerkarte **"Barrierefreiheit"** (in der Nähe der Registerkarte **"Formatvorlagen").**


## <a name="analyzing-the-order-of-keyboard-access-through-sections-of-the-page"></a>Analysieren der Reihenfolge des Tastaturzugriffs über Abschnitte der Seite

Die [Demowebseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] weist eine gegenintuitive Aktivierreihenfolge auf, in der Tastaturbenutzer erst nach dem Tabulatoren über alle **Links "Mehr"** auf das Navigationsmenü in der Seitenleiste zugreifen.  Das Navigationsmenü in der Seitenleiste ist als Verknüpfung gedacht, um tief in den Seiteninhalt zu gelangen.  Da Sie jedoch die gesamte Seite durchlaufen müssen, bevor Sie das Navigationsmenü auf der Seitenleiste erreichen, ist dieses Navigationsmenü für Tastaturbenutzer wirkungslos.

Die `Tab` wichtigste Reihenfolge auf der Demoseite lautet:
1. Das **Suchfeld** und dann die Schaltfläche **"Los"** für das **Suchfeld.**
1. Die Schaltfläche **"Mehr"** im Abschnitt **"Katzen",** um zu einer "Katzen"-Webseite zu navigieren.  Dann die anderen Schaltflächen **"Mehr",** "Hunde", "Hunde", "Hunde", "Dogchen" und dann "Almacas".
1. Die blauen Links des Navigationsmenüs in der Seitenleiste: **Katzen,** **Hunde,** **Hunde, Hunde,** Hunde , **Hunde**und dann **Almacas**.
1. Das Textfeld für die Schenkung im Formular für die Gabe.
1. Die Schaltflächen in der oberen Navigationsleiste: **Home**, **Adopt a pet**, **Environs**, **Jobs**, and then **About Us**.
1. Die obere Fensteroberfläche des Browsers.

Der Grund für die verwirrende `Tab` Tastenreihenfolge ist, dass die Reihenfolge, in der eine Tastatur verwendet wird, durch die Quellreihenfolge des Dokuments bestimmt wird.  Die Reihenfolge, in der eine Tastatur verwendet wird, kann mithilfe des Attributs für Elemente geändert `tabindex` werden, das dieses Element aus der Quellreihenfolge herausnimmt.

Im Quellcode des Dokuments wird das Seitenleisten-Navigationsmenü hinter dem Hauptinhalt der Webseite angezeigt.  CSS wurde verwendet, um das Seitenleisten-Navigationsmenü über den meisten Hauptinhalten der Webseite zu positionieren. 

Sie können die Reihenfolge der Seitenelemente mithilfe der **Quellreihenfolgeanzeige** auf der **Barrierefreiheitsregisterkarte** testen.  Der **Source Order Viewer** ist ein experimentelles Feature. Für weitere Informationen navigieren Sie zur [Quellreihenfolgeanzeige.](../experimental-features/index.md#source-order-viewer)


So aktivieren Sie die Quellreihenfolgeanzeige:

1.  Wählen Sie in DevTools oben rechts die Schaltfläche **Einstellungen** \( ![ Einstellungen Schaltfläche ](../media/settings-button-icon.msft.png) \) aus.  

1.  Wählen Sie unter **Einstellungen** **Experimente**aus.  

1.  Aktivieren Sie das **Kontrollkästchen Quellreihenfolge-Viewer .**

1.  Wählen Sie in der oberen rechten Ecke der **Einstellungen** Seite **X** aus, um die Einstellungen Seite zu schließen.  Oben in DevTools hat sich die Meldung geändert, dass **mindestens eine Einstellung geändert wurde, die ein erneutes Laden erfordert, um wirksam zu werden.** wird angezeigt.  Wählen Sie die Schaltfläche **"DevTools neu laden" aus.**



So aktivieren und verwenden Sie den Source Order Viewer mit der Demoseite:

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte.  Wählen Sie dann **F12** aus, um DevTools zu öffnen.

1.  Wählen Sie im Tool **"Elemente"** rechts auf der Registerkarte **"Formatvorlagen"** die Registerkarte **"Barrierefreiheit"** aus.

1.  Aktivieren Sie im Abschnitt **"Source Order Viewer"** das Kontrollkästchen **"Quellreihenfolge anzeigen".**  Auf der gerenderten Webseite werden Zahlen angezeigt, die die Reihenfolge entsprechend der Steuerung `Tab` durch die Reihenfolge der Codezeilen in der Quelldatei angeben.

1.  Wählen Sie in der DOM-Struktur im **Elementtool** ein Hauptlayoutelement aus, `header` z. B. das Element.  Numerische Überlagerungen werden nun in Abschnitten der gerenderten Seite angezeigt, die die Quellreihenfolge der verschiedenen Elemente angeben. 

    :::image type="complex" source="../media/a11y-testing-source-order-viewer.msft.png" alt-text="Durch Aktivieren des Viewers für die Quellreihenfolge wird die Reihenfolge der Elemente in der Quelle als Überlagerungen auf der Seite angezeigt." lightbox="../media/a11y-testing-source-order-viewer.msft.png":::
        Durch Aktivieren des Viewers für die **Quellreihenfolge** wird die Reihenfolge der Elemente in der Quelle als Überlagerungen auf der Seite angezeigt.
    :::image-end:::
    
1.  Scrollen Sie auf der Seite, um alle numerischen Überlagerungen anzuzeigen, einschließlich des Seitenfußbereichs.


## <a name="see-also"></a>Weitere Informationen:

*  [Übersicht über Barrierefreiheitstests mit DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
