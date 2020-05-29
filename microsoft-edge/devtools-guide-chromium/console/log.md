---
title: Erste Schritte mit der Protokollierung von Nachrichten in der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: d3dbec41bc1e53b5e9001551c796e5a495dd331e
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601733"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="385e8-103">Erste Schritte mit der Protokollierung von Nachrichten in der Konsole</span><span class="sxs-lookup"><span data-stu-id="385e8-103">Get Started With Logging Messages In The Console</span></span>   



<span data-ttu-id="385e8-104">In diesem interaktiven Lernprogramm erfahren Sie, wie Sie Nachrichten in der [Microsoft Edge devtools][MicrosoftEdgeDevTools] -Konsole protokollieren und filtern.</span><span class="sxs-lookup"><span data-stu-id="385e8-104">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

> ##### <span data-ttu-id="385e8-105">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="385e8-105">Figure 1</span></span>  
> <span data-ttu-id="385e8-106">Nachrichten in der Konsole</span><span class="sxs-lookup"><span data-stu-id="385e8-106">Messages in the Console</span></span>  
> ![Nachrichten in der Konsole][ImageLogExample]  

<span data-ttu-id="385e8-108">Dieses Lernprogramm soll in der entsprechenden Reihenfolge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="385e8-108">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="385e8-109">Es wird davon ausgegangen, dass Sie die Grundlagen der Webentwicklung verstehen, beispielsweise die Verwendung von JavaScript zum Hinzufügen von Interaktivität zu einer Seite.</span><span class="sxs-lookup"><span data-stu-id="385e8-109">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <span data-ttu-id="385e8-110">Einrichten der Demo-und DevTools</span><span class="sxs-lookup"><span data-stu-id="385e8-110">Set up the demo and DevTools</span></span>   

<span data-ttu-id="385e8-111">Dieses Lernprogramm ist so konzipiert, dass Sie die Demo öffnen und alle Workflows selbst ausprobieren können.</span><span class="sxs-lookup"><span data-stu-id="385e8-111">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="385e8-112">Wenn Sie physisch miteinander in Verbindung bleiben, können Sie die Workflows später wahrscheinlicher merken.</span><span class="sxs-lookup"><span data-stu-id="385e8-112">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="385e8-113">Halten `Control` Sie \ (Windows \) oder `Command` \ (macOS \) gedrückt, und klicken Sie auf **Konsolenprotokoll Beispiele** , um Sie in einer neuen Registerkarte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="385e8-113">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="385e8-114">Beispiele für Konsolen Protokolle</span><span class="sxs-lookup"><span data-stu-id="385e8-114">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!-- > [!TIP]
    > Move the demo to a separate window.  
    > 
    > > ##### old Figure 2  
    > > The tutorial on the left, and the demo on the right  
    > > ![The tutorial on the left, and the demo on the right][ImageLogSetUp1]  -->
    
