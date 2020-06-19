---
description: Stellt eine Benachrichtigungs Zeichenfolge dar, die von WebView-Inhalt an die Anwendung übergeben wird.
title: ScriptNotifyEvent-Objekt
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 164bfa7228b1f4ccf9817e4b7231361d090f1394
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752024"
---
# <span data-ttu-id="6e2cd-104">ScriptNotifyEvent-Objekt</span><span class="sxs-lookup"><span data-stu-id="6e2cd-104">ScriptNotifyEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="6e2cd-105">Ein Objekt, das ein Ereignis darstellt, das ausgelöst wird, wenn der Inhalt in der [WebView](../webview.md) eine Zeichenfolge mit JavaScript an die Anwendung übergibt.</span><span class="sxs-lookup"><span data-stu-id="6e2cd-105">An object that represents an event fired when content contained in the [webview](../webview.md) passes a string to the application by using JavaScript.</span></span>  

## <span data-ttu-id="6e2cd-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e2cd-106">Properties</span></span>  

### <span data-ttu-id="6e2cd-107">callingUri</span><span class="sxs-lookup"><span data-stu-id="6e2cd-107">callingUri</span></span>  

<span data-ttu-id="6e2cd-108">Ruft den Uniform Resource Identifier (URI) der Seite ab, die das Skript enthält, das das **ScriptNotifyEvent**ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="6e2cd-108">Gets the Uniform Resource Identifier (URI) of the page containing the script that raised the **ScriptNotifyEvent**.</span></span>  

<span data-ttu-id="6e2cd-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6e2cd-109">This property is read-only.</span></span>  

```javascript
var callingUri = ScriptNotifyEvent.callingUri;
```  

#### <span data-ttu-id="6e2cd-110">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="6e2cd-110">Property value</span></span>  

<span data-ttu-id="6e2cd-111">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="6e2cd-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="6e2cd-112">value</span><span class="sxs-lookup"><span data-stu-id="6e2cd-112">value</span></span>  

<span data-ttu-id="6e2cd-113">Der Methodenname, der an die Anwendung übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6e2cd-113">The method name as passed to the application.</span></span>  

<span data-ttu-id="6e2cd-114">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6e2cd-114">This property is read-only.</span></span>  

```javascript
var value = ScriptNotifyEvent.value;
```  

#### <span data-ttu-id="6e2cd-115">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="6e2cd-115">Property value</span></span>  

<span data-ttu-id="6e2cd-116">Geben Sie Folgendes ein: **DOM**</span><span class="sxs-lookup"><span data-stu-id="6e2cd-116">Type: **DOMString**</span></span>  
