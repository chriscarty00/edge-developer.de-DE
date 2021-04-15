---
description: Wenn Sie die gleichen JavaScript-Ausdrücke wiederholt in die Konsole eingeben, versuchen Sie es stattdessen mit Live-Ausdrücken.
title: Beobachten von JavaScript-Ausdruckswerten in Echtzeit mit Live-Ausdrücken
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 51b7aa5119775f43861a84c1055ac9149a626d8a
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483135"
---
# <a name="monitor-changes-in-javascript-using-live-expressions"></a>Überwachen von Änderungen in JavaScript mithilfe von Liveausdrücken  

**Live-Ausdrücke** sind eine hervorragende Möglichkeit, um JavaScript-Ausdrücke zu überwachen, die sich sehr ändern.    Anstatt viele Konsolennachrichten zu lesen und zu navigieren, können Sie Ihre spezifischen JavaScript-Ausdrücke am oberen Rand der Konsole **anheften.**  

## <a name="add-a-new-live-expression"></a>Hinzufügen eines neuen Liveausdrucks  

Wählen Sie zu Beginn die Schaltfläche **Liveausdruck** erstellen \(Eye\) neben dem **Textfeld Filter** aus.  Nachdem Sie ihn auswählen, wird ein Textfeld angezeigt, in das Sie Ihren neuen Ausdruck eingeben können.  

:::image type="complex" source="../media/console-live-expressions-new.msft.png" alt-text="Wählen Sie die Schaltfläche Neuer Liveausdruck aus, um ein Textfeld zum Eingeben eines Ausdrucks zu öffnen." lightbox="../media/console-live-expressions-new.msft.png":::
    Klicken Sie `New live expression` auf die Schaltfläche, um ein Textfeld zum Eingeben eines Ausdrucks zu öffnen.  
:::image-end:::  

**Live-Ausdrücke** können ein beliebiger gültiger JavaScript-Ausdruck sein.  Führen Sie die folgenden Aktionen aus, um dies zu versuchen.  

1.  Öffnen Sie das **Textfeld Live Expression.**  
1.  Geben Sie `document.activeElement` ein.  
1.  Führen Sie zum Speichern des Ausdrucks eine der folgenden Aktionen aus.  
    *   Wählen `Control` + `Enter` Sie \(Windows, Linux\) oder `Command` + `Enter` \(macOS\) aus.  
    *   Wählen Sie außerhalb des **Textfelds Live Expression** aus.  
        
Der Ausdruck ist jetzt live und wird `body` als Ergebnis angezeigt.  

:::image type="complex" source="../media/console-live-expressions-document-active-element.msft.png" alt-text="Liveausdruck für document.activeElement zeigt text als Ergebnis an" lightbox="../media/console-live-expressions-document-active-element.msft.png":::
    Liveausdruck für `document.activeElement` den Anzeigetext als Ergebnis  
:::image-end:::  

Wenn Sie auf der Webseite navigieren, ändert sich der Wert.  In der folgenden Abbildung öffnen Sie beispielsweise das Suchmenü auf der Webseite, und der Ausdruck wird nun `button.nav-bar-button.focus-visible` als Wert angezeigt.  

:::image type="complex" source="../media/console-live-expressions-document-active-element-nav-button.msft.png" alt-text="Um den Wert des Liveausdrucks zu ändern, interagieren Sie mit verschiedenen Elementen auf der Webseite" lightbox="../media/console-live-expressions-document-active-element-nav-button.msft.png":::
    Um den Wert des Liveausdrucks **zu ändern,** interagieren Sie mit verschiedenen Elementen auf der Webseite  
:::image-end:::  

Um den Wert erneut zu ändern, öffnen Sie das Textfeld Suchen auf der Webseite.  

