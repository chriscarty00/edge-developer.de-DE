---
title: Verwenden des Web App-Manifests, um Ihre Progressive Web-App in das Betriebs System zu integrieren
description: Erfahren Sie, wie Sie das Web App-Manifest verwenden, um Ihre Progressive Web-App in Ihr Betriebs System zu integrieren.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: Progressive Web-Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: f493ae0c3cef3a1950b2207d66fef65055b2d959
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659293"
---
# Verwenden des Web App-Manifests, um Ihre Progressive Web-App in das Betriebs System zu integrieren

Ein Web-App-Manifest einer Website steuert, wie Ihre Progressive Web-App \ (PWA \) aussieht und sich verhält, wenn Sie auf einem Gerät installiert ist.  Auf der grundlegendsten Ebene enthält das Manifest Details zum Namen Ihrer APP, zu Symbolen für die Darstellung Ihrer APP in Systemmenüs sowie zu den Designfarben, die das Betriebssystem \ (OS \) in der Titelleiste verwendet.  Darüber hinaus können Sie mit dem Manifest leistungsstarke Features entsperren, mit denen sich Ihre APP wie andere systemeigene apps Verhalten kann.  

## Verwenden von Tastenkombinationen, um schnellen Zugriff auf Funktionen zu ermöglichen  

Die meisten Betriebssysteme bieten schnellen Zugriff auf wichtige App-Features mithilfe von Tastenkombinationen im Kontextmenü, das mit dem Symbol der App verbunden ist.  Wenn Sie Tastenkombinationen in PWA verwenden möchten, schließen `shortcuts` Sie die Eigenschaft in das Web App-Manifest ein.  Der folgende Codeausschnitt zeigt, wie Sie eine Verknüpfung in Ihrem Web App-Manifest definieren.  

```json
"shortcuts": [
    {
        "name": "Play Later",
        "description": "View the list of podcasts you saved for later",
        "url": "/play-later",
        "icons": [
            {
                "src": "/icons/play-later.svg",
                "type": "image/svg+xml",
                "purpose": "any"
            }
        ]
    },
    {
        "name": "Subscriptions",
        "description": "View the list of podcasts available in your subscription",
        "url": "/subscriptions?sort=desc"
    }
]
```  

Wenn Sie ein vollständiges Web App-Manifest hinzugefügt haben, werden im Kontextmenü auf dem Symbol der APP zwei Tastenkombinationen für das Hinzufügen des vorherigen Codeausschnitts aktiviert.  Der erste Name ist `Play Later` ein benutzerdefiniertes Symbol.  Die zweite ist benannt `Subscriptions` und weist kein Symbol auf, da die `icons` Eigenschaft optional ist.  Die `description` Eigenschaft ist ebenfalls optional und kann zum Bereitstellen zusätzlicher Informationen für Barrierefreiheits Zwecke verwendet werden.  

## Identifizieren ihrer App als freigabeziel

Viele Betriebssysteme ermöglichen es Benutzern, schnell Links und Dateien mit systemeigenen Anwendungen zu teilen. Progressive Web-Apps können auch über das `share_target` Mitglied des Web App-Manifests an dieser Funktion teilnehmen. Wenn Sie share_target verwenden, definieren Sie die Seite "Aktion" (ähnlich wie in einem Formular) und die Parameter, die Sie erwarten, an Sie weitergegeben zu werden. Der folgende Codeausschnitt zeigt ein Beispiel für die Verwendung von `share_target` .

```json
"share_target": {
    "action": "/share.html",
    "params": {
        "title": "name",
        "text": "description",
        "url": "link"
    }
}
```

Wenn Sie dem Web App-Manifest hinzugefügt wird, wird "/Share.html" als Aktionsseite für eine Freigabe festgelegt. Darüber hinaus werden drei Parameter definiert, die an die Aktionsseite übergeben werden: "Title", "Text" und "URL". Diese Parameter werden in den Eigenschaften "Name", "Description" und "Link" des [ShareData](https://wicg.github.io/web-share#dom-sharedata) -Objekts gespeichert. Standardmäßig empfängt die Aktionsseite diese Parameter als Teil einer GET-Anforderung, doch Sie können die Anforderung `method` und Codierung \ (as `enctype` \) wie in einem Webformular angeben.

## Weitere Informationen  

Weitere Informationen zu Web App-Manifesten finden Sie in der folgenden Liste verwandter Themen.  

* [Web App-Manifeste][MDNWebAppManifests]  
* [Webfreigabe Ziel][WICGShareTarget]
* [Webfreigabe][WICGShare]

<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Web App-Manifeste | MDN"  
[WICGShareTarget]: https://wicg.github.io/web-share-target/ "Ziel-API für Webfreigaben | WICG"
[WICGShare]: https://w3c.github.io/web-share/ "Webfreigabe-API | WICG"
