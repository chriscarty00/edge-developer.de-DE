---
description: Erfahren Sie, wie Sie Microsoft Edge devtools verwenden, um Wege zu finden, wie Sie Ihre Websites schneller laden können.
title: Optimieren der Website Geschwindigkeit mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: dafcb9c4d1194239baed7507e505d74d2b4ce1c8
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993440"
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





# Optimieren der Website Geschwindigkeit mit Microsoft Edge devtools   



## Ziel des Lernprogramms  

In diesem Lernprogramm erfahren Sie, wie Sie Microsoft Edge devtools verwenden, um Wege zu finden, wie Sie Ihre Websites schneller laden können.  

## Voraussetzungen  

*   Sie sollten über grundlegende Webentwicklungsfunktionen verfügen, ähnlich wie in dieser [Einführung in die Webentwicklungs Klasse][CourseraIntroductionWebDevelopmentClass].  
*   Sie müssen nichts über die Ladeleistung wissen.  In diesem Lernprogramm erfahren Sie mehr darüber!  

## Einführung   

Das ist Tony.  Tony ist in der Cat Society sehr bekannt.  Er hat eine Website entwickelt, damit seine Fans mehr über seine bevorzugten Lebensmittel erfahren können.  Seine Fans lieben die Website, aber Tony hört immer wieder Beschwerden, dass die Website langsam geladen wird.  Tony hat Sie gebeten, ihm beim Beschleunigen der Website zu helfen.  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-tony.msft.png":::
   Tony the Cat  
:::image-end:::  

## Schritt 1: Überwachen der Website   

Wenn Sie die Ladeleistung einer Website verbessern möchten, **beginnen Sie immer mit einer Überwachung**.  
Das Audit hat zwei wichtige Funktionen:  

*   Sie erstellt einen **Basisplan** , in dem Sie nachfolgende Änderungen messen können.  
*   Es gibt Ihnen **umsetzbare Tipps** , welche Änderungen die meisten Auswirkungen haben.  
    
### Einrichtung   

Zunächst müssen Sie die Website so einrichten, dass Sie später Änderungen daran vornehmen können.  

1.  [Öffnen Sie den Quellcode für die Website](https://glitch.com/edit/#!/tony).  Diese Registerkarte wird als **Registerkarte "Editor"** bezeichnet.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Die Registerkarte "Editor"" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       Die **Registerkarte "Editor"**  
    :::image-end:::  
    
1.  Wählen Sie **Tony**aus.  Ein Menü wird angezeigt.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Das Menü, das nach dem Klicken auf "Tony" angezeigt wird" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       Das Menü, das nach dem Klicken auf " **Tony** " angezeigt wird  
    :::image-end:::  
    
1.  Wählen Sie **Remix Project**aus.  Der Name des Projekts wechselt von **Tony** zu einem zufällig generierten Namen.  Sie haben jetzt eine eigene bearbeitbare Kopie des Codes.  Später können Sie Änderungen an diesem Code vornehmen.  
1.  Wählen Sie **in einem neuen Fenster** **anzeigen** und auswählen aus.  Die Demo wird in einer neuen Registerkarte geöffnet.  Diese Registerkarte wird als **Registerkarte Demo**bezeichnet.  Das Laden der Website kann einige Zeit in Anspruch nehmen.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Die Registerkarte "Demo"" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       Die Registerkarte "Demo"  
    :::image-end:::  
    
1.  Drücken Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \).  Microsoft Edge devtools wird parallel zur Demo geöffnet.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools und die Demo" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       DevTools und die Demo  
    :::image-end:::  
    
Für die restlichen Screenshots in diesem Lernprogramm wird devtools in einem separaten Fenster angezeigt.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen, einzugeben `Undock` , und wählen Sie dann **in separates Fenster Abdocken**aus.  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="Nicht angedockte devtools" lightbox="../media/speed-console.msft.png":::
   Nicht angedockte devtools  
:::image-end:::  

### Festlegen eines Basisplans   

Der Basisplan ist eine Aufzeichnung der Vorgehensweise der Website, bevor Sie Leistungsverbesserungen durchgeführt haben.  

