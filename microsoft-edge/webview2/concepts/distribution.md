---
description: Verteilungsoptionen beim Freigeben einer APP mit Microsoft Edge WebView2
title: Verteilung der Microsoft Edge WebView2-Anwendung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: a789b0f4f9c482670f843ed21368b4168f99abe0
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659705"
---
# Verteilung von Anwendungen mithilfe von WebView2 

Das WebView2-Steuerelement verwendet den Microsoft Edge \ (Chromium \)-Browser. Stellen Sie beim Verteilen der APP sicher, dass der Edge-Browser auf allen Benutzercomputern, auf denen die Anwendung ausgeführt wird, installiert ist. Das WebView2-Steuerelement verwendet die stabilste Version des Browsers, der auf einem Computer installiert ist. So können Sie beispielsweise stable, Beta, dev und Canary zur gleichen Zeit installiert haben, und in dieser Situation werden WebView2-Steuerelemente im stable-Kanal ausgeführt. Stellen Sie sicher, dass Sie die Versionshinweise überprüfen, um sicherzustellen, dass die Version des Browsers auf ihren Computern, auf denen Ihre WebView2-Steuerelemente ausgeführt werden, die Mindestanforderungen für die Version erfüllt.

## Roadmap

Wir erkennen an, dass der Edge-Browser möglicherweise nicht auf allen Benutzercomputern verfügbar ist, auf denen Ihre Anwendung ausgeführt wird, oder dass das Installieren des Edge-Browsers in Ihrer Organisation schwierig sein kann. Um sicherzustellen, dass Ihre Anwendung auf allen Computern ausgeführt wird, unabhängig vom installierten Microsoft Edge-Browser, werden wir die Microsoft Edge WebView2-Laufzeit freigeben. Darüber hinaus werden wir WebView2 aktualisieren, um nach der stabilen Version der Runtime zu suchen, bevor Sie nach Vorabversionen des installierten Browsers suchen.

Es wird Unterstützung für zwei Verteilungsoptionen unter Verwendung der WebView2-Laufzeit: Evergreen und eine feste Version geben.

Evergreen ist das empfohlene Verteilungsmodell für die meisten Entwickler. In diesem Modus werden Updates automatisch an die WebView2-Laufzeit übertragen, ohne dass die Anwendung zusätzlichen Aufwand erfordert. Das Evergreen-Modell stellt sicher, dass Ihre APP die neuesten Funktionen und Sicherheitsupdates für gehostete Webinhalte nutzt.

Für abhängige Umgebungen wird Unterstützung für ein festes Versions Verteilungsmodell zur Verfügung stehen. In diesem Modell wählt ihre Anwendung eine bestimmte Version von WebView2 aus und gibt diese Pakete aus. Aktualisierungen der WebView-Version werden nicht automatisch ausgeführt, und die Anwendung ist für Sie verantwortlich. Das Modell der festen Version ist vorteilhaft, wenn Sie die Browserversion Steuern und die Anwendung aktualisieren müssen. 

### Microsoft Edge-WebView2-Laufzeit

Die Microsoft Edge WebView2-Laufzeit verpackt die Browser-Binärdateien, die für die Verwendung durch WebView2-Anwendungen optimiert sind. Es funktioniert eigenständig oder nebeneinander, wenn ein Client-Edge-Browser installiert ist. Das einmalige Installieren der Runtime unterstützt viele WebView2-Anwendungen, die auf dem Clientcomputer ausgeführt werden. Das Installieren der Laufzeit wird nicht als Browser für Endbenutzer angezeigt, und es werden keine Desktopverknüpfungen, ein Einstiegspunkt für das Startmenü oder eine Protokoll Registrierung angezeigt.

Anwendungen, die die WebView2-Laufzeit verwenden, müssen sicherstellen, dass die Runtime-Installation abgeschlossen ist. Um sicherzustellen, dass Ihre Anwendung die Laufzeit als Abhängigkeit installiert, können Sie die Laufzeit dem Installations Fluss hinzufügen. 
