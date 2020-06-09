---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 986b1dc2870375243a0ee664262216105edd95a8
ms.sourcegitcommit: 3f8c8a5643e416b0851254833f9771192883ec45
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699500"
---
# Microsoft. Web. WebView2. Core. CoreWebView2Environment Klasse 

> [!NOTE]
> Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen. Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Dies stellt die WebView2-Umgebung dar.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[BrowserVersionString](#browserversionstring) | Die Browser Versionsinformationen des aktuellen CoreWebView2Environment, einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.
[NewBrowserVersionAvailable](#newbrowserversionavailable) | Das NewBrowserVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.
[CreateAsync](#createasync) | Erstellt eine immergrüne WebView2-Umgebung unter Verwendung der installierten Edge-Version.
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | Erstellen Sie einen neuen WebView asynchron.
[CreateWebResourceResponse](#createwebresourceresponse) | Erstellen Sie ein neues Webressourcen-Antwortobjekt.

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

#### CreateAsync 

Erstellt eine immergrüne WebView2-Umgebung unter Verwendung der installierten Edge-Version.

> public static Async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [createasync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions Optionen)

##### Parameter
* `browserExecutableFolder` Der relative Pfad zu dem Ordner, in dem sich der eingebettete Edge befindet. 

* `userDataFolder` userDataFolder kann angegeben werden, um den Standardspeicherort des Benutzerdatenordners für WebView2 zu ändern. 

* `options` Optionen zum Erstellen der WebView2-Umgebung

#### CreateCoreWebView2ControllerAsync 

Erstellen Sie einen neuen WebView asynchron.

> Public Async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)

ParentWindow ist das HWND, in dem die WebView-Ansicht angezeigt werden soll und von der die Eingabe empfangen werden soll. Die WebView fügt dem bereitgestellten Fenster während der Erstellung von WebView ein untergeordnetes Fenster hinzu. Die Z-Reihenfolge und andere Elemente, die von der Reihenfolge der nebengeordneten Fenster beeinflusst werden, sind dementsprechend betroffen.

Es wird empfohlen, die Anwendungsbenutzer Modell-ID für den Prozess oder das Anwendungsfenster festzulegen. Wenn None gesetzt ist, wird bei der Erstellung von WebView eine generierte Anwendungsbenutzer Modell-ID auf das Stammfenster von ParentWindow eingestellt.

#### CreateWebResourceResponse 

Erstellen Sie ein neues Webressourcen-Antwortobjekt.

> Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int Statuscode, String ReasonPhrase, String Headers)

Die Kopfzeilen ist die unformatierte Antwortheader Zeichenfolge, die durch einen Zeilenumbruch getrennt ist. Es ist auch möglich, dieses Objekt mit einer leeren Headerzeichenfolge zu erstellen und dann die Kopfzeilen Zeile für Zeile mithilfe der CoreWebView2HttpResponseHeaders zu erstellen. Informationen zu anderen Parametern finden Sie unter CoreWebView2WebResourceResponse.

