---
title: Optimieren der Website Geschwindigkeit mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 7efc76fbcb3d1ed6cbd0760f789c8c952030d70c
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611889"
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

> ##### Abbildung1  
> Tony the Cat  
> ![Tony the Cat][ImageTony]  

## Schritt 1: Überwachen der Website   

Wenn Sie die Ladeleistung einer Website verbessern möchten, **beginnen Sie immer mit einer Überwachung**.  
Das Audit hat zwei wichtige Funktionen:  

*   Sie erstellt einen **Basisplan** , in dem Sie nachfolgende Änderungen messen können.  
*   Es gibt Ihnen **umsetzbare Tipps** , welche Änderungen die meisten Auswirkungen haben.  

### Einrichtung   

Zunächst müssen Sie die Website so einrichten, dass Sie später Änderungen daran vornehmen können.  

1.  [Öffnen Sie den Quellcode für die Website](https://glitch.com/edit/#!/tony).  Diese Registerkarte wird als **Registerkarte "Editor"** bezeichnet.  
    
    > ##### Abbildung2  
    > Die Registerkarte "Editor"  
    > ![Die Registerkarte "Editor"][ImageEditor]  

1.  Wählen Sie **Tony**aus.  Ein Menü wird angezeigt.  
    
    > ##### Abbildung 3  
    > Das Menü, das nach dem Klicken auf " **Tony** " angezeigt wird  
    > ![Das Menü, das nach dem Klicken auf "Tony" angezeigt wird][ImageMenu]  
    
1.  Wählen Sie **Remix Project**aus.  Der Name des Projekts wechselt von **Tony** zu einem zufällig generierten Namen.  Sie haben jetzt eine eigene bearbeitbare Kopie des Codes.  Später können Sie Änderungen an diesem Code vornehmen.  
1.  Wählen Sie **in einem neuen Fenster** **anzeigen** und auswählen aus.  Die Demo wird in einer neuen Registerkarte geöffnet.  Diese Registerkarte wird als **Registerkarte Demo**bezeichnet.  Das Laden der Website kann einige Zeit in Anspruch nehmen.  
    
    > ##### Abbildung4  
    > Die Registerkarte "Demo"  
    > ![Die Registerkarte "Demo"][ImageDemo]  

1.  Drücken Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \).  Microsoft Edge devtools wird parallel zur Demo geöffnet.  
    
    > ##### Abbildung5  
    > DevTools und die Demo  
    > ![DevTools und die Demo][ImageDevtools]  

Für die restlichen Screenshots in diesem Lernprogramm wird devtools in einem separaten Fenster angezeigt.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen, einzugeben `Undock` , und wählen Sie dann **in separates Fenster Abdocken**aus.  

> ##### Abbildung6  
> Nicht angedockte devtools  
> ![Nicht angedockte devtools][ImageUndocked]  

### Festlegen eines Basisplans   

Der Basisplan ist eine Aufzeichnung der Vorgehensweise der Website, bevor Sie Leistungsverbesserungen durchgeführt haben.  

