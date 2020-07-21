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
# <span data-ttu-id="d660c-104">Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties Klasse</span><span class="sxs-lookup"><span data-stu-id="d660c-104">Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties class</span></span> 

<span data-ttu-id="d660c-105">Namespace: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="d660c-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="d660c-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span><span class="sxs-lookup"><span data-stu-id="d660c-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties
  : public DependencyObject
```

<span data-ttu-id="d660c-107">Diese Klasse ist ein Bündel der am häufigsten verwendeten Parameter zum Erstellen eines CoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="d660c-107">This class is a bundle of the most common parameters used to create a CoreWebView2Environment.</span></span>

## <span data-ttu-id="d660c-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d660c-108">Summary</span></span>

 <span data-ttu-id="d660c-109">Member</span><span class="sxs-lookup"><span data-stu-id="d660c-109">Members</span></span>                        | <span data-ttu-id="d660c-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d660c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d660c-111">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="d660c-111">BrowserExecutableFolder</span></span>](#browserexecutablefolder) | <span data-ttu-id="d660c-112">Ruft den Wert ab, der als browserExecutableFolder-Parameter von CoreWebView2Environment. createasync übergeben wird, wenn eine Umgebung mit dieser Instanz erstellt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="d660c-112">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="d660c-113">Sprache</span><span class="sxs-lookup"><span data-stu-id="d660c-113">Language</span></span>](#language) | <span data-ttu-id="d660c-114">Ruft den Wert ab, der für die Language-Eigenschaft des CoreWebView2EnvironmentOptions-Parameters verwendet wird, der an CoreWebView2Environment. createasync übergeben wird, wenn eine Umgebung mit dieser Instanz erstellt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="d660c-114">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="d660c-115">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="d660c-115">UserDataFolder</span></span>](#userdatafolder) | <span data-ttu-id="d660c-116">Ruft den Wert ab, der als userDataFolder-Parameter von CoreWebView2Environment. createasync übergeben wird, wenn eine Umgebung mit dieser Instanz erstellt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="d660c-116">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="d660c-117">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="d660c-117">CoreWebView2CreationProperties</span></span>](#corewebview2creationproperties) | <span data-ttu-id="d660c-118">Erstellt eine neue Instanz von CoreWebView2CreationProperties mit Standarddaten für alle Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d660c-118">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

<span data-ttu-id="d660c-119">Sein Hauptziel ist die Einstellung auf [WebView2. CreationProperties](microsoft-web-webview2-wpf-webview2.md) , um die von einem [WebView2](microsoft-web-webview2-wpf-webview2.md) während der impliziten Initialisierung verwendete Umgebung anzupassen.</span><span class="sxs-lookup"><span data-stu-id="d660c-119">Its main purpose is to be set to [WebView2.CreationProperties](microsoft-web-webview2-wpf-webview2.md) in order to customize the environment used by a [WebView2](microsoft-web-webview2-wpf-webview2.md) during implicit initialization.</span></span> <span data-ttu-id="d660c-120">Außerdem handelt es sich um ein nettes WPF-Integrations Dienstprogramm, mit dem häufig verwendete Umgebungsparameter Abhängigkeitseigenschaften aufweisen und im Markup erstellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="d660c-120">It is also a nice WPF integration utility which allows commonly used environment parameters to be dependency properties and be created and used in markup.</span></span>

<span data-ttu-id="d660c-121">Diese Klasse soll nicht alle möglichen Optionen für die umgebungsanpassung enthalten.</span><span class="sxs-lookup"><span data-stu-id="d660c-121">This class isn't intended to contain all possible environment customization options.</span></span> <span data-ttu-id="d660c-122">Wenn Sie die vollständige Kontrolle über die Umgebung benötigen, die von einem WebView2-Steuerelement verwendet wird, müssen Sie das Steuerelement explizit initialisieren, indem Sie eine eigene Umgebung mit CoreWebView2Environment. createasync erstellen und an [WebView2. EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)übergeben,*bevor* Sie die [WebView2. Source](microsoft-web-webview2-wpf-webview2.md) -Eigenschaft auf einen beliebigen Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="d660c-122">If you need complete control over the environment used by a WebView2 control then you'll need to initialize the control explicitly by creating your own environment with CoreWebView2Environment.CreateAsync and passing it to [WebView2.EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*before* you set the [WebView2.Source](microsoft-web-webview2-wpf-webview2.md) property to anything.</span></span> <span data-ttu-id="d660c-123">Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur [WebView2](microsoft-web-webview2-wpf-webview2.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="d660c-123">See the [WebView2](microsoft-web-webview2-wpf-webview2.md) class documentation for an initialization overview.</span></span>

## <span data-ttu-id="d660c-124">Member</span><span class="sxs-lookup"><span data-stu-id="d660c-124">Members</span></span>

#### <span data-ttu-id="d660c-125">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="d660c-125">BrowserExecutableFolder</span></span> 

<span data-ttu-id="d660c-126">Ruft den Wert ab, der als browserExecutableFolder-Parameter von CoreWebView2Environment. createasync übergeben wird, wenn eine Umgebung mit dieser Instanz erstellt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="d660c-126">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="d660c-127">public String [BrowserExecutableFolder](#browserexecutablefolder)</span><span class="sxs-lookup"><span data-stu-id="d660c-127">public string [BrowserExecutableFolder](#browserexecutablefolder)</span></span>

#### <span data-ttu-id="d660c-128">Sprache</span><span class="sxs-lookup"><span data-stu-id="d660c-128">Language</span></span> 

<span data-ttu-id="d660c-129">Ruft den Wert ab, der für die Language-Eigenschaft des CoreWebView2EnvironmentOptions-Parameters verwendet wird, der an CoreWebView2Environment. createasync übergeben wird, wenn eine Umgebung mit dieser Instanz erstellt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="d660c-129">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="d660c-130">öffentliche Zeichenfolgen [Sprache](#language)</span><span class="sxs-lookup"><span data-stu-id="d660c-130">public string [Language](#language)</span></span>

#### <span data-ttu-id="d660c-131">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="d660c-131">UserDataFolder</span></span> 

<span data-ttu-id="d660c-132">Ruft den Wert ab, der als userDataFolder-Parameter von CoreWebView2Environment. createasync übergeben wird, wenn eine Umgebung mit dieser Instanz erstellt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="d660c-132">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="d660c-133">public String [UserDataFolder](#userdatafolder)</span><span class="sxs-lookup"><span data-stu-id="d660c-133">public string [UserDataFolder](#userdatafolder)</span></span>

#### <span data-ttu-id="d660c-134">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="d660c-134">CoreWebView2CreationProperties</span></span> 

<span data-ttu-id="d660c-135">Erstellt eine neue Instanz von CoreWebView2CreationProperties mit Standarddaten für alle Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d660c-135">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

> <span data-ttu-id="d660c-136">Public [CoreWebView2CreationProperties](#corewebview2creationproperties)()</span><span class="sxs-lookup"><span data-stu-id="d660c-136">public [CoreWebView2CreationProperties](#corewebview2creationproperties)()</span></span>

