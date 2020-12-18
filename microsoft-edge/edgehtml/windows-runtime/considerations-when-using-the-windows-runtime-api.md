---
description: Überlegungen bei der Verwendung der Windows-Runtime-API.
title: Überlegungen bei der Verwendung der Windows-Runtime-API
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime API
ms.assetid: 2f56d70c-c80d-4876-8e6a-8ae031d31c22
caps.latest.revision: 8
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 718a23646ec9a82c1d53a2669d7cdbf218647e41
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233930"
---
# <span data-ttu-id="9b34d-103">Überlegungen bei der Verwendung der Windows-Runtime-API</span><span class="sxs-lookup"><span data-stu-id="9b34d-103">Considerations when using the Windows Runtime API</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="9b34d-104">Sie können nahezu jedes Element der Windows-Runtime-API in JavaScript verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b34d-104">You can use nearly every element of the Windows Runtime API in JavaScript.</span></span>  <span data-ttu-id="9b34d-105">Es gibt jedoch einige Aspekte der JavaScript-Darstellung von Windows-Runtime-Elementen, die Sie berücksichtigen sollten.</span><span class="sxs-lookup"><span data-stu-id="9b34d-105">However, there are some aspects of the JavaScript representation of Windows Runtime elements that you should keep in mind.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="9b34d-106">Informationen zum Erstellen von Komponenten für Windows-Runtime in c++, c# oder Visual Basic und deren Verwendung in JavaScript finden Sie unter Erstellen von Komponenten für Windows-Runtime [in c++][WindowsUwpComponentsCreatingCpp] und [Erstellen von Komponenten für Windows-Runtime in C# und Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="9b34d-106">For information about creating Windows Runtime components in C++, C#, or Visual Basic and consuming them in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpComponentsCreatingCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span></span>  