:::image type="complex" source="../media/console-live-expressions-document-active-element-search.msft.png" alt-text="Navigieren Sie zu einem anderen Element auf der Webseite, um den Liveausdruck zu aktualisieren." lightbox="../media/console-live-expressions-document-active-element-search.msft.png":::
    Navigieren Sie zu einem anderen Element auf der Webseite, um den **Liveausdruck zu aktualisieren.**  
:::image-end:::  

## <a name="remove-live-expressions"></a>Entfernen von Liveausdrücken  

Ein **Live-Ausdruck** ist verfügbar, solange Sie ihn aktiv halten.  Wählen Sie den nächsten Ausdruck aus, um einen **Liveausdruck** `x` zu loswerden.  

:::image type="complex" source="../media/console-live-expressions-remove.msft.png" alt-text="Um Liveausdrücke zu entfernen, wählen Sie das x daneben aus." lightbox="../media/console-live-expressions-remove.msft.png":::
    Wählen Sie zum Entfernen von **Liveausdrücken** `x` den nächsten aus.  
:::image-end:::  

## <a name="replace-console-logging-with-live-expressions"></a>Ersetzen der Konsolenprotokollierung durch Liveausdrücke  

Sie können so viele Ausdrücke erstellen, wie Sie möchten, und die einzelnen Ausdrücke in Browsersitzungen und Fenstern beibehalten.  **Live-Ausdrücke** sind eine Möglichkeit, das Rauschen in Ihrem Debugworkflow zu reduzieren.  

Beispielsweise möchten Sie die Mausbewegung auf der aktuellen Webseite überwachen.  Navigieren Sie [zu Protokollierungs-Mausbewegungsdemo,][GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml]öffnen Sie die **Konsole,** und bewegen Sie die Maus, um die Protokolle mit vielen Informationen angezeigt zu werden.  

:::image type="complex" source="../media/console-live-expression-mouse-logging.msft.png" alt-text="Konsole zeigt viele Informationen zur Mausposition an" lightbox="../media/console-live-expression-mouse-logging.msft.png":::
    **Konsole** zeigt viele Informationen zur Mausposition an  
:::image-end:::  

Die große Menge an Informationen verlangsamt nicht nur den Debugprozess, sondern macht es auch einfach, die Änderungen zu verpassen, die Sie überprüfen möchten.  Wenn die **Konsole** weitere Nachrichten anzeigt und Sie die Maus bewegen, werden die Werte, die Sie überprüfen möchten, vom Bildschirm gescrollt.  

Führen Sie die folgenden Aktionen aus, um **Liveausdrücke** als Alternative zu testen.  

1.  Navigieren Sie zur [Mausbewegung, ohne demo protokollieren zu müssen.][GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml]  
1.  Erstellen **von Liveausdrücken** für `x` und `y` .  
    
Wenn Sie **Liveausdrücke verwenden,** erhalten Sie immer die Informationen **** auf demselben Bildschirmteil und behalten Konsolenprotokolle für Werte bei, die sich nicht so stark ändern.

:::image type="complex" source="../media/console-live-expressions-x-and-y.msft.png" alt-text="Anzeigen der x- und y-Position der Maus als Liveausdrücke" lightbox="../media/console-live-expressions-x-and-y.msft.png":::
    Anzeigen der `x` Position und der Maus als `y` **Liveausdrücke**  
:::image-end:::  

**Liveausdrücke** werden ausschließlich auf Ihrem Computer ausgeführt, und Sie müssen nichts in Ihrem Code ändern, um ihn anzeigen zu können.  **Live-Ausdrücke** sind eine hervorragende Möglichkeit, um sicherzustellen, dass Sie nur die Informationen anzeigen, die Sie debuggen möchten.  Darüber hinaus **helfen Ihnen Live-Ausdrücke,** das Rauschen auf den Computern Ihrer Benutzer zu begrenzen.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove.html "Beispiele für Konsolenmeldungen: Verwenden von | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove-no-log.html "Mausbewegung ohne Protokollierung | GitHub"  
