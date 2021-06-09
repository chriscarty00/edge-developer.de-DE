---
description: Analyse der fehlenden Anzeige des Tastaturfokus in einem Randleistenmenü aufgrund einer fehlenden CSS-Pseudoklassenregel für den Fokusstatus eines Links in Kombination mit dem Link ohne Gliederungseinstellung.
title: Analysieren Sie die fehlenden Anzeige des Tastaturfokus in einem Randleistenmenü
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 3626de9bdc2cce266efafe4b1b2e8fff501a74f7
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597461"
---
# <a name="analyze-the-lack-of-indication-of-keyboard-focus-in-a-sidebar-menu"></a>Analysieren Sie die fehlenden Anzeige des Tastaturfokus in einem Randleistenmenü

<!-- Inspect tool, and CSS rules: pseudo-classes for states -->

Auf der Demoseite für Barrierefreiheitstests zeigt das Seitenleisten-Navigationsmenü mit blauen Links nicht visuell an, welcher Link den Fokus hat, wenn eine Tastatur verwendet wird.  Um herauszufinden, warum das Seitenleistenmenü für Tastaturbenutzer verwirrend ist, suchen wir nach CSS-Pseudoklassenregeln für die `hover` `focus` Und-Zustände sowie nach der CSS-Eigenschaft für Linkgliederungen.  

Bei dieser Analyse wird festgestellt, dass die fehlende Anzeige des Tastaturfokus in den Links des Navigationsmenüs auf der Seitenleiste auf Folgendes zurückzuführen ist:
*  Die `a` Links haben eine CSS-Eigenschaftseinstellung von `outline: none` .
*  Den `a` Verknüpfungen fehlt eine CSS-Pseudoklassenregel für den `:focus` Zustand.

Um zum CSS zu navigieren, verwenden wir das Tool **Inspect,** um einen blauen Link im Navigationsmenü auf der Seitenleiste hervorzuheben, und zeigen dann die DOM-Struktur und CSS für das Element an, das `a` diese Verknüpfung definiert.

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.

1.  Wählen Sie die Schaltfläche **Inspect** \( ![ Inspect icon ](../media/inspect-icon.msft.png) \) in der oberen linken Ecke von DevTools aus, sodass die Schaltfläche hervorgehoben ist (blau).

1.  Zeigen Sie im Navigationsmenü der Seitenleiste auf den blauen **Katzenlink.**  Die Inspect-Überlagerung wird angezeigt und zeigt an, dass das `a` Element tastaturfokussierbar ist.  Die Überlagerung zeigt jedoch nicht an, dass es keine visuellen Hinweise gibt, wenn der Link den Fokus hat.

    Als Nächstes überprüfen wir das CSS-Format dieses Links.
 
1.  Wählen Sie im Navigationsmenü der Seitenleiste den Link **"Katzen"** aus.  Das Tool **Inspect** wird deaktiviert, und **das** Elementtool wird geöffnet, wobei der Knoten in der `a` DOM-Struktur hervorgehoben wird.

1.  Wählen Sie die Registerkarte **"Formatvorlagen" aus.**  Die CSS-Regel `#sidebar nav li a` wird zusammen mit einem Link zu einer Zeilennummer in `styles.css` angezeigt.

    :::image type="complex" source="../media/a11y-testing-menu-link.msft.png" alt-text="Überprüfen des Quellcodes und der angewendeten Formatvorlagen eines Links im Menü" lightbox="../media/a11y-testing-menu-link.msft.png":::
        Überprüfen des Quellcodes und der angewendeten Formatvorlagen eines Links im Menü
    :::image-end:::
    
1.  Wählen Sie den Link zur CSS-Datei aus.  Die CSS-Datei wird im **Tool "Quellen"** geöffnet.

    :::image type="complex" source="../media/a11y-testing-menu-link-styles.msft.png" alt-text="Die Formatvorlagen, die auf den Link im Quellentool angewendet werden" lightbox="../media/a11y-testing-menu-link-styles.msft.png":::
        Die Formatvorlagen, die auf den Link im Quellentool angewendet werden
    :::image-end:::
    
Die Formatvorlagen der Seite weisen eine CSS-Pseudoklassenregel für den Zustand auf, die `hover` angibt, welches Menüelement Sie verwenden, wenn Sie eine Maus verwenden: `#sidebar nav li a:hover` .  Es gibt jedoch keine CSS-Pseudoklassenregel für den `focus` Zustand, um visuell anzugeben, welches Menüelement Sie verwenden, wenn Sie eine Tastatur verwenden, z. `#sidebar nav li a:focus` B. .

Beachten Sie außerdem, dass die Links eine CSS-Eigenschaftseinstellung von `outline: none` haben.  Dies ist eine gängige Vorgehensweise, um die Gliederung zu entfernen, die Browser elementen automatisch hinzufügen, wenn Sie sich über eine Tastatur darauf konzentrieren.  Wenn Sie `focus` keine Formatierung verwenden, ist dies für Ihre Benutzer verwirrend.


## <a name="see-also"></a>Weitere Informationen: 

*  [Nachverfolgen, welches Element den Fokus hat](focus.md)
*  [Übersicht über Barrierefreiheitstests mit DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
