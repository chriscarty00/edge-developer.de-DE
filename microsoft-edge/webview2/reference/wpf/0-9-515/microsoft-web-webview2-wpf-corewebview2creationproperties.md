---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/17/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
ms.openlocfilehash: 04c80d3319c74d3461666b6f35fadd0481b45207
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885534"
---
# Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties Klasse 

Namespace: Microsoft. Web. WebView2. WPF \
Assembly: Microsoft.Web.WebView2.Wpf.dll

```
class Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties
  : public DependencyObject
```

Diese Klasse ist ein Bündel der am häufigsten verwendeten Parameter zum Erstellen eines CoreWebView2Environment.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[BrowserExecutableFolder](#browserexecutablefolder) | Ruft den Wert ab, der als browserExecutableFolder-Parameter von CoreWebView2Environment. createasync übergeben wird, wenn eine Umgebung mit dieser Instanz erstellt wird, oder legt diesen fest.
[Sprache](#language) | Ruft den Wert ab, der für die Language-Eigenschaft des CoreWebView2EnvironmentOptions-Parameters verwendet wird, der an CoreWebView2Environment. createasync übergeben wird, wenn eine Umgebung mit dieser Instanz erstellt wird, oder legt diesen fest.
[UserDataFolder](#userdatafolder) | Ruft den Wert ab, der als userDataFolder-Parameter von CoreWebView2Environment. createasync übergeben wird, wenn eine Umgebung mit dieser Instanz erstellt wird, oder legt diesen fest.
[CoreWebView2CreationProperties](#corewebview2creationproperties) | Erstellt eine neue Instanz von CoreWebView2CreationProperties mit Standarddaten für alle Eigenschaften.

Sein Hauptziel ist die Einstellung auf [WebView2. CreationProperties](microsoft-web-webview2-wpf-webview2.md) , um die von einem [WebView2](microsoft-web-webview2-wpf-webview2.md) während der impliziten Initialisierung verwendete Umgebung anzupassen. Außerdem handelt es sich um ein nettes WPF-Integrations Dienstprogramm, mit dem häufig verwendete Umgebungsparameter Abhängigkeitseigenschaften aufweisen und im Markup erstellt und verwendet werden können.

Diese Klasse soll nicht alle möglichen Optionen für die umgebungsanpassung enthalten. Wenn Sie die vollständige Kontrolle über die Umgebung benötigen, die von einem WebView2-Steuerelement verwendet wird, müssen Sie das Steuerelement explizit initialisieren, indem Sie eine eigene Umgebung mit CoreWebView2Environment. createasync erstellen und an [WebView2. EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)übergeben,*bevor* Sie die [WebView2. Source](microsoft-web-webview2-wpf-webview2.md) -Eigenschaft auf einen beliebigen Wert festlegen. Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur [WebView2](microsoft-web-webview2-wpf-webview2.md) -Klasse.

## Member

#### BrowserExecutableFolder 

Ruft den Wert ab, der als browserExecutableFolder-Parameter von CoreWebView2Environment. createasync übergeben wird, wenn eine Umgebung mit dieser Instanz erstellt wird, oder legt diesen fest.

> public String [BrowserExecutableFolder](#browserexecutablefolder)

#### Sprache 

Ruft den Wert ab, der für die Language-Eigenschaft des CoreWebView2EnvironmentOptions-Parameters verwendet wird, der an CoreWebView2Environment. createasync übergeben wird, wenn eine Umgebung mit dieser Instanz erstellt wird, oder legt diesen fest.

> öffentliche Zeichenfolgen [Sprache](#language)

#### UserDataFolder 

Ruft den Wert ab, der als userDataFolder-Parameter von CoreWebView2Environment. createasync übergeben wird, wenn eine Umgebung mit dieser Instanz erstellt wird, oder legt diesen fest.

> public String [UserDataFolder](#userdatafolder)

#### CoreWebView2CreationProperties 

Erstellt eine neue Instanz von CoreWebView2CreationProperties mit Standarddaten für alle Eigenschaften.

> Public [CoreWebView2CreationProperties](#corewebview2creationproperties)()

