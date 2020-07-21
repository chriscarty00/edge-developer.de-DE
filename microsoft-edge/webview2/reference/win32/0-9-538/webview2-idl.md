---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Globals
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 12a730a07945d5f099cd2a0f45a9f2ec5ed02f8c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885548"
---
# Globals 

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[CompareBrowserVersions](#comparebrowserversions) | Diese Methode ist für alle Personen, die die Version richtig vergleichen möchten, um zu ermitteln, welche Version neuer, älter oder gleich ist.
[CreateCoreWebView2Environment](#createcorewebview2environment) | Erstellt eine immergrüne WebView2-Umgebung unter Verwendung der installierten Edge-Version.
[CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions) | DLL-Export zum Erstellen einer WebView2-Umgebung mit einer benutzerdefinierten Version von Edge, Benutzerdatenverzeichnis und/oder zusätzlichen Optionen.
[GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring) | Rufen Sie die Browser Versionsinformationen einschließlich des Kanal namens ab, wenn es sich nicht um den stabilen Kanal oder den eingebetteten Edge handelt.

## Member

#### CompareBrowserVersions 

> Public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR Version1, PCWSTR Version2, int * result)

Diese Methode ist für alle Personen, die die Version richtig vergleichen möchten, um zu ermitteln, welche Version neuer, älter oder gleich ist.

Sie kann verwendet werden, um zu ermitteln, ob webview2 oder eine bestimmte featurebasis auf Version verwendet werden soll. Legt den Wert des Ergebnisses auf-1, 0 oder 1 fest, wenn version1 kleiner als, gleich oder größer als Version2 ist. Gibt E_INVALIDARG zurück, wenn keine der Versionszeichenfolgen analysiert werden kann oder ein Eingabeparameter NULL ist. Die Eingabe kann die von GetAvailableCoreWebView2BrowserVersionString abgerufene VERSIONINFO direkt verwenden, Kanalinformationen werden ignoriert.

#### CreateCoreWebView2Environment 

> Public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)([ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) * environment_created_handler)

Erstellt eine immergrüne WebView2-Umgebung unter Verwendung der installierten Edge-Version.

Dies entspricht dem Aufruf von CreateCoreWebView2EnvironmentWithOptions mit nullptr für browserExecutableFolder, userDataFolder, additionalBrowserArguments. Weitere Informationen finden Sie unter CreateCoreWebView2EnvironmentWithOptions.

#### CreateCoreWebView2EnvironmentWithOptions 

> Public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR browserExecutableFolder, PCWSTR userDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) * environmentoptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) * environment_created_handler)

DLL-Export zum Erstellen einer WebView2-Umgebung mit einer benutzerdefinierten Version von Edge, Benutzerdatenverzeichnis und/oder zusätzlichen Optionen.

Verwenden Sie `browserExecutableFolder` diese Option, um anzugeben, ob WebView2-Steuerelemente eine eingebettete Version von Edge oder die installierte Version von Edge verwenden, die auf einem Clientcomputer vorhanden ist. Wenn Sie eine eingebettete Version von Edge verwenden möchten, übergeben Sie den relativen Pfad des Ordners, in dem sich die eingebettete Version von Edge befindet `browserExecutableFolder` . Wenn Sie die eingebettete Version von Edge abrufen möchten, kopieren Sie den Namen der Version des Ordners aus Ihrer installierten Edge-Version auf einem Clientcomputer. Kopieren Sie beispielsweise den `73.0.52.0` Ordner aus dem Ordner, in dem Edge Version 73.0.52.0 installiert war. Stellen Sie sicher, dass der Ordner sowohl die **msedgewebview2.exe** als auch **msedge.dll** Dateien enthält. Zum Erstellen von WebView2-Steuerelementen, die die installierte Version von Edge verwenden, die auf Clientcomputern vorhanden ist, übergeben Sie eine NULL oder eine leere Zeichenfolge an `browserExecutableFolder` . In diesem Szenario versucht die API, eine kompatible Version von Edge zu finden, die auf dem Clientcomputer (zuerst auf Computerebene und dann pro Benutzer) unter Verwendung der ausgewählten Kanaleinstellung installiert ist.

