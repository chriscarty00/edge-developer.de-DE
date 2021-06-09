---
description: Überprüfen Sie die Tastaturunterstützung mithilfe der Tabulator- und Eingabetasten.
title: Überprüfen Sie die Tastaturunterstützung mithilfe der Tab- und Eingabetasten
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 48151e16a9059b5ebaadca36f29447d4ad3be8c7
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597410"
---
# <a name="check-for-keyboard-support-by-using-the-tab-and-enter-keys"></a>Überprüfen Sie die Tastaturunterstützung mithilfe der Tab- und Eingabetasten


Nicht alle Benutzer verfügen über ein Zeiger- oder Touchgerät, und nicht alle Benutzer können die von uns erstellten Webprojekte sehen.  Aus diesem Grund ist es wichtig, dass die Benutzeroberfläche mindestens mit einer Tastatur funktioniert.  Stellen Sie sicher, dass Sie den Schlüssel verwenden `Tab` können, um den Fokus auf jedes Formularsteuerelement auf einer Webseite zu verschieben, und stellen Sie sicher, dass Sie den Schlüssel zum Senden von Formularen verwenden `Enter` können.

Sie können die Benutzerfreundlichkeit einer Webseite für Tastaturbenutzer auf verschiedene Arten testen:
*  Mithilfe der Tastatur, insbesondere der `Tab` Tasten , `Shift` + `Tab` und `Enter` tasten.  Dieser Ansatz wird in diesem Artikel beschrieben.
*  Überprüfen Sie die Tastaturunterstützung für **** ein einzelnes Element mithilfe des Inspect-Tools.  Die Informationsüberlagerung des Tools "Inspect" enthält einen Abschnitt **"Barrierefreiheit",** der eine zeile mit **Tastaturfokus** enthält.  
*  Überprüfen Sie den Abschnitt **"Barrierefreiheit"** des Berichts **"Probleme"** auf Probleme mit der Tastaturunterstützung.

Führen Sie die folgenden Schritte aus, um die Demoseite auf Barrierefreiheitsprobleme zu überprüfen, indem Sie eine Tastatur anstelle einer Maus verwenden:

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers.

1.  Verwenden Sie eine Tastatur, um durch das Demodokument zu navigieren, und verwenden Sie die `Tab` `Shift` + `Tab` Tasten, um von Element zu Element zu springen.  Auf der Demowebseite `Tab` verschiebt der Schlüssel zuerst den Fokus auf das Suchformular im `header` Abschnitt.

1.  Wählen Sie `Tab` aus, um den Fokus auf eine Schaltfläche zu setzen, und klicken Sie dann `Enter` auf die fokussierte Schaltfläche.  Wählen Sie beispielsweise auf der Demoseite aus, `Tab` um den Fokus auf das **Suchfeld** zu setzen, und wählen Sie dann aus, `Enter` um die Suche zu übermitteln.  Dieser Ansatz führt zu demselben Ergebnis wie das Auswählen der Schaltfläche **"Los".**  Die Auswahl `Enter` zum Senden des **Suchformulars** funktioniert ordnungsgemäß.

1.  Wählen Sie `Tab` erneut aus.  Das nächste Element, auf das Sie den Fokus legen, ist der erste **Link "Mehr"** im `content` Abschnitt der Webseite, wie durch eine Gliederung angegeben.
    
    :::image type="complex" source="../media/a11y-testing-keyboard-focus-on-element.msft.png" alt-text="Navigieren im Dokument mithilfe der Tastatur und der Tabulatortaste. Der Fokus wird auf einem Link im Dokument angezeigt." lightbox="../media/a11y-testing-keyboard-focus-on-element.msft.png":::
        Navigieren im Dokument mithilfe der Tastatur und der Tabulatortaste. Der Fokus wird auf einem Link im Dokument angezeigt.
    :::image-end:::
    
1.  Wählen Sie `Tab` mehrere weitere Male aus, bis Sie den letzten Link **"Mehr"** übergeben haben.  Die Seite scrollt nach oben, und Sie scheinen sich auf einem Element der Seite zu befinden, aber es gibt keine Möglichkeit, zu erkennen, um welches Element es sich handelt.

