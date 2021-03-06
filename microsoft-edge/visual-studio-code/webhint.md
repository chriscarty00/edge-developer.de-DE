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
# <a name="webhint-vs-code-extension"></a><span data-ttu-id="85163-104">Webhint Vs Code Extension</span><span class="sxs-lookup"><span data-stu-id="85163-104">Webhint Vs Code Extension</span></span>  

<span data-ttu-id="85163-105">Verwenden [Sie Webhint][WebhintMain], ein anpassbares Lintingtool, um die Barrierefreiheit, Leistung, browserübergreifende Kompatibilität, PWA-Kompatibilität und Sicherheit Ihrer Website zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="85163-105">Use [webhint][WebhintMain], a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span>  <span data-ttu-id="85163-106">Der Code wird auf bewährte Methoden und häufige Fehler überprüft.</span><span class="sxs-lookup"><span data-stu-id="85163-106">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="85163-107">Dieses Open -Source-Projekt, das ursprünglich vom Microsoft Edge-Team entwickelt wurde, ist jetzt Teil der [OpenJS Foundation][OpenjsFoundation].</span><span class="sxs-lookup"><span data-stu-id="85163-107">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="85163-108">Das Microsoft Edge-Team trägt weiterhin zusammen mit Webentwicklern in der Community zum Webhint bei.</span><span class="sxs-lookup"><span data-stu-id="85163-108">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Screenshot von webhint Visual Studio Codeerweiterung":::
   <span data-ttu-id="85163-110">Screenshot von webhint Visual Studio Codeerweiterung</span><span class="sxs-lookup"><span data-stu-id="85163-110">Screenshot of webhint Visual Studio Code extension</span></span>  
:::image-end:::

<!--![Screenshot of webhint Visual Studio Code extension][ImageWebhintExtension]  -->  

<span data-ttu-id="85163-111">Identifizieren und beheben Sie Probleme in HTML, CSS, JavaScript, TypeScript und mehr, indem Sie die [Webhint-Erweiterung][VisualstudioMarketplaceWebhint]für Visual Studio Code hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="85163-111">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for Visual Studio Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="85163-112">Hinweise werden als Inline unterstreicht angezeigt und im Bereich **Probleme zusammengefasst.**</span><span class="sxs-lookup"><span data-stu-id="85163-112">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  

## <a name="configuration"></a><span data-ttu-id="85163-113">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="85163-113">Configuration</span></span>  

<span data-ttu-id="85163-114">Diese Erweiterung [][GithubWebhintioIndexjson] verwendet eine standardmäßige Konfigurations-Json-Datei, die Hinweise und Parser für HTML, CSS, Templating-Systeme \(JSX/TSX, Angular und so weiter\), JavaScript/TypeScript und vieles mehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="85163-114">This extension uses a [default configuration][GithubWebhintioIndexjson] json file that activates hints and parsers for HTML, CSS, templating systems \(JSX/TSX, Angular, and so on\), JavaScript/TypeScript, and more.</span></span>  

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

<span data-ttu-id="85163-115">Wenn Sie mehr Kontrolle über die Hinweise und Parser haben möchten, die aktiviert werden, erstellen Sie eine lokale Datei zum Konfigurieren `.hintrc` von Webhint.</span><span class="sxs-lookup"><span data-stu-id="85163-115">If you want more control over the hints and parsers that get activated, create a local `.hintrc` file to configure webhint.</span></span>  <span data-ttu-id="85163-116">Hilfe bei der Ausgabe von bestimmten Hinweisen finden Sie unter [Webhint-Benutzerhandbuch][WebhintDocsUserguideConfiguringSummary].</span><span class="sxs-lookup"><span data-stu-id="85163-116">For help with output from specific hints, navigate to [webhint user guide][WebhintDocsUserguideConfiguringSummary].</span></span>  

## <a name="getting-in-touch-with-the-webhint-team"></a><span data-ttu-id="85163-117">Kontakt mit dem Webhint-Team</span><span class="sxs-lookup"><span data-stu-id="85163-117">Getting in touch with the webhint team</span></span>  

<span data-ttu-id="85163-118">Senden Sie Ihr Feedback, [indem Sie ein Problem][GithubWebhintioIssuesNew] im [webhint GitHub-Repository einreichen.][GithubWebhintio]</span><span class="sxs-lookup"><span data-stu-id="85163-118">Send your feedback by [filing an issue][GithubWebhintioIssuesNew] in [webhint GitHub repo][GithubWebhintio].</span></span>  

<span data-ttu-id="85163-119">Um zur Erweiterung beizutragen, navigieren Sie zu [webhint Visual Studio Codeerweiterungsbeitragshandbuch][GithubWebhintioExtensionVscodeContributing].</span><span class="sxs-lookup"><span data-stu-id="85163-119">To contribute to the extension, navigate to [webhint Visual Studio Code extension contribution guide][GithubWebhintioExtensionVscodeContributing].</span></span>  

## <a name="see-also"></a><span data-ttu-id="85163-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="85163-120">See also</span></span>  

*   [<span data-ttu-id="85163-121">Barrierefreiheit</span><span class="sxs-lookup"><span data-stu-id="85163-121">Accessibility</span></span>][AccessibilityIndex]  
*   [<span data-ttu-id="85163-122">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="85163-122">Visual Studio Code</span></span>][VisualstudiocodeIndex]  

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