1.  Wählen Sie die Registerkarte **Audits** aus.  Sie ist möglicherweise hinter der Schaltfläche " **Weitere Panels** \ ![ ][ImageMorePanelsIcon] " verborgen.  Auf diesem Panel befindet sich ein Leuchtturm, weil das Projekt, das das Audit Panel anbietet, den Namen **Lighthouse**trägt.  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Überwachungs Panel" lightbox="../media/speed-audits-performance.msft.png":::
       **Überwachungs** Panel  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  Vergleichen Sie Ihre Überwachungs Konfigurationseinstellungen mit denen in der vorherigen Abbildung.  Nachfolgend finden Sie eine Erläuterung der verschiedenen Optionen:  
    
    *   **Gerät**aus.  Wenn Sie auf **Mobile** festlegen, ändert sich die Zeichenfolge des Benutzer-Agents und simuliert ein mobiles Viewport.  Durch die Einstellung auf den **Desktop** werden die **mobilen** Änderungen so ziemlich deaktiviert.  
    *   **Audits**.  Durch das Deaktivieren einer Kategorie wird verhindert, dass der Überwachungsbereich diese Audits ausführt, und diese Audits werden aus dem Bericht ausgeschlossen.  Lassen Sie die anderen Kategorien aktiviert, wenn Sie die Typen von Empfehlungen anzeigen möchten, die bereitgestellt werden.  Das Deaktivieren von Kategorien beschleunigt den Überwachungsvorgang etwas.  
    *   **Einschränkung**.  Einstellung auf **simulierte langsame 4G, vierfache CPU-Verlangsamung** simuliert die typischen Bedingungen für das Browsen auf einem mobilen Gerät.  Sie wird als "simuliert" bezeichnet, da das Überwachungs Panel während des Überwachungsprozesses nicht tatsächlich gedrosselt wird.  Stattdessen wird nur extrapoliert, wie lange es dauert, bis die Seite unter mobilen Bedingungen geladen wurde.  Mit der Einstellung " **angewendet...** " wird dagegen Ihre CPU und Ihr Netzwerk tatsächlich gedrosselt, mit dem Kompromiss eines längeren Überwachungsprozesses.  
    *   **Speicher löschen**.  Wenn Sie dieses Kontrollkästchen aktivieren, wird vor jeder Überwachung der gesamte Speicherplatz gelöscht, der der Seite zugeordnet ist.  Belasse diese Einstellung, wenn Sie überprüfen möchten, wie die Besucher Ihrer Website erst einmal auftreten.  Deaktivieren Sie diese Einstellung, wenn Sie die Wiederholungs Besuchs Erfahrung wünschen.  
    
1.  Wählen Sie **Audits ausführen**aus.  Nach 10 bis 30 Sekunden wird im Überwachungs Panel ein Bericht über die Leistung der Website angezeigt.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Der Bericht für das Audits-Panel über die Leistung der Website" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       Der Bericht für das Audits-Panel über die Leistung der Website  
    :::image-end:::  
    
#### Behandeln von Berichts Fehlern   

Wenn Sie in Ihrem Audits-Panel-Bericht jemals eine Fehlermeldung erhalten, versuchen Sie, die Registerkarte Demo in einem **InPrivate** -Fenster auszuführen, ohne dass weitere Registerkarten geöffnet sind.  Dadurch wird sichergestellt, dass Sie Microsoft Edge in einem sauberen Zustand ausführen.  Insbesondere Microsoft-Edge-Erweiterungen stören häufig den Überwachungsprozess.  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### Grundlegendes zu Ihrem Bericht   

Die Zahl am oberen Rand des Berichts entspricht dem Gesamtleistungsfaktor für die Website.  Wenn Sie später Änderungen am Code vornehmen, sollte diese Zahl steigen.  Eine höhere Punktzahl bedeutet eine bessere Leistung.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Der Gesamtleistungsfaktor" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   Der Gesamtleistungsfaktor  
:::image-end:::  

Der Abschnitt **Metriken** bietet quantitative Maße für die Leistung der Website.  Jede Metrik bietet Einblicke in einen anderen Aspekt der Leistung.  Beispielsweise erfahren Sie in der **ersten Inhaltsfarbe** , wann Inhalte zuerst auf dem Bildschirm gemalt werden, was ein wichtiger Meilenstein für die Wahrnehmung der Seitenauslastung durch den Benutzer ist, während die **Zeit für interaktive** Kennzeichnung den Punkt angibt, an dem die Seite für die Behandlung von Benutzerinteraktionen bereit angezeigt wird.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Abschnitt "Metriken"" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   Abschnitt " **Metriken** "  
:::image-end:::  

Wählen Sie die hervorgehobene Umschaltfläche in der folgenden Abbildung aus, um eine Beschreibung für jede Metrik anzuzeigen, und klicken Sie auf **Weitere Informationen** , um die Dokumentation dazu zu lesen.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Auswählen der hervorgehobenen Umschaltfläche zum Erweitern der Metriken Elemente" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   Auswählen der hervorgehobenen Umschaltfläche zum Erweitern der Metriken Elemente  
:::image-end:::  

Unter Metriken finden Sie eine Sammlung von Screenshots, die Ihnen zeigen, wie die Seite beim Laden aussah.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Screenshots, wie die Seite beim Laden aussah" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Screenshots, wie die Seite beim Laden aussah  
:::image-end:::  

Im Abschnitt " **Verkaufschancen** " finden Sie spezielle Tipps zum Verbessern der Auslastungs Leistung dieser bestimmten Seite.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Der Abschnitt "Verkaufschancen"" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Der Abschnitt " **Verkaufschancen** "  
:::image-end:::  

