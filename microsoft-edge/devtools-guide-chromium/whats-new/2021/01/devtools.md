---
description: Das Neue-Tool ist jetzt Willkommen, Visual Font Editor im Bereich Formatvorlagen, CSS Flexbox-Debugtools und vieles mehr.
title: Neues in DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 2722da0093b3ba6521b5190e61bb208e02a2041e
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408339"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-89"></a>Neues in DevTools (Microsoft Edge 89)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="whats-new-is-now-welcome"></a>What's New is now Welcome  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Das **Tool What's New** in den Microsoft Edge DevTools hat jetzt ein neues Erscheinungsbild und einen neuen Namen:  **Welcome**.  Das **Willkommenstool** zeigt weiterhin die neuesten DevTools-Neuigkeiten und -Updates an.  Es enthält jetzt auch Links zur Microsoft Edge DevTools-Dokumentation, Möglichkeiten zum Senden von Feedback und vieles mehr.  Wenn Sie das **Willkommenstool** nach jedem Update für Microsoft Edge anzeigen möchten, aktivieren Sie das Kontrollkästchen neben Registerkarte Öffnen nach jedem Update **unter** dem Titel.  Um das **Willkommenstool zu** schließen, wählen Sie **das X** auf der rechten Seite des Registerkartentitels aus.  Wenn Sie das ursprüngliche **Tool What's New** bevorzugen, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings]  >  **Experimente,** und entfernen Sie das Kontrollkästchen neben **Registerkarte Willkommen aktivieren**.  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="Das Willkommenstool wird hervorgehoben" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   Das **Willkommenstool** wird hervorgehoben  
:::image-end:::  

## <a name="visual-font-editor-in-the-styles-pane"></a>Visual Font Editor im Bereich Formatvorlagen  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Wenn Sie mit Schriftarten in CSS arbeiten, verwenden Sie den neuen [visuellen Schriftarten-Editor][DevtoolsInspectStylesEditFonts].  Sie können Fallbackschriftarten definieren und Schieberegler verwenden, um Schriftgewichtung, Schriftgröße, Zeilenhöhe und Abstand zu definieren.  Der **Schriftarten-Editor** hilft Ihnen beim Ausführen der folgenden Aktionen.  

*   Wechseln zwischen Einheiten für unterschiedliche Schriftarteigenschaften  
*   Wechseln zwischen Schlüsselwörtern für unterschiedliche Schriftarteigenschaften  
*   Einheiten konvertieren  
*   Generieren von genauem CSS-Code  
    
Um dieses Experiment zu [][DevtoolsCustomizeIndexSettings]aktivieren, navigieren Sie zu  >  **EinstellungenExperimente,** und wählen Sie das Kontrollkästchen neben **Neue Schriftarten-Editor-Tools**im Bereich Formatvorlagen aktivieren aus.  Weitere Informationen finden Sie unter [Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich Formatvorlagen in DevTools][DevtoolsInspectStylesEditFonts].  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1093229][CR1093229].  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="Der visuelle Schriftarten-Editor wird im Bereich Formatvorlagen hervorgehoben." lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   Der visuelle **Schriftarten-Editor** wird im Bereich **Formatvorlagen** hervorgehoben.  
:::image-end:::  

## <a name="css-flexbox-debugging-tools"></a>CSS-Flexbox-Debuggingtools  

Die Flexbox-Debugfeatures befinden sich in der aktiven Entwicklung.  Um das Experiment für die folgenden beiden Features zu aktivieren, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings]Experimente, und aktivieren Sie das Kontrollkästchen neben  >  **** **Neue CSS-Flexbox-Debugfeatures aktivieren.**  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [1136394][CR1136394] und [1139949][CR1139949].  

### <a name="new-flexbox-flex-icon-helps-identify-and-display-flex-containers"></a>Neues Flexbox(Flex)-Symbol hilft beim Identifizieren und Anzeigen von Flexcontainern  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Im **Elementtool** hilft Ihnen das neue Flexbox(flex)-Symbol, Flexbox-Container in Ihrem Code zu identifizieren.  Wählen Sie das Flexbox \(flex\)-Symbol aus, um den Überlagerungseffekt zu aktivieren oder zu deaktivieren, der einen Flexbox-Container umreißt.  Sie können die Farbe der Überlagerung im **Layoutbereich** anpassen, der sich neben **Formatvorlagen** und **Berechnet befindet.**  

