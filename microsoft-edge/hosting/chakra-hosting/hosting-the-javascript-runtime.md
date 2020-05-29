---
description: Verwenden Sie die standardbasierte Chakra JavaScript-Engine, um Ihrer Windows-Anwendung Skriptfunktionen hinzuzufügen.
title: Hosten der JavaScript-Laufzeit | Microsoft docs
ms.custom: ''
ms.date: 01/15/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 30ec744e-57cc-4ef5-8fe1-d2c27b946548
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9077284d96ff0d9ae22e152329efe9304081ae39
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567349"
---
# Hosten der JavaScript-Laufzeit
Die APIs für JavaScript-Runtime (JsRT) bieten eine Möglichkeit für Desktop-, Windows Store-und serverseitige Anwendungen, die unter dem Windows-Betriebssystem ausgeführt werden, um der Anwendung mithilfe des standardbasierten Chakra JavaScript-Moduls, das auch von Microsoft Edge und Internet Explorer verwendet wird, Skriptfunktionen hinzuzufügen. Diese APIs sind unter Windows 10 und einer beliebigen Version des Windows-Betriebssystems verfügbar, auf dem Internet Explorer, Version 11,0, auf dem Computer installiert ist. Weitere Informationen finden Sie unter [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md). Informationen zur Verwendung von JsRT in Windows Store-Apps finden Sie unter [JsRT und die universelle Windows-Plattform](#Windows).  
  
> [!NOTE]
>  Diese Dokumentation setzt eine allgemeine Vertrautheit mit der JavaScript-Sprache voraus.  
  
## Konzepte  
 Wie Sie das JavaScript-Modul mithilfe der JsRT-APIs hosten, hängt von zwei Schlüsselkonzepten ab: Laufzeiten und Ausführungs Kontexten.  
  
 Eine *Common Language Runtime* stellt eine vollständige JavaScript-Ausführungsumgebung dar. Jede erstellte Laufzeit verfügt über einen eigenen isolierten Garbage Collection-Heap und standardmäßig über einen eigenen Just-in-time (JIT)-Compiler-Thread und einen Garbage Collector-Thread (GC). Ein *Ausführungskontext* stellt eine JavaScript-Umgebung dar, die ein eigenes JavaScript-globales Objekt hat, das sich von allen anderen Ausführungs Kontexten unterscheidet. Eine Laufzeit kann mehrere Ausführungskontexte enthalten, und in solchen Fällen teilen alle Ausführungskontexte den JIT-Compiler und den GC-Thread, der der Laufzeit zugeordnet ist.  
  
 Runtimes stellen einen einzelnen Ausführungsthread dar. In einem bestimmten Thread kann jeweils nur eine Laufzeit aktiv sein, und eine Laufzeit kann nur jeweils für einen Thread aktiv sein. Runtimes sind "Rental-threaded", sodass eine Runtime, die derzeit nicht in einem Thread aktiv ist (also keine JavaScript-Codes ausführt oder auf Anrufe vom Host reagiert), für alle Threads verwendet werden kann, auf denen noch keine aktive Laufzeit vorhanden ist.  
  
 Ausführungskontexte sind an eine bestimmte Laufzeit gebunden und führen Code innerhalb dieser Runtime aus. Im Gegensatz zu Laufzeiten können mehrere Ausführungskontexte gleichzeitig in einem Thread aktiv sein. Damit ein Host einen Aufruf in einem Ausführungskontext durchführen kann, kann dieser Ausführungskontext wieder an den Host zurückrufen, und der Host kann einen Aufruf in einen anderen Ausführungskontext führen.  
  
 ![Mehrere Ausführungskontexte](../chakra-hosting/media/js-chakra-hosting.png "JS_Chakra_Hosting")  
  
 In der Praxis kann ein einzelner Ausführungskontext verwendet werden, es sei denn, ein Host muss Code in getrennten Umgebungen ausführen. Auch wenn ein Host mehrere Codeabschnitte gleichzeitig ausführen muss, genügt eine einzige Laufzeit.  
  
## Speicherverwaltung  
 Bei JavaScript handelt es sich um eine Garbage Collection-Sprache, und es gibt daher verschiedene Aspekte, die beim Arbeiten mit den JsRT-APIs aus einer anderen Sprache berücksichtigt werden müssen.  
  
 Die wichtigste Überlegung ist, dass der JavaScript-Garbage Collector nur Verweise auf Werte an zwei Stellenanzeigen kann: den Heap der Laufzeit und den Stapel. Daher wird ein Verweis auf einen JavaScript-Wert, der in einem anderen JavaScript-Wert oder in einer lokalen Variablen auf dem Stapel gespeichert ist, immer vom Garbage Collector angezeigt. Verweise, die an anderen Speicherorten gespeichert sind, wie Heaps, die vom Host oder System verwaltet werden, werden vom Garbage Collector jedoch nicht angezeigt und können zu einer vorzeitigen Sammlung von Werten führen, die vom Host weiterhin verwendet werden.  
  
> [!IMPORTANT]
>  Bei einigen Sprachcompilern (wie dem Visual Studio C++-Compiler) werden lokale Variablen nach Möglichkeit optimiert. Es muss darauf geachtet werden, dass lokale Variablen, die auf JavaScript-Werte verweisen, auf dem Stapel liegen, wenn Sie davon ausgehen, dass diese Werte weiterhin aktiv sind.  
  
 Wenn ein Verweis auf einen JavaScript-Wert an einem Speicherort gespeichert wird, der für den Garbage Collector nicht sichtbar ist, muss der Host Verweise manuell mithilfe der JsRT-APIs hinzufügen und entfernen.  
  
## Ausnahmebehandlung  
 Wenn während der Skriptausführung eine JavaScript-Ausnahme auftritt, wird die enthaltende Laufzeit in einen Ausnahmezustand versetzt. In einem Ausnahmezustand kann kein Code ausgeführt werden, und alle API-Aufrufe schlagen mit dem Fehlercode fehl, `JsErrorInExceptionState` bis der Host die Ausnahme mithilfe der API abruft und löscht `JsGetAndClearException` . Wenn der Host von einem JavaScript-Rückruf zurückkehrt, ohne die Laufzeit aus einem Ausnahmezustand zu löschen, wird die JavaScript-Ausnahme erneut ausgelöst, sobald die Steuerung wieder an das JavaScript-Modul übergeben wird. Dadurch können Host Rückrufe auch eine JavaScript-Ausnahme auslösen, indem Sie die Laufzeit in einen Ausnahmezustand setzen und dann von einem Host Rückruf zurückkehren.  
  
 Einem Host ist es nicht gestattet, seine eigenen internen Ausnahmen über einen Host Rückruf zu übertragen – alle Rückrufmethoden müssen alle Host Ausnahmen abfangen, bevor Sie die Steuerung an die Laufzeit zurückgeben.  
  
## Laufzeit-Ressourcennutzung  
 Mit den JsRT-APIs wird eine Reihe von Möglichkeiten zum Überwachen und Ändern der Art und Weise der Verwendung von Ressourcen durch Runtimes verfügbar gemacht. Sie gliedern sich im Allgemeinen in die folgenden Kategorien:  
  
-   **Thread Verwendung**. Standardmäßig erstellt jede Laufzeit einen dedizierten JIT-Compiler-Thread und einen dedizierten GC-Thread, der diese Runtime bereitstellt. Wenn eine Common Language Runtime mit dem `JsRuntimeAttributeDisableBackgroundWork` Flag erstellt wird, werden die JIT-und die GC-Arbeit für den Laufzeitthread selbst und nicht für jedes einzelne Hintergrund-Threads ausgeführt. Ein Host kann auch einen Thread Dienst Rückruf für den Aufruf bereitstellen `JsCreateRuntime` , der es dem Host ermöglicht, JIT-und GC-Arbeit in einer Weise zu planen, in der es für Sie geeignet ist.  
  
-   **Speichernutzung**. Es gibt mehrere Möglichkeiten, die Speicherauslastung einer Laufzeit zu überwachen und zu ändern. Wenn die Laufzeit für längere Zeit ausgeführt wird, kann der Host das Flag angeben, `JsRuntimeAttributeEnableIdleProcessing` Wenn die Laufzeit erstellt und dann aufgerufen `JsIdle` wird, wenn sich der Host im Ruhezustand befindet. Dadurch kann das Modul einige Arbeitsspeicher Bereinigung und-Buchhaltung bis zur Leerlaufzeit aufschieben.  
  
     Der Host kann Garbage Collections durch Aufrufen überwachen `JsSetRuntimeBeforeCollectCallback` . Sie kann auch Zuordnungen überwachen, die vom Heap durch einen Aufruf durchgeführt werden `JsSetRuntimeMemoryAllocationCallback` . Beachten Sie, dass diese API nicht bei jeder JavaScript-Zuweisung zurückruft, nur wenn der Heap der Laufzeit mehr Speicherplatz benötigt. Der Speicher Zuweisungs Rückruf ist berechtigt, die Anforderung zu verweigern, wodurch eine Garbage Collection ausgelöst wird und, wenn kein Arbeitsspeicher verfügbar ist, ein Arbeitsspeicherfehler in der Laufzeit auftritt.  
  
     Der Host kann auch aufrufen `JsSetRuntimeMemoryLimit` , um einen Grenzwert für den Arbeitsspeicher festzulegen, den eine Laufzeit verwenden kann. Wenn eine Common Language Runtime auf eine Grenze trifft, wird eine Garbage Collection ausgelöst, und wenn kein Arbeitsspeicher verfügbar ist, wird ein Fehler aufgrund eines Arbeitsspeichers von der Laufzeit ausgelöst.  
  
-   **Skript Unterbrechung und-Auswertung** Der Host kann aufrufen `JsDisableRuntimeExecution` , um die Ausführung innerhalb einer Laufzeit zu terminieren. Dieser Anruf kann jederzeit und von jedem beliebigen Thread aus erfolgen. Da die Skript Beendigung davon abhängt, in den Code eingefügte Guard Points zu erreichen, wird ein Skript möglicherweise nicht zum exakten Zeitpunkt beendet, aber dies wird sehr kurz danach sein. Standardmäßig werden Termination Guard-Punkte in dem generierten Code konservativ plaziert und decken möglicherweise nicht alle Situationen ab, wie etwa eine Endlosschleife. Das Erstellen der Common Language Runtime mit dem `JsRuntimeAttributeAllowScriptInterrupt` Flag führt dazu, dass die Common Language Runtime zusätzliche Überprüfungen für Endlosschleifen einfügt, oft zu Lasten eines geringen Leistungsaufwands.  
  
     Wenn ein Host die Generierung von systemeigenem Code durch den JIT-Compiler nicht zulassen möchte, kann er das `JsRuntimeAttributeDisableNativeCodeGeneration` Flag angeben. Ein Host kann auch verhindern, dass Skripts dynamisch Skripts selbst ausführen, indem Sie das `JsRuntimeAttributeDisableEval` Flag angeben.  
  
## Debuggen und Profilerstellung  
 JsRT-APIs unterstützen das Debuggen und die Profilerstellung über die Active Scripting-Technologie.  
  
 Ab Windows 10 unterstützt das Chakra JavaScript-Modul das Legacy-Modul "Internet Explorer (MSHTML)" und "New Microsoft Edge (EdgeHTML)", und Sie können entweder in JsRT (siehe [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md) für Details). Das Debuggen eines Skripts in Visual Studio funktioniert unterschiedlich zwischen dem Legacy Modul und dem Microsoft Edge-Modul. Beim Legacy Modul muss der Host einen [IDebugApplication-Schnittstellen](/scripting/winscript/reference/idebugapplication-interface) Zeiger bereitstellen, der von einer [IProcessDebugManager-Schnittstellen](/scripting/winscript/reference/iprocessdebugmanager-interface) Instanz abgerufen werden kann. Mit dem Microsoft-Edge-Modul `IDebugApplication` ist veraltet, und das Chakra-Modul ermöglicht das systemeigene und Skriptdebugging über den Visual Studio-Debugger, ohne dass eine Implementierung des Benutzers erforderlich ist `IDebugApplication` .  
  
 Damit Skripts in einem Ausführungskontext debugfähigen werden, muss das Chakra-Modul auf die Verwendung von niedrigeren effizienten Code Ausführungsmethoden umschalten. Daher wird debugfähigen-Code in der Regel langsamer ausgeführt als nicht-debugfähigen-Code. Aus diesem Grund kann ein Host mit dem Legacy Modul entweder von Anfang an das Debuggen in einem Ausführungskontext starten, indem er den Zeiger im `IDebugApplication` Vordergrund bereitstellt `JsCreateContext` , oder es kann warten, bis das Debuggen erforderlich ist, und dann aufrufen `JsStartDebugging` . Mit dem Microsoft-Edge-Modul wird `JsCreateContext` kein Parameter mehr benötigt `IDebugApplication` , und infolgedessen wird das Skript nur debugfähigen, nachdem `JsStartDebugging` es aufgerufen wurde. Beim Debuggen mit Visual Studio muss die Debugger-Option "Skript" aktiviert sein.  
  
 Der JavaScript-Code in einem Ausführungskontext kann auf eine von zwei Arten profiliert werden. Die Befehlszeile Visual Studio Profiler (VSPerf. exe) kann in Windows 8,1 und höheren Versionen mit dem/js-Schalter verwendet werden, um einen Bericht zu erstellen, der auf den in der Anwendung ausgeführten JavaScript-Code ausgerichtet ist. Oder der Host kann direkt anrufen `JsStartProfiling` und `JsStopProfiling` einen Rückruf für die Profilerstellung selbst bereitstellen. Der Host kann den Zustand des Garbage Collection-Heaps auch durch Aufrufen untersuchen `JsEnumerateHeap` . Die Profilerstellung in JsRT funktioniert auf die gleiche Weise zwischen dem Legacy-und dem Microsoft Edge-Modul. JsRT-Profilerstellungs-APIs ( `JsStartProfiling` ,, `JsStopProfiling` `JsEnumerateHeap` , und `JsIsEnumeratingHeap` ) sind jedoch für universelle Windows-apps nicht verfügbar.  
  
<a name="Windows"></a>   
## JsRT und die universelle Windows-Plattform  

Sie können JsRT-APIs verwenden, um einer universellen Windows-App Skriptfunktionen hinzuzufügen. Eine universelle Windows-APP, die die JsRT-APIs verwendet, muss auf die Microsoft Edge JsRT-APIs ausgerichtet sein, die wiederum auf das Edge-Chakra-Modul ausgerichtet sind. Weitere Informationen finden Sie unter [Targeting für Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md). Die vollständige JsRT-API ist für universelle Windows-apps verfügbar, mit Ausnahme der Unterstützung für Profilierungs-und Heap Enumeration (,, `JsStartProfiling` `JsStopProfiling` `JsEnumerateHeap` und `JsIsEnumeratingHeap` werden nicht unterstützt).  
  
JsRT ermöglicht es Skripts auch, nativ auf alle [APIs für die universelle Windows-Plattform (UWP)](https://msdn.microsoft.com/library/windows/apps/br211377.aspx) zuzugreifen, nachdem der API-Namespace über die Microsoft Edge JsRT-API verfügbar gemacht wurde `JsProjectWinRTNamespace` . Während für universelle Windows-Anwendungen zusätzlich zur Projektion notwendiger Namespaces kein Setup erforderlich ist, muss in einer klassischen (Win32-) Windows-Anwendung ein com-initialisierter Delegierter Pumpmechanismus aktiviert werden, um `JsSetProjectionEnqueueCallback` Ereignisse und asynchrone APIs zu ermöglichen. Im folgenden Win32-Beispiel werden asynchrone UWP-APIs verwendet, um einen HTTP-Client zum Abrufen von Inhalten aus einem URI zu erstellen:  
  
```cpp  
typedef struct _jsCall {  
    JsProjectionCallback jsCallback;  
    JsProjectionCallbackContext jsContext;  
    HANDLE event;  
} jsCall;  
  
// Set up delegated pumping mechanism; not necessary in UWP applications.  
jsCall outstandingCall = {};  
CoInitializeEx(nullptr, COINIT_MULTITHREADED);  
JsSetProjectionEnqueueCallback([](JsProjectionCallback jsCallback,   
JsProjectionCallbackContext jsContext, void *callbackState) {  
    jsCall* call = (jsCall*)callbackState;  
    call->jsCallback = jsCallback;  
    call->jsContext = jsContext;  
    SetEvent(call->event);  
    },  
&outstandingCall);  
HANDLE event = CreateEventEx(NULL, NULL, CREATE_EVENT_MANUAL_RESET, EVENT_ALL_ACCESS);  
outstandingCall.event = event;  
  
// Project necessary namespaces.  
JsProjectWinRTNamespace(L"Windows.Foundation");  
JsProjectWinRTNamespace(L"Windows.Web");  
  
// Get content from an Uri.  
JsRunScript(L"var uri = new Windows.Foundation.Uri(\"http://somedatasource.com\"); " \  
    L"var httpClient = new Windows.Web.Http.HttpClient();" \  
    L"httpClient.getStringAsync(uri).done(function (content) { " \  
    L"    // do something with the string content " \    
    L"}, onError); " \  
    L"function onError(reason) { " \  
    L"    // error handling " \        
    L"}",   
    currentSourceContext, L"", &result);  
  
// Wait for async call to come in and then execute; not necessary in UWP applications.  
WaitForSingleObjectEx(outstandingCall.event, 10000, FALSE) == WAIT_OBJECT_0;  
outstandingCall.jsCallback(outstandingCall.jsContext);  
  
```  
  
## Weitere Informationen  
 [JavaScript-Runtime-Beispiel-App](https://go.microsoft.com/fwlink/p/?LinkID=306674&clcid=0x409)   
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)   
 [JavaScript-Runtime-Hosting](../javascript-runtime-hosting.md)  
 