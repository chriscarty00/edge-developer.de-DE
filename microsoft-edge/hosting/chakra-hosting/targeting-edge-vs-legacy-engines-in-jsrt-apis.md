---
description: 'Hier erfahren Sie, wie Sie auf die verschiedenen Windows 10-JavaScript-Module abzielen. '
title: Targeting Microsoft Edge vs. Legacy Engines in JsRT-APIs | Microsoft docs
ms.custom: ''
ms.date: 03/05/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: cbc7df6c-0bc9-48f5-b9ad-b9ed31c42f92
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ed0dc8c67b8189a7433d52185aa995997edb70a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567185"
---
# <span data-ttu-id="b4635-103">Targeting Microsoft Edge vs. Legacy Engines in JsRT-APIs</span><span class="sxs-lookup"><span data-stu-id="b4635-103">Targeting Microsoft Edge vs. Legacy Engines in JsRT APIs</span></span>

<span data-ttu-id="b4635-104">Windows 10 unterstützt zwei verschiedene JavaScript-Module:</span><span class="sxs-lookup"><span data-stu-id="b4635-104">Windows 10 supports two different JavaScript engines:</span></span>

-   <span data-ttu-id="b4635-105">Das alte Chakra-Modul (auch als " *Legacy Modul* " oder "jscript9. dll" bezeichnet), das mit Internet Explorer 11 ausgeliefert wird und unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b4635-105">The old Chakra engine (also called the *legacy engine* or jscript9.dll below) that ships with and supports Internet Explorer 11.</span></span> <span data-ttu-id="b4635-106">Dieses Modul ist in der Zeit eingefroren und bleibt von der Win 8.1/IE11-Version grundsätzlich unverändert.</span><span class="sxs-lookup"><span data-stu-id="b4635-106">This engine is frozen in time and will remain fundamentally unchanged from Win8.1/IE11 release.</span></span>  
  
-   <span data-ttu-id="b4635-107">Das neue Chakra-Modul (auch als " *Edge-Engine* " oder "Chakra. dll" bezeichnet), das mit dem neuen Browser in Windows 10, Microsoft Edge, ausgeliefert wird und unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b4635-107">The new Chakra engine (also called the *Edge engine* or chakra.dll below) that ships with and supports the new browser in Windows 10, Microsoft Edge.</span></span> <span data-ttu-id="b4635-108">Dieses Modul wird kontinuierlich aktualisiert und unterstützt eine "lebendige" [Edge](https://blogs.msdn.com/b/ie/archive/2014/11/11/living-on-the-edge-our-next-step-in-interoperability.aspx) -Engine.</span><span class="sxs-lookup"><span data-stu-id="b4635-108">This engine will be continually updated and will support a "living" [Edge](https://blogs.msdn.com/b/ie/archive/2014/11/11/living-on-the-edge-our-next-step-in-interoperability.aspx) engine.</span></span> <span data-ttu-id="b4635-109">Eine lebendige Microsoft-Edge-Engine impliziert, dass die Microsoft-Edge-Engine im Gegensatz zur Legacy-Engine keine Form von Versions Skript Funktionalitäten für die Opt-in-Funktion weiterleiten würde.</span><span class="sxs-lookup"><span data-stu-id="b4635-109">A living Microsoft Edge engine implies that unlike the legacy engine, the Microsoft Edge engine would not carry forward any form of versioning script functionality to opt into.</span></span>  
  
 <span data-ttu-id="b4635-110">Wenn Sie eine App mithilfe der JavaScript-Runtime-Hosting-API (JsRT) erstellen, können Sie entweder das Legacy-oder das Microsoft Edge-Modul als Ziel auswählen.</span><span class="sxs-lookup"><span data-stu-id="b4635-110">When creating an app using the JavaScript Runtime Hosting (JsRT) API, you can choose to target either the legacy or the Microsoft Edge engine.</span></span>  
  