1.  <span data-ttu-id="385e8-115">Konzentrieren Sie die Demo, und drücken Sie dann `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \), um devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="385e8-115">Focus the demo and then press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="385e8-116">Standardmäßig wird devtools rechts neben der Demo geöffnet.</span><span class="sxs-lookup"><span data-stu-id="385e8-116">By default DevTools opens to the right of the demo.</span></span>  
    
    > ##### <span data-ttu-id="385e8-117">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="385e8-117">Figure 2</span></span>  
    > <span data-ttu-id="385e8-118">DevTools wird rechts neben der Demo geöffnet</span><span class="sxs-lookup"><span data-stu-id="385e8-118">DevTools opens to the right of the demo</span></span>  
    > <span data-ttu-id="385e8-119">! [Devtools wird rechts neben der Demo geöffnet] [ImageDevToolsRight]</span><span class="sxs-lookup"><span data-stu-id="385e8-119">![DevTools opens to the right of the demo][ImageDevToolsRight]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="385e8-120">[Docken Sie devtools an den unteren Rand des Fensters an, oder Entdocken Sie es in einem separaten Fenster][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="385e8-120">[Dock DevTools to the bottom of the window or undock it into a separate window][DevToolsCustomizePlacement].</span></span>  
    
    > ##### <span data-ttu-id="385e8-121">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="385e8-121">Figure 3</span></span>  
    > <span data-ttu-id="385e8-122">DevTools angedockt am Ende der Demo</span><span class="sxs-lookup"><span data-stu-id="385e8-122">DevTools docked to the bottom of the demo</span></span>  
    > <span data-ttu-id="385e8-123">! [Devtools angedockt am Ende der Demo] [ImageDevToolsBottom]</span><span class="sxs-lookup"><span data-stu-id="385e8-123">![DevTools docked to the bottom of the demo][ImageDevToolsBottom]</span></span>  
    
    > ##### <span data-ttu-id="385e8-124">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="385e8-124">Figure 4</span></span>  
    > <span data-ttu-id="385e8-125">Browser in einem separaten Fenster</span><span class="sxs-lookup"><span data-stu-id="385e8-125">Browser in a separate window</span></span>  
    > <span data-ttu-id="385e8-126">! [Browser in einem separaten Fenster] [ImageDevToolsSeparateBrowse]</span><span class="sxs-lookup"><span data-stu-id="385e8-126">![Browser in a separate window][ImageDevToolsSeparateBrowse]</span></span>  
    
    > ##### <span data-ttu-id="385e8-127">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="385e8-127">Figure 5</span></span>  
    > <span data-ttu-id="385e8-128">DevTools Abdocken in einem separaten Fenster</span><span class="sxs-lookup"><span data-stu-id="385e8-128">DevTools undocked in a separate window</span></span>  
    > <span data-ttu-id="385e8-129">! [Devtools in einem separaten Fenster Abdocken] [ImageDevToolsSeparateDevTools]</span><span class="sxs-lookup"><span data-stu-id="385e8-129">![DevTools undocked in a separate window][ImageDevToolsSeparateDevTools]</span></span>  
    
## <span data-ttu-id="385e8-130">Anzeigen von Nachrichten, die von JavaScript protokolliert wurden</span><span class="sxs-lookup"><span data-stu-id="385e8-130">View messages logged from JavaScript</span></span>   

<span data-ttu-id="385e8-131">Die meisten Nachrichten, die Sie in der Konsole sehen, stammen von den Web-Entwicklern, die das JavaScript der Seite verfasst haben.</span><span class="sxs-lookup"><span data-stu-id="385e8-131">Most messages that you see in the Console come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="385e8-132">In diesem Abschnitt möchten wir Ihnen die verschiedenen Nachrichtentypen vorstellen, die Sie wahrscheinlich in der Konsole sehen werden, und erläutern, wie Sie die einzelnen Nachrichtentypen selbst aus Ihrem eigenen JavaScript-Protokoll aufzeichnen können.</span><span class="sxs-lookup"><span data-stu-id="385e8-132">The goal of this section is to introduce you to the different message types that you are likely to see in the Console, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="385e8-133">Klicken Sie in der Demo auf die Schaltfläche **Log-Informationen** .</span><span class="sxs-lookup"><span data-stu-id="385e8-133">Click the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="385e8-134">wird in der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="385e8-134">gets logged to the Console.</span></span>
    
    > ##### <span data-ttu-id="385e8-135">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="385e8-135">Figure 6</span></span>  
    > <span data-ttu-id="385e8-136">Die Konsole nach dem Klicken auf " **Protokollinformationen** "</span><span class="sxs-lookup"><span data-stu-id="385e8-136">The Console after clicking **Log Info**</span></span>  
    > <span data-ttu-id="385e8-137">! [Die Konsole nach dem Klicken auf ' Protokollinformationen '] [ImageLogInfo]</span><span class="sxs-lookup"><span data-stu-id="385e8-137">![The Console after clicking Log Info][ImageLogInfo]</span></span>  
    
1.  <span data-ttu-id="385e8-138">`Hello, Console!`Klicken Sie neben der Nachricht in der Konsole auf **Log. js: 2**.</span><span class="sxs-lookup"><span data-stu-id="385e8-138">Next to the `Hello, Console!` message in the Console click **log.js:2**.</span></span>  <span data-ttu-id="385e8-139">Das Fenster "Quellen" wird geöffnet, und die Codezeile wird hervorgehoben, die dazu geführt hat, dass die Nachricht in der Konsole protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="385e8-139">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="385e8-140">Die Nachricht wurde protokolliert, als das JavaScript der Seite ausgeführt wurde `console.log('Hello, Console!')` .</span><span class="sxs-lookup"><span data-stu-id="385e8-140">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    > ##### <span data-ttu-id="385e8-141">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="385e8-141">Figure 7</span></span>  
    > <span data-ttu-id="385e8-142">DevTools öffnet das Quellen Panel, nachdem Sie auf " **Log. js" klicken: 2**</span><span class="sxs-lookup"><span data-stu-id="385e8-142">DevTools opens the Sources panel after you click **log.js:2**</span></span>  
    > <span data-ttu-id="385e8-143">! [Devtools öffnet das Quellen Panel, nachdem Sie auf "Log. js" klicken: 2] [ImageSourceLog]</span><span class="sxs-lookup"><span data-stu-id="385e8-143">![DevTools opens the Sources panel after you click log.js:2][ImageSourceLog]</span></span>  
    
1.  <span data-ttu-id="385e8-144">Navigieren Sie mit einem der folgenden Workflows zurück zur Konsole:</span><span class="sxs-lookup"><span data-stu-id="385e8-144">Navigate back to the Console using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="385e8-145">Klicken Sie auf die Registerkarte **Konsole** .</span><span class="sxs-lookup"><span data-stu-id="385e8-145">Click the **Console** tab.</span></span>  
    *   <span data-ttu-id="385e8-146">Drücken Sie `Control` + `[` \ (Windows \) oder `Command` + `[` \ (macOS \), bis die Konsole den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="385e8-146">Press `Control`+`[` \(Windows\) or `Command`+`[` \(macOS\) until the Console panel is in focus.</span></span>  
    *   <span data-ttu-id="385e8-147">[Öffnen Sie das Menübefehl][DevToolsCommandMenu], beginnen `Console` Sie mit der Eingabe, wählen Sie den Befehl **Konsolen Panel anzeigen** aus, und drücken Sie dann `Enter` .</span><span class="sxs-lookup"><span data-stu-id="385e8-147">[Open the Command Menu][DevToolsCommandMenu], start typing `Console`, select the **Show Console Panel** command, and then press `Enter`.</span></span>  
    
1.  <span data-ttu-id="385e8-148">Klicken Sie in der Demo auf die Schaltfläche **Warnungsprotokoll** .</span><span class="sxs-lookup"><span data-stu-id="385e8-148">Click the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="385e8-149">wird in der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="385e8-149">gets logged to the Console.</span></span>  <span data-ttu-id="385e8-150">So formatierte Nachrichten sind Warnungen.</span><span class="sxs-lookup"><span data-stu-id="385e8-150">Messages formatted like this are warnings.</span></span>  
    
    > ##### <span data-ttu-id="385e8-151">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="385e8-151">Figure 8</span></span>  
    > <span data-ttu-id="385e8-152">Die Konsole nach dem Klicken auf " **Protokoll Warnung** "</span><span class="sxs-lookup"><span data-stu-id="385e8-152">The Console after clicking **Log Warning**</span></span>  
    > <span data-ttu-id="385e8-153">! [Die Konsole nach dem Klicken auf ' Protokoll Warnung] [ImageConsoleLogWarning]</span><span class="sxs-lookup"><span data-stu-id="385e8-153">![The Console after clicking Log Warning][ImageConsoleLogWarning]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="385e8-154">Wenn Sie den Code anzeigen möchten, der dazu geführt hat, dass eine Nachricht protokolliert wird, klicken Sie auf ein Skript \ (beispielsweise `log.js:12` \), um den Code anzuzeigen, der dazu geführt hat, dass die Nachricht formatiert wurde.</span><span class="sxs-lookup"><span data-stu-id="385e8-154">If you want to see the code that caused a message to get logged a certain way, click on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="385e8-155">Klicken Sie auf das Erweiterungssymbol **erweitern** ![ ][ImageExpandIcon] vor `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="385e8-155">Click the **Expand** ![Expand][ImageExpandIcon] icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="385e8-156">DevTools zeigt die [Stapelüberwachung][WikiStackTrace] an, die zum Aufruf führt.</span><span class="sxs-lookup"><span data-stu-id="385e8-156">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    > ##### <span data-ttu-id="385e8-157">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="385e8-157">Figure 9</span></span>  
    > <span data-ttu-id="385e8-158">Eine Stapelüberwachung</span><span class="sxs-lookup"><span data-stu-id="385e8-158">A stack trace</span></span>  
    > <span data-ttu-id="385e8-159">! [Eine Stapelüberwachung] [Imagestacktrace]</span><span class="sxs-lookup"><span data-stu-id="385e8-159">![A stack trace][ImageStackTrace]</span></span>  
    
    <span data-ttu-id="385e8-160">In der Stapelüberwachung wird Ihnen mitgeteilt, dass eine Funktion namens `logWarning` aufgerufen wurde, die wiederum eine Funktion mit dem Namen genannt wird `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="385e8-160">The stack trace is telling you that a function named `logWarning` was called, which in turn called a function named `quoteDante`.</span></span>  <span data-ttu-id="385e8-161">Anders ausgedrückt: der Aufruf, der sich zuerst ereignet hat, befindet sich am Ende der Stapelüberwachung.</span><span class="sxs-lookup"><span data-stu-id="385e8-161">In other words, the call that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="385e8-162">Sie können Stack-Ablaufverfolgungen jederzeit durch Aufrufen protokollieren `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="385e8-162">You may log stack traces at any time by calling `console.trace()`.</span></span>  

1.  <span data-ttu-id="385e8-163">Klicken Sie auf **Fehler protokollieren**.</span><span class="sxs-lookup"><span data-stu-id="385e8-163">Click **Log Error**.</span></span>  <span data-ttu-id="385e8-164">Die folgende Fehlermeldung wird protokolliert:</span><span class="sxs-lookup"><span data-stu-id="385e8-164">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    > ##### <span data-ttu-id="385e8-165">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="385e8-165">Figure 10</span></span>  
    > <span data-ttu-id="385e8-166">Eine Fehlermeldung</span><span class="sxs-lookup"><span data-stu-id="385e8-166">An error message</span></span>  
    > <span data-ttu-id="385e8-167">! [Eine Fehlermeldung] [ImageLogError]</span><span class="sxs-lookup"><span data-stu-id="385e8-167">![An error message][ImageLogError]</span></span>  
    
1.  <span data-ttu-id="385e8-168">Klicken Sie auf **Protokolltabelle**.</span><span class="sxs-lookup"><span data-stu-id="385e8-168">Click **Log Table**.</span></span>  <span data-ttu-id="385e8-169">Eine Tabelle über berühmte Interpreten wird an der Konsole angemeldet.</span><span class="sxs-lookup"><span data-stu-id="385e8-169">A table about famous artists gets logged to the Console.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="385e8-170">Die `birthday` Spalte wird nur für eine Zeile ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="385e8-170">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="385e8-171">Überprüfen Sie den Code, um herauszufinden, warum das der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="385e8-171">Check the code to figure out why that is.</span></span>
    
    > ##### <span data-ttu-id="385e8-172">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="385e8-172">Figure 11</span></span>  
    > <span data-ttu-id="385e8-173">Eine Tabelle in der Konsole</span><span class="sxs-lookup"><span data-stu-id="385e8-173">A table in the Console</span></span>  
    > <span data-ttu-id="385e8-174">! [Eine Tabelle in der Konsole] [Imageconsoleable]</span><span class="sxs-lookup"><span data-stu-id="385e8-174">![A table in the Console][ImageConsoleTable]</span></span>  
    
1.  <span data-ttu-id="385e8-175">Klicken Sie auf **Protokollgruppe**.</span><span class="sxs-lookup"><span data-stu-id="385e8-175">Click **Log Group**.</span></span>  <span data-ttu-id="385e8-176">Unter dem Label sind die Namen von vier berühmten, kriminalisch bekämpften Schildkröten gruppiert `Adolescent Irradiated Espionage Tortoises` .</span><span class="sxs-lookup"><span data-stu-id="385e8-176">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    > ##### <span data-ttu-id="385e8-177">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="385e8-177">Figure 12</span></span>  
    > <span data-ttu-id="385e8-178">Eine Gruppe von Nachrichten in der Konsole</span><span class="sxs-lookup"><span data-stu-id="385e8-178">A group of messages in the Console</span></span>  
    > <span data-ttu-id="385e8-179">! [Eine Gruppe von Nachrichten in der Konsole] [ImageConsoleLogGroup]</span><span class="sxs-lookup"><span data-stu-id="385e8-179">![A group of messages in the Console][ImageConsoleLogGroup]</span></span>  
    
1.  <span data-ttu-id="385e8-180">Klicken Sie auf **Benutzerdefiniert protokollieren**.</span><span class="sxs-lookup"><span data-stu-id="385e8-180">Click **Log Custom**.</span></span>  <span data-ttu-id="385e8-181">Eine Nachricht mit rotem Rahmen und blauem Hintergrund wird in der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="385e8-181">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    > ##### <span data-ttu-id="385e8-182">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="385e8-182">Figure 13</span></span>  
    > <span data-ttu-id="385e8-183">Eine Nachricht mit benutzerdefinierter Formatierung in der Konsole</span><span class="sxs-lookup"><span data-stu-id="385e8-183">A message with custom formatting in the Console</span></span>  
    > <span data-ttu-id="385e8-184">! [Eine Nachricht mit benutzerdefinierter Formatierung in der Konsole] [ImageConsoleLogCustomFormatting]</span><span class="sxs-lookup"><span data-stu-id="385e8-184">![A message with custom formatting in the Console][ImageConsoleLogCustomFormatting]</span></span>  
    
<span data-ttu-id="385e8-185">Der Grundgedanke hierbei ist, dass Sie eine der Methoden verwenden, wenn Sie Nachrichten von Ihrem JavaScript-Konto in der Konsole protokollieren möchten `console` .</span><span class="sxs-lookup"><span data-stu-id="385e8-185">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="385e8-186">Jede Methode formatiert Nachrichten unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="385e8-186">Each method formats messages differently.</span></span>  

<span data-ttu-id="385e8-187">Es gibt noch mehr Methoden als das, was in diesem Abschnitt gezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="385e8-187">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="385e8-188">In diesem Lernprogramm erfahren Sie, wie Sie die restlichen Methoden erkunden.</span><span class="sxs-lookup"><span data-stu-id="385e8-188">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <span data-ttu-id="385e8-189">Anzeigen von vom Browser protokollierten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="385e8-189">View messages logged by the browser</span></span>   

<span data-ttu-id="385e8-190">Der Browser protokolliert auch Nachrichten an der Konsole.</span><span class="sxs-lookup"><span data-stu-id="385e8-190">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="385e8-191">Dies geschieht in der Regel, wenn ein Problem mit der Seite vorliegt.</span><span class="sxs-lookup"><span data-stu-id="385e8-191">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="385e8-192">Klicken Sie auf **Ursache 404**.</span><span class="sxs-lookup"><span data-stu-id="385e8-192">Click **Cause 404**.</span></span>  <span data-ttu-id="385e8-193">Der Browser protokolliert einen `404` Netzwerkfehler, da das JavaScript der Seite versucht hat, eine Datei abzurufen, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="385e8-193">The browser logs a `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    > ##### <span data-ttu-id="385e8-194">Abbildung 14</span><span class="sxs-lookup"><span data-stu-id="385e8-194">Figure 14</span></span>  
    > <span data-ttu-id="385e8-195">Ein 404-Fehler in der Konsole</span><span class="sxs-lookup"><span data-stu-id="385e8-195">A 404 error in the Console</span></span>  
    > <span data-ttu-id="385e8-196">! [Ein 404-Fehler in der Konsole] [ImageConsoleLogError]</span><span class="sxs-lookup"><span data-stu-id="385e8-196">![A 404 error in the Console][ImageConsoleLogError]</span></span>  
    
1.  <span data-ttu-id="385e8-197">Klicken Sie auf **Fehler verursachen**.</span><span class="sxs-lookup"><span data-stu-id="385e8-197">Click **Cause Error**.</span></span>  <span data-ttu-id="385e8-198">Der Browser protokolliert eine nicht abgefangene `TypeError` , da JavaScript versucht, einen nicht vorhandenen DOM-Knoten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="385e8-198">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    > ##### <span data-ttu-id="385e8-199">Abbildung 15</span><span class="sxs-lookup"><span data-stu-id="385e8-199">Figure 15</span></span>  
    > <span data-ttu-id="385e8-200">Ein TypeError in der Konsole</span><span class="sxs-lookup"><span data-stu-id="385e8-200">A TypeError in the Console</span></span>  
    > <span data-ttu-id="385e8-201">! [Ein TypeError in der Konsole] [ImageConsoleLogTypeError]</span><span class="sxs-lookup"><span data-stu-id="385e8-201">![A TypeError in the Console][ImageConsoleLogTypeError]</span></span>  
    
1.  <span data-ttu-id="385e8-202">Klicken Sie auf die Dropdownliste **Protokollebenen** , und aktivieren Sie die Option **verbose** , wenn Sie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="385e8-202">Click the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="385e8-203">Weitere Informationen zum Filtern finden Sie im nächsten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="385e8-203">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="385e8-204">Sie müssen dies tun, um sicherzustellen, dass die nächste Nachricht, die Sie protokollieren, sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="385e8-204">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > ##### <span data-ttu-id="385e8-205">Abbildung 16</span><span class="sxs-lookup"><span data-stu-id="385e8-205">Figure 16</span></span>  
    > <span data-ttu-id="385e8-206">Aktivieren der **ausführlichen** Protokollebene</span><span class="sxs-lookup"><span data-stu-id="385e8-206">Enabling the **Verbose** log level</span></span>  
    > <span data-ttu-id="385e8-207">! [Aktivieren der ausführlichen Protokollebene] [ImageVerboseLogLevel]</span><span class="sxs-lookup"><span data-stu-id="385e8-207">![Enabling the Verbose log level][ImageVerboseLogLevel]</span></span>  
    
1.  <span data-ttu-id="385e8-208">Klicken Sie auf **Verletzung verursachen**.</span><span class="sxs-lookup"><span data-stu-id="385e8-208">Click **Cause Violation**.</span></span>  <span data-ttu-id="385e8-209">Die Seite reagiert für ein paar Sekunden nicht mehr, und dann protokolliert der Browser die Nachricht `[Violation] 'click' handler took 3000ms` auf der Konsole.</span><span class="sxs-lookup"><span data-stu-id="385e8-209">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="385e8-210">Die genaue Dauer kann variieren.</span><span class="sxs-lookup"><span data-stu-id="385e8-210">The exact duration may vary.</span></span>  
    
    > ##### <span data-ttu-id="385e8-211">Abbildung 17</span><span class="sxs-lookup"><span data-stu-id="385e8-211">Figure 17</span></span>  
    > <span data-ttu-id="385e8-212">Eine Verletzung in der Konsole</span><span class="sxs-lookup"><span data-stu-id="385e8-212">A violation in the Console</span></span>  
    > <span data-ttu-id="385e8-213">! [Eine Verletzung in der Konsole] [ImageConsoleLogViolation]</span><span class="sxs-lookup"><span data-stu-id="385e8-213">![A violation in the Console][ImageConsoleLogViolation]</span></span>  
    
## <span data-ttu-id="385e8-214">Filtern von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="385e8-214">Filter messages</span></span>   

<span data-ttu-id="385e8-215">Auf einigen Seiten wird die Konsole mit Nachrichten überschwemmt.</span><span class="sxs-lookup"><span data-stu-id="385e8-215">On some pages you see the Console get flooded with messages.</span></span>  <span data-ttu-id="385e8-216">DevTools bietet viele verschiedene Methoden zum Filtern von Nachrichten, die für die jeweilige Aufgabe nicht relevant sind.</span><span class="sxs-lookup"><span data-stu-id="385e8-216">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <span data-ttu-id="385e8-217">Nach Protokollebene Filtern</span><span class="sxs-lookup"><span data-stu-id="385e8-217">Filter by log level</span></span>   

<span data-ttu-id="385e8-218">Jeder `console` Methode wird ein Schweregrad zugewiesen: `Verbose` , `Info` , `Warning` , oder `Error` .</span><span class="sxs-lookup"><span data-stu-id="385e8-218">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="385e8-219">Beispielsweise `console.log()` ist eine Nachricht auf einer `Info` Ebene, während `console.error()` die Nachricht auf eine `Error` Ebene lautet.</span><span class="sxs-lookup"><span data-stu-id="385e8-219">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="385e8-220">Klicken Sie auf die Dropdownliste **Protokollebenen** , und deaktivieren Sie **Fehler**.</span><span class="sxs-lookup"><span data-stu-id="385e8-220">Click the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="385e8-221">Eine Ebene ist deaktiviert, wenn daneben kein Häkchen mehr vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="385e8-221">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="385e8-222">Die `Error` Nachrichten auf der Ebene verschwinden.</span><span class="sxs-lookup"><span data-stu-id="385e8-222">The `Error`-level messages disappear.</span></span>  
    
    > ##### <span data-ttu-id="385e8-223">Abbildung 18</span><span class="sxs-lookup"><span data-stu-id="385e8-223">Figure 18</span></span>  
    > <span data-ttu-id="385e8-224">Deaktivieren `Error` von Nachrichten auf der Konsole</span><span class="sxs-lookup"><span data-stu-id="385e8-224">Disabling `Error`-level messages in the Console</span></span>  
    > <span data-ttu-id="385e8-225">! [Deaktivieren von Nachrichten auf Fehlerebene in der Konsole] [ImageConsoleDisablingLogError]</span><span class="sxs-lookup"><span data-stu-id="385e8-225">![Disabling Error-level messages in the Console][ImageConsoleDisablingLogError]</span></span>  
    
1.  <span data-ttu-id="385e8-226">Klicken Sie erneut auf die Dropdownliste **Protokollebenen** , und aktivieren Sie dann **Fehler**erneut.</span><span class="sxs-lookup"><span data-stu-id="385e8-226">Click the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="385e8-227">Die `Error` Nachrichten auf der Ebene werden erneut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="385e8-227">The `Error`-level messages reappear.</span></span>  

### <span data-ttu-id="385e8-228">Filtern nach Text</span><span class="sxs-lookup"><span data-stu-id="385e8-228">Filter by text</span></span>   

<span data-ttu-id="385e8-229">Wenn Sie nur Nachrichten anzeigen möchten, die eine exakte Zeichenfolge enthalten, geben Sie diese Zeichenfolge in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="385e8-229">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="385e8-230">Geben Sie `Dave` in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="385e8-230">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="385e8-231">Alle Nachrichten, die die Zeichenfolge nicht enthalten, `Dave` werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="385e8-231">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="385e8-232">Möglicherweise wird auch die `Adolescent Irradiated Espionage Tortoises` Beschriftung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="385e8-232">You might also see the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="385e8-233">Das ist ein Fehler.</span><span class="sxs-lookup"><span data-stu-id="385e8-233">That is a bug.</span></span>  
    
    > ##### <span data-ttu-id="385e8-234">Abbildung 19</span><span class="sxs-lookup"><span data-stu-id="385e8-234">Figure 19</span></span>  
    > <span data-ttu-id="385e8-235">Filtern von Nachrichten, die nicht enthalten sind</span><span class="sxs-lookup"><span data-stu-id="385e8-235">Filtering out any message that does not include</span></span> `Dave`  
    > <span data-ttu-id="385e8-236">! [Filtert alle Nachrichten, die Dave nicht enthalten] [ImageLogTextFiltering]</span><span class="sxs-lookup"><span data-stu-id="385e8-236">![Filtering out any message that does not include Dave][ImageLogTextFiltering]</span></span>  
    
1.  <span data-ttu-id="385e8-237">Löschen `Dave` aus dem Textfeld " **Filter** "</span><span class="sxs-lookup"><span data-stu-id="385e8-237">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="385e8-238">Alle Nachrichten werden wieder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="385e8-238">All the messages reappear.</span></span>  

### <span data-ttu-id="385e8-239">Nach regulärem Ausdruck filtern</span><span class="sxs-lookup"><span data-stu-id="385e8-239">Filter by regular expression</span></span>   

<span data-ttu-id="385e8-240">Wenn Sie alle Nachrichten anzeigen möchten, die anstelle einer bestimmten Zeichenfolge ein Textmuster enthalten, verwenden Sie einen [regulären Ausdruck][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="385e8-240">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="385e8-241">Geben Sie `/^[AH]/` in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="385e8-241">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="385e8-242">Geben Sie dieses Muster in [regexr][|::ref1::|Main] ein, um zu erläutern, was es tut.</span><span class="sxs-lookup"><span data-stu-id="385e8-242">Type this pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    > ##### <span data-ttu-id="385e8-243">Abbildung 20</span><span class="sxs-lookup"><span data-stu-id="385e8-243">Figure 20</span></span>  
    > <span data-ttu-id="385e8-244">Filtern von Nachrichten, die nicht dem Muster entsprechen</span><span class="sxs-lookup"><span data-stu-id="385e8-244">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    > <span data-ttu-id="385e8-245">! [Filtern von Nachrichten, die nicht mit einem Muster übereinstimmen] [ImageLogRegExFiltering]</span><span class="sxs-lookup"><span data-stu-id="385e8-245">![Filtering out any message that does not match a pattern][ImageLogRegExFiltering]</span></span>  
    
1.  <span data-ttu-id="385e8-246">Löschen `/^[AH]/` aus dem Textfeld " **Filter** "</span><span class="sxs-lookup"><span data-stu-id="385e8-246">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="385e8-247">Alle Nachrichten sind wieder sichtbar.</span><span class="sxs-lookup"><span data-stu-id="385e8-247">All messages are visible again.</span></span>  

### <span data-ttu-id="385e8-248">Nach Nachrichtenquelle Filtern</span><span class="sxs-lookup"><span data-stu-id="385e8-248">Filter by message source</span></span>   

<span data-ttu-id="385e8-249">Wenn Sie nur die Nachrichten anzeigen möchten, die von einer bestimmten URL stammen, verwenden Sie die **Seitenleiste**.</span><span class="sxs-lookup"><span data-stu-id="385e8-249">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="385e8-250">Klicken Sie auf **Konsolen** -Seitenleiste anzeigen ![ ][ImageShowConsoleSidebarIcon] .</span><span class="sxs-lookup"><span data-stu-id="385e8-250">Click **Show Console Sidebar** ![Show Console Sidebar][ImageShowConsoleSidebarIcon].</span></span>  
    
    > ##### <span data-ttu-id="385e8-251">Abbildung 21</span><span class="sxs-lookup"><span data-stu-id="385e8-251">Figure 21</span></span>  
    > <span data-ttu-id="385e8-252">Die Seitenleiste</span><span class="sxs-lookup"><span data-stu-id="385e8-252">The Sidebar</span></span>  
    > <span data-ttu-id="385e8-253">! [Die Seitenleiste] [ImageConsoleSidebar]</span><span class="sxs-lookup"><span data-stu-id="385e8-253">![The Sidebar][ImageConsoleSidebar]</span></span>  
    
1.  <span data-ttu-id="385e8-254">Klicken Sie auf das Erweiterungssymbol **erweitern** ![ ][ImageExpandIcon] neben der Anzahl der Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="385e8-254">Click the **Expand** ![Expand][ImageExpandIcon] icon next to the number of messages.</span></span>  <span data-ttu-id="385e8-255">In [Abbildung 21](#figure-21)wird die Anzahl der Nachrichten als **13 Nachrichten**angezeigt.</span><span class="sxs-lookup"><span data-stu-id="385e8-255">In [Figure 21](#figure-21), the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="385e8-256">Die **Seitenleiste** zeigt eine Liste der URLs, die dazu geführt haben, dass Nachrichten protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="385e8-256">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="385e8-257">Beispielsweise `log.js` verursachte 11 Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="385e8-257">For example, `log.js` caused 11 messages.</span></span>  
    
    > ##### <span data-ttu-id="385e8-258">Abbildung 22</span><span class="sxs-lookup"><span data-stu-id="385e8-258">Figure 22</span></span>  
    > <span data-ttu-id="385e8-259">Anzeigen der Quelle von Nachrichten in der Seitenleiste</span><span class="sxs-lookup"><span data-stu-id="385e8-259">Viewing the source of messages in the Sidebar</span></span>  
    > <span data-ttu-id="385e8-260">! [Anzeigen der Quelle von Nachrichten in der Seitenleiste] [ImageConsoleSidebarLogSource]</span><span class="sxs-lookup"><span data-stu-id="385e8-260">![Viewing the source of messages in the Sidebar][ImageConsoleSidebarLogSource]</span></span>  
    
### <span data-ttu-id="385e8-261">Nach Benutzer Nachrichten filtern</span><span class="sxs-lookup"><span data-stu-id="385e8-261">Filter by user messages</span></span>   

<span data-ttu-id="385e8-262">Wenn Sie zuvor auf **Protokollinformationen**geklickt haben, wurde ein Skript aufgerufen, um `console.log('Hello, Console!')` die Nachricht in der Konsole zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="385e8-262">Earlier, when you clicked **Log Info**, a script called `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="385e8-263">Nachrichten, die von JavaScript wie diesem protokolliert werden, werden als **Benutzer Nachrichten**bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="385e8-263">Messages logged from JavaScript like this are called **user messages**.</span></span>  <span data-ttu-id="385e8-264">Wenn Sie hingegen auf **Ursache 404**geklickt haben, hat der Browser die Meldung auf eine Ebene protokolliert, `Error` die besagt, dass die angeforderte Ressource nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="385e8-264">In contrast, when you clicked **Cause 404**, the browser logged an `Error`-level message stating that the requested resource could not be found.</span></span>  <span data-ttu-id="385e8-265">Nachrichten wie diese werden als **Browser Nachrichten**angesehen.</span><span class="sxs-lookup"><span data-stu-id="385e8-265">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="385e8-266">Verwenden Sie die **Seitenleiste** , um Browser Nachrichten zu filtern und nur Benutzer Nachrichten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="385e8-266">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="385e8-267">Klicken Sie auf **9 Benutzer Nachrichten**.</span><span class="sxs-lookup"><span data-stu-id="385e8-267">Click **9 User Messages**.</span></span>  <span data-ttu-id="385e8-268">Die Browser Nachrichten werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="385e8-268">The browser messages are hidden.</span></span>  
    
    > ##### <span data-ttu-id="385e8-269">Abbildung 23</span><span class="sxs-lookup"><span data-stu-id="385e8-269">Figure 23</span></span>  
    > <span data-ttu-id="385e8-270">Filtern von Browser Nachrichten</span><span class="sxs-lookup"><span data-stu-id="385e8-270">Filtering out browser messages</span></span>  
    > <span data-ttu-id="385e8-271">! [Filtern von Browser Nachrichten] [ImageConsoleLogBrowserFiltering]</span><span class="sxs-lookup"><span data-stu-id="385e8-271">![Filtering out browser messages][ImageConsoleLogBrowserFiltering]</span></span>  
    
1.  <span data-ttu-id="385e8-272">Klicken Sie auf **13 Nachrichten** , um alle Nachrichten erneut anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="385e8-272">Click **13 Messages** to show all messages again.</span></span>  

## <span data-ttu-id="385e8-273">Verwenden der Konsole neben einem anderen Panel</span><span class="sxs-lookup"><span data-stu-id="385e8-273">Use the Console alongside any other panel</span></span>   

<span data-ttu-id="385e8-274">Was passiert, wenn Sie Formatvorlagen bearbeiten, aber Sie müssen das Konsolenprotokoll schnell auf etwas überprüfen?</span><span class="sxs-lookup"><span data-stu-id="385e8-274">What if you are editing styles, but you need to quickly check the Console log for something?</span></span> <span data-ttu-id="385e8-275">Verwenden Sie die Schublade.</span><span class="sxs-lookup"><span data-stu-id="385e8-275">Use the Drawer.</span></span>  

1.  <span data-ttu-id="385e8-276">Klicken Sie auf die Registerkarte **Elemente** .</span><span class="sxs-lookup"><span data-stu-id="385e8-276">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="385e8-277">Drücken Sie `Escape` .</span><span class="sxs-lookup"><span data-stu-id="385e8-277">Press `Escape`.</span></span>  <span data-ttu-id="385e8-278">Die Registerkarte "Konsole" des **Fachs** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="385e8-278">The Console tab of the **Drawer** opens.</span></span>  <span data-ttu-id="385e8-279">Es enthält alle Features des Konsolen Panels, die Sie in diesem Lernprogramm verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="385e8-279">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    > ##### <span data-ttu-id="385e8-280">Abbildung 24</span><span class="sxs-lookup"><span data-stu-id="385e8-280">Figure 24</span></span>  
    > <span data-ttu-id="385e8-281">Die Registerkarte ' Konsole ' im Einzug</span><span class="sxs-lookup"><span data-stu-id="385e8-281">The Console tab in the Drawer</span></span>  
    > <span data-ttu-id="385e8-282">! [Registerkarte ' Konsole ' im Einzug] [ImageDrawerConsole]</span><span class="sxs-lookup"><span data-stu-id="385e8-282">![The Console tab in the Drawer][ImageDrawerConsole]</span></span>  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

 



<!-- image links -->  

[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageLogExample]: /microsoft-edge/devtools-guide-chromium/media/console-ars-technica-console-onload.msft.png "Abbildung 1: Nachrichten in der Konsole"  
<!--[ImageLogSetUp1]: /microsoft-edge/devtools-guide-chromium/media/log-set-up-1.msft.png "old Figure 2: The tutorial on the left, and the demo on the right"  -->  
[ImageDevToolsRight]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-example-devtools-right-Console.msft.png "Abbildung 2: devtools wird rechts neben der Demo angezeigt"  
[ImageDevToolsBottom]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-example-devtools-Bottom-Console.msft.png "Abbildung 3: devtools angedockt am Ende der Demo"  
[ImageDevToolsSeparateBrowse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-example-devtools-separate-Console-Browse.msft.png "Abbildung 4: Browser in einem separaten Fenster"  
[ImageDevToolsSeparateDevTools]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-example-devtools-separate-Console-devtools.msft.png "Abbildung 5: devtools in einem separaten Fenster Abdocken"  
[ImageLogInfo]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-log-info.msft.png "Abbildung 6: die Konsole nach dem Klicken auf" Protokollinformationen "  
[ImageSourceLog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-sources-logjs.msft.png "Abbildung 7: devtools öffnet das Quellen Panel, nachdem Sie auf" Log. js "klicken: 2"  
[ImageConsoleLogWarning]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Log-Warning.msft.png "Abbildung 8: die Konsole nach dem Klicken auf Protokoll Warnung"  
[Imagestacktrace]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Log-Warning-Expanded.msft.png "Abbildung 9: eine Stapelüberwachung"
[ImageStackTrace]: /microsoft-edge/devtools-guide-chromium/media/console-log-warning-expanded.msft.png "Figure 9: A stack trace"  
[ImageLogError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Log-Error.msft.png "Abbildung 10: eine Fehlermeldung"  
[Imageconsoleable]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-log-table.msft.png "Abbildung 11: eine Tabelle in der Konsole"
[ImageConsoleTable]: /microsoft-edge/devtools-guide-chromium/media/console-log-table.msft.png "Figure 11: A table in the Console"  
[ImageConsoleLogGroup]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Log-Group.msft.png "Abbildung 12: eine Gruppe von Nachrichten in der Konsole"  
[ImageConsoleLogCustomFormatting]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Log-Custom.msft.png "Abbildung 13: eine Nachricht mit benutzerdefinierter Formatierung in der Konsole"  
[ImageConsoleLogError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-cause-404.msft.png "Abbildung 14: ein 404-Fehler in der Konsole"  
[ImageConsoleLogTypeError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-cause-Error.msft.png "Abbildung 15: ein TypeError in der Konsole"  
[ImageVerboseLogLevel]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-cause-Error-Log-Levels.msft.png "Abbildung 16: Aktivieren der ausführlichen Protokollebene"  
[ImageConsoleLogViolation]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-cause-Violation.msft.png "Abbildung 17: ein Verstoß in der Konsole"  
[ImageConsoleDisablingLogError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-cause-Violation-Log-Levels.msft.png "Abbildung 18: Deaktivieren von Nachrichten auf Fehlerebene in der Konsole"  
[ImageLogTextFiltering]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-all-messages-Text-Filter.msft.png "Abbildung 19: Filtern einer Nachricht, die Dave nicht enthält"  
[ImageLogRegExFiltering]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-all-messages-Regex-Filter.msft.png "Abbildung 20: Filtern von Nachrichten, die nicht mit einem Muster übereinstimmen"  
[ImageConsoleSidebar]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Sidebar-all-messages.msft.png "Abbildung 21: die Seitenleiste"  
[ImageConsoleSidebarLogSource]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Sidebar-Expanded-all-messages.msft.png "Abbildung 22: Anzeigen der Quelle von Nachrichten in der Seitenleiste"  
[ImageConsoleLogBrowserFiltering]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Sidebar-user-messages.msft.png "Abbildung 23: Filtern von Browser Nachrichten"  
[ImageDrawerConsole]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Console-Elements-drawer-Console-Sidebar-all-messages.msft.png "Abbildung 24: die Registerkarte" Konsole "im Einzug"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge \ (Chrom \)-Entwickler Tools"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  
[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Ändern der Platzierung von Microsoft Edge devtools (abdocken, docken an den unteren Rand, docken nach links)"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Konsolen-API-Referenz"  
[DevToolsConsoleReference]: /microsoft-edge/devtools-guide-chromium/console/reference "Konsolen Referenz"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Erste Schritte mit der Protokollierung von Nachrichten | Glitch"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Reguläre Ausdrücke | MDN"  

[RegExrMain]: https://regexr.com "Regexr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Stack-Trace – Wikipedia"  


> [!NOTE]
> <span data-ttu-id="385e8-316">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="385e8-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="385e8-317">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/log) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="385e8-317">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="385e8-319">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="385e8-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
