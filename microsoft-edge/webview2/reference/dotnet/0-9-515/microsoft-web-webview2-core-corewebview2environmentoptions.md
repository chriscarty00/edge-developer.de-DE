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
ms.openlocfilehash: d29d5a716bb52d2e4e28fc1acf0f3bbf9874584b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654019"
---
# Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions Klasse 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Optionen zum Erstellen der WebView2-Umgebung

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[AdditionalBrowserArguments](#additionalbrowserarguments) | AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern.
[Sprache](#language) | Die Standardsprache, mit der WebView ausgeführt wird.
[TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion) | Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind.
[CoreWebView2EnvironmentOptions](#corewebview2environmentoptions) | Initialisiert eine neue Instanz der CoreWebView2EnvironmentOptions-Klasse.

Eine Standardimplementierung wird in WebView2EnvironmentOptions. h bereitgestellt.

## Member

#### AdditionalBrowserArguments 

AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern.

> public String [AdditionalBrowserArguments](#additionalbrowserarguments)

Diese werden als Teil der Befehlszeile an den Browserprozess übergeben. Weitere Informationen zu Befehlszeilen wechseln in den Browserprozess finden Sie unter [Ausführen von Chrom mit Flags](https://aka.ms/RunChromiumWithFlags) . Wenn die APP mit einem Befehlszeilen Schalter gestartet wird, `--edge-webview-switches=xxx` wird der Wert dieses Schalters (xxx im obigen Beispiel) auch an die Befehlszeile des Browser Prozesses angefügt. Bestimmte Schalter wie `--user-data-dir` sind intern und wichtig für WebView. Diese Schalter werden ignoriert, auch wenn Sie angegeben werden. Wenn dieselben Schalter mehrmals angegeben werden, gewinnt der letzte. Es wird nicht versucht, die verschiedenen Werte desselben Schalters zusammenzuführen, mit Ausnahme von deaktivierten und aktivierten Features. Die Features, die von `--enable-features` und `--disable-features` mit einfacher Logik zusammengeführt werden: die Features sind die Vereinigung der angegebenen Features und integrierten Features, und wenn ein Feature deaktiviert ist, wird es aus der Liste der aktivierten Features entfernt. Der Befehlszeilenwert des App-Prozesses `--edge-webview-switches` wird verarbeitet, nachdem der additionalBrowserArguments-Parameter verarbeitet wurde. Bestimmte Features sind intern deaktiviert und können nicht aktiviert werden. Wenn die Analyse bei den angegebenen Schaltern fehlgeschlagen ist, werden Sie ignoriert. Standardmäßig wird der Browserprozess ohne zusätzliche Flags ausgeführt.

#### Sprache 

Die Standardsprache, mit der WebView ausgeführt wird.

> öffentliche Zeichenfolgen [Sprache](#language)

Sie bezieht sich auf Browser-UIs wie Kontextmenüs und Dialogfelder. Sie gilt auch für den HTTP-Header Accept-Languages, der von WebView an Websites gesendet wird. Das Format von `language[-country]` Where `language` ist der 2-Buchstaben-Code von ISO 639 und `country` der 2-Buchstaben-Code von ISO 3166.

#### TargetCompatibleBrowserVersion 

Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind.

> public String [TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion)

Dies ist standardmäßig die Edge WebView2-Laufzeitversion, die der Version des SDK entspricht, das die Anwendung verwendet. Das Format dieses Werts entspricht dem Format der BrowserVersionString-Eigenschaft und anderen Browserversion-Werten. Nur der Versions Teil des Browserversion-Werts wird berücksichtigt. Wenn es vorhanden ist, wird das Kanal Suffix ignoriert. Die Version der tatsächlich verwendeten Edge-WebView2-Runtime-Binärdateien kann sich vom angegebenen TargetCompatibleBrowserVersion unterscheiden. Sie sind nur garantiert kompatibel. Sie können die aktuelle Version auf der BrowserVersionString-Eigenschaft auf der CoreWebView2Environment-Eigenschaft überprüfen.

#### CoreWebView2EnvironmentOptions 

Initialisiert eine neue Instanz der CoreWebView2EnvironmentOptions-Klasse.

> Public [CoreWebView2EnvironmentOptions](#corewebview2environmentoptions)(String additionalBrowserArguments, String Language, String targetCompatibleBrowserVersion)

##### Parameter
* `additionalBrowserArguments` AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern. 

* `language` Die Standardsprache, mit der WebView ausgeführt wird. 

* `targetCompatibleBrowserVersion` Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind.