1.  Wählen Sie die Registerkarte **Audits** aus.  **Die** ![ Schaltfläche "Weitere Panels" ist möglicherweise ausgeblendet ][ImageMorePanelsIcon] .  Auf diesem Panel befindet sich ein Leuchtturm, weil das Projekt, das das Audit Panel anbietet, den Namen **Lighthouse**trägt.  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    > ##### Abbildung7  
    > Überwachungs Panel  
    > ![Überwachungs Panel][ImageAudits]  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  Vergleichen Sie Ihre Überwachungs Konfigurationseinstellungen mit denen in [Abbildung 7](#figure-7).  Nachfolgend finden Sie eine Erläuterung der verschiedenen Optionen:  

    *   **Gerät**aus.  Wenn Sie auf **Mobile** festlegen, ändert sich die Zeichenfolge des Benutzer-Agents und simuliert ein mobiles Viewport.  Durch die Einstellung auf den **Desktop** werden die **mobilen** Änderungen so ziemlich deaktiviert.  
    *   **Audits**.  Durch das Deaktivieren einer Kategorie wird verhindert, dass der Überwachungsbereich diese Audits ausführt, und diese Audits werden aus dem Bericht ausgeschlossen.  Lassen Sie die anderen Kategorien aktiviert, wenn Sie die Typen von Empfehlungen anzeigen möchten, die bereitgestellt werden.  Das Deaktivieren von Kategorien beschleunigt den Überwachungsvorgang etwas.  
    *   **Einschränkung**.  Einstellung auf **simulierte langsame 4G, vierfache CPU-Verlangsamung** simuliert die typischen Bedingungen für das Browsen auf einem mobilen Gerät.  Sie wird als "simuliert" bezeichnet, da das Überwachungs Panel während des Überwachungsprozesses nicht tatsächlich gedrosselt wird.  Stattdessen wird nur extrapoliert, wie lange es dauert, bis die Seite unter mobilen Bedingungen geladen wurde.  Mit der Einstellung " **angewendet...** " wird dagegen Ihre CPU und Ihr Netzwerk tatsächlich gedrosselt, mit dem Kompromiss eines längeren Überwachungsprozesses.  
    *   **Speicher löschen**.  Wenn Sie dieses Kontrollkästchen aktivieren, wird vor jeder Überwachung der gesamte Speicherplatz gelöscht, der der Seite zugeordnet ist.  Belasse diese Einstellung, wenn Sie überprüfen möchten, wie die Besucher Ihrer Website erst einmal auftreten.  Deaktivieren Sie diese Einstellung, wenn Sie die Wiederholungs Besuchs Erfahrung wünschen.  

1.  Wählen Sie **Audits ausführen**aus.  Nach 10 bis 30 Sekunden wird im Überwachungs Panel ein Bericht über die Leistung der Website angezeigt.  
    
    > ##### Abbildung8  
    > Der Bericht für das Audits-Panel über die Leistung der Website  
    > ![Der Bericht für das Audits-Panel über die Leistung der Website][ImageReport]  

#### Behandeln von Berichts Fehlern   

Wenn Sie in Ihrem Audits-Panel-Bericht jemals eine Fehlermeldung erhalten, versuchen Sie, die Registerkarte Demo in einem **InPrivate** -Fenster auszuführen, ohne dass weitere Registerkarten geöffnet sind.  Dadurch wird sichergestellt, dass Sie Microsoft Edge in einem sauberen Zustand ausführen.  Insbesondere Microsoft-Edge-Erweiterungen stören häufig den Überwachungsprozess.  

<!--todo: add screen capture for error in audit -->  
<!--
> ##### old Figure 9  
> A report that errored  
> ![A report that errored][ImageError]  
-->  

### Grundlegendes zu Ihrem Bericht   

Die Zahl am oberen Rand des Berichts entspricht dem Gesamtleistungsfaktor für die Website.  Wenn Sie später Änderungen am Code vornehmen, sollte diese Zahl steigen.  Eine höhere Punktzahl bedeutet eine bessere Leistung.  

> ##### Abbildung 9  
> Der Gesamtleistungsfaktor  
> ! [Der Gesamtleistungsfaktor] [Imagegesamt]  

Der Abschnitt **Metriken** bietet quantitative Maße für die Leistung der Website.  Jede Metrik bietet Einblicke in einen anderen Aspekt der Leistung.  Beispielsweise erfahren Sie in der **ersten Inhaltsfarbe** , wann Inhalte zuerst auf dem Bildschirm gemalt werden, was ein wichtiger Meilenstein für die Wahrnehmung der Seitenauslastung durch den Benutzer ist, während die **Zeit für interaktive** Kennzeichnung den Punkt angibt, an dem die Seite für die Behandlung von Benutzerinteraktionen bereit angezeigt wird.  

> ##### Abbildung 10  
> Abschnitt "Metriken"  
> ! [Der Abschnitt ' Metriken '] [Imagemetrics]  

Wählen Sie in [Abbildung 11](#figure-11) die hervorgehobene Umschaltfläche aus, um eine Beschreibung für jede Metrik anzuzeigen, und klicken Sie auf **Weitere Informationen** , um die Dokumentation dazu zu lesen.  

> ##### Abbildung 11  
> Auswählen der hervorgehobenen Umschaltfläche zum Erweitern der **Metriken** Elemente  
> ! [Wählen Sie die hervorgehobene Umschaltfläche aus, um die Elemente für Metriken zu erweitern] [ImageFirstMeaningfulPaint]  

Unter Metriken finden Sie eine Sammlung von Screenshots, die Ihnen zeigen, wie die Seite beim Laden aussah.  

> ##### Abbildung 12  
> Screenshots, wie die Seite beim Laden aussah  
> ! [Screenshots, wie die Seite während des Ladens aussah] [Imagescreenshots]  

Im Abschnitt " **Verkaufschancen** " finden Sie spezielle Tipps zum Verbessern der Auslastungs Leistung dieser bestimmten Seite.  

> ##### Abbildung 13  
> Der Abschnitt "Verkaufschancen"  
> ! [Der Abschnitt "Verkaufschancen"] [Imageopportunities]  

Wählen Sie eine Gelegenheit aus, um mehr darüber zu erfahren.  

> ##### Abbildung 14  
> **Eliminieren von Render-Blockierungs Ressourcen**  
> ! [Eliminieren der Render-Blockierung von Ressourcen – Opportunity] [Imagekomprimierung]  

Wählen Sie **Weitere Informationen** aus, um die Dokumentation dazu anzuzeigen, warum eine Verkaufschance wichtig ist, und spezifische Empfehlungen zur Behebung.  

> ##### Abbildung 15  
> Dokumentation für die Möglichkeit zum **eliminieren von Render-Blockierungs Ressourcen**  
> ! [Dokumentation für die Möglichkeit zum Eliminieren von Render-Blockierungs Ressourcen] [Imagereference]  

Der Abschnitt **Diagnostics** enthält weitere Informationen zu Faktoren, die zur Ladezeit der Seite beitragen.  

> ##### Abbildung 16  
> Abschnitt "Diagnose"  
> ! [Der Abschnitt Diagnose] [Imagediagnostics]  

Im Abschnitt "übertragene **Prüfungen** " wird gezeigt, was die Website richtig macht.  Wählen Sie diese Option aus, um den Abschnitt zu erweitern.  

> ##### Abbildung 17  
> Abschnitt "übergebene Überprüfungen"  
> ! [Der Abschnitt ' übertragene Audits] [Imagepassed]  

## Schritt 2: experimentieren   

Im Abschnitt "Verkaufschancen" Ihres Überwachungsberichts erhalten Sie Tipps, wie Sie die Leistung der Seite verbessern können.  In diesem Abschnitt implementieren Sie die empfohlenen Änderungen an der CodeBase, indem Sie die Website nach jeder Änderung überwachen, um zu messen, wie sich dies auf die Geschwindigkeit der Website auswirkt.  

### Aktivieren der Text Komprimierung   

Ihr Bericht besagt, dass die Vermeidung von enormen Netzwerklasten eine der besten Möglichkeiten zur Verbesserung der Leistung der Seite darstellt.  Das Aktivieren der Text Komprimierung bietet die Möglichkeit, die Leistung der Seite zu verbessern.  

Die Text Komprimierung erfolgt, wenn Sie die Größe einer Textdatei reduzieren oder komprimieren, bevor Sie Sie über das Netzwerk senden.  Eine Art gefällt Ihnen, wie Sie einen Ordner komprimieren können, bevor Sie ihn per e-Mail senden, um die Größe zu verringern.  

Bevor Sie die Komprimierung aktivieren, gibt es eine Reihe von Möglichkeiten, um manuell zu überprüfen, ob Textressourcen komprimiert werden.  

1.  Wählen Sie die Registerkarte **Netzwerk** aus.  
    
    > ##### Abbildung 18  
    > Netzwerk Panel  
    > ! [Netzwerk Panel] [Imagenetwork]  
    
1.  Wählen Sie das Symbol **Netzwerkeinstellung** aus.  
1.  Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** .  Die Höhe der Zeilen in der Tabelle der Netzwerkanforderungen nimmt zu.  
    
    > ##### Abbildung 19  
    > Große Zeilen in der Tabelle "Netzwerkanforderungen"  
    > ! [Große Zeilen in der Tabelle ' Netzwerkanforderungen '] [ImageLargeRows]  
    
1.  Wenn die Spalte **Größe** in der Tabelle der Netzwerkanforderungen nicht angezeigt wird, klicken Sie auf die Tabellenüberschrift, und wählen Sie dann **Größe**aus.  

Jede **Größen** Zelle enthält zwei Werte.  Der oberste Wert ist die Größe der heruntergeladenen Ressource.  
Der untere Wert gibt die Größe der unkomprimierten Ressource an.  Wenn die beiden Werte identisch sind, wird die Ressource nicht komprimiert, wenn Sie über das Netzwerk gesendet wird.  In [Abbildung 19](#figure-19) finden Sie beispielsweise die oberen und unteren Werte für " `bundle.js` sind" und " `1.2 MB` `1.2 MB` .  

Überprüfen Sie auf Komprimierung, indem Sie die HTTP-Header einer Ressource prüfen:  

1.  Wählen Sie **Bundle. js**aus.  
1.  Wählen Sie die Registerkarte über **Schriften** aus.  
    
    > ##### Abbildung 20  
    > Die Registerkarte "Überschriften"  
    > ! [Die Registerkarte ' Überschriften '] [Imageheaders]  
    
1.  Durchsuchen Sie den Abschnitt **Antwort Kopfzeilen** nach einer `content-encoding` Kopfzeile.  Sie sollten keines sehen, was bedeutet, dass es sich nicht um eine `bundle.js` Komprimierung handelt.  Wenn eine Ressource komprimiert ist, wird in der Regel dieser Header auf `gzip` , `deflate` oder gesetzt `br` .  Eine Erläuterung dieser Werte finden Sie unter [Direktiven][MDNContentEncodingDirectives] .  

Genug mit den Erläuterungen.  Zeit, einige Änderungen vorzunehmen!  Aktivieren Sie die Text Komprimierung, indem Sie ein paar Codezeilen hinzufügen:  

1.  Klicken Sie auf der Registerkarte Editor auf **Server. js**.  
    
    > ##### Abbildung 21  
    > Bearbeiten von Server. js  
    > ! [Bearbeiten von Server. js] Helios  
    
1.  Fügen Sie den folgenden Code zu " **Server. js**" hinzu.  Stellen Sie sicher, dass Sie dies tun `app.use(compression())` `app.use(express.static('build'))` .  

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
    > ##### Old Figure 22  
    > The animation that indicates that the site is getting built  
    > ![The animation that indicates that the site is getting built][ImageBuilding]  
    -->  
    
Verwenden Sie die zuvor gelernten Workflows, um manuell zu überprüfen, ob die Komprimierung funktioniert:  

1.  Wechseln Sie zur Registerkarte Demo zurück, und laden Sie die Seite neu.  In der Spalte **Größe** sollten nun zwei unterschiedliche Werte für Textressourcen wie angezeigt werden `bundle.js` .  In [Abbildung 23](#figure-23) ist der oberste Wert von `256 KB` für `bundle.js` die Größe der Datei, die über das Netzwerk gesendet wurde, und der untere Wert von `1.2 MB` ist die unkomprimierte Dateigröße.  
    
    > ##### Abbildung 22  
    > In der Spalte "Größe" werden nun zwei unterschiedliche Werte für Textressourcen angezeigt.  
    > ! [In der Spalte ' Größe ' werden nun zwei unterschiedliche Werte für Textressourcen angezeigt] [Imagerequests]  
    
1.  Im Abschnitt " **Antwort Kopfzeilen** " `bundle.js` sollte nun eine `content-encoding: gzip` Kopfzeile enthalten sein.
    
    > ##### Abbildung 23  
    > Der Abschnitt "Antwort Kopfzeilen" enthält jetzt einen Inhalts Codierungs Header.  
    > ! [Der Abschnitt "Antwort Kopfzeilen" enthält jetzt einen Content-Encoding-Header] [Imagegzip]  
    
Überwachen Sie die Seite erneut, um zu messen, welche Art von Auswirkungen die Text Komprimierung auf die Ladeleistung der Seite hat:  

1.  Wählen Sie die Registerkarte **Audits** aus.  
1.  Wählen Sie Audit durchführen einer Überwachung durch **führen** aus ![ ][ImagePerformIcon] .  
1.  Belasse die Einstellungen wie zuvor.  
1.  Wählen Sie **Audit ausführen**aus.  
    
    > ##### Abbildung 24  
    > Ein Überwachungsbericht nach der Aktivierung der Text Komprimierung  
    > ! [Ein Auditbericht nach der Aktivierung der Text Komprimierung] [ImageReport2]  
    
Woohoo!  Das sieht wie ein Fortschritt aus.  Ihr Gesamtleistungsfaktor sollte zugenommen haben, was bedeutet, dass die Website schneller wird.  

#### Text Komprimierung in der realen Welt   

Bei den meisten Servern gibt es wirklich einfache Fehlerbehebungen wie diese zum Aktivieren von Komprimierung!  Führen Sie einfach eine Suche durch, um zu konfigurieren, welcher Server zum Komprimieren von Text verwendet wird.  

### Ändern der Größe von Bildern   

Ihr Bericht weist darauf hin, dass die Vermeidung enormer Netzwerklasten eine der besten Möglichkeiten zur Verbesserung der Leistung der Seite darstellt.  Durch Ändern der Größe von Bildern kann die Größe der Netzwerk Nutzlast verringert werden.  Wenn der Benutzer Ihre Bilder auf einem Bildschirm mit einem mobilen Gerät anzeigt, der 500 Pixel breit ist, ist es wirklich unwichtig, ein 1500-Pixel breites Bild zu senden.  Im Idealfall senden Sie höchstens ein Bild mit einer Breite von 500 Pixel.  

1.  Klicken Sie in Ihrem Bericht auf **enorme Netzwerk Nutzlasten vermeiden** , um festzustellen, welche Bilder geändert werden sollen.  Es sieht so aus, als ob 2 der JPG-Dateien über 2000 KB liegen, was größer als notwendig ist.  
    
    <!--
    > ##### Old Figure 27  
    > Details about the **Properly size images** opportunity  
    > ![Details about the properly size images opportunity][ImageResize]  
    -->

1.  Zurück auf der Registerkarte "Editor" Öffnen `src/model.js` .  
1.  Ersetzen Sie `const dir = 'big'` durch `const dir = 'small'`.  Dieses Verzeichnis enthält Kopien der gleichen Bilder, deren Größe geändert wurde.  
1.  Überprüfen Sie die Seite erneut, um zu sehen, wie sich diese Änderung auf die Ladeleistung auswirkt.  
    
    > ##### Abbildung 25  
    > Ein Überwachungsbericht nach dem Ändern der Größe von Bildern  
    > ! [Ein Überwachungsbericht nach dem Ändern der Größe von Bildern] [ImageReport3]  

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
    
    > ##### Abbildung 26  
    > Weitere Informationen zur Möglichkeit zum **eliminieren von Render-Blockierungs Ressourcen**  
    > ! [Weitere Informationen über die Möglichkeit zum Eliminieren von Render-Blockierungs Ressourcen] [Imagerender]  
    
1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen, mit der Eingabe zu beginnen `Coverage` , und wählen Sie dann **Coverage anzeigen**aus.  
    
    > ##### Abbildung 27  
    > Öffnen des Befehlsmenüs im Überwachungs Panel  
    > ! [Öffnen des Befehlsmenüs im Überwachungs Panel] [ImageCommandMenu]  
    
    > ##### Abbildung 28  
    > Die Registerkarte "Coverage"  
    > ! [Die Registerkarte ' Berichterstattung '] [Imagebelag]  
    
1.  Wählen **Sie Aktualisierung aktualisieren aus** ![ ][ImageRefreshIcon] .  Die Registerkarte **Coverage** bietet eine Übersicht darüber, wie viel des Codes in `bundle.js` , `jquery.js` und `lodash.js` ausgeführt wird, während die Seite geladen wird.  [Abbildung 30](#figure-30) besagt, dass etwa 76% und 30% der jQuery-und Lodash-Dateien nicht verwendet werden.  
    
    > ##### Abbildung 29  
    > Der Bericht "Berichterstattung"  
    > ! [Der Bericht zur Berichterstattung] [ImageCoverageReport]  
    
1.  Wählen Sie die Zeile **jQuery. js** aus.  DevTools öffnet die Datei im Quellen Panel.  Eine Codezeile wird ausgeführt, wenn Sie einen blauen Balken Daneben hat.  Eine rote Leiste bedeutet, dass Sie nicht ausgeführt wurde und beim Laden der Seite definitiv nicht benötigt wird.  
    
    > ##### Abbildung 30  
    > Anzeigen der jQuery-Datei im Quellen Panel  
    > ! [Anzeigen der jQuery-Datei im Quellen Panel] [Imagejquery]  
    
1.  Scrollen Sie ein wenig durch den jQuery-Code.  Einige der Zeilen, die "Run" erhalten, sind eigentlich nur Kommentare.  Wenn Sie diesen Code über einen minifier ausführen, der Kommentare entfernt, ist eine weitere Möglichkeit, die Größe dieser Datei zu verringern.  

Kurz gesagt: Wenn Sie mit Ihrem eigenen Code arbeiten, können Sie mithilfe der Registerkarte Coverage Ihren Code, Zeile für Zeile, analysieren und nur den Code versenden, der für die Seitenauslastung benötigt wird.  

Sind die `jquery.js` und `lodash.js` Dateien auch zum Laden der Seite erforderlich?  Auf der Registerkarte Anforderungs Blockierung wird angezeigt, was geschieht, wenn keine Ressourcen verfügbar sind.  

1.  Wählen Sie die Registerkarte **Netzwerk** aus.  
1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü erneut zu öffnen.  
1.  Beginnen `blocking` Sie mit der Eingabe, und wählen Sie dann **Anforderungs Blockierung anzeigen**aus.  
    
    > ##### Abbildung 31  
    > Die Registerkarte ' Anforderungs Blockierung '  
    > ! [Die Registerkarte ' Anforderungs Blockierung] [Imageblocking]  
    
1.  Wählen Sie **Muster** hinzufügen hinzufügen aus ![ , geben Sie ein ][ImageAddPatternIcon] `/libs/*` , und drücken Sie dann `Enter` , um zu bestätigen.  
    
    > ##### Abbildung 32  
    > Hinzufügen eines Musters zum Blockieren einer Anforderung an das `libs` Verzeichnis  
    > ! [Hinzufügen eines Musters, um eine Anfrage an das libs-Verzeichnis zu blockieren] [Imagelibs]  
    
1.  Aktualisieren Sie die Seite.  Die Anforderungen für jQuery und Lodash sind rot, was bedeutet, dass die Anforderungen blockiert wurden.   Da die Seite immer noch geladen und interaktiv ist, sieht es so aus, als ob diese Ressourcen überhaupt nicht benötigt werden.  
    
    > ##### Abbildung 33  
    > Das Netzwerk Panel zeigt, dass die Anforderungen blockiert wurden.  
    > ! [Das Netzwerk Panel zeigt, dass die Anforderungen blockiert wurden] [ImageBlockedLibs]  
    
1.  Wählen Sie **alle** Muster entfernen aus ![ ][ImageRemoveIcon] , um das `/libs/*` Blockierungs Muster zu löschen.  

Im Allgemeinen ist die Registerkarte Anforderungs Blockierung hilfreich, um zu simulieren, wie sich die Seite verhält, wenn eine bestimmte Ressource nicht verfügbar ist.  

Entfernen Sie nun die Verweise auf diese Dateien aus dem Code, und überwachen Sie die Seite erneut:  

1.  Zurück auf der Registerkarte "Editor" Öffnen `template.html` .  
1.  Löschen Sie `<script src="/libs/lodash.js">` und `<script src="/libs/jquery.js"></script>`.  
1.  Warten Sie, bis die Website neu erstellt und erneut bereitgestellt wird.  
1.  Überwachen Sie die Seite im **Überwachungs** Panel erneut.  Ihre Gesamtpunktzahl sollte erneut verbessert werden.  
    
    > ##### Abbildung 34  
    > Ein Überwachungsbericht nach dem Entfernen der Render-Blockierungs Ressourcen  
    > ! [Ein Überwachungsbericht nach dem Entfernen der Render-Blockierungs Ressourcen] [ImageReport4]  

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
1.  Wählen Sie Einstellungen für Aufnahme **Einstellungen** aus ![ ][ImageCaptureIcon] .  
1.  **Netzwerk** auf **langsame 3G** -und **CPU** -zu- **6x-Verlangsamung**einstellen.  Bei mobilen Geräten gibt es in der Regel mehr Hardwareeinschränkungen als Laptops oder Desktops, sodass Sie mit diesen Einstellungen das Laden der Seite so erleben können, als ob Sie ein weniger leistungsfähiges Gerät verwenden würden.  
1.  Wählen **Sie Aktualisierung aktualisieren aus** ![ ][ImageRefreshIcon] .  DevTools aktualisiert die Seite und erstellt dann eine Visualisierung aller ausgeführten Arbeiten, um die Seite zu laden.  Diese Visualisierung wird als **Ablaufverfolgung**bezeichnet.  
    
    > ##### Abbildung 35  
    > Der Leistungs Panel-Ablaufverfolgung der Seitenauslastung  
    > ! [Der Leistungs Panel-Ablaufverfolgung der Seitenauslastung] [Imageperformance]  

Die Ablaufverfolgung zeigt die Aktivität chronologisch an, von links nach rechts.  Die oben dargestellten fps-, CPU-und net-Diagramme geben Ihnen einen Überblick über Frames pro Sekunde, CPU-Aktivität und Netzwerkaktivität.  Der in [Abbildung 37](#figure-37) ausgewählte gelb markierte Block bedeutet, dass die CPU vollständig mit Skriptaktivitäten ausgelastet war.  Dies ist ein Hinweis darauf, dass Sie möglicherweise die Seitenauslastung beschleunigen können, indem Sie eine geringere JavaScript-Arbeit durchführen.  

> ##### Abbildung 36  
> Der Abschnitt "Übersicht" der Ablaufverfolgung  
> ! [Der Abschnitt ' Übersicht ' der Ablaufverfolgung] [Imageoverview]  

Untersuchen Sie die Ablaufverfolgung, um Möglichkeiten für eine geringere JavaScript-Arbeit zu finden:  

1.  Wählen Sie den Abschnitt **Anzeige** dauern aus, um ihn zu erweitern.  Basierend auf der Tatsache, dass es möglicherweise eine Reihe von [Timings][MDNUserTimingApi] -Maßnahmen von reagieren gibt, scheint es so zu sein, als ob die APP von Tony die Entwicklungsmethode von reagieren verwendet.  Wenn Sie auf den Produktionsmodus von reagieren umstellen, kann dies einige einfache Leistungsgewinne hervorbringen.  
    
    > ##### Abbildung 37  
    > Abschnitt "Anzeigedauern"  
    > ! [Der Abschnitt "Anzeigedauer"] [ImageUserTiming]  

1.  Wählen Sie erneut **Anzeige** dauern aus, um den Abschnitt zu reduzieren.  
1.  Durchsuchen Sie den **Haupt** Abschnitt.  Dieser Abschnitt zeigt ein chronologisches Protokoll der Hauptthread Aktivität, von links nach rechts.  Die y-Achse (von oben nach unten) zeigt, warum Ereignisse aufgetreten sind.  In [Abbildung 39](#figure-39)führte das Ereignis beispielsweise dazu, dass die Funktion ausgeführt wurde, die zur Ausführung führte, `Evaluate Script` `(anonymous)` `(anonymous)` die `__webpack__require__` zur Ausführung führte usw.  
    
    > ##### Abbildung 38  
    > Der Hauptabschnitt  
    > ! [Der Hauptbereich] [Imagemain]  

1.  Scrollen Sie nach unten zum unteren Rand des **Haupt** Abschnitts.  Wenn Sie ein Framework verwenden, wird der größte Teil der oberen Aktivität durch das Framework verursacht, das normalerweise außerhalb des Steuerelements liegt.  Die von Ihrer APP verursachte Aktivität befindet sich normalerweise unten.  In dieser app scheint es so zu sein, dass eine Funktion mit dem Namen `App` viele Anforderungen an eine `mineBitcoin` Funktion verursacht.  Es klingt wie Tony könnte die Geräte seiner Fans verwenden, um cryptocurrency zu vergruben...  
    
    > ##### Abbildung 39  
    > Über die Aktivität zeigen `mineBitcoin`  
    > ! [Schwebt über der mineBitcoin-Aktivität] [Imagemine]  
    
    > [!NOTE]
    > Obwohl die Anforderungen, die Ihr Framework macht, in der Regel nicht in Ihrem Steuerelement enthalten sind, können Sie Ihre APP manchmal so strukturieren, dass das Framework ineffizient ausgeführt wird.  Die Umstrukturierung ihrer App zur effizienten Verwendung des Frameworks ist eine Möglichkeit, um die Arbeit am Hauptthread zu verkürzen.  Dies erfordert jedoch ein umfassendes Verständnis der Funktionsweise des Frameworks und der Art von Änderungen, die Sie in Ihrem eigenen Code vornehmen, um das Framework effizienter zu verwenden.  

1.  Erweitern Sie den Abschnitt **Bottom-up** .  Auf dieser Registerkarte wird aufgeschlüsselt, welche Aktivitäten die meiste Zeit in Anspruch genommen haben.  Wenn im Abschnitt Bottom-up nichts angezeigt wird, klicken Sie auf die Beschriftung für **Haupt** Abschnitt.  Der **Bottom-up-** Abschnitt zeigt nur Informationen zu einer beliebigen Aktivität oder Aktivitätsgruppe, die Sie aktuell ausgewählt haben.  Wenn Sie beispielsweise auf eine der Aktivitäten geklickt haben `mineBitcoin` , werden im Abschnitt **Bottom-up** nur Informationen für diese Aktivität angezeigt.  
    
    > ##### Abbildung 40  
    > Die Registerkarte "Bottom-up"  
    > ! [Die untere Registerkarte] [ImageBottomUp]  

In der Spalte **selbst Zeit** wird angezeigt, wie viel Zeit direkt in den einzelnen Aktivitäten aufgewendet wurde.  [Abbildung 41](#figure-41) zeigt beispielsweise, dass etwa 63% der Hauptthread Zeit für die Funktion aufgewendet wurden `mineBitcoin` .  

Zeit, um zu sehen, ob die Auslastung der Seite durch Verwenden des Produktionsmodus und verringern der JavaScript-Aktivität beschleunigt werden kann.  Beginnen mit dem Produktionsmodus:  

1.  Öffnen Sie auf der Registerkarte Editor den Reiter `webpack.config.js` .  
1.  Ändern Sie `"mode":"development"` in `"mode":"production"`.  
1.  Warten Sie, bis der neue Build bereitgestellt wird.  
1.  Überwachen Sie die Seite erneut.  
    
    > ##### Abbildung 41  
    > Ein Überwachungsbericht nach der Konfiguration von WebPack für die Verwendung des Produktionsmodus  
    > ! [Ein Auditbericht nach der Konfiguration von WebPack zur Verwendung des Produktionsmodus] [ImageReport5]  

Reduzieren Sie die JavaScript-Aktivität, indem Sie die Anforderung entfernen an `mineBitcoin` :  

1.  Öffnen Sie auf der Registerkarte Editor den Reiter `src/App.jsx` .  
1.  Kommentieren Sie die Anforderung `this.mineBitcoin(1500)` in `constructor` .  
1.  Warten Sie, bis der neue Build bereitgestellt wird.  
1.  Überwachen Sie die Seite erneut.  
    
    > ##### Abbildung 42  
    > Ein Überwachungsbericht nach dem Entfernen unnötiger JavaScript-Arbeit  
    > ! [Ein Überwachungsbericht nach dem Entfernen unnötiger JavaScript-Arbeit] [ImageReport6]  

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

<!--    -->  



<!-- image links -->  

[ImageAddPatternIcon]: /microsoft-edge/devtools-guide-chromium/media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-panels-icon.msft.png  
[ImagePerformIcon]: /microsoft-edge/devtools-guide-chromium/media/perform-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  
[ImageRemoveIcon]: /microsoft-edge/devtools-guide-chromium/media/remove-icon.msft.png  

[ImageTony]: /microsoft-edge/devtools-guide-chromium/media/speed-tony.msft.png "Abbildung 1: Tony the Cat"  
[ImageEditor]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-server-js.msft.png "Abbildung 2: die Registerkarte "Editor""  
[ImageMenu]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-server-js-remix-project.msft.png "Abbildung 3: das Menü, das nach dem Klicken auf "Tony" angezeigt wird"  
[ImageDemo]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-show-live.msft.png "Abbildung 4: die Registerkarte "Demo""  
[ImageDevtools]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-show-live-console.msft.png "Abbildung 5: devtools und die Demo"  
[ImageUndocked]: /microsoft-edge/devtools-guide-chromium/media/speed-console.msft.png "Abbildung 6: nicht angedockte devtools"  
[ImageAudits]: /microsoft-edge/devtools-guide-chromium/media/speed-audits-performance.msft.png "Abbildung 7: Überwachungs Panel"  
[ImageReport]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png "Abbildung 8: der Bericht für das Audits-Panel zur Leistung der Website"  
<!--[ImageError]: /microsoft-edge/devtools-guide-chromium/media/speed-.msft.png "Old Figure 9: A report that errored"  -->  
[Imagegesamt]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-Metrics-Collapsed-Metrics-highlighted.msft.png "Abbildung 9: der Gesamtleistungsfaktor"  
[Imagemetrics]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-Metrics-Collapsed-highlighted.msft.png "Abbildung 10: der Abschnitt" Metriken "  
[ImageFirstMeaningfulPaint]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-Metrics-Expanded.msft.png "Abbildung 11: Auswählen der hervorgehobenen Umschaltfläche zum Erweitern der Metriken"  
[Imagescreenshots]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-View-Trace.msft.png "Abbildung 12: Screenshots, wie die Seite beim Laden aussah"  
[Imageopportunities]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-Opportunities.msft.png "Abbildung 13: der Abschnitt" Verkaufschancen "  
[Imagecompression]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-Opportunities-Expanded.msft.png "Abbildung 14: eliminieren von Render-Blockierungs Ressourcen"  
[Imagereference]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Web-dev-Performance-Audits.msft.png "Abbildung 15: Dokumentation für die Möglichkeit zum Eliminieren von Render-Blockierungs Ressourcen"  
[Imagediagnostics]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-Diagnostics.msft.png "Abbildung 16: der Abschnitt" Diagnose "  
[Imagepassed]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-passed-Audits.msft.png "Abbildung 17: der Abschnitt" übergebene Überprüfungen "  
[Imagenetwork]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Network.msft.png "Abbildung 18: Netzwerk Panel"  
[ImageLargeRows]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Network-use-Large-Request-Rows.msft.png "Abbildung 19: große Zeilen in der Tabelle" Netzwerkanforderungen "  
[Imageheaders]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Network-use-Large-Request-Rows-Bundle-js.msft.png "Abbildung 20: die Registerkarte" Überschriften "  
[ImageServer]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Server-js.msft.png "Abbildung 21: Bearbeiten von Server. js"  
<!--[ImageBuilding]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-server-js-edited.msft.png "Old Figure 22: The animation that indicates that the site is getting built"  -->  
[Imagerequests]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Network-Main.msft.png "Abbildung 22: die Spalte" Größe "zeigt jetzt zwei unterschiedliche Werte für Textressourcen an."  
[Imagegzip]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Network-Bundle-js-Headers-Response.msft.png "Abbildung 23: der Abschnitt mit den Antwortheadern enthält jetzt eine `content-encoding` Kopfzeile"  
[ImageReport2]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-Audits-Performance.msft.png "Abbildung 24: ein Überwachungsbericht nach der Aktivierung der Text Komprimierung"  
<!--[ImageResize]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png "Old Figure 27: Details about the properly size images opportunity"  -->
[ImageReport3]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Compression-Small-Images-Audits-Performance.msft.png "Abbildung 25: ein Überwachungsbericht nach dem Ändern der Größe von Bildern"  
[Imagerender]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-Audits-Performance-oppportunities-Expanded.msft.png "Abbildung 26: Weitere Informationen zur Möglichkeit zum Eliminieren von Render-Blockierungs Ressourcen"  
[ImageCommandMenu]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-Audits-Performance-oppportunities-Expanded-Command-Coverage.msft.png "Abbildung 27: Öffnen des Befehlsmenüs im Überwachungs Panel  
[Imagedeckment]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-Audits-Performance-oppportunities-Expanded-drawer-Coverage.msft.png "Abbildung 28: die Registerkarte" Abdeckung "  
[ImageCoverageReport]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-Audits-Performance-oppportunities-Expanded-drawer-Coverage-Reloaded.msft.png "Abbildung 29: der Coverage-Bericht"  
[Imagejquery]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-sources-drawer-Coverage-Reloaded-jQuery-js.msft.png "Abbildung 30: Anzeigen der jQuery-Datei im Quellen Panel"  
[Imageblocking]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-network-drawer-Request-Blocking-Empty.msft.png "Abbildung 31: die Registerkarte" Anforderungs Blockierung "  
[Imagelibs]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-network-drawer-Request-Blocking-Added.msft.png "Abbildung 32: Hinzufügen eines Musters zum Blockieren einer Anforderung an das libs-Verzeichnis"  
[ImageBlockedLibs]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-network-Reloaded-drawer-Request-Blocking-Added.msft.png "Abbildung 33: das Netzwerk Panel zeigt, dass die Anforderungen blockiert wurden"  
[ImageReport4]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-2-Audits-Performance.msft.png "Abbildung 34: ein Überwachungsbericht nach dem Entfernen der Render-Blockierungs Ressourcen"  
[Imageperformance]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Performance-Slow-Network-Slow-CPU.msft.png "Abbildung 35: die Spur des Leistungs Panels der Seitenlast"  
[Imageoverview]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Performance-Slow-Network-Slow-CPU-Main-Highlight.msft.png "Abbildung 36: der Abschnitt" Übersicht "der Ablaufverfolgung"  
[ImageUserTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Performance-Slow-Network-Slow-CPU-Timings.msft.png "Abbildung 37: der Abschnitt" Anzeigedauer "  
[Imagemain]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Performance-Slow-Network-Slow-CPU-Main.msft.png "Abbildung 38: der Hauptabschnitt"  
[Imagemine]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Performance-Slow-Network-Slow-CPU-Timings-minebitcoin.msft.png "Abbildung 39: Hovern über die minebitcoin-Aktivität"  
[ImageBottomUp]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Performance-Slow-Network-Slow-CPU-Timings-Summary-minebitcoin.msft.png "Abbildung 40: die Bottom-up-Registerkarte"  
[ImageReport5]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-3-Audits-Performance.msft.png "Abbildung 41: ein Überwachungsbericht nach der Konfiguration von WebPack für die Verwendung des Produktionsmodus"  
[ImageReport6]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-4-Audits-Performance.msft.png "Abbildung 42: ein Überwachungsbericht nach dem Entfernen unnötiger JavaScript-Arbeit"  

<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Referenz zur Leistungsanalyse"  

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