Wählen Sie eine Gelegenheit aus, um mehr darüber zu erfahren.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Eliminieren von Render-Blockierungs Ressourcen" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   **Eliminieren von Render-Blockierungs Ressourcen**  
:::image-end:::  

Wählen Sie **Weitere Informationen** aus, um die Dokumentation dazu anzuzeigen, warum eine Verkaufschance wichtig ist, und spezifische Empfehlungen zur Behebung.  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Dokumentation für die Möglichkeit zum Eliminieren von Render-Blockierungs Ressourcen" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   Dokumentation für die Möglichkeit zum **eliminieren von Render-Blockierungs Ressourcen**  
:::image-end:::  

Der Abschnitt **Diagnostics** enthält weitere Informationen zu Faktoren, die zur Ladezeit der Seite beitragen.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Abschnitt "Diagnose"" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   Abschnitt " **Diagnose** "  
:::image-end:::  

Im Abschnitt "übertragene **Prüfungen** " wird gezeigt, was die Website richtig macht.  Wählen Sie diese Option aus, um den Abschnitt zu erweitern.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Abschnitt "übergebene Überprüfungen"" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   Abschnitt " **übergebene Überprüfungen** "  
:::image-end:::  

## Schritt 2: experimentieren   

Im Abschnitt "Verkaufschancen" Ihres Überwachungsberichts erhalten Sie Tipps, wie Sie die Leistung der Seite verbessern können.  In diesem Abschnitt implementieren Sie die empfohlenen Änderungen an der CodeBase, indem Sie die Website nach jeder Änderung überwachen, um zu messen, wie sich dies auf die Geschwindigkeit der Website auswirkt.  

### Aktivieren der Text Komprimierung   

Ihr Bericht besagt, dass die Vermeidung von enormen Netzwerklasten eine der besten Möglichkeiten zur Verbesserung der Leistung der Seite darstellt.  Das Aktivieren der Text Komprimierung bietet die Möglichkeit, die Leistung der Seite zu verbessern.  

Die Text Komprimierung erfolgt, wenn Sie die Größe einer Textdatei reduzieren oder komprimieren, bevor Sie Sie über das Netzwerk senden.  Eine Art gefällt Ihnen, wie Sie einen Ordner komprimieren können, bevor Sie ihn per e-Mail senden, um die Größe zu verringern.  

Bevor Sie die Komprimierung aktivieren, gibt es eine Reihe von Möglichkeiten, um manuell zu überprüfen, ob Textressourcen komprimiert werden.  

1.  Wählen Sie die Registerkarte **Netzwerk** aus.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Netzwerk Panel" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       **Netzwerk** Panel  
    :::image-end:::  
    
1.  Wählen Sie das Symbol **Netzwerkeinstellung** aus.  
1.  Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** .  Die Höhe der Zeilen in der Tabelle der Netzwerkanforderungen nimmt zu.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Große Zeilen in der Tabelle "Netzwerkanforderungen"" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       Große Zeilen in der Tabelle "Netzwerkanforderungen"  
    :::image-end:::  
    
1.  Wenn die Spalte **Größe** in der Tabelle der Netzwerkanforderungen nicht angezeigt wird, klicken Sie auf die Tabellenüberschrift, und wählen Sie dann **Größe**aus.  

Jede **Größen** Zelle enthält zwei Werte.  Der oberste Wert ist die Größe der heruntergeladenen Ressource.  
Der untere Wert gibt die Größe der unkomprimierten Ressource an.  Wenn die beiden Werte identisch sind, wird die Ressource nicht komprimiert, wenn Sie über das Netzwerk gesendet wird.  In der vorhergehenden Abbildung sind die oberen und unteren Werte für " `bundle.js` sind" `1.2 MB` und " `1.2 MB` .  

Überprüfen Sie auf Komprimierung, indem Sie die HTTP-Header einer Ressource prüfen:  

1.  Wählen Sie **bundle.js**aus.  
1.  Wählen Sie die Registerkarte über **Schriften** aus.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Die Registerkarte "Überschriften"" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       Die Registerkarte "über **Schriften** "  
    :::image-end:::  
    
1.  Durchsuchen Sie den Abschnitt **Antwort Kopfzeilen** nach einer `content-encoding` Kopfzeile.  Sie sollten keines sehen, was bedeutet, dass es sich nicht um eine `bundle.js` Komprimierung handelt.  Wenn eine Ressource komprimiert ist, wird in der Regel dieser Header auf `gzip` , `deflate` oder gesetzt `br` .  Eine Erläuterung dieser Werte finden Sie unter [Direktiven][MDNContentEncodingDirectives] .  

Genug mit den Erläuterungen.  Zeit, einige Änderungen vorzunehmen!  Aktivieren Sie die Text Komprimierung, indem Sie ein paar Codezeilen hinzufügen:  

