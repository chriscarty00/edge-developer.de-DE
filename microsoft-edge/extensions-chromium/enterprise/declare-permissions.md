---
description: Informationen zum Deklarieren von Berechtigungen für APIs in Ihrem Manifest
title: Deklarieren von API-Berechtigungen in Erweiterungsmanifesten
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Add-Ons, Partner Center, Entwickler
ms.openlocfilehash: 987279a8072388d3fd47ee8b7cbf5f9bb3c483e0
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461532"
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
# <a name="declare-api-permissions-in-extension-manifests"></a>Deklarieren von API-Berechtigungen in Erweiterungsmanifesten  

Um die meisten `chrome.*` APIs verwenden zu können, muss ihre Erweiterung die `permissions` im Manifest deklarieren.  Sie können Berechtigungen mithilfe einer Berechtigungszeichenfolge aus der folgenden Tabelle deklarieren oder ein Muster verwenden, um mit ähnlichen Zeichenfolgen zu übereinstimmen.  Berechtigungen helfen Ihnen, Ihre Erweiterung zu beschränken, wenn sie durch Schadsoftware gefährdet wird.  Einige Berechtigungen werden benutzern möglicherweise vor der Installation der Erweiterung mithilfe von Berechtigungswarnungen angezeigt.  

Wenn eine API erfordert, dass Sie Berechtigungen im Manifest deklarieren, lesen Sie die Dokumentation für diese API, um die erforderlichen Berechtigungen zu verstehen.  Auf der Seite Storage-API wird beispielsweise beschrieben, wie die Berechtigung deklariert `storage` wird.  

Im folgenden Codeausschnitt wird das Deklarieren von Berechtigungen in der Manifestdatei erläutert.  

```json
"permissions": [
  "tabs",
  "bookmarks",
  "http://www.blogger.com/",
  "http://*.google.com/",
  "unlimitedStorage"
]
```  

In der folgenden Tabelle sind die derzeit verfügbaren Berechtigungszeichenfolgen aufgeführt, die in Ihrem Manifest verwendet werden können, sowie die Beschreibungen.  

