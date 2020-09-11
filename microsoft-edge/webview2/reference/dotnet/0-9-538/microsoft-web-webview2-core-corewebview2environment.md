---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Environment
ms.openlocfilehash: d1e30c17239eb1b609eb3f2c63e48a3a59616131
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011027"
---
# 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Environment Klasse 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Dies stellt die WebView2-Umgebung dar.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[BrowserVersionString](#browserversionstring) | Die Browser Versionsinformationen des aktuellen CoreWebView2Environment, einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.
[NewBrowserVersionAvailable](#newbrowserversionavailable) | Das NewBrowserVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.
[CompareBrowserVersions](#comparebrowserversions) | Vergleichen Sie die Browserversionen korrekt, um zu ermitteln, welche Version neuer, älter oder gleich ist.
[CreateAsync](#createasync) | Erstellt eine immergrüne WebView2-Umgebung unter Verwendung der installierten Edge-Version.
[CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync) | Erstellen Sie ein neues WebView-Element für die Verwendung mit Visual Hosting asynchron.
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | Erstellen Sie einen neuen WebView asynchron.
[CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo) | Erstellen Sie ein leeres CoreWebView2PointerInfo.
[CreateWebResourceResponse](#createwebresourceresponse) | Erstellen Sie ein neues Webressourcen-Antwortobjekt.
[GetAvailableBrowserVersionString](#getavailablebrowserversionstring) | Rufen Sie die Browser Versionsinformationen einschließlich des Kanal namens ab, wenn es sich nicht um den stabilen Kanal oder den eingebetteten Edge handelt.
[GetProviderForHwnd](#getproviderforhwnd) | Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die CoreWebView2CompositionController zurück, die dem angegebenen HWND entspricht.

Webansichten, die aus einer Umgebung erstellt wurden, die im Browser Prozess ausgeführt wird, der mit Umgebungsparametern und aus einer Umgebung erstellten Objekten erstellt wurde, sollten in derselben Umgebung verwendet werden. Die Verwendung in unterschiedlichen Umgebungen ist nicht garantiert kompatibel und kann fehlerhaft sein.

## Member

#### BrowserVersionString 

Die Browser Versionsinformationen des aktuellen CoreWebView2Environment, einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.

> public String [BrowserVersionString](#browserversionstring)

Dies entspricht dem Format der GetAvailableCoreWebView2BrowserVersionString-API. Kanalnamen sind "Beta", "dev" und "Canary".

#### NewBrowserVersionAvailable 

Das NewBrowserVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.

> public event EventHandler<-Objekt > [NewBrowserVersionAvailable](#newbrowserversionavailable)

Wenn Sie die neuere Version des Browsers verwenden möchten, müssen Sie eine neue Umgebung und WebView erstellen. Dieses Ereignis wird nur für eine neue Version aus dem gleichen Edge-Kanal ausgelöst, von dem aus der Code ausgeführt wird. Wenn Sie nicht mit installiertem Edge ausgeführt wird, wird kein Ereignis ausgelöst.

Da ein benutzerdatenordner nur von einem Browserprozess gleichzeitig verwendet werden kann, wenn Sie denselben benutzerdatenordner in den Webansichten mithilfe der neuen Browserversion verwenden möchten, müssen Sie die Umgebung und Webansichten schließen, die zuerst die ältere Version des Browsers verwenden. Oder fordern Sie den Benutzer einfach auf, die APP neu zu starten.

#### CompareBrowserVersions 

Vergleichen Sie die Browserversionen korrekt, um zu ermitteln, welche Version neuer, älter oder gleich ist.

> public static int [CompareBrowserVersions](#comparebrowserversions)(String Version1, String Version2)

Gibt-1, 0 oder 1 zurück, je nachdem, ob Version1 kleiner als, gleich oder größer als Version2 ist.

##### Parameter
* `version1` Eine der zu vergleichenden Versionszeichenfolgen. 

* `version2` Die andere zu vergleichende Versionszeichenfolge.

#### CreateAsync 

Erstellt eine immergrüne WebView2-Umgebung unter Verwendung der installierten Edge-Version.

> public static Async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [createasync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions Optionen)

##### Parameter
* `browserExecutableFolder` Der relative Pfad zu dem Ordner, in dem sich der eingebettete Edge befindet. 

* `userDataFolder` userDataFolder kann angegeben werden, um den Standardspeicherort des Benutzerdatenordners für WebView2 zu ändern. 

* `options` Optionen zum Erstellen der WebView2-Umgebung

#### CreateCoreWebView2CompositionControllerAsync 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Erstellen Sie ein neues WebView-Element für die Verwendung mit Visual Hosting asynchron.

> Public Async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)

ParentWindow ist das HWND, in dem die APP die visuelle Struktur von WebView verbindet. Hierbei handelt es sich um das HWND, in dem die APP Zeiger-und Mauseingaben für die WebView erhält (und SendMouseInput/SendPointerInput für Forward verwenden muss). Wenn die APP die visuelle WebView-Struktur unter einem anderen Fenster verschiebt, muss CoreWebView2CompositionController. ParentWindow so eingestellt werden, dass das neue übergeordnete HWND der visuellen Struktur aktualisiert wird.

Legen Sie die RootVisualTarget-Eigenschaft für das erstellte CoreWebView2CompositionController-Objekt so ein, dass es eine visuelle Struktur bereitstellt

Es wird empfohlen, die Anwendungsbenutzer Modell-ID für den Prozess oder das Anwendungsfenster festzulegen. Wenn None gesetzt ist, wird bei der Erstellung von WebView eine generierte Anwendungsbenutzer Modell-ID auf das Stammfenster von ParentWindow eingestellt.

#### CreateCoreWebView2ControllerAsync 

Erstellen Sie einen neuen WebView asynchron.

> Public Async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)

ParentWindow ist das HWND, in dem die WebView-Ansicht angezeigt werden soll und von der die Eingabe empfangen werden soll. Die WebView fügt dem bereitgestellten Fenster während der Erstellung von WebView ein untergeordnetes Fenster hinzu. Die Z-Reihenfolge und andere Elemente, die von der Reihenfolge der nebengeordneten Fenster beeinflusst werden, sind dementsprechend betroffen.

Es wird empfohlen, die Anwendungsbenutzer Modell-ID für den Prozess oder das Anwendungsfenster festzulegen. Wenn None gesetzt ist, wird bei der Erstellung von WebView eine generierte Anwendungsbenutzer Modell-ID auf das Stammfenster von ParentWindow eingestellt.

#### CreateCoreWebView2PointerInfo 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Erstellen Sie ein leeres CoreWebView2PointerInfo.

> Public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()

Der zurückgegebene CoreWebView2PointerInfo muss mit allen relevanten Informationen gefüllt werden, bevor SendPointerInput aufgerufen wird.

#### CreateWebResourceResponse 

Erstellen Sie ein neues Webressourcen-Antwortobjekt.

> Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int Statuscode, String ReasonPhrase, String Headers)

Die Kopfzeilen ist die unformatierte Antwortheader Zeichenfolge, die durch einen Zeilenumbruch getrennt ist. Es ist auch möglich, dieses Objekt mit einer leeren Headerzeichenfolge zu erstellen und dann die Kopfzeilen Zeile für Zeile mithilfe der CoreWebView2HttpResponseHeaders zu erstellen. Informationen zu anderen Parametern finden Sie unter CoreWebView2WebResourceResponse.

#### GetAvailableBrowserVersionString 

Rufen Sie die Browser Versionsinformationen einschließlich des Kanal namens ab, wenn es sich nicht um den stabilen Kanal oder den eingebetteten Edge handelt.

> public static String [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(String browserExecutableFolder)

##### Parameter
* `browserExecutableFolder` Der relative Pfad zu dem Ordner, in dem sich der eingebettete Edge befindet.

#### GetProviderForHwnd 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die CoreWebView2CompositionController zurück, die dem angegebenen HWND entspricht.

> public Object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)

