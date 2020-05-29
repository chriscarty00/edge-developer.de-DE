---
title: Überlegungen bei der Verwendung der Windows-Runtime-API
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime API
ms.assetid: 2f56d70c-c80d-4876-8e6a-8ae031d31c22
caps.latest.revision: 8
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 95b082e27c4f247b841a9540e13bd49bd4c8bd67
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568727"
---
# <span data-ttu-id="989fe-102">Überlegungen bei der Verwendung der Windows-Runtime-API</span><span class="sxs-lookup"><span data-stu-id="989fe-102">Considerations when Using the Windows Runtime API</span></span>  

<span data-ttu-id="989fe-103">Sie können nahezu jedes Element der Windows-Runtime-API in JavaScript verwenden.</span><span class="sxs-lookup"><span data-stu-id="989fe-103">You can use nearly every element of the Windows Runtime API in JavaScript.</span></span>  <span data-ttu-id="989fe-104">Es gibt jedoch einige Aspekte der JavaScript-Darstellung von Windows-Runtime-Elementen, die Sie berücksichtigen sollten.</span><span class="sxs-lookup"><span data-stu-id="989fe-104">However, there are some aspects of the JavaScript representation of Windows Runtime elements that you should keep in mind.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="989fe-105">Informationen zum Erstellen von Komponenten für Windows-Runtime in c++, c# oder Visual Basic und deren Verwendung in JavaScript finden Sie unter Erstellen von Komponenten für Windows-Runtime [in c++][WindowsUwpComponentsCreatingCpp] und [Erstellen von Komponenten für Windows-Runtime in C# und Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="989fe-105">For information about creating Windows Runtime components in C++, C#, or Visual Basic and consuming them in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpComponentsCreatingCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span></span>  

## <span data-ttu-id="989fe-106">Sonderfälle in der JavaScript-Darstellung von Windows-Runtime-Typen</span><span class="sxs-lookup"><span data-stu-id="989fe-106">Special Cases in the JavaScript Representation of Windows Runtime Types</span></span>  