-   <span data-ttu-id="b4635-111">Wenn Sie die Abwärtskompatibilität Ihrer vorhandenen Anwendungen betonen möchten, sollten Sie auf das Legacy Modul Zielen.</span><span class="sxs-lookup"><span data-stu-id="b4635-111">If you need to emphasize backward compatibility of your existing applications, target the legacy engine.</span></span>  
  
-   <span data-ttu-id="b4635-112">Wenn Sie möchten, dass Ihre APP weitergeleitet wird und neue JavaScript-Features bei der Veröffentlichung unterstützt werden (beispielsweise ECMAScript 6), richten Sie das Microsoft Edge-Modul aus.</span><span class="sxs-lookup"><span data-stu-id="b4635-112">If you want your app to be forward looking and support new JavaScript features as they are released (for example, ECMAScript 6), target the Microsoft Edge engine.</span></span>  
  
 <span data-ttu-id="b4635-113">Dieses Thema enthält Details, in denen beschrieben wird, wie die verschiedenen Module ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="b4635-113">This topic includes details that describe how to target the different engines.</span></span>  
  
## <span data-ttu-id="b4635-114">Ziel ihrer bevorzugten Version</span><span class="sxs-lookup"><span data-stu-id="b4635-114">Target your preferred version</span></span>  
 <span data-ttu-id="b4635-115">Wenn Sie eine APP erstellen, können Sie die Version der JsRT auswählen, die entweder das Microsoft Edge-Modul oder das Legacy Modul unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b4635-115">When creating an app, you can select the version of the JsRT that supports either the Microsoft Edge engine or the legacy engine.</span></span> <span data-ttu-id="b4635-116">Sie können die JsRT-Version auf der Grundlage der obigen Richtlinien auswählen.</span><span class="sxs-lookup"><span data-stu-id="b4635-116">You can choose the JsRT version based on the guidelines above.</span></span> <span data-ttu-id="b4635-117">Um diese Unterschiede berücksichtigen zu können, wurden die folgenden Änderungen an `JsCreateRuntime` , `JsCreateContext` und vorgenommen `JsStartDebugging` .</span><span class="sxs-lookup"><span data-stu-id="b4635-117">To accommodate these distinctions, the following changes have been made to `JsCreateRuntime`, `JsCreateContext`, and `JsStartDebugging`.</span></span>  
  
 <span data-ttu-id="b4635-118">Für `JsCreateRuntime` :</span><span class="sxs-lookup"><span data-stu-id="b4635-118">For `JsCreateRuntime`:</span></span>  
  
-   <span data-ttu-id="b4635-119">Beim Targeting auf das Legacy Modul `JsRuntimeVersionEdge` ist der Enumerationswert veraltet, und eine Meldung schlägt stattdessen die Verwendung des `JsRuntimeVersionInternetExplorer11` Werts vor.</span><span class="sxs-lookup"><span data-stu-id="b4635-119">When targeting the legacy engine, the `JsRuntimeVersionEdge` enumeration value is deprecated, and a message will suggest using the `JsRuntimeVersionInternetExplorer11` value instead.</span></span>  
  
-   <span data-ttu-id="b4635-120">Bei der Ausrichtung auf das Microsoft-Edge-Modul wird der Versionsparameter in der `JsCreateRuntime` Funktion ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="b4635-120">When targeting the Microsoft Edge engine, the version parameter is omitted from the `JsCreateRuntime` function.</span></span>  
  
    ```cpp  
    JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
    ```  
  
 <span data-ttu-id="b4635-121">Für `JsCreateContext` und `JsStartDebugging` :</span><span class="sxs-lookup"><span data-stu-id="b4635-121">For `JsCreateContext` and `JsStartDebugging`:</span></span>  
  
