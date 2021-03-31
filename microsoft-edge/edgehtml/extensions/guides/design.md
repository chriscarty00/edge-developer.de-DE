---
description: Informieren Sie sich über die verschiedenen Entwurfsaspekte und das Benutzeroberflächenverhalten, die beim Erstellen von Microsoft Edge-Erweiterungen zu berücksichtigen sind.
title: Erweiterungen – Entwurf
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, JavaScript, Design, Symbole, Entwickler
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a32223f93baf44d2ca523e92cf9d7584ad9a8333
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234181"
---
# Entwurfsrichtlinien für Microsoft Edge-Erweiterungen  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Die folgende Seite enthält verschiedene Entwurfsaspekte und Benutzeroberflächenverhalten, die beim Erstellen von Microsoft Edge-Erweiterungen zu berücksichtigen sind.  

## Symbole  

Sie sollten die Symbole ihrer Erweiterung mithilfe einer Vektorgrafik erstellen.  Sie müssen ein paar unterschiedliche Größen Ihres Symbols für Ihre Erweiterung und drei zusätzliche Größen erstellen, wenn Sie Ihre Erweiterung verpacken möchten.  Microsoft Edge-Erweiterungen unterstützen keine SVG-Symbole.  

Bevor Sie Ihre Erweiterungssymbole erstellen, sollten Sie den Leitfaden zur [Barrierefreiheit][ExtensionsGuidesAccessibility] überprüfen, um sicherzustellen, dass Ihre Symbole einen hohen Kontrast aufweisen und sowohl in hellen als auch in dunklen Designs von Microsoft Edge sichtbar sind.  

Während ein WebKit-Bildformat unterstützt wird, werden PNG-Symbole für die Transparenz Unterstützung empfohlen.  

### Symbole für Ihre Erweiterung  

Für Ihre Erweiterung müssen Sie eine Symbolgröße für die Browser Aktion oder Seiten Aktion und eine Symbolgröße für den Bereich " **Erweiterungen** " erstellen.  Es können mehr als eine Größe für die einzelnen Größen zur Unterstützung von Displays mit höherer Auflösung bereitgestellt werden.  

Eine Erweiterung sollte über eine Browser Aktion oder ein Symbol für eine Seiten Aktion verfügen.  Die Browser Aktion-und Seiten Aktionssymbole können zur Laufzeit mithilfe der [BrowserAction. SetIcon][MSDApiBrowseractionSeticon] -Methode oder der [PageAction. SetIcon][MDNApiPageactionSeticon] -Methode geändert werden.  

#### Browser Aktion  

Die bevorzugten Größen für Browser Aktion und Seiten Aktionssymbole sind `20px` , `25px` , `30px` und `40px` .  Zu den anderen unterstützten Größen gehören `19px` , `35px` und `38px` .  

Die folgende [manifest.jsim][ExtensionsApisupportManifestkeys] Datei-Snippet zeigt ein Standard-und HD-Browser-Aktionssymbol, das mit dem [browser_action][MDNManifestjsonBrowserAction] -Schlüssel angegeben wird.  Für den [page_action][MDNManifestjsonPageAction] -Schlüssel gilt dieselbe Syntax.  

```json
"browser_action": {
    "default_icon": {
        "20": "images/icon_20.png",
        "40": "images/icon_40.png"
    },
    "default_title": "Fetch page info",
    "default_popup": "popup.html"
}
```  

Wenn die Browser Aktion durch die Erweiterung eingestellt wurde, wird Sie entweder im Menü Aktionen nach dem Auswählen von **mehr (...)** oder rechts neben der Adressleiste angezeigt, wenn der Benutzer die **Schaltfläche "anzeigen" neben der Adressleiste** aktiviert hat.  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/actionmenu-browseraction.png" alt-text="Browser Aktion im Menü ' Aktion '":::
         Browser Aktion im Menü ' Aktion ' :::image-end:::
      
      <!--![browser action in action menu][ImageActionmenuBrowseraction]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/browseractionicon.png" alt-text="Browser Aktion":::
         Browser Aktion :::image-end:::
      
      <!--![browser action][ImageBrowserActionIcon]  -->  
   :::column-end:::
:::row-end:::

#### Seiten Aktion  

Der [page_action][MDNManifestjsonPageAction] -Schlüssel hat dieselbe JSON-Manifest-Syntax wie der [browser_action][MDNManifestjsonBrowserAction] -Schlüssel.  Die Seiten Aktion weist auch die gleichen Symbolgrößen Anforderungen wie Browser Aktion auf.  

Wenn die Seiten Aktion in der Datei " [manifest.js][ExtensionsApisupportManifestkeys] " angegeben ist, wird Sie in der Adressleiste angezeigt, wenn die [PageAction. Show][MDNApiPageactionShow] -Methode verwendet wird.  

:::image type="complex" source="../media/pageaction.png" alt-text="Seiten Aktion":::
   Seiten Aktion
:::image-end:::

<!--![page action][ImagePageaction]  -->  

##### Verwaltungsoberfläche  

Wenn Benutzer zum Bereich "Erweiterungen" navigieren, indem Sie im Menü **mehr (.** ..) und dann auf **Erweiterungen**klicken, wird neben dem Namen der Erweiterung ein Symbol angezeigt.  

