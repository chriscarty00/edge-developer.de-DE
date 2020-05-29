---
description: Unternehmensrichtlinien Dokumentation für Edge (Chrom)-Erweiterungen.
title: Übereinstimmungsmuster
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/05/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 16f54fcdc127822e89e050c367a681d886b0c8d0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567512"
---
# Übereinstimmungsmuster

Die Host Berechtigungen und die Inhalts Skript Übereinstimmung basieren auf einer Gruppe von URLs, die durch Übereinstimmungsmuster definiert werden.  Ein Übereinstimmungsmuster ist im Grunde eine URL, die mit einem zulässigen Schema beginnt (,,, `http` `https` oder, `file` `ftp` und das "Zeichen enthalten kann `*` .  Das besondere Muster `<all_urls>` entspricht einer beliebigen URL, die mit einem zulässigen Schema beginnt.  Jedes Übereinstimmungsmuster besteht aus drei Teilen:  

*   _Schema_ – beispielsweise `http` oder `file` oder `*`  

> [!NOTE]
> Der Zugriff auf `file` URLs erfolgt nicht automatisch.  Der Benutzer muss die Seite "erweiterungenverwaltung" besuchen und sich `file` für jede Erweiterung, die ihn anfordert, für den Zugriff entscheiden.  

*   `_host_` – beispielsweise `www.google.com` oder `*.google.com` oder `*` ; Wenn es sich bei dem Schema um eine Datei handelt, gibt es kein Host-Part.  
*   `_path_` – beispielsweise, `/*` , `/foo*` oder `/foo/bar` .  Der Pfad muss in einer Host Berechtigung vorhanden sein, wird aber immer als behandelt `/*` .  

Die grundlegende Syntax:  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

Die Bedeutung von `*` hängt davon ab, ob Sie im Schema-, Host-oder Path-Webpart enthalten ist.  Wenn es sich um ein Schema handelt `*` , entspricht es entweder `http` oder `https` , und nicht `file` , oder `ftp` .  Wenn der Host gerade ist `*` , ist er mit jedem Host identisch. Wenn es sich um einen Host handelt `*.hostname` , entspricht er dem angegebenen Host oder einer der Unterdomänen.  Im Abschnitt Path werden jeweils `*` 0 oder mehr Zeichen abgleichen.  In der folgenden Tabelle sind einige gültige Muster dargestellt.  

| Muster | Funktionsweise | Beispiele für übereinstimmende URLs |  
|:--- |:--- |:--- |  
| `http://*/*` | Entspricht einer URL, die das http-Schema verwendet | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | Entspricht einer URL, die das http-Schema verwendet, auf einem beliebigen Host, solange der Pfad beginnt mit `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | Entspricht einer beliebigen URL, die das HTTPS-Schema verwendet, befindet sich auf einem `google.com` Host \ (wie `www.google.com` , `docs.google.com` oder `google.com` \), solange der Pfad mit beginnt `/foo` und endet mit `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | Entspricht der angegebenen URL | `http://example.org/foo/bar.html` |  
|`file:///foo*` | Entspricht einer beliebigen lokalen Datei, deren Pfad mit beginnt `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | Entspricht einer URL, die das `http` Schema verwendet und sich auf dem Host befindet `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | Entspricht einer URL, die mit "oder" beginnt `http://mail.google.com` `https://mail.google.com` . | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | Entspricht einer URL, die ein zulässiges Schema verwendet. \ (Die Liste der zulässigen Schemas finden Sie am Anfang dieses Abschnitts. \) | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

Nachfolgend finden Sie einige Beispiele für `_invalid_` Musterübereinstimmungen:

| Fehlerhaftes Muster | Warum es schlecht ist |  
|:--- |:--- |  
| `http://www.foo.com` | Nein `_path_` |  
| `http://*foo/bar` | ' ' `*` im Host kann nur mit einem ' `.` ' oder ' ' verfolgt werden `/` . |  
| `http://foo.*.bar/baz` | Wenn " `*` " in der ist `_host_` , muss es das erste Zeichen sein. |  
| `http:/bar` | Fehlendes `_scheme_` Trennzeichen \ (' `/` ' sollte "sein" `//` \) |  
| `foo://*` | Ungültig `_scheme_` |  

Einige Schemas werden in allen Kontexten nicht unterstützt.

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/match_patterns/).  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
