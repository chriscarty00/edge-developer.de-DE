---
description: Erfahren Sie, wie Sie Nachrichten an der Konsole protokollieren.
title: Erste Schritte mit der Protokollierung von Nachrichten in der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: fb428154b00959db1627096819c565dd5dc11346
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439289"
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

# <a name="get-started-with-logging-messages-in-the-console"></a><span data-ttu-id="1f25c-104">Erste Schritte mit der Protokollierung von Nachrichten in der Konsole</span><span class="sxs-lookup"><span data-stu-id="1f25c-104">Get started with logging messages in the Console</span></span>  

<span data-ttu-id="1f25c-105">In diesem interaktiven Lernprogramm erfahren Sie, wie Sie Nachrichten in der [Microsoft Edge DevTools-Konsole][MicrosoftEdgeDevTools] protokollieren und filtern.</span><span class="sxs-lookup"><span data-stu-id="1f25c-105">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   <span data-ttu-id="1f25c-107">Nachrichten in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="1f25c-107">Messages in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="1f25c-108">Dieses Lernprogramm soll in der Reihenfolge abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="1f25c-108">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="1f25c-109">Es wird davon ausgegangen, dass Sie die Grundlagen der Webentwicklung verstehen, z. B. die Verwendung von JavaScript zum Hinzufügen von Interaktivität zu einer Seite.</span><span class="sxs-lookup"><span data-stu-id="1f25c-109">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <a name="set-up-the-demo-and-devtools"></a><span data-ttu-id="1f25c-110">Einrichten der Demo und DevTools</span><span class="sxs-lookup"><span data-stu-id="1f25c-110">Set up the demo and DevTools</span></span>  