Die standardmäßige Kanal Suchreihenfolge ist stable, Beta, dev und Canary. Wenn eine WEBVIEW2_RELEASE_CHANNEL_PREFERENCE Umgebungsvariable oder ein anwendbarer releaseChannelPreference-Registrierungswert mit dem Wert 1 überschrieben wird, wird die Kanal Suchreihenfolge umgekehrt.

userDataFolder kann angegeben werden, um den Standardspeicherort des Benutzerdatenordners für WebView2 zu ändern. Der Pfad kann ein absoluter Dateipfad oder ein relativer Dateipfad sein, der als relativ zur ausführbaren Datei des aktuellen Prozesses interpretiert wird. Andernfalls ist der standardmäßige benutzerdatenordner für UWP-apps der APP-Datenordner für das Paket. bei nicht-UWP-apps wird der standardmäßige benutzerdatenordner `{Executable File Name}.WebView2` im gleichen Verzeichnis neben der ausführbaren App erstellt. Bei der WebView2-Erstellung kann ein Fehler auftreten, wenn die ausführbare Datei in einem Verzeichnis ausgeführt wird, in dem der Prozess keine Berechtigung zum Erstellen eines neuen Ordners aufweist. Die APP ist dafür verantwortlich, ihren benutzerdatenordner zu bereinigen, wenn Sie fertig sind.

Beachten Sie, dass ein Browserprozess möglicherweise für Webansichten freigegeben wird, wenn die WebView-Erstellung mit HRESULT_FROM_WIN32 (ERROR_INVALID_STATE) fehlschlägt, wenn die angegebenen Optionen nicht den Optionen der Webansichten entsprechen, die derzeit im freigegebenen Browserprozess ausgeführt werden.

environment_created_handler ist das Ergebnis des Handlers für den asynchronen Vorgang, der die WebView2Environment enthalten wird, die erstellt wurde.

Die browserExecutableFolder-, userDataFolder-und additionalBrowserArguments-Werte von environmentoptions können von Werten überschrieben werden, die entweder in Umgebungsvariablen oder in der Registrierung angegeben sind.

Beim Erstellen eines WebView2Environment werden die folgenden Umgebungsvariablen überprüft:

```
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

Wenn eine Außerkraftsetzungs Umgebungsvariable gefunden wird, verwenden wir die browserExecutableFolder-, userDataFolder-und additionalBrowserArguments-Werte als Ersatz für die entsprechenden Werte in CreateCoreWebView2EnvironmentWithOptions-Parametern.

Zwar werden keine strengen Außerkraftsetzungen vorhanden, es gibt jedoch zusätzliche Umgebungsvariablen, die festgesetzt werden können:

```
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

Wenn Sie mit einem nicht leeren Wert gefunden wird, deutet dies darauf hin, dass die WebView unter einem Skriptdebugger gestartet wird. In diesem Fall gibt die WebView einen `Page.waitForDebugger` CDP-Befehl aus, der dazu führt, dass die Skriptausführung in der WebView beim Start angehalten wird, bis ein Debugger einen entsprechenden CDP-Befehl ausgibt, `Runtime.runIfWaitingForDebugger` um die Ausführung fortzusetzen. Hinweis: Es gibt keine Entsprechung dieser Umgebungsvariablen für den Registrierungsschlüssel.

