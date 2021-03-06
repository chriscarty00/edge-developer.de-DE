---
title: Verwenden des Web-App-Manifests zum Integrieren Ihrer Progressive Web App in das Betriebssystem
description: Erfahren Sie, wie Sie das Web App-Manifest verwenden, um Ihre Progressive Web App in Ihr Betriebssystem zu integrieren.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: progressive Web-Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 0063323b1fde94d84e70df51170726325dd0f2a9
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399099"
---
# <a name="use-the-web-app-manifest-to-integrate-your-progressive-web-app-into-the-operating-system"></a>Verwenden des Web-App-Manifests zum Integrieren Ihrer Progressive Web App in das Betriebssystem

Ein Web-App-Manifest einer Website bestimmt, wie Ihre Progressive Web App \(PWA\) aussieht und sich verhält, wenn sie auf einem Gerät installiert wird.  Auf der grundlegendsten Ebene enthält das Manifest Details zum Namen Ihrer App, Symbole zur Darstellung Ihrer App in Systemmenüs und die Designfarben, die das Betriebssystem \(OS\) in der Titelleiste verwendet.  Mit dem Manifest können Sie außerdem leistungsstarke Features entsperren, mit denen sich Ihre App wie andere systemeigene Apps auf dem System verhalten kann.  

## <a name="use-shortcuts-to-provide-quick-access-to-features"></a>Verwenden von Verknüpfungen zum schnellen Zugriff auf Features  

Die meisten Betriebssysteme bieten schnellen Zugriff auf wichtige App-Features mithilfe von Verknüpfungen im Kontextmenü, das mit dem Symbol der App verbunden ist.  Um Verknüpfungen in Ihrem PWA zu verwenden, schließen Sie die `shortcuts` Eigenschaft in Ihr Web App-Manifest ein.  Der folgende Codeausschnitt zeigt, wie Sie eine Verknüpfung in Ihrem Web-App-Manifest definieren.  

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

Wenn das Hinzufügen des vorherigen Codeausschnitts zu einem vollständigen Web-App-Manifest hinzugefügt wird, werden zwei Verknüpfungen im Kontextmenü auf dem Symbol der App aktiviert.  Die erste ist benannt `Play Later` und hat ein benutzerdefiniertes Symbol.  Die zweite ist benannt `Subscriptions` und hat kein Symbol, da die Eigenschaft `icons` optional ist.  Die Eigenschaft ist auch optional und kann verwendet werden, um `description` zusätzliche Informationen für Barrierefreiheitszwecke zur Verfügung zu stellen.  

## <a name="identify-your-app-as-a-share-target"></a>Identifizieren Ihrer App als Freigabeziel

Viele Betriebssysteme ermöglichen Benutzern die schnelle Freigabe von Links und Dateien für systemeigene Anwendungen. Progressive Web Apps können auch mit dem Mitglied des Web App-Manifests an `share_target` diesem Feature teilnehmen.  Mit `share_target` definieren Sie die Seite \(ähnlich einem Formular\) und die Parameter, die Sie davon erwarten, `"action"` dass sie übergeben werden.  Im folgenden Codeausschnitt wird ein Beispiel für die Verwendung von `share_target` angezeigt.

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

Beim Hinzufügen zum Web-App-Manifest wird dies `"/share.html"` als Aktionsseite für eine Freigabe etabliert. Darüber hinaus werden drei Parameter definiert, die an diese Aktionsseite übergeben würden: `"title"` `"text"` , und `"url"` .  Diese Parameter werden in den `"name"` Eigenschaften , und des `"description"` `"link"` [ShareData-Objekts][GitHubWicgWebShareDomSharedata] gespeichert.  Standardmäßig empfängt die Aktionsseite die Parameter als Teil einer GET-Anforderung, Aber Sie können die Anforderung und Codierung \(als \) angeben, genau wie in einem `method` `enctype` Webformular.

## <a name="see-also"></a>Weitere Informationen  

Weitere Informationen zu Web-App-Manifesten finden Sie in der folgenden Liste verwandter Themen.  

*   [Web App-Manifeste][MDNWebAppManifests]  
*   [Web Share Target][GitHubWicgWebShareTarget]
*   [Web Share][GithubW3cWebShare]
    
<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Web-App-Manifeste | MDN"  

[GitHubWicgWebShareTarget]: https://wicg.github.io/web-share-target "Web Share Target API | WICG"
[GitHubWicgWebShareDomSharedata]: https://wicg.github.io/web-share#dom-sharedata "ShareData-Wörterbuch – Web Share-API-| WICG"  

[GithubW3cWebShare]: https://w3c.github.io/web-share/ "Web Share-API-| WICG"
