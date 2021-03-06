---
description: Überlegungen bei der Verwendung der Windows-Runtime-API
title: Überlegungen bei der Verwendung der Windows-Runtime-API
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime API
ms.assetid: 2f56d70c-c80d-4876-8e6a-8ae031d31c22
caps.latest.revision: 8
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 170374fd109802bff0aa0fc93cea6c8d50c9d7c7
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399344"
---
# <a name="considerations-when-using-the-windows-runtime-api"></a><span data-ttu-id="4b84b-103">Überlegungen bei der Verwendung der Windows-Runtime-API</span><span class="sxs-lookup"><span data-stu-id="4b84b-103">Considerations when using the Windows Runtime API</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="4b84b-104">Sie können fast jedes Element der Windows-Runtime-API in JavaScript verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b84b-104">You can use nearly every element of the Windows Runtime API in JavaScript.</span></span>  <span data-ttu-id="4b84b-105">Es gibt jedoch einige Aspekte der JavaScript-Darstellung von Windows-Runtime-Elementen, die Sie berücksichtigen sollten.</span><span class="sxs-lookup"><span data-stu-id="4b84b-105">However, there are some aspects of the JavaScript representation of Windows Runtime elements that you should keep in mind.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="4b84b-106">Informationen zum Erstellen von Windows-Runtime-Komponenten in C++, C# oder Visual Basic und deren Verwendung in JavaScript finden Sie unter [Creating Windows Runtime Components in C++][WindowsUwpComponentsCreatingCpp] und Creating Windows Runtime Components in C# and [Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="4b84b-106">For information about creating Windows Runtime components in C++, C#, or Visual Basic and consuming them in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpComponentsCreatingCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span></span>  

