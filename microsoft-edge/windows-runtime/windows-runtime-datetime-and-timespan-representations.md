---
title: Windows-Runtime-DateTime-und TimeSpan-Darstellungen
ms.custom: ''
ms.date: 04/01/2020
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
ms.openlocfilehash: d3e138493b80face1238118a99c03f6015a6a8ef
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568708"
---
# Windows-Runtime-DateTime-und TimeSpan-Darstellungen  

Die JavaScript-Darstellung von Datums-und Uhrzeitangaben unterscheidet sich von der Windows-Runtime-Version.  Die Windows-Runtime- [DateTime][UwpWindowsFoundationDatetime] -Struktur wird in JavaScript als ein [Datum][MDNDate] mit einem Sicherungsspeicher dargestellt, der den `DateTime` Daten entspricht \ (und hat einen anderen Bereich und eine andere Genauigkeit als JavaScript `Date` \).  Wenn Sie dieses benutzerdefinierte `Date` Objekt ändern, wird es zu einem Standard `Date` -JavaScript und verliert die Genauigkeit.  JavaScript `Date` -Werte können an eine Windows-Runtime übergeben werden `DateTime` und werden bereichsübergreifend überprüft, was zum Marshalling von Ausnahmen führen kann.  

 Die Windows-Runtime- [TimeSpan][UwpWindowsFoundationTimespan] -Struktur wird in Millisekunden konvertiert und als JavaScript-Zahl zurückgegeben.  

## Weitere Informationen  

[Verwenden der Windows-Runtime in JavaScript][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Verwenden der Windows-Runtime in JavaScript"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "DateTime-Struktur"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "TimeSpan-Struktur"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Datum | MDN"  