1.  Klicken Sie auf der Registerkarte Editor auf **server.js**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="server.js bearbeiten" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       Bearbeiten `server.js`  
    :::image-end:::  
    
1.  Fügen Sie **server.js**den folgenden Code hinzu.  Stellen Sie sicher, dass Sie dies tun `app.use(compression())` `app.use(express.static('build'))` .  

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
    > In der Regel müssen Sie das `compression` Paket über einen ähnlichen `npm i -S compression` Vorgang installieren, dies wurde aber bereits für Sie erledigt.  
    
1.  Warten Sie, bis glitch den neuen Build der Website bereitgestellt hat.  Die raffinierte Animation neben **Tools** bedeutet, dass die Website neu erstellt und erneut bereitgestellt wird.  Die Änderung ist fertig, wenn die Animation neben **Tools** verschwindet.  Wählen Sie wieder **in einem neuen Fenster** **anzeigen** und auswählen aus.  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
Verwenden Sie die zuvor gelernten Workflows, um manuell zu überprüfen, ob die Komprimierung funktioniert:  

1.  Wechseln Sie zur Registerkarte Demo zurück, und laden Sie die Seite neu.  In der Spalte **Größe** sollten nun zwei unterschiedliche Werte für Textressourcen wie angezeigt werden `bundle.js` .  In der folgenden Abbildung ist der oberste Wert von für die `256 KB` Größe der Datei, die `bundle.js` über das Netzwerk gesendet wurde, und der untere Wert von `1.2 MB` ist die unkomprimierte Dateigröße.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="In der Spalte "Größe" werden nun zwei unterschiedliche Werte für Textressourcen angezeigt." lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       In der Spalte " **Größe** " werden nun zwei unterschiedliche Werte für Textressourcen angezeigt.  
    :::image-end:::  
    
1.  Im Abschnitt " **Antwort Kopfzeilen** " `bundle.js` sollte nun eine `content-encoding: gzip` Kopfzeile enthalten sein.
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="Der Abschnitt "Antwort Kopfzeilen" enthält jetzt einen Inhalts Codierungs Header." lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       Der Abschnitt " **Antwort Kopfzeilen** " enthält jetzt einen Inhalts Codierungs Header.  
    :::image-end:::  
    
Überwachen Sie die Seite erneut, um zu messen, welche Art von Auswirkungen die Text Komprimierung auf die Ladeleistung der Seite hat:  

1.  Wählen Sie die Registerkarte **Audits** aus.  
1.  Wählen Sie **Audit durchführen** \ ( ![ Audit durchführen ][ImagePerformIcon] \) aus.  
1.  Belasse die Einstellungen wie zuvor.  
1.  Wählen Sie **Audit ausführen**aus.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach der Aktivierung der Text Komprimierung" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       Ein Überwachungsbericht nach der Aktivierung der Text Komprimierung  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  Ihr Gesamtleistungsfaktor sollte zugenommen haben, was bedeutet, dass die Website schneller wird.  

#### Text Komprimierung in der realen Welt   

Bei den meisten Servern gibt es wirklich einfache Fehlerbehebungen wie diese zum Aktivieren von Komprimierung!  Führen Sie einfach eine Suche durch, um zu konfigurieren, welcher Server zum Komprimieren von Text verwendet wird.  

### Ändern der Größe von Bildern   

Ihr Bericht weist darauf hin, dass die Vermeidung enormer Netzwerklasten eine der besten Möglichkeiten zur Verbesserung der Leistung der Seite darstellt.  Durch Ändern der Größe von Bildern kann die Größe der Netzwerk Nutzlast verringert werden.  Wenn der Benutzer Ihre Bilder auf einem Bildschirm mit einem mobilen Gerät anzeigt, der 500 Pixel breit ist, ist es wirklich unwichtig, ein 1500-Pixel breites Bild zu senden.  Im Idealfall senden Sie höchstens ein Bild mit einer Breite von 500 Pixel.  

1.  Klicken Sie in Ihrem Bericht auf **enorme Netzwerk Nutzlasten vermeiden** , um festzustellen, welche Bilder geändert werden sollen.  Es sieht so aus, als ob 2 der JPG-Dateien über 2000 KB liegen, was größer als notwendig ist.  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  Zurück auf der Registerkarte "Editor" Öffnen `src/model.js` .  
1.  Ersetzen Sie `const dir = 'big'` durch `const dir = 'small'`.  Dieses Verzeichnis enthält Kopien der gleichen Bilder, deren Größe geändert wurde.  
1.  Überprüfen Sie die Seite erneut, um zu sehen, wie sich diese Änderung auf die Ladeleistung auswirkt.  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach dem Ändern der Größe von Bildern" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       Ein Überwachungsbericht nach dem Ändern der Größe von Bildern  
    :::image-end:::  
    
