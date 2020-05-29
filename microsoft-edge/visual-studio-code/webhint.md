---
description: Verwenden von webhint in Visual Studio-Code
title: webhint vs-Code Erweiterung
author: hxlnt
ms.author: raweil
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, vs-Code, Visual Studio-Code, webhint
ms.openlocfilehash: d3102bf4d8d4a8bba9225d8d3f68432197f775ac
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568656"
---
# <span data-ttu-id="86787-104">webhint vs-Code Erweiterung</span><span class="sxs-lookup"><span data-stu-id="86787-104">webhint VS Code extension</span></span>

<span data-ttu-id="86787-105">Verwenden Sie [webhint](https://webhint.io), ein anpassbares linting-Tool, um die Barrierefreiheit, die Leistung, die browserübergreifende Kompatibilität, die PWA-Kompatibilität und die Sicherheit Ihrer Website zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="86787-105">Use [webhint](https://webhint.io), a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span> <span data-ttu-id="86787-106">Sie überprüft Ihren Code auf bewährte Methoden und häufige Fehler.</span><span class="sxs-lookup"><span data-stu-id="86787-106">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="86787-107">Dieses Open-Source-Projekt, das ursprünglich vom Microsoft Edge-Team entwickelt wurde, ist jetzt Teil der [OpenJS-Foundation](https://openjsf.org/).</span><span class="sxs-lookup"><span data-stu-id="86787-107">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation](https://openjsf.org/).</span></span> <span data-ttu-id="86787-108">Das Microsoft Edge-Team trägt weiterhin zu webhint neben Webentwicklern in der Community bei.</span><span class="sxs-lookup"><span data-stu-id="86787-108">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>

![Screenshot der webhint vs-Code Erweiterung](./media/webhint-extension.png)

<span data-ttu-id="86787-110">Identifizieren und beheben Sie Probleme in HTML, CSS, JavaScript, Manuskript und mehr, indem Sie die [webhint-Erweiterung für vs-Code](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint)hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="86787-110">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for VS Code](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint).</span></span> <span data-ttu-id="86787-111">Hinweise werden als Inline Unterstriche angezeigt und im Problembereich zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="86787-111">Hints appear as inline underlines and are summarized in the Problems pane.</span></span>

## <span data-ttu-id="86787-112">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="86787-112">Configuration</span></span>

<span data-ttu-id="86787-113">Bei dieser Erweiterung wird eine JSON- [Standard](https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json) Datei verwendet, die Hinweise und Parser für HTML, CSS, Vorlagen Systeme (jsx/TSX, eckig usw.), JavaScript/schreibscript und vieles mehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="86787-113">This extension uses a [default configuration](https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json) json file that activates hints and parsers for HTML, CSS, templating systems (JSX/TSX, Angular, and so on), JavaScript/TypeScript, and more.</span></span>

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

<span data-ttu-id="86787-114">Wenn Sie mehr Kontrolle über die zu aktivierenden Hinweise und Parser erhalten möchten, erstellen Sie eine lokale `.hintrc` Datei, um webhint zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="86787-114">If you want more control over the hints and parsers that get activated, create a local `.hintrc` file to configure webhint.</span></span> <span data-ttu-id="86787-115">Hilfe zur Ausgabe spezifischer Hinweise finden Sie im [webhint-Nutzerleitfaden](https://webhint.io/docs/user-guide/configuring-webhint/summary/).</span><span class="sxs-lookup"><span data-stu-id="86787-115">For help with output from specific hints, see the [webhint user guide](https://webhint.io/docs/user-guide/configuring-webhint/summary/).</span></span>

## <span data-ttu-id="86787-116">Feedback senden</span><span class="sxs-lookup"><span data-stu-id="86787-116">Feedback</span></span>

<span data-ttu-id="86787-117">Senden Sie uns Ihr Feedback, indem Sie [ein Problem](https://github.com/webhintio/hint/issues/new) im [webhint GitHub Repo](https://github.com/webhintio/hint)einreichen.</span><span class="sxs-lookup"><span data-stu-id="86787-117">Send us your feedback by [filing an issue](https://github.com/webhintio/hint/issues/new) on the [webhint GitHub repo](https://github.com/webhintio/hint).</span></span> 

<span data-ttu-id="86787-118">Wenn Sie zur Erweiterung beitragen möchten, lesen Sie den [Leitfaden zur Beitrags-und Code Erweiterung webhint vs](https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md).</span><span class="sxs-lookup"><span data-stu-id="86787-118">To contribute to the extension, please read the [webhint VS Code extension contribution guide](https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md).</span></span>

## <span data-ttu-id="86787-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="86787-119">See also</span></span>
  - [<span data-ttu-id="86787-120">Bedienungshilfen</span><span class="sxs-lookup"><span data-stu-id="86787-120">Accessibility</span></span>](/microsoft-edge/accessibility)
  - [<span data-ttu-id="86787-121">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="86787-121">Visual Studio Code</span></span>](/microsoft-edge/visual-studio-code/)