-   <span data-ttu-id="b4635-122">Wenn Sie das Legacy Modul verwenden, `IDebugApplication` wird die Schnittstelle verwendet, um Ihre eigenen nicht Remotedebuggen-Methoden bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b4635-122">When targeting the legacy engine, the `IDebugApplication` interface is used to supply your own non-remote debugging methods.</span></span> <span data-ttu-id="b4635-123">Zu Debugging-Zwecken, `JsCreateContext` und `JsStartDebugging` die Funktionen werden `IDebugApplication` als Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="b4635-123">For debugging purposes, `JsCreateContext` and `JsStartDebugging` functions take `IDebugApplication` as parameter.</span></span>  
  
-   <span data-ttu-id="b4635-124">Bei der Ausrichtung auf das Microsoft Edge-Modul `IDebugApplication` ist die Schnittstelle veraltet.</span><span class="sxs-lookup"><span data-stu-id="b4635-124">When targeting the Microsoft Edge engine, the `IDebugApplication` interface is deprecated.</span></span> <span data-ttu-id="b4635-125">Das Chakra-Modul ermöglicht die systemeigene und Skriptdebugging-Funktion mit dem Visual Studio-Debugger, ohne dass eine Implementierung des Benutzers erforderlich ist `IDebugApplication` .</span><span class="sxs-lookup"><span data-stu-id="b4635-125">The Chakra engine enables native and script debugging capability with Visual Studio debugger without requiring an implementation of `IDebugApplication` from user.</span></span> <span data-ttu-id="b4635-126">Die Schnittstelle ist nicht mehr ein Parameter für `JsCreateContext` und `JsStartDebugging` als Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="b4635-126">The interface is no longer a parameter for `JsCreateContext` and `JsStartDebugging` as a result.</span></span>  
  
 <span data-ttu-id="b4635-127">Die Signaturen für die vorherigen APIs im Legacy Modul lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b4635-127">The signatures for the preceding APIs in the legacy engine are as follows:</span></span>  
  
```cpp  
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsRuntimeVersion version, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
  
JsErrorCode JsCreateContext(JsRuntimeHandle runtime, IDebugApplication *debugApplication, JsContextRef *newContext);  
  
JsErrorCode JsStartDebugging(IDebugApplication *debugApplication);  
```  
  
 <span data-ttu-id="b4635-128">Die Signaturen für die vorhergehenden APIs im Microsoft Edge-Modul lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b4635-128">The signatures for the preceding APIs in the Microsoft Edge engine are as follows:</span></span>  
  
```cpp  
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
  
JsErrorCode JsCreateContext(JsRuntimeHandle runtime, JsContextRef *newContext);  
  
JsErrorCode JsStartDebugging();  
```  
  
## <span data-ttu-id="b4635-129">Kompilieren für Ihre bevorzugte Version mit Visual C++</span><span class="sxs-lookup"><span data-stu-id="b4635-129">Compile for your preferred version using Visual C++</span></span>  
 <span data-ttu-id="b4635-130">Wenn Sie Visual C++ verwenden, importieren Sie die JsRT-API, indem Sie den JsRT. h-Header einschließen, und stellen Sie sicher, dass JsRT. lib in der Liste der Linker-Eingabedateien enthalten ist:</span><span class="sxs-lookup"><span data-stu-id="b4635-130">When using Visual C++, import the JsRT API by including the jsrt.h header, and ensure that jsrt.lib is included in your linker input files list:</span></span>  
  
```cpp  
#include <jsrt.h>  
```  
  
 ![Hinzufügen von jsrt. lib als Linker-Eingabedatei](../chakra-hosting/media/js-chakra.png "JS_Chakra_")  
  
 <span data-ttu-id="b4635-132">Wenn Sie die Microsoft-Edge-Engine-Binärdateien als Ziel festlegen möchten, müssen Sie das Makro `USE_EDGEMODE_JSRT` vor dem einschließen von jsrt. h definieren, und statt mit jsrt. lib zu verknüpfen, sollten Sie einen Link zu chakrart. lib erstellen:</span><span class="sxs-lookup"><span data-stu-id="b4635-132">If you want to target the Microsoft Edge engine binaries, you need to define the macro `USE_EDGEMODE_JSRT` before including jsrt.h, and instead of linking against jsrt.lib, you should link against chakrart.lib:</span></span>  
  
