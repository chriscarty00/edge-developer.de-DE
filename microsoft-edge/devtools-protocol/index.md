---
description: Verwenden Sie das Microsoft Edge devtools-Protokoll zum Überprüfen und Debuggen des Microsoft Edge (EdgeHTML)-Browsers.
title: Microsoft Edge devtools-Protokoll
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 8bef24c98dae284f2111f6a16fca4a6f27c89dc4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567525"
---
# Microsoft Edge (EdgeHTML) devtools-Protokoll

> [!NOTE]
> Das EdgeHTML-devtools-Protokoll (Microsoft Edge) funktioniert nur unter [Windows 10 April 2018-Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) und neueren Versionen.

Entwicklertools können das **Microsoft Edge (EdgeHTML)-devtools-Protokoll** zum Überprüfen und Debuggen des Microsoft Edge-Browsers (EdgeHTML) verwenden. Sie stellt eine Reihe von Methoden und Ereignissen bereit, die in verschiedenen [Domänen](0.2/domains/index.md) der EdgeHTML-Modul Instrumentation organisiert sind.

 Tooling-Clients können diese Methoden aufrufen und diese Ereignisse über JSON Web Socket-Nachrichten überwachen, die mit dem von Microsoft Edge (EdgeHTML) gehosteten *devtools-Server* oder dem Windows-Geräte Portal ausgetauscht werden. Microsoft Edge (EdgeHTML) devtools verwendet dieses Protokoll zum Aktivieren des [Remotedebuggens](0.2/clients.md#microsoft-edge-devtools-preview) eines Hostcomputers, auf dem Microsoft Edge (EdgeHTML) ausgeführt wird, vom eigenständigen devtools-Client, der im [Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj)verfügbar ist.

Das Microsoft Edge (EdgeHTML)-devtools-Protokoll ist so konzipiert, dass es eng mit dem Chrom-devtools-Protokoll ausgerichtet wird (siehe [W3C-WICG für devtools-Protokolle](https://github.com/WICG/devtools-protocol/)), obwohl es in dieser Version bekannte Interoperabilitäts Lücken gibt.

## Verwenden des Protokolls

Hier erfahren Sie, wie Sie einen benutzerdefinierten Tooling-Client an den devtools-Server in Microsoft Edge (EdgeHTML) anfügen. Lesen Sie die Anweisungen für das [Remotedebuggen](0.2/clients.md#microsoft-edge-devtools-preview) , wenn Sie Microsoft Edge devtools als Client verwenden.

1. Starten Sie Microsoft Edge (EdgeHTML) mit geöffnetem Remote Debugging-Port, und geben Sie die URL an, die Sie öffnen möchten. Beispiel:

    ```
    MicrosoftEdge.exe --devtools-server-port 9222 https://www.bing.com
    ```

    Wenn Edge bereits gestartet wurde, ist der URL-Parameter optional. Neben der Adressleiste des Browsers wird eine Schaltfläche angezeigt, die angibt, dass der **Entwicklertools-Server** gestartet wurde:

    ![Developer Tools-Server](media/developer-tools-server.png) 

2. Verwenden Sie diesen [HTTP-Endpunkt](0.2/http.md) , um eine Liste von anfügbaren Seiten Zielen abzurufen:

    ```
    http://localhost:9222/json/list
    ```

3. Stellen Sie eine Verbindung mit der Liste der `webSocketDebuggerUrl` gewünschten Seite her, um weitere [Protokollbefehle](0.2/domains/index.md) auszugeben und Ereignismeldungen über den devtools-Socketserver zu empfangen.

## Status und Feedback

[Version 0,2](0.2/index.md) des devtools-Protokolls bietet neue Domänen für Stil-und Layoutfunktionen (schreibgeschützt) sowie Debug-und Konsolen-APIs sowie die Kernskript Debugging-Funktionen, die in [Version 0,1](0.1/index.md)eingeführt wurden. In der Benutzeroberfläche von Microsoft Edge devtools wird dadurch die Funktionalität übersetzt, die in den Panels [**Elemente**](../devtools-guide/elements.md), [**Konsole**](../devtools-guide/console.md) und [**Debugger**](../devtools-guide/debugger.md) zur Verfügung steht.

Vielen Dank, dass Sie das Edge devtools-Protokoll ausprobiert haben! Wir freuen uns über Ihr Feedback unter:

 - [**Microsoft Edge Developer UserVoice**](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer?category_id=84475): devtools-Feature-Ideen und-Anforderungen

 - [**EdgeHTML Issue Tracker**](https://developer.microsoft.com/microsoft-edge/platform/issues/): Protokoll-, devtools-und EdgeHTML-Platt Formfehler und-Probleme

 - [**Microsoft Edge devtools-Feedback-Hub**](feedback-hub:?referrer=microsoftEdge&tabID=2&newFeedback=true&ContextId=344): Protokoll-und DevTools-Probleme und Vorschläge über die Feedback-Hub-App

## Häufig gestellte Fragen (FAQ)

#### Können mehrere Clients eine Verbindung mit demselben devtools-Server herstellen?
Nein, nicht gleichzeitig, wenn die Clients Debuggen. Der letzte zu verbindende Client startet den vorherigen. Wenn zusätzliche Tools unterstützt werden, werden in Zukunft wahrscheinlich gleichzeitige Clientverbindungen unterstützt.

#### Muss ich 9222 als devtools-Server-Port verwenden?
Nein. Sie können einen beliebigen Port angeben, aber sicher sein, dass Sie einen Port auswählen, der noch nicht verwendet wird. Port 9222 für das Remotedebuggen wird von der Konvention verwendet.

#### Wie verbinde ich meinen benutzerdefinierten Tooling-Client mit Microsoft Edge (EdgeHTML), auf dem der devtools-Server ausgeführt wird?
Weitere Informationen finden Sie unter [*Verwenden der*](#using-the-protocol) oben aufgeführten Protokollanweisungen für das Anfügen an Microsoft Edge (EdgeHTML), das auf dem lokalen Computer ausgeführt wird. Wenn Sie das Remotedebuggen unterstützen möchten, müssen Sie einen Benutzer Workflow für die Installation des SSL-Zertifikats des Hostcomputers auf dem Client entwerfen, beispielsweise mit einem Installationsdialogfeld, in dem [Microsoft Edge devtools Preview](./0.2/clients.md#microsoft-edge-devtools-preview) verwendet wird.

#### Wenn ich mithilfe von Edge-devtools Remotedebuggen möchte, muss ich den Hostbrowser Prozess mit *--devtools-Server-Port* cmd-Zeilenschalter starten? 
Nein. Wenn Sie das [Remotedebuggen mithilfe von Microsoft Edge devtools Preview](./0.2/clients.md#microsoft-edge-devtools-preview)einrichten, `--devtools-server-port` ist die Befehlszeilenoption für das Starten von Edge nicht erforderlich. In diesem Fall wird im Windows- *Geräte Portal* der devtools-Server im Auftrag des Browsers gehostet.

#### Kann ich das Edge devtools-Protokoll verwenden, um einen WWAHost. exe-oder WebView-Prozess Remote zu Debuggen?
Das Edge devtools-Protokoll unterstützt derzeit nur browserregisterkarten. WWAHost. exe und WebView-Prozesse werden nicht unterstützt.
