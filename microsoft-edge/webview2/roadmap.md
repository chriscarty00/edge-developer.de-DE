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
ms.openlocfilehash: dcc9a92ee4db4c41a024aee565dfafe22b185e2a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698176"
---
# <span data-ttu-id="12475-104">Roadmap für Microsoft Edge-WebView2</span><span class="sxs-lookup"><span data-stu-id="12475-104">Microsoft Edge WebView2 roadmap</span></span>

##### <span data-ttu-id="12475-105">Letzte Aktualisierung: Mai 2020</span><span class="sxs-lookup"><span data-stu-id="12475-105">Last Updated: May 2020</span></span>

<span data-ttu-id="12475-106">Das WebView2-Steuerelement ermöglicht Entwicklern das Einbetten von Webtechnologien in ihre systemeigenen Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="12475-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span> <span data-ttu-id="12475-107">Dieses Dokument beschreibt den prospektiven Plan für WebView2.</span><span class="sxs-lookup"><span data-stu-id="12475-107">This document outlines the prospective roadmap for WebView2.</span></span> 

> [!NOTE]
> <span data-ttu-id="12475-108">WebView2 steht unter aktiver Entwicklung, und die Roadmap wird weiterhin auf der Grundlage von Marktveränderungen und Kundenfeedback entwickelt, bitte beachten Sie, dass die hier dargelegten Pläne nicht erschöpfend sind und sich Änderungen unterwerfen können.</span><span class="sxs-lookup"><span data-stu-id="12475-108">WebView2 is under active development and the roadmap will continue to evolve based on market changes and customer feedback, so please note that the plans outlined here aren't exhaustive and are subject to change.</span></span> 

<span data-ttu-id="12475-109">Wenn Sie Bedenken oder Fragen zur Roadmap haben, hinterlassen Sie bitte Feedback im [Feedback-Repo](https://github.com/MicrosoftEdge/WebViewFeedback).</span><span class="sxs-lookup"><span data-stu-id="12475-109">If you have concerns or questions about the Roadmap, please leave feedback in the [feedback repo](https://github.com/MicrosoftEdge/WebViewFeedback).</span></span>

<span data-ttu-id="12475-110">Das WebView2-Team hat einige große Anstrengungen im Gange:</span><span class="sxs-lookup"><span data-stu-id="12475-110">The WebView2 team has a few major efforts underway:</span></span>

1.  <span data-ttu-id="12475-111">WebView2-Runtime-Installationsprogramm (Q4 2020)</span><span class="sxs-lookup"><span data-stu-id="12475-111">WebView2 Runtime Installer (Q4 2020)</span></span>
2.  <span data-ttu-id="12475-112">Feste Version (Q4 2020)</span><span class="sxs-lookup"><span data-stu-id="12475-112">Fixed Version (Q4 2020)</span></span>
3.  <span data-ttu-id="12475-113">Allgemeine Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="12475-113">General Availability</span></span> 
    *   <span data-ttu-id="12475-114">Win32 C/C++ (Q4 2020)</span><span class="sxs-lookup"><span data-stu-id="12475-114">Win32 C/C++ (Q4 2020)</span></span>
    *   <span data-ttu-id="12475-115">.Net (Q4 2020)</span><span class="sxs-lookup"><span data-stu-id="12475-115">.NET (Q4 2020)</span></span>
    *   [<span data-ttu-id="12475-116">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="12475-116">WinUI 3.0</span></span>](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md)

## <span data-ttu-id="12475-117">WebView2 Runtime & Installer</span><span class="sxs-lookup"><span data-stu-id="12475-117">WebView2 Runtime & Installer</span></span>

<span data-ttu-id="12475-118">WebView2 [Evergreen](./concepts/distribution.md#microsoft-edge-webview2-runtime) -Verteilungsmodell ermöglicht es Ihnen, die WebView2-Laufzeit auf dem Computer Ihres Benutzers zu verwenden oder zu verketten.</span><span class="sxs-lookup"><span data-stu-id="12475-118">WebView2 [Evergreen](./concepts/distribution.md#microsoft-edge-webview2-runtime) distribution model will allow you to target or chain install the WebView2 Runtime onto your user's machine.</span></span> <span data-ttu-id="12475-119">Es wird erwartet, dass in Q4 2020 eine Vorschau der WebView2-Laufzeit und des Installationsprogramms für Q3 2020 und GA verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="12475-119">A preview of the WebView2 Runtime and installer is expected to be available Q3 2020 and GA in Q4 2020.</span></span>

## <span data-ttu-id="12475-120">Feste Version</span><span class="sxs-lookup"><span data-stu-id="12475-120">Fixed version</span></span>

<span data-ttu-id="12475-121">Mit dem [festen](./concepts/distribution.md#roadmap) Verteilungsmodell von WebView2 können Sie die Microsoft Edge-Binärdateien in der systemeigenen Anwendung verpacken.</span><span class="sxs-lookup"><span data-stu-id="12475-121">WebView2 [Fixed](./concepts/distribution.md#roadmap) distribution model allows you to package the Microsoft Edge binaries inside your native application.</span></span> <span data-ttu-id="12475-122">Technische Arbeiten sind derzeit im Gange, mit einer Vorschau, die voraussichtlich gegen Ende des Q3 2020 und GA Q4 2020 bereit steht.</span><span class="sxs-lookup"><span data-stu-id="12475-122">Engineering work is currently under way with a preview anticipated to be ready towards the end of  Q3 2020 and GA Q4 2020.</span></span>

## <span data-ttu-id="12475-123">Allgemeine Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="12475-123">General availability</span></span> 

### <span data-ttu-id="12475-124">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="12475-124">Win32 C/C++</span></span>

<span data-ttu-id="12475-125">Das Win32 C/C++-SDK wird in Q4 2020, kurz nach der WebView2-Laufzeit und dem Installer GA, erwartet.</span><span class="sxs-lookup"><span data-stu-id="12475-125">The Win32 C/C++ SDK is expected to GA in Q4 2020, shortly after the WebView2 Runtime and installer GA.</span></span>

### <span data-ttu-id="12475-126">.NET</span><span class="sxs-lookup"><span data-stu-id="12475-126">.NET</span></span>

<span data-ttu-id="12475-127">Das .NET SDK umschließt das Win32 C/C++-SDK.</span><span class="sxs-lookup"><span data-stu-id="12475-127">The .NET SDK wraps the Win32 C/C++ SDK.</span></span> <span data-ttu-id="12475-128">Das .NET SDK wird in Kürze nach der Win32 C/C++ ga in Q4 2020 zu GA erwartet.</span><span class="sxs-lookup"><span data-stu-id="12475-128">The .NET SDK is expected to GA shortly after the Win32 C/C++ GA in Q4 2020.</span></span>

### <span data-ttu-id="12475-129">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="12475-129">WinUI 3.0</span></span>

<span data-ttu-id="12475-130">Sie können WebView2 zu UWP-Anwendungen über [Win UI 3,0](/uwp/toolkits/winui3/), derzeit in Alpha, führen.</span><span class="sxs-lookup"><span data-stu-id="12475-130">You can bring WebView2 to UWP applications through [Win UI 3.0](/uwp/toolkits/winui3/), currently in alpha.</span></span> <span data-ttu-id="12475-131">Checken Sie die [Windows-UI-Bibliothek-Roadmap](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md) aus, um auf dem neuesten Stand zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="12475-131">Checkout the [Windows UI Library Roadmap](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md) to keep up to date.</span></span>  