:::row:::
   :::column span="":::
      Zum Aktivieren und Deaktivieren des Überlagerungseffekts, der den Flexbox-Container umreißt, wählen Sie das Symbol Flexbox \( `flex` \) aus.  
   :::column-end:::
   :::column span="":::
      Sie können die Farbe der Überlagerung im **Layoutbereich** neben **Formatvorlagen** und **Berechnet anpassen.**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="Das Flexbox (Flex)-Symbol und die hervorgehobene Webseite" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         Das **Flexbox-Symbol** `flex` \( \) und die hervorgehobene Webseite :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="Die im Layoutbereich hervorgehobenen Flexbox-Überlagerungen" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         Die **im Layoutbereich hervorgehobenen Flexbox-Überlagerungen** ****  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-alignment-icons-and-gridlines-when-flexbox-layouts-change-using-css-properties"></a>Anzeigen von Ausrichtungssymbolen und Gitternetzlinien beim Ändern von Flexboxlayouts mithilfe von CSS-Eigenschaften  

<!--  Title: Display alignment icons and gridlines for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Wenn Sie CSS für Ihr Flexbox-Layout bearbeiten, **** werden bei automatischen CSS-Vervollständigungen im Bereich Formatvorlagen nun hilfreiche Symbole neben relevanten Flexbox-Eigenschaften angezeigt.  Öffnen Sie zum Testen dieses neuen Features das **Tool Elemente,** und wählen Sie einen Flexcontainer aus.  Fügen Sie dann eine Eigenschaft für den Container im Bereich Formatvorlagen hinzu oder ändern Sie **sie.**  

:::row:::
   :::column span="":::
      Im Menü autocomplete werden jetzt Symbole angezeigt, die die Auswirkung von Ausrichtungseigenschaften wie und `align-content` `align-items` angeben.  
   :::column-end:::
   :::column span="":::
      Darüber hinaus zeigt DevTools jetzt eine Leitlinie an, um die `align-items` CSS-Eigenschaft besser zu überprüfen.  Die `gap` CSS-Eigenschaft wird ebenfalls unterstützt.  In der folgenden Abbildung wird die CSS-Eigenschaft auf festgelegt, und das Schraffurmuster für `gap` `gap: 12px;` jede Lücke wird angezeigt.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Das Menü "AutoComplete" wird für CSS-Eigenschaften hervorgehoben, die mit ausrichtungs-" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         Menü "AutoVervollständigung" für CSS-Eigenschaften hervorgehoben, die mit beginnen `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Flexboxlücke in CSS-Eigenschaften und webseite hervorgehoben" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         Flexbox `gap` in CSS-Eigenschaften und hervorgehobener Webseite  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="add-tools-quickly-with-new-more-tools-button"></a>Schnelles Hinzufügen von Tools mit der neuen Schaltfläche "Weitere Tools"  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Sie haben nun eine neue Möglichkeit, weitere Tools in den Microsoft Edge DevTools zu öffnen.  Nachdem Sie dieses Experiment aktivieren, wird das Symbol Weitere **Tools** rechts neben dem Hauptbereich als Pluszeichen ( `+` ) angezeigt.  Wenn Sie eine Liste anderer Tools anzeigen möchten, die dem Hauptbereich hinzugefügt werden, wählen Sie das Symbol Weitere **Tools** \( `+` \) aus.  Um dieses Experiment zu aktivieren, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings]Experimente, und wählen Sie dann das Kontrollkästchen neben Registerkartenmenüs aktivieren + aus, um  >  **** weitere Tools **zu öffnen.**  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Weitere In DevTools hervorgehobene Tools" lightbox="../../media/2021/01/more-tools.msft.png":::
   **Weitere In** DevTools hervorgehobene Tools  
:::image-end:::  

## <a name="assistive-technologies-now-announce-position-and-count-of-css-suggestions"></a>Hilfstechnologien kündigen jetzt Position und Anzahl von CSS-Vorschlägen an  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

