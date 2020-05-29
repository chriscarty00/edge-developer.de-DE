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
# Targeting Microsoft Edge vs. Legacy Engines in JsRT-APIs

Windows 10 unterstützt zwei verschiedene JavaScript-Module:

-   Das alte Chakra-Modul (auch als " *Legacy Modul* " oder "jscript9. dll" bezeichnet), das mit Internet Explorer 11 ausgeliefert wird und unterstützt. Dieses Modul ist in der Zeit eingefroren und bleibt von der Win 8.1/IE11-Version grundsätzlich unverändert.  
  
-   Das neue Chakra-Modul (auch als " *Edge-Engine* " oder "Chakra. dll" bezeichnet), das mit dem neuen Browser in Windows 10, Microsoft Edge, ausgeliefert wird und unterstützt. Dieses Modul wird kontinuierlich aktualisiert und unterstützt eine "lebendige" [Edge](https://blogs.msdn.com/b/ie/archive/2014/11/11/living-on-the-edge-our-next-step-in-interoperability.aspx) -Engine. Eine lebendige Microsoft-Edge-Engine impliziert, dass die Microsoft-Edge-Engine im Gegensatz zur Legacy-Engine keine Form von Versions Skript Funktionalitäten für die Opt-in-Funktion weiterleiten würde.  
  
 Wenn Sie eine App mithilfe der JavaScript-Runtime-Hosting-API (JsRT) erstellen, können Sie entweder das Legacy-oder das Microsoft Edge-Modul als Ziel auswählen.  
  
-   Wenn Sie die Abwärtskompatibilität Ihrer vorhandenen Anwendungen betonen möchten, sollten Sie auf das Legacy Modul Zielen.  
  
-   Wenn Sie möchten, dass Ihre APP weitergeleitet wird und neue JavaScript-Features bei der Veröffentlichung unterstützt werden (beispielsweise ECMAScript 6), richten Sie das Microsoft Edge-Modul aus.  
  
 Dieses Thema enthält Details, in denen beschrieben wird, wie die verschiedenen Module ausgerichtet werden.  
  
## Ziel ihrer bevorzugten Version  
 Wenn Sie eine APP erstellen, können Sie die Version der JsRT auswählen, die entweder das Microsoft Edge-Modul oder das Legacy Modul unterstützt. Sie können die JsRT-Version auf der Grundlage der obigen Richtlinien auswählen. Um diese Unterschiede berücksichtigen zu können, wurden die folgenden Änderungen an `JsCreateRuntime` , `JsCreateContext` und vorgenommen `JsStartDebugging` .  
  
 Für `JsCreateRuntime` :  
  
-   Beim Targeting auf das Legacy Modul `JsRuntimeVersionEdge` ist der Enumerationswert veraltet, und eine Meldung schlägt stattdessen die Verwendung des `JsRuntimeVersionInternetExplorer11` Werts vor.  
  
-   Bei der Ausrichtung auf das Microsoft-Edge-Modul wird der Versionsparameter in der `JsCreateRuntime` Funktion ausgelassen.  
  
    ```cpp  
    JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
    ```  
  
 Für `JsCreateContext` und `JsStartDebugging` :  
  
-   Wenn Sie das Legacy Modul verwenden, `IDebugApplication` wird die Schnittstelle verwendet, um Ihre eigenen nicht Remotedebuggen-Methoden bereitzustellen. Zu Debugging-Zwecken, `JsCreateContext` und `JsStartDebugging` die Funktionen werden `IDebugApplication` als Parameter verwendet.  
  
-   Bei der Ausrichtung auf das Microsoft Edge-Modul `IDebugApplication` ist die Schnittstelle veraltet. Das Chakra-Modul ermöglicht die systemeigene und Skriptdebugging-Funktion mit dem Visual Studio-Debugger, ohne dass eine Implementierung des Benutzers erforderlich ist `IDebugApplication` . Die Schnittstelle ist nicht mehr ein Parameter für `JsCreateContext` und `JsStartDebugging` als Ergebnis.  
  
 Die Signaturen für die vorherigen APIs im Legacy Modul lauten wie folgt:  
  
```cpp  
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsRuntimeVersion version, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
  
JsErrorCode JsCreateContext(JsRuntimeHandle runtime, IDebugApplication *debugApplication, JsContextRef *newContext);  
  
JsErrorCode JsStartDebugging(IDebugApplication *debugApplication);  
```  
  
 Die Signaturen für die vorhergehenden APIs im Microsoft Edge-Modul lauten wie folgt:  
  
```cpp  
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
  
JsErrorCode JsCreateContext(JsRuntimeHandle runtime, JsContextRef *newContext);  
  
JsErrorCode JsStartDebugging();  
```  
  
## Kompilieren für Ihre bevorzugte Version mit Visual C++  
 Wenn Sie Visual C++ verwenden, importieren Sie die JsRT-API, indem Sie den JsRT. h-Header einschließen, und stellen Sie sicher, dass JsRT. lib in der Liste der Linker-Eingabedateien enthalten ist:  
  
```cpp  
#include <jsrt.h>  
```  
  
 ![Hinzufügen von jsrt. lib als Linker-Eingabedatei](../chakra-hosting/media/js-chakra.png "JS_Chakra_")  
  
 Wenn Sie die Microsoft-Edge-Engine-Binärdateien als Ziel festlegen möchten, müssen Sie das Makro `USE_EDGEMODE_JSRT` vor dem einschließen von jsrt. h definieren, und statt mit jsrt. lib zu verknüpfen, sollten Sie einen Link zu chakrart. lib erstellen:  
  
```cpp  
#define USE_EDGEMODE_JSRT  
#include <jsrt.h>  
```  
  
 ![Hinzufügen von chakrart. lib als Linker-Eingabedatei](../chakra-hosting/media/js-chakra-hosting.png "JS_Chakra_Hosting_")  
  
 Wenn Sie mit einer neuen Anwendung beginnen, können Sie jetzt mit dem Schreiben von Code für die JsRT-API beginnen.  
  
## Kompilieren für Ihre bevorzugte Version mit .net  
 Wenn Sie .net und P/Invoke verwenden, müssen Sie Ihre JsRT-API [DllImport]-Deklarationen so ändern, dass Sie "Chakra. dll" anstelle von "jscript9. dll" importieren. Darüber hinaus ändern Sie die Definition von `JsCreateRuntime` , um den Parameter `JsRuntimeVersion` und die Definition von zu entfernen `JsCreateContext` und `JsStartDebugging` den `IDebugApplication` Parameter zu entfernen.  
  
 Verwenden Sie für das Legacy Modul den folgenden Code.  
  
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
  
 Verwenden Sie für das Microsoft Edge-Modul den folgenden Code.  
  
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
>  Wenn Sie den Funktionszeiger manuell Marshallen (beispielsweise über LoadLibrary/GetProcAddress), ist es wichtig, dass Sie die Deklarationen der Methode nicht vermischen, oder Sie werden den Stapel aufheben, was zu einem unvorhersehbaren Verhalten führt, wie beispielsweise, dass die APP abstürzt. Das gleiche Problem tritt auf, wenn Sie eine globale Suche-und-Ersetzung von Instanzen von jscript9. dll im Import Code durchführen, da Sie den Parameter verpassen, der `version` gelöscht wird.  
  
## Zusammenfassung  
 In Windows 10 werden die JavaScript-Runtime-Hosting-APIs in zwei aufgeteilt. Diese APIs unterstützen nun eine "lebendige" Microsoft Edge-Engine, deren Sprachfunktionen mit dem Microsoft Edge-Modul "Living" in Microsoft Edge ausgerichtet werden. Sie können diese Funktionen von Ihren Desktop-oder Store-Apps nutzen, um neue und aufregende Möglichkeiten zum Erweitern Ihrer Anwendung und zur Nutzung moderner Webkenntnisse in Ihrer vorhandenen CodeBase zu schaffen. Da es jedoch subtile Unterschiede zwischen früheren Versionen gibt, müssen Sie bei der Ausrichtung auf das Edge-oder Legacy Modul die folgenden Punkte beachten.  
  
-   Ihre APP kann pro Prozess nur eine Version von JsRT unterstützen.  
  
     So können Sie beispielsweise keine Microsoft Edge Engine-Laufzeit und dann eine Legacy Modul-Laufzeit erstellen und davon ausgehen, dass Sie im gleichen Prozess ordnungsgemäß ausgeführt werden. Dies wird nicht unterstützt und kann zu einem undokumentierten Verhalten führen, beispielsweise beim Laden der zweiten dll.  
  
-   Bei der Ausrichtung auf das Microsoft Edge-Modul kann Ihre APP unerwartete neue Features erwerben, wenn die zugrunde liegende Plattform automatisch aktualisiert wird.  
  
     Beispielsweise unterstützt der Internet Explorer 11-Modus der Legacy-Laufzeit Block bereichsübergreifende Variablendeklarationen wie `let` und `const` . Wenn das Verhalten der automatischen Versionsverwaltung von Microsoft Edge Engine zuvor der Standard war, wurde möglicherweise der Code, der im Internet Explorer 10-Modus funktionierte, der keine Regeln für das Blockieren von Gültigkeitsbereichen aufwies, beim automatischen Upgrade der Plattform gestartet. Dies muss bei der Auswahl des zu verwendenden Laufzeitmodells berücksichtigt werden. Obwohl wir der Meinung sind, dass Sie die Microsoft Edge-Engine nach Möglichkeit ansprechen sollten, müssen Sie bei der Verwendung von JavaScript-Code Strukturen vorsichtig sein, die in Zukunft ungültig werden können.  
  
-   JsRT für den Windows Store unterstützt nur die Microsoft Edge Engine (Chakra. dll). Für apps, die versuchen, eine Verknüpfung mit einer JsRT-API in jscript9. dll herzustellen, wird die Zertifizierung nicht ausgeführt.  
  
-   Es ist wichtig, dass Sie die Deklaration von `JsCreateRuntime` `JsCreateContext` und `JsStartDebugging` zwischen jscript9. dll und Chakra. dll nicht verwechseln, da dies zu einem Unwuchten des Stapels führt.  
  
     Wenn Sie C und C++ verwenden, wird ein linker-Fehler angezeigt, wenn Sie versuchen, die falsche Deklaration zu verwenden, solange Sie nicht so etwas wie Anrufe `LoadLibrary` und dann tun `GetProcAddress` . .NET-Entwickler finden dieses Problem möglicherweise nicht so einfach, also überprüfen Sie Ihren Code, wenn Sie dieses Feature verwenden.  
  
## Weitere Informationen  
 [JavaScript-Runtime-Hosting](../javascript-runtime-hosting.md)
 