```cpp  
#define USE_EDGEMODE_JSRT  
#include <jsrt.h>  
```  
  
 ![Hinzufügen von chakrart. lib als Linker-Eingabedatei](../chakra-hosting/media/js-chakra-hosting.png "JS_Chakra_Hosting_")  
  
 <span data-ttu-id="b4635-134">Wenn Sie mit einer neuen Anwendung beginnen, können Sie jetzt mit dem Schreiben von Code für die JsRT-API beginnen.</span><span class="sxs-lookup"><span data-stu-id="b4635-134">If you're starting with a new application, you are now ready to start writing code against the JsRT API.</span></span>  
  
## <span data-ttu-id="b4635-135">Kompilieren für Ihre bevorzugte Version mit .net</span><span class="sxs-lookup"><span data-stu-id="b4635-135">Compile for your preferred version using .NET</span></span>  
 <span data-ttu-id="b4635-136">Wenn Sie .net und P/Invoke verwenden, müssen Sie Ihre JsRT-API [DllImport]-Deklarationen so ändern, dass Sie "Chakra. dll" anstelle von "jscript9. dll" importieren.</span><span class="sxs-lookup"><span data-stu-id="b4635-136">If you're using .NET and P/Invoke, you must change your JsRT API [DllImport] declarations to import chakra.dll instead of jscript9.dll.</span></span> <span data-ttu-id="b4635-137">Darüber hinaus ändern Sie die Definition von `JsCreateRuntime` , um den Parameter `JsRuntimeVersion` und die Definition von zu entfernen `JsCreateContext` und `JsStartDebugging` den `IDebugApplication` Parameter zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="b4635-137">In addition, change the definition of `JsCreateRuntime` to remove the `JsRuntimeVersion` parameter and the definition of `JsCreateContext` and `JsStartDebugging` to remove the `IDebugApplication` parameter.</span></span>  
  
 <span data-ttu-id="b4635-138">Verwenden Sie für das Legacy Modul den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="b4635-138">For the legacy engine, use the following code.</span></span>  
  
```c#  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsCreateRuntime(  
    JsRuntimeAttributes attributes,  
    JsRuntimeVersion version,  
    JsThreadServiceCallback callback,  
    out JsRuntimeSafeHandle runtime  
);  
  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsCreateContext(  
    JsRuntimeSafeHandle runtime,  
    IDebugApplication debugApplication,  
    out JsContextRef newContext  
);   
  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsStartDebugging(  
    IDebugApplication debugApplication,  
);  
```  
  
 <span data-ttu-id="b4635-139">Verwenden Sie für das Microsoft Edge-Modul den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="b4635-139">For the Microsoft Edge engine, use the following code.</span></span>  
  
```c#  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsCreateRuntime(  
    JsRuntimeAttributes attributes,  
    JsThreadServiceCallback callback,  
    out JsRuntimeSafeHandle runtime  
);  
  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsCreateContext(  
    JsRuntimeSafeHandle runtime,  
    out JsContextRef newContext  
);   
  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsStartDebugging();  
```  
  