1.  Beachten Sie die URL unten links.  Wenn Sie links unten auf dem Bildschirm suchen (oder eine Sprachausgabe verwenden), erkennen Sie, dass Sie sich im Navigationsmenü der Seitenleiste mit blauen Links befinden, da der Browser die URL anzeigt, auf die der **Katzenlink** zeigt ( `#cats` ).

    :::image type="complex" source="../media/a11y-testing-lack-of-focus-style.msft.png" alt-text="Eine fehlende Fokusformatvorlage macht es unmöglich, zu wissen, wo Sie sich derzeit im Dokument befinden. Der einzige Hinweis ist die Anzeige des Linkziels in der unteren linken Ecke des Bildschirms." lightbox="../media/a11y-testing-lack-of-focus-style.msft.png":::
        Eine fehlende Fokusformatvorlage macht es unmöglich, zu wissen, wo Sie sich derzeit im Dokument befinden. Der einzige Hinweis ist die Anzeige des Linkziels in der unteren linken Ecke des Bildschirms.
    :::image-end:::

1.  Wählen Sie `Tab` erneut aus, um zum Eingabefeld im Schenkungsformular zu gelangen.  Sie können jedoch die Schaltflächen über dem Textfeld nicht erreichen, indem Sie `Tab` . Sie können die Tastatur nicht verwenden, um den Fokus auf die **Schaltflächen 50,** **100**oder **200** zu setzen und sie dann auszuwählen.  Außerdem wird bei Auswahl `Enter` des Formulars kein Schenkungsformular übermittelt.

    :::image type="complex" source="../media/a11y-testing-form-field-with-outline.msft.png" alt-text="Das einzige element, auf das über die Tastatur zugegriffen werden kann, ist das Texteingabefeld im Gabeformular." lightbox="../media/a11y-testing-form-field-with-outline.msft.png":::
        Das einzige element, auf das über die Tastatur zugegriffen werden kann, ist das Texteingabefeld im Gabeformular.
    :::image-end:::
    
1.  Wenn Sie `Tab` erneut auswählen, wird der Fokus auf der oberen Navigationsleiste der Seite mit Menüschaltflächen für **Home**, **Adopt a Pet**, Adoption , **Adoption**, **Jobs**und **About Us**platziert.  Aktivieren oder setzen Sie `Tab` `Shift` + `Tab` den Fokus auf eine Menüschaltfläche, wie durch eine Fokusgliederung angegeben.  Wählen Sie dann `Enter` aus, um auf diesen Abschnitt der Webseite zuzugreifen.

    :::image type="complex" source="../media/a11y-testing-menu-with-outline.msft.png" alt-text="Das Hauptmenü weist eine Hervorhebung und eine Fokusgliederung auf und ist daher über die Tastatur zugänglich." lightbox="../media/a11y-testing-menu-with-outline.msft.png":::
        Das Hauptmenü weist eine Hervorhebung und eine Fokusgliederung auf und ist daher über die Tastatur zugänglich.
    :::image-end:::
    
Basierend auf der obigen exemplarischen Vorgehensweise haben wir die folgenden Probleme gefunden, die behoben werden müssen.

*  Bei Verwendung einer Tastatur zeigen die blauen Links des Navigationsmenüs auf der Seitenleiste nicht visuell an, welcher Link den Fokus hat.  Navigieren Sie für weitere Informationen zu ["Analysieren der fehlenden Anzeige des Tastaturfokus in einem Randleistenmenü".](test-analyze-no-focus-indicator.md)

*  Im Formular für die Schenkung funktionieren die Schaltflächen für den Betrag und die Schaltfläche Betrag nicht mit einer Tastatur. ****  Navigieren Sie zu ["Analysieren der fehlenden Tastaturunterstützung in einem Formular",](test-analyze-no-keyboard-support.md)um weitere Informationen zu erfahren.

*  Die Reihenfolge des Tastaturzugriffs über Abschnitte der Seite ist nicht korrekt.  Sie navigieren durch alle **"Mehr"-Links** im Dokument, bevor Sie das Navigationsmenü auf der Seitenleiste erreichen.  Zu dem Zeitpunkt, zu dem die `Tab` Taste den Fokus auf das Navigationsmenü auf der Seitenleiste legt, haben Sie bereits den gesamten Seiteninhalt durchlaufen. Das Navigationsmenü auf der Seitenleiste sollte einfachen Zugriff auf den Seiteninhalt bieten.  For more information on how to solve this issue, navigate to [Test keyboard support using the Source Order Viewer](test-tab-key-source-order-viewer.md).


## <a name="see-also"></a>Weitere Informationen:

*  [Übersicht über Barrierefreiheitstests mit DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