| Berechtigungszeichenfolge | Details |  
|:--- |:--- |  
| `activeTab` | Fordert an, dass der Erweiterung Berechtigungen gemäß der Spezifikation `activeTab` erteilt werden. |  
| `alarms` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.alarms` API. |  
| `background` | Ermöglicht Microsoft Edge, frühzeitig zu starten und zu spät heruntergefahren zu werden, sodass Erweiterungen möglicherweise eine längere Lebensdauer haben.  Wenn eine installierte Erweiterung über Berechtigungen verfügt, wird Microsoft Edge ausgeführt, sobald sich der Benutzer am Computer des Benutzers anmeldet und bevor der Benutzer `background` Microsoft Edge.  Mit der Berechtigung wird Microsoft Edge auch nach dem Schließen des letzten Fensters fortgesetzt, bis der Benutzer die Ausführung `background` Microsoft Edge.  Diese Berechtigung hat keine Auswirkungen auf Erweiterungen, die im Browser deaktiviert sind.  Die `background` Berechtigung wird normalerweise auf einer Hintergrundseite verwendet. |  
| `bookmarks` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.bookmarks` API. |  
| `browsingData` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.browsingData` API. |  
| `certificateProvider` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.certificateProvider` API. |  
| `clipboardRead` | Erforderlich, wenn die Erweiterung `document.execCommand('paste')` verwendet . |  
| `clipboardWrite` | Gibt an, dass die Erweiterung `document.execCommand('copy')` verwendet oder `document.execCommand('cut')` . |  
| `contentSettings` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.contentSettings` API. |  
| `contextMenus` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.contextMenus` API. |  
| `cookies` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.cookies` API. |  
| `debugger` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.debugger` API. |  
| `declarativeContent` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.declarativeContent` API. |  
| `declarativeNetRequest` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.declarativeNetRequest` API. |  
| `declarativeNetRequestFeedback` | Gewährt der Erweiterung Zugriff auf Ereignisse und Methoden innerhalb der API, die Informationen zu `chrome.declarativeNetRequest` übereinstimmenden deklarativen Regeln zurückgibt. |  
| `declarativeWebRequest` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.declarativeWebRequest` API. |  
| `desktopCapture` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.desktopCapture` API. |  
| `documentScan` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.documentScan` API. |  
| `downloads` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.downloads` API. |  
| `enterprise.deviceAttributes` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.enterprise.deviceAttributes` API. |  
| `enterprise.hardwarePlatform` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.enterprise.hardwarePlatform` API. |  
| `enterprise.networkingAttributes` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.enterprise.networkingAttributes` API. |  
| `enterprise.platformKeys` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.enterprise.platformKeys` API. |  
| `experimental` | Erforderlich, wenn die Erweiterung eine API `chrome.experimental.*` verwendet. |  
| `fileBrowserHandler` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.fileBrowserHandler` API. |  
| `fileSystemProvider` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.fileSystemProvider` API. |  
| `fontSettings` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.fontSettings` API. |  
| `geolocation` | Ermöglicht der Erweiterung die Verwendung der Geolocation-API, ohne dass der Benutzer zur Berechtigung aufgefordert wird. |  
| `history` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.history` API. |  
| `identity` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.identity` API. |  
| `idle` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.idle` API. |  
| `loginState` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.loginState` API. |  
| `management` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.management` API. |  
| `nativeMessaging` | Gewährt Ihrer Erweiterung Zugriff auf die systemeigene Messaging-API. |  
| `notifications` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.notifications` API. |  
| `pageCapture` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.pageCapture` API. |  
| `platformKeys` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.platformKeys` API. |  
| `power` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.power` API. |  
| `printerProvider` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.printerProvider` API. |  
| `printing` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.printing` API. |  
| `printingMetrics` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.printingMetrics` API. |  
| `privacy` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.privacy` API. |  
| `processes` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.processes` API. |  
| `proxy` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.proxy` API. |  
| `scripting` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.scripting` API. |  
| `search` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.search` API. |  
| `sessions` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.sessions` API. |  
| `signedInDevices` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.signedInDevices` API. |  
| `storage` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.storage` API. |  
| `system.cpu` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.system.cpu` API. |  
| `system.display` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.system.display` API. |  
| `system.memory` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.system.memory` API. |  
| `system.storage` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.system.storage` API. |  
| `tabCapture` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.tabCapture` API. |  
| `tabGroups` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.tabGroups` API. |  
| `tabs` | Gewährt Ihrer Erweiterung Zugriff auf privilegierte Felder der Objekte, die von mehreren APIs verwendet werden `Tab` können, einschließlich `chrome.tabs` und `chrome.windows` .  In vielen Fällen muss Ihre Erweiterung nicht die Berechtigung zum Verwenden `tabs` dieser APIs deklarieren. |  
| `topSites` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.topSites` API. |  
| `tts` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.tts` API. |  
| `ttsEngine` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.ttsEngine` API. |  
| `unlimitedStorage` | Bietet ein unbegrenztes Kontingent zum Speichern clientseitiger Daten, z. B. Datenbanken und lokale Speicherdateien.  Ohne diese Berechtigung ist die Erweiterung auf 5 MB lokalen Speicher beschränkt. |  
| `vpnProvider` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.vpnProvider` API. |  
| `wallpaper` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.wallpaper` API. |  
| `webNavigation` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.webNavigation` API. |  
| `webRequest` | Gewährt Ihrer Erweiterung Zugriff auf die `chrome.webRequest` API. |  
| `webRequestBlocking` | Erforderlich, wenn die Erweiterung die `chrome.webRequest` API zum Blockieren von Anforderungen verwendet. |  

<!-- links -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/docs/extensions/mv3/declare_permissions/).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
