---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2Controller
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Controller
ms.openlocfilehash: 1162061dc3555968c5732372b083951b22998145
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012098"
---
# Microsoft. Web. WebView2. Core. CoreWebView2Controller Klasse 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Diese Klasse ist der Besitzer des CoreWebView2-Objekts und bietet Unterstützung für die Größenänderung, das ein-und ausblenden, die Fokussierung und andere Funktionen im Zusammenhang mit Fenster und Komposition.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[AcceleratorKeyPressed](#acceleratorkeypressed) | AcceleratorKeyPressed wird ausgelöst, wenn eine Zugriffstasten-oder Tastenkombination gedrückt oder freigegeben wird, während die WebView fokussiert ist.
[Grenzen](#bounds) | Die WebView-Begrenzungen.
[CoreWebView2](#corewebview2) | Ruft das CoreWebView2 ab, das diesem CoreWebView2Controller zugeordnet ist.
[GotFocus](#gotfocus) | GotFocus wird ausgelöst, wenn WebView den Fokus erhält.
[IsVisible](#isvisible) | Die IsVisible-Eigenschaft bestimmt, ob die WebView angezeigt oder ausgeblendet werden soll.
[LostFocus](#lostfocus) | LostFocus wird ausgelöst, wenn WebView den Fokus verloren hat.
[MoveFocusRequested](#movefocusrequested) | MoveFocusRequested wird ausgelöst, wenn der Benutzer versucht, die Tab-Taste aus der WebView zu ziehen.
[ParentWindow](#parentwindow) | Das übergeordnete Fenster, das von der APP bereitgestellt wird, die von dieser WebView zum Rendern von Inhalten verwendet wird.
[ZoomFactor](#zoomfactor) | Der Zoomfaktor für die WebView.
[ZoomFactorChanged](#zoomfactorchanged) | ZoomFactorChanged wird ausgelöst, wenn die ZoomFactor-Eigenschaft der WebView geändert wird.
[Schließen](#close) | Schließt die WebView und bereinigt die zugrunde liegende Browserinstanz.
[MoveFocus](#movefocus) | Verschieben des Fokus in WebView
[NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged) | Hierbei handelt es sich um eine Benachrichtigung, die sich von den Grenzen unterscheidet, die WebView das übergeordnete HWND (oder ein Vorgänger) verschoben hat.
[SetBoundsAndZoomFactor](#setboundsandzoomfactor) | Gleichzeitiges Aktualisieren von Begrenzungen und ZoomFactor-Eigenschaften

Die CoreWebView2Controller besitzt den CoreWebView2, und wenn alle Verweise auf die CoreWebView2Controller verschwindet, wird die WebView geschlossen.

## Member

#### AcceleratorKeyPressed 

AcceleratorKeyPressed wird ausgelöst, wenn eine Zugriffstasten-oder Tastenkombination gedrückt oder freigegeben wird, während die WebView fokussiert ist.

> public event EventHandler< [CoreWebView2AcceleratorKeyPressedEventArgs](microsoft-web-webview2-core-corewebview2acceleratorkeypressedeventargs.md)  >  [AcceleratorKeyPressed](#acceleratorkeypressed)

AcceleratorKeyPressed wird ausgelöst, wenn eine Zugriffstasten-oder Tastenkombination gedrückt oder freigegeben wird, während die WebView fokussiert ist. Ein Schlüssel wird in folgenden Fällen als Beschleuniger betrachtet:

1. STRG oder alt wird derzeit gehalten, oder

1. die Taste gedrückt wird einem Zeichen nicht zugeordnet. Einige bestimmte Tasten gelten nie als Beschleuniger, wie etwa die UMSCHALTTASTE. Die Escape-Taste wird immer als Beschleuniger angesehen.

Durch automatisch wiederholte Tastenereignisse, die durch das Drücken der Taste nach unten verursacht werden, wird dieses Ereignis ebenfalls ausgelöst. Sie können diese filtern, indem Sie das Ereignis args ' KeyEventLParam oder PhysicalKeyStatus.

Im Fenstermodus wird dieser Ereignishandler synchron aufgerufen. Bis Sie Handled () für die Ereignis-args aufgerufen haben oder der Ereignishandler zurückgegeben wird, wird der Browserprozess blockiert, und ausgehende prozessübergreifende com-Aufrufe schlagen mit RPC_E_CANTCALLOUT_ININPUTSYNCCALL fehl. Allerdings funktionieren alle CoreWebView2-API-Methoden.

Im Fenstermodus wird der Ereignishandler asynchron aufgerufen. Eine weitere Eingabe erreicht den Browser erst, wenn der Ereignishandler zurückgegeben oder Handled () aufgerufen wird, aber der Browserprozess selbst wird nicht blockiert, und ausgehende com-Aufrufe funktionieren normal.

Es wird empfohlen, Handled (true) so früh wie möglich anzurufen, wenn Sie wissen, dass Sie die Zugriffstaste behandeln möchten.

#### Grenzen 

Die WebView-Begrenzungen.

> [Begrenzungen](#bounds) für öffentliches Rechteck

Begrenzungen sind relativ zum übergeordneten HWND. Die APP hat zwei Möglichkeiten, um eine WebView-Position zu positionieren:

1. Erstellen Sie ein untergeordnetes HWND, das das übergeordnete HWND von WebView ist. Positionieren Sie dieses Fenster, in dem sich die WebView befinden soll. Verwenden Sie in diesem Fall (0, 0) für die Bound's obere linke Ecke des Webviews (den Offset).

1. Verwenden Sie das oberste Fenster der App als übergeordnetes WebView-HWND. Stellen Sie die Bound's-obere linke Ecke der WebView so ein, dass die WebView in der APP richtig positioniert ist. Die Werte der Bounds befinden sich im Koordinatenbereich des Hosts.

#### CoreWebView2 

Ruft das CoreWebView2 ab, das diesem CoreWebView2Controller zugeordnet ist.

> öffentliche [CoreWebView2](microsoft-web-webview2-core-corewebview2.md) - [CoreWebView2](#corewebview2)

#### GotFocus 

GotFocus wird ausgelöst, wenn WebView den Fokus erhält.

> public event EventHandler<-Objekt > [GotFocus](#gotfocus)

#### IsVisible 

Die IsVisible-Eigenschaft bestimmt, ob die WebView angezeigt oder ausgeblendet werden soll.

> public bool [IsVisible](#isvisible)

Wenn IsVisible auf "false" festgelegt ist, ist die WebView transparent und wird nicht gerendert. Dies wirkt sich jedoch nicht auf das Fenster aus, das die WebView enthält (den HWND-Parameter, der an CreateCoreWebView2Controller übergeben wurde). Wenn Sie möchten, dass das Fenster ebenfalls ausgeblendet wird, rufen Sie ShowWindow direkt zusätzlich zum Ändern der IsVisible-Eigenschaft auf. WebView als untergeordnetes Fenster ruft keine Fenster Meldungen ab, wenn das oberste Fenster minimiert oder wiederhergestellt wird. Aus Leistungsgründen sollte Entwickler die IsVisible-Eigenschaft der WebView-Eigenschaft auf "false" festlegen, wenn das App-Fenster minimiert wird, und zurück zu "true", wenn das App-Fenster wiederhergestellt wird. Das App-Fenster kann dies tun, indem SC_MINIMIZE und SC_RESTORE Befehl beim empfangen WM_SYSCOMMAND Nachricht behandelt werden.

#### LostFocus 

LostFocus wird ausgelöst, wenn WebView den Fokus verloren hat.

> public event EventHandler< Objekt > [LostFocus](#lostfocus)

In dem Fall, in dem das MoveFocusRequested-Ereignis ausgelöst wird, liegt der Fokus weiterhin auf WebView, wenn das MoveFocusRequested-Ereignis ausgelöst wird. LostFocus wird erst anschließend ausgelöst, wenn der app-Code oder die Standardaktion des MoveFocusRequested-Ereignisses den Fokus von WebView absetzen.

#### MoveFocusRequested 

MoveFocusRequested wird ausgelöst, wenn der Benutzer versucht, die Tab-Taste aus der WebView zu ziehen.

> public event EventHandler< [CoreWebView2MoveFocusRequestedEventArgs](microsoft-web-webview2-core-corewebview2movefocusrequestedeventargs.md)  >  [MoveFocusRequested](#movefocusrequested)

Der Fokus der WebView wurde nicht geändert, wenn dieses Ereignis ausgelöst wird.

#### ParentWindow 

Das übergeordnete Fenster, das von der APP bereitgestellt wird, die von dieser WebView zum Rendern von Inhalten verwendet wird.

> öffentliche IntPtr- [ParentWindow](#parentwindow)

Das Festlegen der Eigenschaft bewirkt, dass die WebView das Fenster des neu bereitgestellten Fensters erneut übermittelt.

#### ZoomFactor 

Der Zoomfaktor für die WebView.

> öffentliches Doppel [ZoomFactor](#zoomfactor)

Beachten Sie, dass das Ändern des Zoomfaktors `window.innerWidth/innerHeight` zu einer Änderung des Seitenlayouts führen kann. Ein Zoomfaktor, der vom Host durch Aufrufen von ZoomFactor angewendet wird, wird zum neuen Standardzoom für die WebView. Dieser Zoomfaktor gilt für alle Navigationselemente und der Zoomfaktor WebView wird zurückgegeben, wenn der Benutzer STRG + 0 drückt. Wenn der Zoomfaktor vom Benutzer geändert wird (was im App-Empfang ZoomFactorChanged), gilt dieser Zoom nur für die aktuelle Seite. Der Zoom eines Benutzers, der angewendet wird, ist nur für die aktuelle Seite vorgesehen und wird in einer Navigation zurückgesetzt. Die Angabe einer ZoomFactor kleiner oder gleich 0 ist nicht zulässig. WebView verfügt auch über einen internen unterstützten Zoomfaktor Bereich. Wenn sich ein angegebener Zoomfaktor außerhalb dieses Bereichs befindet, wird er normalisiert, sodass er innerhalb des Bereichs liegt, und ein ZoomFactorChanged-Ereignis wird für den tatsächlich angewendeten Zoomfaktor ausgelöst. Wenn diese Bereichs Normalisierung erfolgt, meldet die ZoomFactor-Eigenschaft den Zoomfaktor, der während der vorherigen Änderung der ZoomFactor-Eigenschaft angegeben wird, bis das ZoomFactorChanged-Ereignis empfangen wird, nachdem WebView den normalisierten Zoomfaktor angewendet hat.

#### ZoomFactorChanged 

ZoomFactorChanged wird ausgelöst, wenn die ZoomFactor-Eigenschaft der WebView geändert wird.

> public event EventHandler<-Objekt > [ZoomFactorChanged](#zoomfactorchanged)

Das Ereignis konnte ausgelöst werden, weil der Aufrufer die ZoomFactor-Eigenschaft geändert hat, oder weil der Benutzer den Zoom manuell geändert hat. Wenn Sie vom Aufrufer über die ZoomFactor-Eigenschaft geändert wird, wird der interne Zoomfaktor sofort aktualisiert, und es gibt kein ZoomFactorChanged-Ereignis. WebView ordnet den zuletzt verwendeten Zoomfaktor für jede Website zu. Daher ist es möglich, dass sich der Zoomfaktor ändert, wenn Sie zu einer anderen Seite navigieren. Wenn sich der Zoomfaktor aufgrund dieser Änderung ändert, wird das ZoomFactorChanged-Ereignis direkt hinter dem ContentLoading-Ereignis ausgelöst.

#### Schließen 

Schließt die WebView und bereinigt die zugrunde liegende Browserinstanz.

> publicvoid [Close](#close)()

Beim Bereinigen der Browserinstanz werden die Ressourcen freigegeben, die die WebView-Ansicht auslösen. Die Browserinstanz wird heruntergefahren, wenn keine anderen Webansichten verwendet werden.

Nach dem Aufruf von Close werden alle Methodenaufrufe fehlschlagen, und die Ereignishandler werden nicht mehr ausgelöst. Insbesondere gibt die WebView Ihre Verweise auf die Ereignishandler frei, wenn Close aufgerufen wird.

Close wird implizit aufgerufen, wenn die CoreWebView2Controller den endgültigen Bezug verliert und zerstört wird. Es empfiehlt sich jedoch, explizit Close aufzurufen, um einen zufälligen Zyklus von Verweisen zwischen WebView und app-Code zu vermeiden. Insbesondere wenn Sie einen Verweis auf die WebView in einem Ereignishandler aufzeichnen, erstellen Sie einen Referenz Zyklus zwischen WebView und dem Ereignishandler. Durch das Aufrufen von Close wird dieser Zyklus unterbrochen, indem alle Ereignishandler freigegeben werden. Um dies zu vermeiden, empfiehlt es sich, sowohl explizit Close für die WebView zu verwenden als auch einen Verweis auf die WebView zu erfassen, um sicherzustellen, dass die WebView ordnungsgemäß bereinigt werden kann.

#### MoveFocus 

Verschieben des Fokus in WebView

> publicvoid [MoveFocus](#movefocus)([CoreWebView2MoveFocusReason](./namespace-microsoft-web-webview2-core.md) Reason)

WebView erhält den Fokus, und der Fokus wird auf das korrespondierende Element auf der Seite gesetzt, die in der WebView gehostet wird. Aus Programm Gründen wird der Fokus auf das zuvor fokussierte Element oder auf das Standardelement gesetzt, wenn kein zuvor fokussiertes Element vorhanden ist. Aus dem nächsten Grund wird der Fokus auf das erste Element gesetzt. Aus vorherigen Gründen wird der Fokus auf das letzte Element gesetzt. WebView kann auch den Fokus über die Benutzerinteraktion erhalten, wie das Klicken in WebView oder die Tab-Taste. Für die Tab-Taste kann die APP MoveFocus mit der nächsten oder vorherigen aufrufen, um mit Tab und UMSCHALT + TAB auszurichten, wenn Sie beschließt, dass die WebView das nächste Tabbed-Element ist. Oder die APP kann IsDialogMessage als Teil der Nachrichtenschleife aufrufen, damit die Plattform die Tab-Funktion automatisch verarbeiten kann. Die Plattform wird durch alle Fenster mit WS_TABSTOP gedreht. Wenn die WebView den Fokus von IsDialogMessage erhält, wird der Fokus intern auf das erste oder letzte Element für Tab und UMSCHALT + TAB gesetzt.

#### NotifyParentWindowPositionChanged 

Hierbei handelt es sich um eine Benachrichtigung, die sich von den Grenzen unterscheidet, die WebView das übergeordnete HWND (oder ein Vorgänger) verschoben hat.

> publicvoid [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()

Dies ist für die Barrierefreiheit und bestimmte Dialogfelder in WebView erforderlich, um ordnungsgemäß zu funktionieren.

#### SetBoundsAndZoomFactor 

Gleichzeitiges Aktualisieren von Begrenzungen und ZoomFactor-Eigenschaften

> publicvoid [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(Rectangle-Begrenzungen, Doppel ZoomFactor)

Dieser Vorgang ist aus der Perspektive des Hosts atomar. Nach der Rückgabe von dieser Funktion werden die Bounds-Eigenschaft und die ZoomFactor-Eigenschaft beide aktualisiert, wenn die Funktion erfolgreich ist, oder keine wird aktualisiert, wenn die Funktion fehlschlägt. Wenn Grenz-und ZoomFactor sowohl auf der gleichen Skala aktualisiert werden (d. h., dass die Begrenzungen und ZoomFactor beide verdoppelt werden), wird der Seite keine Änderung in Window. InnereBreite/InnereHoehe angezeigt, und die WebView rendert den Inhalt mit der neuen Größe und zoomt ohne zwischen Renderings. Diese Funktion kann auch verwendet werden, um nur eine von ZoomFactor oder Begrenzungen zu aktualisieren, indem der neue Wert für einen und der aktuelle Wert für den anderen übergeben wird.

