---
description: DateTime- und TimeSpan-Darstellungen in Windows Runtime
title: DateTime- und TimeSpan-Darstellungen in Windows Runtime
ms.custom: ''
ms.date: 11/03/2020
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
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c2627826755f041a440112c3390ecb17d1f703ce
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398126"
---
# <a name="windows-runtime-datetime-and-timespan-representations"></a><span data-ttu-id="f875b-103">DateTime- und TimeSpan-Darstellungen in Windows-Runtime</span><span class="sxs-lookup"><span data-stu-id="f875b-103">Windows Runtime DateTime and TimeSpan representations</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="f875b-104">Die JavaScript-Darstellung von Datums- und Zeitangaben ist anders als die Windows-Runtime-Version.</span><span class="sxs-lookup"><span data-stu-id="f875b-104">The JavaScript representation of dates and times is different from the Windows Runtime version.</span></span>  <span data-ttu-id="f875b-105">Die Windows-Runtime-DateTime-Struktur wird [][MDNDate] in JavaScript als Date dargestellt, der einen Sicherungsspeicher hat, der den Daten entspricht \(und einen anderen Bereich und eine andere Genauigkeit als [][UwpWindowsFoundationDatetime] `DateTime` JavaScript \ `Date` hat).</span><span class="sxs-lookup"><span data-stu-id="f875b-105">The Windows Runtime [DateTime][UwpWindowsFoundationDatetime] structure is represented in JavaScript as a [Date][MDNDate] that has a backing store that matches the `DateTime` data \(and has a different range and precision from the JavaScript `Date`\).</span></span>  <span data-ttu-id="f875b-106">Wenn Sie dieses benutzerdefinierte Objekt `Date` ändern, wird es zu einem standardmäßigen JavaScript `Date` und verliert an Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="f875b-106">If you modify this custom `Date` object, it becomes a standard JavaScript `Date` and loses precision.</span></span>  <span data-ttu-id="f875b-107">JavaScript-Werte können an eine Windows-Runtime übergeben werden und werden bereichsüberprüfungen, was zu `Date` `DateTime` Marshallausnahmen führen kann.</span><span class="sxs-lookup"><span data-stu-id="f875b-107">JavaScript `Date` values can be passed to a Windows Runtime `DateTime` and will be range-checked, which might result in marshaling exceptions.</span></span>  

<span data-ttu-id="f875b-108">Die [Windows-Runtime-TimeSpan-Struktur][UwpWindowsFoundationTimespan] wird in Millisekunden konvertiert und als JavaScript-Nummer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f875b-108">The Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] structure is converted to milliseconds and returned as a JavaScript number.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f875b-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f875b-109">See also</span></span>  

[<span data-ttu-id="f875b-110">Verwenden der Windows-Runtime in JavaScript</span><span class="sxs-lookup"><span data-stu-id="f875b-110">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Verwenden der Windows-Runtime in JavaScript-| Microsoft Docs"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "DateTime Struct | Microsoft Docs"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "TimeSpan Struct | Microsoft Docs"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Datum | MDN"  
