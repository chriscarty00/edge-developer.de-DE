---
description: Die neuesten experimentellen Features in Microsoft Edge für Web Apps
title: Experimentelle Features | Progressive Web Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, experiment, progressive web apps, web apps, PWAs, PWA
ms.openlocfilehash: 641b6fd5185e7f96289c1de6482764979ee0981d
ms.sourcegitcommit: 9cc54ba3e731ecc8b713c3cf215018848f7405b9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/19/2021
ms.locfileid: "11496756"
---
# <a name="experimental-features-in-progressive-web-apps-pwas"></a>Experimentelle Features in Progressive Web Apps (PWAs)  

Microsoft Edge bietet Zugriff auf experimentelle Features, die sich noch in der Entwicklung befinden.  Testen Und geben Sie Feedback, um zu ermitteln, ob die einzelnen Features bereit sind und wann sie [veröffentlicht werden.](#providing-feedback-on-experimental-features)  

Experimentelle Features sind in allen Kanälen der Microsoft Edge verfügbar, aber die neuesten experimentellen Features sind nur in der Microsoft Edge Canary Channel.  

## <a name="turn-on-experimental-features"></a>Aktivieren experimenteller Features  

Führen Sie die folgenden Schritte aus, um die experimentellen Features in Microsoft Edge aktivieren.  
  
1.  Öffnen Sie Microsoft Edge.   
    
    > [!NOTE]
    > Stellen Sie sicher, dass Sie Microsoft Edge version verwenden, in der das Experiment in diesem Artikel aufgeführt ist.  Navigieren Sie zu [Experimentelle Features](#features-that-are-available-to-test).  
    
1.  Navigieren Sie zu `edge://flags`.  
1.  Navigieren Sie zum entsprechenden Experiment.  
1.  Wählen Sie das Dropdownmenü neben der Experimentbeschreibung aus, und wählen Sie `Enabled` aus.  
    
    :::image type="complex" source="../media/turn-on-experimental-flag.png" alt-text="Wählen Sie Aktiviert aus, um ein Experiment zu aktivieren." lightbox="../media/turn-on-experimental-flag.png":::
       Wählen **Sie Aktiviert** aus, um ein Experiment zu aktivieren.  
    :::image-end:::  
    
    > [!NOTE]
    > Jedes Experiment verfügt in der Regel über ein Dropdownmenü, um die folgenden Werte zu wählen.  Wenn ein experimentelles Feature keinen Eintrag zu **Experimenten**enthält, werden Anweisungen bereitgestellt, um Microsoft Edge über die Befehlszeile zu starten.
    > 
    > *   `Default`  
    > *   `Disabled`  
    > *   `Enabled`  
    
1.  Starten Sie Microsoft Edge neu.  
    
### <a name="origin-trials"></a>Herkunfts Versuche  

Microsoft Edge verwendet manchmal Ursprungstests, um Features für bestimmte Domänen oder Websites zu testen.  Möglicherweise möchten Sie eine Origin-Testversion für Ihre Website verwenden, um ein bestimmtes Feature anzuwenden.  Wenn Sie Websitebesitzer sind, können Sie sich an einer Ursprungsprobe registrieren.  Eine Origin-Testversion bietet Features für einen Prozentsatz der Microsoft Edge, die Ihre Website besuchen.

Weitere Informationen zu Origin Trials finden Sie unter [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].  
    
> [!NOTE]
> Experimentelle Features werden ständig aktualisiert und können Leistungsprobleme verursachen.  Navigieren Sie zum Deaktivieren eines experimentellen Features zu Aktivieren experimenteller [Features,](#turn-on-experimental-features)navigieren Sie zum Experiment, und wählen Sie dann `Disabled` aus.  

## <a name="features-that-are-available-to-test"></a>Features, die zum Testen verfügbar sind  

In der folgenden Liste werden die neuen experimentellen Web-App-Features beschrieben, die zum Testen und Überprüfen auf Microsoft Edge.  

| Feature | Microsoft Edge Version | Plattform |  
|:--- |:--- |:--- |  
| [URI-Protokollbehandlung](#uri-protocol-handling) | 91 oder höher | Windows und Linux |    
| [URL Link Handling](#url-link-handling) | 91 oder höher | Windows|
| [Überlagerung von Fenstersteuerelementen für Desktop-Apps](#window-controls-overlay-for-installed-desktop-web-apps) | 91 oder höher | Windows 10|   
| [Ausführen unter Betriebssystemanmeldung](#run-on-os-login) | 88 oder höher | Alle |  
| [Tastenkombinationen](#shortcuts) | 87 oder höher | Alle |  
| [Dateiverarbeitung](#file-handling) | 83 oder höher | All Desktop |  


## <a name="uri-protocol-handling"></a>URI-Protokollbehandlung  

Ein einheitlicher Ressourcenbezeichner \(URI\) kann verwendet werden, um mehr als nur Links zu Webseiten und Webinhalten mithilfe des HTTP- oder FTP-Protokolls zu definieren.  URIs können verwendet werden, um Links zu allem zu beschreiben, was Sie in einem Schema codieren.  Beispielsweise wird das Protokoll verwendet, um einen E-Mail-Link zu beschreiben, und das Betriebssystem \(OS\) oder der Browser entscheidet, welche Webseite oder App dieses Protokoll `mailto://` verarbeiten soll.  

Weitere Informationen zur vorhandenen browserbasierten Unterstützung finden Sie unter [Webbasierte Protokollhandler][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers].  

Mit diesem Feature können Sie die folgenden Aktionen ausführen.  

*   Registrieren Der PWA mit dem Hostbetriebssystem mithilfe des Manifests Ihrer Web-App
*   Deklarieren, dass PWA ein bestimmtes URI-Protokoll verarbeitet  
     
Nachdem Sie einen PWA als Protokollhandler registriert haben, wird der registrierte PWA vom Betriebssystem aktiviert und empfängt den URI, wenn ein Benutzer einen Hyperlink mit einem bestimmten Schema wie oder aus einem Browser oder einer systemeigenen App aus `mailto://` `web+music://` wählt.  

Dieses Feature erfordert, dass Sie das Web-App-Manifest so aktualisieren, dass es ein Array enthält, in das Array müssen `protocol_handlers` Sie zwei Felder angeben:  

*   `protocol`: Das Protokoll zur Verarbeitung der Anforderung, z. B. `mailto` oder `web+jngl` .  
*   `url`: Der HTTPS-URI im App-Bereich, der das Protokoll behandelt.  In Zukunft soll der URI, der mit dem Protokollhandlerschema beginnt, das Token `%s` ersetzen.  
    
Aktualisieren Sie Ihr Manifest, um das Protokoll zu unterstützen, das Sie registrieren möchten.  Nachdem Sie dieses Feature aktivieren, Microsoft Edge die folgenden Aktionen abgeschlossen.  

1.  Erkennt Änderungen im Manifest  
1.  Registriert die App für das Protokoll  
    
Wenn mehrere Apps ein Protokoll registrieren, wird dem Benutzer eine Eingabeaufforderung angezeigt.  Der Benutzer wählt die entsprechende App aus der Liste aus, die vom Betriebssystem oder Browser angezeigt wird.  

Wenn Sie eine Vorschau der Protokollverarbeitung in Microsoft Edge Windows anzeigen möchten, navigieren Sie zu [Aktivieren](#turn-on-experimental-features) von experimentellen Features, und aktivieren Sie desktop **PWA Protocol handling**.  

Weitere Informationen zur Ausführung der Ursprungsprozedur für Protokollhandler finden Sie unter Registrieren für die Registrierung von [Web App-Protokollhandlern.][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]  

### <a name="example-manifest"></a>Beispielmanifest

In diesem Beispiel deklariert ein Web-App-Manifest, dass die App für die Verarbeitung der Protokolle und registriert `web+jngl` werden `web+jnglstore` soll.

```json
{
  "name": "Jungle",
  "description": "A plant encyclopedia",
  "protocol_handlers": [
    {
      "protocol": "web+jngl",
      "url": "/lookup?type=%s"
    },
    {
      "protocol": "web+jnglstore",
      "url": "/shop?for=%s"
    }
  ],
  "icons": [
    {
      "src": "images/icons-192.png",
      "type": "image/png",
      "sizes": "192x192"
    },
  ],
  "background_color": "#007f87",

  "display": "standalone",
  "start_url": "/",
}
```  
 
## <a name="url-link-handling"></a>URL Link Handling  

Ein uniform resource locator \(URL\) ist ein URI-Typ.  Erstellen Sie eine ansprechendere Umgebung, wenn Progressive Web Apps \(PWAs\) sich als Handler für https-URIs registrieren.  PWAs können anfordern, dass sie gestartet werden, wenn zugeordnete URIs aktiviert werden.  Wenn ein Benutzer beispielsweise einen Link zu einem Nachrichtentext aus einer E-Mail-Nachricht wählt.  Eine zugeordnete PWA zum Anzeigen von Nachrichten wird automatisch gestartet, um die Aktivierung des Links zu verarbeiten.  

Mit diesem Feature können Sie eine PWA mit dem Browser mithilfe des Web-App-Manifests registrieren und deklarieren, dass der Browser bestimmte Links verarbeitet.  Um eine PWA beim Browser zu registrieren, fügen Sie der Manifestdatei das optionale `url_handlers` Element hinzu.  Das `url_handlers` Mitglied ist ein Element, das die Ursprünge von URIs, die die `object[]` App verarbeiten möchte, gruppen.  

Die Linkbehandlung wird vom Browser mithilfe einer JSON-Datei überprüft, die `web-app-origin-association` sich am Ursprung befindet.  Die Ursprungsdatei stimmt die eingeschlossenen oder ausgeschlossenen Pfade am Ursprung weiter ab.  Ausführliche Anweisungen zum Testen des URL-Handlers finden Sie unter [PWAs as URL Handlers][GithubWicgPwaUrlHandlerBlobMainExplainerMd].  

Navigieren Sie zum Anzeigen der URL-Linkbehandlung in Microsoft Edge Windows zu [Aktivieren](#turn-on-experimental-features) experimenteller Features, und aktivieren Sie **desktop PWA URL Handling**.  

### <a name="example-of-the-url_handlers-in-the-manifest"></a>Beispiel für url_handlers im Manifest  

Der folgende Codeausschnitt ist ein Beispiel-Web-App-Manifest mit dem `url_handlers` Element.  

```json 
{
    "name": "Contoso Business App",
    "display": "standalone",
    "icons": [
        {
            "src": "images/icons-144.png",
            "type": "image/png",
            "sizes": "144x144"
        }
    ],
    "capture_links": "existing_client_event",
    "url_handlers" : [
        {
            "origin": "https://contoso.com"
        },
        {
            "origin": "https://conto.so"
        },
        {
            "origin": "https://*.contoso.com"
        }
    ]
}
```  

Ein PWA stimmt mit einem URI für die URL-Behandlung überein, wenn der URI mit einer der Ursprungszeichenfolgen in übereinstimmen und der Browser überprüft, ob der Ursprung zustimmt, dass diese App einen solchen `url_handlers` URI verarbeiten kann.  

Das Element enthält einen Ursprung, der den Bereich und andere nicht verwandte Ursprünge der anfordernden `url_handlers` PWA.  Wenn Sie URIs nicht auf denselben Bereich oder dieselbe Domäne beschränken wie die anfordernde PWA können Sie unterschiedliche Domänennamen für denselben Inhalt verwenden, sie jedoch mit demselben PWA.  

#### <a name="wildcard-matching"></a>Platzhalterabgleich  

Verwenden Sie das Platzhalterzeichen \( `*` \), um einem oder mehreren Zeichen zu entsprechen.  

Ein Platzhalterpräfix wird in Ursprungszeichenfolgen des Mitglieds verwendet, `url_handlers` um für unterschiedliche Unterdomänen zu entsprechen.  Das Präfix muss `*.` für diese Verwendung verwendet werden.  Das `https` Schema wird angenommen, wenn Sie ein Platzhalterpräfix verwenden.  

Beispielsweise ist der `url_handlers` Memberwert auf Übereinstimmungen und `*.contoso.com` `tenant.contoso.com` `www.tenant.contoso.com` festgelegt, aber nicht mit `contoso.com` .  

## <a name="window-controls-overlay-for-installed-desktop-web-apps"></a>Überlagerung von Fenstersteuerelementen für installierte Desktop-Web-Apps  

Um eine immersive Titelleiste wie eine systemeigene App für Ihre installierte Desktop-Web-App zu erstellen, werden mit der **Window Controls Overlay-Funktion** die folgenden Aktionen ausgeführt.  
    
1.  Entfernt die vom System reservierte Titelleiste.  Sie umfasst in der Regel die Breite des Clientframes.  
1.  Ersetzt sie durch eine Überlagerung.  Sie enthält nur die kritischen Fenstersteuerelemente, die für einen Benutzer erforderlich sind, um das Fenster selbst zu steuern.  
    
Nachdem eine Überlagerung zur Verfügung steht, steht Ihnen der gesamte Webclientbereich zur Verfügung.  Dieses Feature enthält eine Manifestaktualisierung.  Es bietet Ihnen Möglichkeiten, die Größe und Position der Überlagerung zu bestimmen, um Ihnen bei der Organisation von Inhalten zu helfen.  

Navigieren Sie zum Anzeigen einer Vorschau der Fenstersteuerelementüberlagerungen in Microsoft Edge für Windows 10 zu [Aktivieren](#turn-on-experimental-features) von experimentellen Features und navigieren Sie zu **Desktop-PWA-Fenstersteuerelemente-Überlagerung**.   

### <a name="examples-of-title-bar-area-customization"></a>Beispiele für die Anpassung des Titelleistenbereichs  

Dieses Feature basiert auf der Möglichkeit in nativen Apps, die Titelleiste anzupassen.  Sie können eine Titelleiste für wichtige App-Aktionen oder -Benachrichtigungen anpassen.  Lesen Sie die folgenden Beispiele für Microsoft Visual Studio Code und Microsoft Teams.  

#### <a name="visual-studio-code"></a>Visual Studio Code  

Microsoft Visual Studio Code ist ein beliebter Editor, der auf Electron baut und auf mehreren Desktopplattformen enthalten ist.  

Im folgenden Beispiel wird Visual Studio Code die Titelleiste verwendet, um die verfügbare Bildschirmimmobilie zu maximieren, um den aktuellen Dateinamen und die Menüstruktur auf oberster Ebene in die Titelleiste zu verwenden.  

:::image type="complex" source="../media/visual-studio-code-title-customization.png" alt-text="Ein Beispiel für die Titelleiste in Visual Studio Code" lightbox="../media/visual-studio-code-title-customization.png":::
   Ein Beispiel für die Titelleiste in Visual Studio Code  
:::image-end:::  

#### <a name="microsoft-teams"></a>Microsoft Teams  

Die Tools für die Zusammenarbeit und Kommunikation am Arbeitsplatz Microsoft Teams auch mit Electron erstellt und auf mehreren Desktopplattformen verfügbar.  Im folgenden Beispiel werden Microsoft Teams und `back` `forward` Navigationsschaltflächen, ein Suchfeld und Benutzerprofilsteuerelemente angezeigt.  

:::image type="complex" source="../media/teams-title-customization.png" alt-text="Ein Beispiel für die Titelleiste in Microsoft Teams" lightbox="../media/teams-title-customization.png":::
   Ein Beispiel für die Titelleiste in Microsoft Teams  
:::image-end:::  

### <a name="overlay-window-controls-on-a-frameless-window"></a>Überlagerungsfenstersteuerelemente in einem framelosen Fenster  

Um den adressierbaren Bereich für Webinhalte zu maximieren, erstellt der Browser ein frameloses Fenster.  Ein rahmenloses Fenster entfernt alle Browserbenutzeroberflächen, mit Ausnahme der als Überlagerung bereitgestellten Fenstersteuerelemente.  Mit der Überlagerung von Fenstersteuerelementen können Benutzer die App weiterhin minimieren, maximieren, wiederherstellen und schließen.  Darüber hinaus bietet es über das Web-App-Menü Zugriff auf relevante Browsersteuerelemente.  Für Chromium browser enthält die Überlagerung die folgenden Steuerelemente.  

*   Ein ziehbarer Bereich mit der gleichen Breite und Höhe der einzelnen Fenstersteuerelementschaltflächen  
*   Die **Einstellungen und mehr** \(...\)-Schaltfläche  
*   Die Schaltflächen des Fenstersteuerelements minimieren, maximieren, wiederherstellen und schließen  
    
Neben den zuvor aufgeführten Steuerelementen wird die in der Überlagerung angezeigte Benutzeroberfläche in den folgenden Szenarien dynamisch angepasst.  

*   Wenn eine installierte Web-App gestartet wird, wird der Ursprung der Webseite links vom Menü **Einstellungen** und mehr \(...\) für einige Sekunden angezeigt und wird dann ausgeblendet.  
*   Wenn ein Benutzer mithilfe des Menüs **Einstellungen** und mehr \(...\) mit einer Erweiterung interagiert, wird das Symbol der Erweiterung in der Überlagerung links neben dem Menü mit drei Punkten angezeigt.  Nachdem Sie ein Erweiterungsdialogfeld beendet haben, wird das Symbol aus der Überlagerung entfernt.  
    
| Sprachrichtung | Überlagerungsspeicherort | Details |  
|:--- |:--- |:--- |  
| Von links nach rechts \(LTR\) | Links oben im Clientbereich | Die Steuerelemente werden gekippt |  
| Von rechts nach links \(RTL\) | Obere rechte Ecke des Clientbereichs |  |  

> [!IMPORTANT]
> Die Überlagerung befindet sich immer über dem Z-Index des Webinhalts und akzeptiert alle Benutzereingaben, ohne sie an den Webinhalt weiter zu fließen.  

### <a name="working-around-the-window-controls-overlay"></a>Arbeiten an der Überlagerung von Fenstersteuerelementen  

Ihre Webinhalte müssen den reservierten Bereich für die Steuerelementüberlagerung beachten.  Stellen Sie sicher, dass der reservierte Bereich keine Benutzerinteraktion erwartet.  Fragen Sie den Browser nach dem umgebenden Rechteck und der Sichtbarkeit der Steuerelementüberlagerung.  Die Informationen werden Ihnen über JavaScript-APIs und CSS-Umgebungsvariablen bereitgestellt.  

#### <a name="javascript-apis"></a>JavaScript-APIs  

Mit einem `windowControlsOverlay` neuen Objekt in der Eigenschaft können Sie das `window.navigator` begrenzungsgebundene Rechteck der Steuerelementüberlagerung abfragen.  

Das `windowControlsOverlay` Objekt verfügt über die folgenden beiden Objekte.  

*   `getBoundingClientRect()`  gibt ein `DOMRect`-Objekt zurück.  Das `DOMRect` Objekt stellt den Bereich unter der Fenstersteuerelementüberlagerung dar.  
*   `visible` ist ein boolescher Wert, der angibt, dass die Steuerelementüberlagerung gerendert und angezeigt wird.  
    
> [!IMPORTANT]
> Aus Datenschutzgründen ist der Zugriff auf Elemente `windowControlsOverlay` `iframe` im Webinhalt nicht möglich.  

Wenn die Überlagerungsgröße geändert wird, wird ein Ereignis für das Objekt ausgeführt, um den Client zu benachrichtigen, das `geometrychange` `navigator.windowControlsOverlay` Inhaltslayout neu zu berechnen.  Das neu berechnete Inhaltslayout basiert auf dem neuen umgebenden Rechteck der Überlagerung.  

#### <a name="css-environment-variables"></a>CSS-Umgebungsvariablen  

Neben der JavaScript-API können Sie CSS zum Abfragen des umgebenden Rechtecks der Steuerelementüberlagerung verwenden.  Verwenden Sie die folgenden vier neuen CSS-Umgebungsvariablen zum Abfragen.  

*   `titlebar-area-x`  
*   `titlebar-area-y`  
*   `titlebar-area-width`  
*   `titlebar-area-height`  
    
### <a name="define-draggable-regions-in-web-content"></a>Definieren von draggable Regions in Web Content  

Benutzer erwarten, dass sie den oberen Bereich eines Fensters packen und ziehen.  Um die Erwartungen zu erfüllen, deklarieren Sie bestimmte Teile des Webinhalts als draggable.  
Um anzugeben, dass ein Element draggierbar ist, verwenden Sie die WebKit-proprietäre `-webkit-app-region` CSS-Eigenschaft.  Die CSS-Arbeitsgruppe bemüht sich weiterhin, die Eigenschaft zu `app-region` standardisieren.  

### <a name="custom-title-bar-example"></a>Beispiel für benutzerdefinierte Titelleiste  

Im folgenden Beispiel wird angezeigt, wie die neuen Features eine Web-App mit einer benutzerdefinierten Titelleiste erstellen.  

:::image type="complex" source="../media/teams-title-customization-example.png" alt-text="Beispiel für eine benutzerdefinierte Titelleiste in Microsoft Teams" lightbox="../media/teams-title-customization-example.png":::
   Beispiel für eine benutzerdefinierte Titelleiste in Microsoft Teams  
:::image-end:::  

#### <a name="manifestwebmanifest"></a>manifest.webmanifest  

Legen Sie im Manifest array `display_override` auf  `window-controls-overlay` .  Legen Sie die Farbe für die Titelleiste auf `theme_color` Ihre Auswahl an.  Legen Sie den Anzeigemodus auf einen geeigneten Fallback für den Fall ein, wenn eine oder `display_override` `window-controls-overlay` nicht unterstützt wird.  

Der folgende Codeausschnitt enthält die empfohlenen Manifestupdates.  

```json
{
  "name": "Example PWA",
  "display": "standalone",
  "display_override": [ 
    "window-controls-overlay" 
  ],
  "theme_color": "#254B85"
}
```  

### <a name="indexhtml"></a>index.html  

Die folgenden IDs stellen die beiden Hauptbereiche der Webseite dar.  

*   `titleBarContainer`  
*   `mainContent`  
    
Das Element mit der ID ist auf festgelegt, und das untergeordnete `div` `titleBar` Suchfeldelement ist auf `draggable` `input` `nonDraggable` festgelegt.  

```html
<div id="titleBar" class=" draggable">
    <span class="draggable">Example PWA</span>
    <input class="nonDraggable" type="text" placeholder="Search"></input>
</div>
```

Im Element mit der ID stellt der mit der ID den sichtbaren Teil des `div` `titleBarContainer` `div` `titleBar` Titelleistenbereichs dar.  

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>Example PWA</title>
    <link rel="stylesheet" href="style.css">
    <link rel="manifest" href="./manifest.webmanifest">
  </head>
  <body>
    <div id="titleBarContainer">
      <div id="titleBar" class=" draggable">
        <span class="draggable">Example PWA</span>
        <input class="nonDraggable" type="text" placeholder="Search"></input>
      </div>
    </div>
    <div id="mainContent"><!-- The rest of the webpage --></div>
  </body>
</html>
```  

### <a name="stylecss"></a>style.css  

Die bereiche draggable und non-draggable werden mit und `-webkit-app-region: drag` `-webkit-app-region: no-drag` festgelegt.  

```css
.draggable {
    app-region: drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: drag;
}

.nonDraggable {
    app-region: no-drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: no-drag;
}
```  

Für das Element werden Ränder festgelegt, um sicherzustellen, dass die Titelleiste bis an die Ränder `body` `0` des Fensters reicht.  

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}
```  

Die ID verwendet und legt den auf fest, der den Container am `titleBarContainer` oberen Rand der Webseite `position: absolute` `top` `titlebar-area-inset-top` anheften soll.  Der `bottom` wird auf festgelegt und fällt auf `titlebar-area-inset-bottom` `100% - var(--fallback-title-bar-height)` zurück, wenn die Fenstersteuerelementüberlagerung nicht sichtbar ist.  Die Hintergrundfarbe der `titleBarContainer` ID ist identisch mit der `theme_color` .  Die Breite ist auf festgelegt, sodass das Element die Breite der Webseite ausfüllt und unter der Überlagerung fließt, wenn es für eine zusammenhängende `100%` `div` Darstellung sichtbar ist.  

```css
#titleBarContainer {
    position: absolute;
    top: env(titlebar-area-y, 0);
    bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    width: 100%;
    background-color:#254B85;
}
```  

Die ID verwendet und fügt sie auch `titleBar` am oberen Rand des `position: absolute` `top: titlebar-area-inset-top` Fensters an.  Standardmäßig wird die volle Breite des Fensters verwendet.  The `left` and edges are set to and `right` `titlebar-area-inset-left` `titlebar-area-inset-right` respectively, both fall back to `0` when the values aren't set.  Außerdem soll verhindert werden, dass versucht wird, das verbrauchte Fenster zu ziehen, stattdessen wird `user-select: none` Text im Element `div` hervorgehoben.  

```css
#titleBar {
    position: absolute;
    top: 0;
    display: flex;
    user-select: none;
    height: 100%;
    left: env(titlebar-area-x, 0);
    right: env(titlebar-area-width, 0);
    color: #FFFFFF;
    font-weight: bold;
    text-align: center;
}

#titleBar > span {
    margin: auto;
    padding: 0px 16px 0px 16px;
}

#titleBar > input {
    flex: 1;
    margin: 8px;
    border-radius: 5px;
    border: none;
    padding: 8px;
}
```

Der Container für die ID wird ebenfalls mit fixiert und am unteren Rand `mainContent` `position: absolute` der Webseite angefügt.  Der wird auf festgelegt und fällt zurück, um den verbleibenden Platz unterhalb der `height` `titlebar-area-inset-bottom` `100% - var(--fallback-titlebar-height)` Titelleiste zu füllen.  Es wird `overflow-y: scroll` so definiert, dass der Inhalt vertikal im Container scrollen kann.  

```css
#mainContent {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    overflow-y: scroll;
}
```

In Fällen, in denen der Browser die Überlagerung von Fenstersteuerelementen nicht unterstützt, wird eine CSS-Variable hinzugefügt, um eine Standardhöhe für die Titelleiste festlegen.  Die Grenzen von und IDs werden zunächst so festgelegt, dass sie den gesamten Clientbereich füllen, und Sie müssen ihn nicht ändern, wenn die Überlagerung `titleBarContainer` `mainContent` nicht unterstützt wird.  

Der folgende Codeausschnitt enthält alle empfohlenen CSS-Updates.

```css
:root {
  --fallback-title-bar-height: 40px;
}

.draggable {
  app-region: drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: drag;
}

.nonDraggable {
  app-region: no-drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: no-drag;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  margin: 0;
}

#titleBarContainer {
  position: absolute;
  top: env(titlebar-area-y, 0);
  bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  width: 100%;
  background-color:#254B85;
}

#titleBar {
  position: absolute;
  top: 0;
  display: flex;
  user-select: none;
  height: 100%;
  left: env(titlebar-area-x, 0);
  right: env(titlebar-area-width, 0);
  color: #FFFFFF;
  font-weight: bold;
  text-align: center;
}

#titleBar > span {
  margin: auto;
  padding: 0px 16px 0px 16px;
}

#titleBar > input {
  flex: 1;
  margin: 8px;
  border-radius: 5px;
  border: none;
  padding: 8px;
}

#mainContent {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  overflow-y: scroll;
}
```  

## <a name="run-on-os-login"></a>Ausführen unter Betriebssystemanmeldung  

Mit diesem Feature können Sie Ihre App so konfigurieren, dass sie automatisch gestartet wird, wenn sich der Benutzer bei Microsoft Windows.  Mehrere Klassen von Apps nutzen die Funktion.  Zu den Klassen von Apps gehören E-Mails, Chats, Überwachungsdashboards und Echtzeit-Datenanzeige-Apps.  Die Funktion ermöglicht es einem Benutzer, sich mit den Apps zu beschäftigen, sobald sich der Benutzer beim Betriebssystem anmeldet.  Dieses Feature startet die PWA automatisch auf die gleiche Weise, wie sie manuell gestartet wird.  

> [!IMPORTANT]
> **Ausführen unter Betriebssystemanmeldung** ist ein [leistungsstarkes Feature.][GithubW3cPermissionsPowerfulFeature]  Benutzer sollten entscheiden, ob sie die Funktion für die installierte Web-App aktivieren möchten.  

### <a name="turn-on-run-on-os-login"></a>Aktivieren der Anmeldung unter Betriebssystem ausführen  

Navigieren Sie zum Anzeigen einer Vorschau der Run **On Os Login-Funktionen** für PWA zu [Aktivieren](#turn-on-experimental-features) von experimentellen Features und Aktivieren von **Desktop-PWAs,** die unter Betriebssystemanmeldung ausgeführt werden.  

:::image type="complex" source="../media/desktop-pwas-run-on-os-login-flag.png" alt-text="Aktivieren des Desktop-PWAs, das beim Betriebssystemanmeldungsexperiment ausgeführt wird" lightbox="../media/desktop-pwas-run-on-os-login-flag.png":::
   Aktivieren des **Desktop-PWAs, das beim Betriebssystemanmeldungsexperiment ausgeführt** wird  
:::image-end:::  

### <a name="turn-on-the-feature-for-the-installed-web-app"></a>Aktivieren des Features für die installierte Web-App  

Um das Feature `Start app when you sign in` für eine installierte PWA 

1.  Öffnen Sie Microsoft Edge.   
1.  Navigieren Sie zu `edge://apps`.  
1.  Zeigen Sie auf Ihre App.  
1.  Öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie dann App starten **aus, wenn Sie sich anmelden.**  
    
    :::image type="complex" source="../media/turn-on-run-on-os-login-flag.png" alt-text="Verwenden Sie das Kontextmenü, um die Start-App zu aktivieren, wenn Sie sich in der App Microsoft Edge" lightbox="../media/turn-on-run-on-os-login-flag.png":::
       Verwenden Sie das Kontextmenü, um die **Start-App** zu aktivieren, wenn Sie sich in der App Microsoft Edge  
    :::image-end:::  
    
## <a name="shortcuts"></a>Tastenkombinationen  

`Shortcuts` ist ein neues Mitglied der Manifestdatei.  Sie können Links zu Teilen, wichtigen Webseiten oder Aktionen in Ihrer Web-App definieren.  Microsoft Windows integriert es als **Jumplists**.  **Sprunglisten definieren** Popupmenüs, die angezeigt werden, wenn Sie eines der folgenden Benutzeroberflächenelemente verwenden und ein kontextbezogenes Menü \(rechtsklicken\) öffnen.  

*   Eine Kachel im Startmenü  
*   Ein Symbol auf der Taskleiste  
    
Wenn ein Benutzer eine Verknüpfung aufruft, navigiert der Benutzer zu der vom Element der `url` Verknüpfung angegebenen Adresse.  
  
:::image type="complex" source="../media/jumplists-on-windows-10.png" alt-text="Ein Beispiel für Jumplists auf Windows 10" lightbox="../media/jumplists-on-windows-10.png":::
   Ein Beispiel für **Jumplists** auf Windows 10  
:::image-end:::  

### <a name="shortcuts-in-the-manifest-file"></a>Verknüpfungen in der Manifestdatei  

```json
"shortcuts" : [
  {
    "name": "Today's agenda",
    "url": "/today",
    "description": "List of events planned for today"
  },
  {
    "name": "New event",
    "url": "/create/event"
  },
  {
    "name": "New reminder",
    "url": "/create/reminder"
  }
]
```  

#### <a name="properties-of-shortcuts"></a>Eigenschaften von Verknüpfungen  

Die folgenden Eigenschaften definieren jede Verknüpfung.  

| Eigenschaft | Details |  
|:--- |:--- |  
| `name` | Eine Zeichenfolge, die dem Benutzer auf **Sprunglisten oder** im Kontextmenü angezeigt wird. |  
| `short_name` | Eine Zeichenfolge, die angezeigt wird, wenn nicht genügend Speicherplatz vorhanden ist, um den vollständigen Namen der Verknüpfung anzeigen zu können. |  
| `description` | Eine Zeichenfolge, die den Zweck der Verknüpfung beschreibt.  Auf sie kann durch Hilfstechnologie zugegriffen werden. |  
| `url` | Der URI in der Web-App, der geöffnet wird, wenn die Verknüpfung aktiviert wird. |  
| `icons` | Eine Reihe von Symbolen, die die Verknüpfung darstellt. |  

## <a name="file-handling"></a>Dateiverarbeitung  

Die Möglichkeit, sich als Dateityphandler zu registrieren, befindet sich in der Experimentierphase.  Sie können die Dateitypen angeben, die Ihre App in einem Manifesteintrag verarbeitet.  Während der Installation registriert das Hostbetriebssystem des Benutzers Ihre App als Dateihandler für die aufgeführten Dateitypen.  Stellen Sie sicher, dass das Feature im Startcode Ihrer Apps enthalten ist und `launchQueue` die Datei verarbeitet wird.  

Chromium Browser testen und gestalten dieses Feature.  Weitere Informationen einschließlich Codebeispielen finden Sie unter [Let web applications be file handlers][WebDevFileHandling].  

Wenn Sie eine Vorschau der Dateiverarbeitung in Microsoft Edge für Windows 10 anzeigen möchten, navigieren Sie zu Aktivieren experimenteller [Features](#turn-on-experimental-features) und Aktivieren der **Dateibehandlungs-API**.  
    
## <a name="providing-feedback-on-experimental-features"></a>Bereitstellen von Feedback zu experimentellen Features  

So geben Sie Feedback zu Microsoft Edge Web-App-Experimenten.  

*   Senden Sie Ihr Feedback **Einstellungen und mehr** \( `...` \) > Feedback an Microsoft **senden.**  
*   Wählen Sie `Alt` + `Shift` + `I` aus.  
    
:::image type="complex" source="../media/send-feedback-from-progressive-web-app.png" alt-text="Senden von Feedback von PWA" lightbox="../media/send-feedback-from-progressive-web-app.png":::
   Senden von Feedback von PWA  
:::image-end:::  

<!-- links -->  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Origin Trials | Microsoft Edge Entwickler"  
[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "Registrieren für die Registrierung von Web App-Protokollhandlern | Microsoft Developer"  

[MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]: https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler/Web-based_protocol_handlers "Webbasierte Protokollhandler | MDN"  

[GithubW3cPermissionsPowerfulFeature]: https://w3c.github.io/permissions#powerful-feature "Leistungsstarkes Feature – Berechtigungen | GitHub"  

[GithubWicgPwaUrlHandlerBlobMainExplainerMd]: https://github.com/WICG/pwa-url-handler/blob/main/explainer.md "PWAs als URL Handlers | GitHub"  

[WebDevFileHandling]: https://web.dev/file-handling "Webanwendungen als Dateihandler verwenden | web.dev"  
