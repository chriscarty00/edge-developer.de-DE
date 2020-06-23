---
description: Informationen zum Verwalten von benutzerdatenordnern in WebView2-Anwendungen
title: Verwalten von benutzerdatenordnern in WebView2-Anwendungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/02/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML, benutzerdatenordner
ms.openlocfilehash: a7a6fd620cfb417e349a03159204ceb68998745e
ms.sourcegitcommit: e49b86082da884299fdd485d3311d63a7688c0d0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2020
ms.locfileid: "10755397"
---
# Verwalten des Benutzerdatenordners

WebView2-Anwendungen interagieren mit benutzerdatenordnern, um Browserdaten wie Cookies, Berechtigungen und zwischengespeicherte Ressourcen zu speichern. Jede Instanz eines WebView2-Steuerelements ist mit einem benutzerdatenordner verknüpft. Jeder benutzerdatenordner ist für einen Benutzer eindeutig.

## Bewährte Methoden

Benutzerdatenordner werden automatisch von WebView2 erstellt. WebView2-Entwickler steuern die Lebensdauer des Benutzerdatenordners. Wenn Ihre Anwendung Benutzerdaten aus Anwendungssitzungen erneut verwendet, sollten Sie die benutzerdatenordner speichern, andernfalls können Sie Sie löschen. Berücksichtigen Sie bei der Entscheidung, wie Ihre benutzerdatenordner verwaltet werden sollen, die folgenden Szenarien:

*   Wenn derselbe Benutzer Ihre Anwendung wiederholt verwendet und der Webinhalt der Anwendung auf den Daten des Benutzers basiert, speichern Sie den Ordner Benutzerdaten. Wenn mehrere Benutzer Ihre Anwendung wiederholt verwenden, erstellen Sie einen neuen benutzerdatenordner für jeden neuen Benutzer, und speichern Sie den benutzerdatenordner der einzelnen Benutzer.
*   Wenn Ihre Anwendung keine Wiederholungs Benutzer enthält, erstellen Sie einen neuen benutzerdatenordner für jeden Benutzer, und löschen Sie den vorherigen benutzerdatenordner.

## Erstellen von benutzerdatenordnern

Wenn Sie den Speicherort des Benutzerdatenordners angeben möchten, schließen Sie den Parameter ein, `userDataFolder` Wenn Sie [ICoreWebView2Environment](../reference/win32/0-9-538/icorewebview2environment) (Win32) oder [CoreWebView2Environment](../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment) (.net) aufrufen. Nach der Erstellung werden Browserdaten aus Ihrem WebView2-Steuerelement in einem Unterordner von gespeichert `userDataFolder` . Wenn `userDataFolder` nicht angegeben, erstellt WebView2 benutzerdatenordner an Standardspeicherorten wie folgt:

* Für verpackte Windows Store-Apps ist der Standardbenutzerordner der Unterordner `ApplicationData\LocalFolder` im Paketordner.
* Bei vorhandenen Desktop-Apps ist der standardmäßige benutzerdatenordner der exe-Pfad Ihrer Anwendung + `.WebView2` . Anstatt die Standardeinstellung zu verwenden, empfiehlt es sich, einen benutzerdatenordner anzugeben und ihn im gleichen Ordner zu erstellen, in dem alle anderen APP-Daten gespeichert sind.

## Löschen von benutzerdatenordnern

Ihre Anwendung muss möglicherweise benutzerdatenordner löschen:

* Wenn Sie Ihre APP deinstallieren. Wenn Sie verpackte Windows Store-apps deinstallieren, löscht Windows benutzerdatenordner automatisch. 
* So bereinigen Sie den gesamten Browser-Datenverlauf
* So stellen Sie die Datenbeschädigung wieder her
* Zum Entfernen von vorherigen Sitzungsdaten. 


> [!NOTE]
> Dateien in benutzerdatenordnern können nach dem Schließen der WebView2-Anwendung weiterhin verwendet werden. In diesem Fall warten Sie, bis der Browserprozess und alle untergeordneten Prozesse beendet sind, bevor Sie den Ordner löschen. Sie können die Prozess-ID des Browser Prozesses mithilfe der `BrowserProcessId` Eigenschaft des WebView2 abrufen.

## Freigeben von benutzerdatenordnern

WebView2-Steuerelemente können dieselben benutzerdatenordner für folgende Personen freigeben:

* [Optimieren Sie die Systemressourcen](https://docs.microsoft.com/en-us/microsoft-edge/webview2/reference/win32/0-9-538/icorewebview2#process-model) , indem Sie in einem Browserprozess ausgeführt werden.
* Freigeben des Browserverlaufs und der zwischengespeicherten Ressourcen 

Beim Freigeben von benutzerdatenordnern sollten Sie Folgendes bedenken: 

1. Stellen Sie beim erneuten Erstellen von WebView2-Steuerelementen zum Aktualisieren von Browserversionen mithilfe von [add_NewBrowserVersionAvailable](../reference/win32/0-9-538/icorewebview2environment#add_newbrowserversionavailable) (Win32)-oder [NewBrowserVersionAvailable](../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment#newbrowserversionavailable) (.net)-Ereignissen sicher, dass Browserprozesse Exit und WebView2-Steuerelemente schließen, die denselben benutzerdatenordner verwenden. Um die Prozess-ID des Browser Prozesses abzurufen, verwenden Sie die `BrowserProcessId` -Eigenschaft des WebView2-Steuerelements.

2. WebView2-Steuerelemente, für die derselbe benutzerdatenordner freigegeben ist, müssen die gleichen Optionen für [ICoreWebView2Environment](../reference/win32/0-9-538/icorewebview2environment) (Win32) oder [CoreWebView2Environment](../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment) (.net) verwenden. Wenn dies nicht der Fall ist, schlägt die WebView2-Erstellung fehl `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)` . 

Wenn Sie verschiedene Teile der Anwendung isolieren oder Daten zwischen WebView2-Steuerelementen freigeben möchten, ist es möglich, dass Sie unterschiedliche benutzerdatenordner verwenden. Eine Anwendung kann beispielsweise aus zwei WebView2-Steuerelementen bestehen, einer für die Anzeige einer Werbung und der anderen zum Anzeigen von Anwendungsinhalten. In diesem Szenario können Entwickler entscheiden, für jedes WebView2-Steuerelement unterschiedliche benutzerdatenordner zu verwenden. 

> [!NOTE]
> Jeder WebView2-Browserprozess beansprucht zusätzlichen Arbeitsspeicher und Speicherplatz. Daher empfiehlt es sich, WebView2s nicht mit zu vielen unterschiedlichen benutzerdatenordnern zur gleichen Zeit zu verwenden. 
