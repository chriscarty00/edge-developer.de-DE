---
description: Hier finden Sie Informationen zu aktuellen und zukünftigen APIs sowie zu den bekannten Problemen/Chrom-Inkompatibilitäten.
title: Erweiterungen – unterstützte APIs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: fceba67f5fab1a223cfc94abf7f19a0a9d1bcdf0
ms.sourcegitcommit: 0879b205aa88c6b73d84f106b4b435d5a0e8cadc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/18/2020
ms.locfileid: "10937182"
---
# Unterstützte APIs  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Im folgenden finden Sie eine detaillierte Liste der API-Member, die unterstützt werden. Die Entwicklung der Erweiterungs Plattform wird fortgesetzt, daher sollten Sie regelmäßig nach Updates suchen!

> [!NOTE]
>  - Für Microsoft Edge sind alle Erweiterungs-APIs unter dem `browser` Namespace, beispielsweise `browser.browserAction.disable()` .
>  - Microsoft Edge Extension-APIs verwenden Rückrufe, keine Versprechungen.


## Übergreifende Probleme

Die folgenden bekannten Probleme spannen sich über die Erweiterungs Plattform und werden in naher Zukunft behoben:

- Wenn die CSS `url()` -Eigenschaft verwendet wird, funktionieren absolute URLs `ms-browser-extension://` nicht wie in Chrome. Um dieses Problem zu umgehen, verwenden Sie stattdessen relative Pfade zu Ressourcen (beginnend im Root-Erweiterungsverzeichnis).
- `window.open()` funktioniert nicht in Erweiterungs-hintergrundskripts. Verwenden Sie `browser.windows.create()` stattdessen bitte.
- Freigegebene Cookies werden unterstützt, allerdings kann das Erweiterungs-Hintergrundskript keinen Zugriff auf Sitzungscookies haben, die auf der Registerkarte gesetzt sind, bevor die Erweiterung aktiviert ist. Dieses Problem wirkt sich nicht auf persistente Cookies aus.
- Wenn nur nicht unterstützte Berechtigungen für eine Erweiterung angegeben werden, also `activeTab`führt der Versuch, die Erweiterung zu querladen, dazu, dass die Erweiterung deinstalliert wird, wobei die folgende Meldung angezeigt wird: "bei ihren Erweiterungen ist etwas schief gelaufen, daher mussten wir Sie neu installieren. Sie müssen Sie wieder aktivieren. "
- Das Auslösen eines Downloads über ein verborgenes Anchor-Tag schlägt in hintergrundskripts fehl. Dies sollte stattdessen über eine Erweiterungsseite erfolgen.


## Lesezeichen

Die folgenden `bookmarks` APIs werden unterstützt:

| API                                   | Bekannte Probleme                                             | Chrom-Inkompatibilitäten
|---------------------------------------|----------------------------------------------------------|--------------------------|
| [Lesezeichen](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks) | | |
| [Bookmarks. Create](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/create) | | |
| [Bookmarks. Remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/remove) | | |
| [Bookmarks. gettree](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/getTree) |  | |
| [Bookmarks. Move](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/move) | | |
| [Bookmarks. removeTree](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/removeTree) | | |
| [Bookmarks. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/update)            | | |


## BrowserAction

Die folgenden `browserAction` APIs werden unterstützt:

| API                                   | Bekannte Probleme                                             | Chrom-Inkompatibilitäten
|---------------------------------------|----------------------------------------------------------|--------------------------|
| [BrowserAction](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction) | | |
| [Browser-Funktion. Disable](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/disable) | | |
| [Browser-Funktion. enable](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/enable) | | |
| [Browser-getBadgeBackgroundColor](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getBadgeBackgroundColor) |  | |
| [Browser-setBadgeBackgroundColor](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setBadgeBackgroundColor) | | |
| [Browser-Click](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/onClicked) | | |
| [Browser-setBadgeText](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setBadgeText)            | | |
| [Browser-Menü. setpopup](https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setPopup)  | | |
| [Browser-getBadgeText](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getBadgeText)   | | |
| [Browser-"setsymbol"](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setIcon) | `browserAction.setIcon` wird nicht beibehalten. <br/><br/> Der `imageData` Parameter wird nicht unterstützt. <br/><br/> `path` ist ein erforderlicher Parameter.| |
| [Browser-Feld. getTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getTitle) | | |
| [Browser-"SetTitle"](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setTitle) | | |

