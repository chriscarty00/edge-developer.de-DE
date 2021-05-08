---
description: Enterprise Richtliniendokumentation für Edgeerweiterungen (Chromium).
title: Übereinstimmungsmuster
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: fcb87b62cac063c7663f575fa3d992b187408c28
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461248"
---
<!-- Copyright A. W. Fuchs

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="match-patterns"></a>Übereinstimmungsmuster

Hostberechtigungen und Inhaltsskriptabgleich basieren auf einer Reihe von URLs, die durch Übereinstimmungsmuster definiert sind.  Ein Übereinstimmungsmuster ist im Wesentlichen eine URL, die mit einem zulässigen Schema beginnt ( , , , oder , und die `http` ' ' Zeichen enthalten `https` `file` `ftp` `*` kann.  Das spezielle Muster `<all_urls>` entspricht jeder URL, die mit einem zulässigen Schema beginnt.  Jedes Übereinstimmungsmuster hat 3 Teile:  

*   _schema_ – z. `http` B. `file` oder oder `*`  

> [!NOTE]
> Der Zugriff `file` auf URLs erfolgt nicht automatisch.  Der Benutzer muss die Verwaltungsseite Erweiterungen besuchen und sich für jede Erweiterung, die sie anfordert, `file` für den Zugriff entscheiden.  

*   `_host_` – z. `www.google.com` B. `*.google.com` oder ; wenn das Schema `*` datei ist, gibt es keinen Hostteil.  
*   `_path_` – z. B. `/*` , `/foo*` oder `/foo/bar` .  Der Pfad muss in einer Hostberechtigung vorhanden sein, wird jedoch immer als `/*` behandelt.  

Die grundlegende Syntax:  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

Die Bedeutung von `*` hängt davon ab, ob sie sich im Schema-, Host- oder Pfadteil befindet.  Wenn das Schema `*` ist , entspricht es entweder oder , und nicht , oder `http` `https` `file` `ftp` .  Wenn der Host nur `*` ist, entspricht er einem beliebigen Host. Wenn der Host ist, entspricht er dem angegebenen Host oder einer `*.hostname` der Unterdomänen.  Im Abschnitt Pfad entspricht jede `*` 0 oder mehr Zeichen.  In der folgenden Tabelle sind einige gültige Muster aufgeführt.  

| Muster | Was dies bedeutet | Beispiele für übereinstimmende URLs |  
|:--- |:--- |:--- |  
| `http://*/*` | Entspricht einer beliebigen URL, die das http-Schema verwendet | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | Entspricht jeder URL, die das http-Schema auf einem beliebigen Host verwendet, solange der Pfad mit beginnt `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | Entspricht jeder URL, die das https-Schema verwendet, befindet sich auf einem Host \(z. B. `google.com` `www.google.com` , oder `docs.google.com` `google.com` \), solange der Pfad mit beginnt und `/foo` mit endet `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | Entspricht der angegebenen URL | `http://example.org/foo/bar.html` |  
|`file:///foo*` | Entspricht einer lokalen Datei, deren Pfad mit beginnt `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | Entspricht jeder URL, die das `http` Schema verwendet und sich auf dem Host befindet `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | Entspricht jeder URL, die mit oder `http://mail.google.com` `https://mail.google.com` beginnt. | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | Entspricht jeder URL, die ein zulässiges Schema verwendet. \(Am Anfang dieses Abschnitts finden Sie eine Liste der zulässigen Schemas.\) | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

Im Folgenden finden Sie einige Beispiele für `_invalid_` Muster übereinstimmungen:

| Ungültiges Muster | Warum es schlecht ist |  
|:--- |:--- |  
| `http://www.foo.com` | Nein `_path_` |  
| `http://*foo/bar` | ' ' im Host kann nur von einem `*` ' ' oder ' ' gefolgt `.` `/` werden |  
| `http://foo.*.bar/baz` | Wenn ' `*` ' in `_host_` ist, muss es das erste Zeichen sein. |  
| `http:/bar` | Fehlendes `_scheme_` Trennzeichen \(' `/` ' sollte " `//` "\) sein. |  
| `foo://*` | Ungültig `_scheme_` |  

Einige Schemas werden nicht in allen Kontexten unterstützt.

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/match_patterns).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
