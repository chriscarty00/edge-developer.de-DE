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
# <a name="handling-windows-runtime-events-in-javascript"></a><span data-ttu-id="83791-103">Windows-Runtime-Ereignissen in JavaScript behandeln</span><span class="sxs-lookup"><span data-stu-id="83791-103">Handling Windows Runtime events in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="83791-104">Windows-Runtime-Ereignisse werden in JavaScript nicht auf die gleiche Weise dargestellt wie in C++ oder .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="83791-104">Windows Runtime events are not represented in the same way in JavaScript as they are in C++ or the .NET Framework.</span></span>  <span data-ttu-id="83791-105">Sie sind keine Klasseneigenschaften, sondern werden als \(Kleinbuchstabe\)-Zeichenfolgenbezeichner dargestellt, die an die Methoden und Methoden der `addEventListener` Klasse übergeben `removeEventListener` werden.</span><span class="sxs-lookup"><span data-stu-id="83791-105">They are not class properties, but rather are represented as \(lowercase\) string identifiers that are passed to the class's `addEventListener` and `removeEventListener` methods.</span></span>  <span data-ttu-id="83791-106">Sie können beispielsweise einen Ereignishandler für das [Geolocator.PositionChanged-Ereignis][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] hinzufügen, indem Sie die Zeichenfolge an `positionchanged` die -Methode `Geolocator.addEventListener` übergeben:</span><span class="sxs-lookup"><span data-stu-id="83791-106">For example, you can add an event handler for the [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] event by passing the string `positionchanged` to the `Geolocator.addEventListener` method:</span></span>  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

<span data-ttu-id="83791-107">Sie können auch die Eigenschaft `locator.onpositionchanged` festlegen:</span><span class="sxs-lookup"><span data-stu-id="83791-107">You can also set the `locator.onpositionchanged` property:</span></span>  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

<span data-ttu-id="83791-108">Ein weiterer Unterschied zwischen .NET/C++ und JavaScript ist die Anzahl der Parameter, die von einem Ereignishandler verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83791-108">Another difference between .NET/C++ and JavaScript is the number of parameters taken by an event handler.</span></span>  <span data-ttu-id="83791-109">In .NET/C++ benötigt ein Handler zwei: den Ereignisabsender und die Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="83791-109">In .NET/C++, a handler takes two:  the event sender, and the event data.</span></span>  <span data-ttu-id="83791-110">In JavaScript werden die beiden als einzelnes Objekt `Event` gebündelt.</span><span class="sxs-lookup"><span data-stu-id="83791-110">In JavaScript, the two are bundled as a single `Event` object.</span></span>  <span data-ttu-id="83791-111">Im folgenden Beispiel enthält der Parameter sowohl den Absender des Ereignisses \(die Eigenschaft\) als auch die Ereignisdateneigenschaften `ev` `target` \(hier, nur `position` \).</span><span class="sxs-lookup"><span data-stu-id="83791-111">In the following example, the `ev` parameter contains both the sender of the event \(the `target` property\) and the event data properties \(here, just `position`\).</span></span>  <span data-ttu-id="83791-112">Die Ereignisdateneigenschaften sind die Eigenschaften, die für jedes Ereignis dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="83791-112">The event data properties are the ones that are documented for each event.</span></span>  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> <span data-ttu-id="83791-113">Windows-Runtime-Features sind für Apps, die in Internet Explorer ausgeführt werden, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83791-113">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <a name="see-also"></a><span data-ttu-id="83791-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="83791-114">See also</span></span>  

[<span data-ttu-id="83791-115">Verwenden der Windows-Runtime in JavaScript</span><span class="sxs-lookup"><span data-stu-id="83791-115">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Verwenden der Windows-Runtime in JavaScript-| Microsoft Docs"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Geolocator-Klasse | Microsoft Docs"  
