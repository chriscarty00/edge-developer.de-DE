---
title: Behandeln von Windows-Runtime-Ereignissen in JavaScript
ms.custom: ''
ms.date: 04/01/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime events
- Windows Runtime events [JavaScript]
ms.assetid: d9436aff-2c30-4846-b8df-eaa3e63fd75c
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c3db0116a3d464c75fe754e73e41ff1d154f928e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568723"
---
# Behandeln von Windows-Runtime-Ereignissen in JavaScript  

Windows-Runtime-Ereignisse werden in JavaScript nicht wie in C++ oder .NET Framework auf die gleiche Weise dargestellt.  Es handelt sich nicht um Klassen Eigenschaften, sondern um Zeichenfolgenbezeichner mit \ (Kleinbuchstaben), die an die Klassen `addEventListener` und Methoden übergeben werden `removeEventListener` .  Beispielsweise können Sie einen Ereignishandler für das [GeoLocator. positionelle][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] -Ereignis hinzufügen, indem Sie die Zeichenfolge "positionelle" an die `Geolocator.addEventListener` Methode übergeben:  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

Sie können auch die `locator.onpositionchanged` Eigenschaft festlegen:  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

Ein weiterer Unterschied zwischen .NET/C++ und JavaScript ist die Anzahl von Parametern, die von einem Ereignishandler übernommen werden.  In .NET/C++ benötigt ein Handler zwei: den Ereignis Absender und die Ereignisdaten.  In JavaScript sind die beiden als einzelnes `Event` Objekt gebündelt.  Im folgenden Beispiel `ev` enthält der Parameter sowohl den Absender des Ereignisses \ (die `target` Eigenschaft \) als auch die ereignisdateneigenschaften \ (hier nur `position` \).  Die ereignisdateneigenschaften sind diejenigen, die für jedes Ereignis dokumentiert sind.  

```javascript
function (ev) {
    console.log("Sender:  " + ev.target);
    console.log("Position:  " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> Windows-Runtime-Features stehen für apps, die in Internet Explorer ausgeführt werden, nicht zur Verfügung.  

## Weitere Informationen  

[Verwenden der Windows-Runtime in JavaScript][WindowsRuntimeJavascript]  

 <!-- image links -->  

 <!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Verwenden der Windows-Runtime in JavaScript"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "GeoLocator-Klasse"  
