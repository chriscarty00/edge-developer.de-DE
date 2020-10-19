---
description: Informationen zum Erstellen einer Microsoft Edge-Erweiterung
title: Erstellen einer Erweiterung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.custom: seodec18
ms.openlocfilehash: a08fc6bd604ce810895e7103f7f6384dbedc9f78
ms.sourcegitcommit: 0bc1312a1e6a0ac37cf385201db4361fc05184fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2020
ms.locfileid: "10683651"
---
# Erstellen einer Microsoft Edge-Erweiterung  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

In diesem Leitfaden erfahren Sie, wie Sie eine Erweiterung für Microsoft Edge erstellen.  Mit dieser Beispielerweiterung können Sie bestimmte CSS für [docs.Microsoft.com][MicrosoftDocs] -Seiten manipulieren, einschließlich der Erstellung einer Manifestdatei, der Benutzeroberfläche sowie von Hintergrund-und Inhalts Skripts.  

:::image type="complex" source="../media/color-changer_header.png" alt-text="Docs.Microsoft.com Body in blau geändert":::
   Docs.Microsoft.com Body in blau geändert
:::image-end:::

<!--![Docs.microsoft.com body changed to blue][ImageColorChangerHeader]  -->  

In diesem Lernprogramm wird davon ausgegangen, dass Sie grundlegende Kenntnisse darüber haben, was eine Browser Erweiterung ist und wie Sie funktioniert.  Weitere Informationen zu den Bausteinen für Erweiterungen finden Sie unter [Anatomie einer Erweiterung][MDNAnatomyExtension].  

Laden Sie den Code für das [vollständige Beispiel auf GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger]herunter.  

## Erstellen der Manifestdatei  

Erstellen Sie zunächst ein Verzeichnis für Ihre Erweiterung, und geben Sie Ihr einen Namen `color-changer` .  

Erstellen Sie innerhalb des `color-changer` Ordners eine Datei mit dem Namen `manifest.json` .  Die `manifest.json` Datei ist für alle Erweiterungen erforderlich und enthält wichtige Informationen für die Erweiterung, die vom Namen der Erweiterung bis zu den Berechtigungen reichen.  

> [!NOTE] 
> Dieser Leitfaden führt Sie durch alle manifestschlüssel, die Sie in diesem Leitfaden verwenden müssen, aber eine Liste aller unterstützten und empfohlenen manifestschlüssel finden Sie unter [unterstützte Manifest-Schlüssel][ExtensionsApisupportManifestKeys].  

`manifest.json`Fügen Sie im Inneren den folgenden Code hinzu.  

```json
{
  &quot;name&quot;: &quot;Color Changer&quot;,
  &quot;author&quot;: &quot;Microsoft Edge Extension Developer&quot;,
  &quot;version&quot;: &quot;1.0&quot;,
  &quot;description&quot;: &quot;Change the color of the body on docs.microsoft.com&quot;,
  &quot;permissions&quot;: [
    &quot;*://docs.microsoft.com/*&quot;,
    &quot;tabs&quot;
  ], 
  &quot;browser_action&quot;: {
    &quot;default_icon&quot;: {
      &quot;20&quot;: &quot;images/color-changer20.png&quot;,
      &quot;40&quot;: &quot;images/color-changer40.png&quot;
    },
    &quot;default_title&quot;: &quot;Color Changer&quot;,
    &quot;default_popup&quot;: &quot;popup.html&quot;
  }
}
```  

### Definitionen für manifestschlüssel  

| Schlüssel | Details |  
|:--- |:--- |  
| [name][MDNManifestjsonName] | Der Name der Erweiterung.  |  
| [Autor][MDNManifestjsonAuthor] | Der Autor der Erweiterung.  |  
| [version][MDNManifestjsonVersion] | Die Versionsnummer der Erweiterung.  |  
| [description][MDNManifestjsonDescription] | Die Beschreibung der Erweiterung, die im Abschnitt &quot;Info&quot; des Menüs &quot;Erweiterung&quot; in Microsoft Edge angezeigt wird.  |  
| [Berechtigungen][MDNManifestjsonPermissions] | Ein Array von Zeichenfolgen, die Berechtigungen für die Erweiterung anfordern.  Für Ihre Erweiterung fordern Sie Berechtigungen an, um die besuchten Websites anzuzeigen \ (&quot;Registerkarten&quot; \), und um den Inhalt der URLs zu aktualisieren, die &quot; `*://docs.microsoft.com/*` " entsprechen.  |  
| [browser_action][MDNManifestjsonBrowserAction] | Enthält die Informationen für ein Symbol. Das Symbol befindet sich auf der Microsoft Edge-Symbolleiste rechts neben der Adressleiste.  |  