<span data-ttu-id="1f25c-111">Dieses Lernprogramm ist so konzipiert, dass Sie die Demo öffnen und alle Workflows selbst ausprobieren können.</span><span class="sxs-lookup"><span data-stu-id="1f25c-111">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="1f25c-112">Wenn Sie physisch folgen, werden Sie sich die Workflows wahrscheinlich später merken.</span><span class="sxs-lookup"><span data-stu-id="1f25c-112">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="1f25c-113">Halten `Control` Sie \(Windows, Linux\) oder \(macOS\) fest, und wählen Sie `Command` **Konsolenprotokollbeispiele** aus, um auf einer neuen Registerkarte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1f25c-113">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="1f25c-114">Beispiele für Konsolenprotokolle</span><span class="sxs-lookup"><span data-stu-id="1f25c-114">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  <span data-ttu-id="1f25c-115">Fokussieren Sie die Demo, und wählen Sie `Control` + `Shift` + `J` dann \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1f25c-115">Focus the demo and then select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="1f25c-116">Standardmäßig wird DevTools rechts neben der Demo geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1f25c-116">By default DevTools opens to the right of the demo.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools wird rechts neben der Demo geöffnet" lightbox="../media/console-example-devtools-right-console.msft.png":::
             <span data-ttu-id="1f25c-118">DevTools wird rechts neben der Demo geöffnet</span><span class="sxs-lookup"><span data-stu-id="1f25c-118">DevTools opens to the right of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="1f25c-119">[Dock DevTools am unteren Rand des Fensters][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="1f25c-119">[Dock DevTools to the bottom of the window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools am Unteren Rand der Demo angedockt" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             <span data-ttu-id="1f25c-121">DevTools am Unteren Rand der Demo angedockt</span><span class="sxs-lookup"><span data-stu-id="1f25c-121">DevTools docked to the bottom of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="1f25c-122">[Trennen Sie DevTools in ein separates Fenster.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="1f25c-122">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Browser in einem separaten Fenster" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             <span data-ttu-id="1f25c-124">Browser in einem separaten Fenster</span><span class="sxs-lookup"><span data-stu-id="1f25c-124">Browser in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="1f25c-125">[Trennen Sie DevTools in ein separates Fenster.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="1f25c-125">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools in einem separaten Fenster entdockt" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             <span data-ttu-id="1f25c-127">DevTools in einem separaten Fenster entdockt</span><span class="sxs-lookup"><span data-stu-id="1f25c-127">DevTools undocked in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="view-messages-logged-from-javascript"></a><span data-ttu-id="1f25c-128">Anzeigen von Nachrichten, die von JavaScript protokolliert wurden</span><span class="sxs-lookup"><span data-stu-id="1f25c-128">View messages logged from JavaScript</span></span>  

<span data-ttu-id="1f25c-129">Die meisten Nachrichten, die in der Konsole angezeigt **werden,** stammen von den Webentwicklern, die das JavaScript der Seite geschrieben haben.</span><span class="sxs-lookup"><span data-stu-id="1f25c-129">Most messages that are displayed in the **Console** come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="1f25c-130">Das Ziel dieses Abschnitts besteht in der Einführung in die verschiedenen Nachrichtentypen, die Sie wahrscheinlich in der **Konsole**überprüfen werden, und zu erläutern, wie Sie jeden Nachrichtentyp selbst aus Ihrem eigenen JavaScript protokollieren können.</span><span class="sxs-lookup"><span data-stu-id="1f25c-130">The goal of this section is to introduce you to the different message types that you are likely to review in the **Console**, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="1f25c-131">Wählen Sie in der Demo die Schaltfläche **Protokollinformationen** aus.</span><span class="sxs-lookup"><span data-stu-id="1f25c-131">Choose the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="1f25c-132">wird bei der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="1f25c-132">gets logged to the Console.</span></span>
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="Die Konsole nach der Auswahl von Protokollinformationen" lightbox="../media/console-log-info.msft.png":::
       <span data-ttu-id="1f25c-134">Die **Konsole** nach der Auswahl von **Protokollinformationen**</span><span class="sxs-lookup"><span data-stu-id="1f25c-134">The **Console** after you choose **Log Info**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f25c-135">Wählen Sie neben `Hello, Console!` der Nachricht in der Konsole **log.js:2 aus.**</span><span class="sxs-lookup"><span data-stu-id="1f25c-135">Next to the `Hello, Console!` message in the Console choose **log.js:2**.</span></span>  <span data-ttu-id="1f25c-136">Der Bereich Quellen wird geöffnet und die Codezeile hervorgehoben, die dazu führte, dass die Nachricht bei der Konsole protokolliert wurde.</span><span class="sxs-lookup"><span data-stu-id="1f25c-136">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="1f25c-137">Die Nachricht wurde protokolliert, als das JavaScript der Seite angezeigt `console.log('Hello, Console!')` wurde.</span><span class="sxs-lookup"><span data-stu-id="1f25c-137">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="DevTools öffnet das Sources-Tool, nachdem Sie log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       <span data-ttu-id="1f25c-139">DevTools öffnet das **Tool "Quellen",** nachdem Sie die Option</span><span class="sxs-lookup"><span data-stu-id="1f25c-139">DevTools opens the **Sources** tool after you choose</span></span> `log.js:2`  
    :::image-end:::  
    
1.  <span data-ttu-id="1f25c-140">Navigieren Sie mithilfe **eines** der folgenden Workflows zurück zur Konsole:</span><span class="sxs-lookup"><span data-stu-id="1f25c-140">Navigate back to the **Console** using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="1f25c-141">Wählen Sie das **Konsolentool** aus.</span><span class="sxs-lookup"><span data-stu-id="1f25c-141">Choose the **Console** tool.</span></span>  
    *   <span data-ttu-id="1f25c-142">Wählen `Control` + `[` Sie \(Windows, Linux\) oder `Command` + `[` \(macOS\) aus, bis das **Konsolentool** im Fokus steht.</span><span class="sxs-lookup"><span data-stu-id="1f25c-142">Select `Control`+`[` \(Windows, Linux\) or `Command`+`[` \(macOS\) until the **Console** tool is in focus.</span></span>  
    *   <span data-ttu-id="1f25c-143">[Öffnen Sie das Befehlsmenü,][DevToolsCommandMenu] `Console` geben Sie ein, wählen Sie den Befehl **Konsolenbereich** anzeigen aus, und wählen Sie dann `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="1f25c-143">[Open the Command Menu][DevToolsCommandMenu], type `Console`, choose the **Show Console Panel** command, and then select `Enter`.</span></span>  
    
1.  <span data-ttu-id="1f25c-144">Wählen Sie **in der Demo** die Schaltfläche Protokollwarnung aus.</span><span class="sxs-lookup"><span data-stu-id="1f25c-144">Choose the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="1f25c-145">wird bei der Konsole **protokolliert.**</span><span class="sxs-lookup"><span data-stu-id="1f25c-145">gets logged to the **Console**.</span></span>  <span data-ttu-id="1f25c-146">Nachrichten, die so formatiert sind, sind Warnungen.</span><span class="sxs-lookup"><span data-stu-id="1f25c-146">Messages formatted like this are warnings.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="Die Konsole nach der Auswahl der Protokollwarnung" lightbox="../media/console-log-warning.msft.png":::
       <span data-ttu-id="1f25c-148">Die **Konsole** nach der Auswahl der **Protokollwarnung**</span><span class="sxs-lookup"><span data-stu-id="1f25c-148">The **Console** after you choose **Log Warning**</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="1f25c-149">Wenn Sie den Code anzeigen möchten, der dazu führte, dass eine Nachricht auf eine bestimmte Weise protokolliert wurde, wählen Sie ein Skript \(z. B. \) aus, um den Code zu sehen, der dazu führte, dass die Nachricht `log.js:12` formatiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1f25c-149">If you want to display the code that caused a message to get logged a certain way, choose on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="1f25c-150">Wählen Sie **das Symbol Erweitern** \( Erweitern ![ ](../media/expand-icon.msft.png) \) vor `Abandon Hope All Ye Who Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="1f25c-150">Choose the **Expand** \(![Expand](../media/expand-icon.msft.png)\) icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="1f25c-151">DevTools zeigt die [Stapelverfolgung an,][WikiStackTrace] die zum Aufruf führt.</span><span class="sxs-lookup"><span data-stu-id="1f25c-151">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Eine Stapelverfolgung" lightbox="../media/console-log-warning-expanded.msft.png":::
       <span data-ttu-id="1f25c-153">Eine Stapelverfolgung</span><span class="sxs-lookup"><span data-stu-id="1f25c-153">A stack trace</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="1f25c-154">Die Stapelverfolgung gibt an, dass eine Funktion namens ausgeführt wird, die `logWarning` wiederum eine Funktion mit dem Namen ausgeführt `quoteDante` wird.</span><span class="sxs-lookup"><span data-stu-id="1f25c-154">The stack trace is telling you that a function named `logWarning` is run, which in turn runs a function named `quoteDante`.</span></span>  <span data-ttu-id="1f25c-155">Mit anderen Worten, die Anforderung, die zuerst passiert ist, befindet sich am unteren Rand der Stapelverfolgung.</span><span class="sxs-lookup"><span data-stu-id="1f25c-155">In other words, the request that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="1f25c-156">Sie können Stapelverfolgungen jederzeit protokollieren, indem Sie `console.trace()` ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f25c-156">You may log stack traces at any time by running `console.trace()`.</span></span>  

1.  <span data-ttu-id="1f25c-157">Wählen **Sie Protokollfehler aus.**</span><span class="sxs-lookup"><span data-stu-id="1f25c-157">Choose **Log Error**.</span></span>  <span data-ttu-id="1f25c-158">Die folgende Fehlermeldung wird protokolliert:</span><span class="sxs-lookup"><span data-stu-id="1f25c-158">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Eine Fehlermeldung" lightbox="../media/console-log-error.msft.png":::
       <span data-ttu-id="1f25c-160">Eine Fehlermeldung</span><span class="sxs-lookup"><span data-stu-id="1f25c-160">An error message</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f25c-161">Wählen **Sie Protokolltabelle**aus.</span><span class="sxs-lookup"><span data-stu-id="1f25c-161">Choose **Log Table**.</span></span>  <span data-ttu-id="1f25c-162">Eine Tabelle über bekannte Künstler wird bei der Konsole **protokolliert.**</span><span class="sxs-lookup"><span data-stu-id="1f25c-162">A table about famous artists gets logged to the **Console**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="1f25c-163">Die `birthday` Spalte wird nur für eine Zeile aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="1f25c-163">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="1f25c-164">Überprüfen Sie den Code, um zu ermitteln, warum dies der Grund ist.</span><span class="sxs-lookup"><span data-stu-id="1f25c-164">Review the code to determine why that is.</span></span>
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Eine Tabelle in der Konsole" lightbox="../media/console-log-table.msft.png":::
       <span data-ttu-id="1f25c-166">Eine Tabelle in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="1f25c-166">A table in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f25c-167">Wählen **Sie Protokollgruppe aus.**</span><span class="sxs-lookup"><span data-stu-id="1f25c-167">Choose **Log Group**.</span></span>  <span data-ttu-id="1f25c-168">Die Namen von 4 bekannten Schildkröten zur Bekämpfung von Straftaten werden unter der Bezeichnung `Adolescent Irradiated Espionage Tortoises` gruppieren.</span><span class="sxs-lookup"><span data-stu-id="1f25c-168">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Eine Gruppe von Nachrichten in der Konsole" lightbox="../media/console-log-group.msft.png":::
       <span data-ttu-id="1f25c-170">Eine Gruppe von Nachrichten in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="1f25c-170">A group of messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f25c-171">Wählen **Sie Log Custom aus.**</span><span class="sxs-lookup"><span data-stu-id="1f25c-171">Choose **Log Custom**.</span></span>  <span data-ttu-id="1f25c-172">Eine Nachricht mit rotem Rahmen und blauem Hintergrund wird bei der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="1f25c-172">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Eine Nachricht mit benutzerdefinierter Formatierung in der Konsole" lightbox="../media/console-log-custom.msft.png":::
       <span data-ttu-id="1f25c-174">Eine Nachricht mit benutzerdefinierter Formatierung in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="1f25c-174">A message with custom formatting in the **Console**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="1f25c-175">Die Hauptidee hier ist, dass Sie eine der Methoden verwenden, wenn Sie Nachrichten über Ihr JavaScript an der Konsole `console` protokollieren möchten.</span><span class="sxs-lookup"><span data-stu-id="1f25c-175">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="1f25c-176">Jede Methode formatiert Nachrichten unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="1f25c-176">Each method formats messages differently.</span></span>  

<span data-ttu-id="1f25c-177">Es gibt noch mehr Methoden als in diesem Abschnitt gezeigt.</span><span class="sxs-lookup"><span data-stu-id="1f25c-177">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="1f25c-178">In diesem Lernprogramm erfahren Sie, wie Sie die restlichen Methoden erkunden.</span><span class="sxs-lookup"><span data-stu-id="1f25c-178">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <a name="view-messages-logged-by-the-browser"></a><span data-ttu-id="1f25c-179">Vom Browser protokollierte Nachrichten anzeigen</span><span class="sxs-lookup"><span data-stu-id="1f25c-179">View messages logged by the browser</span></span>  

<span data-ttu-id="1f25c-180">Der Browser protokolliert nachrichten auch an der Konsole.</span><span class="sxs-lookup"><span data-stu-id="1f25c-180">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="1f25c-181">Dies geschieht in der Regel, wenn ein Problem mit der Seite vor liegt.</span><span class="sxs-lookup"><span data-stu-id="1f25c-181">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="1f25c-182">Wählen **Sie Ursache 404 aus.**</span><span class="sxs-lookup"><span data-stu-id="1f25c-182">Choose **Cause 404**.</span></span>  <span data-ttu-id="1f25c-183">Der Browser protokolliert einen HTTP-Statuscode des Netzwerkfehlers, da das JavaScript der Seite versucht hat, eine datei zu abrufen, die `404` nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1f25c-183">The browser logs an HTTP status code of `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Ein 404-Fehler in der Konsole" lightbox="../media/console-cause-404.msft.png":::
       <span data-ttu-id="1f25c-185">Ein `404` Fehler in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="1f25c-185">A `404` error in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f25c-186">Wählen **Sie Ursache Fehler aus.**</span><span class="sxs-lookup"><span data-stu-id="1f25c-186">Choose **Cause Error**.</span></span>  <span data-ttu-id="1f25c-187">Der Browser protokolliert einen nicht abgefangenen Knoten, da javaScript versucht, `TypeError` einen nicht vorhandenen DOM-Knoten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1f25c-187">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Ein TypeError in der Konsole" lightbox="../media/console-cause-error.msft.png":::
       <span data-ttu-id="1f25c-189">A `TypeError` in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="1f25c-189">A `TypeError` in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f25c-190">Wählen Sie **das Dropdownmenü Protokollebenen** aus, und aktivieren Sie die **Option Verbose,** wenn sie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1f25c-190">Choose the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="1f25c-191">Weitere Informationen zum Filtern finden Sie im nächsten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="1f25c-191">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="1f25c-192">Sie müssen dies tun, um sicherzustellen, dass die nächste nachricht, die Sie protokollieren, sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="1f25c-192">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="1f25c-193">Wenn das Dropdownmenü Standardebenen deaktiviert ist, müssen Sie möglicherweise die **Konsolenseite** schließen.</span><span class="sxs-lookup"><span data-stu-id="1f25c-193">If the Default Levels dropdown is disabled, you may need to close the **Console** Sidebar.</span></span>  <span data-ttu-id="1f25c-194">Filtern Sie unten nach Nachrichtenquelle, um weitere Informationen zur **Konsolen-Sidebar** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1f25c-194">Filter by Message Source below for more information about the **Console** Sidebar.</span></span>
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Aktivieren der ausführlichen Protokollebene" lightbox="../media/console-cause-error-log-levels.msft.png":::
       <span data-ttu-id="1f25c-196">Aktivieren der ausführlichen Protokollebene</span><span class="sxs-lookup"><span data-stu-id="1f25c-196">Enabling the Verbose log level</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f25c-197">Wählen Sie **Ursache Verletzung aus.**</span><span class="sxs-lookup"><span data-stu-id="1f25c-197">Choose **Cause Violation**.</span></span>  <span data-ttu-id="1f25c-198">Die Seite reagiert für einige Sekunden nicht mehr, und dann protokolliert der Browser die Nachricht `[Violation] 'click' handler took 3000ms` an der Konsole.</span><span class="sxs-lookup"><span data-stu-id="1f25c-198">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="1f25c-199">Die genaue Dauer kann variieren.</span><span class="sxs-lookup"><span data-stu-id="1f25c-199">The exact duration may vary.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Ein Verstoß in der Konsole" lightbox="../media/console-cause-violation.msft.png":::
       <span data-ttu-id="1f25c-201">Ein Verstoß in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="1f25c-201">A violation in the **Console**</span></span>  
    :::image-end:::  
    
## <a name="filter-messages"></a><span data-ttu-id="1f25c-202">Filtern von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="1f25c-202">Filter messages</span></span>  

<span data-ttu-id="1f25c-203">Auf einigen Webseiten wird \*\*\*\* die Konsole mit Nachrichten überflutet.</span><span class="sxs-lookup"><span data-stu-id="1f25c-203">On some webpages you review the **Console** get flooded with messages.</span></span>  <span data-ttu-id="1f25c-204">DevTools bietet viele verschiedene Möglichkeiten zum Herausfiltern von Nachrichten, die für die jeweilige Aufgabe nicht relevant sind.</span><span class="sxs-lookup"><span data-stu-id="1f25c-204">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <a name="filter-by-log-level"></a><span data-ttu-id="1f25c-205">Filtern nach Protokollebene</span><span class="sxs-lookup"><span data-stu-id="1f25c-205">Filter by log level</span></span>  

<span data-ttu-id="1f25c-206">Jeder `console` Methode wird ein Schweregrad zugewiesen: , , oder `Verbose` `Info` `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="1f25c-206">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="1f25c-207">Beispielsweise handelt es `console.log()` sich um eine Nachricht auf `Info` Ebene, während es sich um eine `console.error()` Nachricht auf `Error` -Ebene handelt.</span><span class="sxs-lookup"><span data-stu-id="1f25c-207">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="1f25c-208">Wählen Sie **das Dropdownmenü Protokollebenen** aus, und deaktivieren Sie **Fehler.**</span><span class="sxs-lookup"><span data-stu-id="1f25c-208">Choose the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="1f25c-209">Eine Ebene ist deaktiviert, wenn kein Häkchen mehr daneben ist.</span><span class="sxs-lookup"><span data-stu-id="1f25c-209">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="1f25c-210">Die `Error` Nachrichten auf -Ebene werden nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1f25c-210">The `Error`-level messages disappear.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Deaktivieren von Nachrichten auf Fehlerebene in der Konsole" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       <span data-ttu-id="1f25c-212">Deaktivieren von Nachrichten auf Fehlerebene in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="1f25c-212">Disable Error-level messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f25c-213">Wählen Sie **erneut das Dropdownmenü** Protokollebenen aus, und aktivieren Sie **Fehler erneut.**</span><span class="sxs-lookup"><span data-stu-id="1f25c-213">Choose the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="1f25c-214">Die `Error` Nachrichten auf -Ebene werden erneut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1f25c-214">The `Error`-level messages reappear.</span></span>  

### <a name="filter-by-text"></a><span data-ttu-id="1f25c-215">Filtern nach Text</span><span class="sxs-lookup"><span data-stu-id="1f25c-215">Filter by text</span></span>  

<span data-ttu-id="1f25c-216">Wenn Sie nur Nachrichten anzeigen möchten, die eine genaue Zeichenfolge enthalten, geben Sie diese Zeichenfolge in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="1f25c-216">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="1f25c-217">Geben `Dave` Sie in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="1f25c-217">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="1f25c-218">Alle Nachrichten, die die Zeichenfolge nicht `Dave` enthalten, werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="1f25c-218">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="1f25c-219">Sie können auch die Bezeichnung `Adolescent Irradiated Espionage Tortoises` überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1f25c-219">You may also review the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="1f25c-220">Dies ist ein Fehler.</span><span class="sxs-lookup"><span data-stu-id="1f25c-220">That is a bug.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Filtern sie alle Nachrichten heraus, die Dave nicht enthalten" lightbox="../media/console-all-messages-text-filter.msft.png":::
       <span data-ttu-id="1f25c-222">Filtern von Nachrichten, die nicht enthalten sind</span><span class="sxs-lookup"><span data-stu-id="1f25c-222">Filter out any message that does not include</span></span> `Dave`  
    :::image-end:::  
    
1.  <span data-ttu-id="1f25c-223">Löschen `Dave` sie \*\*\*\* aus dem Textfeld Filter.</span><span class="sxs-lookup"><span data-stu-id="1f25c-223">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="1f25c-224">Alle Nachrichten werden erneut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1f25c-224">All the messages reappear.</span></span>  

### <a name="filter-by-regular-expression"></a><span data-ttu-id="1f25c-225">Filtern nach regulärem Ausdruck</span><span class="sxs-lookup"><span data-stu-id="1f25c-225">Filter by regular expression</span></span>  

<span data-ttu-id="1f25c-226">Wenn Sie alle Nachrichten anzeigen möchten, die ein Textmuster anstelle einer bestimmten Zeichenfolge enthalten, verwenden Sie einen [regulären Ausdruck][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="1f25c-226">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="1f25c-227">Geben `/^[AH]/` Sie in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="1f25c-227">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="1f25c-228">Geben Sie das Muster in [RegExr ein,][|::ref1::|Main] um eine Erläuterung ihrer Aktivitäten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1f25c-228">Type the pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Filtern von Nachrichten, die nicht mit einem Muster übereinstimmen" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       <span data-ttu-id="1f25c-230">Filtern von Nachrichten, die nicht mit dem Muster übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="1f25c-230">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    :::image-end:::  
    
1.  <span data-ttu-id="1f25c-231">Löschen `/^[AH]/` sie \*\*\*\* aus dem Textfeld Filter.</span><span class="sxs-lookup"><span data-stu-id="1f25c-231">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="1f25c-232">Alle Nachrichten sind wieder sichtbar.</span><span class="sxs-lookup"><span data-stu-id="1f25c-232">All messages are visible again.</span></span>  

### <a name="filter-by-message-source"></a><span data-ttu-id="1f25c-233">Filtern nach Nachrichtenquelle</span><span class="sxs-lookup"><span data-stu-id="1f25c-233">Filter by message source</span></span>  

<span data-ttu-id="1f25c-234">Wenn Sie nur die Nachrichten anzeigen möchten, die von einer bestimmten URL stammten, verwenden Sie die **Sidebar**.</span><span class="sxs-lookup"><span data-stu-id="1f25c-234">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="1f25c-235">Wählen **Sie Konsolenseite anzeigen** \( ![ Konsolenseite anzeigen ](../media/show-console-sidebar-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="1f25c-235">Choose **Show Console Sidebar** \(![Show Console Sidebar](../media/show-console-sidebar-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="Die Seitenleiste" lightbox="../media/console-sidebar-all-messages.msft.png":::
       <span data-ttu-id="1f25c-237">Die Seitenleiste</span><span class="sxs-lookup"><span data-stu-id="1f25c-237">The Sidebar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f25c-238">Wählen Sie **das Symbol Erweitern** \( Erweitern ![ ](../media/expand-icon.msft.png) \) neben der Anzahl der Nachrichten aus.</span><span class="sxs-lookup"><span data-stu-id="1f25c-238">Choose the **Expand** \(![Expand](../media/expand-icon.msft.png)\) icon next to the number of messages.</span></span>  <span data-ttu-id="1f25c-239">In der folgenden Abbildung wird die Anzahl der Nachrichten als **13 Nachrichten angegeben.**</span><span class="sxs-lookup"><span data-stu-id="1f25c-239">In the following figure, the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="1f25c-240">Die **Seitenleiste** zeigt eine Liste der URLs an, die dazu führte, dass Nachrichten protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="1f25c-240">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="1f25c-241">Beispielsweise wurden `log.js` 11 Nachrichten verursacht.</span><span class="sxs-lookup"><span data-stu-id="1f25c-241">For example, `log.js` caused 11 messages.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Anzeigen der Nachrichtenquelle in der Seitenleiste" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       <span data-ttu-id="1f25c-243">Anzeigen der Nachrichtenquelle in der Seitenleiste</span><span class="sxs-lookup"><span data-stu-id="1f25c-243">Viewing the source of messages in the Sidebar</span></span>  
    :::image-end:::  
    
### <a name="filter-by-user-messages"></a><span data-ttu-id="1f25c-244">Filtern nach Benutzernachrichten</span><span class="sxs-lookup"><span data-stu-id="1f25c-244">Filter by user messages</span></span>  

<span data-ttu-id="1f25c-245">Wenn Sie zuvor Log **Info**auswählen, ein Skript mit dem Namen, um die Nachricht bei `console.log('Hello, Console!')` der Konsole zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="1f25c-245">Earlier, when you choose **Log Info**, a script named `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="1f25c-246">Nachrichten, die von JavaScript wie diesem protokolliert werden, sind **benannte Benutzernachrichten.**</span><span class="sxs-lookup"><span data-stu-id="1f25c-246">Messages logged from JavaScript like this are named **user messages**.</span></span>  <span data-ttu-id="1f25c-247">Wenn Sie dagegen Ursache **404**auswählen, protokolliert der Browser eine Meldung auf -Ebene, die besagt, dass die `Error` angeforderte Ressource nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="1f25c-247">In contrast, when you choose **Cause 404**, the browser logs an `Error`-level message stating that the requested resource is not found.</span></span>  <span data-ttu-id="1f25c-248">Nachrichten wie diese werden als **Browsernachrichten betrachtet.**</span><span class="sxs-lookup"><span data-stu-id="1f25c-248">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="1f25c-249">Verwenden Sie **die Seitenleiste,** um Browsernachrichten herausfiltern und nur Benutzernachrichten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1f25c-249">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="1f25c-250">Wählen **Sie 9 Benutzernachrichten aus.**</span><span class="sxs-lookup"><span data-stu-id="1f25c-250">Choose **9 User Messages**.</span></span>  <span data-ttu-id="1f25c-251">Die Browsernachrichten werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="1f25c-251">The browser messages are hidden.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Filtern von Browsernachrichten" lightbox="../media/console-sidebar-user-messages.msft.png":::
       <span data-ttu-id="1f25c-253">Filtern von Browsernachrichten</span><span class="sxs-lookup"><span data-stu-id="1f25c-253">Filtering out browser messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f25c-254">Wählen **Sie 13 Nachrichten aus,** um alle Nachrichten erneut zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="1f25c-254">Choose **13 Messages** to show all messages again.</span></span>  

## <a name="use-the-console-alongside-any-other-tools"></a><span data-ttu-id="1f25c-255">Verwenden der Konsole zusammen mit anderen Tools</span><span class="sxs-lookup"><span data-stu-id="1f25c-255">Use the Console alongside any other tools</span></span>  

<span data-ttu-id="1f25c-256">Wenn Sie Formatvorlagen bearbeiten, aber schnell im Konsolenprotokoll nach etwas suchen müssen, verwenden Sie die Drawer.</span><span class="sxs-lookup"><span data-stu-id="1f25c-256">If you are editing styles, but you need to quickly check the Console log for something, Use the Drawer.</span></span>  

1.  <span data-ttu-id="1f25c-257">Wählen Sie das **Elementtool** aus.</span><span class="sxs-lookup"><span data-stu-id="1f25c-257">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="1f25c-258">Wählen Sie `Escape` aus.</span><span class="sxs-lookup"><span data-stu-id="1f25c-258">Select `Escape`.</span></span>  <span data-ttu-id="1f25c-259">Das **Konsolentool** in **der Schublade** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1f25c-259">The **Console** tool in the **Drawer** opens.</span></span>  <span data-ttu-id="1f25c-260">Es verfügt über alle Features des Konsolenbereichs, die Sie in diesem Lernprogramm verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="1f25c-260">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Das Konsolentool in der Schublade" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         <span data-ttu-id="1f25c-262">Das **Konsolentool** in **der Schublade**</span><span class="sxs-lookup"><span data-stu-id="1f25c-262">The **Console** tool in the **Drawer**</span></span>  
    :::image-end:::  
    
## <a name="see-also"></a><span data-ttu-id="1f25c-263">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1f25c-263">See also</span></span>  

*   <span data-ttu-id="1f25c-264">Weitere Features und Workflows im \*\*\*\* Zusammenhang mit der Konsolenbenutzeroberfläche finden Sie unter [Konsolenreferenz][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="1f25c-264">To explore more features and workflows related to the **Console** UI,navigate to [Console Reference][DevToolsConsoleApi].</span></span>  
*   <span data-ttu-id="1f25c-265">Weitere Informationen zu allen methoden, die in View `console` messages logged from [JavaScript](#view-messages-logged-from-javascript) gezeigt werden, und die anderen Methoden, die in diesem Artikel nicht behandelt werden, finden Sie unter `console` Console API [Reference][DevToolsConsoleReference].</span><span class="sxs-lookup"><span data-stu-id="1f25c-265">To learn more about all of the `console` methods demonstrated in [View messages logged from JavaScript](#view-messages-logged-from-javascript) and explore the other `console` methods not covered in this article, navigate to [Console API Reference][DevToolsConsoleReference].</span></span>  
<!--*   Navigate to [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  
     
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="1f25c-266">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="1f25c-266">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge \(Chromium\) developer tools | Microsoft Docs"  
[DevToolsCommandMenu]: ../command-menu/index.md "Ausführen von Befehlen mit dem Microsoft Edge DevTools Command-Menü | Microsoft Docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Ändern der Platzierung von Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsConsoleApi]: ./api.md "Konsolen-API-| Microsoft Docs"  
[DevToolsConsoleReference]: ./reference.md "Konsolenreferenz | Microsoft Docs"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Erste Schritte mit der Protokollierung | Glitch"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Reguläre Ausdrücke | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Stapelverfolgung – Wikipedia"  
> [!NOTE]
> <span data-ttu-id="1f25c-276">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f25c-276">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1f25c-277">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/log) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="1f25c-277">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="1f25c-279">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1f25c-279">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