## contextMenus

Die folgenden `contextMenus` APIs werden unterstützt:

| API                    | Bekannte Probleme | Chrom-Inkompatibilitäten
|------------------------|--------------|----------------------|
| [contextMenus](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus)  |  | |
| [ContextMenus. ContextType](https://developer.mozilla.org/Add-ons/WebExtensions/API/contextMenus/ContextType) | `"page_action"` `ContextType` wird im Kontextmenü "Seiten Aktion" nicht angezeigt.| Microsoft Edge unterstützt nicht die `"launcher"` `ContextType` .|
| [ContextMenus. Create](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/create)    | Wenn Erweiterungen keine angeben `contextmenuid` , `id` ist der generierte nicht eindeutig. | |
| [ContextMenus. onclicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/onClicked) | | |
| [ContextMenus. Remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/remove) | | |
| [ContextMenus. entfernenalles](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/removeAll) | | |
| [ContextMenus. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/update) | | |

## Cookies

Die folgenden `cookies` APIs werden unterstützt:

| API                    | Bekannte Probleme | Chrom-Inkompatibilitäten
|------------------------|--------------|----------------------|
| [Cookies](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/cookies)  |  | |
| [Cookies. Abrufen](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/get)    |  | |
| [Cookies. getAll](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/getAll) |   | Wenn keine URL bereitgestellt wird, werden Cookies nur für URLs in aktuell geöffneten Registerkarten abgerufen. In Chrome werden alle Cookies auf dem Computer eines Benutzers abgerufen. |
| [Cookies. getAllCookieStores](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/getAllCookieStores)  | | Gibt immer denselben standardmäßigen Cookiespeicher mit der ID "0" zurück. Alle Cookies gehören diesem Store. |
| [Cookies. ongeändert](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/onChanged)    | | Nicht unterstützt |
| [Cookies. Remove](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/remove) |  | |
| [Cookies. Satz](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/set)    |  | |



## Erweiterung

Die folgenden `extension` APIs werden unterstützt:

| API                                   | Bekannte Probleme | Chrom-Inkompatibilitäten
|---------------------------------------|----------------------------------------------------------|-------------|
[Erweiterung](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension) | | |
[Extension. getBackgroundPage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension/getBackgroundPage) | | |
[Extension. getURL](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension/getURL) | | |
[Erweiterung. GetViews](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/getViews) | | |
[Extension. isAllowedIncognitoAccess](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/isAllowedIncognitoAccess) | | | 
[extension.inIncognitoContext](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/inIncognitoContext) | | | 



## i18n

Die folgenden `i18n` APIs werden unterstützt:

API | Bekannte Probleme | Chrom-Inkompatibilitäten
:------| :-------- | :---------------------
[i18n](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n) | | |
[i18n. getAcceptLanguages](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n/getAcceptLanguages) | | |
[i18n. GetMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/i18n/getMessage) | `i18n.getMessage` mit ungültiger Taste wird eine Ausnahme ausgelöst, anstatt dass Sie ordnungsgemäß fehlschlägt. <br/><br/> `i18n.getMessage` Das Argument erwartet Zeichenfolgen, sollte aber auch eine Ganzzahl zulassen oder eine Ausnahme auslösen. | |
[i18n. getUILanguage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n/getUILanguage) | | |

## im Leerlauf

Die folgenden `idle` APIs werden unterstützt:

API | Bekannte Probleme | Chrom-Inkompatibilitäten
:------| :-------- | :---------------------
[im Leerlauf](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle) | | |
[Idle. setDetectionInterval](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle/setDetectionInterval) | | |
[Idle. queryState](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle/queryState) | | |

## Benachrichtigungen

Die folgenden `notifications` APIs werden unterstützt:

API | Bekannte Probleme | Chrom-Inkompatibilitäten
:------| :-------- | :---------------------
[Benachrichtigungen](https://developer.mozilla.org/Add-ons/WebExtensions/API/notifications) | | |
[Benachrichtigungen. Notificationoptions](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/NotificationOptions) | | |
[Benachrichtigungen. TemplateType](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/TemplateType) | | |
[Benachrichtigungen. löschen](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/clear) | | |
[Benachrichtigungen. Erstellen](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/create) | | |
[Notifications. getAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/getAll) | | |
[Benachrichtigungen. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/update) | | |
[Notifications. onButtonClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onButtonClicked) | | |
[Benachrichtigungen. onclicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onClicked) | | |
[Benachrichtigungen. OnClosed](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onClosed) | | |
Notifications. onPermissionLevelChanged | | |
Notifications. getPermissionLevel | | |

## PageAction

Die folgenden `pageAction` APIs werden unterstützt:

API | Bekannte Probleme | Chrom-Inkompatibilitäten
:------------ | :------------- | :--------------------
[PageAction](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction) | | |
[pagestyle. getpopup](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/getPopup) | | |
[pagestyle. getTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/getTitle) | | |
[Pagen. Hide](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/hide) | | |
[Pagen. onclicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/onClicked) | | |
[pagestyle. setsymbol](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setIcon) | | Der `imageData` Parameter wird nicht unterstützt. <br/><br/> `path` ist ein erforderlicher Parameter. |
[pagestyle. setpopup](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setPopup) | | |
[Pagen. SetTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setTitle) | | |
[pagestyle. Show](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/show) | | |



## Runtime

Die folgenden `runtime` APIs werden unterstützt:

API | Bekannte Probleme | Chrom-Inkompatibilitäten
:------------ | :------------- | :-------------------
[Runtime](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime) | | |
[Runtime. Port. Disconnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[Runtime. Port. Disconnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[Runtime. Port. PostMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[Runtime. Connect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connect) | | |
[Runtime. connectNative](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) | | |
[runtime.id](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/id) | | |
[Runtime. getBackgroundPage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/getBackgroundPage) | | |
[Runtime. getmanifest](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/getManifest) | | |
[Runtime. getURL](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/getURL) | | |
[Runtime. LastError](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/lastError) | | |
[Runtime. Reload](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/reload) | | |
[Runtime. SendMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage) | Microsoft Edge-Erweiterungsseiten können `runtime.sendMessage` / `onMessage` zum Senden von Nachrichten an sich selbst verwendet werden. <br/><br/> `runtime.sendmessage` wird von Website Seiten nicht unterstützt. | Microsoft Edge unterstützt den `options` Parameter nicht.|
[Runtime. sendNativeMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) | | |
[Runtime. setUninstallUrl](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/setUninstallUrl) | | |
[Runtime. OnConnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onConnect) | | |
[Runtime. oninstalliert](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/onInstalled) | | |
[Runtime. onMessage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/onMessage) | `tab` das Objekt in `runtime.onMessage` Event ist nicht vollständig implementiert. | `MessageSender.tlsChannelId` wird in Microsoft Edge nicht unterstützt.|

## Speicher

Die folgenden `storage` APIs werden unterstützt:

API | Bekannte Probleme | Chrom-Inkompatibilitäten
:------------ | :------------- | :------------------------
[Speicher](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage) |  | |
[Speicher. local. Get](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/get)  | | |
[Speicher. local. Remove](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/remove)  | | |
[Speicher. local. Satz](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/set)  | | |
[Speicher. local. Clear](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/clear) | | |
[Speicher. local. getBytesInUse](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/getBytesInUse) | | `storage.local` Daten werden in einem anderen Format als Chrome beibehalten, wodurch beim Aufrufen ein anderer Wert zurückgegeben wird `storage.local.getBytesInUse` .  <br/><br/>Ex: `storage.local.set({ "k": { "s": "âas" } }` gibt 13 in Chrome und 50 in Microsoft Edge zurück.|
[Speicher. Sync. Get](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/get) | Wenn die kombinierte Anzahl von Zeichen in den `name` `author` Feldern und Manifesten mehr als 31 Zeichen enthält, `storage.sync` funktioniert der Namespace möglicherweise nicht. | |
[Speicher. Sync. Remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/remove) | | |
[Storage. Sync. Satz](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/set) | | |
[Speicher. ongeändert](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/onChanged) | | |

## Registerkarten

Die folgenden `tabs` APIs werden unterstützt:

API | Bekannte Probleme | Chrom-Inkompatibilitäten
:------------ | :------------- | :----------------
[Registerkarten](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs) | | |
[Tabs. captureVisibleTab](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/captureVisibleTab) | | |
[Tabs. Create](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/create) | | `selected`, `pinned` und `openerTabId` werden nicht unterstützt. |
[Tabs. detectLanguage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/detectLanguage) | | |
[tabs.executeScript](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/executeScript) | `runAt` wird ignoriert, allerdings aktiviert. Das Ausführen eines Skripts in einem bestimmten Frame wird noch nicht unterstützt. | |
[Tabs. Abrufen](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/get) | Optionen Seiten, bei Fragen zu einer Registerkarte, die sich nicht in Ihrem Fenster befindet, führen diesen Anruf nicht aus. | |
[Tabs. GetCurrent](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/getCurrent) | | |
[Tabs. insertCSS](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/insertCSS) | `runAt` wird ignoriert, allerdings aktiviert. | `cssOrigin` wird nicht unterstützt. |
[Tabs. OnDeactivated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onActivated) | | |
[Tabs. onattached](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onAttached) | | |
[Tabs. OnCreated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onCreated) | | |
[Tabs. onlosgelöst](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs) | | |
[Tabs. OnRemoved](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onRemoved) | | |
[Tabs. onreplaced](https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/onReplaced) | | |
[Tabs. OnUpdated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onUpdated) | Nach der Deinstallation/erneuten Installation wird die URL erst empfangen, nachdem Microsoft Edge neu gestartet wurde. | |
[Tabs. Query](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/query) | `pinned`, `audible` und `muted` werden noch nicht unterstützt. <br/><br/> `"popup"` `windowType` wird noch nicht unterstützt. | `highlighted` wird nicht unterstützt. <br/><br/> `"panel"`, `"app"` und `"devtools"` `windowType` werden nicht unterstützt. |
[Tabs. Reload](https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/reload) | | Microsoft Edge unterstützt keine Zusagen. |
[Tabs. Remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/remove) | | |
[Tabs. SendMessage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/sendMessage) | Messaging ein bestimmter Frame wird noch nicht unterstützt. `tabs.sendMessage` sendet nie eine Antwort nach einer Registerkarten Aktualisierung `runtime.onMessage` , wenn auf der Registerkarte "empfangen" keine Listener vorhanden sind. | |
[Tabs. Registerkarte](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/Tab) | `audible`, `mutedInfo` , `inPrivate` , `width` und `height` Eigenschaften werden noch nicht unterstützt. | `openerTabId`, `selected` und `highlighted` Eigenschaften werden nicht unterstützt. |
[Tabs. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/update) | `pinned` und `muted` werden noch nicht unterstützt. | `highlighted` und `selected` werden nicht unterstützt. |


## Webnavigation

Die folgenden `webNavigation` APIs werden unterstützt:


| API                                                                                                                                                           | Bekannte Probleme                                | Chrom-Inkompatibilitäten                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [Webnavigation](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation)                                                     | Die Registerkarten-IDs sind falsch.                      | Filter, TransitionTypes und TransitionQualifiers werden nicht unterstützt. <br/><br/> Bei einer Registerkarte `processIds` werden alle identisch sein. |
| [Webnavigation. getAllFrames](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/getAllFrames)                           | Enthält keine Objekt-als-IFRAME-Elemente. |                                                                                                                             |
| [Webnavigation. GetFrame](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/getFrame)                                   |                                             |                                                                                                                             |
| [Webnavigation. onBeforeNavigate](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onBeforeNavigate)                   |                                             |                                                                                                                             |
| [Webnavigation. OnCommitted](https://developer.mozilla.org/Add-ons/WebExtensions/API/webNavigation/onCommitted)                                           |                                             |                                                                                                                             |
| [Webnavigation. OnCompleted](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onCompleted)                             |                                             |                                                                                                                             |
| [Webnavigation. onCreatedNavigationTarget](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onCreatedNavigationTarget) |                                             |                                                                                                                             |
| [Webnavigation. onDOMContentLoaded](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onDOMContentLoaded)               |                                             |                                                                                                                             |
| [Webnavigation. onErrorOccurred](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onErrorOccurred)                     |                                             |                                                                                                                             |
| [Webnavigation. onHistoryStateUpdated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onHistoryStateUpdated)         |                                             |                                                                                                                             |
| [Webnavigation. onReferenceFragmentUpdated](https://developer.mozilla.org/Add-ons/WebExtensions/API/webNavigation/onReferenceFragmentUpdated)            |                                             |                                                                                                                             |
| [Webnavigation. onTabReplaced](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onTabReplaced)                         |                                             | Nicht unterstützt                                                                                                              |
| [Webnavigation. transitiontype](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/TransitionType)                       |                                             |                                                                                                                             |
| [Webnavigation. TransitionQualifier](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/TransitionQualifier)             |                                             |                                                                                                                             |

## WebRequest

Die folgenden `webRequest` APIs werden unterstützt:

API | Bekannte Probleme | Chrom-Inkompatibilitäten
:------ | :----- | :-------
[WebRequest](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest) | `webRequest` für synchrone nicht unterstützt `XmlHttpRequests` . | Netzwerkanforderungen aus Erweiterungen, wie Optionen, Hintergrund oder Popup Seiten, werden nicht unterstützt.<br/><br/> Netzwerkanforderungen von `<object>` und- `<embed>` Elementen werden nicht unterstützt.<br/><br/> Header können für zwischengespeicherte Anforderungen nicht geändert werden.  |
[handlerBehaviorChanged](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/handlerBehaviorChanged) | | Handler-Änderungen werden in Microsoft Edge automatisch gehandhabt.<br/><br/>Das Aufrufen dieser Funktion hat keine Auswirkungen.  |
[onAuthRequired](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onAuthRequired) | | |
[onBeforeRedirect](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeRedirect) | | |
[onBeforeRequest](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeRequest) | | `requestBody` wird nicht unterstützt. |
[onBeforeSendHeaders](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeSendHeaders) | | |
[onCompleted](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onCompleted) | | |
[onErrorOccurred](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onErrorOccurred) | | |
[onHeadersReceived](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onHeadersReceived) | |  |
[onResponseStarted](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onResponseStarted) | |  |
[onSendHeaders](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onSendHeaders) | | |

## windows

Die folgenden `windows` APIs werden unterstützt:


| API                                                                                                                               | Bekannte Probleme                                                   | Chrom-Inkompatibilitäten                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [windows](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows)                                     |                                                                | `Window` Objekte unterstützen keine `alwaysOnTop` Eigenschaft in Microsoft Edge. <br/><br/>InPrivate wird nicht unterstützt. |
| [Windows. CreateType](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/CreateType)                            |                                                                | `"panel"` und `"detached_panel"` werden in Microsoft Edge nicht unterstützt.                                           |
| [Windows. Create](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/create)                                    |                                                                | `tabId` der Parameter für das abreißen einer Registerkarte wird nicht unterstützt.                                                       |
| [Windows. Get](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/get)                             |                                                                |                                                                                                                 |
| [Windows. getAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getAll)                       | `windows.getAll({populate: true})` Eigenschaft fehlt `tabs` . |                                                                                                                 |
| [Windows. GetCurrent](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getCurrent)               |                                                                |                                                                                                                 |
| [Windows. getLastFocused](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getLastFocused)       |                                                                |                                                                                                                 |
| [Windows. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/update)                       | Die Angabe der Position wird nicht unterstützt.                          | `"minimized"`/`"maximized"`/`"fullscreen"` und `drawAttention` werden in Microsoft Edge nicht unterstützt.             |
| [Windows. OnCreated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/onCreated)                 |                                                                | `WindowType` Filter wird nicht unterstützt.                                                                           |
| [Windows. onfocusd](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/onFocusChanged)                    |                                                                | `WindowType` Filter wird nicht unterstützt.                                                                           |
| [Windows. WindowState](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/WindowState)                          | `"minimized"`, `"maximized"` `"fullscreen"` werden nicht unterstützt. | `"docked"` wird in Microsoft Edge nicht unterstützt.                                                                  |
| [Windows. WindowType](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/WindowType)                            |                                                                | `"panel"`, `"app"` und `"devtools"` werden in Microsoft Edge nicht unterstützt.                                       |
| [Windows. WINDOW_ID_CURRENT](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/WINDOW_ID_CURRENT) |                                                                |                                                                                                                 |
| [Windows. WINDOW_ID_NONE](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/WINDOW_ID_NONE)       |                                                                |                                                                                                                 |
