---
title: DateTime- und TimeSpan-Darstellungen in Windows Runtime
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime dates and times
- TimeSpan [JavaScript]
- DateTime [JavaScript]
ms.assetid: 9743e9ac-9054-463e-8264-427183e4905f
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1c51bba74bb7e5182eb25342badcae848eeba339
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942056"
---
# <span data-ttu-id="4a22c-102">Windows-Runtime-DateTime-und TimeSpan-Darstellungen</span><span class="sxs-lookup"><span data-stu-id="4a22c-102">Windows Runtime DateTime and TimeSpan representations</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="4a22c-103">Die JavaScript-Darstellung von Datums-und Uhrzeitangaben unterscheidet sich von der Windows-Runtime-Version.</span><span class="sxs-lookup"><span data-stu-id="4a22c-103">The JavaScript representation of dates and times is different from the Windows Runtime version.</span></span>  <span data-ttu-id="4a22c-104">Die Windows-Runtime- [DateTime][UwpWindowsFoundationDatetime] -Struktur wird in JavaScript als ein [Datum][MDNDate] mit einem Sicherungsspeicher dargestellt, der den `DateTime` Daten entspricht \ (und hat einen anderen Bereich und eine andere Genauigkeit als JavaScript `Date` \).</span><span class="sxs-lookup"><span data-stu-id="4a22c-104">The Windows Runtime [DateTime][UwpWindowsFoundationDatetime] structure is represented in JavaScript as a [Date][MDNDate] that has a backing store that matches the `DateTime` data \(and has a different range and precision from the JavaScript `Date`\).</span></span>  <span data-ttu-id="4a22c-105">Wenn Sie dieses benutzerdefinierte `Date` Objekt ändern, wird es zu einem Standard `Date` -JavaScript und verliert die Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="4a22c-105">If you modify this custom `Date` object, it becomes a standard JavaScript `Date` and loses precision.</span></span>  <span data-ttu-id="4a22c-106">JavaScript `Date` -Werte können an eine Windows-Runtime übergeben werden `DateTime` und werden bereichsübergreifend überprüft, was zum Marshalling von Ausnahmen führen kann.</span><span class="sxs-lookup"><span data-stu-id="4a22c-106">JavaScript `Date` values can be passed to a Windows Runtime `DateTime` and will be range-checked, which might result in marshaling exceptions.</span></span>  

 <span data-ttu-id="4a22c-107">Die Windows-Runtime- [TimeSpan][UwpWindowsFoundationTimespan] -Struktur wird in Millisekunden konvertiert und als JavaScript-Zahl zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4a22c-107">The Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] structure is converted to milliseconds and returned as a JavaScript number.</span></span>  

## <span data-ttu-id="4a22c-108">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4a22c-108">See also</span></span>  

[<span data-ttu-id="4a22c-109">Verwenden der Windows-Runtime in JavaScript</span><span class="sxs-lookup"><span data-stu-id="4a22c-109">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Verwenden der Windows-Runtime in JavaScript | Microsoft docs"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "DateTime-Struktur | Microsoft docs"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "TimeSpan-Struktur | Microsoft docs"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Datum | MDN"  
