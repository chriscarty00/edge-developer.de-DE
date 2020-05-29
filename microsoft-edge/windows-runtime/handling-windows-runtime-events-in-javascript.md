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
# <span data-ttu-id="a9948-102">Behandeln von Windows-Runtime-Ereignissen in JavaScript</span><span class="sxs-lookup"><span data-stu-id="a9948-102">Handling Windows Runtime Events in JavaScript</span></span>  

<span data-ttu-id="a9948-103">Windows-Runtime-Ereignisse werden in JavaScript nicht wie in C++ oder .NET Framework auf die gleiche Weise dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a9948-103">Windows Runtime events are not represented in the same way in JavaScript as they are in C++ or the .NET Framework.</span></span>  <span data-ttu-id="a9948-104">Es handelt sich nicht um Klassen Eigenschaften, sondern um Zeichenfolgenbezeichner mit \ (Kleinbuchstaben), die an die Klassen `addEventListener` und Methoden übergeben werden `removeEventListener` .</span><span class="sxs-lookup"><span data-stu-id="a9948-104">They are not class properties, but rather are represented as \(lowercase\) string identifiers that are passed to the class's `addEventListener` and `removeEventListener` methods.</span></span>  <span data-ttu-id="a9948-105">Beispielsweise können Sie einen Ereignishandler für das [GeoLocator. positionelle][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] -Ereignis hinzufügen, indem Sie die Zeichenfolge "positionelle" an die `Geolocator.addEventListener` Methode übergeben:</span><span class="sxs-lookup"><span data-stu-id="a9948-105">For example, you can add an event handler for the [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] event by passing the string "positionchanged" to the `Geolocator.addEventListener` method:</span></span>  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

<span data-ttu-id="a9948-106">Sie können auch die `locator.onpositionchanged` Eigenschaft festlegen:</span><span class="sxs-lookup"><span data-stu-id="a9948-106">You can also set the `locator.onpositionchanged` property:</span></span>  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

<span data-ttu-id="a9948-107">Ein weiterer Unterschied zwischen .NET/C++ und JavaScript ist die Anzahl von Parametern, die von einem Ereignishandler übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="a9948-107">Another difference between .NET/C++ and JavaScript is the number of parameters taken by an event handler.</span></span>  <span data-ttu-id="a9948-108">In .NET/C++ benötigt ein Handler zwei: den Ereignis Absender und die Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="a9948-108">In .NET/C++, a handler takes two:  the event sender, and the event data.</span></span>  <span data-ttu-id="a9948-109">In JavaScript sind die beiden als einzelnes `Event` Objekt gebündelt.</span><span class="sxs-lookup"><span data-stu-id="a9948-109">In JavaScript, the two are bundled as a single `Event` object.</span></span>  <span data-ttu-id="a9948-110">Im folgenden Beispiel `ev` enthält der Parameter sowohl den Absender des Ereignisses \ (die `target` Eigenschaft \) als auch die ereignisdateneigenschaften \ (hier nur `position` \).</span><span class="sxs-lookup"><span data-stu-id="a9948-110">In the following example, the `ev` parameter contains both the sender of the event \(the `target` property\) and the event data properties \(here, just `position`\).</span></span>  <span data-ttu-id="a9948-111">Die ereignisdateneigenschaften sind diejenigen, die für jedes Ereignis dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="a9948-111">The event data properties are the ones that are documented for each event.</span></span>  

```javascript
function (ev) {
    console.log("Sender:  " + ev.target);
    console.log("Position:  " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> <span data-ttu-id="a9948-112">Windows-Runtime-Features stehen für apps, die in Internet Explorer ausgeführt werden, nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a9948-112">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="a9948-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a9948-113">See Also</span></span>  

[<span data-ttu-id="a9948-114">Verwenden der Windows-Runtime in JavaScript</span><span class="sxs-lookup"><span data-stu-id="a9948-114">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

 <!-- image links -->  

 <!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Verwenden der Windows-Runtime in JavaScript"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "GeoLocator-Klasse"  
