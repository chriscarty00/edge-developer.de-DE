---
description: Verwenden von Webhint in Visual Studio Code
title: webhint Visual Studio Codeerweiterung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, vs code, visual studio code, webhint
ms.openlocfilehash: 3dfd900bf818d02dbc8123c00e7928e56d9b6ade
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399274"
---
# <a name="webhint-vs-code-extension"></a>Webhint Vs Code Extension  

Verwenden [Sie Webhint][WebhintMain], ein anpassbares Lintingtool, um die Barrierefreiheit, Leistung, browserübergreifende Kompatibilität, PWA-Kompatibilität und Sicherheit Ihrer Website zu verbessern.  Der Code wird auf bewährte Methoden und häufige Fehler überprüft. Dieses Open -Source-Projekt, das ursprünglich vom Microsoft Edge-Team entwickelt wurde, ist jetzt Teil der [OpenJS Foundation][OpenjsFoundation].  Das Microsoft Edge-Team trägt weiterhin zusammen mit Webentwicklern in der Community zum Webhint bei.  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Screenshot von webhint Visual Studio Codeerweiterung":::
   Screenshot von webhint Visual Studio Codeerweiterung  
:::image-end:::

<!--![Screenshot of webhint Visual Studio Code extension][ImageWebhintExtension]  -->  

Identifizieren und beheben Sie Probleme in HTML, CSS, JavaScript, TypeScript und mehr, indem Sie die [Webhint-Erweiterung][VisualstudioMarketplaceWebhint]für Visual Studio Code hinzufügen.  Hinweise werden als Inline unterstreicht angezeigt und im Bereich **Probleme zusammengefasst.**  

## <a name="configuration"></a>Konfiguration  

Diese Erweiterung [][GithubWebhintioIndexjson] verwendet eine standardmäßige Konfigurations-Json-Datei, die Hinweise und Parser für HTML, CSS, Templating-Systeme \(JSX/TSX, Angular und so weiter\), JavaScript/TypeScript und vieles mehr aktiviert.  

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

Wenn Sie mehr Kontrolle über die Hinweise und Parser haben möchten, die aktiviert werden, erstellen Sie eine lokale Datei zum Konfigurieren `.hintrc` von Webhint.  Hilfe bei der Ausgabe von bestimmten Hinweisen finden Sie unter [Webhint-Benutzerhandbuch][WebhintDocsUserguideConfiguringSummary].  

## <a name="getting-in-touch-with-the-webhint-team"></a>Kontakt mit dem Webhint-Team  

Senden Sie Ihr Feedback, [indem Sie ein Problem][GithubWebhintioIssuesNew] im [webhint GitHub-Repository einreichen.][GithubWebhintio]  

Um zur Erweiterung beizutragen, navigieren Sie zu [webhint Visual Studio Codeerweiterungsbeitragshandbuch][GithubWebhintioExtensionVscodeContributing].  

## <a name="see-also"></a>Weitere Informationen  

*   [Barrierefreiheit][AccessibilityIndex]  
*   [Visual Studio Code][VisualstudiocodeIndex]  

<!-- image links -->  

<!--[ImageWebhintExtension]: ./media/webhint-extension.png "Screenshot of webhint Visual Studio Code extension"  -->  

<!--links -->  

[AccessibilityIndex]: /microsoft-edge/accessibility "Barrierefreiheit | Microsoft Docs"  

[VisualstudiocodeIndex]: /microsoft-edge/visual-studio-code/index "Visual Studio Code | Microsoft Docs"  

[GithubWebhintio]: https://github.com/webhintio/hint "webhint | GitHub"  
[GithubWebhintioExtensionVscodeContributing]: https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md "Mitwirken – webhint | GitHub"  
[GithubWebhintioIndexjson]: https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json "index.js- webhintio/hint | GitHub"
[GithubWebhintioIssuesNew]: https://github.com/webhintio/hint/issues/new "Neue Probleme – webhintio/hint | GitHub"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

[WebhintDocsUserguideConfiguringSummary]: https://webhint.io/docs/user-guide/configuring-webhint/summary "Konfigurieren von Webhint-| webhint-Dokumentation"  
[WebhintMain]:  https://webhint.io "webhint"  
