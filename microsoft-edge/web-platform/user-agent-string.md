---
description: Diese Seite enthält die Dokumentation zur Microsoft Edge-Benutzer-Agent-Zeichenfolge.
title: Microsoft Edge-Benutzer-Agent-Zeichenfolge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Compatibility, Web Platform, Benutzer-Agent-Zeichenfolge, UA-Zeichenfolge, UA-Überschreibungen
ms.openlocfilehash: 73401219b7708a739292a46b6131fe40765e9c8c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568733"
---
# Microsoft Edge-Benutzer-Agent-Zeichenfolge (Desktop)  

Eine Benutzer-Agent-Zeichenfolge kann verwendet werden, um zu ermitteln, welche Version eines bestimmten Browsers für ein bestimmtes Betriebssystem verwendet wird.  Wie andere Browser enthält Microsoft Edge diese Informationen `User-Agent` immer dann im HTTP-Header, wenn eine Anforderung an eine Website gestellt wird.  Sie können auch über JavaScript aufgerufen werden, indem Sie den Wert von Abfragen `navigator.userAgent` .  

Microsoft empfiehlt Webentwicklern, nach Möglichkeit die [Funktionserkennung](https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection) zu verwenden, um die Verwaltbarkeit von Code zu verbessern, die Anfälligkeit von Code zu verringern und das Risiko von Code Bruch bei zukünftigen UA-Zeichenfolgen Updates zu vermeiden.  

In Fällen, in denen die Funktionserkennung nicht anwendbar ist und die UA-Erkennung verwendet werden muss, sieht das Format von Microsoft Edge UA auf dem Desktop wie folgt aus:

Der `User-Agent` Anforderungsheader weist das folgende Format auf:

```http
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.74 Safari/537.36 Edg/79.0.309.43
``` 

Der Rückgabewert von `navigator.userAgent` ist im folgenden Format:

```javascript
"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.74 Safari/537.36 Edg/79.0.309.43"
```  

Plattformbezeichner werden basierend auf dem verwendeten Betriebssystem geändert, und Versionsnummern werden im Laufe der Zeit ebenfalls inkrementiert.  Dieses Format entspricht dem Chrom ua mit dem Hinzufügen eines neuen `Edg` Tokens am Ende.  Microsoft hat das `Edg` Token ausgewählt, um Kompatibilitätsprobleme zu vermeiden, die möglicherweise durch die Verwendung der Zeichenfolge verursacht werden `Edge` , die von der Version von Microsoft Edge auf Grundlage von EdgeHTML verwendet wird.  Das `Edg` Token ist auch mit [vorhandenen Tokens](https://blogs.windows.com/msedgedev/2017/10/05/microsoft-edge-ios-android-developer/) konsistent, die in IOS und Android verwendet werden.

## Zuordnung der UA-Zeichenfolge zu Browser Name
Das Zuordnen von UA-Zeichenfolgentoken zu einem besser lesbaren Browsernamen für die Verwendung in Code ist heute ein allgemeines Muster im Web. Bei der Zuordnung des neuen `Edg` Tokens zu einem Browsernamen empfiehlt Microsoft, einen anderen Namen als die Entwickler zu verwenden, die für die Legacy Version von Microsoft Edge verwendet werden, um versehentlich vorhandene Problemumgehungen zu vermeiden, die nicht auf Chrom basierte Browser zutreffen.

## Benutzer-Agent-Überschreibungen  

Manchmal erkennt eine Website die aktualisierte Version von Microsoft Edge UA nicht.  Daher funktioniert eine Reihe der Features dieser Website möglicherweise nicht ordnungsgemäß.  Wenn Microsoft über diese Art von Problemen benachrichtigt wird, werden Websitebesitzer kontaktiert und über das aktualisierte UA informiert.  

Die Websites benötigen häufig einige Zeit, um die UA-Erkennungslogik zu aktualisieren und zu testen, um die Probleme zu beheben, die Microsoft an Websitebesitzer meldet.  In diesen Fällen verwendet Microsoft eine Liste der UA-Außerkraftsetzungen in unseren Beta-und stable-Kanälen, um die Kompatibilität für Benutzer zu maximieren, die auf diese Websites zugreifen.  Die Außerkraftsetzungen geben neue UA-Werte an, die von Microsoft Edge anstelle des standardmäßigen ua für bestimmte Websites gesendet werden sollen.  Sie können die Liste der UA-Außerkraftsetzungen anzeigen, die derzeit angewendet werden, indem Sie `edge://compat/useragent` in den Beta-und stable-Kanälen von Microsoft Edge navigieren. 

Unsere Kanaren-und dev-Kanäle erhalten derzeit keine UA-Überschreibungen, damit Webentwickler eine Umgebung haben, in der Sie auf einfache Weise Probleme auf ihren Websites reproduzieren können, die durch den standardmäßigen Microsoft Edge UA verursacht werden.  Wenn Sie aus irgendeinem Grund die Möglichkeit benötigen, UA-Außerkraftsetzungen in den Beta-oder stable-Kanälen von Microsoft Edge zu deaktivieren, können Sie die ausführbare Microsoft Edge-Datei mit dem folgenden Befehlszeilenargument ausführen:  

```shell
--disable-domain-action-user-agent-override
```  