```
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

Wenn Sie mit einem nicht leeren Wert gefunden wird, deutet dies darauf hin, dass die WebView unter einem Skriptdebugger gestartet wird, der auch Hostanwendungen unterstützt, die mehrere Webansichten verwenden. Der Wert wird als Bezeichner für eine Named Pipe verwendet, die geöffnet und geschrieben wird, wenn eine neue WebView von der Hostanwendung erstellt wird. Die Nutzlast entspricht der des JSON-Ziels "Remotedebuggen-Port" und kann vom externen Debugger zum Anfügen an eine bestimmte WebView-Instanz verwendet werden. Das Format der vom Debugger erstellten Pipe sollte wie folgt lauten: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}`

* `{app_name}` ist der Dateiname der Host-Anwendung exe, beispielsweise WebView2Example.exe

* `{pipe_name}` ist der Wert, der für WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER gesetzt ist.

Um das Debuggen der von der JSON angegebenen Ziele zu aktivieren, müssen Sie auch die WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS Umgebungsvariable so festlegen, dass Sie gesendet wird, `--remote-debugging-port={port_num}` wobei:

* `{port_num}` ist der Port, an dem der CDP-Server gebunden wird.

Beachten Sie, dass das Festlegen der Umgebungsvariablen WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER und WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS dazu führt, dass die in Ihrer Anwendung gehosteten Webansichten und deren Inhalte für Anwendungen von Drittanbietern wie Debuggern verfügbar gemacht werden.

Hinweis: Es gibt keine Entsprechung dieser Umgebungsvariablen für den Registrierungsschlüssel.

Wenn keine dieser Umgebungsvariablen vorhanden ist, wird die Registrierung als nächstes überprüft. Die folgenden Registrierungsschlüssel werden überprüft:

```
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

In dem unwahrscheinlichen Szenario, in dem einige Instanzen von WebView während eines Browser Updates geöffnet sind, könnten wir das Löschen von alten Edge-Browsern blockieren. Um zu vermeiden, dass der Speicherplatz knapp wird, schlägt eine neue WebView-Erstellung mit dem nächsten Fehler fehl, wenn erkannt wird, dass viele alte Versionen vorhanden sind.

```
ERROR_DISK_FULL
```

Die maximal zulässige Standardanzahl von Edge-Versionen beträgt 20.

Die maximal zulässige Anzahl Alter Edge-Versionen kann mit dem Wert der folgenden Umgebungsvariablen überschrieben werden.

```
WEBVIEW2_MAX_INSTANCES
```

Wenn die WebView von einem installierten Edge abhängt und deinstalliert wird, schlägt die spätere Erstellung mit dem nächsten Fehler fehl

```
ERROR_PRODUCT_UNINSTALLED
```

Als erstes überprüfen wir root als HKLM und dann HKCU. Die Anwendungs-ID des aufrufenden Prozesses wird zunächst auf die Anwendungsbenutzer Modell-ID festgesetzt, und wenn kein entsprechender Registrierungsschlüssel vorhanden ist, wird die APP auf den ausführbaren Namen des Prozesses des Aufrufers festgesetzt, oder wenn es sich nicht um einen Registrierungsschlüssel handelt, "*". Wenn ein Registrierungsschlüssel für die Überschreibung gefunden wird, verwenden wir die Registrierungswerte browserExecutableFolder, userDataFolder und additionalBrowserArguments als Ersatz für die entsprechenden Werte in CreateCoreWebView2EnvironmentWithOptions-Parametern.

#### GetAvailableCoreWebView2BrowserVersionString 

> Public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR browserExecutableFolder, LPWSTR * VERSIONINFO)

Rufen Sie die Browser Versionsinformationen einschließlich des Kanal namens ab, wenn es sich nicht um den stabilen Kanal oder den eingebetteten Edge handelt.

Kanalnamen sind Beta, dev und Canary. Wenn für die browserExecutableFolder oder die Kanaleinstellung eine Überschreibung vorhanden ist, wird die Außerkraftsetzung verwendet. Wenn keine Überschreibung vorhanden ist, wird der an GetAvailableCoreWebView2BrowserVersionString übergebene Parameter verwendet.

