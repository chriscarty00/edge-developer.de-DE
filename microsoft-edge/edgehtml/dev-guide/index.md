---
description: Dieses Handbuch bietet eine Übersicht über die Entwicklerfeatures und -standards, die in Microsoft Edge enthalten sind.
title: Neues in EdgeHTML 18
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: edge, web development, html, css, javascript, developer, devtools
ms.custom: RS5
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6b53163115ad7db8e5b792cadda0c59b93b6711b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399225"
---
# <a name="microsoft-edge-developer-guide"></a>Microsoft Edge Developer Guide  

> [!TIP]
> Wir haben [](https://blogs.windows.com/msedgedev/2017/10/18/documenting-web-together-mdn-web-docs/) eine Partnerschaft mit anderen Browsern und der Web-Community hergestellt, um MDN Web [Docs](https://developer.mozilla.org/) als endgültigen Ort für nützliche, unvoreingenommene, browseragnostische Dokumentation für aktuelle und neue standardsbasierte Webtechnologien zu übernehmen.  Details zur EdgeHTML-API-Unterstützung finden Sie direkt auf jeder Seite der [MDN-Webreferenzbibliothek.](https://developer.mozilla.org/docs/Web)  Besuchen Sie den Plattformstatus von Microsoft [Edge,](https://developer.microsoft.com/microsoft-edge/platform/status/?q=edge%3AShipped%20edge%3APrefixed%20edge%3A'Preview%20Release) um die neuesten in Microsoft Edge unterstützten Features zu erhalten.  

## <a name="whats-new-in-edgehtml-18"></a>Neues in EdgeHTML 18  

EdgeHTML 18 enthält die folgenden neuen und aktualisierten Features, die in der aktuellen Version der Microsoft Edge-Plattform ab dem [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) \(10/2018, Build 17763\) enthalten sind.  Änderungen an bestimmten [Windows Insider](https://insider.windows.com) Preview-Builds finden Sie unter Microsoft [Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) und [What's New in EdgeHTML](./whats-new.md).  

Hier sehen Sie den Permalink für die folgende Liste der Änderungen: [https://docs.microsoft.com/microsoft-edge/dev-guide](#new-apis-in-edgehtml-18) .  

## <a name="new-and-updated-features"></a>Neue und aktualisierte Features  

### <a name="autoplay-policies"></a>AutoPlay-Richtlinien  

Mit dem Windows 10 October 2018 Update bietet Microsoft Edge Kunden die Möglichkeit, ihre Browsereinstellungen auf Websites zu personalisieren, die Medien automatisch mit Sound spielen, um Ablenkungen im Web zu minimieren und Bandbreite zu sparen.  Benutzer können das Medienverhalten sowohl mit globalen als auch mit automatischen Wiedergabesteuerelementen pro Standort anpassen.  Darüber hinaus unterdrückt Microsoft Edge automatisch die automatische Wiedergabe von Medien in Hintergrundregisterkarten.  

Weitere Informationen und [bewährte Methoden finden](./browser-features/autoplay-policies.md) Sie im Leitfaden für automatische Wiedergaberichtlinien, um eine gute Benutzererfahrung mit auf Ihrer Website gehosteten Medien zu gewährleisten.  

### <a name="chakra-improvements"></a>Verbesserungen bei den Chakrays  

EdgeHTML 18 enthält Updates für das JavaScript-Modul von Javascript zur Unterstützung neuer ES- und WASM-Features sowie Leistungs- und Interoperabilitätsverbesserungen.  Weitere Informationen finden Sie in den Versionshinweisen zu ["1.11" von "1.11".](https://github.com/Microsoft/ChakraCore/wiki/Roadmap#chakracore-111)  

### <a name="css-updates"></a>CSS-Updates  

Wir haben weitere Fortschritte bei unserer experimentellen [CSS Masking-Implementierung](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking) \(hinter dem *Kennzeichen CSS-Maskierung* aktivieren\) mit der zusätzlichen Unterstützung für [mask-composite,](https://developer.mozilla.org/docs/Web/CSS/mask-composite) [mask-position](https://developer.mozilla.org/docs/Web/CSS/mask-position)und [mask-repeat gemacht.](https://developer.mozilla.org/docs/Web/CSS/mask-repeat)  Zur Websitekompatibilität unterstützt Microsoft Edge auch die folgenden *-webkit-Eigenschaften:* -webkit-mask, -webkit-mask-composite, -webkit-mask-image, -webkit-mask-position, -webkit-mask-position-x, -webkit-mask-position-y, -webkit-mask-repeat, -webkit-mask-size.  

Darüber hinaus bietet Microsoft Edge jetzt Unterstützung für [Überlaufumbruch](https://developer.mozilla.org/docs/Web/CSS/overflow-wrap) und teilweise Unterstützung für das [Overscrollverhalten](https://developer.mozilla.org/docs/Web/CSS/overscroll-behavior) \( `auto` und `contain` Werte\).  

### <a name="developer-tools"></a>Entwicklungstools  

Das neueste Update für Microsoft Edge DevTools bietet sowohl auf der Benutzeroberfläche als auch unter der Blende eine Reihe von Komfort, einschließlich neuer dedizierter Panels für Service Workers und Speicher, Quelldateisuchtools im Debugger und neue Edge DevTools-Protokolldomänen für Stil-/Layoutdebugger und Konsolen-APIs.  

[DevTools im neuesten Windows 10-Update (EdgeHTML 18)](./whats-new.md) hat alle Details.  

### <a name="listening-to-your-feedback"></a>Abhören Ihres Feedbacks  

Wir lauschen Ihrem Feedback und haben unterstützung für mehrere angeforderte APIs in EdgeHTML 18 implementiert, einschließlich der [DataTransfer.setDragImage()-Methode,](https://developer.mozilla.org/docs/Web/API/DataTransfer/setDragImage) die zum Festlegen eines benutzerdefinierten Bilds beim Ziehen und Ablegen verwendet wird, und [secureConnectionStart](https://developer.mozilla.org/docs/Web/API/PerformanceResourceTiming/secureConnectionStart), eine Eigenschaft der Performance Resource Timing-API, die zum Zurückgeben eines Zeitstempels unmittelbar vor dem Starten des Handshakeprozesses zum Sichern der aktuellen Verbindung verwendet werden kann.  

Darüber hinaus mag niemand das Aufzählen der Attributes-Auflistung, daher haben wir Unterstützung für [Element.getAttributeNames](https://developer.mozilla.org/docs/Web/API/Element/getAttributeNames) hinzugefügt, um die Attributnamen des Elements als Array von Zeichenfolgen zurückzukehren, sowie [Element.toggleAttribute,](https://developer.mozilla.org/docs/Web/API/Element/toggleAttribute) um ein boolesches Attribut \(Entfernen, wenn vorhanden, und Hinzufügen, wenn nicht\) umschalten zu können.  

### <a name="progressive-web-apps"></a>Progressive Web Apps  

#### <a name="lifetime-background-script"></a>Lifetime Background Script  

Windows 10-JavaScript-Apps \(In einem Prozess ausgeführte Web-Apps\) unterstützen nun ein optionales Anwendungshintergrundskript, das gestartet wird, bevor Ansichten aktiviert werden und für die Dauer des Prozesses ausgeführt `WWAHost.exe` werden.  Damit können Sie Navigationen überwachen und ändern, den Status über Navigationen hinweg nachverfolgen, Navigationsfehler überwachen und Code ausführen, bevor Ansichten aktiviert werden.  

Wenn sie als [StartPage](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) in Ihrem App-Manifest angegeben [wird,](/uwp/schemas/appxpackage/appx-package-manifest)werden alle Ansichten der App \(windows\) für das Skript als Instanzen der neuen [WebUIView-Klasse](/uwp/api/windows.ui.webui.webuiview) verfügbar gemacht und bieten dieselben Ereignisse, Eigenschaften und Methoden wie eine allgemeine \(Win32\) [WebView](/uwp/api/windows.web.ui.iwebviewcontrol).  Ihr Skript kann auf das [NewWebUIViewCreated-Ereignis](/uwp/api/windows.ui.webui.newwebuiviewcreatedeventargs) lauschen, um die Steuerung der Navigation für eine neue Ansicht abzufangen:  

```javascript
Windows.UI.WebUI.WebUIApplication.addEventListener("newwebuiviewcreated", newWebUIViewCreatedEventHandler);
```  

 Jede App-Aktivierung mit dem Hintergrundskript als das `StartPage` wird sich auf das Skript selbst für die Navigation verlassen.  

#### <a name="text-scaling"></a>Textskalierung  

Das Windows 10 October 2018 [](/windows/uwp/design/input/text-scaling#user-experience) Update führt die Einstellung Text vergrößern für verbesserte Endbenutzerfreundlichkeit ein, und unter Windows installierte PWAs \(zusätzlich UWP und die meisten Desktop-Apps\) unterstützen dieses Feature jetzt automatisch.  Bei PWAs- und WebView-Steuerelementen funktioniert die Textskalierung genauso wie die DPI-Skalierung.  Wenn ein Benutzer sowohl die Text- als auch die DPI-Skalierung ändert, ist das Ergebnis das Produkt der beiden.  

 Anleitungen zum Entwurf finden Sie im UWP-Leitfaden [zur Textskalierung](/windows/uwp/design/input/text-scaling) in *Windows Dev Center*.  

### <a name="service-worker-updates"></a>Service Worker-Updates  

Eine Aktualisierung darüber, was Service Workers sind und wie sie funktionieren, finden Sie in der [Service Worker-API-Zusammenfassung,](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) die von unseren Partnern unter MDN geschrieben wurde.  Es gab mehrere Updates für Microsoft Edge, die Service Workers in EdgeHTML 18 unterstützen.  Der `fetchEvent` ermöglicht es dem Dienstmitarbeiter, [preloadResponse](https://developer.mozilla.org/docs/Web/API/FetchEvent) zu verwenden, um eine Antwort zu versprechen, und die [resultierendeClientId](https://developer.mozilla.org/docs/Web/API/FetchEvent/clientId) gibt die ID des Clients zurück, den der aktuelle Dienstmitarbeiter steuert.  
Die [NavigationPreloadManager-Schnittstelle](https://developer.mozilla.org/docs/Web/API/NavigationPreloadManager) stellt Methoden zum Verwalten des Vorladens von Ressourcen bereit, sodass Sie eine Anforderung parallel beim Starten eines Dienstmitarbeiters stellen können, wodurch Zeitverzögerungen vermieden werden.  Sehen Sie sich die [neu unterstützten API-Eigenschaften](#new-apis-in-edgehtml-18) für die Liste der Service Worker-Vorablademethoden und -eigenschaften an.  

### <a name="web-authentication"></a>Webauthentifizierung  

Microsoft Edge bietet jetzt eine nicht vorbereite Unterstützung für die neue [Webauthentifizierungs-API](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge) \(aka [WebAuthN](https://w3c.github.io/webauthn)\).  Die Webauthentifizierung bietet eine offene, skalierbare und interoperable Lösung, um die Authentifizierung zu vereinfachen und eine bessere und sicherere Benutzererfahrung zu ermöglichen, indem Kennwörter durch stärkere hardwaregebundene Anmeldeinformationen ersetzt werden.  Die Implementierung in Microsoft Edge [](https://www.microsoft.com/windows/windows-hello) ermöglicht es Benutzern, sich neben externen Authentatoren [](https://fidoalliance.org) wie FIDO2-Sicherheitsschlüsseln oder FIDO U2F-Sicherheitsschlüsseln mit Ihrem Gesicht, Fingerabdruck oder PIN bei Websites zu anmelden.  

Weitere Informationen finden Sie im Blogbeitrag [Introducing Web Authentication in Microsoft Edge](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge).  

### <a name="webdriver"></a>WebDriver  

WebDriver ist jetzt ein [Windows-Feature](https://docs.microsoft.com/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) bei Bedarf \(FoD\), das es einfacher denn je macht, Tests in Microsoft Edge zu automatisieren und die richtige Version für Ihr Gerät zu erhalten.  Sie müssen bei der Installation von WebDriver nicht mehr manuell mit dem Build/Branch/Flavor übereinstimmen. Ihr [WebDriver](https://www.w3.org/TR/webdriver) wird automatisch aktualisiert, um neue Windows 10-Updates zu erhalten.  

Sie können WebDriver installieren, indem Sie den Entwicklermodus aktivieren oder es als eigenständiges Programm installieren, indem Sie zu **Einstellungen**  >  **Apps**  >  **Apps & Features**Verwalten  >  **optionaler Features wechseln.**  Weitere Informationen finden Sie in der [WebDriver-Ankündigung auf der Windows-Blogwebsite](https://blogs.windows.com/msedgedev/2018/06/14/webdriver-w3c-recommendation-feature-on-demand).  

### <a name="web-notification-properties"></a>Webbenachrichtigungseigenschaften  

Vier neue Eigenschaften werden jetzt für Webbenachrichtigungen  [unterstützt:](https://developer.mozilla.org/docs/Web/API/notification/actions) [Aktionen,](https://developer.mozilla.org/docs/Web/API/notification/badge) [Signal,](https://developer.mozilla.org/docs/Web/API/notification/image)Bild und , was unsere Fähigkeit verbessert, Benachrichtigungen im Web zu erstellen, die mit vorhandenen Benachrichtigungssystemen kompatibel sind, während wir plattformunabhängig  `maxActions` bleiben.  

### <a name="webview"></a>WebView  

#### <a name="service-workers"></a>Service Workers  

[Dienstmitarbeiter](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) werden jetzt im WebView-Steuerelement unterstützt, zusätzlich zum Microsoft Edge-Browser und Windows 10-JavaScript-Apps.  Alle Varianten der Microsoft Edge-Webview \([PWA](/microsoft-edge/hosting/webview), [UWP](/uwp/api/Windows.UI.Xaml.Controls.WebView), [Win32](/windows/communitytoolkit/controls/wpf-winforms/webview)\) unterstützen Servicemitarbeiter, beachten Sie jedoch, dass die [Push-API](https://developer.mozilla.org/docs/Web/API/Push_API) noch nicht für die UWP- und Win32-Versionen verfügbar ist.  

x64-App-Architekturen erfordern Neutral \(Any CPU\) oder x64-Pakete, da Servicemitarbeiter in WoW64-Prozessen nicht unterstützt werden.  \(Um Speicherplatz zu sparen, ist die WoW-Version der erforderlichen DLLs nicht systemeigener in Windows enthalten.\)  

#### <a name="win32-webview-updates"></a>Win32 WebView-Updates  

Die EdgeHTML [WebViewControl](/windows/communitytoolkit/controls/wpf-winforms/webview) für Windows-Desktop-Apps \(Win32\) wurden mit mehreren neuen Features aktualisiert, einschließlich der Möglichkeit, Skript beim Laden der Seite zu injizieren, bevor andere Skripts auf der Seite ausgeführt werden \([AddInitializeScript](/uwp/api/windows.web.ui.interop.webviewcontrol.addinitializescript)\) und wissen, wann ein bestimmtes WebViewControl den Fokus erhält oder verliert \([GotFocus](/uwp/api/windows.web.ui.interop.webviewcontrol.gotfocus) / [LostFocus](/uwp/api/windows.web.ui.interop.webviewcontrol.lostfocus)\).  

Darüber hinaus können Sie jetzt ein neues WebViewControl als geöffnetes Fenster von [window.open erstellen.](https://developer.mozilla.org/docs/Web/API/Window/open)  Das [NewWindowRequested-Ereignis](/uwp/api/windows.web.ui.iwebviewcontrol.newwindowrequested) benachrichtigt eine App weiterhin, wenn ein Skript innerhalb des WebViewControl-Aufrufs window.open wie immer aufruft, aber mit EdgeHTML 18 enthält [seine NewWindowRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs) die Möglichkeit, eine Verschiebung zu nehmen \([GetDeferral](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.getdeferral)\) zum Festlegen eines neuen WebViewControl \([NewWindow](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.newwindow)\) als Ziel für das window.open:  

```csharp
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

Schließlich bemerken Die Netzbenutzer möglicherweise die App des Desktop App Web Viewer \(zuvor win32WebViewHost\), einer internen System-App, die win32 WebView darstellt, an den folgenden Stellen:  

*   Im Windows 10 Action Center.  Die Quelle dieser Benachrichtigungen sollte in einer WebView verstanden werden, die von einer Win32-App gehostet wird.  
*   In der Benutzeroberfläche der Gerätezugriffseinstellungen \( `Settings`  >  `Privacy`  >  `Camera/Location/Microphone` \).  Wenn Sie eine dieser Einstellungen deaktivieren, wird der Zugriff von allen WebViews verweigert, die in Win32-Apps gehostet werden.  

![Einstellung für den Zugriff auf Desktop-App-Web Viewer-Geräte](./media/desktop-app-web-viewer.png)  

## <a name="deprecated-features"></a>Veraltete Funktionen  

### <a name="xss-filter-now-retired"></a>XSS-Filter jetzt eingestellt  

Mit EdgeHTML 18 wird der XSS-Filter in Microsoft Edge zurückgef?  Unsere Kunden bleiben dank moderner Standards wie [Content Security Policy (CSP)](https://developer.mozilla.org/docs/Web/HTTP/CSP)geschützt, die leistungsfähigere, leistungsfähigere und sichere Mechanismen zum Schutz vor Inhaltsinjektionsangriffen bieten, mit hoher Kompatibilität in modernen Browsern.  

## <a name="new-apis-in-edgehtml-18"></a>Neue APIs in EdgeHTML 18  

Sehen Sie sich die vollständige Liste der neuen APIs in EdgeHTML 18 an.  Sie sind im Format [Schnittstellenname] aufgeführt. [API-Name].  

> [!NOTE] 
> Obwohl die folgenden APIs im DOM verfügbar gemacht werden, ist das End-to-End-Verhalten einiger möglicherweise noch in der Entwicklung und hinter einem experimentellen Flag verborgen.  Das offizielle Wort zur Featureunterstützung finden Sie unter Microsoft Edge-Plattformstatus. [](https://developer.microsoft.com/microsoft-edge/platform/status/)  

<iframe height='580' scrolling='no' title='Neue APIs in EdgeHTML 18' src='//codepen.io/MSEdgeDev/embed/5d7be9404d82575162b486e79d0dd58f
/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Weitere Informationen finden Sie unter Pen <a href='https://codepen.io/MSEdgeDev/pen/5d7be9404d82575162b486e79d0dd58f'> New APIs in EdgeHTML 18 </a> by MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) auf </a> <a href='https://codepen.io'> CodePen </a> .</iframe>  

## <a name="previous-edgehtml-releases"></a>Frühere EdgeHTML-Versionen  

[EdgeHTML 13 / Windows Build 10586 (11/2015)](./whats-new/edgehtml-13.md)  

[EdgeHTML 14 / Windows Build 14393 (8/2016)](./whats-new/edgehtml-14.md)  

[EdgeHTML 15 / Windows Build 15063 (4/2017)](./whats-new/edgehtml-15.md)  

[EdgeHTML 16 / Windows Build 16299 (10/2017)](./whats-new/edgehtml-16.md)  

[EdgeHTML 17 / Windows Build 17134 (04/2018)](https://aka.ms/devguide_edgehtml_17)  
