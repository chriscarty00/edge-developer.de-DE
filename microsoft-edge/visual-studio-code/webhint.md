---
description: Verwenden von webhint in Visual Studio-Code
title: webhint vs-Code Erweiterung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, vs-Code, Visual Studio-Code, webhint
ms.openlocfilehash: ec218fab8cbfb8181a0416c8e0eadc0e00412529
ms.sourcegitcommit: c1b5fdd48d39d874a76c9b8f68309eb1b507fd0b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "10695859"
---
# Webhint vs-Code Erweiterung  

Verwenden Sie [webhint][WebhintMain], ein anpassbares linting-Tool, um die Barrierefreiheit, die Leistung, die browserübergreifende Kompatibilität, die PWA-Kompatibilität und die Sicherheit Ihrer Website zu verbessern.  Sie überprüft Ihren Code auf bewährte Methoden und häufige Fehler. Dieses Open-Source-Projekt, das ursprünglich vom Microsoft Edge-Team entwickelt wurde, ist jetzt Teil der [OpenJS-Foundation][OpenjsFoundation].  Das Microsoft Edge-Team trägt weiterhin zu webhint neben Webentwicklern in der Community bei.  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Screenshot der webhint vs-Code Erweiterung&quot;:::
   Screenshot der webhint vs-Code Erweiterung  
:::image-end:::

<!--![Screenshot of webhint VS Code extension][ImageWebhintExtension]  -->  

Identifizieren und beheben Sie Probleme in HTML, CSS, JavaScript, Manuskript und mehr, indem Sie die [webhint-Erweiterung für vs-Code][VisualstudioMarketplaceWebhint]hinzufügen.  Hinweise werden als Inline Unterstriche angezeigt und im **Problem** Bereich zusammengefasst.  

## Konfiguration  

Diese Erweiterung verwendet eine JSON- [Standard][GithubWebhintioIndexjson] Datei, die Hinweise und Parser für HTML, CSS, Vorlagen Systeme \ (jsx/TSX, eckig usw. \), JavaScript/schreibscript und vieles mehr aktiviert.  

```json
{
    &quot;connector&quot;: &quot;local&quot;,
    &quot;extends&quot;: [
        &quot;accessibility&quot;,
        &quot;progressive-web-apps&quot;
    ],
    &quot;formatters&quot;: [
        &quot;html&quot;,
        &quot;summary&quot;
    ],
    &quot;hints&quot;: [
        &quot;apple-touch-icons&quot;,
        &quot;button-type&quot;,
        &quot;compat-api/css&quot;,
        &quot;compat-api/html&quot;,
        &quot;create-element-svg&quot;,
        &quot;css-prefix-order&quot;,
        &quot;disown-opener&quot;,
        &quot;highest-available-document-mode&quot;,
        &quot;manifest-exists&quot;,
        &quot;meta-charset-utf-8&quot;,
        &quot;meta-viewport&quot;,
        &quot;no-bom&quot;,
        &quot;no-protocol-relative-urls&quot;,
        &quot;scoped-svg-styles&quot;,
        &quot;sri&quot;,
        &quot;typescript-config/consistent-casing&quot;,
        &quot;typescript-config/import-helpers&quot;,
        &quot;typescript-config/is-valid&quot;,
        &quot;typescript-config/no-comments&quot;,
        &quot;typescript-config/strict&quot;,
        &quot;typescript-config/target&quot;
    ],
    &quot;hintsTimeout&quot;: 10000,
    &quot;parsers&quot;: [
        &quot;babel-config&quot;,
        &quot;css&quot;,
        &quot;html&quot;,
        &quot;javascript&quot;,
        &quot;jsx&quot;,
        &quot;less&quot;,
        &quot;sass&quot;,
        &quot;typescript&quot;,
        &quot;typescript-config&quot;,
        &quot;webpack-config&quot;
    ]
}
```  

Wenn Sie mehr Kontrolle über die zu aktivierenden Hinweise und Parser erhalten möchten, erstellen Sie eine lokale `.hintrc` Datei, um webhint zu konfigurieren.  Hilfe zur Ausgabe spezifischer Hinweise finden Sie im [webhint-Nutzerleitfaden][WebhintDocsUserguideConfiguringSummary].  

## Mit dem webhint-Team in Kontakt treten  

Senden Sie Ihr Feedback, indem Sie [ein Problem][GithubWebhintioIssuesNew] in [webhint GitHub Repo][GithubWebhintio]einreichen.  

Wenn Sie zur Erweiterung beitragen möchten, lesen Sie [webhint vs Code Extension Contribution Guide][GithubWebhintioExtensionVscodeContributing].  

## Weitere Informationen  

*   [Bedienungshilfen][AccessibilityIndex]  
*   [Visual Studio Code][VisualstudiocodeIndex]  

<!-- image links -->  

<!--[ImageWebhintExtension]: ./media/webhint-extension.png &quot;Screenshot of webhint VS Code extension&quot;  -->  

<!--links -->  

[AccessibilityIndex]: /microsoft-edge/accessibility &quot;Barrierefreiheit | Microsoft docs&quot;  

[VisualstudiocodeIndex]: /microsoft-edge/visual-studio-code/index &quot;Visual Studio-Code | Microsoft docs&quot;  

[GithubWebhintio]: https://github.com/webhintio/hint &quot;webhint | GitHub&quot;  
[GithubWebhintioExtensionVscodeContributing]: https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md &quot;Beitrag-webhint | GitHub&quot;  
[GithubWebhintioIndexjson]: https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json &quot;index.json-webhintio/Hint | GitHub&quot;
[GithubWebhintioIssuesNew]: https://github.com/webhintio/hint/issues/new &quot;Neue Probleme-webhintio/Hint | GitHub"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

[WebhintDocsUserguideConfiguringSummary]: https://webhint.io/docs/user-guide/configuring-webhint/summary "Konfigurieren von webhint | webhint-Dokumentation"  
[WebhintMain]:  https://webhint.io "webhint"  
