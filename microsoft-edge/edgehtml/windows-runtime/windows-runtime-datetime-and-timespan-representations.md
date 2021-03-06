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
# <a name="windows-runtime-datetime-and-timespan-representations"></a>DateTime- und TimeSpan-Darstellungen in Windows-Runtime  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Die JavaScript-Darstellung von Datums- und Zeitangaben ist anders als die Windows-Runtime-Version.  Die Windows-Runtime-DateTime-Struktur wird [][MDNDate] in JavaScript als Date dargestellt, der einen Sicherungsspeicher hat, der den Daten entspricht \(und einen anderen Bereich und eine andere Genauigkeit als [][UwpWindowsFoundationDatetime] `DateTime` JavaScript \ `Date` hat).  Wenn Sie dieses benutzerdefinierte Objekt `Date` ändern, wird es zu einem standardmäßigen JavaScript `Date` und verliert an Genauigkeit.  JavaScript-Werte können an eine Windows-Runtime übergeben werden und werden bereichsüberprüfungen, was zu `Date` `DateTime` Marshallausnahmen führen kann.  

Die [Windows-Runtime-TimeSpan-Struktur][UwpWindowsFoundationTimespan] wird in Millisekunden konvertiert und als JavaScript-Nummer zurückgegeben.  

## <a name="see-also"></a>Weitere Informationen  

[Verwenden der Windows-Runtime in JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Verwenden der Windows-Runtime in JavaScript-| Microsoft Docs"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "DateTime Struct | Microsoft Docs"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "TimeSpan Struct | Microsoft Docs"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Datum | MDN"  
