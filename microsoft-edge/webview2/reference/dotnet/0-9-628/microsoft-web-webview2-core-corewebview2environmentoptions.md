---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions
ms.openlocfilehash: b5f940dedd513e15564d410e7edf0f94024f4e37
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012026"
---
# Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions Klasse 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Optionen zum Erstellen der WebView2-Umgebung

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[AdditionalBrowserArguments](#additionalbrowserarguments) | AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern.
[AllowSingleSignOnUsingOSPrimaryAccount](#allowsinglesignonusingosprimaryaccount) | Die AllowSingleSignOnUsingOSPrimaryAccount-Eigenschaft wird verwendet, um die einmalige Anmeldung mit Azure Active Directory (AAD)-Ressourcen in WebView unter Verwendung des angemeldeten Windows-Kontos und des einmaligen Anmeldens bei Websites zu aktivieren, die das Microsoft-Konto verwenden, das mit dem Anmeldenamen im Windows-Konto verknüpft ist.
[Sprache](#language) | Die Standardsprache, mit der WebView ausgeführt wird.
[TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion) | Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind.
[CoreWebView2EnvironmentOptions](#corewebview2environmentoptions) | Initialisiert eine neue Instanz der CoreWebView2EnvironmentOptions-Klasse.

Eine Standardimplementierung wird in WebView2EnvironmentOptions. h bereitgestellt.

## Member

#### AdditionalBrowserArguments 

AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern.

> public String [AdditionalBrowserArguments](#additionalbrowserarguments)

Diese werden als Teil der Befehlszeile an den Browserprozess übergeben. Weitere Informationen zu Befehlszeilen wechseln in den Browserprozess finden Sie unter [Ausführen von Chrom mit Flags](https://aka.ms/RunChromiumWithFlags) . Wenn die APP mit einem Befehlszeilen Schalter gestartet wird, `--edge-webview-switches=xxx` wird der Wert dieses Schalters (xxx im obigen Beispiel) auch an die Befehlszeile des Browser Prozesses angefügt. Bestimmte Schalter wie `--user-data-dir` sind intern und wichtig für WebView. Diese Schalter werden ignoriert, auch wenn Sie angegeben werden. Wenn dieselben Schalter mehrmals angegeben werden, gewinnt der letzte. Es wird nicht versucht, die verschiedenen Werte desselben Schalters zusammenzuführen, mit Ausnahme von deaktivierten und aktivierten Features. Die Features, die von `--enable-features` und `--disable-features` mit einfacher Logik zusammengeführt werden: die Features sind die Vereinigung der angegebenen Features und integrierten Features, und wenn ein Feature deaktiviert ist, wird es aus der Liste der aktivierten Features entfernt. Der Befehlszeilenwert des App-Prozesses `--edge-webview-switches` wird verarbeitet, nachdem der additionalBrowserArguments-Parameter verarbeitet wurde. Bestimmte Features sind intern deaktiviert und können nicht aktiviert werden. Wenn die Analyse bei den angegebenen Schaltern fehlgeschlagen ist, werden Sie ignoriert. Standardmäßig wird der Browserprozess ohne zusätzliche Flags ausgeführt.

#### AllowSingleSignOnUsingOSPrimaryAccount 

Die AllowSingleSignOnUsingOSPrimaryAccount-Eigenschaft wird verwendet, um die einmalige Anmeldung mit Azure Active Directory (AAD)-Ressourcen in WebView unter Verwendung des angemeldeten Windows-Kontos und des einmaligen Anmeldens bei Websites zu aktivieren, die das Microsoft-Konto verwenden, das mit dem Anmeldenamen im Windows-Konto verknüpft ist.

> public bool [AllowSingleSignOnUsingOSPrimaryAccount](#allowsinglesignonusingosprimaryaccount)

Standard ist deaktiviert. Universelle Windows-Plattform-apps müssen auch die [Eingeschränkte](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) enterpriseCloudSSO-Funktion für das einmalige Anmelden deklarieren.

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

> Public [CoreWebView2EnvironmentOptions](#corewebview2environmentoptions)(String additionalBrowserArguments, String Language, String targetCompatibleBrowserVersion, bool allowSingleSignOnUsingOSPrimaryAccount)

##### Parameter
* `additionalBrowserArguments` AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern. 

* `language` Die Standardsprache, mit der WebView ausgeführt wird. 

* `targetCompatibleBrowserVersion` Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind. 

* `allowSingleSignOnUsingOSPrimaryAccount` Auf "true" festlegen, wenn einmaliges Anmelden mit dem primären Betriebssystemkonto des Endbenutzers aktiviert werden soll. Standardwert ist false.

