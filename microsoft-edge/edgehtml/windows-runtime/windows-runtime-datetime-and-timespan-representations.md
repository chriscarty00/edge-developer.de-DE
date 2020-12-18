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
# DateTime- und TimeSpan-Darstellungen in Windows-Runtime  

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
