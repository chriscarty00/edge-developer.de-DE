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

:::image type="complex" source="./media/webhint-extension.png" alt-text="Screenshot der webhint vs-Code Erweiterung":::
   Screenshot der webhint vs-Code Erweiterung  
:::image-end:::

<!--![Screenshot of webhint VS Code extension][ImageWebhintExtension]  -->  

Identifizieren und beheben Sie Probleme in HTML, CSS, JavaScript, Manuskript und mehr, indem Sie die [webhint-Erweiterung für vs-Code][VisualstudioMarketplaceWebhint]hinzufügen.  Hinweise werden als Inline Unterstriche angezeigt und im **Problem** Bereich zusammengefasst.  

## Konfiguration  

Diese Erweiterung verwendet eine JSON- [Standard][GithubWebhintioIndexjson] Datei, die Hinweise und Parser für HTML, CSS, Vorlagen Systeme \ (jsx/TSX, eckig usw. \), JavaScript/schreibscript und vieles mehr aktiviert.  

```json
{
    "connector": "local",
    "extends": [
        "accessibility",
        "progressive-web-apps"
    ],
    "formatters": [
        "html",
        "summary"
    ],
    "hints": [
        "apple-touch-icons",
        "button-type",
        "compat-api/css",
        "compat-api/html",
        "create-element-svg",
        "css-prefix-order",
        "disown-opener",
        "highest-available-document-mode",
        "manifest-exists",
        "meta-charset-utf-8",
        "meta-viewport",
        "no-bom",
        "no-protocol-relative-urls",
        "scoped-svg-styles",
        "sri",
        "typescript-config/consistent-casing",
        "typescript-config/import-helpers",
        "typescript-config/is-valid",
        "typescript-config/no-comments",
        "typescript-config/strict",
        "typescript-config/target"
    ],
    "hintsTimeout": 10000,
    "parsers": [
        "babel-config",
        "css",
        "html",
        "javascript",
        "jsx",
        "less",
        "sass",
        "typescript",
        "typescript-config",
        "webpack-config"
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

<!--[ImageWebhintExtension]: ./media/webhint-extension.png "Screenshot of webhint VS Code extension"  -->  

<!--links -->  

[AccessibilityIndex]: /microsoft-edge/accessibility "Barrierefreiheit | Microsoft docs"  

[VisualstudiocodeIndex]: /microsoft-edge/visual-studio-code/index "Visual Studio-Code | Microsoft docs"  

[GithubWebhintio]: https://github.com/webhintio/hint "webhint | GitHub"  
[GithubWebhintioExtensionVscodeContributing]: https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md "Beitrag-webhint | GitHub"  
[GithubWebhintioIndexjson]: https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json "Index. JSON-webhintio/Hint | GitHub"
[GithubWebhintioIssuesNew]: https://github.com/webhintio/hint/issues/new "Neue Probleme-webhintio/Hint | GitHub"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

[WebhintDocsUserguideConfiguringSummary]: https://webhint.io/docs/user-guide/configuring-webhint/summary "Konfigurieren von webhint | webhint-Dokumentation"  
[WebhintMain]:  https://webhint.io "webhint"  
