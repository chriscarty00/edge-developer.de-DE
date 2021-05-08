---
description: Diese Seite enthält Eine Dokumentation zur Microsoft Edge Benutzer-Agent-Zeichenfolge
title: Microsoft Edge Zeichenfolge "User Agent"
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibility, web platform, user agent string, ua string, ua overrides
ms.openlocfilehash: 73401219b7708a739292a46b6131fe40765e9c8c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568733"
---
# Microsoft Edge User Agent String (Desktop)  

Eine Zeichenfolge des Benutzer-Agents \(UA\) kann verwendet werden, um zu ermitteln, welche Version eines bestimmten Browsers unter einem bestimmten Betriebssystem verwendet wird.  Wie andere Browser enthält Microsoft Edge diese Informationen immer dann in den `User-Agent` HTTP-Header, wenn eine Anforderung an eine Website gesendet wird.  Auf sie kann auch über JavaScript zugegriffen werden, indem der Wert von abgefragt `navigator.userAgent` wird.  

Microsoft empfiehlt Webentwicklern, [](https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection) die Featureerkennung nach Möglichkeit zu nutzen, um die Codeverfügbarkeit zu verbessern, die Anfälligkeit von Code zu verringern und das Risiko von Codebrüchen bei zukünftigen UA-Zeichenfolgenupdates zu vermeiden.  

In Fällen, in denen die Featureerkennung nicht anwendbar ist und die UA-Erkennung verwendet werden muss, lautet das Format der Microsoft Edge UA auf dem Desktop wie folgt:

Der `User-Agent` Anforderungsheader hat das folgende Format:

```http
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.74 Safari/537.36 Edg/79.0.309.43
``` 

Der Rückgabewert `navigator.userAgent` von hat das folgende Format:

```javascript
"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.74 Safari/537.36 Edg/79.0.309.43"
```  

Plattformbezeichner ändern sich basierend auf dem verwendeten Betriebssystem, und die Versionsnummern werden ebenfalls im Zeitschritt erhöht.  Dieses Format ist identisch mit dem Chromium UA mit dem Zusatz eines neuen `Edg` Tokens am Ende.  Microsoft hat das Token ausgewählt, um Kompatibilitätsprobleme zu vermeiden, die durch die Zeichenfolge verursacht werden können, die von der Version von Microsoft Edge EdgeHTML verwendet `Edg` `Edge` wird.  Das `Edg` Token entspricht auch vorhandenen [Token,](https://blogs.windows.com/msedgedev/2017/10/05/microsoft-edge-ios-android-developer/) die unter iOS und Android verwendet werden.

## Zuordnen von UA-Zeichenfolge zu Browsername
Das Zuordnen von UA-Zeichenfolgentoken zu einem besser lesbaren Browsernamen für die Verwendung im Code ist heute ein gängiges Muster im Web. Beim Zuordnen des neuen Tokens zu einem Browsernamen empfiehlt Microsoft, einen anderen Namen als den für die Ältere Version von Microsoft Edge verwendeten Namen zu verwenden, um zu vermeiden, dass versehentlich Legacyumgehungen angewendet werden, die nicht für `Edg` Chromium-basierte Browser gelten.

## Außerkraftsetzungen des Benutzer-Agents  

Manchmal erkennt eine Website die aktualisierte Version des Microsoft Edge UA.  Daher funktioniert eine Reihe von Features dieser Website möglicherweise nicht ordnungsgemäß.  Wenn Microsoft über diese Art von Problemen benachrichtigt wird, werden Websitebesitzer kontaktiert und über die aktualisierten UA informiert.  

Die Websites benötigen häufig etwas Zeit, um die Erkennungslogik der UA zu aktualisieren und zu testen, um die Probleme zu beheben, die Microsoft den Websitebesitzern meldet.  In diesen Fällen verwendet Microsoft eine Liste der UA-Überschreibungen in unseren Beta- und Stable-Kanälen, um die Kompatibilität für Benutzer zu maximieren, die auf diese Websites zugreifen.  Die Außerkraftsetzungen geben neue UA-Werte an, Microsoft Edge anstatt der Standard-UA für bestimmte Websites gesendet werden sollen.  Sie können die Liste der ua-Überschreibungen anzeigen, die derzeit angewendet werden, indem Sie in den Beta- und Stable-Kanälen von `edge://compat/useragent` Microsoft Edge. 

Unsere Canary- und Dev-Kanäle erhalten derzeit keine UA-Überschreibungen, sodass Webentwickler über eine Umgebung verfügen, in der sie problemlos Probleme auf ihren Websites reproduzieren können, die durch die Standard-UA Microsoft Edge werden.  Wenn Sie aus einem bestimmten Grund die Möglichkeit zum Deaktivieren von UA-Überschreibungen in den Beta- oder Stable-Kanälen von Microsoft Edge benötigen, können Sie die ausführbare Datei Microsoft Edge mit dem folgenden Befehlszeilenargument ausführen:  

```shell
--disable-domain-action-user-agent-override
```  