Wenn Sie CSS bearbeiten, erhalten Sie eine Dropdownliste mit Features.  Dieses Feature war für Benutzer von Hilfstechnologien nicht verfügbar, da es in Microsoft Edge, Version 89, angekündigt ist.  Ein Benutzer von Hilfstechnologien kann nun im Bereich Formatvorlagen durch **CSS-Vorschläge** navigieren.  In Microsoft Edge, Version 88 und früher, navigierte die als Benutzer angekündigte Hilfstechnologie beim Bearbeiten von CSS im Bereich Formatvorlagen durch die Liste der `Suggestion` Vorschläge. ****  In Microsoft Edge, Version 89, hört ein Benutzer der Hilfstechnologie jetzt die Position und Anzahl des aktuellen Vorschlags.  Jeder Vorschlag wird angekündigt, wenn der Benutzer durch die Liste der Vorschläge navigiert, z. B. Vorschlag 3 von 5.  Weitere Informationen zum Schreiben von CSS in devTools finden Sie unter [Ändern von CSS][DevtoolsCssReferenceChangeCss].  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1157329][CR1157329].  

Um ein Video anzuzeigen, das mehrere Vorschläge anzeigt und laut vorlesen kann, wenn dieses Experiment aktiviert ist, navigieren Sie zu Voiceover, in dem [Devtools-Optionen](https://youtu.be/9TcUpleEwwA) auf YouTube angekündigt werden.  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="Der im Bereich Formatvorlagen hervorgehobene Vorschlag" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   Die `suggestion` im Bereich Formatvorlagen **hervorgehobene** Liste  
:::image-end:::  

## <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a>Emulieren von Surface Duo und Samsung Galaxy Fold  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

Testen Sie die Darstellung Ihrer Website oder App auf den folgenden Geräten in Microsoft Edge.  

*   [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [Samsung -Galaxis-Faltung][SamsungUsMobileGalaxyFold]  
    
Aktivieren Sie **Die Features der Experimentellen Webplattform,** um auf das neue Feature für den Medienbildschirmbereich und [die getWindowSegments-JavaScript-API zu zugreifen.][DualScreenWebJavascriptGetwindowsegments] [][DualScreenWebCssMediaSpanning]  Navigieren Sie `edge://flags` zu und umschalten Sie das Flag neben **Experimental Web Platform Features**.  Verwenden Sie beim Emulieren des Geräts die folgenden Features, um Ihre Website oder App für die dualen bildschirm- und faltbaren [Geräte zu verbessern.][DevtoolsDeviceModeIndex]  

*   [Spanning][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices], das ist, wenn Ihre Website \(oder App\) auf beiden Bildschirmen angezeigt wird.  
*   [Rendern der Naht][DualScreenIntroductionHowToWorkWithSeam], d. h. des Abstands zwischen den beiden Bildschirmen.  
    
Navigieren Sie zu Issue [1054281,][CR1054281]um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Emulieren des dualen Bildschirms" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   Emulieren des dualen Bildschirms  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-112"></a>Microsoft Edge Developer Tools for Visual Studio Code Version 1.1.2  

Die [Microsoft Edge Developer Tools für Visual Studio Codeerweiterung][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] Version 1.1.2 für Microsoft Visual Studio Code hat die folgenden Änderungen seit der vorherigen Version.  Microsoft Visual Studio Code aktualisiert Erweiterungen automatisch.  Navigieren Sie zum manuellen Aktualisieren auf Version 1.1.2 zu [Manuelles Aktualisieren einer Erweiterung.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  

*   Jedem **Element in** der Zielliste wurde eine Schaltfläche "Instanz schließen" hinzugefügt \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)  
*   Microsoft [Edge DevTools-Version][DevtoolsMain] von 84.0.522.63 auf [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)  
*   Enthaltener [Debugger für Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] als Abhängigkeit \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)  
*   Implementierte Einstellungsoption zum Ändern von Erweiterungsthemen \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)  
    
Sie können Probleme datein und zur Erweiterung im [vscode-edge-devtools GitHub-Repository beitragen.][GithubMicrosoftVscodeEdgeDevtools]  