*   <span data-ttu-id="989fe-107">Zeichenfolgen: eine nicht initialisierte Zeichenfolge wird als Zeichenfolge "undefined" an eine Windows-Runtime-Methode übergeben, und ein Zeichenfolgensatz, `null` der als Zeichenfolge "Null" übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="989fe-107">Strings: An uninitialized string is passed to a Windows Runtime method as the string "undefined", and a string set to `null` is passed as the string "null".</span></span>  <span data-ttu-id="989fe-108">\ (Dies ist wahr, wenn ein `null` oder `undefined` -Wert in eine Zeichenfolge umgewandelt wird. \) bevor Sie eine Zeichenfolge an eine Windows-Runtime-Methode übergeben, sollten Sie Sie als leere Zeichenfolge initialisieren \ ("" \).</span><span class="sxs-lookup"><span data-stu-id="989fe-108">\(This is true whenever a `null` or `undefined` value is coerced to a string.\)  Before you pass a string to a Windows Runtime method, you should initialize it as the empty string \(""\).</span></span>  
*   <span data-ttu-id="989fe-109">Schnittstellen: Sie können in JavaScript keine Windows-Runtime-Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="989fe-109">Interfaces: You cannot implement a Windows Runtime interface in JavaScript.</span></span>  
*   <span data-ttu-id="989fe-110">Arrays: Windows-Runtime-Arrays sind nicht veränderbar, daher funktionieren Methoden, die die Größe von Arrays in JavaScript ändern, nicht auf Windows-Runtime-Arrays.</span><span class="sxs-lookup"><span data-stu-id="989fe-110">Arrays: Windows Runtime arrays are not resizable, so methods that resize arrays in JavaScript do not work on Windows Runtime arrays.</span></span>  
*   <span data-ttu-id="989fe-111">Arrays: Wenn Sie einen JavaScript-Array Wert an eine Windows-Runtime-Methode übergeben, wird das Array kopiert.</span><span class="sxs-lookup"><span data-stu-id="989fe-111">Arrays: If you pass a JavaScript array value to a Windows Runtime method, the array is copied.</span></span>  <span data-ttu-id="989fe-112">Die Windows-Runtime-Methode kann das Array oder seine Member nicht ändern und an Ihre JavaScript-App zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="989fe-112">The Windows Runtime method is not able to modify the array or its members and return it to your JavaScript app.</span></span>  <span data-ttu-id="989fe-113">Sie können jedoch typisierte Arrays verwenden (beispielsweise Int32Array- [Objekt][MDNInt32array]\), die nicht kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="989fe-113">However, you can use typed arrays \(for example, [Int32Array Object][MDNInt32array]\), which are not copied.</span></span>  
*   <span data-ttu-id="989fe-114">Strukturen: Windows-Runtime-Strukturen sind Objekte in JavaScript.</span><span class="sxs-lookup"><span data-stu-id="989fe-114">Structures: Windows Runtime structures are objects in JavaScript.</span></span>  <span data-ttu-id="989fe-115">Wenn Sie eine Windows-Runtime-Struktur an eine Windows-Runtime-Methode übergeben möchten, instanziieren Sie die Struktur nicht mit dem `new` Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="989fe-115">If you want to pass a Windows Runtime structure to a Windows Runtime method, don't instantiate the structure with the `new` keyword.</span></span>  <span data-ttu-id="989fe-116">Erstellen Sie stattdessen ein Objekt, und fügen Sie die relevanten Member und deren Werte hinzu.</span><span class="sxs-lookup"><span data-stu-id="989fe-116">Instead, create an object and add the relevant members and their values.</span></span>  <span data-ttu-id="989fe-117">Die Namen der Mitglieder sollten im Camel-Fall liegen: `SomeStruct.firstMember` .</span><span class="sxs-lookup"><span data-stu-id="989fe-117">The names of the members should be in camel case: `SomeStruct.firstMember`.</span></span>  
*   <span data-ttu-id="989fe-118">Objekte: JavaScript-Objekte sind nicht identisch mit verwalteten Code Objekten \ ( `System.Object` \).</span><span class="sxs-lookup"><span data-stu-id="989fe-118">Objects: JavaScript objects aren't the same as managed code objects \(`System.Object`\).</span></span>  <span data-ttu-id="989fe-119">Sie können ein JavaScript-Objekt nicht an eine Windows-Runtime-Methode übergeben, für die ein `System.Object` .</span><span class="sxs-lookup"><span data-stu-id="989fe-119">You can't pass a JavaScript object to a Windows Runtime method that requires a `System.Object`.</span></span>  
*   <span data-ttu-id="989fe-120">Objektidentität: in den meisten Fällen ändern sich die Objekte, die zwischen der Windows-Runtime und JavaScript hin-und hergeleitet werden, nicht.</span><span class="sxs-lookup"><span data-stu-id="989fe-120">Object identity: In most cases, the objects passed back and forth between the Windows Runtime and JavaScript do not change.</span></span>  <span data-ttu-id="989fe-121">Das JavaScript-Modul verwaltet eine Karte mit bekannten Objekten.</span><span class="sxs-lookup"><span data-stu-id="989fe-121">The JavaScript engine maintains a map of known objects.</span></span>  <span data-ttu-id="989fe-122">Wenn ein Objekt von der Windows-Runtime zurückgegeben wird, wird es mit der Zuordnung abgeglichen, und wenn es nicht vorhanden ist, wird ein neues Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="989fe-122">When an object is returned from the Windows Runtime it is matched against the map, and if it does not exist a new object is created.</span></span>  <span data-ttu-id="989fe-123">Das gleiche Verfahren wird für Objekte befolgt, die Schnittstellen darstellen, die von Windows-Runtime-Methoden zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="989fe-123">The same procedure is followed for objects that represent interfaces that are returned by Windows Runtime methods.</span></span>  <span data-ttu-id="989fe-124">Es gibt zwei Arten von Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="989fe-124">There are two kinds of exceptions:</span></span>  

    *   <span data-ttu-id="989fe-125">Objekte, die von einem Windows-Runtime-Aufruf zurückgegeben werden und dann neue \ (Expando \)-Eigenschaften hinzugefügt wurden, behalten ihre neuen Eigenschaften nicht bei, wenn Sie an die Windows-Runtime zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="989fe-125">Objects that are returned from a Windows Runtime call, and then have new \(expando\) properties added, don't retain their new properties when they are passed back to the Windows Runtime.</span></span>  <span data-ttu-id="989fe-126">Wenn Sie jedoch an die JavaScript-App zurückgegeben werden, da Sie dem vorhandenen Objekt zugeordnet sind, verfügt das zurückgegebene Objekt über die Expando-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="989fe-126">However, when they are returned to the JavaScript app, because they're matched to the existing object, the returned object does have the expando properties.</span></span>  
    *   <span data-ttu-id="989fe-127">Strukturen und Stellvertretungen in der Windows-Runtime können nicht als identisch mit zuvor verwendeten Strukturen oder Stellvertretungen identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="989fe-127">Structures and delegates in Windows Runtime can't be identified as identical to previously-used structures or delegates.</span></span>  <span data-ttu-id="989fe-128">Jedes Mal, wenn eine Struktur oder ein Delegat zurückgegeben wird, wird ein neuer Verweis abgerufen.</span><span class="sxs-lookup"><span data-stu-id="989fe-128">Every time a structure or delegate is returned, it gets a new reference.</span></span>  