## <a name="special-cases-in-the-javascript-representation-of-windows-runtime-types"></a><span data-ttu-id="4b84b-107">Sonderfälle in der JavaScript-Darstellung von Windows-Runtime-Typen</span><span class="sxs-lookup"><span data-stu-id="4b84b-107">Special cases in the JavaScript Representation of Windows Runtime types</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="4b84b-108">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="4b84b-108">Strings</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="4b84b-109">Eine nicht initialisierte Zeichenfolge wird an eine Windows-Runtime-Methode als Zeichenfolge "undefined" übergeben, und eine Zeichenfolge, die auf festgelegt ist, wird als Zeichenfolge `null` "null" übergeben.</span><span class="sxs-lookup"><span data-stu-id="4b84b-109">An uninitialized string is passed to a Windows Runtime method as the string "undefined", and a string set to `null` is passed as the string "null".</span></span>  <span data-ttu-id="4b84b-110">\(Dies gilt, wenn ein oder ein Wert an eine Zeichenfolge gecced wird.\) Bevor Sie eine Zeichenfolge an eine Windows-Runtime-Methode übergeben, sollten Sie sie als leere Zeichenfolge `null` `undefined` \(""\) initialisieren.</span><span class="sxs-lookup"><span data-stu-id="4b84b-110">\(This is true whenever a `null` or `undefined` value is coerced to a string.\)  Before you pass a string to a Windows Runtime method, you should initialize it as the empty string \(""\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="4b84b-111">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4b84b-111">Interfaces</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="4b84b-112">Sie können keine Windows-Runtime-Schnittstelle in JavaScript implementieren.</span><span class="sxs-lookup"><span data-stu-id="4b84b-112">You cannot implement a Windows Runtime interface in JavaScript.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="4b84b-113">Arrays</span><span class="sxs-lookup"><span data-stu-id="4b84b-113">Arrays</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="4b84b-114">Windows-Runtime-Arrays können nicht geändert werden, sodass Methoden, die die Größe von Arrays in JavaScript ändern, nicht auf Windows-Runtime-Arrays funktionieren.</span><span class="sxs-lookup"><span data-stu-id="4b84b-114">Windows Runtime arrays are not resizable, so methods that resize arrays in JavaScript do not work on Windows Runtime arrays.</span></span>  
      *   <span data-ttu-id="4b84b-115">Arrays: Wenn Sie einen JavaScript-Arraywert an eine Windows-Runtime-Methode übergeben, wird das Array kopiert.</span><span class="sxs-lookup"><span data-stu-id="4b84b-115">Arrays: If you pass a JavaScript array value to a Windows Runtime method, the array is copied.</span></span>  <span data-ttu-id="4b84b-116">Die Windows-Runtime-Methode kann das Array oder seine Member nicht ändern und an Ihre JavaScript-App zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4b84b-116">The Windows Runtime method is not able to modify the array or its members and return it to your JavaScript app.</span></span>  <span data-ttu-id="4b84b-117">Sie können jedoch typierte Arrays \(z. B. [Int32Array-Objekt][MDNInt32array]\) verwenden, die nicht kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="4b84b-117">However, you can use typed arrays \(for example, [Int32Array Object][MDNInt32array]\), which are not copied.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="4b84b-118">Strukturen</span><span class="sxs-lookup"><span data-stu-id="4b84b-118">Structures</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="4b84b-119">Windows-Runtime-Strukturen sind Objekte in JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4b84b-119">Windows Runtime structures are objects in JavaScript.</span></span>  <span data-ttu-id="4b84b-120">Wenn Sie eine Windows-Runtime-Struktur an eine Windows-Runtime-Methode übergeben möchten, instanziieren Sie die Struktur nicht mit dem `new` Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="4b84b-120">If you want to pass a Windows Runtime structure to a Windows Runtime method, don't instantiate the structure with the `new` keyword.</span></span>  <span data-ttu-id="4b84b-121">Erstellen Sie stattdessen ein Objekt, und fügen Sie die relevanten Elemente und deren Werte hinzu.</span><span class="sxs-lookup"><span data-stu-id="4b84b-121">Instead, create an object and add the relevant members and their values.</span></span>  <span data-ttu-id="4b84b-122">Die Namen der Mitglieder sollten in Kamelfall sein: `SomeStruct.firstMember` .</span><span class="sxs-lookup"><span data-stu-id="4b84b-122">The names of the members should be in camel case: `SomeStruct.firstMember`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="4b84b-123">Objekte</span><span class="sxs-lookup"><span data-stu-id="4b84b-123">Objects</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="4b84b-124">JavaScript-Objekte sind nicht mit verwalteten Codeobjekten \( `System.Object` \) identisch.</span><span class="sxs-lookup"><span data-stu-id="4b84b-124">JavaScript objects aren't the same as managed code objects \(`System.Object`\).</span></span>  <span data-ttu-id="4b84b-125">Sie können ein JavaScript-Objekt nicht an eine Windows-Runtime-Methode übergeben, die eine `System.Object` erfordert.</span><span class="sxs-lookup"><span data-stu-id="4b84b-125">You can't pass a JavaScript object to a Windows Runtime method that requires a `System.Object`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="4b84b-126">Objektidentität</span><span class="sxs-lookup"><span data-stu-id="4b84b-126">Object identity</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="4b84b-127">In den meisten Fällen ändern sich die zwischen der Windows-Runtime und JavaScript übergebenen Objekte nicht.</span><span class="sxs-lookup"><span data-stu-id="4b84b-127">In most cases, the objects passed back and forth between the Windows Runtime and JavaScript do not change.</span></span>  <span data-ttu-id="4b84b-128">Das JavaScript-Modul verwaltet eine Karte bekannter Objekte.</span><span class="sxs-lookup"><span data-stu-id="4b84b-128">The JavaScript engine maintains a map of known objects.</span></span>  <span data-ttu-id="4b84b-129">Wenn ein Objekt von der Windows-Runtime zurückgegeben wird, wird es mit der Karte abgestimmt, und wenn es nicht vorhanden ist, wird ein neues Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="4b84b-129">When an object is returned from the Windows Runtime it is matched against the map, and if it does not exist a new object is created.</span></span>  <span data-ttu-id="4b84b-130">Dasselbe Verfahren wird für Objekte befolgt, die Schnittstellen darstellen, die von Windows-Runtime-Methoden zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4b84b-130">The same procedure is followed for objects that represent interfaces that are returned by Windows Runtime methods.</span></span>  <span data-ttu-id="4b84b-131">Es gibt zwei Arten von Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="4b84b-131">There are two kinds of exceptions:</span></span>  
      
      *   <span data-ttu-id="4b84b-132">Objekte, die von einem Windows-Runtime-Aufruf zurückgegeben werden und dann neue \(expando\)-Eigenschaften hinzugefügt haben, behalten ihre neuen Eigenschaften nicht bei, wenn sie an die Windows-Runtime übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="4b84b-132">Objects that are returned from a Windows Runtime call, and then have new \(expando\) properties added, don't retain their new properties when they are passed back to the Windows Runtime.</span></span>  <span data-ttu-id="4b84b-133">Wenn sie jedoch an die JavaScript-App zurückgegeben werden, da sie mit dem vorhandenen Objekt übereinstimmen, verfügt das zurückgegebene Objekt über die expando-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4b84b-133">However, when they are returned to the JavaScript app, because they're matched to the existing object, the returned object does have the expando properties.</span></span>  
      *   <span data-ttu-id="4b84b-134">Strukturen und Delegaten in der Windows-Runtime können nicht als identisch mit zuvor verwendeten Strukturen oder Delegaten identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="4b84b-134">Structures and delegates in Windows Runtime can't be identified as identical to previously-used structures or delegates.</span></span>  <span data-ttu-id="4b84b-135">Jedes Mal, wenn eine Struktur oder ein Delegat zurückgegeben wird, erhält sie einen neuen Verweis.</span><span class="sxs-lookup"><span data-stu-id="4b84b-135">Every time a structure or delegate is returned, it gets a new reference.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="4b84b-136">Namenskollision</span><span class="sxs-lookup"><span data-stu-id="4b84b-136">Name collisions</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="4b84b-137">Mehrere Windows-Runtime-Schnittstellen können Mitglieder mit denselben Namen haben.</span><span class="sxs-lookup"><span data-stu-id="4b84b-137">Multiple Windows Runtime interfaces may have members with the same names.</span></span>  <span data-ttu-id="4b84b-138">Wenn sie in einem einzelnen JavaScript-Objekt kombiniert werden (dies kann eine Darstellung einer Laufzeitklasse oder einer Schnittstelle sein), werden die Member mit vollqualifizierten Namen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4b84b-138">If they are combined in a single JavaScript object (which can be a representation of a runtime class or an interface), the members are represented with fully-qualified names.</span></span>  <span data-ttu-id="4b84b-139">Sie können diese Elemente mithilfe der folgenden Syntax aufrufen:</span><span class="sxs-lookup"><span data-stu-id="4b84b-139">You can call these members by using the following syntax:</span></span>  
      
      ```cpp
      Class["MemberName"](parameter)
      ```  
      
      <span data-ttu-id="4b84b-140">Im folgenden Code verfügen zwei Schnittstellen über eine Draw-Methode, und eine Laufzeitklasse implementiert beide Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4b84b-140">In the following code, two interfaces have a Draw method, and a runtime class implements both interfaces.</span></span>  
      
      ```cpp
      namespace CollisionExample {
          interface InterfaceA
          {
              HRESULT Draw([in] Int32 a);
          }
          interface InterfaceB
          {
              HRESULT Draw([in] HString a);
          }
          runtimeclass ExampleObject {
            interface InterfaceA
            interface InterfaceB
          }
      }
      ```  
      
      <span data-ttu-id="4b84b-141">Hier erfahren Sie, wie Sie den obigen Code in JavaScript aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="4b84b-141">Here is how you can call the above code in JavaScript.</span></span>  
      
      ```javascript
      var example = new ExampleObject();
      example["CollisionExample.InterfaceA.draw"](12);
      example["CollisionExample.InterfaceB.draw"]("hello");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `Out` <span data-ttu-id="4b84b-142">parameter</span><span class="sxs-lookup"><span data-stu-id="4b84b-142">parameters</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="4b84b-143">Wenn eine Windows-Runtime-Methode über mehrere Parameter verfügt, verfügt die Methode in JavaScript über ein JavaScript-Objekt als Rückgabewert, und das Objekt verfügt über Eigenschaften, die `out` dem Parameter `out` entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4b84b-143">If a Windows Runtime method has multiple `out` parameters, in JavaScript the method has a JavaScript object as its return value, and the object has properties that correspond to the `out` parameter.</span></span>  <span data-ttu-id="4b84b-144">Berücksichtigen Sie beispielsweise die folgende Windows-Runtime-Signatur in C++.</span><span class="sxs-lookup"><span data-stu-id="4b84b-144">For example, consider the following Windows Runtime signature in C++.</span></span>  
      
      ```cpp
      void ExampleMethod(
          [OutAttribute] char^ first,
          [OutAttribute] char^ second
      )
      ```  
      
      <span data-ttu-id="4b84b-145">Die JavaScript-Version dieser Signatur ist:</span><span class="sxs-lookup"><span data-stu-id="4b84b-145">The JavaScript version of this signature is:</span></span>  
      
      ```javascript
      var returnValue = exampleMethod();
      ```  
      
      <span data-ttu-id="4b84b-146">In diesem Beispiel `returnValue` ist ein JavaScript-Objekt mit zwei Feldern: `first` und `second` .</span><span class="sxs-lookup"><span data-stu-id="4b84b-146">In this example, `returnValue` is a JavaScript object that has two fields: `first` and `second`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="4b84b-147">Statische Elemente</span><span class="sxs-lookup"><span data-stu-id="4b84b-147">Static members</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="4b84b-148">Die Windows-Runtime definiert sowohl statische Member als auch Instanzmitglieder.</span><span class="sxs-lookup"><span data-stu-id="4b84b-148">The Windows Runtime defines both static members and instance members.</span></span>  <span data-ttu-id="4b84b-149">In JavaScript werden statische Member dem Objekt hinzugefügt, das der Windows-Runtime-Klasse oder -Schnittstelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4b84b-149">In JavaScript, static members are added to the object that is associated with the Windows Runtime class or interface.</span></span>  
      
      ```javascript
      // Static method.
      var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
      // Instance method.
      var reading = accel.getCurrentReading();
      ```  
   :::column-end:::
:::row-end:::  
    
<span data-ttu-id="4b84b-150">Weitere Informationen zur JavaScript-Darstellung von grundlegenden Windows-Runtime-Typen finden Sie unter [JavaScript Representation of Windows Runtime Types][WindowsRuntimeJavascriptTypes].</span><span class="sxs-lookup"><span data-stu-id="4b84b-150">For more information about the JavaScript representation of Windows Runtime basic types, see [JavaScript Representation of Windows Runtime Types][WindowsRuntimeJavascriptTypes].</span></span>  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "JavaScript-Darstellung von Windows-Laufzeittypen | Microsoft Docs"  

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Windows-Runtime-Komponenten mit C++/CX-| Microsoft Docs"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Windows-Runtime-Komponenten mit C# und Visual Basic | Microsoft Docs"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  
