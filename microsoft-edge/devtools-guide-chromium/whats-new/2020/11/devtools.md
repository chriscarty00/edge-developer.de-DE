---
description: Microsoft Edge unter Linux, verbesserte webhint-Tipps im Problem Tool, neue Features für die Dienst Worker-Debuggen und vieles mehr.
title: Neuerungen in devtools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 500b64e7b51e0f02c9fcbcb7a83e8273b3a5a0d7
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "11205243"
---
# Neuerungen in devtools (Microsoft Edge 88)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Microsoft Edge-und Microsoft Edge-Treiber jetzt auf Linux verfügbar  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

Microsoft Edge dev wird nun auf der Grundlage von Ubuntu-, Debian-, Fedora-und openSUSE-Distributionen unterstützt.  Laden Sie Microsoft Edge dev `.deb` oder `.rpm` Package direkt von der [Microsoft Edge Insider-Website][MicrosoftinsiderDownloadPlatformLinux] herunter, und installieren Sie Sie, oder verwenden Sie die standardmäßigen Paket Verwaltungstools Ihrer Linux-Distribution.  

Wenn Sie eine Linux-Umgebung in ihrer Continuous Integration and Delivery \ (CI/CD \)-Lösungen verwenden, steht Microsoft Edge Driver auch unter Linux zur Verfügung.  Wenn Sie mit der Automatisierung von Microsoft Edge dev mit Microsoft Edge Driver beginnen möchten, navigieren Sie zur [Seite Microsoft Edge Driver Downloads][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].  Hilfe zur Automatisierung von Microsoft Edge dev zusammen mit Microsoft Edge Driver finden [Sie unter Verwenden von WebDriver (Chrom) für die Testautomatisierung][WebDriverChromiumMain].  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools in Microsoft Edge unter Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   DevTools in Microsoft Edge unter Linux  
:::image-end:::  

## Verbesserte Tipps für webhints und Plattformen im Problem Tool  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

Ein Open-Source-Tool, [webhint][WebhintMain], bietet Echtzeitfeedback für Websites und lokale Webseiten.  Beginnen Sie mit [Microsoft Edge, Version 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], und überprüfen Sie das webhint-Feedback im [Issues][DevtoolsIssuesIndex] -Tool.  Probleme, die im Tool " **Probleme** " angezeigt werden, sind jetzt mit dem Hinzufügen der folgenden Kategorien leichter zu überprüfen.  

*   [Barrierefreiheit][WebhintUserGuideHintsAccessibility]  
*   [Kompatibilität][WebhintUserGuideHintsCompatibility]  
*   [Leistung][WebhintUserGuideHintsPerformance]  
*   [Von Fallgruben][WebhintUserGuideHintsPitfalls]  
*   [PWA][WebhintUserGuideHintsPwa]  
*   [Sicherheit][WebhintUserGuideHintsSecurity]  
    
Sie können jetzt die Probleme von Drittanbietern mithilfe eines neuen Kontrollkästchens herausfiltern.  Die Filterfunktionalität hilft Ihnen, Probleme im Zusammenhang mit Code aus Drittanbieterbibliotheken oder anderen Quellen zu verbergen.  

Damit Sie die von [webhint][WebhintMain]aufgedeckten Probleme überprüfen können, werden im Tool **Probleme** nun die folgenden Informationen angezeigt.  

*   Verbesserte Codeausschnitte.  
*   Links zu anderen relevanten Panels.  
*   Links zur Dokumentation, die Ihnen bei der Behebung von Problemen in Ihrer Website helfen.  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Problem Tool" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   **Problem** Tool  
:::image-end:::  

## Zusammengesetzte Layer sind jetzt in der 3D-Ansicht  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

