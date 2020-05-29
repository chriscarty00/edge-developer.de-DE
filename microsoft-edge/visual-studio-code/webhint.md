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
# webhint vs-Code Erweiterung

Verwenden Sie [webhint](https://webhint.io), ein anpassbares linting-Tool, um die Barrierefreiheit, die Leistung, die browserübergreifende Kompatibilität, die PWA-Kompatibilität und die Sicherheit Ihrer Website zu verbessern. Sie überprüft Ihren Code auf bewährte Methoden und häufige Fehler. Dieses Open-Source-Projekt, das ursprünglich vom Microsoft Edge-Team entwickelt wurde, ist jetzt Teil der [OpenJS-Foundation](https://openjsf.org/). Das Microsoft Edge-Team trägt weiterhin zu webhint neben Webentwicklern in der Community bei.

![Screenshot der webhint vs-Code Erweiterung](./media/webhint-extension.png)

Identifizieren und beheben Sie Probleme in HTML, CSS, JavaScript, Manuskript und mehr, indem Sie die [webhint-Erweiterung für vs-Code](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint)hinzufügen. Hinweise werden als Inline Unterstriche angezeigt und im Problembereich zusammengefasst.

## Konfiguration

Bei dieser Erweiterung wird eine JSON- [Standard](https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json) Datei verwendet, die Hinweise und Parser für HTML, CSS, Vorlagen Systeme (jsx/TSX, eckig usw.), JavaScript/schreibscript und vieles mehr aktiviert.

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

Wenn Sie mehr Kontrolle über die zu aktivierenden Hinweise und Parser erhalten möchten, erstellen Sie eine lokale `.hintrc` Datei, um webhint zu konfigurieren. Hilfe zur Ausgabe spezifischer Hinweise finden Sie im [webhint-Nutzerleitfaden](https://webhint.io/docs/user-guide/configuring-webhint/summary/).

## Feedback senden

Senden Sie uns Ihr Feedback, indem Sie [ein Problem](https://github.com/webhintio/hint/issues/new) im [webhint GitHub Repo](https://github.com/webhintio/hint)einreichen. 

Wenn Sie zur Erweiterung beitragen möchten, lesen Sie den [Leitfaden zur Beitrags-und Code Erweiterung webhint vs](https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md).

## Weitere Informationen
  - [Bedienungshilfen](/microsoft-edge/accessibility)
  - [Visual Studio Code](/microsoft-edge/visual-studio-code/)
