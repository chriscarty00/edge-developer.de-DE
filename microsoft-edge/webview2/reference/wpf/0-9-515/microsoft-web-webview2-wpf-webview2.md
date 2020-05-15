---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/13/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: f2c3bcb5334abc907a838971ebc1773b6485194f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653787"
---
# Microsoft. Web. WebView2. WPF. WebView2 Klasse 

Namespace: Microsoft. Web. WebView2. WPF \
Assembly: Microsoft. Web. WebView2. WPF. dll

```
class Microsoft.Web.WebView2.Wpf.WebView2
  : public HwndHost
```

Ein Steuerelement zum Einbetten von Webinhalten in eine WPF-Anwendung.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[ContentLoading](#contentloading) | Ein Wrapper um das CoreWebView2. ContentLoading-Ereignis von CoreWebView2.
[CoreWebView2Ready](#corewebview2ready) | Dieses Ereignis wird ausgelöst, wenn die CoreWebView2 des Steuerelements initialisiert wurde (unabhängig davon, wie die Initialisierung ausgelöst wurde), aber bevor Sie für irgendetwas verwendet wird.
[NavigationCompleted](#navigationcompleted) | Ein Wrapper um das CoreWebView2. NavigationCompleted-Ereignis von CoreWebView2.
[NavigationStarting](#navigationstarting) | Ein Wrapper um das CoreWebView2. NavigationStarting-Ereignis von CoreWebView2.
[SourceChanged](#sourcechanged) | Ein Wrapper um das CoreWebView2. Sourcecode-Ereignis von CoreWebView2.
[WebMessageReceived](#webmessagereceived) | Ein Wrapper um das CoreWebView2. WebMessageReceived-Ereignis von CoreWebView2.
[CanGoBack](#cangoback) | Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.
[CanGoForward](#cangoforward) | Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.
[CoreWebView2](#corewebview2) | Greifen Sie auf die vollständige Funktionalität der zugrunde liegenden Core. CoreWebView2-com-API zu.
[CreationProperties](#creationproperties) | Ruft eine Sammlung von Optionen ab, die während der Initialisierung des CoreWebView2 des Steuerelements verwendet werden, oder legt diese fest.
[Source](#source) | Der URI der obersten Ebene, den die WebView aktuell anzeigt (oder wird angezeigt, sobald die Initialisierung des CoreWebView2-Endgeräts endet).
[EnsureCoreWebView2Async](#ensurecorewebview2async) | Initialisierung der CoreWebView2 des Steuerelements explizit auslösen.
[ExecuteScriptAsync](#executescriptasync) | Führt JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.
[GoBack](#goback) | Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.
[GoForward](#goforward) | Navigiert die WebView zur nächsten Seite im Navigationsverlauf.
[NavigateToString](#navigatetostring) | Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.
[Laden](#reload) | Lädt die aktuelle Seite neu.
[Stop](#stop) | Stoppt alle Navigations-und ausstehenden Ressourcen Abrufe.
[WebView2](#webview2) | Erstellt eine neue Instanz eines WebView2-Steuerelements.
[BuildWindowCore](#buildwindowcore) | Dies wird von HwndHost überschrieben und aufgerufen, um uns zu beauftragen, unser HWND zu erstellen.
[DestroyWindowCore](#destroywindowcore) | Dies wird von HwndHost überschrieben und aufgerufen, um uns anzuweisen, unser HWND zu zerstören.
[Löschen](#dispose) | Dies wird von unserer Basisklasse entsprechend der typischen Implementierung des IDispose-Musters aufgerufen.
[HasFocusWithinCore](#hasfocuswithincore) | Dies wird von HwndHost überschrieben und aufgerufen, wenn WPF wissen muss, ob sich der Fokus in unserem Steuerelement/Fenster befindet.
[OnKeyDown](#onkeydown) | Dies wird von UIElement überschrieben und aufgerufen, damit wir die Eingabe von Tasten drücken verarbeiten können.
[OnKeyUp](#onkeyup) | Siehe OnKeyDown.
[OnPreviewKeyDown](#onpreviewkeydown) | Dies ist die "Vorschau" (also
[OnPreviewKeyUp](#onpreviewkeyup) | Siehe OnPreviewKeyDown.
[OnWindowPositionChanged](#onwindowpositionchanged) | Dieser wird von HwndHost überschrieben und aufgerufen, wenn sich der Standort des Steuerelements geändert hat.
[TabIntoCore](#tabintocore) | Dies wird von HwndHost überschrieben und wird aufgerufen, um uns mitzuteilen, dass die Tab-Taste dazu geführt hat, dass der Fokus in unser Control/Window verschoben wurde.

Dieses Steuerelement ist effektiv ein Wrapper um die WebView2-com-API, in dem Sie die Dokumentation finden können: [https://aka.ms/webview2](https://aka.ms/webview2) Sie können direkt auf die zugrunde liegende ICoreWebView2-Schnittstelle und ihre gesamte Funktionalität zugreifen, indem Sie auf die CoreWebView2-Eigenschaft zugreifen. Einige der gängigsten com-Funktionen können auch direkt über Wrappermethoden/Eigenschaften/Ereignisse für das Steuerelement aufgerufen werden.

Bei der Erstellung ist die CoreWebView2-Eigenschaft des Steuerelements NULL. Dies liegt daran, dass das Erstellen der CoreWebView2 eine kostspielige Operation ist, die Dinge wie das Starten von Edge-Browser-Prozessen umfasst. Es gibt zwei Möglichkeiten, das Erstellen der CoreWebView2 zu veranlassen: 1) rufen Sie die EnsureCoreWebView2Async-Methode auf. Dies wird als explizite Initialisierung bezeichnet. 2) stellen Sie die Source-Eigenschaft ein, die beispielsweise über Markup erfolgen kann. Dies wird als implizite Initialisierung bezeichnet. Mit einer der beiden Optionen wird die Initialisierung im Hintergrund gestartet, und Sie kehren zum Aufrufer zurück, ohne darauf zu warten, dass er beendet wird. Wenn Sie Optionen für den Initialisierungsprozess angeben möchten, übergeben Sie entweder Ihr eigenes CoreWebView2Environment an EnsureCoreWebView2Async, oder legen Sie die CreationProperties-Eigenschaft des Steuerelements vor der Initialisierung fest.

Wenn die Initialisierung beendet wurde (unabhängig davon, wie Sie ausgelöst wurde), treten die folgenden Dinge in dieser Reihenfolge auf: 1) das CoreWebView2Ready-Ereignis des Steuerelements wird aufgerufen. Wenn Sie vor der Verwendung eine einmalige Setup Operation für das CoreWebView2 durchführen müssen, sollten Sie dies in einem Handler für dieses Ereignis tun. 2) Wenn ein URI auf die Source-Eigenschaft gesetzt wurde, wird das Steuerelement im Hintergrund zu ihm navigieren (d. h., diese Schritte werden fortgesetzt, ohne darauf zu warten, dass die Navigation beendet wird). 3) die Aufgabe, die von EnsureCoreWebView2Async zurückgegeben wird, wird abgeschlossen.

Weitere Informationen zu den Methoden/Eigenschaften/Ereignissen, die am Initialisierungsprozess beteiligt sind, finden Sie in der jeweiligen Dokumentation.

Da das CoreWebView2-Steuerelement ein sehr Schwergewichts Objekt ist (potenziell verantwortlich für mehrere ausgeführte Prozesse und Megabytes an Speicherplatz), implementiert das Steuerelement IDisposable, um eine explizite Möglichkeit zum Freigeben bereitzustellen. Durch Aufrufen von Dispose werden die CoreWebView2 und die zugrunde liegenden Ressourcen (mit Ausnahme der von anderen Webansichten verwendeten) freigegeben und CoreWebView2 auf Null zurückgesetzt. Nachdem Dispose aufgerufen wurde, kann CoreWebView2 nicht erneut initialisiert werden, und jeder Versuch, die Funktionalität zu verwenden, die dies erfordert, löst eine ObjectDisposedException aus.

Beachten Sie, dass dieses Steuerelement HwndHost erweitert, um Fenster einzubetten, die außerhalb des WPF-Ökosystems Leben. Dies hat Auswirkungen auf das Eingabe-und Ausgabeverhalten des Steuerelements sowie auf die Funktionalität, die es von UIElement und FrameworkElement erbt. Weitere Informationen finden Sie in der HwndHost-und WPF/Win32-Interop-Dokumentation:

* [https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost](https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost)

* [https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf](https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf)

## Member

#### ContentLoading 

Ein Wrapper um das CoreWebView2. ContentLoading-Ereignis von CoreWebView2.

> public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)

Der einzige Unterschied zwischen diesem Ereignis und CoreWebView2. ContentLoading ist der erste Parameter, der an Handler übergeben wird. Handler dieses Ereignisses empfangen das WebView2-Steuerelement, während Handler von CoreWebView2. ContentLoading die CoreWebView2-Instanz empfangen.

#### CoreWebView2Ready 

Dieses Ereignis wird ausgelöst, wenn die CoreWebView2 des Steuerelements initialisiert wurde (unabhängig davon, wie die Initialisierung ausgelöst wurde), aber bevor Sie für irgendetwas verwendet wird.

> public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)

Sie sollten dieses Ereignis behandeln, wenn Sie eine einmalige Einrichtungs Operation für die CoreWebView2 durchführen müssen, für die Sie alle ihre Verwendungen beeinflussen möchten (beispielsweise das Hinzufügen von Ereignishandlern, das Konfigurieren von Einstellungen, das Installieren von Dokument Erstellungsskripts und das Hinzufügen von Host Objekten). Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.

Dieses Ereignis stellt keine Argumente bereit, und der Absender ist das WebView2-Steuerelement, dessen CoreWebView2-Eigenschaft zum ersten Mal gültig (also ungleich null) ist.

#### NavigationCompleted 

Ein Wrapper um das CoreWebView2. NavigationCompleted-Ereignis von CoreWebView2.

> public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)

Der einzige Unterschied zwischen diesem Ereignis und CoreWebView2. NavigationCompleted ist der erste Parameter, der an Handler übergeben wird. Handler dieses Ereignisses empfangen das WebView2-Steuerelement, während Handler von CoreWebView2. NavigationCompleted die CoreWebView2-Instanz empfangen.

#### NavigationStarting 

Ein Wrapper um das CoreWebView2. NavigationStarting-Ereignis von CoreWebView2.

> public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)

Der einzige Unterschied zwischen diesem Ereignis und CoreWebView2. NavigationStarting ist der erste Parameter, der an Handler übergeben wird. Handler dieses Ereignisses empfangen das WebView2-Steuerelement, während Handler von CoreWebView2. NavigationStarting die CoreWebView2-Instanz empfangen.

#### SourceChanged 

Ein Wrapper um das CoreWebView2. Sourcecode-Ereignis von CoreWebView2.

> public event EventHandler< CoreWebView2SourceChangedEventArgs > [Quelle](#sourcechanged)

Der einzige Unterschied zwischen diesem Ereignis und CoreWebView2. Sourcecode ist der erste Parameter, der an Handler übergeben wird. Handler dieses Ereignisses empfangen das WebView2-Steuerelement, während Handler von CoreWebView2. sourced die CoreWebView2-Instanz empfangen.

#### WebMessageReceived 

Ein Wrapper um das CoreWebView2. WebMessageReceived-Ereignis von CoreWebView2.

> public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)

Der einzige Unterschied zwischen diesem Ereignis und CoreWebView2. WebMessageReceived ist der erste Parameter, der an Handler übergeben wird. Handler dieses Ereignisses empfangen das WebView2-Steuerelement, während Handler von CoreWebView2. WebMessageReceived die CoreWebView2-Instanz empfangen.

#### CanGoBack 

Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.

> public bool [CanGoBack](#cangoback)

Wrapper um die CoreWebView2. CanGoBack-Eigenschaft von CoreWebView2. Wenn CoreWebView2 noch nicht initialisiert ist, wird false zurückgegeben.

#### CanGoForward 

Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.

> public bool [CanGoForward](#cangoforward)

Wrapper um die CoreWebView2. CanGoForward-Eigenschaft von CoreWebView2. Wenn CoreWebView2 noch nicht initialisiert ist, wird false zurückgegeben.

#### CoreWebView2 

Greifen Sie auf die vollständige Funktionalität der zugrunde liegenden Core. CoreWebView2-com-API zu.

> öffentliche CoreWebView2- [CoreWebView2](#corewebview2)

Gibt NULL zurück, bis die Initialisierung abgeschlossen ist. Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.

##### Ausnahmen
* `InvalidOperationException` Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread). Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.

#### CreationProperties 

Ruft eine Sammlung von Optionen ab, die während der Initialisierung des CoreWebView2 des Steuerelements verwendet werden, oder legt diese fest.

> öffentliche CoreWebView2CreationProperties- [CreationProperties](#creationproperties)

Das Festlegen dieser Eigenschaft funktioniert nicht, nachdem die Initialisierung des CoreWebView2 des Steuerelements begonnen hat (der alte Wert bleibt erhalten). Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.

#### Source 

Der URI der obersten Ebene, den die WebView aktuell anzeigt (oder wird angezeigt, sobald die Initialisierung des CoreWebView2-Endgeräts endet).

> öffentliche URI- [Quelle](#source)

Im Allgemeinen entspricht das Abrufen dieser Eigenschaft dem Abrufen der CoreWebView2. Source-Eigenschaft von CoreWebView2, und das Festlegen dieser Eigenschaft entspricht dem Aufrufen der CoreWebView2. Navigate-Methode für CoreWebView2. Wenn Sie diese Eigenschaft abrufen, bevor die CoreWebView2 initialisiert wurde, wird der letzte URI abgerufen, der auf ihn gesetzt wurde. Wenn diese Eigenschaft vor dem Initialisieren der CoreWebView2-Eigenschaft festgelegt wurde, wird die Initialisierung im Hintergrund gestartet (falls Sie noch nicht ausgeführt wird), nachdem die WebView2 zum angegebenen URI navigiert. Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.

##### Ausnahmen
* `ObjectDisposedException` Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.

#### EnsureCoreWebView2Async 

Initialisierung der CoreWebView2 des Steuerelements explizit auslösen.

> öffentliche Aufgaben- [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment-Umgebung)

Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.

##### Parameter
* `environment` Eine zuvor erstellte CoreWebView2Environment, die zum Erstellen des CoreWebView2 verwendet werden soll. Durch das Erstellen einer eigenen Umgebung können Sie verschiedene Optionen steuern, die sich auf die Initialisierung des CoreWebView2 auswirken. Wenn Sie eine Umgebung an diese Methode übergeben, werden alle in der CreationProperties-Eigenschaft angegebenen Einstellungen außer Kraft gesetzt. Wenn Sie NULL (den Standardwert) übergeben und kein Wert auf CreationProperties festgesetzt wurde, wird eine Standardumgebung erstellt und automatisch verwendet. 

##### Gibt
Eine Aufgabe, die den Hintergrund Initialisierungsprozess darstellt. Wenn die Aufgabe abgeschlossen ist, steht die CoreWebView2-Eigenschaft zur Verwendung zur Verfügung (also nicht-null). Beachten Sie, dass das CoreWebView2Ready-Ereignis des Steuerelements aufgerufen wird, bevor die Aufgabe abgeschlossen ist. 

Das zusätzliche Aufrufen dieser Methode hat keine Auswirkungen (jede angegebene Umgebung wird ignoriert) und gibt dieselbe Aufgabe wie beim ersten Aufruf zurück. Das Aufrufen dieser Methode, nachdem die Initialisierung implizit ausgelöst wurde, indem die Source-Eigenschaft festgelegt wird, hat keine Auswirkungen (jede angegebene Umgebung wird ignoriert) und gibt einfach eine Aufgabe zurück, die die bereits ausgeführte Initialisierung darstellt. Beachten Sie, dass auch wenn diese Methode asynchron ist und eine Aufgabe zurückgibt, Sie dennoch im UI-Thread aufgerufen werden muss, wie die meisten öffentlichen Funktionen der meisten UI-Steuerelemente. 

##### Ausnahmen
* `InvalidOperationException` Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread). Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.

#### ExecuteScriptAsync 

Führt JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.

> Public Async Task< String > [ExecuteScriptAsync](#executescriptasync)(String javaScript)

Entspricht dem Aufrufen von CoreWebView2. ExecuteScriptAsync auf CoreWebView2

##### Ausnahmen
* `InvalidOperationException` Wird ausgelöst, wenn CoreWebView2 noch nicht initialisiert wurde.

* `InvalidOperationException` Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread). Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.

#### GoBack 

Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.

> publicvoid [GoBack](#goback)()

Entspricht dem Aufrufen von CoreWebView2. GoBack auf CoreWebView2, wenn CoreWebView2 noch nicht initialisiert wurde, dann aber nichts tut.

##### Ausnahmen
* `InvalidOperationException` Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread). Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.

#### GoForward 

Navigiert die WebView zur nächsten Seite im Navigationsverlauf.

> publicvoid [GoForward](#goforward)()

Entspricht dem Aufrufen von CoreWebView2. GoForward auf CoreWebView2, wenn CoreWebView2 noch nicht initialisiert wurde, dann aber nichts tut.

##### Ausnahmen
* `InvalidOperationException` Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread). Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.

#### NavigateToString 

Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.

> publicvoid [NavigateToString](#navigatetostring)(String htmlContent)

Entspricht dem Aufrufen von CoreWebView2. NavigateToString auf CoreWebView2

##### Ausnahmen
* `InvalidOperationException` Wird ausgelöst, wenn CoreWebView2 noch nicht initialisiert wurde.

" <exception cref="InvalidOperationException"> Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).  Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.

#### Laden 

Lädt die aktuelle Seite neu.

> public void [Reload](#reload)()

Entspricht dem Aufruf von CoreWebView2. Reload auf CoreWebView2

##### Ausnahmen
* `InvalidOperationException` Wird ausgelöst, wenn CoreWebView2 noch nicht initialisiert wurde.

" <exception cref="InvalidOperationException"> Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).  Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.

#### Stop 

Stoppt alle Navigations-und ausstehenden Ressourcen Abrufe.

> öffentlicher void- [Stopp](#stop)()

Entspricht dem Aufruf von CoreWebView2. Stop auf CoreWebView2

##### Ausnahmen
* `InvalidOperationException` Wird ausgelöst, wenn CoreWebView2 noch nicht initialisiert wurde.

" <exception cref="InvalidOperationException"> Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).  Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.

#### WebView2 

Erstellt eine neue Instanz eines WebView2-Steuerelements.

> Public [WebView2](#webview2)()

Beachten Sie, dass der CoreWebView2 des Steuerelements bis zur Initialisierung NULL ist. Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.

#### BuildWindowCore 

Dies wird von HwndHost überschrieben und aufgerufen, um uns zu beauftragen, unser HWND zu erstellen.

> protected override HandleRef [BuildWindowCore](#buildwindowcore)(HandleRef hwndParent)

##### Parameter
* `hwndParent` Das HWND, das wir als übergeordnetes Element des erstellten verwenden sollen.

##### Gibt
Das von uns erstellte HWND.

#### DestroyWindowCore 

Dies wird von HwndHost überschrieben und aufgerufen, um uns anzuweisen, unser HWND zu zerstören.

> protected override void [DestroyWindowCore](#destroywindowcore)(HandleRef HWND)

##### Parameter
* `hwnd` Unser HWND, das wir zerstören müssen.

#### Löschen 

Dies wird von unserer Basisklasse entsprechend der typischen Implementierung des IDispose-Musters aufgerufen.

> protected override void [Dispose](#dispose)(bool disposing)

Wir implementieren es durch die Freigabe aller zugrunde liegenden com-Ressourcen, einschließlich unserer CoreWebView2.

##### Parameter
* `disposing` True, wenn ein Aufrufer explizit Dispose aufruft, false, wenn wir finalisiert werden.

#### HasFocusWithinCore 

Dies wird von HwndHost überschrieben und aufgerufen, wenn WPF wissen muss, ob sich der Fokus in unserem Steuerelement/Fenster befindet.

> protected override bool [HasFocusWithinCore](#hasfocuswithincore)()

WPF kann nicht alleine wissen, da wir ein nicht-WPF-Fenster hosten, stattdessen fragt es uns, indem wir dies aufrufen. Zur Beantwortung wird der Zustand auf der Grundlage von CoreWebView2-Ereignissen, die ausgelöst werden, wenn er den Fokus erhält oder verliert, einfach nach vollführt.

##### Gibt
True, wenn sich der Fokus in unserem Control/Window befindet, andernfalls false.

#### OnKeyDown 

Dies wird von UIElement überschrieben und aufgerufen, damit wir die Eingabe von Tasten drücken verarbeiten können.

> protected override void [OnKeyDown](#onkeydown)(KeyEventArgs e)

WPF sollte diesen Anruf eigentlich nie als Antwort auf Tastaturereignisse aufrufen, da wir ein nicht-WPF-Fenster hosten. Wenn unser Fenster den Fokus hat, sendet Windows die Eingabe direkt an Sie, anstatt an das WPF-Fenster auf oberster Ebene und an das Eingabesystem. Diese Außerkraftsetzung sollte nur aufgerufen werden, wenn wir die Zugriffstasten Eingabe aus dem CoreWebView2 explizit an WPF (in CoreWebView2Controller_AcceleratorKeyPressed) weiterleiten. Selbst dann wird diese KeyDownEvent nur ausgelöst, weil Sie von unserer PreviewKeyDownEvent-Implementierung explizit ausgelöst wird, die dem normalen WPF-System entspricht. Der Prozess lautet also: CoreWebView2Controller_AcceleratorKeyPressed > Raise PreviewKeyDownEvent-> OnPreviewKeyDown-> Raise KeyDownEvent-> OnKeyDown

#### OnKeyUp 

Siehe OnKeyDown.

> protected override void [onkeyup](#onkeyup)(KeyEventArgs e)

#### OnPreviewKeyDown 

Dies ist die "Vorschau" (also

> protected override void [OnPreviewKeyDown](#onpreviewkeydown)(KeyEventArgs e)

Tunneling)-Version von OnKeyDown aus, sodass dies zunächst geschieht. Wie OnKeyDown wird dies immer nur aufgerufen, wenn wir die Schlüsselpressen explizit aus dem CoreWebView2 weiterleiten. Um die Standardeingabe Behandlung von WPF nachzuahmen, wenn wir dies erhalten, drehen wir den standardmäßigen sprudelnden KeyDownEvent um und zünden ihn an. Auf diese Weise sehen andere in der WPF-Struktur dasselbe Standardpaar von Eingabeereignissen, die von WPF selbst ausgelöst wurden, wenn Sie die Tastenkombination verarbeiten.

#### OnPreviewKeyUp 

Siehe OnPreviewKeyDown.

> protected override void [OnPreviewKeyUp](#onpreviewkeyup)(KeyEventArgs e)

#### OnWindowPositionChanged 

Dieser wird von HwndHost überschrieben und aufgerufen, wenn sich der Standort des Steuerelements geändert hat.

> protected override void [OnWindowPositionChanged](#onwindowpositionchanged)(Rect rcBoundingBox)

HwndHost sorgt für die Aktualisierung des von uns erstellten HWNDs. Wir müssen unsere CoreWebView2 so verschieben, dass Sie dem neuen Standort entspricht.

#### TabIntoCore 

Dies wird von HwndHost überschrieben und wird aufgerufen, um uns mitzuteilen, dass die Tab-Taste dazu geführt hat, dass der Fokus in unser Control/Window verschoben wurde.

> protected override bool [TabIntoCore](#tabintocore)(TraversalRequest Request)

Da WPF den Übergang des Fokus nicht in ein nicht-WPF-HWND verwalten kann, wird hier der Übergang an uns delegiert. Unsere Aufgabe ist es also, den Fokus auf unser externes HWND zu legen.

##### Parameter
* `request` Informationen dazu, wie der Fokus verschoben wird.

##### Gibt
"True", um anzugeben, dass die Navigation gehandhabt wurde, oder "false", um anzugeben, dass dies nicht der Fall ist.

