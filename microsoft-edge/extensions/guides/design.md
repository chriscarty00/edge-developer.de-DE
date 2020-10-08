---
description: Informieren Sie sich über die verschiedenen Entwurfsaspekte und das Benutzeroberflächenverhalten, die beim Erstellen von Microsoft Edge-Erweiterungen zu berücksichtigen sind.
title: Erweiterungen – Entwurf
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, JavaScript, Design, Symbole, Entwickler
ms.openlocfilehash: 622d72453ea3ecd2897efcf8f67e1b2aa7a0937c
ms.sourcegitcommit: da768193c7ae7b611f4fbb1746f16d9818e42bac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684064"
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
      :::image type="complex" source="../media/browseractionicon.png" alt-text="Browser Aktion im Menü ' Aktion '" angegeben ist, wird Sie in der Adressleiste angezeigt, wenn die [PageAction. Show][MDNApiPageactionShow] -Methode verwendet wird.  

:::image type="complex" source="../media/pageaction.png" alt-text="Browser Aktion im Menü ' Aktion '"
},
```  

:::image type="complex" source="../media/management-ui.png" alt-text="Browser Aktion im Menü ' Aktion '":::
   Verwaltungsoberfläche
:::image-end:::

<!--![management UI][ImageManagementUi]  -->  

### Symbole für Verpackungen  

Sobald Ihre Erweiterung für die Verpackung bereit ist, müssen Sie drei weitere Symbolgrößen bereithalten.  

| Size | Details |  
|:--- |:--- |  
| 44px | Wird in der Windows-Benutzeroberfläche verwendet \ (**App-Liste**, **Einstellungen**  \>  **System**-  \>  **apps & Funktionen**\). |  
| 50px | Verpackungsanforderung \ (nirgendwo sichtbar \). |  
| 150px | Wird als Symbol für den Microsoft Store verwendet. |  


Sehen Sie sich entweder den Leitfaden für [Manuelle Verpackungen][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] oder das [ManifoldJS-verpackungshandbuch][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] an, um festzustellen, wo diese Symbole plaziert sind.  Dies hängt davon ab, welche Verpackungsmethode Sie auswählen.  

#### Symbol für Microsoft Store  

Wenn das 150px-Symbol für den Microsoft Store über einen transparenten Hintergrund verfügt, wird die Akzentfarbe des Geräts des Benutzers als Hintergrundfarbe des Symbols angezeigt.  

Wenn ein Benutzer beispielsweise Rosa als Akzentfarbe ausgewählt hat, wird der transparente Hintergrund des Store-Symbols als Rosa angezeigt.  

:::row:::
   :::column span="1":::
       :::image type="complex" source="../media/windows-accent-color.png" alt-text="Browser Aktion im Menü ' Aktion '":::
          Windows-Akzentfarbe :::image-end:::
       
       <!--![Windows accent color][ImageWindowsAccentColor]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/store-icon-with-transparent-background.png" alt-text="Browser Aktion im Menü ' Aktion '"  
