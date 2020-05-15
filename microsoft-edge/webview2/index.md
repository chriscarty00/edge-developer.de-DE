---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Steuerelement "Microsoft Edge WebView 2"
title: Microsoft Edge WebView 2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: b1ec0c43b57fb107490ddb34b330bb6ec378ac41
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653813"
---
# Microsoft Edge WebView2 (Developer Preview)

Mit dem Microsoft Edge WebView2-Steuerelement können Sie Webinhalte in Ihrer Anwendung mithilfe von [Microsoft Edge (Chrom)](https://www.microsoftedgeinsider.com/) als Rendering-Modul hosten.

Das WebView2-Steuerelement befindet sich derzeit in der Entwicklervorschau, in der Sie Ihre Lösungen Prototypieren und Feedback an uns senden können, um die zukünftige stabile API zu gestalten. Es werden wahrscheinlich einige wichtige Änderungen auftreten, während wir die API während der Vorschau entwickeln, und wenn dies der Fall ist, müssen Sie sowohl das WebView2-SDK als auch den Microsoft Edge (Chrom)-Browser aktualisieren. Wichtige Änderungen werden in den [Versions](./releasenotes.md) Hinweisen des SDK aufgeführt. Dies wird gesperrt, da WebView2 sich Beta und stable nähert.

## Unterstützte Plattformen

Für Win32 C/C++ und Windows Forms und WPF unter .NET Framework 4.6.2 oder höher und .net Core 3,0 oder höher unter Windows 10, Windows 8,1, Windows 8, Windows 7, Windows Server 2016, Windows Server 2012/2012R2 und Windows Server 2008 R2 steht eine Entwicklervorschau zur Verfügung. Eine Alpha-Version für WinUI 3,0 steht [hier](https://docs.microsoft.com/uwp/toolkits/winui3/)zur Verfügung.

## Erste Schritte

Wenn Sie Ihre Anwendung mithilfe des WebView2-Steuerelements erstellen und testen möchten, müssen Sie sowohl [Microsoft Edge (Chrom)](https://www.microsoftedgeinsider.com/download/) als auch das [WebView2-SDK](https://aka.ms/webviewnuget) installiert haben. Wählen Sie eine der folgenden Optionen aus, um zu beginnen!

* [Erste Schritte mit Win32 C/C++](./gettingstarted/win32.md)
* [Erste Schritte mit WPF](./gettingstarted/wpf.md)
* [Erste Schritte mit Windows Forms](./gettingstarted/winforms.md)

Bitte geben Sie uns Feedback in unserem [WebView2 Feedback](https://aka.ms/webviewfeedback) Repo.

## WebView2-Beispiele

Das [WebView2-Beispiel](https://github.com/MicrosoftEdge/WebView2Samples) -Repository enthält Beispiele, in denen alle Features des WebView2 SDK sowie deren API-Verwendungsmuster veranschaulicht werden. Wenn wir dem WebView2-SDK weitere Funktionen hinzufügen, werden wir unsere Beispielanwendungen regelmäßig aktualisieren.

## App-Verteilung

Das WebView2-Steuerelement verwendet den Microsoft Edge (Chrom)-Browser. Beim Verteilen der APP ist es wichtig, sicherzustellen, dass der Edge-Browser auf allen Benutzercomputern installiert ist, auf denen die Anwendung ausgeführt wird. Beachten Sie auch, welche Version und welcher Kanal installiert ist, beispielsweise stable, Beta, dev oder Canary. Der WebView2-Controller verwendet die stabilste Version des Browsers, wenn er auf einem Computer installiert ist.

### Geplante Änderungen in Zukunft

Wir erkennen an, dass der Edge-Browser möglicherweise nicht auf allen Benutzercomputern verfügbar ist, die Ihre Anwendung ausführen soll, oder dass die Steuerung des Edge-Browser-Installationsprozesses schwierig sein kann. Um sicherzustellen, dass die Anwendung auf allen Computern ausgeführt wird, unabhängig vom Installationsstatus des Microsoft Edge-Browsers für Microsoft Edge, werden wir die Microsoft Edge WebView2-Laufzeit freigeben. Wir werden WebView2 weiter aktualisieren, um nach der stabilen Version der Runtime zu suchen, bevor Sie nach Vorabversionen des installierten Browsers suchen.

Wir erkennen auch, dass einige App-Entwickler in abhängigen Umgebungen arbeiten und beabsichtigen, zwei Verteilungsoptionen zu unterstützen: Evergreen und Fixed-Version.

Evergreen ist das empfohlene Verteilungsmodell für die meisten Entwickler. In diesem Modus werden Updates der WebView2-Laufzeit vollständig von Microsoft verwaltet, sodass Sie automatisch ohne zusätzlichen Aufwand von Ihrer Anwendung auf dem neuesten Stand sind. Mit diesem selbst aktualisierbaren Modell können Sie sicher sein, dass Ihre APP die neuesten Funktionen und Sicherheitsupdates für gehostete Webinhalte nutzt.

Für abhängige Umgebungen unterstützen wir auch ein festes Versions Verteilungsmodell. In diesem Modell wird Ihre Anwendung eine bestimmte WebView2-Version auswählen und Verpacken. Updates für die WebView-Version sind in der Verantwortung der Anwendung und werden unabhängig von verwalteten Microsoft Update-Mechanismen sein. Wählen Sie dieses Modell aus, wenn es von entscheidender Bedeutung ist, die Browserversion und die Aktualisierungszeiten, die Ihre Anwendung nutzt, absolut zu kontrollieren.

## Microsoft Edge-WebView2-Laufzeit

Die Microsoft Edge WebView2-Laufzeit ist eine Verpackung der Browser-Binärdateien, die für die Verwendung durch WebView2-Anwendungen optimiert sind. Es wird eigenständig oder nebeneinander mit einer Client-Edge-Browser-Installation funktionieren. Eine einzelne Installation der Laufzeit unterstützt eine beliebige Anzahl von WebView2-Anwendungen. Die Installation der Common Language Runtime wird nicht als Browserinstallation für Endbenutzer angezeigt, also keine Desktopverknüpfungen, Startmenüeintrag oder Protokoll Registrierung.

Eine Anwendung, die WebView2 verwendet, muss sicherstellen, dass die Installation der Microsoft Edge WebView2-Laufzeit erfolgt ist. Bei der Anwendungs Installationszeit sollten Sie den aktuellen Installationsstatus überprüfen, der mithilfe von [GetAvailableCoreWebView2BrowserVersionString](./reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring)ermittelt werden kann. Wenn die WebView2-Laufzeit nicht zur Verfügung steht, sollten Sie das Installationsprogramm für Microsoft Edge WebView2-Runtime an den Installations Fluss anketten.

## Microsoft Edge WebView2 SDK

Damit Sie WebView2 in Ihrer APP verwenden können, müssen Sie das WebView2- [SDK](https://aka.ms/webviewnuget) in Ihrer Anwendung installieren und darauf verweisen. Unsere NuGet-Versionen enthalten sowohl eine Veröffentlichungs-als auch eine Vorabversion. Die Veröffentlichungsversion enthält die öffentlichen APIs, die derzeit zur allgemeinen Verfügbarkeit freigegeben werden sollen.

Die Pre-Release-Version enthält zusätzliche [experimentelle APIs](./reference/win32/0-9-488-reference-webview2.md#experimental). Hierbei handelt es sich um APIs und Funktionen, die wir evaluieren und [Feedback](https://aka.ms/webviewfeedback) erhalten möchten, bevor Sie auf die Veröffentlichungsversion heraufstufen.

## Entwicklung gegen bevorstehende Versionen

Für die Entwicklung möchten Sie möglicherweise auf Beta, dev oder Canary Zielen, um sicherzustellen, dass Ihre Anwendung mit anstehenden Versionen funktioniert, oder um die Vorteile der bevorstehenden Funktionen zu nutzen. Alle vorab freigegebenen Kanäle werden vom installierten Client Microsoft Edge-Browser bereitgestellt. Um auf einen dieser Kanäle zu Zielen, stellen Sie sicher, dass der installierte Edge-Browser auf Ihrem Entwicklungscomputer der Kanal ist, den Sie möchten. Entwickler können einen Registrierungsschlüssel oder eine Umgebungsvariable verwenden, um die WebView2 von der stabilsten Version zu ändern, die gefunden wurde. Weitere Details finden Sie unter [CreateCoreWebView2EnvironmentWithOptions](./reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions).

## Debuggen von WebView2

### DevTools

Sie können [Microsoft Edge (Chrom)-Entwickler Tools](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium) zum Debuggen von Webinhalten verwenden, die in WebView angezeigt werden, genau wie im Browser. Wenn Sie den Fokus auf das WebView-Fenster legen, drücken `F12` oder drücken Sie `Ctrl`  +  `Shift`  +  `I` , oder klicken Sie mit der rechten Maustaste auf, `Inspect` um die Entwickler Tools zu öffnen.

:::image type="complex" source="./media/f12.png" alt-text="F12":::
   F12
:::image-end:::  

<!--![F12](./media/f12.png)  -->  

**Hinweis Wenn das Debuggen einer Anwendung in Visual Studio mit dem systemeigenen Debugger angefügt wird, `F12` kann der systemeigene Debugger anstelle der Entwickler Tools ausgelöst werden. Verwenden `Ctrl`  +  `Shift`  +  `I` Sie oder klicken Sie mit der rechten Maustaste, `Inspect` um mögliche Hotkey-Konflikte zu vermeiden.**

### Visual Studio

Sie können den Skriptdebugger in Visual Studio 2019 (minimale Version 16,4 Preview 2) verwenden, um Ihr Skript in WebView2 direkt aus der IDE zu debuggen. Stellen Sie sicher, dass die **JavaScript-Diagnose** Komponente in der **Desktop Entwicklung mit C++** -Arbeitsauslastung installiert ist.

:::image type="complex" source="./media/vs-js-diagnostics.jpg" alt-text="Visual Studio-JavaScript-Diagnose":::
   Visual Studio-JavaScript-Diagnose
:::image-end:::  

<!--![vs-js-diagnostics](./media/vs-js-diagnostics.jpg)  -->  

Klicken Sie mit der rechten Maustaste auf Ihr Projekt, und wählen Sie **Eigenschaften**aus. Wählen Sie unter **Konfigurationseigenschaften**  >  **Debug**-  >  **Debuggertyp**die Option **JavaScript (WebView2)** aus, um das WebView2-Skriptdebuggen zu aktivieren. Weitere Details folgen in Kürze.

:::image type="complex" source="./media/vs-script-debugger.jpg" alt-text="Visual Studio-Skriptdebugger":::
   Visual Studio-Skriptdebugger
:::image-end:::  

<!--![vs-script-debugger](./media/vs-script-debugger.jpg)  -->  

### Visual Studio Code

Sie können auch Visual Studio-Code verwenden, um Ihr Skript innerhalb der WebView2 direkt aus der IDE zu debuggen. Weitere Informationen finden Sie [hier](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).

## Kontakt mit dem WebView2-Team  

Helfen Sie uns, ein reicheres WebView2-Erlebnis zu schaffen, indem Sie Ihr Feedback austauschen! Besuchen Sie unser [Feedback-Repo](https://aka.ms/webviewfeedback) , um Feature-Anfragen oder Fehlerberichte einzureichen.

Es ist auch ein guter Ort, um nach bekannten Problemen zu suchen.
Während der Entwicklervorschau werden wir auch Telemetrie-Daten sammeln, damit wir eine bessere WebView erstellen können. Benutzer können die WebView-Datensammlung deaktivieren, indem Sie im Browser zu Edge://Settings/Privacy navigieren und die Browserdaten Sammlung deaktivieren.
