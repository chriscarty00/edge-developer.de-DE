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
# Windows-Runtime-DateTime-und TimeSpan-Darstellungen  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Die JavaScript-Darstellung von Datums-und Uhrzeitangaben unterscheidet sich von der Windows-Runtime-Version.  Die Windows-Runtime- [DateTime][UwpWindowsFoundationDatetime] -Struktur wird in JavaScript als ein [Datum][MDNDate] mit einem Sicherungsspeicher dargestellt, der den `DateTime` Daten entspricht \ (und hat einen anderen Bereich und eine andere Genauigkeit als JavaScript `Date` \).  Wenn Sie dieses benutzerdefinierte `Date` Objekt ändern, wird es zu einem Standard `Date` -JavaScript und verliert die Genauigkeit.  JavaScript `Date` -Werte können an eine Windows-Runtime übergeben werden `DateTime` und werden bereichsübergreifend überprüft, was zum Marshalling von Ausnahmen führen kann.  

 Die Windows-Runtime- [TimeSpan][UwpWindowsFoundationTimespan] -Struktur wird in Millisekunden konvertiert und als JavaScript-Zahl zurückgegeben.  

## Weitere Informationen  

[Verwenden der Windows-Runtime in JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Verwenden der Windows-Runtime in JavaScript | Microsoft docs"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "DateTime-Struktur | Microsoft docs"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "TimeSpan-Struktur | Microsoft docs"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Datum | MDN"  