#### browser_action Schlüsseldefinitionen  

| Schlüssel | Details |  
|:--- |:--- |  
| `default_icon` | Das Symbol, das auf der Symbolleiste verwendet wird.  |  
| `default_title` | Der Text, der angezeigt wird, wenn ein Benutzer auf das Symbol in der Symbolleiste zeigt.  |  
| `default_popup` | Der Pfad zur HTML-Datei für das Popupfenster.  |  

Nachdem Sie die Manifestdatei erstellt haben, benötigen Sie eine Benutzeroberfläche für die Erweiterung.  

## Erstellen des Popups  

Erstellen Sie für Ihre Erweiterung ein Popup für die Benutzeroberfläche, wie unten beschrieben.  

:::image type="complex" source="../media/color-changer_popup.png" alt-text="Docs.Microsoft.com Body in blau geändert":::
   Docs.Microsoft.com Body in blau geändert
:::image-end:::

<!--![Docs.microsoft.com body changed to blue][ImageColorChangerHeader]  -->  

In diesem Lernprogramm wird davon ausgegangen, dass Sie grundlegende Kenntnisse darüber haben, was eine Browser Erweiterung ist und wie Sie funktioniert.  Weitere Informationen zu den Bausteinen für Erweiterungen finden Sie unter [Anatomie einer Erweiterung][MDNAnatomyExtension].  

Laden Sie den Code für das [vollständige Beispiel auf GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger]herunter.  

## Erstellen der Manifestdatei  

Erstellen Sie zunächst ein Verzeichnis für Ihre Erweiterung, und geben Sie Ihr einen Namen `color-changer` .  

Erstellen Sie innerhalb des `color-changer` Ordners eine Datei mit dem Namen `manifest.json` .  Die `manifest.json` Datei ist für alle Erweiterungen erforderlich und enthält wichtige Informationen für die Erweiterung, die vom Namen der Erweiterung bis zu den Berechtigungen reichen.  

> [!NOTE] 
> Dieser Leitfaden führt Sie durch alle manifestschlüssel, die Sie in diesem Leitfaden verwenden müssen, aber eine Liste aller unterstützten und empfohlenen manifestschlüssel finden Sie unter [unterstützte Manifest-Schlüssel][ExtensionsApisupportManifestKeys].  

`manifest.json`Fügen Sie im Inneren den folgenden Code hinzu.  

```json
{
  &quot;name&quot;: &quot;Color Changer&quot;,
  &quot;author&quot;: &quot;Microsoft Edge Extension Developer&quot;,
  &quot;version&quot;: &quot;1.0&quot;,
  &quot;description&quot;: &quot;Change the color of the body on docs.microsoft.com&quot;,
  &quot;permissions&quot;: [
    &quot;*://docs.microsoft.com/*&quot;,
    &quot;tabs&quot;
  ], 
  &quot;browser_action&quot;: {
    &quot;default_icon&quot;: {
      &quot;20&quot;: &quot;images/color-changer20.png&quot;,
      &quot;40&quot;: &quot;images/color-changer40.png&quot;
    },
    &quot;default_title&quot;: &quot;Color Changer&quot;,
    &quot;default_popup&quot;: &quot;popup.html&quot;
  }
}
```  

### Definitionen für manifestschlüssel  

| Schlüssel | Details |  
|:--- |:--- |  
| [name][MDNManifestjsonName] | Der Name der Erweiterung.  |  
| [Autor][MDNManifestjsonAuthor] | Der Autor der Erweiterung.  |  
| [version][MDNManifestjsonVersion] | Die Versionsnummer der Erweiterung.  |  
| [description][MDNManifestjsonDescription] | Die Beschreibung der Erweiterung, die im Abschnitt &quot;Info&quot; des Menüs &quot;Erweiterung&quot; in Microsoft Edge angezeigt wird.  |  
| [Berechtigungen][MDNManifestjsonPermissions] | Ein Array von Zeichenfolgen, die Berechtigungen für die Erweiterung anfordern.  Für Ihre Erweiterung fordern Sie Berechtigungen an, um die besuchten Websites anzuzeigen \ (&quot;Registerkarten&quot; \), und um den Inhalt der URLs zu aktualisieren, die &quot; `*://docs.microsoft.com/*` ":::
   Die Popup Schnittstelle der Erweiterung
