---
description: Stellt eine Benachrichtigungs Zeichenfolge dar, die von WebView-Inhalt an die Anwendung übergeben wird.
title: ScriptNotifyEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 22313f2d96ca2c5d4d3554ca40589b9a583c89cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566693"
---
# <span data-ttu-id="bbd79-104">ScriptNotifyEvent-Objekt</span><span class="sxs-lookup"><span data-stu-id="bbd79-104">ScriptNotifyEvent object</span></span>

<span data-ttu-id="bbd79-105">Ein Objekt, das ein Ereignis darstellt, das ausgelöst wird, wenn der Inhalt in der [WebView](../webview.md) eine Zeichenfolge mit JavaScript an die Anwendung übergibt.</span><span class="sxs-lookup"><span data-stu-id="bbd79-105">An object that represents an event fired when content contained in the [webview](../webview.md) passes a string to the application by using JavaScript.</span></span>

## <span data-ttu-id="bbd79-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bbd79-106">Properties</span></span>
    
### <span data-ttu-id="bbd79-107">callingUri</span><span class="sxs-lookup"><span data-stu-id="bbd79-107">callingUri</span></span>

<span data-ttu-id="bbd79-108">Ruft den Uniform Resource Identifier (URI) der Seite ab, die das Skript enthält, das das **ScriptNotifyEvent**ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="bbd79-108">Gets the Uniform Resource Identifier (URI) of the page containing the script that raised the **ScriptNotifyEvent**.</span></span>

<span data-ttu-id="bbd79-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bbd79-109">This property is read-only.</span></span>

```js
var callingUri = ScriptNotifyEvent.callingUri;
```

#### <span data-ttu-id="bbd79-110">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="bbd79-110">Property value</span></span>
<span data-ttu-id="bbd79-111">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="bbd79-111">Type: **DOMString**</span></span>

### <span data-ttu-id="bbd79-112">value</span><span class="sxs-lookup"><span data-stu-id="bbd79-112">value</span></span>

<span data-ttu-id="bbd79-113">Der Methodenname, der an die Anwendung übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="bbd79-113">The method name as passed to the application.</span></span>

<span data-ttu-id="bbd79-114">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bbd79-114">This property is read-only.</span></span>

```js
var value = ScriptNotifyEvent.value;
```

#### <span data-ttu-id="bbd79-115">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="bbd79-115">Property value</span></span>
<span data-ttu-id="bbd79-116">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="bbd79-116">Type: **DOMString**</span></span>