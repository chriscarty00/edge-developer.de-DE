---
description: Erfahren Sie, wie Sie Microsoft Edge DevTools verwenden, um Möglichkeiten zu finden, wie Sie Ihre Websites schneller laden können.
title: Optimieren der Websitegeschwindigkeit mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 75c9df5d86ce994cebfda882a0adfa2664b6ec30
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439444"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.  
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="optimize-website-speed-with-microsoft-edge-devtools"></a>Optimieren der Websitegeschwindigkeit mit Microsoft Edge DevTools  

## <a name="goal-of-tutorial"></a>Ziel des Lernprogramms  

In diesem Lernprogramm erfahren Sie, wie Sie Microsoft Edge DevTools verwenden, um Möglichkeiten zu finden, wie Sie Ihre Websites schneller laden können.  

## <a name="prerequisites"></a>Voraussetzungen  

*   Sie sollten über grundlegende Webentwicklungserfahrungen verfügen, ähnlich wie in dieser Einführung in [die Webentwicklungsklasse][CourseraIntroductionWebDevelopmentClass].  
*   Sie müssen nichts über die Ladeleistung wissen.  In diesem Lernprogramm erfahren Sie mehr darüber.  

## <a name="introduction"></a>Einführung  

Dies ist Tony.  Tony ist in der Katzengesellschaft sehr bekannt.  Er hat eine Website erstellt, damit seine Fans mehr über seine Lieblingsprodukte erfahren können.  Seine Fans lieben die Website, aber Tony hört immer wieder Beschwerden, dass die Website langsam geladen wird.  Tony hat Sie gebeten, ihm bei der Beschleunigung der Website zu helfen.  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony, die Katze" lightbox="../media/speed-tony.msft.png":::
   Tony, die Katze  
:::image-end:::  

## <a name="step-1-audit-the-site"></a>Schritt 1: Überwachen der Website  

Beginnen Sie immer mit einer Überwachung, wenn Sie die Lastleistung eines Standorts **verbessern möchten.**  
Die Überwachung hat zwei wichtige Funktionen:  

*   Es wird eine **Basislinie erstellt,** mit der Sie nachfolgende Änderungen messen können.  
*   Sie erhalten praktische **Tipps dazu,** welche Änderungen die größten Auswirkungen haben.  
    
### <a name="set-up"></a>Einrichtung  

Zunächst müssen Sie die Website so einrichten, dass Sie später Änderungen daran vornehmen können.  