:::image-end:::

<!--![The pop-up interface of the extension][ImageColorChangerPopup]  -->  

Erstellen Sie eine Datei mit dem Namen `popup.html` im Stammverzeichnis Ihres `color-changer` Ordners.  Fügen Sie den folgenden Code in ein `popup.html` .  

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" type="text/css" href="css/styles.css" />
    </head>
    <body>
        <h1>Creating a Microsoft Edge Extension</h1>
        <p>Color Changer</p>
        <input id="aliceblue" type="button" value="Aliceblue" />
        <input id="cornsilk" type="button" value="Cornsilk" />
        <input id="reset" type="button" value="Reset" />
        <script src="js/popup.js"></script>
    </body>
</html>
```  

In `popup.html` können Sie einen Titel, einen Absatz und drei Schaltflächen (AliceBlue, Cornsilk und Reset \) erstellen.  

Erstellen Sie nun einen Ordner mit dem Namen `css` und in Erstellen einer Datei mit dem Namen `styles.css` .  Fügen Sie die folgenden Formatvorlagen hinzu.  

```css
/* main styles */
* {
    font-family: 'Segoe UI';
}

h1 {
    font-weight: 600;
    font-size: .9em;
}

p {
    font-weight: 500;
    font-size: .8em;
    margin-bottom: 10px;  
}
```  

Dieses CSS gibt unserer Erweiterung einige einfache Formatvorlagen.  Sie können weitere Formatvorlagen hinzufügen, um Ihre Erweiterung anzupassen.  

Als nächstes müssen Sie die JavaScript-Datei erstellen, die mit dem Popup interagiert.  Erstellen Sie einen `js` Ordner und eine Datei mit dem Namen `popup.js` innen.  Aktualisieren Sie `popup.js` mit dem folgenden Code.  

```JavaScript
// get the buttons by id
let aliceblue = document.getElementById('aliceblue');
let cornsilk = document.getElementById('cornsilk');
let reset = document.getElementById('reset');

// use tabs.insertCSS to change header color on button click

// aliceblue
aliceblue.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: aliceblue !important; }"});
};

// cornsilk
cornsilk.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: cornsilk !important; }"});
};

// back to original
reset.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: none !important; }"});
};
```  

In bietet `popup.js` die [Registerkarten][MDNApiTabs] -API die Möglichkeit, mit den Registerkarten des Browsers zu interagieren und Skripts und Formatvorlagen in den Seiteninhalt einzufügen.  Mit der [Tab. insertCSS ()][MDNApiTabsInsertcss] -Methode fügen Sie das angegebene CSS in die Seite ein, wodurch die Kopfzeile von [docs.Microsoft.com][MicrosoftDocs] in eine andere Farbe geändert wird, wenn auf die angegebene Schaltfläche geklickt wird.  

Nachdem Sie nun über die grundlegenden Popup Funktionen verfügen, fügen Sie der Erweiterung Symbole hinzu.  

## Hinzufügen von Symbolen  

Symbole werden verwendet, um die Erweiterung in der Symbolleiste des Browsers, im Menüerweiterungen und an anderen Stellen darzustellen.  Laden [Sie die Symbole für Ihre Erweiterung auf GitHub][GithubMicrosoftEdgeExtensionsDemosColorChangerImages]herunter. Weitere Informationen zu Erweiterungssymbolen in Microsoft Edge finden Sie unter [Entwurfshandbuch][ExtensionsGuidesDesignIcons].  

Nachdem Sie die Erweiterungssymbole heruntergeladen haben, speichern Sie die Symbole in einem `images` Ordner in `color-changer` .  

Das Symbol, das auf der Symbolleiste angezeigt wird `default_icon` , wird innerhalb des [browser_action][MDNManifestjsonBrowserAction] Schlüssels festgesetzt, den Sie bereits zu Ihrer Manifestdatei in einem früheren Abschnitt hinzugefügt haben.  

Der `icons` Schlüssel definiert, welche Symbole in den Menüs für die Erweiterungseinstellungen verwendet werden sollen.  Im folgenden geben Sie mehrere Symbole mit unterschiedlichen Größen an, die für unterschiedliche Bildschirmauflösungen berücksichtigt werden sollen.  Der Name der Symbole `25` und `48` die Höhe der Symbole in Pixeln.  

Schließen Sie im [manifest.jsauf][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] Datei einen Schlüssel auf oberster Ebene für ein `icons` .  

```json
  "icons": {
    "25": "images/color-changer25.png",
    "48": "images/color-changer48.png"
  }
