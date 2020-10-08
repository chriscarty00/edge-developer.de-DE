---
title: Neuerungen in EdgeHTML 18
description: Dieser Leitfaden enthält eine Übersicht über die Entwicklerfeatures und-Standards, die in Microsoft Edge enthalten sind.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/06/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, devtools
ms.custom: RS5
ms.openlocfilehash: b9285be7169f197a687e9f754a20cf67bbde160d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566773"
---
# Microsoft Edge-Entwicklerhandbuch

> [!TIP]
> Wir haben uns mit anderen Browsern und der Web-Community [zusammengetan,](https://blogs.windows.com/msedgedev/2017/10/18/documenting-web-together-mdn-web-docs/) um [MDN Web docs](https://developer.mozilla.org/) als den definitiven Ort für nützliche, unvoreingenommene, Browser unabhängige Dokumentationen für aktuelle und neu auf Standards basierende Webtechnologien zu übernehmen. Details zur EdgeHTML-API-Unterstützung finden Sie direkt auf jeder Seite der [MDN-Webverweis Bibliothek](https://developer.mozilla.org/docs/Web). Besuchen Sie den [Platt Form Status](https://developer.microsoft.com/microsoft-edge/platform/status/?q=edge%3AShipped%20edge%3APrefixed%20edge%3A'Preview%20Release) von Microsoft Edge für die neuesten Features, die in Microsoft Edge unterstützt werden. 


## Neuerungen in EdgeHTML 18

EdgeHTML 18 umfasst die folgenden neuen und aktualisierten Features, die in der aktuellen Version der Microsoft Edge-Plattform ausgeliefert wurden, ab dem [Windows 10 October 2018-Update](/windows/uwp/whats-new/windows-10-build-17763) (10/2018, Build 17763). Änderungen an bestimmten [Windows Insider](https://insider.windows.com/) Preview-Builds finden Sie im [Microsoft Edge-Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog/) und [Neuerungen in EdgeHTML](./dev-guide/whats-new.md).

Hier ist der Permalink für die folgende Liste der [https://aka.ms/devguide_edgehtml_18](https://aka.ms/devguide_edgehtml_18) Änderungen:

## Neue und aktualisierte Features

### AutoPlay-Richtlinien

Mit dem 2018-Update für Windows 10 Oktober bietet Microsoft Edge Kunden die Möglichkeit, Ihre Browsereinstellungen auf Websites zu personalisieren, die Medien mit Sound wiedergeben, um Ablenkungen im Internet zu minimieren und die Bandbreite zu sparen. Benutzer können das Medienverhalten mit den Steuerelementen für die automatische Wiedergabe auf globaler und pro Website anpassen. Darüber hinaus unterdrückt Microsoft Edge automatisch die automatische Wiedergabe von Medien in Hintergrundregisterkarten.

Informieren Sie sich im Leitfaden " [Richtlinien](./dev-guide/browser-features/autoplay-policies.md) für die automatische Wiedergabe" über Details und bewährte Methoden, um eine gute Benutzererfahrung mit auf Ihrer Website gehosteten Medien zu gewährleisten.

### Chakra-Verbesserungen

EdgeHTML 18 enthält Updates für das Chakra JavaScript-Modul zur Unterstützung neuer es-und WASM-Features sowie zur Verbesserung der Leistung und Interoperabilität. Weitere Informationen finden Sie in den Versionshinweisen zu [ChakraCore 1,11](https://github.com/Microsoft/ChakraCore/wiki/Roadmap#chakracore-111) .

### CSS-Updates

Wir haben weitere Fortschritte bei unserer experimentellen [CSS-Maskierungs](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking) Implementierung (hinter dem Flag " *CSS-Maskierung aktivieren* ") mit zusätzlicher Unterstützung für [Maske-Composite](https://developer.mozilla.org/docs/Web/CSS/mask-composite), [Mask-Position](https://developer.mozilla.org/docs/Web/CSS/mask-position)und [Mask-Repeat](https://developer.mozilla.org/docs/Web/CSS/mask-repeat)erzielt. Bei der Website Kompatibilität unterstützt Microsoft Edge auch die folgenden *WebKit* -Eigenschaften:-webkit-Mask,-WebKit-Mask-Composite,-WebKit-Mask-Image,-WebKit-Mask-Position,-WebKit-Maske-Position-x,-WebKit-Mask-Position-y,-WebKit-Maske-wiederholen,-WebKit-Mask-Size.

Darüber hinaus bietet Microsoft Edge jetzt Unterstützung für [Überlauf-Wrap](https://developer.mozilla.org/docs/Web/CSS/overflow-wrap
) und partielle Unterstützung für [overscroll-Verhalten](https://developer.mozilla.org/docs/Web/CSS/overscroll-behavior) ( `auto` und `contain` Werte).


### Entwicklungstools

Das neueste Update für Microsoft Edge devtools bietet eine Reihe von Vorteilen sowohl für die Benutzeroberfläche als auch unter der Haube, einschließlich neuer dedizierter Panels für Dienstmitarbeiter und Speicher, Quelldatei-Such Tools im Debugger und neuen Edge-devtools-Protokoll Domänen für das Debuggen von Stilen und Layouts sowie für Konsolen-APIs.

[Devtools im neuesten Windows 10-Update (EdgeHTML 18)](./devtools-guide/whats-new.md) enthält alle Details.

### Abhören Ihres Feedbacks

Wir hören Ihr Feedback an und haben Unterstützung für mehrere angeforderte APIs in EdgeHTML 18 implementiert, einschließlich der [`DataTransfer.setDragImage()`](https://developer.mozilla.org/docs/Web/API/DataTransfer/setDragImage) Methode, mit der ein benutzerdefiniertes Bild beim Ziehen und ablegen festgesetzt wird, und [`secureConnectionStart`](https://developer.mozilla.org/docs/Web/API/PerformanceResourceTiming/secureConnectionStart) eine Eigenschaft der Leistungsressourcen-Timing-API, die verwendet werden kann, um einen Zeitstempel zurückzugeben, unmittelbar bevor der Browser den Handshake-Prozess zum Sichern der aktuellen Verbindung startet. 

Darüber hinaus möchte niemand die Attributes-Sammlung aufzählen, daher haben wir die Unterstützung für das [`Element.getAttributeNames`](https://developer.mozilla.org/docs/Web/API/Element/getAttributeNames) zurückgeben der Attributnamen des Elements als Array von Zeichenfolgen sowie [`Element.toggleAttribute`](https://developer.mozilla.org/docs/Web/API/Element/toggleAttribute) zum Umschalten eines booleschen Attributs (entfernen, falls vorhanden und hinzufügen wenn nicht) hinzugefügt.

### Progressive Web Apps

#### Hintergrundskript für Lebensdauer

Windows 10-JavaScript-Apps (Web-Apps, die in einem *WWAHost.exe* -Prozess ausgeführt werden) unterstützen jetzt ein optionales Hintergrundskript für jede Anwendung, das beginnt, bevor alle Ansichten aktiviert werden und für die Dauer des Prozesses ausgeführt werden. Damit können Sie die Navigation überwachen und ändern, den Zustand für die Navigation nachverfolgen, Navigationsfehler überwachen und Code ausführen, bevor Ansichten aktiviert werden. 

Wenn [`StartPage`](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) Sie in Ihrem APP- [Manifest](/uwp/schemas/appxpackage/appx-package-manifest)angegeben sind, werden alle Ansichten (Windows) der APP für das Skript als Instanzen der neuen Klasse verfügbar gemacht [`WebUIView`](/uwp/api/windows.ui.webui.webuiview) , wobei dieselben Ereignisse, Eigenschaften und Methoden wie eine allgemeine (Win32) [WebView](/uwp/api/windows.web.ui.iwebviewcontrol)bereitgestellt werden. Ihr Skript kann das Ereignis überwachen [`NewWebUIViewCreated`](/uwp/api/windows.ui.webui.newwebuiviewcreatedeventargs) , um die Steuerung der Navigation für eine neue Ansicht abzufangen:

```JavaScript
Windows.UI.WebUI.WebUIApplication.addEventListener("newwebuiviewcreated", newWebUIViewCreatedEventHandler);
```

 Jede APP-Aktivierung mit dem Hintergrundskript wie der `StartPage` wird sich auf das Skript selbst für die Navigation verlassen.

#### Textskalierung

Das Windows 10 October 2018-Update führt die Einstellung " [*Text vergrößern*](https://review.docs.microsoft.com/windows/uwp/design/input/text-scaling?branch=master#user-experience) " für eine verbesserte Barrierefreiheit des Endbenutzers ein, und PWAs, das unter Windows installiert ist (zusätzlich UWP und die meisten Desktop-Apps), unterstützen dieses Feature nun automatisch. Bei PWAs-und WebView-Steuerelementen funktioniert die Textskalierung wie bei der DPI-Skalierung. Wenn ein Benutzer sowohl die Textskalierung als auch die DPI-Skalierung ändert, ist das Ergebnis das Produkt der beiden.

 Informationen zur Entwurfs Anleitung finden Sie im Leitfaden zur [Text Skalierung](/windows/uwp/design/input/text-scaling) UWP unter *Windows dev Center*.

### Updates für Dienstmitarbeiter 

Eine Auffrischung darüber, was Servicemitarbeiter sind und wie Sie funktionieren, finden Sie in der Zusammenfassung der [Service Worker-API]( https://developer.mozilla.org/docs/Web/API/Service_Worker_API) , die von unseren Partnern in MDN verfasst wurde.  Es gab mehrere Updates für Microsoft Edge, das Service Mitarbeiter in EdgeHTML 18 unterstützt. Das `fetchEvent` ermöglicht es dem Dienstmitarbeiter, [`preloadResponse`]( https://developer.mozilla.org/docs/Web/API/FetchEvent) eine Antwort zu versprechen, und die, [`resultingClientId`]( https://developer.mozilla.org/docs/Web/API/FetchEvent/clientId) um die ID des Clients zurückzugeben, der vom aktuellen Dienstmitarbeiter gesteuert wird.  
Die [`NavigationPreloadManager`]( https://developer.mozilla.org/docs/Web/API/NavigationPreloadManager) Schnittstelle bietet Methoden zum Verwalten des Vorladens von Ressourcen, sodass Sie eine Anforderung parallel durchführen können, während ein Dienstmitarbeiter bootet, wodurch keine Zeitverzögerung erfolgt. Schauen Sie sich die [neu unterstützten API-Eigenschaften](#new-apis-in-edgehtml-18) für die Liste der Methoden und Eigenschaften von Service Worker preload an. 

### Webauthentifizierung

Microsoft Edge enthält jetzt [eine Unterstützung für die neue Webauthentifizierungs-API](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge/) (aka [webauthn](https://w3c.github.io/webauthn/)). Die Webauthentifizierung bietet eine offene, skalierbare und interoperable Lösung zur Vereinfachung der Authentifizierung, wodurch bessere und sicherere Benutzer Erfahrungen durch Ersetzen von Kennwörtern durch stärkere Hardware gebundene Anmeldeinformationen ermöglicht werden. Die Implementierung in Microsoft Edge ermöglicht die Verwendung von [Windows Hello](https://www.microsoft.com/windows/windows-hello) , mit der Benutzer sich mit Ihrem Face-, Fingerabdruck-oder PIN-Konto anmelden können, zusätzlich zu [externen Authentifikatoren](https://fidoalliance.org) wie FIDO2-Sicherheitsschlüsseln oder Fido U2F-Sicherheitsschlüsseln, um sich auf Websites sicher zu authentifizieren.

Weitere Informationen finden Sie im Blogbeitrag [Introducing Web Authentication in Microsoft Edge](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge).

### WebDriver

WebDriver ist jetzt ein [Windows-Feature on Demand](https://docs.microsoft.com/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (FOD), wodurch es einfacher als je zuvor ist, Tests in Microsoft Edge zu automatisieren und die richtige Version für Ihr Gerät zu erhalten. Wenn Sie WebDriver installieren, müssen Sie den Build/Branch/Flavor nicht mehr manuell anpassen, da Ihr [WebDriver](https://www.w3.org/TR/webdriver) automatisch auf alle neuen Windows 10-Updates aktualisiert wird. 

Sie können WebDriver installieren, indem Sie den Entwicklermodus aktivieren oder als eigenständiges Programm installieren, indem Sie zu Einstellungen > apps > apps & Features > optionale Features verwalten wechseln. Weitere Informationen finden Sie [in der Ankündigung von WebDriver auf der Windows-Blog Website](https://blogs.windows.com/msedgedev/2018/06/14/webdriver-w3c-recommendation-feature-on-demand).

### Web-Benachrichtigungseigenschaften
Vier neue Eigenschaften werden jetzt für webbenachrichtigungen unterstützt:,, [`actions`](https://developer.mozilla.org/docs/Web/API/notification/actions) [`badge`](https://developer.mozilla.org/docs/Web/API/notification/badge) [`image`](https://developer.mozilla.org/docs/Web/API/notification/image) und  `maxActions` verbessern die Möglichkeit zum Erstellen von Benachrichtigungen im Web, die mit vorhandenen Benachrichtigungs Systemen kompatibel sind, während die Plattform unabhängig bleibt.

### WebView

#### Dienstmitarbeiter
[Dienstmitarbeiter](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) werden nun zusätzlich zum Microsoft Edge-Browser und zu Windows 10 JavaScript-apps im WebView-Steuerelement unterstützt. Alle Flavors von Microsoft Edge WebView ([PWA](/microsoft-edge/hosting/webview), [UWP](/uwp/api/Windows.UI.Xaml.Controls.WebView), [Win32](/windows/communitytoolkit/controls/wpf-winforms/webview)) unterstützen Dienstmitarbeiter, doch beachten Sie bitte, dass die [Push-API](https://developer.mozilla.org/docs/Web/API/Push_API) für die UWP-und Win32-Versionen noch nicht verfügbar ist.

x64-App-Architekturen erfordern *neutrale* (Any CPU)-oder *x64* -Pakete, da Dienstmitarbeiter in WOW64-Prozessen nicht unterstützt werden. (Um Speicherplatz zu sparen, ist die WoW-Version der erforderlichen DLLs nicht nativ in Windows enthalten.)

#### Win32-WebView-Updates

Die EdgeHTML [webviewcontrol](/windows/communitytoolkit/controls/wpf-winforms/webview) für Windows Desktop-Apps (Win32) wurde mit verschiedenen neuen Features aktualisiert, einschließlich der Möglichkeit, Skripts beim Laden der Seite einzufügen, bevor andere Skripts auf der Seite ausgeführt werden ( [`AddInitializeScript`](/uwp/api/windows.web.ui.interop.webviewcontrol.addinitializescript) ) und wissen, wann ein bestimmtes webviewcontrol den Fokus erhält oder verliert ( [`GotFocus`](/uwp/api/windows.web.ui.interop.webviewcontrol.gotfocus) / [`LostFocus`](/uwp/api/windows.web.ui.interop.webviewcontrol.lostfocus) ).

Darüber hinaus können Sie jetzt ein neues webviewcontrol-Fenster als geöffnetes Fenster erstellen [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) . Das [`NewWindowRequested`](/uwp/api/windows.web.ui.iwebviewcontrol.newwindowrequested) Ereignis benachrichtigt weiterhin eine APP, wenn das Skript innerhalb des webviewcontrol-Anruffensters geöffnet wird, wie es immer der Fall ist, aber mit EdgeHTML 18 bietet es [`NewWindowRequestedEventArgs`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs) die Möglichkeit, eine Verzögerung () zu verwenden, um [`GetDeferral`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.getdeferral) ein neues webviewcontrol ( [`NewWindow`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.newwindow) ) als Ziel für das Fenster festzulegen. Öffnen Sie:

```C#
WebViewControlProcess wvProc;
WebViewControl webView;

void OnWebViewControlNewWindowRequested(WebViewControl sender, WebViewControlNewWindowRequestedEventArgs args)
{

    if (args.Uri.Domain == "mydomain.com")
    {
        using deferral = args.GetDeferral();
        args.NewWindow = await wvProc.CreateWebViewControlAsync(
            parentWindow, targetWebViewBounds);
        deferral.Complete();
    }
    else
    {
        // Prevent WebView from launching in the default browser.
        args.Handled = true;
    }
}

String htmlContent = "<html><script>window.open('http://mydomain.com')</script><body></body></html>";

webView.NavigateToString(htmlContent);

```

Schließlich bemerken die Hauptbenutzer möglicherweise die apppearance des *Desktop-App-WebViewers* (vormals *Win32WebViewHost*), einer internen System-App, die die Win32-WebView darstellt, an den folgenden Stellen:
- Im *Windows 10-Wartungs Center*. Die Quelle dieser Benachrichtigungen sollte von einer WebView verstanden werden, die von einer Win32-App gehostet wird.
- In der Benutzeroberfläche für gerätezugriffseinstellungen (*Einstellungen – >Datenschutz – >Kamera/Standort/Mikrofon*). Wenn Sie diese Einstellungen deaktivieren, wird der Zugriff von allen Webansichten verweigert, die in Win32-apps gehostet werden.

![Einstellung für den Zugriff auf den Desktop-App-webviewer](./dev-guide/media/desktop-app-web-viewer.png)


## Veraltete Funktionen

### XSS-Filter jetzt eingestellt

Mit EdgeHTML 18 werden wir den XSS-Filter in Microsoft Edge zurückziehen. Unsere Kunden bleiben durch moderne Standards wie [Content Security Policy (CSP)](https://developer.mozilla.org/docs/Web/HTTP/CSP)geschützt, die leistungsstärkere, leistungsfähigere und sichere Mechanismen zum Schutz vor Content-Injection-Attacken mit einer hohen Kompatibilität in modernen Browsern bieten.

## Neue APIs in EdgeHTML 18

Schauen Sie sich die vollständige Liste der neuen APIs in EdgeHTML 18 an. Sie werden im Format [Schnittstellenname] aufgeführt. [API-Name].

> [!NOTE] 
> Obwohl die folgenden APIs im DOM verfügbar gemacht werden, kann sich das End-to-End-Verhalten einiger nach wie vor in der Entwicklung befinden und hinter einer experimentellen Kennzeichnung verborgen sein. Informationen zum offiziellen Word-Feature-Support finden Sie im  [Microsoft Edge-Platt Form Status](https://developer.microsoft.com/microsoft-edge/platform/status/) .

<iframe height='580' scrolling='no' title='Neue APIs in EdgeHTML 18' src='//codepen.io/MSEdgeDev/embed/5d7be9404d82575162b486e79d0dd58f
/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Weitere Informationen finden Sie in den neuen APIs für Stifte <a href='https://codepen.io/MSEdgeDev/pen/5d7be9404d82575162b486e79d0dd58f'> in EdgeHTML 18 </a> von MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) auf <a href='https://codepen.io'> CodePen </a> .</iframe>

## Vorherige EdgeHTML-Versionen

[EdgeHTML 13/Windows Build 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)

[EdgeHTML 14/Windows Build 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)

[EdgeHTML 15/Windows Build 15063 (4/2017)](https://aka.ms/devguide_edgehtml_15)

[EdgeHTML 16/Windows Build 16299 (10/2017)](https://aka.ms/devguide_edgehtml_16)

[EdgeHTML 17/Windows Build 17134 (04/2018)](https://aka.ms/devguide_edgehtml_17)