Sie können jetzt **Layer** -Inhalte neben z-Index-Werten und dem Dokumentobjektmodell \ (DOM \) visualisieren.  Mit dieser Funktion können Sie so oft Debuggen, ohne zwischen [3D-Ansicht][Devtools3dViewIndex] und **Layer** -Tools umzuschalten.  Für ein umfassendes visuelles Debugging [werden jetzt die 3D-Ansicht und die zusammengesetzten Ebenen kombiniert][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Bereich ' zusammengesetzte Ebenen '" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   Bereich ' **zusammengesetzte Ebenen** '  
:::image-end:::  

## CSS-Variablendefinitionen im Bereich "Formatvorlagen"  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

Im Bereich " **Formatvorlagen** " werden die [CSS-Variablen][MdnUsingCssCustomProperties] nun direkt mit jeder Definition verknüpft.  Wählen Sie die Variable aus, um die Definition der CSS-Variablen einfach anzuzeigen oder zu ändern.  Im Beispiel zeigt devtools die CSS-Attribute für das `body` Element an.  Führen Sie die folgenden Aktionen aus, um die Variablendefinition für die `--theme-body-background` CSS-Variable anzuzeigen.  

1.  Wählen Sie im Bereich **Formatvorlagen** die Option aus `var(--theme-body-background)` .  
1.  Im Bereich " **Formatvorlagen** " wird nun die Definition der `--theme-body-background` CSS-Variable angezeigt.  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Mit der Formatvorlage verknüpfte CSS-Variable" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         Mit der Formatvorlage verknüpfte CSS-Variable  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Mit Formatvorlagen Ziel verknüpfte CSS-Variable" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         Mit Formatvorlagen Ziel verknüpfte CSS-Variable  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Verbesserungen des Service Worker-Debuggens  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

Die folgenden neuen Features in den Tools " [Netzwerk](#network-tool)", " [Anwendung](#application-tool)" und " [Quellen](#sources-tool) " unterstützen Sie beim Erstellen Ihrer [PWA][ProgressiveWebAppsChromiumIndex].  Verwenden Sie die folgenden Features, wenn Probleme beim Debuggen Ihrer Dienstmitarbeiter auftreten können.  

Anforderungs Routing zeigt die `startup` und- `fetch` Ereignisse basierend auf den Netzwerkanforderungen an, die von Dienst Mitarbeitern ausgeführt werden.  Der Zugriff auf die Zeitpläne erfolgt entweder über die **Anwendung** oder das **Netzwerk** Tool.  Die Zeitpläne helfen, wenn Sie Probleme mit Servicemitarbeitern haben, und möchten sehen, ob ein Fehler mit dem oder-Ereignis vorliegt `startup` `fetch` .  

### Anwendungstool  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

Zeigen Sie alle Routinginformationen für Dienstmitarbeiter an, und klicken Sie auf den Link neue **Netzwerkanforderungen** .  Führen Sie die folgenden Aktionen aus, um beim Debuggen des Dienst Arbeitsthreads zusätzlichen Kontext anzuzeigen.  

1.  Navigieren Sie zu **Anwendungs**  >  **Dienst Mitarbeitern**.  
1.  Wählen Sie **Netzwerkanforderungen**aus.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Öffnen des Tools "Netzwerk" im Bereich "Dienstmitarbeiter"" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       Öffnen des Tools " **Netzwerk** " im Bereich " **Dienstmitarbeiter** "
    :::image-end:::  
    
1.  Das **Netzwerk** Tool wird im **Einzug** geöffnet und zeigt alle Netzwerkanforderungen für Dienstmitarbeiter an.  Die Netzwerkanforderungen werden mithilfe von gefiltert `is:service-worker-intercepted` .  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Netzwerktool in der Schublade" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       **Netzwerk** Tool in der **Schublade**  
    :::image-end:::
    
1. Wenn Sie das **Netzwerk** Tool an den oberen Bereich zurücksetzen möchten, schließen Sie die **Schublade**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Schließen der Schublade, um das Netzwerktool zurückzugeben" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       Schließen der **Schublade** , um das **Netzwerk** Tool zurückzugeben  
    :::image-end:::  
    
### Netzwerktool  

Debuggen von Netzwerkanforderungen, die über Dienstmitarbeiter ausgeführt werden.  Sie können Netzwerkanforderungen auch über das **Anwendungs** Tool öffnen.  Für jede Anforderung zeigen devtools die folgenden Informationen [im Bereich "Anzeigedauer][DevtoolsNetworkReferenceViewTimingBreakdownRequest] " an.  

*   Der Anfang einer Anforderung und die Dauer des Bootstrap.  
*   Änderungen an der Service Worker-Registrierung.  
*   Die Laufzeit eines `fetch` Ereignishandlers.  
*   Die Laufzeit aller `fetch` Ereignisse zum Laden eines Clients.  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Bereich "Anzeigedauer"" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   Bereich " **Anzeige** Dauer"  
:::image-end:::  

### Quellen Tool  

In früheren Versionen von Microsoft Edge war der Grad der Tiefe in der Aufrufliste auf den JavaScript-Code in Ihrem Dienstmitarbeiter limitiert.  In Microsoft Edge 88 zeigt die Aufrufliste nun den Initiator von Anforderungen an, die über Ihren Dienstmitarbeiter ausgeführt werden.  

Zum Auffinden des Initiators der Anforderung verwenden Sie die Aufrufliste Ihres JavaScript-Codes im Dienstmitarbeiter.  Die Aufrufliste in den folgenden Zahlen beginnt mit dem JavaScript-Code in Ihrem Dienstmitarbeiter und zeigt einen Verweis auf die ursprüngliche Webanforderungs Seite als an `(index):157` .  In der zweiten Abbildung wird der Bezug ausgewählt und der Initiator geöffnet, der die Anforderung gestellt hat.  Der Initiator in der zweiten Abbildung ist die Webseite.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="Der service-worker.js Datei-und Aufruf Stapel, der den Absender anfordert" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         Der `service-worker.js` Datei-und Aufruf Stapel, der den Absender anfordert  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="Die (Index-) Webseite ist der Anforderungs Initiator" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         Die `(index)` Webseite ist der Anforderungs Initiator  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Kopieren des Eigenschaftswerts einer Netzwerkanforderung  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

Kopieren Sie im Tool **Netzwerk** den Eigenschaftswert einer Netzwerkanforderung unter Verwendung der Option neuer **Kopier Wert** .  Der Eigenschaftswert wird als decodierter JSON-Wert kopiert.  In früheren Versionen von Microsoft Edge mussten Sie einen Wert mithilfe einer der folgenden Aktionen kopieren.  

*   Markieren Sie den gesamten Text, und kopieren Sie ihn.  
*   Speichern Sie den Wert als globale Variable (sofern zutreffend), und kopieren Sie Sie aus der devtools- [Konsole][DevtoolsConsoleIndex].  
    
Navigieren Sie zum Kopieren des Eigenschaftswerts in die Zwischenablage, um eine [formatierte Antwort-JSON in die Zwischenablage zu kopieren][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].  Navigieren Sie zu Issue [1132084][CR1132084], um den Verlauf dieses Features im Open-Source-Projekt Chrom zu überprüfen.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Kopieren des Eigenschaftswerts in devtools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         Kopieren des Eigenschaftswerts in devtools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Einfügen des Eigenschaftswerts in Visual Studio-Code" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         Einfügen des Eigenschaftswerts in Visual Studio-Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Anpassen von Tastenkombinationen für mehrere Tastenkombinationen  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

[Seit Microsoft Edge, Version 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], können Sie Tastenkombinationen für jede Aktion in devtools anpassen.  In Microsoft Edge, Version 88, können Sie jetzt Multi-drücken Sie Tastenkombinationen erstellen.  Wenn Sie eine Tastenkombination für eine Aktion im devtools festlegen möchten, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings]  >  **Experimente** , und aktivieren Sie das Kontrollkästchen neben **Tastenkombinationen-Editor aktivieren**.  Weitere Informationen zum Anpassen und Bearbeiten von Tastenkombinationen finden Sie unter Aktivieren des Features für den [Tasten Kombinations-Editor][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  

Die rote Markierung zeigt beispielsweise eine Tastenkombination mit mehreren drücken an, die für die Aktion " **Aufzeichnen von Ereignissen starten** " angepasst wurde.  Navigieren Sie zu [Issue #174309][CR174309], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Tastenkombinationen für Akkorde" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   Tastenkombinationen für mehrere Tastenkombinationen  
:::image-end:::  

## Ankündigungen aus dem Chromium-Projekt  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Neue CSS-Visualisierungstools für Winkel  

DevTools unterstützt jetzt das Debuggen von CSS-Winkeln besser.  Wenn auf der Seite auf einem HTML-Element ein CSS-Winkel angewendet wurde, wird neben dem Winkel im **Formatvorlagen** Tool ein Clock-Symbol angezeigt.  Wenn Sie die Uhr-Überlagerung umschalten möchten, wählen Sie das Symbol Uhr aus.  Wenn Sie den Winkel ändern möchten, wählen Sie eine beliebige Stelle in der Uhr aus, oder ziehen Sie die Nadel.  Zum Ändern des Winkelwerts können Sie auch Maus-und Tastenkombinationen verwenden.  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  Navigieren Sie zu Problemen [1126178][CR1126178] und [1138633][CR1138633], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.  

<!--todo:  add link when css angle clock section exists.  -->  

Für das Beispiel wird der folgende CSS-Winkel verwendet.  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="CSS-Winkel" lightbox="../../media/2020/11/css-angle.msft.png":::
   CSS-Winkel  
:::image-end:::  

### Simulieren der Speicherkontingent Größe im Speicherbereich  

Sie können jetzt die Größe des Speicherkontingents im **Speicher** Bereich außer Kraft setzen.  Dieses Feature ermöglicht es Ihnen, verschiedene Geräte zu simulieren und das Verhalten Ihrer Website oder app in Szenarien mit geringer Verfügbarkeit zu testen.  Führen Sie die folgenden Aktionen aus, um das Speicherkontingent zu simulieren.  

1.  Navigieren Sie zum **Anwendungs**  >  **Speicher**.  
1.  Aktivieren Sie das Kontrollkästchen **benutzerdefinierten Speicherkontingent simulieren** .  
1.  Geben Sie eine gültige Nummer ein.  
    
Weitere Informationen zum Emulieren von mobilen Geräten und anderen Features in der devtools finden Sie unter [emulieren von mobilen Geräten in Microsoft Edge devtools ][DevtoolsDeviceModeIndex].  Navigieren Sie zu Problemen [945786][CR945786] und [1146985][CR1146985], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simulieren der Speicherkontingent Größe" lightbox="../../media/2020/11/storage-quota.msft.png":::
   Simulieren der Speicherkontingent Größe  
:::image-end:::  

### Melden von CORS-Fehlern im Netzwerktool  

Testen Sie diese Funktion, indem Sie zur [CORS-Fehler Demo][GlitchCorsErrors]navigieren.  Öffnen Sie das Tool **Netzwerk** , aktualisieren Sie die Seite, und beobachten Sie die fehlerhafte CORS-Netzwerkanforderung.  In der Spalte Status wird der **CORS-Fehler**angezeigt.  Wenn Sie auf den Fehler zeigen, wird in der QuickInfo nun der Fehlercode angezeigt.  In Microsoft Edge, Version 87 und früheren Versionen, devtools nur den generischen **(fehlerhaften)** Status für CORS-Fehler angezeigt.  Navigieren Sie zu Issue [1141824][CR1141824], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="CORS-Fehler" lightbox="../../media/2020/11/cors-err.msft.png":::
   CORS-Fehler  
:::image-end:::  

### Frame Details-Ansicht Updates  

#### Informationen zur übergreifenden Isolierung in der Ansicht "Frame Details"  

Der übergreifende isolierte Status wird nun unter dem Abschnitt **Sicherheit & Isolierung** angezeigt.  Im Abschnitt neue **API-Verfügbarkeit** werden die Verfügbarkeit von `SharedArrayBuffer` s \ (SAB \) und die Angabe, ob die Puffer freigegeben werden können, angezeigt `postMessage()` .  Eine veraltete Warnung wird angezeigt, wenn das SAB-Element und `postMessage()` derzeit verfügbar ist, der Kontext aber nicht über eine isolierte Herkunft verfügt.  `SharedArrayBuffers`Navigieren Sie zu [WindowOrWorkerGlobalScope. crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated], wenn Sie weitere Informationen zur isolierten Ursprungs Isolierung benötigen und warum Sie für Features wie erforderlich ist.  Navigieren Sie zu Issue [1139899][CR1139899], um Echtzeitupdates dieser Funktion im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Informationen über einen anderen Ursprung" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   Informationen über einen anderen Ursprung  
:::image-end:::  

#### Neue Web Worker-Informationen in der Ansicht "Frame Details"  

DevTools organisiert nun Web-Worker unter dem entsprechenden übergeordneten Frame.  Beispiel: Wenn der `someName` Frame erstellt wird `worker.js` , `worker.js` wird unter `someName` in der Liste **Frames** angezeigt.  Führen Sie die folgenden Aktionen aus, um die Details des Web Worker anzuzeigen.  

1.  Öffnen Sie das **Anwendungs** Tool.  
1.  Erweitern Sie einen Frame, der Web Workers enthält.  
1.  Erweitern Sie die **Worker** -Struktur.  
1.  Wählen Sie eine Arbeitskraft aus.  
    
Navigieren Sie zu Problemen [1122507][CR1122507] und [1051466][CR1051466], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Informationen für Web-Worker" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   Informationen für Web-Worker  
:::image-end:::  

#### Anzeigen von Details zum Öffnen des Frames für geöffnete Fenster  

DevTools organisiert nun geöffnete [Fenster][MdnWindowConstructors] unter dem relevanten übergeordneten [Frame][MdnWindowFrames].  Wenn beispielsweise der `top` Frame a an geöffnet `Window` wird `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium` , `Window` wird unter `top` in der Liste **Frames** angezeigt.  

Führen Sie die folgenden Aktionen aus, um den Frame anzuzeigen, der für das Öffnen eines anderen Fensters im **Element** Tool verantwortlich ist.  

1.  Öffnen Sie die **Frame** Struktur.  
1.  Erweitern Sie **geöffnete Fenster** , und wählen `Window` Sie den für den übergeordneten Frame aus, den Sie wissen möchten.  
1.  Wählen Sie den Link **öffnender Frame** aus.  

Die Details werden angezeigt, in welchem Frame die Eröffnung eines anderen verursacht wurde `Window` .  Führen Sie die folgenden Aktionen aus, um den Öffner im **Element** -Tool anzuzeigen.  

1.  Öffnen Sie die **Frame** Struktur.  
1.  Wählen Sie ein geöffnetes Fenster aus, um die Details zu öffnen `Window` .  
1.  Wählen Sie den Link **öffnender Frame** aus.  
    
Navigieren Sie zu Issue [1107766][CR1107766], um den Verlauf dieses Features im Open-Source-Projekt Chrom zu überprüfen.  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Details zum geöffneten Frame" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   Details zum geöffneten Frame  
:::image-end:::  

### Kopieren von StackTrace für den Netzwerk Initiator  

Führen Sie die folgenden Aktionen aus, um den StackTrace in Ihre Zwischenablage zu kopieren.  

1.  Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \).  
1.  Wählen **Copy**Sie Copy  >  **StackTrace**kopieren aus.  
    
Navigieren Sie zu Issue [1139615][CR1139615], um den Verlauf dieses Features im Open-Source-Projekt Chrom zu überprüfen.

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Kopieren von StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   Kopieren von StackTrace  
:::image-end:::  

### Vorschau von WASM-Variablenwert bei Mouseover  

Verwenden Sie dieses Feature, um den Wert einer Webassembly \ (WASM \)-Variablen zu überprüfen, wenn der Code angehalten wird.  Um den aktuellen Wert einer Variablen anzuzeigen, zeigen Sie auf eine Variable.  Navigieren Sie zu Problemen [1058836][CR1058836] und [1071432][CR1071432], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Vorschau WASM-Variable bei Mouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   Vorschau WASM-Variable bei Mouseover  
:::image-end:::  

### Einheitliche Maßeinheiten für die Größe von Dateien und Arbeitsspeicher  

DevTools wird jetzt immer wieder verwendet `kB` , um die Größe von Dateien und Arbeitsspeicher anzuzeigen.  Zuvor devtools Mixed `kB` und `KiB` .

*   `kB` oder Kilobyte \ (10 ^ 3 oder 1000 Bytes \)  
*   `KiB` oder Kibibyte \ (2 ^ 10 oder 1024 Bytes \)  
    
Beispiel: das **Netzwerk** Tool, das zuvor `kB` in den Etiketten verwendet, aber `KiB` in Berechnungen verwendet wurde.  Ihr Feedback hat gezeigt, dass diese Inkonsistenz Verwirrung verursacht hat.  Navigieren Sie zu Issue [1035309][CR1035309], um den Verlauf dieses Features im Open-Source-Projekt Chrom zu überprüfen.  

## Herunterladen der Microsoft Edge Preview-Kanäle  

Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge Preview Channels] [MicrosoftEdgePreviewChannels] als Standard Entwicklungsbrowser verwenden.  Über die Vorschau Kanäle erhalten Sie Zugriff auf die neuesten devtools-Funktionen.  

## Kontakt mit dem Microsoft Edge devtools-Team  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "3D-Ansicht | Microsoft docs"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Übersicht über die Konsole | Microsoft docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Einstellungen – anpassen von Microsoft Edge devtools | Microsoft docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emulieren von mobilen Geräten in Microsoft Edge devtools | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Aktivieren des Tasten Kombinations-Editors – experimentelle Features | Microsoft docs"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Aktivieren von zusammengesetzten Layern in der 3D-Ansicht – experimentelle Features | Microsoft docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Suchen und Beheben von Problemen mit dem Microsoft Edge devtools Issues Tool | Microsoft docs"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Kopieren der formatierten Antwort JSON in die Zwischenablage – Netzwerkanalyse Referenz | Microsoft docs"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Anzeigen der zeitlichen Aufschlüsselung einer Anforderung – Netzwerkanalyse Referenz | Microsoft docs"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Verwenden von WebDriver (Chrom) für die Testautomatisierung | Microsoft docs"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Progressive Web-Apps unter Windows | Microsoft docs"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/10/devtools#customize-keyboard-shortcuts-in-settings "Anpassen von Tastenkombinationen in Einstellungen-Neuerungen in devtools (Microsoft Edge 87) | Microsoft docs"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools#webhint-feedback-in-the-issues-panel "webhint-Feedback im Bereich "Probleme" – Neuerungen in devtools (Microsoft Edge 85) | Microsoft docs"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "WebDriver herunterladen | Microsoft-Entwickler"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Herunterladen von Microsoft Edge-Insider Kanälen"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio-Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chrom Fehler"  

[CR174309]: https://crbug.com/174309 "Problem 174309: devtools: zulassen der Anpassung von Tastenkombinationen/Tastenbindungen | Chrom Fehler"  
[CR945786]: https://crbug.com/945786 "Problem 945786: devtools: zulassen des Überschreibens von Navigator. Storage. Estimate () | Chrom Fehler"  
[CR1029427]: https://crbug.com/1029427 "Problem 1029427: Reduzieren des Performance-Overhead beim Protokollnachrichten Versand im Front-End | Chrom Fehler"  
[CR1035309]: https://crbug.com/1035309 "Problem 1035309: devtools sollte konsistent MB verwenden, um Megabyte zu bedeuten, nicht Mebibyte | Chrom Fehler"  
[CR1051466]: https://crbug.com/1051466 "Problem 1051466: unterstützen des Coop/COEP-Debuggens in devtools | Chrom Fehler"  
[CR1058836]: https://crbug.com/1058836 "Problem 1058836: UX-Probleme rund um das WASM-Debuggen | Chrom Fehler"  
[CR1071432]: https://crbug.com/1071432 "Problem 1071432: ☂️ WASM Basic Developer Experience | Chrom Fehler"  
[CR1107766]: https://crbug.com/1107766 "Problem 1107766: zeigt Informationen zu Frames an, die von "Window. Open ()" in der Frame Struktur generiert wurden | Chrom Fehler"  
[CR1122507]: https://crbug.com/1122507 "Problem 1122507: Surface Worker-Informationen in der Frame Strukturansicht | Chrom Fehler"  
[CR1126178]: https://crbug.com/1126178 "Problem 1126178: ☂ devtools: CSS <Typ> Komponenten | Chrom Fehler"  
[CR1130556]: https://crbug.com/1130556 "Problem 1130556: devtools: Testen von Bild Fallbacks (Emulation) | Chrom Fehler"  
[CR1132084]: https://crbug.com/1132084 "Problem 1132084: keine einfache Möglichkeit zum Kopieren von JSON-Anforderungsnutzlast | Chrom Fehler"  
[CR1136394]: https://crbug.com/1136394 "Problem 1136394: Flexbox-Tooling | Chrom Fehler"  
[CR1138633]: https://crbug.com/1138633 "Problem 1138633: devtools: CSS <Winkel> Komponente sollte das Erscheinungsbild Ihrer Eigenschaft im Hintergrund der Uhr widerspiegeln | Chrom Fehler"  
[CR1139615]: https://crbug.com/1139615 "Problem 1139615: Netzwerk Initiator sollte die Möglichkeit bieten, die Stapelüberwachung zu kopieren | Chrom Fehler"  
[CR1139899]: https://crbug.com/1139899 "Problem 1139899: Verfügbarkeit der Gated-API in der Frame Detailansicht | Chrom Fehler"  
[CR1139945]: https://crbug.com/1139945 "Problem 1139945: Symbole für Flexbox-CSS-Eigenschaften im Bereich "Formatvorlagen" | Chrom Fehler"  
[CR1141824]: https://crbug.com/1141824 "Problem 1141824: verbessern der CORS-Fehlerberichterstattung in devtools | Chrom Fehler"  
[CR1144090]: https://crbug.com/1144090 "Problem 1144090: Hinzufügen von Flex-Stil Adornern zur Elementstruktur | Chrom Fehler"  
[CR1146985]: https://crbug.com/1146985 "Problem 1146985: der gelöschte Text wird weiterhin im Textfeld "Speicher" im Abschnitt "dev tools" angezeigt | Chrom Fehler"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "CORS-Fehler | Glitch"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Übergreifende Ressourcenfreigabe (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Verwenden von benutzerdefinierten CSS-Eigenschaften (Variablen) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Konstruktoren – Fenster | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window. Frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope. crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "webhint"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Barrierefreiheit | webhint"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Kompatibilität | webhint"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Leistung | webhint"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Fallstricke | webhint"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | webhint"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Sicherheit | webhint"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/updates/2020/11/devtools/index) gefunden und von [Jecelyn Yeen][JecelynYeen] \ (Developer Advocate, Chrome devtools \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