```  

### Definitionen für manifestschlüssel  

| Schlüssel | Details |  
|:--- |:--- |  
| [Symbole][MDNManifestjsonIcons] | Die Symbole für Ihre Erweiterung mit Schlüssel-Wert-Paaren der Bildgröße in `px` und Bild Pfad relativ zum Stammverzeichnis der Erweiterung. |  

> [!NOTE]
> Verwenden Sie die Symbole `inactive##.png` , die sich im Ordner "Bilder" befinden, später in diesem Leitfaden.  

## Testen der Erweiterung  

Nachdem Sie nun die Benutzeroberfläche und die erstellten Symbole hinzugefügt haben, testen Sie Ihre Erweiterung.  Führen Sie die Schritte zum [Hinzufügen einer Erweiterung][ExtensionsGuidesAddingRemovingExtensionsAdding] zu Microsoft Edge durch.  Kehren Sie anschließend zu diesem Leitfaden zurück.  

Navigieren Sie nach dem Hinzufügen der Erweiterung zu einer beliebigen [docs.Microsoft.com][MicrosoftDocs] -Seite.  Nachdem Sie auf die Browser Aktion geklickt haben, sollte das folgende Popup angezeigt werden.  Die Farbe des [docs.Microsoft.com][MicrosoftDocs] -Texts sollte auch die Farbe ändern.  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_aliceblue.png" alt-text="Docs.Microsoft.com Body in blau geändert":::
   Docs.Microsoft.com Body in blau geändert
:::image-end:::

<!--![Docs.microsoft.com body changed to blue][ImageColorChangerHeader]  -->  

In diesem Lernprogramm wird davon ausgegangen, dass Sie grundlegende Kenntnisse darüber haben, was eine Browser Erweiterung ist und wie Sie funktioniert.  Weitere Informationen zu den Bausteinen für Erweiterungen finden Sie unter [Anatomie einer Erweiterung][MDNAnatomyExtension].  

Laden Sie den Code für das [vollständige Beispiel auf GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger]herunter.  

## Erstellen der Manifestdatei  

Erstellen Sie zunächst ein Verzeichnis für Ihre Erweiterung, und geben Sie Ihr einen Namen `color-changer` .  

Erstellen Sie innerhalb des `color-changer` Ordners eine Datei mit dem Namen `manifest.json` .  Die `manifest.json` Datei ist für alle Erweiterungen erforderlich und enthält wichtige Informationen für die Erweiterung, die vom Namen der Erweiterung bis zu den Berechtigungen reichen.  

> [!NOTE] 
> Dieser Leitfaden führt Sie durch alle manifestschlüssel, die Sie in diesem Leitfaden verwenden müssen, aber eine Liste aller unterstützten und empfohlenen manifestschlüssel finden Sie unter [unterstützte Manifest-Schlüssel][ExtensionsApisupportManifestKeys].  

`manifest.json`Fügen Sie im Inneren den folgenden Code hinzu.  

```json
{
  &quot;name&quot;: &quot;Color Changer&quot;,
  &quot;author&quot;: &quot;Microsoft Edge Extension Developer&quot;,
  &quot;version&quot;: &quot;1.0&quot;,
  &quot;description&quot;: &quot;Change the color of the body on docs.microsoft.com&quot;,
  &quot;permissions&quot;: [
    &quot;*://docs.microsoft.com/*&quot;,
    &quot;tabs&quot;
  ], 
  &quot;browser_action&quot;: {
    &quot;default_icon&quot;: {
      &quot;20&quot;: &quot;images/color-changer20.png&quot;,
      &quot;40&quot;: &quot;images/color-changer40.png&quot;
    },
    &quot;default_title&quot;: &quot;Color Changer&quot;,
    &quot;default_popup&quot;: &quot;popup.html&quot;
  }
}
```  

### Definitionen für manifestschlüssel  

