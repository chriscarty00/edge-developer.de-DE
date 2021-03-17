---
description: Verwenden Sie das Microsoft Edge DevTools-Protokoll, um den Microsoft Edge (EdgeHTML)-Browser zu überprüfen und zu debuggen.
title: Microsoft Edge DevTools-Protokoll
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bc95f6c167479e958ffd16137176418aba872a43
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439310"
---
# <a name="microsoft-edge-edgehtml-devtools-protocol"></a>Microsoft Edge (EdgeHTML) DevTools Protocol

> [!NOTE]
> Das Microsoft Edge (EdgeHTML)-DevTools-Protokoll funktioniert nur unter [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) und späteren Builds.

Entwicklertools können das **Microsoft Edge (EdgeHTML)-DevTools-Protokoll** verwenden, um den Microsoft Edge (EdgeHTML)-Browser zu überprüfen und zu debuggen. Es bietet eine Reihe von Methoden und Ereignissen, die in verschiedene [Domänen der](0.2/domains/index.md) EdgeHTML-Modulinstrumentierung organisiert sind.

 Toolclients können diese Methoden aufrufen und diese Ereignisse über JSON-Websocketnachrichten überwachen, die mit dem *devTools Server* ausgetauscht werden, der von Microsoft Edge (EdgeHTML) oder dem Windows Device Portal gehostet wird. Microsoft Edge (EdgeHTML) DevTools verwendet dieses Protokoll, um das [Remotedebuding](0.2/clients.md#microsoft-edge-devtools-preview) eines Hostcomputers zu ermöglichen, auf dem Microsoft Edge (EdgeHTML) vom eigenständigen DevTools-Client ausgeführt wird, der im [Microsoft Store verfügbar ist.](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj)

Das Microsoft Edge (EdgeHTML)-DevTools-Protokoll ist so konzipiert, dass es eng mit dem Chrome DevTools-Protokoll (siehe [W3C WICG für DevTools-Protokolle)](https://github.com/WICG/devtools-protocol/)in Einklang steht, obwohl in dieser Version bekannte Interoperabilitätslücken bestehen.

## <a name="using-the-protocol"></a>Verwenden des Protokolls

Hier erfahren Sie, wie Sie einen benutzerdefinierten Toolclient an den DevTools Server in Microsoft Edge (EdgeHTML) anfügen. Lesen Sie die Anweisungen zum Remotedebug, wenn Sie Microsoft Edge DevTools als Client verwenden. [](0.2/clients.md#microsoft-edge-devtools-preview)

1. Starten Sie Microsoft Edge (EdgeHTML), wenn der Remotedebugport geöffnet ist, und geben Sie die URL an, die Sie öffnen möchten. Zum Beispiel:

    ```shell
    MicrosoftEdge.exe --devtools-server-port 9222 https://www.bing.com
    ```

    Wenn Edge bereits gestartet wurde, ist der PARAMETER URL optional. Neben der Browseradressenleiste wird eine Schaltfläche angezeigt, die angibt, dass der **Entwicklertoolsserver** gestartet wurde:

    ![Entwicklertoolsserver](media/developer-tools-server.png) 

2. Verwenden Sie diesen [HTTP-Endpunkt,](0.2/http.md) um eine Liste der anfügenbaren Seitenziele zu erhalten:

    ```http
    http://localhost:9222/json/list
    ```

3. Stellen Sie eine Verbindung mit der Liste der gewünschten Seite zur Ausgabe weiterer Protokollbefehle und zum Empfangen von Ereignismeldungen über `webSocketDebuggerUrl` den devtools-Socketserver fest. [](0.2/domains/index.md)

## <a name="status-and-feedback"></a>Status und Feedback

[Version 0.2](0.2/index.md) des DevTools-Protokolls stellt neben den in [Version 0.1](0.1/index.md)eingeführten grundlegenden Skriptdebudfunktionen neue Domänen für Das Debuggen von Formaten und Layouts (schreibgeschützt) und Konsolen-APIs bereit. In der Benutzeroberfläche von Microsoft Edge DevTools bedeutet dies, dass funktionen in den [**Panels Elemente,**](../devtools-guide/elements.md) [**Konsole**](../devtools-guide/console.md) und [**Debugger verfügbar**](../devtools-guide/debugger.md) sind.

Vielen Dank für das Ausprobieren des Edge DevTools-Protokolls! Wir freuen uns über Ihr Feedback unter:

<!-- - [**Microsoft Edge Developer UserVoice**](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer?category_id=84475): DevTools feature ideas and requests-->  

 - [**EdgeHTML Issue Tracker**](https://developer.microsoft.com/microsoft-edge/platform/issues/): Protokoll-, DevTools- und EdgeHTML-Plattformfehler und -probleme

 - [**Microsoft Edge DevTools Feedback Hub**](feedback-hub:?referrer=microsoftEdge&tabID=2&newFeedback=true&ContextId=344): Protokoll- und DevTools-Probleme und Vorschläge über die FeedbackHub-App

## <a name="faq"></a>FAQ

#### <a name="can-multiple-clients-connect-to-the-same-devtools-server"></a>Können mehrere Clients eine Verbindung mit demselben DevTools Server herstellen?
Nein, nicht gleichzeitig, wenn die Clients debuggen. Der letzte Client, der eine Verbindung herstellen soll, startet den vorherigen Client. Wenn in Zukunft zusätzliche Tools unterstützt werden, werden diese wahrscheinlich gleichzeitige Clientverbindungen unterstützen.

#### <a name="do-i-have-to-use-9222-as-the-devtools-server-port"></a>Muss ich 9222 als DevTools Server-Port verwenden?
Nein. Sie können einen beliebigen Port angeben, aber achten Sie darauf, einen Port zu wählen, der noch nicht verwendet wird. Port 9222 für Remotedebu debugging wird konventionskonvent verwendet.

#### <a name="how-do-i-connect-my-custom-tooling-client-to-microsoft-edge-edgehtml-running-the-devtools-server"></a>Wie kann ich meinen benutzerdefinierten Toolclient mit Microsoft Edge (EdgeHTML) verbinden, auf dem devTools Server ausgeführt wird?
Informationen [*zum Anfügen an*](#using-the-protocol) Microsoft Edge (EdgeHTML), das auf dem lokalen Computer ausgeführt wird, finden Sie unter Verwenden der obigen Protokollanweisungen. Wenn Sie remote debuggen möchten, müssen Sie einen Benutzerworkflow für die Installation des SSL-Zertifikats des Hostcomputers auf dem Client entwickeln, z. B. mit einem Installationsdialogfeld, wie [microsoft Edge DevTools Preview](./0.2/clients.md#microsoft-edge-devtools-preview) verwendet.

#### <a name="if-im-remote-debugging-using-edge-devtools-do-i-need-to-start-the-host-browser-process-with---devtools-server-port-cmd-line-switch"></a>Wenn ich remote debugge mit Edge DevTools bin, muss ich den Hostbrowserprozess mit *--devtools-server-port* cmd line switch starten? 
Nein. Wenn Sie das Remotedebuding mit [Microsoft Edge DevTools Preview](./0.2/clients.md#microsoft-edge-devtools-preview)einrichten, ist der Befehlszeilenschalter zum Starten von Edge nicht `--devtools-server-port` erforderlich. In diesem Fall *hosten* windows Device Portal den DevTools Server im Namen des Browsers.

#### <a name="can-i-use-the-edge-devtools-protocol-to-remotely-debug-a-wwahostexe-or-webview-process"></a>Kann ich das Edge DevTools-Protokoll zum Remotedebuggern eines WWAHost.exe webview-Prozesses verwenden?
Das Edge DevTools-Protokoll unterstützt derzeit nur Browserregisterkarten. WWAHost.exe und Webviewprozesse werden nicht unterstützt.