> [!CAUTION]
>  <span data-ttu-id="b4635-140">Wenn Sie den Funktionszeiger manuell Marshallen (beispielsweise über LoadLibrary/GetProcAddress), ist es wichtig, dass Sie die Deklarationen der Methode nicht vermischen, oder Sie werden den Stapel aufheben, was zu einem unvorhersehbaren Verhalten führt, wie beispielsweise, dass die APP abstürzt.</span><span class="sxs-lookup"><span data-stu-id="b4635-140">If you are manually marshaling the function pointer (such as via LoadLibrary/GetProcAddress), it is critical that you do not mix the declarations of the method, or else you will unbalance the stack, which will result in unpredictable behavior such as causing your app to crash.</span></span> <span data-ttu-id="b4635-141">Das gleiche Problem tritt auf, wenn Sie eine globale Suche-und-Ersetzung von Instanzen von jscript9. dll im Import Code durchführen, da Sie den Parameter verpassen, der `version` gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="b4635-141">The same problem will occur if you perform a global search-and-replace of instances of jscript9.dll in your import code, because you'll miss the `version` parameter being dropped.</span></span>  
  
## <span data-ttu-id="b4635-142">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b4635-142">Summary</span></span>  
 <span data-ttu-id="b4635-143">In Windows 10 werden die JavaScript-Runtime-Hosting-APIs in zwei aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="b4635-143">In Windows 10, the JavaScript Runtime Hosting APIs are splitting into two.</span></span> <span data-ttu-id="b4635-144">Diese APIs unterstützen nun eine "lebendige" Microsoft Edge-Engine, deren Sprachfunktionen mit dem Microsoft Edge-Modul "Living" in Microsoft Edge ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="b4635-144">These APIs now support a "living" Microsoft Edge engine, whose language capabilities will be aligned with the "living" Microsoft Edge engine in the Microsoft Edge.</span></span> <span data-ttu-id="b4635-145">Sie können diese Funktionen von Ihren Desktop-oder Store-Apps nutzen, um neue und aufregende Möglichkeiten zum Erweitern Ihrer Anwendung und zur Nutzung moderner Webkenntnisse in Ihrer vorhandenen CodeBase zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="b4635-145">You can leverage these capabilities from your desktop or Store apps to create new and exciting ways to extend your application and to leverage modern Web skills in your existing code base.</span></span> <span data-ttu-id="b4635-146">Da es jedoch subtile Unterschiede zwischen früheren Versionen gibt, müssen Sie bei der Ausrichtung auf das Edge-oder Legacy Modul die folgenden Punkte beachten.</span><span class="sxs-lookup"><span data-stu-id="b4635-146">However, because there are subtle differences between previous versions, you must be aware of the following points when targeting the Edge or legacy engine.</span></span>  
  
-   <span data-ttu-id="b4635-147">Ihre APP kann pro Prozess nur eine Version von JsRT unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b4635-147">Your app can support only one version of JsRT per process.</span></span>  
  
     <span data-ttu-id="b4635-148">So können Sie beispielsweise keine Microsoft Edge Engine-Laufzeit und dann eine Legacy Modul-Laufzeit erstellen und davon ausgehen, dass Sie im gleichen Prozess ordnungsgemäß ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b4635-148">For example, you can't create a Microsoft Edge engine runtime and then a legacy engine runtime and expect them to run correctly in the same process.</span></span> <span data-ttu-id="b4635-149">Dies wird nicht unterstützt und kann zu einem undokumentierten Verhalten führen, beispielsweise beim Laden der zweiten dll.</span><span class="sxs-lookup"><span data-stu-id="b4635-149">This is unsupported and may result in undocumented behavior, such as failure to load the second DLL.</span></span>  
  
