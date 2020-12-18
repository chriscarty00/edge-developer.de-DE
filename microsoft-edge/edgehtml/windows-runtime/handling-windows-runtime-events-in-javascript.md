---
description: Behandeln von Windows-Runtime-Ereignissen in JavaScript
title: Behandeln von Windows-Runtime-Ereignissen in JavaScript
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
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e0a3e35c908c766c0308903381b271f5ccdb27a3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234116"
---
# <span data-ttu-id="a77bd-103">Windows-Runtime-Ereignissen in JavaScript behandeln</span><span class="sxs-lookup"><span data-stu-id="a77bd-103">Handling Windows Runtime events in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="a77bd-104">Windows-Runtime-Ereignisse werden in JavaScript nicht wie in C++ oder .NET Framework auf die gleiche Weise dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a77bd-104">Windows Runtime events are not represented in the same way in JavaScript as they are in C++ or the .NET Framework.</span></span>  <span data-ttu-id="a77bd-105">Es handelt sich nicht um Klassen Eigenschaften, sondern um Zeichenfolgenbezeichner mit \ (Kleinbuchstaben), die an die Klassen `addEventListener` und Methoden übergeben werden `removeEventListener` .</span><span class="sxs-lookup"><span data-stu-id="a77bd-105">They are not class properties, but rather are represented as \(lowercase\) string identifiers that are passed to the class's `addEventListener` and `removeEventListener` methods.</span></span>  <span data-ttu-id="a77bd-106">Beispielsweise können Sie einen Ereignishandler für das [GeoLocator. positionelle][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] -Ereignis hinzufügen, indem Sie die Zeichenfolge `positionchanged` an die `Geolocator.addEventListener` Methode übergeben:</span><span class="sxs-lookup"><span data-stu-id="a77bd-106">For example, you can add an event handler for the [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] event by passing the string `positionchanged` to the `Geolocator.addEventListener` method:</span></span>  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

<span data-ttu-id="a77bd-107">Sie können auch die `locator.onpositionchanged` Eigenschaft festlegen:</span><span class="sxs-lookup"><span data-stu-id="a77bd-107">You can also set the `locator.onpositionchanged` property:</span></span>  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

<span data-ttu-id="a77bd-108">Ein weiterer Unterschied zwischen .NET/C++ und JavaScript ist die Anzahl von Parametern, die von einem Ereignishandler übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="a77bd-108">Another difference between .NET/C++ and JavaScript is the number of parameters taken by an event handler.</span></span>  <span data-ttu-id="a77bd-109">In .NET/C++ benötigt ein Handler zwei: den Ereignis Absender und die Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="a77bd-109">In .NET/C++, a handler takes two:  the event sender, and the event data.</span></span>  <span data-ttu-id="a77bd-110">In JavaScript sind die beiden als einzelnes `Event` Objekt gebündelt.</span><span class="sxs-lookup"><span data-stu-id="a77bd-110">In JavaScript, the two are bundled as a single `Event` object.</span></span>  <span data-ttu-id="a77bd-111">Im folgenden Beispiel `ev` enthält der Parameter sowohl den Absender des Ereignisses \ (die `target` Eigenschaft \) als auch die ereignisdateneigenschaften \ (hier nur `position` \).</span><span class="sxs-lookup"><span data-stu-id="a77bd-111">In the following example, the `ev` parameter contains both the sender of the event \(the `target` property\) and the event data properties \(here, just `position`\).</span></span>  <span data-ttu-id="a77bd-112">Die ereignisdateneigenschaften sind diejenigen, die für jedes Ereignis dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="a77bd-112">The event data properties are the ones that are documented for each event.</span></span>  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> <span data-ttu-id="a77bd-113">Windows-Runtime-Features stehen für apps, die in Internet Explorer ausgeführt werden, nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a77bd-113">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="a77bd-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a77bd-114">See also</span></span>  

[<span data-ttu-id="a77bd-115">Verwenden der Windows-Runtime in JavaScript</span><span class="sxs-lookup"><span data-stu-id="a77bd-115">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Verwenden der Windows-Runtime in JavaScript | Microsoft docs"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "GeoLocator-Klasse | Microsoft docs"  
