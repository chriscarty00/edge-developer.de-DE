---
description: DateTime- und TimeSpan-Darstellungen in Windows Runtime
title: DateTime- und TimeSpan-Darstellungen in Windows Runtime
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime dates and times
- TimeSpan [JavaScript]
- DateTime [JavaScript]
ms.assetid: 9743e9ac-9054-463e-8264-427183e4905f
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1ee3d601e727601aba03f2ff7efa532171b8f815
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233864"
---
# <span data-ttu-id="f0e32-103">DateTime- und TimeSpan-Darstellungen in Windows-Runtime</span><span class="sxs-lookup"><span data-stu-id="f0e32-103">Windows Runtime DateTime and TimeSpan representations</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="f0e32-104">Die JavaScript-Darstellung von Datums-und Uhrzeitangaben unterscheidet sich von der Windows-Runtime-Version.</span><span class="sxs-lookup"><span data-stu-id="f0e32-104">The JavaScript representation of dates and times is different from the Windows Runtime version.</span></span>  <span data-ttu-id="f0e32-105">Die Windows-Runtime- [DateTime][UwpWindowsFoundationDatetime] -Struktur wird in JavaScript als ein [Datum][MDNDate] mit einem Sicherungsspeicher dargestellt, der den `DateTime` Daten entspricht \ (und hat einen anderen Bereich und eine andere Genauigkeit als JavaScript `Date` \).</span><span class="sxs-lookup"><span data-stu-id="f0e32-105">The Windows Runtime [DateTime][UwpWindowsFoundationDatetime] structure is represented in JavaScript as a [Date][MDNDate] that has a backing store that matches the `DateTime` data \(and has a different range and precision from the JavaScript `Date`\).</span></span>  <span data-ttu-id="f0e32-106">Wenn Sie dieses benutzerdefinierte `Date` Objekt ändern, wird es zu einem Standard `Date` -JavaScript und verliert die Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="f0e32-106">If you modify this custom `Date` object, it becomes a standard JavaScript `Date` and loses precision.</span></span>  <span data-ttu-id="f0e32-107">JavaScript `Date` -Werte können an eine Windows-Runtime übergeben werden `DateTime` und werden bereichsübergreifend überprüft, was zum Marshalling von Ausnahmen führen kann.</span><span class="sxs-lookup"><span data-stu-id="f0e32-107">JavaScript `Date` values can be passed to a Windows Runtime `DateTime` and will be range-checked, which might result in marshaling exceptions.</span></span>  

 <span data-ttu-id="f0e32-108">Die Windows-Runtime- [TimeSpan][UwpWindowsFoundationTimespan] -Struktur wird in Millisekunden konvertiert und als JavaScript-Zahl zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f0e32-108">The Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] structure is converted to milliseconds and returned as a JavaScript number.</span></span>  

## <span data-ttu-id="f0e32-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f0e32-109">See also</span></span>  

[<span data-ttu-id="f0e32-110">Verwenden der Windows-Runtime in JavaScript</span><span class="sxs-lookup"><span data-stu-id="f0e32-110">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Verwenden der Windows-Runtime in JavaScript | Microsoft docs"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "DateTime-Struktur | Microsoft docs"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "TimeSpan-Struktur | Microsoft docs"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Datum | MDN"  
