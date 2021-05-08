---
description: Informationen zum Verwalten von Benutzerdatenordnern in WebView2-Anwendungen
title: Verwalten des Benutzerdatenordners in WebView2-Anwendungen.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html, user data folder
ms.openlocfilehash: a6399e59f153d4446946937461e61667f325f4ae
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535961"
---
# <a name="manage-the-user-data-folder"></a>Verwalten des Benutzerdatenordners  

WebView2-Anwendungen interagieren mit Benutzerdatenordnern, um Browserdaten wie Cookies, Berechtigungen und zwischengespeicherte Ressourcen zu speichern.  Jede Instanz eines WebView2-Steuerelements ist einem Benutzerdatenordner zugeordnet.  Jeder Benutzerdatenordner ist für einen Benutzer eindeutig.  

## <a name="best-practices"></a>Bewährte Methoden  

Benutzerdatenordner werden automatisch von WebView2 erstellt.  WebView2-Entwickler steuern die Lebensdauer des Benutzerdatenordners.  Wenn Ihre Anwendung Benutzerdaten aus Anwendungssitzungen erneut verwendet, sollten Sie die Benutzerdatenordner speichern, andernfalls können Sie sie löschen.  Berücksichtigen Sie bei der Entscheidung, wie Sie Ihre Benutzerdatenordner verwalten, die folgenden Szenarien:  

*   Wenn derselbe Benutzer Ihre Anwendung wiederholt verwendet und der Webinhalt der Anwendung auf den Daten des Benutzers basiert, speichern Sie den Benutzerdatenordner.  Wenn mehrere Benutzer Ihre Anwendung wiederholt verwenden, erstellen Sie einen neuen Benutzerdatenordner für jeden neuen Benutzer, und speichern Sie den Benutzerdatenordner der einzelnen Benutzer.
*   Wenn Ihre Anwendung nicht über wiederholte Benutzer verfügt, erstellen Sie einen neuen Benutzerdatenordner für jeden Benutzer, und löschen Sie den vorherigen Benutzerdatenordner.  
    
## <a name="create-user-data-folders"></a>Erstellen von Benutzerdatenordnern  

Um den Speicherort des Benutzerdatenordners anzugeben, geben Sie den Parameter beim Aufrufen von `userDataFolder` [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \(Win32\) oder [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \(.NET\) an.  Nach der Erstellung werden Browserdaten aus Ihrem WebView2-Steuerelement in einem Unterordner von `userDataFolder` gespeichert.  Wenn `userDataFolder` dieser Parameter nicht angegeben ist, erstellt WebView2 Benutzerdatenordner an standardmäßigen Speicherorten wie folgt:  

*   Für verpackte Windows Store ist der Standardbenutzerordner der Unterordner im `ApplicationData\LocalFolder` Ordner des Pakets.  
*   Bei vorhandenen Desktop-Apps ist der Standardbenutzerdatenordner der Exe-Pfad Ihrer Anwendung + `.WebView2` .  Anstelle der Standardeinstellung wird empfohlen, einen Benutzerdatenordner anzugeben und ihn im selben Ordner zu erstellen, in dem alle anderen App-Daten gespeichert sind.  
    
## <a name="delete-user-data-folders"></a>Löschen von Benutzerdatenordnern  

Ihre Anwendung muss möglicherweise Benutzerdatenordner löschen:  

*   Beim Deinstallieren Ihrer App.  Wenn Sie gepackte Apps Windows Store deinstallieren, Windows Benutzerdatenordner automatisch gelöscht.  
*   So bereinigen Sie den browserdatenverlauf.  
*   So stellen Sie datenbeschädigungen wiederher.  
*   So entfernen Sie frühere Sitzungsdaten.  
    
> [!NOTE]
> Dateien in Benutzerdatenordnern werden möglicherweise weiterhin verwendet, nachdem die WebView2-Anwendung geschlossen wurde.  Warten Sie in diesem Fall, bis der Browserprozess und alle untergeordneten Prozesse beendet werden, bevor Sie den Ordner löschen.  Sie können die Prozess-ID des Browserprozesses mithilfe der `BrowserProcessId` Eigenschaft von WebView2 abrufen.  

## <a name="share-user-data-folders"></a>Freigeben von Benutzerdatenordnern  

WebView2-Steuerelemente können die gleichen Benutzerdatenordner für:  

*   [Optimieren Sie Systemressourcen,](../concepts/process-model.md) indem Sie in einem Browserprozess ausgeführt werden.  
*   Freigeben des Browserverlaufs und zwischengespeicherter Ressourcen.  
    
Berücksichtigen Sie folgendes beim Freigeben von Benutzerdatenordnern:  

1.  Stellen Sie beim erneuten Erstellen von WebView2-Steuerelementen zum Aktualisieren von Browserversionen mithilfe von [add_NewBrowserVersionAvailable](/microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable) \(Win32\) oder [NewBrowserVersionAvailable](/dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable) \(.NET\)-Ereignissen sicher, dass Browserprozesse beendet werden, und schließen Sie WebView2-Steuerelemente, die denselben Benutzerdatenordner gemeinsam verwenden.  Verwenden Sie zum Abrufen der Prozess-ID des Browserprozesses die `BrowserProcessId` Eigenschaft des WebView2-Steuerelements.  
1.  WebView2-Steuerelemente, die denselben Benutzerdatenordner gemeinsam verwenden, müssen die gleichen Optionen für [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \(Win32\) oder [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \(.NET\) verwenden.  Andern falls nicht, wird bei der WebView2-Erstellung ein Fehler mit `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)` angezeigt.  
    
Um verschiedene Teile Ihrer Anwendung zu isolieren oder wenn die Freigabe von Daten zwischen WebView2-Steuerelementen nicht erforderlich ist, können Sie verschiedene Benutzerdatenordner verwenden.  Eine Anwendung kann z. B. aus zwei WebView2-Steuerelementen bestehen, eines zum Anzeigen einer Ankündigung und das andere zum Anzeigen von Anwendungsinhalten.  In diesem Szenario können Entwickler unterschiedliche Benutzerdatenordner für jedes WebView2-Steuerelement verwenden.  

> [!NOTE]
> Jeder WebView2-Browserprozess verbraucht zusätzlichen Arbeitsspeicher und Speicherplatz.  Daher wird empfohlen, WebView2s nicht mit zu vielen verschiedenen Benutzerdatenordnern gleichzeitig zu ausführen.  