## <span data-ttu-id="9b34d-107">Sonderfälle in der JavaScript-Darstellung von Windows-Runtime-Typen</span><span class="sxs-lookup"><span data-stu-id="9b34d-107">Special cases in the JavaScript Representation of Windows Runtime types</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="9b34d-108">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="9b34d-108">Strings</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="9b34d-109">Eine nicht initialisierte Zeichenfolge wird als Zeichenfolge "undefined" an eine Windows-Runtime-Methode übergeben, und ein Zeichenfolgensatz, `null` der als Zeichenfolge "Null" übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9b34d-109">An uninitialized string is passed to a Windows Runtime method as the string "undefined", and a string set to `null` is passed as the string "null".</span></span>  <span data-ttu-id="9b34d-110">\ (Dies ist wahr, wenn ein `null` oder `undefined` -Wert in eine Zeichenfolge umgewandelt wird. \) bevor Sie eine Zeichenfolge an eine Windows-Runtime-Methode übergeben, sollten Sie Sie als leere Zeichenfolge initialisieren \ ("" \).</span><span class="sxs-lookup"><span data-stu-id="9b34d-110">\(This is true whenever a `null` or `undefined` value is coerced to a string.\)  Before you pass a string to a Windows Runtime method, you should initialize it as the empty string \(""\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9b34d-111">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9b34d-111">Interfaces</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="9b34d-112">Sie können in JavaScript keine Windows-Runtime-Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="9b34d-112">You cannot implement a Windows Runtime interface in JavaScript.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9b34d-113">Arrays</span><span class="sxs-lookup"><span data-stu-id="9b34d-113">Arrays</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="9b34d-114">Windows-Runtime-Arrays sind nicht veränderbar, daher funktionieren Methoden, die die Größe von Arrays in JavaScript ändern, nicht auf Windows-Runtime-Arrays.</span><span class="sxs-lookup"><span data-stu-id="9b34d-114">Windows Runtime arrays are not resizable, so methods that resize arrays in JavaScript do not work on Windows Runtime arrays.</span></span>  
      *   <span data-ttu-id="9b34d-115">Arrays: Wenn Sie einen JavaScript-Array Wert an eine Windows-Runtime-Methode übergeben, wird das Array kopiert.</span><span class="sxs-lookup"><span data-stu-id="9b34d-115">Arrays: If you pass a JavaScript array value to a Windows Runtime method, the array is copied.</span></span>  <span data-ttu-id="9b34d-116">Die Windows-Runtime-Methode kann das Array oder seine Member nicht ändern und an Ihre JavaScript-App zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9b34d-116">The Windows Runtime method is not able to modify the array or its members and return it to your JavaScript app.</span></span>  <span data-ttu-id="9b34d-117">Sie können jedoch typisierte Arrays verwenden (beispielsweise Int32Array- [Objekt][MDNInt32array]\), die nicht kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b34d-117">However, you can use typed arrays \(for example, [Int32Array Object][MDNInt32array]\), which are not copied.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9b34d-118">Strukturen</span><span class="sxs-lookup"><span data-stu-id="9b34d-118">Structures</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="9b34d-119">Windows-Runtime-Strukturen sind Objekte in JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9b34d-119">Windows Runtime structures are objects in JavaScript.</span></span>  <span data-ttu-id="9b34d-120">Wenn Sie eine Windows-Runtime-Struktur an eine Windows-Runtime-Methode übergeben möchten, instanziieren Sie die Struktur nicht mit dem `new` Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="9b34d-120">If you want to pass a Windows Runtime structure to a Windows Runtime method, don't instantiate the structure with the `new` keyword.</span></span>  <span data-ttu-id="9b34d-121">Erstellen Sie stattdessen ein Objekt, und fügen Sie die relevanten Member und deren Werte hinzu.</span><span class="sxs-lookup"><span data-stu-id="9b34d-121">Instead, create an object and add the relevant members and their values.</span></span>  <span data-ttu-id="9b34d-122">Die Namen der Mitglieder sollten im Camel-Fall liegen: `SomeStruct.firstMember` .</span><span class="sxs-lookup"><span data-stu-id="9b34d-122">The names of the members should be in camel case: `SomeStruct.firstMember`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9b34d-123">Objekte</span><span class="sxs-lookup"><span data-stu-id="9b34d-123">Objects</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="9b34d-124">JavaScript-Objekte sind nicht mit verwalteten Code Objekten identisch `System.Object` .</span><span class="sxs-lookup"><span data-stu-id="9b34d-124">JavaScript objects aren't the same as managed code objects \(`System.Object`\).</span></span>  <span data-ttu-id="9b34d-125">Sie können ein JavaScript-Objekt nicht an eine Windows-Runtime-Methode übergeben, für die ein `System.Object` .</span><span class="sxs-lookup"><span data-stu-id="9b34d-125">You can't pass a JavaScript object to a Windows Runtime method that requires a `System.Object`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9b34d-126">Objektidentität</span><span class="sxs-lookup"><span data-stu-id="9b34d-126">Object identity</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="9b34d-127">In den meisten Fällen ändern sich die Objekte, die zwischen der Windows-Runtime und JavaScript hin-und hergeleitet werden, nicht.</span><span class="sxs-lookup"><span data-stu-id="9b34d-127">In most cases, the objects passed back and forth between the Windows Runtime and JavaScript do not change.</span></span>  <span data-ttu-id="9b34d-128">Das JavaScript-Modul verwaltet eine Karte mit bekannten Objekten.</span><span class="sxs-lookup"><span data-stu-id="9b34d-128">The JavaScript engine maintains a map of known objects.</span></span>  <span data-ttu-id="9b34d-129">Wenn ein Objekt von der Windows-Runtime zurückgegeben wird, wird es mit der Zuordnung abgeglichen, und wenn es nicht vorhanden ist, wird ein neues Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="9b34d-129">When an object is returned from the Windows Runtime it is matched against the map, and if it does not exist a new object is created.</span></span>  <span data-ttu-id="9b34d-130">Das gleiche Verfahren wird für Objekte befolgt, die Schnittstellen darstellen, die von Windows-Runtime-Methoden zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b34d-130">The same procedure is followed for objects that represent interfaces that are returned by Windows Runtime methods.</span></span>  <span data-ttu-id="9b34d-131">Es gibt zwei Arten von Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="9b34d-131">There are two kinds of exceptions:</span></span>  
      
      *   <span data-ttu-id="9b34d-132">Objekte, die von einem Windows-Runtime-Aufruf zurückgegeben werden und dann neue \ (Expando \)-Eigenschaften hinzugefügt wurden, behalten ihre neuen Eigenschaften nicht bei, wenn Sie an die Windows-Runtime zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b34d-132">Objects that are returned from a Windows Runtime call, and then have new \(expando\) properties added, don't retain their new properties when they are passed back to the Windows Runtime.</span></span>  <span data-ttu-id="9b34d-133">Wenn Sie jedoch an die JavaScript-App zurückgegeben werden, da Sie dem vorhandenen Objekt zugeordnet sind, verfügt das zurückgegebene Objekt über die Expando-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9b34d-133">However, when they are returned to the JavaScript app, because they're matched to the existing object, the returned object does have the expando properties.</span></span>  
      *   <span data-ttu-id="9b34d-134">Strukturen und Stellvertretungen in der Windows-Runtime können nicht als identisch mit zuvor verwendeten Strukturen oder Stellvertretungen identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="9b34d-134">Structures and delegates in Windows Runtime can't be identified as identical to previously-used structures or delegates.</span></span>  <span data-ttu-id="9b34d-135">Jedes Mal, wenn eine Struktur oder ein Delegat zurückgegeben wird, wird ein neuer Verweis abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9b34d-135">Every time a structure or delegate is returned, it gets a new reference.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9b34d-136">Namenskollisionen</span><span class="sxs-lookup"><span data-stu-id="9b34d-136">Name collisions</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="9b34d-137">Mehrere Windows-Runtime-Schnittstellen verfügen möglicherweise über Member mit den gleichen Namen.</span><span class="sxs-lookup"><span data-stu-id="9b34d-137">Multiple Windows Runtime interfaces may have members with the same names.</span></span>  <span data-ttu-id="9b34d-138">Wenn Sie in einem einzelnen JavaScript-Objekt kombiniert werden (Dies kann eine Darstellung einer Runtime-Klasse oder einer Schnittstelle sein), werden die Member durch vollqualifizierte Namen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9b34d-138">If they are combined in a single JavaScript object (which can be a representation of a runtime class or an interface), the members are represented with fully-qualified names.</span></span>  <span data-ttu-id="9b34d-139">Sie können diese Member mithilfe der folgenden Syntax aufrufen:</span><span class="sxs-lookup"><span data-stu-id="9b34d-139">You can call these members by using the following syntax:</span></span>  
      
      ```cpp
      Class["MemberName"](parameter)
      ```  
      
      <span data-ttu-id="9b34d-140">Im folgenden Code verfügen zwei Schnittstellen über eine Draw-Methode, und eine Runtime-Klasse implementiert beide Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="9b34d-140">In the following code, two interfaces have a Draw method, and a runtime class implements both interfaces.</span></span>  
      
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
      
      <span data-ttu-id="9b34d-141">Hier erfahren Sie, wie Sie den obigen Code in JavaScript aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="9b34d-141">Here is how you can call the above code in JavaScript.</span></span>  
      
      ```javascript
      var example = new ExampleObject();
      example["CollisionExample.InterfaceA.draw"](12);
      example["CollisionExample.InterfaceB.draw"]("hello");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `Out` <span data-ttu-id="9b34d-142">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b34d-142">parameters</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="9b34d-143">Wenn eine Windows-Runtime-Methode über mehrere `out` Parameter verfügt, verfügt die Methode in JavaScript über ein JavaScript-Objekt als Rückgabewert, und das Objekt verfügt über Eigenschaften, die dem `out` Parameter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9b34d-143">If a Windows Runtime method has multiple `out` parameters, in JavaScript the method has a JavaScript object as its return value, and the object has properties that correspond to the `out` parameter.</span></span>  <span data-ttu-id="9b34d-144">Nehmen Sie beispielsweise die folgende Windows-Runtime-Signatur in C++ in Frage.</span><span class="sxs-lookup"><span data-stu-id="9b34d-144">For example, consider the following Windows Runtime signature in C++.</span></span>  
      
      ```cpp
      void ExampleMethod(
          [OutAttribute] char^ first,
          [OutAttribute] char^ second
      )
      ```  
      
      <span data-ttu-id="9b34d-145">Die JavaScript-Version dieser Signatur lautet:</span><span class="sxs-lookup"><span data-stu-id="9b34d-145">The JavaScript version of this signature is:</span></span>  
      
      ```javascript
      var returnValue = exampleMethod();
      ```  
      
      <span data-ttu-id="9b34d-146">In diesem Beispiel `returnValue` ist ein JavaScript-Objekt mit zwei Feldern: `first` und `second` .</span><span class="sxs-lookup"><span data-stu-id="9b34d-146">In this example, `returnValue` is a JavaScript object that has two fields: `first` and `second`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9b34d-147">Statische Member</span><span class="sxs-lookup"><span data-stu-id="9b34d-147">Static members</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="9b34d-148">Die Windows-Runtime definiert sowohl statische Member als auch Instanzen Mitglieder.</span><span class="sxs-lookup"><span data-stu-id="9b34d-148">The Windows Runtime defines both static members and instance members.</span></span>  <span data-ttu-id="9b34d-149">In JavaScript werden statische Member dem Objekt hinzugefügt, das der Windows-Runtime-Klasse oder-Schnittstelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9b34d-149">In JavaScript, static members are added to the object that is associated with the Windows Runtime class or interface.</span></span>  
      
      ```javascript
      // Static method.
      var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
      // Instance method.
      var reading = accel.getCurrentReading();
      ```  
   :::column-end:::
:::row-end:::  
    
<span data-ttu-id="9b34d-150">Weitere Informationen zur JavaScript-Darstellung von Windows-Runtime Basic-Typen finden Sie unter [JavaScript-Darstellung von Windows-Runtime-Typen][WindowsRuntimeJavascriptTypes].</span><span class="sxs-lookup"><span data-stu-id="9b34d-150">For more information about the JavaScript representation of Windows Runtime basic types, see [JavaScript Representation of Windows Runtime Types][WindowsRuntimeJavascriptTypes].</span></span>  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "JavaScript-Darstellung von Windows-Runtime-Typen | Microsoft docs"

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Komponenten für Windows-Runtime mit C++/CX | Microsoft docs"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Komponenten für Windows-Runtime mit C# und Visual Basic | Microsoft docs"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  