1.  [Öffnen Sie den Quellcode für die Website](https://glitch.com/edit/#!/tony).  Diese Registerkarte wird als **Editorregisterkarte bezeichnet.**  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Die Registerkarte Editor" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       Die **Registerkarte Editor**  
    :::image-end:::  
    
1.  Wählen Sie **tony**aus.  Es wird ein Menü angezeigt.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Das Menü, das nach der Auswahl von tony angezeigt wird" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       Das Menü, das nach der Auswahl von **tony angezeigt wird**  
    :::image-end:::  
    
1.  Wählen Sie **#A0 aus.**  Der Name des Projekts wird von **tony** in einen zufällig generierten Namen geändert.  Sie verfügen nun über eine eigene bearbeitbare Kopie des Codes.  Später können Sie Änderungen an diesem Code vornehmen.  
1.  Wählen **Sie Anzeigen** aus, und wählen Sie In einem neuen Fenster **aus.**  Die Demo wird auf einer neuen Registerkarte geöffnet.  Diese Registerkarte wird als Demoregisterkarte **bezeichnet.**  Es kann eine Weile dauern, bis die Website geladen ist.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Die Registerkarte Demo" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       Die Registerkarte Demo  
    :::image-end:::  
    
1.  Wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.  Microsoft Edge DevTools wird neben der Demo geöffnet.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools und die Demo" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       DevTools und die Demo  
    :::image-end:::  
    
Für die restlichen Screenshots in diesem Lernprogramm wird DevTools in einem separaten Fenster angezeigt.  Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, `Undock` **** um das Befehlsmenü zu öffnen, und geben Sie ein, und wählen Sie dann Abdocken in ein separates Fenster aus.  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="Nicht gesockte DevTools" lightbox="../media/speed-console.msft.png":::
   Nicht gesockte DevTools  
:::image-end:::  

### <a name="establish-a-baseline"></a>Einrichten einer Basislinie  

Die Basislinie ist eine Aufzeichnung der Leistung der Website, bevor Sie Leistungsverbesserungen vorgenommen haben.  

1.  Wählen Sie das **Tool Überwachungen** aus.  Sie kann hinter der Schaltfläche **Weitere Bereiche** \( Weitere ![ Bereiche ](../media/more-panels-icon.msft.png) \) ausgeblendet werden.  In diesem Panel befindet sich ein Leuchtturm, da das Projekt, das das Auditpanel unterstützt, den Namen **"Leuchtkraft" trägt.**  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Das Tool "Überwachungen"" lightbox="../media/speed-audits-performance.msft.png":::
       Das **Tool "Überwachungen"**  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  Passen Sie Ihre Überwachungskonfigurationseinstellungen den Einstellungen in der vorherigen Abbildung an.  Hier finden Sie eine Erläuterung der verschiedenen Optionen:  
    
    *   **Gerät**.  Auf **Mobile festgelegt** ändert die Zeichenfolge des Benutzer-Agents und simuliert einen mobilen Viewport.  Wenn Sie **auf Desktop** festlegen, werden die Mobile-Änderungen **einfach** deaktiviert.  
    *   **Überwachungen**.  Deaktivieren Sie eine Kategorie, um zu verhindern, dass diese Überwachungen vom Überwachungsbericht ausgeführt werden, und schließen Sie diese Überwachungen aus Ihrem Bericht aus. ****  Lassen Sie die anderen Kategorien aktiviert, wenn Sie die typen von Empfehlungen anzeigen möchten, die bereitgestellt werden.  Deaktivieren Sie Kategorien, um den Überwachungsprozess geringfügig zu beschleunigen.  
    *   **Einschränkung**.  Auf **Simulierte langsame 4G festgelegt, simuliert die 4-fache CPU-Verlangsamung** die typischen Bedingungen des Browsens auf einem mobilen Gerät.  Er wird als "simuliert" bezeichnet, da der Überwachungsprozess während des Überwachungsprozesses nicht tatsächlich gedrosselt wird.  Stattdessen wird lediglich extrapoliert, wie lange die Seite unter mobilen Bedingungen geladen werden muss.  Die **Einstellung Applied...** hingegen drosselt ihre CPU und Ihr Netzwerk, was zu einem längeren Überwachungsprozess beit.  
    *   **Speicher löschen**.  Aktivieren Sie das Kontrollkästchen, um den speicher, der der Seite zugeordnet ist, vor jeder Überwachung zu löschen.  Lassen Sie diese Einstellung bei, wenn Sie überwachen möchten, wie Besucher Ihre Website beim ersten Mal erleben.  Deaktivieren Sie diese Einstellung, wenn Sie die Wiederholungsbesuchserfahrung wünschen.  
    
1.  Wählen **Sie Überwachungen ausführen aus.**  Nach 10 bis 30 **** Sekunden zeigt der Bereich Überwachungen einen Bericht über die Leistung der Website an.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Der Bericht für den Überwachungsbericht über die Leistung der Website" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       Der Bericht für den Überwachungsbericht über die Leistung der Website  
    :::image-end:::  
    
#### <a name="handling-report-errors"></a>Behandeln von Berichtsfehlern  

Wenn Sie jemals einen Fehler in Ihrem Bericht zum Überwachungsbericht erhalten, versuchen Sie, die Demoregisterkarte aus einem **InPrivate-Fenster** zu führen, ohne dass andere Registerkarten geöffnet sind.  Dadurch wird sichergestellt, dass Microsoft Edge in einem sauberen Zustand ausgeführt wird.  Insbesondere Microsoft Edge Extensions stören häufig den Überwachungsprozess.  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <a name="understand-your-report"></a>Verstehen Ihres Berichts  

Die Nummer oben in Ihrem Bericht ist die Gesamtleistungsnote für die Website.  Wenn Sie später Änderungen am Code vornehmen, sollte die angezeigte Anzahl steigen.  Eine höhere Punktzahl bedeutet eine bessere Leistung.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Gesamtleistungsergebnis" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   Gesamtleistungsergebnis  
:::image-end:::  

Der **Abschnitt Metriken** enthält mengenmäßige Messungen der Leistung der Website.  Jede Metrik bietet Einblick in einen anderen Aspekt der Leistung.  Beispielsweise informiert **First Contentful Paint,** wann Inhalte zum ersten Mal auf den Bildschirm gefärbt werden. Dies ist ein wichtiger Meilenstein in der Wahrnehmung der Seitenlast durch den Benutzer, während **Time To Interactive** den Punkt markiert, an dem die Seite so bereit erscheint, dass Benutzerinteraktionen ausgeführt werden können.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Abschnitt "Metriken"" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   Abschnitt **"Metriken"**  
:::image-end:::  

Wählen Sie die hervorgehobene Umschaltfläche in der folgenden Abbildung aus, um eine Beschreibung für jede Metrik anzeigen zu können, und wählen Sie **Weitere** Informationen aus, um die Dokumentation dazu zu lesen.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Wählen Sie die hervorgehobene Umschaltfläche aus, um die Metrikelemente zu erweitern." lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   Wählen Sie die hervorgehobene Umschaltfläche aus, um die Metrikelemente zu erweitern.  
:::image-end:::  

Unter Metriken finden Sie eine Sammlung von Screenshots, die ihnen zeigen, wie die Seite wie geladen aussah.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Screenshots, wie die Seite beim Laden aussah" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Screenshots, wie die Seite beim Laden aussah  
:::image-end:::  

Der **Abschnitt Verkaufschancen** enthält spezifische Tipps zur Verbesserung der Ladeleistung dieser spezifischen Seite.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Der Abschnitt Verkaufschancen" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Der **Abschnitt Verkaufschancen**  
:::image-end:::  

Wählen Sie eine Gelegenheit aus, um mehr darüber zu erfahren.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Eliminieren von Möglichkeiten zum Rendern blockierender Ressourcen" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   **Eliminieren von Möglichkeiten zum Rendern blockierender** Ressourcen  
:::image-end:::  

Wählen **Sie Weitere Informationen** aus, um Dokumentation darüber zu erhalten, warum eine Gelegenheit wichtig ist, und spezifische Empfehlungen zum Beheben dieser Möglichkeit.  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Dokumentation zur Möglichkeit zum Entfernen von Renderblockierungsressourcen" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   Dokumentation zur **Möglichkeit zum Entfernen von Renderblockierungsressourcen**  
:::image-end:::  

Der **Abschnitt Diagnose** enthält weitere Informationen zu Faktoren, die zur Ladezeit der Seite beitragen.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Der Abschnitt "Diagnostics"" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   Der **Abschnitt "Diagnostics"**  
:::image-end:::  

Der **Abschnitt "Bestandene Prüfungen"** zeigt Ihnen, was die Website ordnungsgemäß macht.  Wählen Sie aus, um den Abschnitt zu erweitern.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Der Abschnitt "Bestandene Überwachungen"" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   Der **Abschnitt "Bestandene Überwachungen"**  
:::image-end:::  

## <a name="step-2-experiment"></a>Schritt 2: Experiment  

Im Abschnitt Verkaufschancen Ihres Überwachungsberichts erhalten Sie Tipps zur Verbesserung der Leistung der Seite.  In diesem Abschnitt implementieren Sie die empfohlenen Änderungen an der Codebasis und überwachen die Website nach jeder Änderung, um zu messen, wie sich dies auf die Websitegeschwindigkeit auswirkt.  

### <a name="enable-text-compression"></a>Aktivieren der Textkomprimierung  

In Ihrem Bericht heißt es, dass die Vermeidung enormer Netzwerknutzlasten eine der besten Möglichkeiten zur Verbesserung der Leistung der Seite ist.  Das Aktivieren der Textkomprimierung ist eine Möglichkeit, die Leistung der Seite zu verbessern.  

Die Textkomprimierung ist, wenn Sie die Größe einer Textdatei reduzieren oder komprimieren, bevor Sie sie über das Netzwerk senden.  Ähnlich wie Sie ein Verzeichnis archivieren können, bevor Sie es senden, um die Größe zu reduzieren.  

Bevor Sie die Komprimierung aktivieren, finden Sie hier eine Reihe von Möglichkeiten, um manuell zu überprüfen, ob Textressourcen komprimiert sind.  

1.  Wählen Sie das **Netzwerktool** aus.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Netzwerkbereich" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       Das **Netzwerktool**  
    :::image-end:::  
    
1.  Wählen Sie das **Symbol Netzwerkeinstellung** aus.  
1.  Aktivieren Sie das **Kontrollkästchen Große Anforderungszeilen** verwenden.  Die Höhe der Zeilen in der Tabelle der Netzwerkanforderungen nimmt zu.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Große Zeilen in der Tabelle "Netzwerkanforderungen"" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       Große Zeilen in der Tabelle "Netzwerkanforderungen"  
    :::image-end:::  
    
1.  Wenn die **Spalte Größe** in der Tabelle der Netzwerkanforderungen nicht angezeigt wird, wählen Sie die Tabellenkopfzeile > **Größe aus.**  

Jede **Zelle Size** zeigt zwei Werte an.  Der höchste Wert ist die Größe der heruntergeladenen Ressource.  
Der untere Wert ist die Größe der nicht komprimierten Ressource.  Wenn die beiden Werte identisch sind, wird die Ressource nicht komprimiert, wenn sie über das Netzwerk gesendet wird.  In der vorherigen Abbildung sind beispielsweise die oberen und unteren Werte `bundle.js` für und `1.2 MB` `1.2 MB` .  

Überprüfen Sie auf Komprimierung, indem Sie die HTTP-Header einer Ressource überprüfen:  

1.  Wählen Sie `bundle.js` aus.  
1.  Wählen Sie **den Bereich Kopfzeilen** aus.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Der Kopfzeilenbereich" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       Der **Kopfzeilenbereich**  
    :::image-end:::  
    
1.  Durchsuchen Sie **den Abschnitt Antwortkopfzeilen** nach einer `content-encoding` Kopfzeile.  Eine `content-encoding` Überschrift wird nicht angezeigt, d. h. sie wurde nicht `bundle.js` komprimiert.  Wenn eine Ressource komprimiert wird, wird dieser Header in der Regel auf `gzip` , `deflate` oder `br` festgelegt.  Eine Erläuterung der Werte finden Sie unter [Direktiven][MDNContentEncodingDirectives].  

Genug mit den Erläuterungen.  Zeit für einige Änderungen.  Aktivieren Sie die Textkomprimierung, indem Sie ein paar Codezeilen hinzufügen:  

1.  Wählen Sie auf der Registerkarte Editor ** die Optionserver.js**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Bearbeiten server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       Bearbeiten `server.js`  
    :::image-end:::  
    
1.  Fügen Sie den folgenden Code zu **server.js. **  Stellen Sie sicher, dass Sie vor `app.use(compression())` `app.use(express.static('build'))` setzen.  

    ```javascript
    const express = require('express');
    const app = express();
    const fs = require('fs');
    const compression = require('compression');

    app.use(compression());
    app.use(express.static('build'));
    
    const listener = app.listen(process.env.PORT || 1234, function () {
        console.log(`Listening on port ${listener.address().port}`);
    });
    ```  
    
    > [!NOTE]
    > In der Regel müssen Sie das Paket über so etwas wie installieren, aber dies wurde `compression` bereits für Sie `npm i -S compression` durchgeführt.  
    
1.  Warten Sie, bis Glitch den neuen Build der Website bereitgestellt hat.  Die ausgefallene Animation neben **Tools** bedeutet, dass die Website neu erstellt und erneut zur Verfügung steht.  Die Änderung ist bereit, wenn die Animation neben **Tools** nicht mehr angezeigt wird.  Wählen **Sie Anzeigen** aus, und wählen Sie erneut In einem neuen **Fenster** aus.  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
Verwenden Sie die Workflows, die Sie zuvor gelernt haben, um manuell zu überprüfen, ob die Komprimierung funktioniert:  

1.  Wechseln Sie zurück zur Demoregisterkarte, und aktualisieren Sie die Seite.  In **der Spalte** Größe sollten nun 2 verschiedene Werte für Textressourcen wie angezeigt `bundle.js` werden.  In der Abbildung nach der folgenden Abbildung ist der oberste Wert für die Größe der Datei, die über das Netzwerk gesendet wurde, und der untere Wert ist die nicht komprimierte `256 KB` `bundle.js` `1.2 MB` Dateigröße.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="Die Spalte Größe zeigt jetzt 2 verschiedene Werte für Textressourcen an." lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       Die **Spalte Größe** zeigt jetzt 2 verschiedene Werte für Textressourcen an.  
    :::image-end:::  
    
1.  Der **Abschnitt Antwortkopfzeilen** für `bundle.js` sollte jetzt einen Header `content-encoding: gzip` enthalten.
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="Der Abschnitt Antwortkopfzeilen enthält jetzt einen Header für die Inhaltscodierung." lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       Der **Abschnitt Antwortkopfzeilen** enthält jetzt einen Header für die Inhaltscodierung.  
    :::image-end:::  
    
Überwachen Sie die Seite erneut, um zu messen, welche Art von Auswirkung die Textkomprimierung auf die Ladeleistung der Seite hat:  

1.  Wählen Sie das **Tool Überwachungen** aus.  
1.  Wählen **Sie Ausführen einer Überwachung** \( Ausführen einer Überwachung ![ ](../media/perform-icon.msft.png) \).  
1.  Lassen Sie die Einstellungen wie zuvor.  
1.  Wählen **Sie Überwachung ausführen aus.**  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach der Aktivierung der Textkomprimierung" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       Ein Überwachungsbericht nach der Aktivierung der Textkomprimierung  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  Ihr Gesamtleistungsergebnis sollte erhöht sein, was bedeutet, dass die Website schneller wird.  

#### <a name="text-compression-in-the-real-world"></a>Textkomprimierung in der realen Welt  

Die meisten Server verfügen tatsächlich über einfache Korrekturen wie dies zum Aktivieren der Komprimierung!  Suchen Sie einfach, wie Sie den Server konfigurieren, den Sie zum Komprimieren von Text verwenden.  

### <a name="resize-images"></a>Ändern der Größe von Bildern  

Ihr Bericht weist darauf hin, dass das Vermeiden enormer Netzwerknutzlasten eine der besten Möglichkeiten zur Verbesserung der Leistung der Seite ist.  Die Größenänderung von Bildern trägt dazu bei, die Größe der Netzwerknutzlast zu reduzieren.  Wenn Ihr Benutzer Ihre Bilder auf einem 500 Pixel breiten Bildschirm des mobilen Geräts anschaut, hat es wirklich keinen Sinn, ein 1500 Pixel breites Bild zu senden.  Idealerweise senden Sie ein Bild mit einer Breite von 500 Pixeln.  

1.  Wählen Sie in Ihrem Bericht **Enorme Netzwerknutzlast** vermeiden aus, um die Größe der Bilder anzeigen zu lassen.  Es sieht so aus, als seien 2 der JPG-Dateien über 2000 KB, was größer als erforderlich ist.  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  Öffnen Sie zurück auf der Registerkarte Editor `src/model.js` .  
1.  Ersetzen Sie `const dir = 'big'` durch `const dir = 'small'`.  Dieses Verzeichnis enthält Kopien der gleichen Bilder, deren Größe geändert wurde.  
1.  Überwachen Sie die Seite erneut, um zu zeigen, wie sich die Änderung auf die Lastleistung auswirkt.  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach der Größenänderung von Bildern" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       Ein Überwachungsbericht nach der Größenänderung von Bildern  
    :::image-end:::  
    
Die angezeigte Änderung hat nur geringfügige Auswirkungen auf die Gesamtleistungsleistung.  Die Bewertung zeigt jedoch nicht eindeutig, wie viele Netzwerkdaten Sie Ihre Benutzer speichern.  Die Gesamtgröße der alten Fotos lag bei etwa 5,3 Megabyte, jetzt sind es nur noch etwa 0,18 Megabyte.  

#### <a name="resizing-images-in-the-real-world"></a>Ändern der Größe von Bildern in der realen Welt  

Für eine kleine App ist eine einmal angepasste Größe wie dies möglicherweise ausreichend.  Bei einer großen App ist dies jedoch offensichtlich nicht skalierbar.  Hier sind einige Strategien zum Verwalten von Bildern in großen Apps:  

*   Ändern der Größe von Bildern während des Buildprozesses.  
*   Erstellen Sie während des Erstellungsprozesses mehrere Größen der einzelnen Bilder, und verwenden Sie sie `srcset` dann in Ihrem Code.  Zur Laufzeit übernimmt der Browser die Auswahl, welche Größe für das Gerät am besten ist.  
    <!--Navigate to [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   Verwenden Sie ein Image-CDN, mit dem Sie die Größe eines Bilds dynamisch ändern können, wenn Sie es anfordern.  
*   Optimieren Sie zumindest jedes Bild.  Dies kann zu enormen Einsparungen führen.  
  Optimierung ist, wenn Sie ein Bild über ein spezielles Programm ausführen, das die Größe der Bilddatei reduziert.  Weitere Tipps finden Sie unter [Essential Image Optimization][EssentialImageOptimization].  
    
### <a name="eliminate-render-blocking-resources"></a>Eliminieren von render blockierenden Ressourcen  

In Ihrem neuesten Bericht heißt es, dass das Eliminieren von Renderblockierressourcen jetzt die größte Möglichkeit ist.  

Eine Renderblockierressource ist eine externe JavaScript- oder CSS-Datei, die der Browser herunterladen, analysieren und ausführen muss, bevor die Seite angezeigt wird.  Ziel ist es, nur den zentralen CSS- und JavaScript-Code ausführen, der zum ordnungsgemäßen Anzeigen der Seite erforderlich ist.  

Die erste Aufgabe besteht also darin, Code zu finden, den Sie beim Laden der Seite nicht ausführen müssen.  

1.  Wählen **Sie Render blockierende Ressourcen entfernen aus,** um die blockierten Ressourcen anzeigen zu können:  
    `lodash.js` und `jquery.js` .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Weitere Informationen zur Gelegenheit Rendersperren von Ressourcen beseitigen" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       Weitere Informationen zur **Gelegenheit Rendersperren von Ressourcen** beseitigen  
    :::image-end:::  
    
1.  Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, `Coverage` **** um das Befehlsmenü zu öffnen, mit der Eingabe zu beginnen, und wählen Sie dann Abdeckung anzeigen aus.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Öffnen des Befehlsmenüs im Überwachungbereich" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       Öffnen des Befehlsmenüs im **Überwachungbereich**  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="Das Tool "Abdeckung"" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       Das **Tool "Abdeckung"**  
    :::image-end:::  
    
1.  Wählen **Sie Aktualisieren** \( Aktualisieren ![ ](../media/reload-icon.msft.png) \).  Das **Tool** Coverage bietet eine Übersicht darüber, wie viel Code in , und ausgeführt wird, während `bundle.js` die Seite geladen `jquery.js` `lodash.js` wird.  In der Abbildung nach der folgenden Abbildung werden ca. 76 % bzw. 30 % der jQuery- und Lodash-Dateien nicht verwendet.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="Der Bericht "Abdeckung"" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       Der Bericht "Abdeckung"  
    :::image-end:::  
    
1.  Wählen Sie ** diejquery.js** aus.  DevTools öffnet die Datei im Bereich Quellen.  Eine Codezeile wurde angezeigt, wenn sie einen blauen Balken daneben hat.  Eine rote Leiste bedeutet, dass sie nicht ausgeführt wurde und bei der Seitenlast definitiv nicht benötigt wird.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Anzeigen der jQuery-Datei im Bereich Quellen" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       Anzeigen der jQuery-Datei im **Bereich Quellen**  
    :::image-end:::  
    
1.  Scrollen Sie ein wenig durch den jQuery-Code.  Einige der Zeilen, die "ausführen" erhalten, sind eigentlich nur Kommentare.  Das Ausführen dieses Codes über ein Minifier, das Kommentare entfernt, ist eine weitere Möglichkeit, die Größe dieser Datei zu reduzieren.  

Kurz gesagt, wenn Sie mit Ihrem **** eigenen Code arbeiten, hilft Ihnen das Coverage-Tool dabei, Ihren Code zeiler zu analysieren und nur den Code zu versenden, der für das Laden von Seiten erforderlich ist.  

Sind die `jquery.js` `lodash.js` Und-Dateien sogar zum Laden der Seite erforderlich?  Das **Tool zum Blockieren** von Anfragen zeigt an, was geschieht, wenn Ressourcen nicht verfügbar sind.  

1.  Wählen Sie das **Netzwerktool** aus.  
1.  Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das Befehlsmenü erneut zu öffnen.  
1.  Beginnen Sie mit der `blocking` Eingabe, und wählen Sie **Dann Anforderungsblockierung anzeigen aus.**  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="Das Tool zum Blockieren von Anfragen" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       Das **Tool zum Blockieren von** Anfragen  
    :::image-end:::  
    
1.  Wählen **Sie Muster hinzufügen** \( Muster hinzufügen \), geben Sie ![ ](../media/add-pattern-icon.msft.png) `/libs/*` ein, und wählen Sie dann `Enter` aus, um dies zu bestätigen.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Hinzufügen eines Musters zum Blockieren jeder Anforderung zum libs-Verzeichnis" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       Hinzufügen eines Musters zum Blockieren einer Anforderung zum `libs` Verzeichnis  
    :::image-end:::  
    
1.  Aktualisieren Sie die Seite.  Die jQuery- und Lodash-Anforderungen sind rot, d. h., die Anforderungen wurden blockiert.   Die Seite wird weiterhin geladen und ist interaktiv, daher sieht es so aus, als ob diese Ressourcen überhaupt nicht benötigt werden!  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="Der Netzwerkbereich zeigt an, dass die Anforderungen blockiert wurden" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       Das **Netzwerktool** zeigt, dass die Anforderungen blockiert wurden  
    :::image-end:::  
    
1.  Wählen **Sie Alle Muster entfernen** \( Alle Muster entfernen ![ ](../media/remove-icon.msft.png) \), um das `/libs/*` Blockierungsmuster zu löschen.  
    
Im Allgemeinen ist das **Tool zum** Blockieren von Anforderungen hilfreich, um das Verhalten Ihrer Seite zu simulieren, wenn keine bestimmte Ressource verfügbar ist.  

Entfernen Sie nun die Verweise auf diese Dateien aus dem Code, und überwachen Sie die Seite erneut:  

1.  Öffnen Sie zurück auf der Registerkarte Editor `template.html` .  
1.  Löschen Sie `<script src="/libs/lodash.js">` und `<script src="/libs/jquery.js"></script>`.  
1.  Warten Sie, bis die Website neu erstellen und erneut bereitgestellt wird.  
1.  Überwachen Sie die Seite erneut über das **Überwachungstool.**  Ihr Gesamtergebnis sollte sich erneut verbessert haben.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach dem Entfernen der renderblocking-Ressourcen" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       Ein **Überwachungsbericht** nach dem Entfernen der renderblocking-Ressourcen  
    :::image-end:::  
    
#### <a name="optimizing-the-critical-rendering-path-in-the-real-world"></a>Optimieren des kritischen Renderingpfads in der realen Welt  

Der **Kritische Renderingpfad** bezieht sich auf den Code, den Sie zum Laden einer Seite benötigen.  Beschleunigen Sie im Allgemeinen das Laden der Seite, indem Sie während des Seitenladevorganges nur kritischen Code versenden und dann alles andere verzögert laden.  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   Es ist unwahrscheinlich, dass Sie Skripts finden können, die Sie ganz einfach entfernen können, aber möglicherweise finden Sie viele Skripts, die Sie während des Seitenlades nicht anfordern müssen, sondern möglicherweise asynchron angefordert werden.  <!--Navigate to [Using async or defer][async].  -->  
*   Wenn Sie ein Framework verwenden, überprüfen Sie, ob es über einen Produktionsmodus verfügt.  In diesem Modus kann [][WebpackTreeShaking] ein Feature wie z. B. das Baumschütteln verwendet werden, um unnötigen Code zu vermeiden, der das kritische Rendern blockiert.  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <a name="do-less-main-thread-work"></a>Weniger Hauptthreadarbeit  

Ihr aktueller Bericht zeigt einige geringfügige potenzielle Einsparungen im Abschnitt Verkaufschancen, aber wenn Sie im Abschnitt Diagnose nach unten schauen, sieht es so aus, als ob der größte Engpass zu viel Hauptthreadaktivität ist.  

Der Hauptthread ist der Ort, an dem der Browser die meiste Arbeit zum Anzeigen einer Seite vor sich hat, z. B. die Analyse und Ausführung von HTML, CSS und JavaScript.  

Das Ziel besteht in der Verwendung des Leistungsbereichs, um zu analysieren, welche Arbeit der Hauptthread während des Ladens der Seite macht, und Möglichkeiten zum Zurück- oder Entfernen unnötiger Arbeit zu finden.  

1.  Wählen Sie das **Tool Leistung** aus.  
1.  Wählen **Sie Aufnahmeeinstellungen** \( ![ Aufnahmeeinstellungen ](../media/capture-icon.msft.png) \).  
1.  Legen **Sie Netzwerk** auf **Langsame 3G** und CPU **auf** **6x Verlangsamung.**  Mobile Geräte haben in der Regel mehr Hardwareeinschränkungen als Laptops oder Desktops. Mit diesen Einstellungen können Sie die Seitenlast so erleben, als würden Sie ein weniger leistungsfähiges Gerät verwenden.  
1.  Wählen **Sie Aktualisieren** \( Aktualisieren ![ ](../media/reload-icon.msft.png) \).  DevTools aktualisiert die Seite und erstellt dann eine Visualisierung aller Ausgeführten, um die Seite zu laden.  Diese Visualisierung wird als Ablaufverfolgung **bezeichnet.**  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Die Ablaufverfolgung des Leistungstools für die Seitenlast" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       Die **Ablaufverfolgung** des Leistungstools für die Seitenlast  
    :::image-end:::  
    
Die Ablaufverfolgung zeigt die Aktivität chronologisch von links nach rechts an.  Die FpS-, CPU- und #A0 oben bieten Ihnen eine Übersicht über Frames pro Sekunde, #A1 und Netzwerkaktivität.  Der gelbe Block, der in der Abbildung nach dem nächsten hervorgehoben ist, war die CPU vollständig mit Skriptaktivität beschäftigt.  Dies ist ein Hinweis darauf, dass Sie möglicherweise die Seitenlast beschleunigen können, indem Sie weniger JavaScript-Arbeit tun.  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="Der Abschnitt Übersicht der Ablaufverfolgung" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   Der Abschnitt Übersicht der Ablaufverfolgung  
:::image-end:::  

Untersuchen Sie die Ablaufverfolgung, um Möglichkeiten für weniger JavaScript-Arbeit zu finden:  

1.  Wählen Sie den **Abschnitt Timings** aus, um ihn zu erweitern.  Basierend auf der Tatsache, dass es eine Reihe von [Timings-Maßnahmen][MDNUserTimingApi] von React gibt, scheint es, als würde Tonys App den Entwicklungsmodus von React verwenden.  Der Wechsel in den Produktionsmodus von React kann zu einfachen Leistungsgewinnen führen.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="Der Abschnitt Timings" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       Der **Abschnitt Timings**  
    :::image-end:::  
    
1.  Wählen **Sie Timings** erneut aus, um diesen Abschnitt zu reduzieren.  
1.  Durchsuchen Sie **den Abschnitt Main.**  Dieser Abschnitt zeigt ein chronologisches Protokoll der Hauptthreadaktivität von links nach rechts.  Die y-Achse (oben nach unten) zeigt, warum Ereignisse aufgetreten sind.  Beispielsweise führte das Ereignis im Feigenblatt nach dem folgenden Ereignis dazu, dass die Funktion ausgeführt wurde, was zur Ausführung führte, was dazu führte, dass sie ausgeführt `Evaluate Script` `(anonymous)` `(anonymous)` `__webpack__require__` wurde, und so weiter.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Der Abschnitt "Main"" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       Der **Abschnitt "Main"**  
    :::image-end:::  
    
1.  Scrollen Sie nach unten im **Abschnitt Main.**  Wenn Sie ein Framework verwenden, wird der Großteil der oberen Aktivität durch das Framework verursacht, das in der Regel nicht in Ihrem Steuerelement liegt.  Die von Ihrer App verursachte Aktivität befindet sich in der Regel unten.  In dieser App scheint eine Funktion namens viele Anforderungen an `App` eine Funktion zu `mineBitcoin` verursachen.  Es klingt, als würde Tony die Geräte seiner Fans zum Minen von Kryptowährung verwenden...  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Zeigen auf die mineBitcoin-Aktivität" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       Zeigen auf die `mineBitcoin` Aktivität  
    :::image-end:::  
    
    > [!NOTE]
    > Obwohl die Anforderungen, die Ihr Framework stellt, in der Regel nicht in Ihrem Steuerelement sind, können Sie Ihre App manchmal so strukturieren, dass das Framework ineffizient ausgeführt wird.  Die Umstrukturierung Ihrer App zur effizienten Verwendung des Frameworks ist eine Möglichkeit, weniger Hauptthreadarbeit zu leisten.  Dies erfordert jedoch ein tiefes Verständnis der Funktionsweise Ihres Frameworks und der Art von Änderungen, die Sie in Ihrem eigenen Code vornehmen, um das Framework effizienter zu verwenden.  
    
1.  Erweitern Sie **den Abschnitt Bottom-Up.**  Diese Registerkarte bricht auf, welche Aktivitäten die meiste Zeit in Sich nahmen.  Wenn im Abschnitt "Bottom-Up" nichts angezeigt wird, wählen Sie die Bezeichnung für **den Abschnitt "Main"** aus.  Im **Abschnitt Bottom-Up** werden nur Informationen zu den derzeit ausgewählten Aktivitäten oder Gruppen von Aktivitäten angezeigt.  Wenn Sie beispielsweise eine der Aktivitäten ausgewählt haben, zeigt der `mineBitcoin` **Abschnitt Bottom-Up** nur Informationen für diese eine Aktivität an.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="Registerkarte Bottom-Up" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       Registerkarte **Unten nach** oben  
    :::image-end:::  
    
In **der Spalte** Self Time wird angezeigt, wie viel Zeit direkt in jeder Aktivität verbracht wurde.  In der folgenden Abbildung wurden beispielsweise ca. 63 % der Hauptthreadzeit für die Funktion `mineBitcoin` verwendet.  

Zeit, um zu überprüfen, ob die Verwendung des Produktionsmodus und die Reduzierung der JavaScript-Aktivität die Seitenlast beschleunigen kann.  Beginnen Sie mit dem Produktionsmodus:  

1.  Öffnen Sie auf der Registerkarte Editor `webpack.config.js` .  
1.  Ändern Sie `"mode":"development"` in `"mode":"production"`.  
1.  Warten Sie, bis der neue Build bereitgestellt wird.  
1.  Überwachen Sie die Seite erneut.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach der Konfiguration von Webpack für die Verwendung des Produktionsmodus" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       Ein Überwachungsbericht nach der Konfiguration von Webpack für die Verwendung des Produktionsmodus  
    :::image-end:::  
    
Reduzieren Sie die JavaScript-Aktivität, indem Sie die Anforderung zu `mineBitcoin` entfernen:  

1.  Öffnen Sie auf der Registerkarte Editor `src/App.jsx` .  
1.  Kommentieren Sie die Anforderung `this.mineBitcoin(1500)` an in `constructor` aus.  
1.  Warten Sie, bis der neue Build bereitgestellt wird.  
1.  Überwachen Sie die Seite erneut.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach dem Entfernen unnötiger JavaScript-Arbeit" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       Ein Überwachungsbericht nach dem Entfernen unnötiger JavaScript-Arbeit  
    :::image-end:::  
    
Sieht so aus, als habe diese letzte Änderung einen enormen Leistungssprung verursacht!  

> [!NOTE]
> Dieser Abschnitt bot eine ziemlich kurze Einführung in den Bereich "Leistung".  Weitere Informationen zum Analysieren der Seitenleistung finden Sie unter [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference].  

<!--todo: add section when available -->  

#### <a name="doing-less-main-thread-work-in-the-real-world"></a>Weniger Hauptthreadarbeit in der realen Welt  

Im Allgemeinen ist das **Performance-Tool** die am häufigsten verwendeten Methoden, um zu verstehen, welche Aktivitäten Ihre Website beim Laden macht, und Wie Sie unnötige Aktivitäten entfernen können.  

Wenn Sie einen Ansatz bevorzugen, der sich eher anfühlt, können Sie mit der `console.log()` [User Timing-API][MDNUserTimingApi] bestimmte Phasen ihres App-Lebenszyklus beliebig markieren, um nachverfolgt zu werden, wie lange jede dieser Phasen dauert.  

## <a name="summary"></a>Zusammenfassung  

*   Wenn Sie die Auslastungsleistung eines Standorts optimieren möchten, beginnen Sie immer mit einer Überwachung.  Die Überwachung legt eine Basislinie fest und gibt Ihnen Tipps zur Verbesserung.  
*   Nehmen Sie jeweils eine Änderung vor, und überwachen Sie die Webseite nach jeder Änderung, um anzuzeigen, wie sich diese isolierte Änderung auf die Leistung auswirkt.  

<!--
## Next steps  

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Leistungsanalysereferenz | Microsoft Docs"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Einführung in web development class | Coursera"  

[EssentialImageOptimization]: https://images.guide "Wesentliche Bildoptimierung"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Direktiven – Inhaltscodierungsrichtlinien | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "Benutzer-Timing-API-| MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Baumschütteln | webpack"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
