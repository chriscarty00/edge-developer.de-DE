---
description: Stellt einen WebView-Prozess dar.
title: MSWebViewProcess-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 7581f6da3a23295180c50f6d41cc282ce998b64e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567169"
---
# <span data-ttu-id="bac1a-104">MSWebViewProcess-Objekt</span><span class="sxs-lookup"><span data-stu-id="bac1a-104">MSWebViewProcess object</span></span>

<span data-ttu-id="bac1a-105">Stellt einen [WebView](../webview.md) -Prozess dar.</span><span class="sxs-lookup"><span data-stu-id="bac1a-105">Represents a [webview](../webview.md) process.</span></span>

```js
var wvprocess = new MSWebViewProcess();
```

## <span data-ttu-id="bac1a-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bac1a-106">Properties</span></span>

### <span data-ttu-id="bac1a-107">Enterprise-Nr</span><span class="sxs-lookup"><span data-stu-id="bac1a-107">enterpriseId</span></span>

<span data-ttu-id="bac1a-108">Die Enterprise-ID des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="bac1a-108">The enterprise ID of the process.</span></span>

```js
var enterpriseId = wvprocess.enterpriseId;
```

<span data-ttu-id="bac1a-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bac1a-109">This property is read-only.</span></span>

#### <span data-ttu-id="bac1a-110">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="bac1a-110">Property value</span></span>
<span data-ttu-id="bac1a-111">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="bac1a-111">Type: **DOMString**</span></span>

### <span data-ttu-id="bac1a-112">isPrivateNetworkClientServerCapabilityEnabled</span><span class="sxs-lookup"><span data-stu-id="bac1a-112">isPrivateNetworkClientServerCapabilityEnabled</span></span>

<span data-ttu-id="bac1a-113">Ruft einen Wert ab, der angibt, ob der [WebView](../webview.md) -Prozess im App-Manifest die Funktion für die universelle Windows- [App-Funktionsdeklaration](/windows/uwp/packaging/app-capability-declarations) für *private Netzwerke (Client & Server)* aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="bac1a-113">Gets a value indicating whether the [webview](../webview.md) process has the *Private Networks (Client & Server)* Universal Windows [App capability declaration](/windows/uwp/packaging/app-capability-declarations) enabled in the app manifest.</span></span>

```js
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```

<span data-ttu-id="bac1a-114">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bac1a-114">This property is read-only.</span></span>

#### <span data-ttu-id="bac1a-115">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="bac1a-115">Property value</span></span>
<span data-ttu-id="bac1a-116">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="bac1a-116">Type: **Boolean**</span></span>

## <span data-ttu-id="bac1a-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="bac1a-117">Methods</span></span>

### <span data-ttu-id="bac1a-118">CreateWebViewAsync</span><span class="sxs-lookup"><span data-stu-id="bac1a-118">CreateWebViewAsync</span></span>

<span data-ttu-id="bac1a-119">Erstellt eine [WebView](../webview.md) in einem bestimmten Prozess.</span><span class="sxs-lookup"><span data-stu-id="bac1a-119">Creates a [webview](../webview.md) in a specific process.</span></span>

```js
wvprocess.createWebviewAsync();
```

#### <span data-ttu-id="bac1a-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bac1a-120">Return value</span></span>

<span data-ttu-id="bac1a-121">Geben**`Promise<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="bac1a-121">Type: **`Promise<MSHTMLWebViewElement>`**</span></span>

### <span data-ttu-id="bac1a-122">Webviews</span><span class="sxs-lookup"><span data-stu-id="bac1a-122">GetWebViews</span></span>

<span data-ttu-id="bac1a-123">Gibt eine Sequenz von **MSWebViewProcess** -Objekten zurück, die innerhalb des Prozesses gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="bac1a-123">Returns a sequence of **MSWebViewProcess** objects hosted within the process.</span></span>

#### <span data-ttu-id="bac1a-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bac1a-124">Return value</span></span>

<span data-ttu-id="bac1a-125">Geben**`sequence<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="bac1a-125">Type: **`sequence<MSHTMLWebViewElement>`**</span></span>

### <span data-ttu-id="bac1a-126">Beenden</span><span class="sxs-lookup"><span data-stu-id="bac1a-126">Terminate</span></span>

<span data-ttu-id="bac1a-127">Beendet den Prozess.</span><span class="sxs-lookup"><span data-stu-id="bac1a-127">Terminates the process.</span></span>

```js
wvprocess.terminate();
```

#### <span data-ttu-id="bac1a-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bac1a-128">Return value</span></span>

<span data-ttu-id="bac1a-129">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bac1a-129">This method does not return a value.</span></span>