-   <span data-ttu-id="b4635-150">Bei der Ausrichtung auf das Microsoft Edge-Modul kann Ihre APP unerwartete neue Features erwerben, wenn die zugrunde liegende Plattform automatisch aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b4635-150">When targeting the Microsoft Edge engine, your app may unexpectedly acquire new features when the underlying platform is automatically updated.</span></span>  
  
     <span data-ttu-id="b4635-151">Beispielsweise unterstützt der Internet Explorer 11-Modus der Legacy-Laufzeit Block bereichsübergreifende Variablendeklarationen wie `let` und `const` .</span><span class="sxs-lookup"><span data-stu-id="b4635-151">For example, the Internet Explorer 11 mode of the legacy runtime supports block-scoping variable declarations such as `let` and `const`.</span></span> <span data-ttu-id="b4635-152">Wenn das Verhalten der automatischen Versionsverwaltung von Microsoft Edge Engine zuvor der Standard war, wurde möglicherweise der Code, der im Internet Explorer 10-Modus funktionierte, der keine Regeln für das Blockieren von Gültigkeitsbereichen aufwies, beim automatischen Upgrade der Plattform gestartet.</span><span class="sxs-lookup"><span data-stu-id="b4635-152">If the Microsoft Edge engine automatic versioning behavior had been the standard previously, code that had worked in Internet Explorer 10 mode, which did not have block-scoping rules, may have started failing when the platform had automatically upgraded.</span></span> <span data-ttu-id="b4635-153">Dies muss bei der Auswahl des zu verwendenden Laufzeitmodells berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="b4635-153">This must be a consideration when choosing which runtime model to use.</span></span> <span data-ttu-id="b4635-154">Obwohl wir der Meinung sind, dass Sie die Microsoft Edge-Engine nach Möglichkeit ansprechen sollten, müssen Sie bei der Verwendung von JavaScript-Code Strukturen vorsichtig sein, die in Zukunft ungültig werden können.</span><span class="sxs-lookup"><span data-stu-id="b4635-154">While we believe you should target the Microsoft Edge engine whenever possible, you must be careful about using JavaScript code structures that may become invalid in the future.</span></span>  
  
-   <span data-ttu-id="b4635-155">JsRT für den Windows Store unterstützt nur die Microsoft Edge Engine (Chakra. dll).</span><span class="sxs-lookup"><span data-stu-id="b4635-155">JsRT for the Windows Store only supports the Microsoft Edge engine (chakra.dll).</span></span> <span data-ttu-id="b4635-156">Für apps, die versuchen, eine Verknüpfung mit einer JsRT-API in jscript9. dll herzustellen, wird die Zertifizierung nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4635-156">Apps attempting to link against any JsRT API in jscript9.dll will fail certification.</span></span>  
  
-   <span data-ttu-id="b4635-157">Es ist wichtig, dass Sie die Deklaration von `JsCreateRuntime` `JsCreateContext` und `JsStartDebugging` zwischen jscript9. dll und Chakra. dll nicht verwechseln, da dies zu einem Unwuchten des Stapels führt.</span><span class="sxs-lookup"><span data-stu-id="b4635-157">It is critical that you do not confuse the declaration of `JsCreateRuntime`, `JsCreateContext`, and `JsStartDebugging` between jscript9.dll and chakra.dll, because it will result in imbalancing the stack.</span></span>  
  
     <span data-ttu-id="b4635-158">Wenn Sie C und C++ verwenden, wird ein linker-Fehler angezeigt, wenn Sie versuchen, die falsche Deklaration zu verwenden, solange Sie nicht so etwas wie Anrufe `LoadLibrary` und dann tun `GetProcAddress` .</span><span class="sxs-lookup"><span data-stu-id="b4635-158">When using C and C++, you will receive a linker error if you try to use the wrong declaration, as long as you're not doing something like calling `LoadLibrary` and then `GetProcAddress`.</span></span> <span data-ttu-id="b4635-159">.NET-Entwickler finden dieses Problem möglicherweise nicht so einfach, also überprüfen Sie Ihren Code, wenn Sie dieses Feature verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4635-159">.NET developers may not find this problem as easily, so double-check your code when using this feature.</span></span>  
  
## <span data-ttu-id="b4635-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b4635-160">See Also</span></span>  
 [<span data-ttu-id="b4635-161">JavaScript-Runtime-Hosting</span><span class="sxs-lookup"><span data-stu-id="b4635-161">JavaScript Runtime Hosting</span></span>](../javascript-runtime-hosting.md)
 