Sie sollten die folgenden Symbolgrößen angeben.  

| Schlüssel | Details |  
|:--- |:--- |  
| `48px` | Das Symbol für die Standardauflösung wird angezeigt. |  
| `128px` | Symbol für Displays mit höherer Auflösung. |  
| `176px` | Das Symbol für eine noch höhere Auflösung wird angezeigt. |  


```json
"icons": {
    "48": "images/icon_48.png",
    "128": "images/icon_128.png",
    "176": "images/icon_176.png"
},
```  

:::image type="complex" source="../media/management-ui.png" alt-text="Verwaltungsoberfläche":::
   Verwaltungsoberfläche
:::image-end:::

<!--![management UI][ImageManagementUi]  -->  

### Symbole für Verpackungen  

Sobald Ihre Erweiterung für die Verpackung bereit ist, müssen Sie drei weitere Symbolgrößen bereithalten.  

| Size | Details |  
|:--- |:--- |  
| 44px | Wird in der Windows-Benutzeroberfläche verwendet \(**App-Liste**, **Einstellungen**  \>  **System**-  \>  **apps & Funktionen**\). |  
| 50px | Verpackungsanforderung \(nirgendwo sichtbar \). |  
| 150px | Wird als Symbol für den Microsoft Store verwendet. |  


Sehen Sie sich entweder den Leitfaden für [Manuelle Verpackungen][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] oder das [ManifoldJS-verpackungshandbuch][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] an, um festzustellen, wo diese Symbole plaziert sind.  Dies hängt davon ab, welche Verpackungsmethode Sie auswählen.  

#### Symbol für Microsoft Store  

Wenn das 150px-Symbol für den Microsoft Store über einen transparenten Hintergrund verfügt, wird die Akzentfarbe des Geräts des Benutzers als Hintergrundfarbe des Symbols angezeigt.  

Wenn ein Benutzer beispielsweise Rosa als Akzentfarbe ausgewählt hat, wird der transparente Hintergrund des Store-Symbols als Rosa angezeigt.  

:::row:::
   :::column span="1":::
       :::image type="complex" source="../media/windows-accent-color.png" alt-text="Windows-Akzentfarbe":::
          Windows-Akzentfarbe :::image-end:::
       
       <!--![Windows accent color][ImageWindowsAccentColor]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/store-icon-with-transparent-background.png" alt-text="Automatisch ausgewählte Hintergrundfarbe":::
         Automatisch ausgewählte Hintergrundfarbe :::image-end:::
      
      <!--![Background color auto selected][ImageStoreIconTransparencyBackground]  -->  
   :::column-end:::
:::row-end:::

Wenn Sie Ihre eigene Hintergrundfarbe für Ihren Microsoft Store aussuchen möchten, müssen Sie den Hintergrund undurchsichtig machen.  

> [!NOTE]
> Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion.  [Kontaktieren Sie uns][AkaExtensionRequest] mit Ihren Anforderungen für den Microsoft Store, und Ihre Anfrage wird für ein zukünftiges Update in Betracht gezogen.  

<!-- image links -->  

<!--[ImageActionmenuBrowseraction]: ../media/actionmenu-browseraction.png "browser action in action menu"  -->  
<!--[ImageBrowserActionIcon]: ../media/browseractionicon.png "browser action"  -->  
<!--[ImagePageaction]: ../media/pageaction.png "page action"  -->  
<!--[ImageManagementUi]: ../media/management-ui.png "management UI"  -->  
<!--[ImageWindowsAccentColor]: ../media/windows-accent-color.png "Windows accent color"  -->  
<!--[ImageStoreIconTransparencyBackground]: ../media/store-icon-with-transparent-background.png "Background color auto selected"  -->  

<!-- links -->  

[ExtensionsGuidesAccessibility]: ./accessibility.md "Barrierefreiheit | Microsoft docs"  
[ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder]: ./packaging/creating-and-testing-extension-packages.md#assets-folder "Ordner "Objekte" – erstellen und Testen eines Microsoft Edge Extension AppX-Pakets | Microsoft docs"  
[ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs]: ./packaging/using-manifoldjs-to-package-extensions.md#packaging-with-manifoldjs "Verpacken mit ManifoldJS – Verwenden von ManifoldJS zum Erstellen von Erweiterungs AppX-Paketen | Microsoft docs"  

[ExtensionsApisupportManifestkeys]: ../API-support/supported-manifest-keys.md "Unterstützte manifestschlüssel | Microsoft docs"  

[AkaExtensionRequest]: https://aka.ms/extension-request "Erreichen Sie uns"  

[MSDApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "BrowserControl. SetIcon ()-API | MDN"  
[MDNApiPageactionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/pageAction/setIcon "pagestyle. SetIcon ()-API | MDN"  
[MDNApiPageactionShow]: https://developer.mozilla.org/Add-ons/WebExtensions/API/pageAction/show "pagestyle. Show ()-API | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/browser_action "browser_action-manifest.js| MDN"  
[MDNManifestjsonPageAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action "page_action-manifest.js| MDN"  
