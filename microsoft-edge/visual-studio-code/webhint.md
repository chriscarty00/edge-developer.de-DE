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
# <span data-ttu-id="680b6-104">Webhint vs-Code Erweiterung</span><span class="sxs-lookup"><span data-stu-id="680b6-104">Webhint Vs Code Extension</span></span>  

<span data-ttu-id="680b6-105">Verwenden Sie [webhint][WebhintMain], ein anpassbares linting-Tool, um die Barrierefreiheit, die Leistung, die browserübergreifende Kompatibilität, die PWA-Kompatibilität und die Sicherheit Ihrer Website zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="680b6-105">Use [webhint][WebhintMain], a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span>  <span data-ttu-id="680b6-106">Sie überprüft Ihren Code auf bewährte Methoden und häufige Fehler.</span><span class="sxs-lookup"><span data-stu-id="680b6-106">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="680b6-107">Dieses Open-Source-Projekt, das ursprünglich vom Microsoft Edge-Team entwickelt wurde, ist jetzt Teil der [OpenJS-Foundation][OpenjsFoundation].</span><span class="sxs-lookup"><span data-stu-id="680b6-107">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="680b6-108">Das Microsoft Edge-Team trägt weiterhin zu webhint neben Webentwicklern in der Community bei.</span><span class="sxs-lookup"><span data-stu-id="680b6-108">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Screenshot der webhint vs-Code Erweiterung":::
   <span data-ttu-id="680b6-110">Screenshot der webhint vs-Code Erweiterung</span><span class="sxs-lookup"><span data-stu-id="680b6-110">Screenshot of webhint VS Code extension</span></span>  
:::image-end:::

<!--![Screenshot of webhint VS Code extension][ImageWebhintExtension]  -->  

<span data-ttu-id="680b6-111">Identifizieren und beheben Sie Probleme in HTML, CSS, JavaScript, Manuskript und mehr, indem Sie die [webhint-Erweiterung für vs-Code][VisualstudioMarketplaceWebhint]hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="680b6-111">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for VS Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="680b6-112">Hinweise werden als Inline Unterstriche angezeigt und im **Problem** Bereich zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="680b6-112">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  

## <span data-ttu-id="680b6-113">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="680b6-113">Configuration</span></span>  

<span data-ttu-id="680b6-114">Diese Erweiterung verwendet eine JSON- [Standard][GithubWebhintioIndexjson] Datei, die Hinweise und Parser für HTML, CSS, Vorlagen Systeme \ (jsx/TSX, eckig usw. \), JavaScript/schreibscript und vieles mehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="680b6-114">This extension uses a [default configuration][GithubWebhintioIndexjson] json file that activates hints and parsers for HTML, CSS, templating systems \(JSX/TSX, Angular, and so on\), JavaScript/TypeScript, and more.</span></span>  

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

<span data-ttu-id="680b6-115">Wenn Sie mehr Kontrolle über die zu aktivierenden Hinweise und Parser erhalten möchten, erstellen Sie eine lokale `.hintrc` Datei, um webhint zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="680b6-115">If you want more control over the hints and parsers that get activated, create a local `.hintrc` file to configure webhint.</span></span>  <span data-ttu-id="680b6-116">Hilfe zur Ausgabe spezifischer Hinweise finden Sie im [webhint-Nutzerleitfaden][WebhintDocsUserguideConfiguringSummary].</span><span class="sxs-lookup"><span data-stu-id="680b6-116">For help with output from specific hints, see [webhint user guide][WebhintDocsUserguideConfiguringSummary].</span></span>  

## <span data-ttu-id="680b6-117">Mit dem webhint-Team in Kontakt treten</span><span class="sxs-lookup"><span data-stu-id="680b6-117">Getting in touch with the webhint team</span></span>  

<span data-ttu-id="680b6-118">Senden Sie Ihr Feedback, indem Sie [ein Problem][GithubWebhintioIssuesNew] in [webhint GitHub Repo][GithubWebhintio]einreichen.</span><span class="sxs-lookup"><span data-stu-id="680b6-118">Send your feedback by [filing an issue][GithubWebhintioIssuesNew] in [webhint GitHub repo][GithubWebhintio].</span></span>  

<span data-ttu-id="680b6-119">Wenn Sie zur Erweiterung beitragen möchten, lesen Sie [webhint vs Code Extension Contribution Guide][GithubWebhintioExtensionVscodeContributing].</span><span class="sxs-lookup"><span data-stu-id="680b6-119">To contribute to the extension, see [webhint VS Code extension contribution guide][GithubWebhintioExtensionVscodeContributing].</span></span>  

## <span data-ttu-id="680b6-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="680b6-120">See also</span></span>  

*   [<span data-ttu-id="680b6-121">Bedienungshilfen</span><span class="sxs-lookup"><span data-stu-id="680b6-121">Accessibility</span></span>][AccessibilityIndex]  
*   [<span data-ttu-id="680b6-122">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="680b6-122">Visual Studio Code</span></span>][VisualstudiocodeIndex]  

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