## <a name="announcements-from-the-chromium-project"></a>Ankündigungen aus dem Chromium-Projekt  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="capture-node-screenshot-beyond-viewport"></a>Screenshot des Aufnahmeknotens über viewport hinaus  

In Microsoft Edge, Version 89, sind Knotenfotos genauer und erfassen den vollständigen Knoten, auch wenn Der Inhalt des Knotens im Viewport nicht sichtbar ist.  Zeigen Sie **im Elementtool** auf ein Element, öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und wählen Sie Screenshot des **Knotens erfassen aus.**  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1003629][CR1003629].  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Screenshot des Aufnahmeknotens im Kontextmenü des Elements-Tools" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   **Screenshot des Aufnahmeknotens** im Kontextmenü des **Elements-Tools**  
:::image-end:::  

### <a name="elements-tool-updates"></a>Aktualisierungen des Elements-Tools  

#### <a name="support-forcing-the-target-css-state"></a>Unterstützung zum Erzwingen des CSS-Status :target  

Sie können devTools nun verwenden, um die CSS-Pseudoklasse [:target][MdnDocsWebCssTarget] zu erzwingen.  Die Pseudoklasse wird ausgelöst, wenn ein eindeutiges `:target` Element \(das Zielelement\) über ein Element verfügt, das einem `id` Fragment der URL entspricht.  Beispielsweise löst die URL die Pseudoklasse für `http://www.example.com/index.html#section1` ein `:target` HTML-Element mit `id="section1"` aus.  Um eine Demo mit hervorgehobener Abschnitt 1 zu testen, navigieren Sie zu [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1156628][CR1156628].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="Die Webseite ohne erzwungene CSS hervorgehoben" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         Webseite ohne erzwungene CSS hervorgehoben  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text=":target CSS erzwungen und Webseite hervorgehoben" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` CSS erzwungen und Webseite hervorgehoben  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <a name="use-duplicate-elements-to-copy-elements"></a>Kopieren von Elementen mithilfe duplizierter Elemente  

Verwenden Sie die neue **Duplikatelementverknüpfung,** um ein Element zu klonen.  Zeigen Sie **im Tool Elemente** auf ein Element, öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\), wählen Sie **Duplikatelement aus.**  Unter dem ausgewählten Element wird ein neues Element erstellt.  Um das Element mit einer Tastenkombination zu duplizieren, wählen `Shift` + `Alt` + `Down Arrow` Sie \(Windows/Linux\) oder `Shift` + `Option` + `Down Arrow` \(macOS\).  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1150797][CR1150797].  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="Das Duplicate-Element wird im Kontextmenü eines Elements im Element des Elements-Tools hervorgehoben." lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   Das **Duplicate-Element** wird im Kontextmenü eines Elements im Element **des Elements-Tools** hervorgehoben.  
:::image-end:::  

#### <a name="color-pickers-for-custom-css-properties"></a>Farbauswahl für benutzerdefinierte CSS-Eigenschaften  

Im **Bereich Formatvorlagen** werden nun Farbauswahlen für benutzerdefinierte CSS-Eigenschaften angezeigt.  Zum Durchschleifen der RGBA-, HSLA- und Hex-Formate des Farbwerts halten Sie die Farbauswahl fest, und wählen `Shift` Sie sie aus.  Navigieren Sie zu Issue [1147016,][CR1147016]um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Farbauswahl für benutzerdefinierte CSS-Eigenschaften" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   Farbauswahl für benutzerdefinierte CSS-Eigenschaften  
:::image-end:::  

#### <a name="copy-css-classes-and-properties"></a>Kopieren von CSS-Klassen und -Eigenschaften  

Sie können jetzt die CSS-Eigenschaften mit einigen neuen Optionen im Kontextmenü schneller kopieren.  Wählen Sie **im Elementtool** ein Element aus.  Wenn Sie den Wert **** kopieren möchten, zeigen Sie im Bereich Formatvorlagen auf eine CSS-Klasse oder eine CSS-Eigenschaft, öffnen Sie ein Kontextmenü \(rechtsklicken\), und wählen Sie die Kopieroption aus.  

:::row:::
   :::column span="":::
      Kopieren von Optionen für eine CSS-Klasse.  
      
      | Option | Details |  
      |:--- |:--- |  
      | **Auswahl kopieren** | Kopieren Sie den aktuellen Selektornamen. |  
      | **Kopierregel** | Kopieren Sie die Regel der aktuellen Auswahl. |  
      | **Kopieren aller Deklarationen** | Kopieren Sie alle Deklarationen unter der aktuellen Regel, einschließlich nicht gültiger Und Präfixeigenschaften. |  
   :::column-end:::
   :::column span="":::
      Kopieren von Optionen für eine CSS-Eigenschaft.  
      
      | Option | Details |      
      |:--- |:--- |  
      | **Kopierdeklaration** | Kopieren Sie die Deklaration der aktuellen Zeile. |  
      | **Copy-Eigenschaft** | Kopieren Sie die Eigenschaft der aktuellen Zeile. |  
      | **Kopierwert** | Kopieren Sie den Wert der aktuellen Zeile. |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Kopieren von Optionen für eine CSS-Klasse im Kontextmenü" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         Kopieren von Optionen für eine CSS-Klasse im Kontextmenü  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Kopieren von Optionen für eine CSS-Eigenschaft im Kontextmenü" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         Kopieren von Optionen für eine CSS-Eigenschaft im Kontextmenü  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1152391][CR1152391].  

### <a name="cookies-updates"></a>Updates für Cookies  

#### <a name="new-option-to-display-url-decoded-cookies"></a>Neue Option zum Anzeigen von URL-decodierten Cookies  

Sie können jetzt entscheiden, den URL-decodierten Cookiewert im Bereich **Cookies anzuzeigen.**  Navigieren Sie zum Anzeigen des **** decodierten Cookies zum Bereich Anwendungscookies, wählen Sie ein beliebiges Cookie in der Liste aus, und aktivieren Sie das Kontrollkästchen neben  >  **** **Decodierte URL anzeigen.**  Navigieren Sie zu Issue [997625,][CR997625]um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Option zum Anzeigen von URL-decodierten Cookies" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   Option zum Anzeigen von URL-decodierten Cookies  
:::image-end:::  

#### <a name="filter-and-clear-visible-cookies"></a>Filtern und Löschen sichtbarer Cookies  

In Microsoft Edge, Version 88 **** oder früher, bot das Anwendungstool nur eine Möglichkeit, alle Cookies mit der Schaltfläche **Alle Cookies löschen zu** löschen.  In Microsoft Edge, Version 89, können Sie nun gefilterte Cookies löschen auswählen, um nur die gefilterten Cookies zu löschen. ****  Navigieren Sie zum Filtern von Cookies zu **Anwendungscookies,**  >  **** und geben Sie in das Textfeld **Filter** ein.  Um die angezeigten Cookies zu löschen, wählen Sie die Schaltfläche **Gefilterte Cookies löschen** aus.  Wenn Sie alle anderen Cookies anzeigen möchten, löschen Sie den Filtertext.  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [978059][CR978059].  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Nur sichtbare Cookies löschen" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   Nur sichtbare Cookies löschen  
:::image-end:::  

#### <a name="new-option-to-clear-third-party-cookies-in-the-storage-pane"></a>Neue Option zum Löschen von Drittanbietercookies im Speicherbereich  

DevTools löschen jetzt standardmäßig nur Cookies von Erst drittanbietern.  Navigieren Sie zum Löschen von Websitedaten **** und Erst-Cookies zu Anwendungsspeicher, und wählen Sie  >  **** **dann Websitedaten löschen aus.**  

Um Websitedaten und alle Cookies **** zu löschen, navigieren Sie zu  >  **Anwendungsspeicher**.  Aktivieren Sie das Kontrollkästchen neben dem Einschleingen von **Drittanbietercookies,** und wählen Sie **dann Websitedaten löschen aus.**  

Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1012337][CR1012337].  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Option zum Löschen von Drittanbietercookies" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   Option zum Löschen von Drittanbietercookies  
:::image-end:::  

### <a name="network-tool-updates"></a>Netzwerktoolupdates  

#### <a name="persist-record-network-log-setting"></a>Netzwerkprotokolleinstellung für "Datensatz beibehalten"  

In Microsoft Edge version 88 or earlier, DevTools reset the **Record network log setting** when a webpage refreshes.  In Microsoft Edge, Version 89, bleibt DevTools nun die **Einstellung Netzwerkprotokoll aufzeichnen** erhalten.  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1122580][CR1122580].  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Aufzeichnen des Netzwerkprotokolls" lightbox="../../media/2021/01/network-log.msft.png":::
   Aufzeichnen des Netzwerkprotokolls  
:::image-end:::  

#### <a name="online-option-is-now-no-throttling-option"></a>Onlineoption ist jetzt keine Einschränkungsoption  

Die Netzwerkemulationsoption **Online** wird jetzt in **No Throttling umbenannt.**  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1028078][CR1028078].  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Keine Einschränkungsoption" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   **Keine Einschränkungsoption**  
:::image-end:::  

### <a name="new-copy-options-in-the-console-tool-sources-tool-and-styles-pane"></a>Neue Kopieroptionen im Bereich Konsolentool, Quellentool und Formatvorlagen

#### <a name="copy-object-in-the-console-and-sources-tool"></a>Kopieren des Objekts im Tool Konsole und Quellen  

Sie können nun Objektwerte in die **Konsolen-** und **Quellentools** kopieren.  Die Möglichkeit, Objektwerte zu kopieren, ist bei der Arbeit mit großen Objekten hilfreich.  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [1148353][CR1148353] und [1149859][CR1149859].  

:::row:::
   :::column span="":::
      Zeigen Sie **im Konsolentool** auf ein Objekt, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **dann Objekt kopieren aus.**  
   :::column-end:::
   :::column span="":::
      Zeigen **Sie im** Tool Quellen auf einem Haltepunkt **** auf ein Objekt, markieren Sie im Popupfenster Objekt ein Objekt, öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und wählen Sie dann Objekt kopieren **aus.**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Copy-Objekt in der Konsole" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         Copy-Objekt in der **Konsole**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Copy-Objekt in Sources" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         Copy-Objekt in **Sources**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="copy-file-name-in-the-sources-tool-and-styles-pane"></a>Kopieren des Dateinamens im Bereich "Quellen" und "Formatvorlagen"  

Sie können nun einen Dateinamen mithilfe des Kontextmenüs kopieren.  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [1155120][CR1155120].  

:::row:::
   :::column span="":::
      Zeigen Sie **im Tool Quellen** auf einen Dateinamen, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie dann **Dateinamen kopieren aus.**  
   :::column-end:::
   :::column span="":::
      Zeigen **Sie** im Elementtool > **Formatvorlagen** auf einen Dateinamen, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste auf\), und wählen Sie dann **Dateinamen kopieren aus.**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Kopieren des Dateinamens in Quellen" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         Kopieren des Dateinamens in **Quellen**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Kopieren des Dateinamens im Formatvorlagenbereich" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         Kopieren des Dateinamens im **Formatvorlagenbereich**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="updates-to-frame-details"></a>Updates für Frame-Details  

#### <a name="service-workers-information-in-frame-details"></a>Service Workers-Informationen in Framedetails  

DevTools listet nun einen dedizierten Dienstmitarbeiter unter dem übergeordneten Frame auf.  In der folgenden Abbildung werden Die Details der Dienstmitarbeiter angezeigt.  Um die Details der Dienstmitarbeiter anzuzeigen, navigieren Sie zu **Application**  >  **Frames**  >  `top`  >  **Service Workers,** und wählen Sie dann einen Dienstmitarbeiter aus.  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1122507][CR1122507].  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Service Workers-Informationen in den Frames-Details" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   **Service Workers-Informationen** in den **Frames-Details**  
:::image-end:::  

#### <a name="measure-memory-information-in-frame-details"></a>Messen von Speicherinformationen in Framedetails  

Der `performance.measureMemory()` API-Status wird nun im Abschnitt **API-Verfügbarkeit** angezeigt.  Die neue `performance.measureMemory()` API schätzt die Speicherauslastung der gesamten Webseite.  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1139899][CR1139899].  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Messen des Arbeitsspeichers" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   Messen des Arbeitsspeichers  
:::image-end:::  

### <a name="dropped-frames-in-the-performance-tool"></a>Verworfene Frames im Tool "Leistung"  

Wenn Sie [die Lastleistung im Tool Leistung analysieren,][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]markiert der **Abschnitt Frames** verworfene Frames nun als rot.  Zeigen Sie zum Anzeigen der Framerate auf einen verworfenen Frame.  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1075865][CR1075865].  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Verworfene Frames" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   Verworfene Frames  
:::image-end:::  

#### <a name="new-color-contrast-calculation---advanced-perceptual-contrast-algorithm-apca"></a>Neue Farbkontrastberechnung – Advanced Perceptual Contrast Algorithm (APCA)  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Der [Advanced Perceptual Contrast Algorithm (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] ersetzt das [AA][W3cWaiWcag21QuickrefContrastMinimum] / [AAA-Richtlinienkontrastverhältnis][W3cWaiWcag21QuickrefContrastEnhanced] in der [Farbauswahl.][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]  APCA ist eine neue Methode zum Berechnen des Kontrasts.  Sie basiert auf modernen Forschungen zur Farbwahrnehmung.  Im Vergleich zu AA/AAA-Richtlinien ist APCA kontextabhängiger.  Der Kontrast wird basierend auf den folgenden räumlichen Eigenschaften des Texts, der Farbe und des Kontexts berechnet.  

*   Räumliche Eigenschaften von Text, die Schriftgewichtung und Schriftgröße enthalten.  
*   Räumliche Eigenschaften der Farbe, die wahrgenommenen Kontrast zwischen Text und Hintergrund enthalten.  
*   Räumliche Eigenschaften des Kontexts, die Umgebungslicht, Umgebung und beabsichtigten Zweck enthalten.  
    
Um dieses Experiment zu [][DevtoolsCustomizeIndexSettings]aktivieren, navigieren Sie zu EinstellungenExperimente, und aktivieren Sie das Kontrollkästchen neben Aktivieren des neuen Advanced Perceptual Contrast Algorithm (APCA), der das vorherige Kontrastverhältnis und  >  **** **AA/AAA-Richtlinien ersetzt.**  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1121900][CR1121900].  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA in der Farbauswahl" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   APCA in der Farbauswahl  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Neues in DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Anzeigen des Kontrastverhältnisses eines Textelements in der Farbauswahl – Barrierefreiheitsreferenz | Microsoft Docs"  
[DevtoolsCssReferenceChangeCss]: /microsoft-edge/devtools-guide-chromium/css/reference#change-css "Ändern von CSS – CSS-| Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: microsoft-edge/devtools-guide-chromium/customize/shortcuts "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools-| Microsoft Docs"  
[DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/device-mode/dual-screen-and-foldables#testing-on-foldable-and-dual-screen-devices "Testen auf zusammenklappbaren und dualen Bildschirmgeräten – Emulieren von Dual-Screen- und faltbaren Geräten in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emulieren von mobilen Geräten in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simulieren eines mobilen Viewports – Emulieren mobiler Geräte in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-load-performance "Datensatzlastleistung – Leistungsanalysereferenz | Microsoft Docs"  
[DevtoolsInspectStylesEditFonts]: /microsoft-edge/devtools-guide-chromium/inspect-styles/edit-fonts "Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich Formatvorlagen in DevTools | Microsoft Docs"  
[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium/index "Microsoft Edge (Chromium) Developer Tools – Übersicht | Microsoft Docs"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Arbeiten mit der Naht – Einführung in duale Bildschirmgeräte | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Css-Medienbildschirm-Spannfunktion für die Erkennung von | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "Die getWindowSegments-JavaScript-API für Dual-Screen-| Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Abschnitt 1 – CSS :target demo for What's New in DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229: Implementieren des Dropdowns in Einstellungen zum Ändern von Designs | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: Einschl. Debugger für Microsoft Edge als Abhängigkeitsmodus | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: Upgrade der Edge DevTools-Version auf 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248: Hinzufügen einzelner Schließenschaltflächen zum Instanzenbereich | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Wählen Sie Schriftartmerkmale und Hintergrundfarben aus, um genügend Kontrast für die Lesbarkeit | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Vertrauenswürdige | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Neue Surface Duo-| Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Preview Channels"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Manuelles Aktualisieren einer Erweiterung – Erweiterung Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  
[CR978059]: https://crbug.com/978059 "Problem 978059: Löschen von Cookies beim Filtern, löschen Sie nicht nur die gefilterten | Chromium-Fehler"  
[CR997625]: https://crbug.com/997625 "Issue 997625: New Feature Req | Option zum Sehen des url-decodierten Werts in Cookies | Chromium-Fehler"  
[CR1003629]: https://crbug.com/1003629 "Problem 1003629: Der Aufnahmeknoten screenshott den Knoten unterhalb der Falte nicht mehr. | Chromium-Fehler"  
[CR1012337]: https://crbug.com/1012337 "Issue 1012337: Clear Site Data destroys Google session on non-Google sites | Chromium-Fehler"  
[CR1028078]: https://crbug.com/1028078 "Issue 1028078: Put Online and Offline next to each each in the list | Chromium-Fehler"  
[CR1054281]: https://crbug.com/1054281 "Problem 1054281: Featureanforderung: DevTools sollte zusammenklappbare und duale Bildschirmgeräte emulieren, die | Chromium-Fehler"  
[CR1075865]: https://crbug.com/1075865 "Issue 1075865: Show dropped frames in devtools timeline | Chromium-Fehler"  
[CR1093229]: https://crbug.com/1093229 "Issue 1093229: DevTools: offer a specialized typeface editor ui | Chromium-Fehler"  
[CR1121900]: https://crbug.com/1121900 "Issue 1121900: DevTools: update contrast calculation logic per new spec | Chromium-Fehler"  
[CR1122507]: https://crbug.com/1122507 "Problem 1122507: Anzeigen von Worker-Informationen in der Framestrukturansicht | Chromium-Fehler"  
[CR1122580]: https://crbug.com/1122580 "Problem 1122580: Das Deaktivieren der Netzwerkaufzeichnung bei neu geladenen | Chromium-Fehler"  
[CR1136394]: https://crbug.com/1136394 "Problem 1136394: Flexbox-Tooling | Chromium-Fehler"  
[CR1139899]: https://crbug.com/1139899 "Problem 1139899: Verfügbarkeit der Gated-API in der Frame-Detailansicht melden | Chromium-Fehler"  
[CR1139949]: https://crbug.com/1139949 "Problem 1139949: Flexbox-| Chromium-Fehler"  
[CR1147016]: https://crbug.com/1147016 "Problem 1147016: Die Farbauswahl wird in der var()-Funktion nicht angezeigt. | Chromium-Fehler"  
[CR1148353]: https://crbug.com/1148353 "Problem 1148353: Featureanforderung: Objekt aus der devtools-Konsole kopieren | Chromium-Fehler"  
[CR1149859]: https://crbug.com/1149859 "Problem 1149859: [Featureanforderung][Konsole] Hinzufügen eines Kopierobjekts zum Zwischenablageelement zum kontextbezogenen menübezogenen | Chromium-Fehler"  
[CR1150797]: https://crbug.com/1150797 "Problem 1150797: Hinzufügen eines Kontextmenüs für doppelte Elemente im Elementbereich | Chromium-Fehler"  
[CR1152391]: https://crbug.com/1152391 "Issue 1152391: Support for copy CSS context menu in styles panel | Chromium-Fehler"  
[CR1155120]: https://crbug.com/1155120 "Problem 1155120: [FR]Dateiname und Zeilennummer | Chromium-Fehler"  
[CR1156628]: https://crbug.com/1156628 "Problem 1156628: DevTools: Add support for :target in force element state feature | Chromium-Fehler"  
[CR1157329]: https://crbug.com/1157329 "Problem 1157329: Barrierefreiheit – Sprachausgabe: Die Sprachausgabe kündigt nicht die Anzahl und Position für Vorschläge an, die für Code auf der Registerkarte Formatvorlagen verfügbar | Chromium-Fehler"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxis fold | Samsung US"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contrast (Enhanced) – So erfüllen Sie WCAG (Quick Reference) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Contrast (Minimum) – So erfüllen Sie WCAG (Quick Reference) | W3C"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/updates/2021/01/devtools/index) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen

[SpanningPlaceholder]: link-t-b-d "Übergreifender Platzhalter"  