Sieht so aus, als ob die Änderung nur eine geringfügige Auswirkung auf den Gesamtleistungsfaktor hat.  Die Punktzahl zeigt jedoch nicht eindeutig, wie viel Netzwerkdaten Sie für Ihre Benutzer speichern.  Die Gesamtgröße der alten Fotos betrug etwa 5,3 Megabyte, während es jetzt nur noch etwa 0,18 Megabytes gibt.  

#### Ändern der Größe von Bildern in der realen Welt   

Bei einer kleinen app kann eine einmalige Größenänderung so gut wie möglich sein.  Bei einer umfangreichen APP ist dies natürlich nicht skalierbar.  Im folgenden finden Sie einige Strategien zum Verwalten von Bildern in umfangreichen apps:  

*   Ändern der Größe von Bildern während des Buildprozesses  
*   Erstellen Sie mehrere Größen der einzelnen Bilder während des Buildprozesses, und verwenden `srcset` Sie Sie dann in Ihrem Code.  Zur Laufzeit sorgt der Browser dafür, welche Größe für das Gerät am besten geeignet ist.  
    <!--See [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   Verwenden Sie ein Image CDN, mit dem Sie die Größe eines Bilds dynamisch ändern können, wenn Sie es anfordern.  
*   Optimieren Sie zumindest jedes Bild.  Dies kann zu enormen Einsparungen führen.  
  Optimierung ist, wenn Sie ein Bild über ein spezielles Programm ausführen, das die Größe der Bilddatei reduziert.  Weitere Tipps finden Sie unter [grundlegende Bildoptimierung][EssentialImageOptimization] .  
    
### Eliminieren von Render-Blockierungs Ressourcen   

Ihr neuester Bericht besagt, dass das Eliminieren von Render-Blockierungs Ressourcen jetzt die größte Chance darstellt.  

Eine Render-Blockierungs Ressource ist eine externe JavaScript-oder CSS-Datei, die vom Browser heruntergeladen, analysiert und ausgeführt werden muss, bevor die Seite angezeigt wird.  Das Ziel besteht darin, nur den zentralen CSS-und JavaScript-Code auszuführen, der erforderlich ist, um die Seite ordnungsgemäß anzuzeigen.  

Die erste Aufgabe besteht darin, Code zu finden, den Sie beim Laden der Seite nicht ausführen müssen.  

1.  Wählen Sie **Render-Blockierungs Ressourcen eliminieren** aus, um die blockierten Ressourcen anzuzeigen:  
    `lodash.js` und `jquery.js` .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Weitere Informationen zur Möglichkeit zum Eliminieren von Render-Blockierungs Ressourcen" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       Weitere Informationen zur Möglichkeit zum **eliminieren von Render-Blockierungs Ressourcen**  
    :::image-end:::  
    
1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen, mit der Eingabe zu beginnen `Coverage` , und wählen Sie dann **Coverage anzeigen**aus.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Öffnen des Befehlsmenüs im Überwachungs Panel" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       Öffnen des Befehlsmenüs im **Überwachungs** Panel  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="Die Registerkarte "Coverage"" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       Die Registerkarte " **Coverage** "  
    :::image-end:::  
    
1.  Wählen Sie **Aktualisieren** \ ( ![ aktualisieren ][ImageRefreshIcon] \) aus.  Die Registerkarte **Coverage** bietet eine Übersicht darüber, wie viel des Codes in `bundle.js` , `jquery.js` und `lodash.js` ausgeführt wird, während die Seite geladen wird.  In der folgenden Abbildung werden etwa 76% und 30% der jQuery-und Lodash-Dateien nicht verwendet.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="Der Bericht "Berichterstattung"" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       Der Bericht "Berichterstattung"  
    :::image-end:::  
    
1.  Wählen Sie die Zeile **jquery.js** aus.  DevTools öffnet die Datei im Quellen Panel.  Eine Codezeile wird ausgeführt, wenn Sie einen blauen Balken Daneben hat.  Eine rote Leiste bedeutet, dass Sie nicht ausgeführt wurde und beim Laden der Seite definitiv nicht benötigt wird.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Anzeigen der jQuery-Datei im Quellen Panel" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       Anzeigen der jQuery-Datei im **Quellen** Panel  
    :::image-end:::  
    
1.  Scrollen Sie ein wenig durch den jQuery-Code.  Einige der Zeilen, die "Run" erhalten, sind eigentlich nur Kommentare.  Wenn Sie diesen Code über einen minifier ausführen, der Kommentare entfernt, ist eine weitere Möglichkeit, die Größe dieser Datei zu verringern.  

Kurz gesagt: Wenn Sie mit Ihrem eigenen Code arbeiten, können Sie mithilfe der Registerkarte Coverage Ihren Code, Zeile für Zeile, analysieren und nur den Code versenden, der für die Seitenauslastung benötigt wird.  

Sind die `jquery.js` und `lodash.js` Dateien auch zum Laden der Seite erforderlich?  Auf der Registerkarte Anforderungs Blockierung wird angezeigt, was geschieht, wenn keine Ressourcen verfügbar sind.  

1.  Wählen Sie die Registerkarte **Netzwerk** aus.  
1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü erneut zu öffnen.  
1.  Beginnen `blocking` Sie mit der Eingabe, und wählen Sie dann **Anforderungs Blockierung anzeigen**aus.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="Die Registerkarte ' Anforderungs Blockierung '" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       Die Registerkarte ' **Anforderungs Blockierung** '  
    :::image-end:::  
    
1.  Wählen Sie **Muster hinzufügen** \ ( ![ Muster hinzufügen ][ImageAddPatternIcon] ) aus, geben Sie ein `/libs/*` , und drücken Sie dann `Enter` , um zu bestätigen.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Hinzufügen eines Musters, um jede Anforderung an das libs-Verzeichnis zu blockieren" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       Hinzufügen eines Musters zum Blockieren einer Anforderung an das `libs` Verzeichnis  
    :::image-end:::  
    
1.  Aktualisieren Sie die Seite.  Die Anforderungen für jQuery und Lodash sind rot, was bedeutet, dass die Anforderungen blockiert wurden.   Da die Seite immer noch geladen und interaktiv ist, sieht es so aus, als ob diese Ressourcen überhaupt nicht benötigt werden.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="Das Netzwerk Panel zeigt, dass die Anforderungen blockiert wurden." lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       Das **Netzwerk** Panel zeigt, dass die Anforderungen blockiert wurden.  
    :::image-end:::  
    
1.  Wählen Sie **alle Muster entfernen** \ ( ![ alle Muster entfernen ][ImageRemoveIcon] \) aus, um das `/libs/*` Blockierungs Muster zu löschen.  
    
Im Allgemeinen ist die Registerkarte Anforderungs Blockierung hilfreich, um zu simulieren, wie sich die Seite verhält, wenn eine bestimmte Ressource nicht verfügbar ist.  

Entfernen Sie nun die Verweise auf diese Dateien aus dem Code, und überwachen Sie die Seite erneut:  

1.  Zurück auf der Registerkarte "Editor" Öffnen `template.html` .  
1.  Löschen Sie `<script src="/libs/lodash.js">` und `<script src="/libs/jquery.js"></script>`.  
1.  Warten Sie, bis die Website neu erstellt und erneut bereitgestellt wird.  
1.  Überwachen Sie die Seite im **Überwachungs** Panel erneut.  Ihre Gesamtpunktzahl sollte erneut verbessert werden.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach dem Entfernen der Render-Blockierungs Ressourcen" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       Ein **Überwachungs** Bericht nach dem Entfernen der Render-Blockierungs Ressourcen  
    :::image-end:::  
    
#### Optimieren des kritischen Rendering-Pfads in der realen Welt   

Der **kritische Rendering-Pfad** bezieht sich auf den Code, der zum Laden einer Seite erforderlich ist.  Im Allgemeinen können Sie die Seitenauslastung beschleunigen, indem Sie nur den Versand von kritischem Code während des Ladens der Seite durchführen und dann alles andere verzögert laden.  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   Es ist unwahrscheinlich, dass Sie in der Lage sind, Skripts zu finden, die Sie direkt entfernen können, aber möglicherweise viele Skripts finden, die Sie beim Laden der Seite nicht anfordern müssen, und stattdessen möglicherweise asynchron angefordert werden.  <!--See [Using async or defer][async].  -->  
*   Wenn Sie ein Framework verwenden, überprüfen Sie, ob es einen Produktionsmodus aufweist.  In diesem Modus wird möglicherweise ein Feature wie das [schütteln von Strukturen][WebpackTreeShaking] verwendet, um unnötigen Code zu eliminieren, der das kritische Rendern blockiert.  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### Arbeiten mit einem geringeren Hauptthread   

Ihr neuester Bericht zeigt einige kleinere potenzielle Einsparungen im Abschnitt "Verkaufschancen", aber wenn Sie im Abschnitt "Diagnose" nach unten suchen, sieht es so aus, als wäre der größte Engpass zu viel Hauptthread Aktivität.  

Der Hauptthread ist der Ort, an dem der Browser die meiste Arbeit ausführt, die zum Anzeigen einer Seite erforderlich ist, beispielsweise das analysieren und Ausführen von HTML, CSS und JavaScript.  

Das Ziel besteht darin, mithilfe des Leistungs Panels zu analysieren, welche Arbeit der Hauptthread beim Laden der Seite unternimmt, und Wege zu finden, um unnötige Arbeit zu verzögern oder zu entfernen.  

1.  Wählen Sie die Registerkarte **Leistung** aus.  
1.  Wählen Sie **aufnahmeeinstellungen** \ ( ![ Aufnahmeeinstellungen ][ImageCaptureIcon] \) aus.  
1.  **Netzwerk** auf **langsame 3G** -und **CPU** -zu- **6x-Verlangsamung**einstellen.  Bei mobilen Geräten gibt es in der Regel mehr Hardwareeinschränkungen als Laptops oder Desktops, sodass Sie mit diesen Einstellungen das Laden der Seite so erleben können, als ob Sie ein weniger leistungsfähiges Gerät verwenden würden.  
1.  Wählen Sie **Aktualisieren** \ ( ![ aktualisieren ][ImageRefreshIcon] \) aus.  DevTools aktualisiert die Seite und erstellt dann eine Visualisierung aller ausgeführten Arbeiten, um die Seite zu laden.  Diese Visualisierung wird als **Ablaufverfolgung**bezeichnet.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Der Leistungs Panel-Ablaufverfolgung der Seitenauslastung" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       Der **Leistungs** Panel-Ablaufverfolgung der Seitenauslastung  
    :::image-end:::  
    
Die Ablaufverfolgung zeigt die Aktivität chronologisch an, von links nach rechts.  Die oben dargestellten fps-, CPU-und net-Diagramme geben Ihnen einen Überblick über Frames pro Sekunde, CPU-Aktivität und Netzwerkaktivität.  Der gelb markierte Block, der in der Abbildung nachfolgend angezeigt wird, war die CPU vollständig mit Skriptaktivitäten ausgelastet.  Dies ist ein Hinweis darauf, dass Sie möglicherweise die Seitenauslastung beschleunigen können, indem Sie eine geringere JavaScript-Arbeit durchführen.  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="Der Abschnitt "Übersicht" der Ablaufverfolgung" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   Der Abschnitt "Übersicht" der Ablaufverfolgung  
:::image-end:::  

Untersuchen Sie die Ablaufverfolgung, um Möglichkeiten für eine geringere JavaScript-Arbeit zu finden:  

1.  Wählen Sie den Abschnitt **Anzeige** dauern aus, um ihn zu erweitern.  Basierend auf der Tatsache, dass es möglicherweise eine Reihe von [Timings][MDNUserTimingApi] -Maßnahmen von reagieren gibt, scheint es so zu sein, als ob die APP von Tony die Entwicklungsmethode von reagieren verwendet.  Wenn Sie auf den Produktionsmodus von reagieren umstellen, kann dies einige einfache Leistungsgewinne hervorbringen.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="Abschnitt "Anzeigedauern"" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       Abschnitt " **Anzeige** dauern"  
    :::image-end:::  
    
1.  Wählen Sie erneut **Anzeige** dauern aus, um den Abschnitt zu reduzieren.  
1.  Durchsuchen Sie den **Haupt** Abschnitt.  Dieser Abschnitt zeigt ein chronologisches Protokoll der Hauptthread Aktivität, von links nach rechts.  Die y-Achse (von oben nach unten) zeigt, warum Ereignisse aufgetreten sind.  In der figyre nach dem folgenden Beispiel hat das Ereignis zum Ausführen der Funktion geführt, die zur Ausführung führte, die `Evaluate Script` `(anonymous)` `(anonymous)` `__webpack__require__` zum Ausführen führte usw.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Der Hauptabschnitt" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       Der **Haupt** Abschnitt  
    :::image-end:::  
    
1.  Scrollen Sie nach unten zum unteren Rand des **Haupt** Abschnitts.  Wenn Sie ein Framework verwenden, wird der größte Teil der oberen Aktivität durch das Framework verursacht, das normalerweise außerhalb des Steuerelements liegt.  Die von Ihrer APP verursachte Aktivität befindet sich normalerweise unten.  In dieser app scheint es so zu sein, dass eine Funktion mit dem Namen `App` viele Anforderungen an eine `mineBitcoin` Funktion verursacht.  Es klingt wie Tony könnte die Geräte seiner Fans verwenden, um cryptocurrency zu vergruben...  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Zeigen Sie auf die mineBitcoin-Aktivität." lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       Zeigen Sie auf die `mineBitcoin` Aktivität.  
    :::image-end:::  
    
    > [!NOTE]
    > Obwohl die Anforderungen, die Ihr Framework macht, in der Regel nicht in Ihrem Steuerelement enthalten sind, können Sie Ihre APP manchmal so strukturieren, dass das Framework ineffizient ausgeführt wird.  Die Umstrukturierung ihrer App zur effizienten Verwendung des Frameworks ist eine Möglichkeit, um die Arbeit am Hauptthread zu verkürzen.  Dies erfordert jedoch ein umfassendes Verständnis der Funktionsweise des Frameworks und der Art von Änderungen, die Sie in Ihrem eigenen Code vornehmen, um das Framework effizienter zu verwenden.  
    
1.  Erweitern Sie den Abschnitt **Bottom-up** .  Auf dieser Registerkarte wird aufgeschlüsselt, welche Aktivitäten die meiste Zeit in Anspruch genommen haben.  Wenn im Abschnitt Bottom-up nichts angezeigt wird, klicken Sie auf die Beschriftung für **Haupt** Abschnitt.  Der **Bottom-up-** Abschnitt zeigt nur Informationen zu einer beliebigen Aktivität oder Aktivitätsgruppe, die Sie aktuell ausgewählt haben.  Wenn Sie beispielsweise auf eine der Aktivitäten geklickt haben `mineBitcoin` , werden im Abschnitt **Bottom-up** nur Informationen für diese Aktivität angezeigt.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="Die Registerkarte "Bottom-up"" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       Die Registerkarte " **Bottom-up** "  
    :::image-end:::  
    
In der Spalte **selbst Zeit** wird angezeigt, wie viel Zeit direkt in den einzelnen Aktivitäten aufgewendet wurde.  In der folgenden Abbildung wurden etwa 63% der Hauptthread Zeit für die Funktion aufgewendet `mineBitcoin` .  

Zeit, um zu sehen, ob die Auslastung der Seite durch Verwenden des Produktionsmodus und verringern der JavaScript-Aktivität beschleunigt werden kann.  Beginnen mit dem Produktionsmodus:  

1.  Öffnen Sie auf der Registerkarte Editor den Reiter `webpack.config.js` .  
1.  Ändern Sie `"mode":"development"` in `"mode":"production"`.  
1.  Warten Sie, bis der neue Build bereitgestellt wird.  
1.  Überwachen Sie die Seite erneut.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach der Konfiguration von WebPack für die Verwendung des Produktionsmodus" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       Ein Überwachungsbericht nach der Konfiguration von WebPack für die Verwendung des Produktionsmodus  
    :::image-end:::  
    
Reduzieren Sie die JavaScript-Aktivität, indem Sie die Anforderung entfernen an `mineBitcoin` :  

1.  Öffnen Sie auf der Registerkarte Editor den Reiter `src/App.jsx` .  
1.  Kommentieren Sie die Anforderung `this.mineBitcoin(1500)` in `constructor` .  
1.  Warten Sie, bis der neue Build bereitgestellt wird.  
1.  Überwachen Sie die Seite erneut.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach dem Entfernen unnötiger JavaScript-Arbeit" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       Ein Überwachungsbericht nach dem Entfernen unnötiger JavaScript-Arbeit  
    :::image-end:::  
    
Sieht so aus, als ob diese letzte Änderung einen massiven Sprung in der Leistung verursacht hat!  

> [!NOTE]
> Dieser Abschnitt enthält eine relativ kurze Einführung in das Leistungs Panel.  Weitere Informationen zum Analysieren der Seitenleistung finden Sie unter [Referenz zur Leistungsanalyse][DevtoolsEvaluatePerformanceReference] .  

<!--todo: add section when available -->  

#### Arbeiten mit einem niedrigeren Hauptthread in der realen Welt   

Im Allgemeinen ist der Bereich " **Leistung** " die häufigste Methode, um zu verstehen, welche Aktivitäten Ihre Website während der Auslastung durchführt, und Möglichkeiten zum Entfernen unnötiger Aktivitäten zu finden.  

Wenn Sie einen Ansatz bevorzugen, der sich eher wie anfühlt `console.log()` , können Sie mit der API für die [Benutzersteuerung][MDNUserTimingApi] bestimmte Phasen des App-Lebenszyklus willkürlich kennzeichnen, um zu verfolgen, wie lange diese Phasen dauern.  

## Zusammenfassung   

*   Wenn Sie die Auslastungs Leistung einer Website optimieren möchten, beginnen Sie immer mit einer Überwachung.  Mit der Überprüfung wird ein Basisplan erstellt, und Sie erhalten Tipps zum verbessern.  
*   Führen Sie jeweils eine Änderung durch, und überprüfen Sie die Seite nach jeder Änderung, um zu sehen, wie sich diese isolierte Änderung auf die Leistung auswirkt.  

<!--
## Next steps   

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

<!--  
  


-->  

<!-- image links -->  

[ImageAddPatternIcon]: ../media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: ../media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: ../media/more-panels-icon.msft.png  
[ImagePerformIcon]: ../media/perform-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  
[ImageRemoveIcon]: ../media/remove-icon.msft.png  
<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Referenz zur Leistungsanalyse | Microsoft docs"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Einführung in die Webentwicklungs Klasse | Coursera"  

[EssentialImageOptimization]: https://images.guide "Essentielle Bildoptimierung"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Direktiven – Inhaltscodierung | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "Benutzer-Timing-API | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Baum Erschütterung | WebPack"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