| Schlüssel | Details |  
|:--- |:--- |  
| [name][MDNManifestjsonName] | Der Name der Erweiterung.  |  
| [Autor][MDNManifestjsonAuthor] | Der Autor der Erweiterung.  |  
| [version][MDNManifestjsonVersion] | Die Versionsnummer der Erweiterung.  |  
| [description][MDNManifestjsonDescription] | Die Beschreibung der Erweiterung, die im Abschnitt &quot;Info&quot; des Menüs &quot;Erweiterung&quot; in Microsoft Edge angezeigt wird.  |  
| [Berechtigungen][MDNManifestjsonPermissions] | Ein Array von Zeichenfolgen, die Berechtigungen für die Erweiterung anfordern.  Für Ihre Erweiterung fordern Sie Berechtigungen an, um die besuchten Websites anzuzeigen \ (&quot;Registerkarten&quot; \), und um den Inhalt der URLs zu aktualisieren, die &quot; `*://docs.microsoft.com/*` ":::
         Docs.Microsoft.com-Kopfzeile geändert in AliceBlue :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Aliceblue][ImageColorChangerHeaderAliceblue]  -->
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_cornsilk.png" alt-text="Docs.Microsoft.com Body in blau geändert":::
   Docs.Microsoft.com Body in blau geändert
:::image-end:::

<!--![Docs.microsoft.com body changed to blue][ImageColorChangerHeader]  -->  

In diesem Lernprogramm wird davon ausgegangen, dass Sie grundlegende Kenntnisse darüber haben, was eine Browser Erweiterung ist und wie Sie funktioniert.  Weitere Informationen zu den Bausteinen für Erweiterungen finden Sie unter [Anatomie einer Erweiterung][MDNAnatomyExtension].  

Laden Sie den Code für das [vollständige Beispiel auf GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger]herunter.  

## Erstellen der Manifestdatei  

Erstellen Sie zunächst ein Verzeichnis für Ihre Erweiterung, und geben Sie Ihr einen Namen `color-changer` .  

Erstellen Sie innerhalb des `color-changer` Ordners eine Datei mit dem Namen `manifest.json` .  Die `manifest.json` Datei ist für alle Erweiterungen erforderlich und enthält wichtige Informationen für die Erweiterung, die vom Namen der Erweiterung bis zu den Berechtigungen reichen.  

> [!NOTE] 
> Dieser Leitfaden führt Sie durch alle manifestschlüssel, die Sie in diesem Leitfaden verwenden müssen, aber eine Liste aller unterstützten und empfohlenen manifestschlüssel finden Sie unter [unterstützte Manifest-Schlüssel][ExtensionsApisupportManifestKeys].  

`manifest.json`Fügen Sie im Inneren den folgenden Code hinzu.  

```json
{
  &quot;name&quot;: &quot;Color Changer&quot;,
  &quot;author&quot;: &quot;Microsoft Edge Extension Developer&quot;,
  &quot;version&quot;: &quot;1.0&quot;,
  &quot;description&quot;: &quot;Change the color of the body on docs.microsoft.com&quot;,
  &quot;permissions&quot;: [
    &quot;*://docs.microsoft.com/*&quot;,
    &quot;tabs&quot;
  ], 
  &quot;browser_action&quot;: {
    &quot;default_icon&quot;: {
      &quot;20&quot;: &quot;images/color-changer20.png&quot;,
      &quot;40&quot;: &quot;images/color-changer40.png&quot;
    },
    &quot;default_title&quot;: &quot;Color Changer&quot;,
    &quot;default_popup&quot;: &quot;popup.html&quot;
  }
}
```  

### Definitionen für manifestschlüssel  

| Schlüssel | Details |  
|:--- |:--- |  
| [name][MDNManifestjsonName] | Der Name der Erweiterung.  |  
| [Autor][MDNManifestjsonAuthor] | Der Autor der Erweiterung.  |  
| [version][MDNManifestjsonVersion] | Die Versionsnummer der Erweiterung.  |  
| [description][MDNManifestjsonDescription] | Die Beschreibung der Erweiterung, die im Abschnitt &quot;Info&quot; des Menüs &quot;Erweiterung&quot; in Microsoft Edge angezeigt wird.  |  
| [Berechtigungen][MDNManifestjsonPermissions] | Ein Array von Zeichenfolgen, die Berechtigungen für die Erweiterung anfordern.  Für Ihre Erweiterung fordern Sie Berechtigungen an, um die besuchten Websites anzuzeigen \ (&quot;Registerkarten&quot; \), und um den Inhalt der URLs zu aktualisieren, die &quot; `*://docs.microsoft.com/*` ":::
         Docs.Microsoft.com-Kopfzeile geändert in Cornsilk :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Cornsilk][ImageColorChangerHeaderCornsilk]  -->
   :::column-end:::
:::row-end:::

Wenn Fehler oder Funktionen auftreten, die nicht funktionieren, lesen Sie den Leitfaden zum [Debuggen von Erweiterungen][ExtensionsGuidesDebuggingExtensions] , oder laden Sie das [vollständige Beispiel auf GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger]herunter.  