*   <span data-ttu-id="989fe-129">Namenskollisionen: mehrere Windows-Runtime-Schnittstellen verfügen möglicherweise über Member mit denselben Namen.</span><span class="sxs-lookup"><span data-stu-id="989fe-129">Name collisions: Multiple Windows Runtime interfaces may have members with the same names.</span></span>  <span data-ttu-id="989fe-130">Wenn Sie in einem einzelnen JavaScript-Objekt kombiniert werden (Dies kann eine Darstellung einer Runtime-Klasse oder einer Schnittstelle sein), werden die Member durch vollqualifizierte Namen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="989fe-130">If they are combined in a single JavaScript object (which can be a representation of a runtime class or an interface), the members are represented with fully-qualified names.</span></span>  <span data-ttu-id="989fe-131">Sie können diese Member mithilfe der folgenden Syntax aufrufen:</span><span class="sxs-lookup"><span data-stu-id="989fe-131">You can call these members by using the following syntax:</span></span>  
    
    ```cpp
    Class["MemberName"](parameter)
    ```  
    
    <span data-ttu-id="989fe-132">Im folgenden Code verfügen zwei Schnittstellen über eine Draw-Methode, und eine Runtime-Klasse implementiert beide Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="989fe-132">In the following code, two interfaces have a Draw method, and a runtime class implements both interfaces.</span></span>  
    
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
    
    <span data-ttu-id="989fe-133">Hier erfahren Sie, wie Sie den obigen Code in JavaScript aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="989fe-133">Here is how you can call the above code in JavaScript.</span></span>  
    
    ```javascript
    var example = new ExampleObject();
    example["CollisionExample.InterfaceA.draw"](12);
    example["CollisionExample.InterfaceB.draw"]("hello");
    ```  
    
*   `Out` <span data-ttu-id="989fe-134">Parameter: Wenn eine Windows-Runtime-Methode über mehrere `out` Parameter verfügt, verfügt die Methode in JavaScript über ein JavaScript-Objekt als Rückgabewert, und das Objekt verfügt über Eigenschaften, die dem `out` Parameter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="989fe-134">parameters: If a Windows Runtime method has multiple `out` parameters, in JavaScript the method has a JavaScript object as its return value, and the object has properties that correspond to the `out` parameter.</span></span>  <span data-ttu-id="989fe-135">Nehmen Sie beispielsweise die folgende Windows-Runtime-Signatur in C++ in Frage.</span><span class="sxs-lookup"><span data-stu-id="989fe-135">For example, consider the following Windows Runtime signature in C++.</span></span>  
    
    ```cpp
    void ExampleMethod(
      [OutAttribute] char^ first,
      [OutAttribute] char^ second
    )
    ```  
    
    <span data-ttu-id="989fe-136">Die JavaScript-Version dieser Signatur lautet:</span><span class="sxs-lookup"><span data-stu-id="989fe-136">The JavaScript version of this signature is:</span></span>  
    
    ```javascript
    var returnValue = exampleMethod();
    ```  
    
    <span data-ttu-id="989fe-137">In diesem Beispiel `returnValue` ist ein JavaScript-Objekt mit zwei Feldern: `first` und `second` .</span><span class="sxs-lookup"><span data-stu-id="989fe-137">In this example, `returnValue` is a JavaScript object that has two fields: `first` and `second`.</span></span>  
    
*   <span data-ttu-id="989fe-138">Statische Member: die Windows-Runtime definiert sowohl statische Member als auch Instanzmember.</span><span class="sxs-lookup"><span data-stu-id="989fe-138">Static members: The Windows Runtime defines both static members and instance members.</span></span>  <span data-ttu-id="989fe-139">In JavaScript werden statische Member dem Objekt hinzugefügt, das der Windows-Runtime-Klasse oder-Schnittstelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="989fe-139">In JavaScript, static members are added to the object that is associated with the Windows Runtime class or interface.</span></span>  
    
    ```javascript
    // Static method.
    var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
    // Instance method.
    var reading = accel.getCurrentReading();
    ```  
    
<span data-ttu-id="989fe-140">Weitere Informationen zur JavaScript-Darstellung von Windows-Runtime Basic-Typen finden Sie unter [JavaScript-Darstellung von Windows-Runtime-Typen][WindowsRuntimeJavascriptTypes].</span><span class="sxs-lookup"><span data-stu-id="989fe-140">For more information about the JavaScript representation of Windows Runtime basic types, see [JavaScript Representation of Windows Runtime Types][WindowsRuntimeJavascriptTypes].</span></span>  

<!-- image links -->  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: /microsoft-edge/windows-runtime/javascript-representation-of-windows-runtime-types "JavaScript-Darstellung von Windows-Runtime-Typen"

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Komponenten für Windows-Runtime mit C++/CX"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Komponenten für Windows-Runtime mit C# und Visual Basic"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  