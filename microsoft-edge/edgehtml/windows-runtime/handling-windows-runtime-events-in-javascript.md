---
description: Behandeln von Windows-Runtime-Ereignissen in JavaScript
title: Behandeln von Windows-Runtime-Ereignissen in JavaScript
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime events
- Windows Runtime events [JavaScript]
ms.assetid: d9436aff-2c30-4846-b8df-eaa3e63fd75c
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 08562f7ebff0c02b96bfc8229238a62463b95451
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397524"
---
# <a name="handling-windows-runtime-events-in-javascript"></a>Windows-Runtime-Ereignissen in JavaScript behandeln  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Windows-Runtime-Ereignisse werden in JavaScript nicht auf die gleiche Weise dargestellt wie in C++ oder .NET Framework.  Sie sind keine Klasseneigenschaften, sondern werden als \(Kleinbuchstabe\)-Zeichenfolgenbezeichner dargestellt, die an die Methoden und Methoden der `addEventListener` Klasse übergeben `removeEventListener` werden.  Sie können beispielsweise einen Ereignishandler für das [Geolocator.PositionChanged-Ereignis][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] hinzufügen, indem Sie die Zeichenfolge an `positionchanged` die -Methode `Geolocator.addEventListener` übergeben:  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

Sie können auch die Eigenschaft `locator.onpositionchanged` festlegen:  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

Ein weiterer Unterschied zwischen .NET/C++ und JavaScript ist die Anzahl der Parameter, die von einem Ereignishandler verwendet werden.  In .NET/C++ benötigt ein Handler zwei: den Ereignisabsender und die Ereignisdaten.  In JavaScript werden die beiden als einzelnes Objekt `Event` gebündelt.  Im folgenden Beispiel enthält der Parameter sowohl den Absender des Ereignisses \(die Eigenschaft\) als auch die Ereignisdateneigenschaften `ev` `target` \(hier, nur `position` \).  Die Ereignisdateneigenschaften sind die Eigenschaften, die für jedes Ereignis dokumentiert sind.  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> Windows-Runtime-Features sind für Apps, die in Internet Explorer ausgeführt werden, nicht verfügbar.  

## <a name="see-also"></a>Weitere Informationen  

[Verwenden der Windows-Runtime in JavaScript][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Verwenden der Windows-Runtime in JavaScript-| Microsoft Docs"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Geolocator-Klasse | Microsoft Docs"  
