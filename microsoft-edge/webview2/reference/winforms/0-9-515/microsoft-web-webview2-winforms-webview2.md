---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 25ea8367aa9d64d0a1066cf8c1564f4d9c9f05ed
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653714"
---
# Microsoft. Web. WebView2. WinForms. WebView2 Klasse 

Namespace: Microsoft. Web. WebView2. WinForms \
Assembly: Microsoft. Web. WebView2. WinForms. dll

```
class Microsoft.Web.WebView2.WinForms.WebView2
  : public Control
```

Steuerelement zum Einbetten von WebView2 in WinForms

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[ContentLoading](#contentloading) | ContentLoading wird nach dem Beginn einer Navigation zu einem neuen URI und dem Rendern des Inhalts dieses URIs ausgelöst.
[CoreWebView2Ready](#corewebview2ready) | Dieses Ereignis wird ausgelöst, wenn die [CoreWebView2](#corewebview2) des Steuerelements initialisiert wurde (unabhängig davon, wie die Initialisierung ausgelöst wurde), aber bevor Sie für irgendetwas verwendet wird.
[NavigationCompleted](#navigationcompleted) | NavigationCompleted-nach einer Navigation im Dokument der obersten Ebene wird das Rendering erfolgreich abgeschlossen.
[NavigationStarting](#navigationstarting) | NavigationStarting versendet, bevor eine neue Navigate-Datei für das Dokument der obersten Ebene des WebView2 gestartet wird.
[SourceChanged](#sourcechanged) | Die Quellcodeverteilung wird nach dem Ändern der Quelleigenschaft weitergeleitet.
[WebMessageReceived](#webmessagereceived) | WebMessageReceived sendet nach dem Senden einer Nachricht an den App-Host per Webinhalt `chrome.webview.postMessage` .
[CoreWebView2](#corewebview2) | Der zugrunde liegende CoreWebView2.
[Source](#source) | Die Source-Eigenschaft ist der URI des Dokuments der obersten Ebene des WebView2.
[ZoomFactor](#zoomfactor) | Der Zoomfaktor für die WebView.
[CanGoBack](#cangoback) | Gibt "true" zurück, wenn die WebView über die GoBack-Methode zu einer vorherigen Seite im Navigationsverlauf navigieren kann.
[CanGoForward](#cangoforward) | Gibt "true" zurück, wenn die WebView über die GoForward-Methode zu einer nächsten Seite im Navigationsverlauf navigieren kann.
[EnsureCoreWebView2Async](#ensurecorewebview2async) | Initialisierung der [CoreWebView2](#corewebview2)des Steuerelements explizit auslösen.
[ExecuteScriptAsync](#executescriptasync) | Führt das bereitgestellte Skript im Dokument der obersten Ebene des WebView2 aus.
[GoBack](#goback) | Navigieren Sie im Navigationsverlauf zur vorherigen Seite.
[GoForward](#goforward) | Navigieren Sie im Navigationsverlauf zur nächsten Seite.
[NavigateToString](#navigatetostring) | Rendern Sie den bereitgestellten HTML-Code als Dokument der obersten Ebene des WebView2.
[Laden](#reload) | Laden Sie das Dokument der obersten Ebene des WebView2.
[Stop](#stop) | Beenden Sie die Navigation in Progress in der WebView2.
[WebView2](#webview2) | Erstellen Sie ein neues WebView2 WinForms-Steuerelement.
[OnEnter](#onenter) | Geschützter Fokus Handler.
[OnSizeChanged](#onsizechanged) | Geschützter SizeChanged-Handler.
[OnVisibleChanged](#onvisiblechanged) | Geschützter Sichtbarkeits Handler.

## Member

#### ContentLoading 

ContentLoading wird nach dem Beginn einer Navigation zu einem neuen URI und dem Rendern des Inhalts dieses URIs ausgelöst.

> public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)

Dies entspricht dem ContentLoading-Ereignis im CoreWebView2. Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. ContentLoading.

#### CoreWebView2Ready 

Dieses Ereignis wird ausgelöst, wenn die [CoreWebView2](#corewebview2) des Steuerelements initialisiert wurde (unabhängig davon, wie die Initialisierung ausgelöst wurde), aber bevor Sie für irgendetwas verwendet wird.

> public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)

Sie sollten dieses Ereignis behandeln, wenn Sie eine einmalige Einrichtungs Operation für die CoreWebView2 durchführen müssen, für die Sie alle ihre Verwendungen beeinflussen möchten (beispielsweise das Hinzufügen von Ereignishandlern, das Konfigurieren von Einstellungen, das Installieren von Dokument Erstellungsskripts und das Hinzufügen von Host Objekten).

Dieses Ereignis stellt keine Argumente bereit, und der Absender ist das WebView2-Steuerelement, dessen CoreWebView2-Eigenschaft zum ersten Mal gültig (also ungleich null) ist.

#### NavigationCompleted 

NavigationCompleted-nach einer Navigation im Dokument der obersten Ebene wird das Rendering erfolgreich abgeschlossen.

> public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)

Dies entspricht dem NavigationCompleted-Ereignis im CoreWebView2. Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. NavigationCompleted.

#### NavigationStarting 

NavigationStarting versendet, bevor eine neue Navigate-Datei für das Dokument der obersten Ebene des WebView2 gestartet wird.

> public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)

Dies entspricht dem NavigationStarting-Ereignis im CoreWebView2. Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. NavigationStarting.

#### SourceChanged 

Die Quellcodeverteilung wird nach dem Ändern der Quelleigenschaft weitergeleitet.

> public event EventHandler< CoreWebView2SourceChangedEventArgs > [Quelle](#sourcechanged)

Dies kann während einer Navigation auftreten, oder wenn andernfalls das Skript auf der Seite den URI des Dokuments ändert. Dies entspricht dem CoreWebView2-Ereignis. Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. Quellcode.

#### WebMessageReceived 

WebMessageReceived sendet nach dem Senden einer Nachricht an den App-Host per Webinhalt `chrome.webview.postMessage` .

> public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)

Dies entspricht dem WebMessageReceived-Ereignis im CoreWebView2. Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. WebMessageReceived.

#### CoreWebView2 

Der zugrunde liegende CoreWebView2.

> öffentliche CoreWebView2- [CoreWebView2](#corewebview2)

Verwenden Sie diese Eigenschaft, um mehr Vorgänge für den WebView2-Inhalt durchzuführen, als auf dem WebView2 verfügbar gemacht wird. Dieser Wert ist NULL, bis er initialisiert wird. Sie können erzwingen, dass der zugrunde liegende CoreWebView2 über die InitializeAsync-Methode initialisiert wird.

#### Source 

Die Source-Eigenschaft ist der URI des Dokuments der obersten Ebene des WebView2.

> öffentliche URI- [Quelle](#source)

Das Festlegen der Quelle entspricht dem Aufruf von CoreWebView2. Navigate. Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, lautet diese Eigenschaft "about: blank". Wenn die Eigenschaft auf einen nicht absoluten URI oder Null festgesetzt ist, bleibt die Eigenschaft unverändert. Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. Navigate.

#### ZoomFactor 

Der Zoomfaktor für die WebView.

> öffentliches Doppel [ZoomFactor](#zoomfactor)

#### CanGoBack 

Gibt "true" zurück, wenn die WebView über die GoBack-Methode zu einer vorherigen Seite im Navigationsverlauf navigieren kann.

> public bool [CanGoBack](#cangoback)

Dies entspricht der CanGoBack-Eigenschaft für CoreWebView2. Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, ist diese Eigenschaft false. Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. CanGoBack.

#### CanGoForward 

Gibt "true" zurück, wenn die WebView über die GoForward-Methode zu einer nächsten Seite im Navigationsverlauf navigieren kann.

> public bool [CanGoForward](#cangoforward)

Dies entspricht der CanGoForward-Eigenschaft für CoreWebView2. Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, ist diese Eigenschaft false. Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. CanGoForward.

#### EnsureCoreWebView2Async 

Initialisierung der [CoreWebView2](#corewebview2)des Steuerelements explizit auslösen.

> öffentliche Aufgaben- [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment-Umgebung)

##### Parameter
* `environment` Eine zuvor erstellte CoreWebView2Environment, die zum Erstellen des CoreWebView2 verwendet werden soll. Durch das Erstellen einer eigenen Umgebung können Sie verschiedene Optionen steuern, die sich auf die Initialisierung des CoreWebView2 auswirken. Wenn Sie NULL (den Standardwert) übergeben, wird eine Standardumgebung erstellt und automatisch verwendet. 

##### Gibt
Eine Aufgabe, die den Hintergrund Initialisierungsprozess darstellt. Wenn die Aufgabe abgeschlossen ist, steht die CoreWebView2-Eigenschaft zur Verwendung zur Verfügung (also nicht-null). Beachten Sie, dass das [CoreWebView2Ready](#corewebview2ready) -Ereignis des Steuerelements aufgerufen wird, bevor die Aufgabe abgeschlossen ist. 

Das zusätzliche Aufrufen dieser Methode hat keine Auswirkungen (jede angegebene Umgebung wird ignoriert) und gibt dieselbe Aufgabe wie beim ersten Aufruf zurück. Das Aufrufen dieser Methode, nachdem die Initialisierung implizit ausgelöst wurde, indem die [Source](#source) -Eigenschaft festgelegt wird, hat keine Auswirkungen (jede angegebene Umgebung wird ignoriert) und gibt einfach eine Aufgabe zurück, die die bereits ausgeführte Initialisierung darstellt. 

##### Ausnahmen
* `System.InvalidOperationException` Wird ausgelöst, wenn Sie von einem nicht-UI-Thread aufgerufen werden.

#### ExecuteScriptAsync 

Führt das bereitgestellte Skript im Dokument der obersten Ebene des WebView2 aus.

> Public Async Task< Zeichenfolge > [ExecuteScriptAsync](#executescriptasync)(Zeichenfolgen Skript)

Dies entspricht der ExecuteScriptAsync-Methode auf der CoreWebView2. Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, löst diese Methode eine InvalidOperationException aus. Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. ExecuteScriptAsync.

#### GoBack 

Navigieren Sie im Navigationsverlauf zur vorherigen Seite.

> publicvoid [GoBack](#goback)()

Dies entspricht der GoBack-Methode auf der CoreWebView2. Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, hat diese Methode keine Auswirkungen. Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. GoBack.

#### GoForward 

Navigieren Sie im Navigationsverlauf zur nächsten Seite.

> publicvoid [GoForward](#goforward)()

Dies entspricht der GoForward-Methode auf der CoreWebView2. Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, hat diese Methode keine Auswirkungen. Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. GoForward.

#### NavigateToString 

Rendern Sie den bereitgestellten HTML-Code als Dokument der obersten Ebene des WebView2.

> publicvoid [NavigateToString](#navigatetostring)(String htmlContent)

Dies entspricht der NavigateToString-Methode auf der CoreWebView2. Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, löst diese Methode eine InvalidOperationException aus. Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. NavigateToString.

#### Laden 

Laden Sie das Dokument der obersten Ebene des WebView2.

> public void [Reload](#reload)()

Dies entspricht der Reload-Methode auf der CoreWebView2. Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, löst diese Methode eine InvalidOperationException aus. Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. Reload.

#### Stop 

Beenden Sie die Navigation in Progress in der WebView2.

> öffentlicher void- [Stopp](#stop)()

Dies entspricht der Stop-Methode auf der CoreWebView2. Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, hat diese Methode keine Auswirkungen. Weitere Informationen finden Sie unter CoreWebView2. Stop-Dokumentation.

#### WebView2 

Erstellen Sie ein neues WebView2 WinForms-Steuerelement.

> Public [WebView2](#webview2)()

Nach der Erstellung ist die CoreWebView2-Eigenschaft NULL. Rufen Sie [EnsureCoreWebView2Async](#ensurecorewebview2async) auf, um die zugrunde liegende CoreWebView2 zu initialisieren.

#### OnEnter 

Geschützter Fokus Handler.

> protected override void [OnEnter](#onenter)(EventArgs e)

#### OnSizeChanged 

Geschützter SizeChanged-Handler.

> protected override void [onsized](#onsizechanged)(EventArgs e)

#### OnVisibleChanged 

Geschützter Sichtbarkeits Handler.

> protected override void [onvisibled](#onvisiblechanged)(EventArgs e)

