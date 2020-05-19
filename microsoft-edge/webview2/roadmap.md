---
description: Informieren Sie sich über die nächsten Schritte für WebView2
title: Roadmap für Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: bc55c5a731ab6cba8f9be15208029aad0ad5357a
ms.sourcegitcommit: a75e062b71831ea850c85287a8d7d7ce3b55ec84
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659744"
---
# Roadmap für Microsoft Edge-WebView2

##### Letzte Aktualisierung: Mai 2020

Das WebView2-Steuerelement ermöglicht Entwicklern das Einbetten von Webtechnologien in ihre systemeigenen Anwendungen. Dieses Dokument beschreibt den prospektiven Plan für WebView2. 

> [!NOTE]
> WebView2 steht unter aktiver Entwicklung, und die Roadmap wird weiterhin auf der Grundlage von Marktveränderungen und Kundenfeedback entwickelt, bitte beachten Sie, dass die hier dargelegten Pläne nicht erschöpfend sind und sich Änderungen unterwerfen können. 

Wenn Sie Bedenken oder Fragen zur Roadmap haben, hinterlassen Sie bitte Feedback im [Feedback-Repo](https://github.com/MicrosoftEdge/WebViewFeedback).

Das WebView2-Team hat einige große Anstrengungen im Gange:

1.  WebView2-Runtime-Installationsprogramm (Q4 2020)
2.  Feste Version (Q4 2020)
3.  Allgemeine Verfügbarkeit 
    *   Win32 C/C++ (Q4 2020)
    *   .Net (Q4 2020)
    *   [WinUI 3,0](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md)

## WebView2 Runtime & Installer

WebView2 [Evergreen](./concepts/distribution.md#microsoft-edge-webview2-runtime) -Verteilungsmodell ermöglicht es Ihnen, die WebView2-Laufzeit auf dem Computer Ihres Benutzers zu verwenden oder zu verketten. Es wird erwartet, dass in Q4 2020 eine Vorschau der WebView2-Laufzeit und des Installationsprogramms für Q3 2020 und GA verfügbar ist.

## Feste Version

Mit dem [festen](./concepts/distribution.md#roadmap) Verteilungsmodell von WebView2 können Sie die Microsoft Edge-Binärdateien in der systemeigenen Anwendung verpacken. Technische Arbeiten sind derzeit im Gange, mit einer Vorschau, die voraussichtlich gegen Ende des Q3 2020 und GA Q4 2020 bereit steht.

## Allgemeine Verfügbarkeit 

### Win32 C/C++

Das Win32 C/C++-SDK wird in Q4 2020, kurz nach der WebView2-Laufzeit und dem Installer GA, erwartet.

### .NET

Das .NET SDK umschließt das Win32 C/C++-SDK. Das .NET SDK wird in Kürze nach der Win32 C/C++ ga in Q4 2020 zu GA erwartet.

### WinUI 3,0

Sie können WebView2 zu UWP-Anwendungen über [Win UI 3,0](/uwp/toolkits/winui3/), derzeit in Alpha, führen. Checken Sie die [Windows-UI-Bibliothek-Roadmap](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md) aus, um auf dem neuesten Stand zu bleiben.  