## Hinzufügen von Inhalten und hintergrundskripts  

Gehen Sie einen Schritt weiter und fügen Sie Logik hinzu, um die Erweiterung von der Arbeit an Seiten außerhalb der [docs.Microsoft.com][MicrosoftDocs] -Domäne zu deaktivieren.  

Sie müssen zuerst ein [Inhalts Skript][MDNContentScripts]erstellen.  Als nächstes müssen Sie Inhalts Skripts erstellen, die im Kontext einer bestimmten Webseite ausgeführt werden, in der Lage sind, auf den Inhalt einer Webseite zuzugreifen, und die in der Lage sind, mit hintergrundskripts zu kommunizieren.  Erstellen Sie in Ihrem `js` Verzeichnis eine Datei mit dem Namen, `content.js` und fügen Sie den folgenden Code hinzu.  

```javascript
// get the URL of the page
var url = document.location.href;

// if not on a docs.microsoft.com domain
if (url.indexOf("//docs.microsoft.com") === -1) {
    // send inactive icons
    browser.runtime.sendMessage({
        "iconPath20": "images/inactive20.png",
        "iconPath40": "images/inactive40.png"
    });
}
```  

Dieses Skript ruft die URL der aktuellen Seite ab `document.location.href` und überprüft, ob sich die aktuelle Seite in der [docs.Microsoft.com][MicrosoftDocs] -Domäne befindet.  Wenn sich die Seite nicht in der [docs.Microsoft.com][MicrosoftDocs] -Domäne befindet \ (beispielsweise  [https://www.bing.com/][|::ref1::|] \), werden die Pfade zu den inaktiven Symbolen \ (abgeblendete Symbole \) mithilfe von [Runtime. SendMessage ()][MDNApiRuntimeSendmessage]an das Hintergrundskript gesendet.  

Sie müssen die [manifest.jsauf][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] Datei aktualisieren, um den folgenden `content_scripts` Schlüssel einzubeziehen.  

```json
  "content_scripts": [{
    "matches": [
        "<all_urls>"
    ],
    "js": ["js/content.js"],
    "run_at": "document_end"
}]
```  

### Definitionen für manifestschlüssel  

| Schlüssel | Details |  
|:--- |:---- |  
| [content_scripts][MDNManifestjsonContentScripts] | Enthält die Informationen dazu, welche Inhalts Skripts vom Browser geladen werden sollen. |  

#### content_scripts Schlüsseldefinitionen  

| Schlüssel | Details |  
|:--- |:---- |  
| `matches` \ (erforderlich \) | Das URL-Muster, das vor dem Laden des Inhalts Skripts übereinstimmen soll. |  
| `js` | Das Skript, das auf übereinstimmende URLs geladen werden soll. |  
| `run_at` | Gibt an, wo die JavaScript-Dateien aus dem `js` Schlüssel eingefügt werden. |  

Als nächstes müssen Sie ein [Hintergrundskript][MDNAnatomyExtensionBackgroundScripts]erstellen.  Hintergrundskripts werden im Hintergrund des Browsers ausgeführt, unabhängig von der Lebensdauer einer Webseite oder eines Browserfensters ausgeführt und können mit Inhalts Skripts kommunizieren.  

Erstellen Sie innerhalb Ihres `js` Ordners eine Datei mit dem Namen, `background.js` und fügen Sie den folgenden Code hinzu.  

```javascript
// listen for sendMessage() from content script
browser.runtime.onMessage.addListener(
    function (request, sender, sendResponse) {
        // set the icon for the browser action from sendMessage() in content script
        browser.browserAction.setIcon({
            path: {
                "20": request.iconPath20,
                "40": request.iconPath40
            },
            tabId: sender.tab.id
        });
        // disable browser action for the current tab
        browser.browserAction.disable(sender.tab.id);
    });
```  

Die [Runtime. onMessage][MDNApiRuntimeOnmessage] -Methode wartet auf [Runtime. SendMessage ()][MDNApiRuntimeSendmessage] aus dem Inhalts Skript.  Wenn die Domäne der Seite nicht [docs.Microsoft.com][MicrosoftDocs]ist, legt die [Browser-Methode. SetIcon ()][MDNApiBrowseractionSeticon] -Methode die Symbolpfade auf die inaktiven Bilder fest.  

Das Skript deaktiviert auch die Browser Aktion \ (BrowserAction[. Disable][MDApiBrowseractionDisable]\), damit Benutzer nicht in der Lage sind, auf die Browser Aktion außerhalb einer [docs.Microsoft.com][MicrosoftDocs] -Seite zu klicken.  

Sie müssen das Hintergrundskript zur Datei [manifest.js][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] hinzufügen.  Fügen Sie dem `background` Manifest den folgenden Schlüssel hinzu.  

```json
"background": {
    "scripts": ["js/background.js"],
    "persistent": true
  }
```  

### Definitionen für manifestschlüssel  

| Schlüssel | Details|  
|:--- |:--- |  
| [Hintergrund][MDNManifestjsonBackground] | Enthält die hintergrundskripts. |  

#### Definitionen für den Hintergrund Schlüssel  

| Schlüssel | Details |  
|:--- |:--- |  
| `scripts` | Der Pfad zu einer JavaScript-Datei. |  
| `persistent` (erforderlich) | Dieser muss auf oder eingestellt `true` sein `false` .  Wenn Sie auf gesetzt `true` ist, wird das Hintergrundskript geladen und für den gesamten Browsing-Abschnitt beibehalten.  Wenn Sie auf gesetzt `false` ist, wird das Hintergrundskript mit einer Verzögerung geladen und für die Browsersitzung beibehalten. |  

Laden Sie Ihre Erweiterung erneut, und testen Sie Sie erneut.  So laden Sie Ihre Erweiterung erneut: Klicken Sie auf die **Optionen für Einstellungen** und mehr in Microsoft Edge, klicken Sie auf **Erweiterungen**, klicken Sie auf Ihre Durchwahl \ (**Farbwechsler**\), und klicken Sie auf **Erweiterung erneut laden**.  

Öffnen Sie nun eine neue Registerkarte, oder aktualisieren Sie eine vorhandene Registerkarte, bei der es sich nicht um eine [docs.Microsoft.com][MicrosoftDocs] -Seite handelt.  Sie sollten das Symbol inaktiv sehen und nicht auf die Browser Aktion klicken können.  

Herzlichen Glückwunsch!  Sie haben eine Erweiterung für Microsoft Edge erstellt!  Sehen Sie [sich das vollständige Beispiel auf GitHub an][GithubMicrosoftEdgeExtensionsDemosColorChanger].  Lesen Sie weiter, um mehr über Erweiterungen zu erfahren.  

## Schreiben einer komplexeren Erweiterung  

Möchten Sie eine komplexere Erweiterung erstellen?  Sehen Sie sich die Beastify-Erweiterung auf MDN im Artikel, [ihrer zweiten Erweiterung][MDNYourSecondWebextension], an.  Das Erweiterungsmodell für Microsoft Edge weicht etwas vom Erweiterungsmodell für Firefox ab, die in [ihrer zweiten Erweiterung][MDNYourSecondWebextension] erstellte Beastify-Erweiterung wurde an die Funktion in Microsoft Edge angepasst.  Überprüfen Sie es auf [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].  

Beachten Sie beim Durchlaufen des Artikels zu MDN, [ihrer zweiten Erweiterung][MDNYourSecondWebextension], die folgenden Abschnitte.  

### APIs  

Eine Liste der unterstützten Erweiterungen-APIs in Microsoft Edge finden Sie auf der Seite [unterstützte APIs][ExtensionsAPIsupportApis] .  

### Symbolgrößen  

Die bevorzugten Erweiterungssymbol Größen für Microsoft Edge sind,, `20px` `25px` `30px` und `40px` .  Weitere unterstützte Größen sind `19px` , `35px` und `38px` .  Weitere Informationen zu Symbolgrößen und bewährten Methoden finden Sie im [Design][ExtensionsGuidesDesign] Handbuch.  

### JavaScript  

Das Erweiterungsmodell für Microsoft Edge unterstützt keine JavaScript-Versprechungen.  Verwenden Sie stattdessen Rückrufe.  Weitere Beispiele für die Verwendung von Rückrufen in einer Erweiterung finden Sie in den Demos zu  [Schnelldruck][GithubMicrosoftEdgeExtensionsDemosQuickPrint] und [Text Austausch][GithubMicrosoftEdgeExtensionsDemosTextSwap] .  

Navigieren Sie im folgenden Video zum [Schnelldruck][GithubMicrosoftEdgeExtensionsDemosQuickPrint] -Beispiel.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Adding-a-Background-Script-to-you-Edge-Extension/player]  

### Manifest.jsein  

*   Der `author` Schlüssel ist in Microsoft Edge erforderlich.  
*   Der `activeTab` Schlüssel wird in Microsoft Edge nicht unterstützt.  

Weitere Informationen zu [Browser Erweiterungen][MDNBrowserExtensions]finden Sie unter [MDN Web docs][MDNWebDocs].  

<!-- image links -->  

<!--[ImageColorChangerHeader]: ../media/color-changer_header.png "Docs.microsoft.com body changed to blue"  -->  
<!--[ImageColorChangerPopup]: ../media/color-changer_popup.png "The pop-up interface of the extension"  -->  
<!--[ImageColorChangerHeaderAliceblue]: ../media/color-changer_header_aliceblue.png "[Docs.microsoft.com header changed to Aliceblue"  -->  
<!--[ImageColorChangerHeaderCornsilk]: ../media/color-changer_header_cornsilk.png "Docs.microsoft.com header changed to Cornsilk"  -->  

<!-- links -->  

[ExtensionsGuidesAddingRemovingExtensionsAdding]: ./adding-and-removing-extensions.md#adding-an-extension "Hinzufügen einer Erweiterung – hinzufügen, verschieben und Entfernen von Erweiterungen für Microsoft Edge | Microsoft docs"  
[ExtensionsGuidesDebuggingExtensions]: ./debugging-extensions.md "Debugging-Erweiterungen | Microsoft docs"  
[ExtensionsGuidesDesign]: ./design.md "Entwurfsrichtlinien für Microsoft Edge-Erweiterungen | Microsoft docs"  
[ExtensionsGuidesDesignIcons]: ./design.md#icons "Symbole – Entwurfsrichtlinien für Microsoft Edge-Erweiterungen | Microsoft docs"  
[ExtensionsAPIsupportApis]: ../api-support/supported-apis.md " Unterstützte APIs | Microsoft docs"  
[ExtensionsApisupportManifestKeys]: ../api-support/supported-manifest-keys.md "Unterstützte manifestschlüssel | Microsoft docs"  

[MicrosoftDocs]: https://docs.microsoft.com "Microsoft docs"  

[MDNWebDocs]: https://developer.mozilla.org "MDN Web docs"  
[MDNBrowserExtensions]: https://developer.mozilla.org/Add-ons/WebExtensions "Browser-Erweiterungen | MDN"  
[MDNAnatomyExtension]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension "Anatomie einer Erweiterung | MDN"  
[MDNAnatomyExtensionBackgroundScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension#Background_scripts "Hintergrundskripts – Anatomie einer Erweiterung | MDN"  
[MDApiBrowseractionDisable]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/disable "Browser-Funktion. Disable ()-API | MDN" 
[MDNApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "BrowserControl. SetIcon ()-API | MDN"  
[MDNApiRuntimeOnmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onmessage "Runtime. onMessage-API | MDN"  
[MDNApiRuntimeSendmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage "Runtime. SendMessage ()-API | MDN"  
[MDNApiTabs]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs "Registerkarten-API | MDN"  
[MDNApiTabsInsertcss]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/insertCSS "Tabs. insertCSS ()-API | MDN"  
[MDNContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Inhalts Skripts | MDN"  
[MDNManifestjsonAuthor]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author "Autor-manifest.jsauf | MDN"  
[MDNManifestjsonBackground]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/background "Background-manifest.jsauf | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/browser_action "browser_action-manifest.js| MDN"  
[MDNManifestjsonContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_scripts "content_scripts-manifest.js| MDN"  
[MDNManifestjsonDescription]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/description "Beschreibung-manifest.jsauf | MDN"  
[MDNManifestjsonIcons]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/icons "Symbole – manifest.jsauf | MDN"  
[MDNManifestjsonName]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/name "Name-manifest.jsauf | MDN"  
[MDNManifestjsonPermissions]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions "Berechtigungen – manifest.jsauf | MDN"  
[MDNManifestjsonVersion]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/version "Version-manifest.jsauf | MDN"  
[MDNYourSecondWebextension]: https://developer.mozilla.org/Add-ons/WebExtensions/Your_second_WebExtension "Ihre zweite Durchwahl | MDN"  

[Bing]: https://www.bing.com "Bing"  

[GithubMicrosoftEdgeExtensionsDemosBeastify]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/beastify_edge "Beastify-MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChanger]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer "Farbwechsler-MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerImages]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer/images "Bilder-Farbwechsler-MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/color_changer/manifest.json "Manifest.json-Color Changer-MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosQuickPrint]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/quick_print "Schnelldruck-MicrosoftEdge/MicrosoftEdge-Erweiterungen-Demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosTextSwap]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/text_swap "Text Austausch-MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
