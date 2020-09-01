---
title: Erste Schritte mit der Protokollierung von Nachrichten in der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: c2cf868e6daaf9dd45c7acc90a71c2154261b9c3
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982668"
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





# <span data-ttu-id="3c2c5-103">Erste Schritte mit der Protokollierung von Nachrichten in der Konsole</span><span class="sxs-lookup"><span data-stu-id="3c2c5-103">Get Started With Logging Messages In The Console</span></span>   



<span data-ttu-id="3c2c5-104">In diesem interaktiven Lernprogramm erfahren Sie, wie Sie Nachrichten in der [Microsoft Edge devtools][MicrosoftEdgeDevTools] -Konsole protokollieren und filtern.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-104">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   <span data-ttu-id="3c2c5-106">Nachrichten in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="3c2c5-106">Messages in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="3c2c5-107">Dieses Lernprogramm soll in der entsprechenden Reihenfolge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-107">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="3c2c5-108">Es wird davon ausgegangen, dass Sie die Grundlagen der Webentwicklung verstehen, beispielsweise die Verwendung von JavaScript zum Hinzufügen von Interaktivität zu einer Seite.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-108">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <span data-ttu-id="3c2c5-109">Einrichten der Demo-und DevTools</span><span class="sxs-lookup"><span data-stu-id="3c2c5-109">Set up the demo and DevTools</span></span>   

<span data-ttu-id="3c2c5-110">Dieses Lernprogramm ist so konzipiert, dass Sie die Demo öffnen und alle Workflows selbst ausprobieren können.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-110">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="3c2c5-111">Wenn Sie physisch miteinander in Verbindung bleiben, können Sie die Workflows später wahrscheinlicher merken.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-111">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="3c2c5-112">Halten `Control` Sie \ (Windows \) oder `Command` \ (macOS \) gedrückt, und klicken Sie auf **Konsolenprotokoll Beispiele** , um Sie in einer neuen Registerkarte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-112">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="3c2c5-113">Beispiele für Konsolen Protokolle</span><span class="sxs-lookup"><span data-stu-id="3c2c5-113">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  <span data-ttu-id="3c2c5-114">Konzentrieren Sie die Demo, und drücken Sie dann `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \), um devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-114">Focus the demo and then press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="3c2c5-115">Standardmäßig wird devtools rechts neben der Demo geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-115">By default DevTools opens to the right of the demo.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools wird rechts neben der Demo geöffnet" lightbox="../media/console-example-devtools-right-console.msft.png":::
             <span data-ttu-id="3c2c5-117">DevTools wird rechts neben der Demo geöffnet</span><span class="sxs-lookup"><span data-stu-id="3c2c5-117">DevTools opens to the right of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="3c2c5-118">[Docken Sie devtools an den unteren Rand des Fensters an][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="3c2c5-118">[Dock DevTools to the bottom of the window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools angedockt am Ende der Demo" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             <span data-ttu-id="3c2c5-120">DevTools angedockt am Ende der Demo</span><span class="sxs-lookup"><span data-stu-id="3c2c5-120">DevTools docked to the bottom of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="3c2c5-121">[Docken Sie devtools in einem separaten Fenster][DevToolsCustomizePlacement]ab.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-121">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Browser in einem separaten Fenster" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             <span data-ttu-id="3c2c5-123">Browser in einem separaten Fenster</span><span class="sxs-lookup"><span data-stu-id="3c2c5-123">Browser in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="3c2c5-124">[Docken Sie devtools in einem separaten Fenster][DevToolsCustomizePlacement]ab.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-124">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools Abdocken in einem separaten Fenster" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             <span data-ttu-id="3c2c5-126">DevTools Abdocken in einem separaten Fenster</span><span class="sxs-lookup"><span data-stu-id="3c2c5-126">DevTools undocked in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="3c2c5-127">Anzeigen von Nachrichten, die von JavaScript protokolliert wurden</span><span class="sxs-lookup"><span data-stu-id="3c2c5-127">View messages logged from JavaScript</span></span>   

<span data-ttu-id="3c2c5-128">Die meisten Nachrichten, die Sie in der Konsole sehen, stammen von den Web-Entwicklern, die das JavaScript der Seite verfasst haben.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-128">Most messages that you see in the Console come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="3c2c5-129">In diesem Abschnitt möchten wir Ihnen die verschiedenen Nachrichtentypen vorstellen, die Sie wahrscheinlich in der Konsole sehen werden, und erläutern, wie Sie die einzelnen Nachrichtentypen selbst aus Ihrem eigenen JavaScript-Protokoll aufzeichnen können.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-129">The goal of this section is to introduce you to the different message types that you are likely to see in the Console, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="3c2c5-130">Klicken Sie in der Demo auf die Schaltfläche **Log-Informationen** .</span><span class="sxs-lookup"><span data-stu-id="3c2c5-130">Click the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="3c2c5-131">wird in der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-131">gets logged to the Console.</span></span>
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="Die Konsole nach dem Klicken auf "Protokollinformationen"" lightbox="../media/console-log-info.msft.png":::
       <span data-ttu-id="3c2c5-133">Die **Konsole** nach dem Klicken auf " **Protokollinformationen** "</span><span class="sxs-lookup"><span data-stu-id="3c2c5-133">The **Console** after clicking **Log Info**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3c2c5-134">`Hello, Console!`Klicken Sie neben der Nachricht in der Konsole auf **log.js:2**.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-134">Next to the `Hello, Console!` message in the Console click **log.js:2**.</span></span>  <span data-ttu-id="3c2c5-135">Das Fenster "Quellen" wird geöffnet, und die Codezeile wird hervorgehoben, die dazu geführt hat, dass die Nachricht in der Konsole protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-135">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="3c2c5-136">Die Nachricht wurde protokolliert, als das JavaScript der Seite ausgeführt wurde `console.log('Hello, Console!')` .</span><span class="sxs-lookup"><span data-stu-id="3c2c5-136">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="DevTools öffnet das Quellen Panel, nachdem Sie auf log.js:2 Klicken" lightbox="../media/console-sources-logjs.msft.png":::
       <span data-ttu-id="3c2c5-138">DevTools öffnet das **Quellen** Panel, nachdem Sie auf</span><span class="sxs-lookup"><span data-stu-id="3c2c5-138">DevTools opens the **Sources** panel after you click</span></span> `log.js:2`  
    :::image-end:::  
    
1.  <span data-ttu-id="3c2c5-139">Navigieren Sie mit einem der folgenden Workflows zurück zur **Konsole** :</span><span class="sxs-lookup"><span data-stu-id="3c2c5-139">Navigate back to the **Console** using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="3c2c5-140">Klicken Sie auf die Registerkarte **Konsole** .</span><span class="sxs-lookup"><span data-stu-id="3c2c5-140">Click the **Console** tab.</span></span>  
    *   <span data-ttu-id="3c2c5-141">Drücken Sie `Control` + `[` \ (Windows \) oder `Command` + `[` \ (macOS \), bis die Konsole den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-141">Press `Control`+`[` \(Windows\) or `Command`+`[` \(macOS\) until the Console panel is in focus.</span></span>  
    *   <span data-ttu-id="3c2c5-142">[Öffnen Sie das Menübefehl][DevToolsCommandMenu], beginnen `Console` Sie mit der Eingabe, wählen Sie den Befehl **Konsolen Panel anzeigen** aus, und drücken Sie dann `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3c2c5-142">[Open the Command Menu][DevToolsCommandMenu], start typing `Console`, select the **Show Console Panel** command, and then press `Enter`.</span></span>  
    
1.  <span data-ttu-id="3c2c5-143">Klicken Sie in der Demo auf die Schaltfläche **Warnungsprotokoll** .</span><span class="sxs-lookup"><span data-stu-id="3c2c5-143">Click the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="3c2c5-144">wird in der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-144">gets logged to the Console.</span></span>  <span data-ttu-id="3c2c5-145">So formatierte Nachrichten sind Warnungen.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-145">Messages formatted like this are warnings.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="Die Konsole, nachdem Sie auf "Protokoll Warnung" klicken" lightbox="../media/console-log-warning.msft.png":::
       <span data-ttu-id="3c2c5-147">Die **Konsole** , nachdem Sie auf " **Protokoll Warnung** " klicken</span><span class="sxs-lookup"><span data-stu-id="3c2c5-147">The **Console** after you click **Log Warning**</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="3c2c5-148">Wenn Sie den Code anzeigen möchten, der dazu geführt hat, dass eine Nachricht protokolliert wird, klicken Sie auf ein Skript \ (beispielsweise `log.js:12` \), um den Code anzuzeigen, der dazu geführt hat, dass die Nachricht formatiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-148">If you want to see the code that caused a message to get logged a certain way, click on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="3c2c5-149">Klicken Sie auf das Symbol **erweitern** \ ( ![ Erweitern ][ImageExpandIcon] \) vor `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="3c2c5-149">Click the **Expand** \(![Expand][ImageExpandIcon]\) icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="3c2c5-150">DevTools zeigt die [Stapelüberwachung][WikiStackTrace] an, die zum Aufruf führt.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-150">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Eine Stapelüberwachung" lightbox="../media/console-log-warning-expanded.msft.png":::
       <span data-ttu-id="3c2c5-152">Eine Stapelüberwachung</span><span class="sxs-lookup"><span data-stu-id="3c2c5-152">A stack trace</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="3c2c5-153">In der Stapelüberwachung wird Ihnen mitgeteilt, dass eine Funktion namens `logWarning` aufgerufen wurde, die wiederum eine Funktion mit dem Namen genannt wird `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="3c2c5-153">The stack trace is telling you that a function named `logWarning` was called, which in turn called a function named `quoteDante`.</span></span>  <span data-ttu-id="3c2c5-154">Anders ausgedrückt: der Aufruf, der sich zuerst ereignet hat, befindet sich am Ende der Stapelüberwachung.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-154">In other words, the call that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="3c2c5-155">Sie können Stack-Ablaufverfolgungen jederzeit durch Aufrufen protokollieren `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="3c2c5-155">You may log stack traces at any time by calling `console.trace()`.</span></span>  

1.  <span data-ttu-id="3c2c5-156">Klicken Sie auf **Fehler protokollieren**.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-156">Click **Log Error**.</span></span>  <span data-ttu-id="3c2c5-157">Die folgende Fehlermeldung wird protokolliert:</span><span class="sxs-lookup"><span data-stu-id="3c2c5-157">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Eine Fehlermeldung" lightbox="../media/console-log-error.msft.png":::
       <span data-ttu-id="3c2c5-159">Eine Fehlermeldung</span><span class="sxs-lookup"><span data-stu-id="3c2c5-159">An error message</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3c2c5-160">Klicken Sie auf **Protokolltabelle**.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-160">Click **Log Table**.</span></span>  <span data-ttu-id="3c2c5-161">Eine Tabelle über berühmte Interpreten wird an der Konsole angemeldet.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-161">A table about famous artists gets logged to the Console.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="3c2c5-162">Die `birthday` Spalte wird nur für eine Zeile ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-162">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="3c2c5-163">Überprüfen Sie den Code, um zu ermitteln, warum dies der Grund ist.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-163">Review the code to determine why that is.</span></span>
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Eine Tabelle in der Konsole" lightbox="../media/console-log-table.msft.png":::
       <span data-ttu-id="3c2c5-165">Eine Tabelle in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="3c2c5-165">A table in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3c2c5-166">Klicken Sie auf **Protokollgruppe**.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-166">Click **Log Group**.</span></span>  <span data-ttu-id="3c2c5-167">Unter dem Label sind die Namen von vier berühmten, kriminalisch bekämpften Schildkröten gruppiert `Adolescent Irradiated Espionage Tortoises` .</span><span class="sxs-lookup"><span data-stu-id="3c2c5-167">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Eine Gruppe von Nachrichten in der Konsole" lightbox="../media/console-log-group.msft.png":::
       <span data-ttu-id="3c2c5-169">Eine Gruppe von Nachrichten in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="3c2c5-169">A group of messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3c2c5-170">Klicken Sie auf **Benutzerdefiniert protokollieren**.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-170">Click **Log Custom**.</span></span>  <span data-ttu-id="3c2c5-171">Eine Nachricht mit rotem Rahmen und blauem Hintergrund wird in der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-171">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Eine Nachricht mit benutzerdefinierter Formatierung in der Konsole" lightbox="../media/console-log-custom.msft.png":::
       <span data-ttu-id="3c2c5-173">Eine Nachricht mit benutzerdefinierter Formatierung in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="3c2c5-173">A message with custom formatting in the **Console**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="3c2c5-174">Der Grundgedanke hierbei ist, dass Sie eine der Methoden verwenden, wenn Sie Nachrichten von Ihrem JavaScript-Konto in der Konsole protokollieren möchten `console` .</span><span class="sxs-lookup"><span data-stu-id="3c2c5-174">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="3c2c5-175">Jede Methode formatiert Nachrichten unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-175">Each method formats messages differently.</span></span>  

<span data-ttu-id="3c2c5-176">Es gibt noch mehr Methoden als das, was in diesem Abschnitt gezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-176">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="3c2c5-177">In diesem Lernprogramm erfahren Sie, wie Sie die restlichen Methoden erkunden.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-177">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <span data-ttu-id="3c2c5-178">Anzeigen von vom Browser protokollierten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="3c2c5-178">View messages logged by the browser</span></span>   

<span data-ttu-id="3c2c5-179">Der Browser protokolliert auch Nachrichten an der Konsole.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-179">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="3c2c5-180">Dies geschieht in der Regel, wenn ein Problem mit der Seite vorliegt.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-180">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="3c2c5-181">Klicken Sie auf **Ursache 404**.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-181">Click **Cause 404**.</span></span>  <span data-ttu-id="3c2c5-182">Der Browser protokolliert einen HTTP-Statuscode des `404` Netzwerkfehlers, weil das JavaScript der Seite versucht hat, eine Datei abzurufen, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-182">The browser logs an HTTP status code of `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Ein 404-Fehler in der Konsole" lightbox="../media/console-cause-404.msft.png":::
       <span data-ttu-id="3c2c5-184">`404`Fehler in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="3c2c5-184">A `404` error in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3c2c5-185">Klicken Sie auf **Fehler verursachen**.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-185">Click **Cause Error**.</span></span>  <span data-ttu-id="3c2c5-186">Der Browser protokolliert eine nicht abgefangene `TypeError` , da JavaScript versucht, einen nicht vorhandenen DOM-Knoten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-186">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Ein TypeError in der Konsole" lightbox="../media/console-cause-error.msft.png":::
       <span data-ttu-id="3c2c5-188">A `TypeError` in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="3c2c5-188">A `TypeError` in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3c2c5-189">Klicken Sie auf die Dropdownliste **Protokollebenen** , und aktivieren Sie die Option **verbose** , wenn Sie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-189">Click the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="3c2c5-190">Weitere Informationen zum Filtern finden Sie im nächsten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-190">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="3c2c5-191">Sie müssen dies tun, um sicherzustellen, dass die nächste Nachricht, die Sie protokollieren, sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-191">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="3c2c5-192">Wenn die Dropdownliste Standardebenen deaktiviert ist, müssen Sie möglicherweise die Sidebar der **Konsole** schließen.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-192">If the Default Levels dropdown is disabled, you may need to close the **Console** Sidebar.</span></span>  <span data-ttu-id="3c2c5-193">Filtern nach Nachrichtenquelle unten, um weitere Informationen zur Sidebar der **Konsole** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-193">Filter by Message Source below for more information about the **Console** Sidebar.</span></span>
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Aktivieren der ausführlichen Protokollebene" lightbox="../media/console-cause-error-log-levels.msft.png":::
       <span data-ttu-id="3c2c5-195">Aktivieren der ausführlichen Protokollebene</span><span class="sxs-lookup"><span data-stu-id="3c2c5-195">Enabling the Verbose log level</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3c2c5-196">Klicken Sie auf **Verletzung verursachen**.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-196">Click **Cause Violation**.</span></span>  <span data-ttu-id="3c2c5-197">Die Seite reagiert für ein paar Sekunden nicht mehr, und dann protokolliert der Browser die Nachricht `[Violation] 'click' handler took 3000ms` auf der Konsole.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-197">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="3c2c5-198">Die genaue Dauer kann variieren.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-198">The exact duration may vary.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Eine Verletzung in der Konsole" lightbox="../media/console-cause-violation.msft.png":::
       <span data-ttu-id="3c2c5-200">Eine Verletzung in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="3c2c5-200">A violation in the **Console**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="3c2c5-201">Filtern von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="3c2c5-201">Filter messages</span></span>   

<span data-ttu-id="3c2c5-202">Auf einigen Seiten wird die Konsole mit Nachrichten überschwemmt.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-202">On some pages you see the Console get flooded with messages.</span></span>  <span data-ttu-id="3c2c5-203">DevTools bietet viele verschiedene Methoden zum Filtern von Nachrichten, die für die jeweilige Aufgabe nicht relevant sind.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-203">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <span data-ttu-id="3c2c5-204">Nach Protokollebene Filtern</span><span class="sxs-lookup"><span data-stu-id="3c2c5-204">Filter by log level</span></span>   

<span data-ttu-id="3c2c5-205">Jeder `console` Methode wird ein Schweregrad zugewiesen: `Verbose` , `Info` , `Warning` , oder `Error` .</span><span class="sxs-lookup"><span data-stu-id="3c2c5-205">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="3c2c5-206">Beispielsweise `console.log()` ist eine Nachricht auf einer `Info` Ebene, während `console.error()` die Nachricht auf eine `Error` Ebene lautet.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-206">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="3c2c5-207">Klicken Sie auf die Dropdownliste **Protokollebenen** , und deaktivieren Sie **Fehler**.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-207">Click the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="3c2c5-208">Eine Ebene ist deaktiviert, wenn daneben kein Häkchen mehr vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-208">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="3c2c5-209">Die `Error` Nachrichten auf der Ebene verschwinden.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-209">The `Error`-level messages disappear.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Deaktivieren von Nachrichten auf Fehlerebene in der Konsole" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       <span data-ttu-id="3c2c5-211">Deaktivieren von Nachrichten auf Fehlerebene in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="3c2c5-211">Disabling Error-level messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3c2c5-212">Klicken Sie erneut auf die Dropdownliste **Protokollebenen** , und aktivieren Sie dann **Fehler**erneut.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-212">Click the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="3c2c5-213">Die `Error` Nachrichten auf der Ebene werden erneut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-213">The `Error`-level messages reappear.</span></span>  

### <span data-ttu-id="3c2c5-214">Filtern nach Text</span><span class="sxs-lookup"><span data-stu-id="3c2c5-214">Filter by text</span></span>   

<span data-ttu-id="3c2c5-215">Wenn Sie nur Nachrichten anzeigen möchten, die eine exakte Zeichenfolge enthalten, geben Sie diese Zeichenfolge in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-215">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="3c2c5-216">Geben Sie `Dave` in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-216">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="3c2c5-217">Alle Nachrichten, die die Zeichenfolge nicht enthalten, `Dave` werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-217">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="3c2c5-218">Möglicherweise wird auch die `Adolescent Irradiated Espionage Tortoises` Beschriftung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-218">You might also see the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="3c2c5-219">Das ist ein Fehler.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-219">That is a bug.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Filtern von Nachrichten, die Dave nicht enthalten" lightbox="../media/console-all-messages-text-filter.msft.png":::
       <span data-ttu-id="3c2c5-221">Filtern von Nachrichten, die nicht enthalten sind</span><span class="sxs-lookup"><span data-stu-id="3c2c5-221">Filtering out any message that does not include</span></span> `Dave`  
    :::image-end:::  
    
1.  <span data-ttu-id="3c2c5-222">Löschen `Dave` aus dem Textfeld " **Filter** "</span><span class="sxs-lookup"><span data-stu-id="3c2c5-222">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="3c2c5-223">Alle Nachrichten werden wieder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-223">All the messages reappear.</span></span>  

### <span data-ttu-id="3c2c5-224">Nach regulärem Ausdruck filtern</span><span class="sxs-lookup"><span data-stu-id="3c2c5-224">Filter by regular expression</span></span>   

<span data-ttu-id="3c2c5-225">Wenn Sie alle Nachrichten anzeigen möchten, die anstelle einer bestimmten Zeichenfolge ein Textmuster enthalten, verwenden Sie einen [regulären Ausdruck][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="3c2c5-225">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="3c2c5-226">Geben Sie `/^[AH]/` in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-226">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="3c2c5-227">Geben Sie dieses Muster in [regexr][|::ref1::|Main] ein, um zu erläutern, was es tut.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-227">Type this pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Filtern von Nachrichten, die nicht mit einem Muster übereinstimmen" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       <span data-ttu-id="3c2c5-229">Filtern von Nachrichten, die nicht dem Muster entsprechen</span><span class="sxs-lookup"><span data-stu-id="3c2c5-229">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    :::image-end:::  
    
1.  <span data-ttu-id="3c2c5-230">Löschen `/^[AH]/` aus dem Textfeld " **Filter** "</span><span class="sxs-lookup"><span data-stu-id="3c2c5-230">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="3c2c5-231">Alle Nachrichten sind wieder sichtbar.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-231">All messages are visible again.</span></span>  

### <span data-ttu-id="3c2c5-232">Nach Nachrichtenquelle Filtern</span><span class="sxs-lookup"><span data-stu-id="3c2c5-232">Filter by message source</span></span>   

<span data-ttu-id="3c2c5-233">Wenn Sie nur die Nachrichten anzeigen möchten, die von einer bestimmten URL stammen, verwenden Sie die **Seitenleiste**.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-233">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="3c2c5-234">Klicken Sie auf **Console Sidebar anzeigen** \ ( ![ Konsolen ][ImageShowConsoleSidebarIcon] -Sidebar anzeigen \).</span><span class="sxs-lookup"><span data-stu-id="3c2c5-234">Click **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\).</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="Die Seitenleiste" lightbox="../media/console-sidebar-all-messages.msft.png":::
       <span data-ttu-id="3c2c5-236">Die Seitenleiste</span><span class="sxs-lookup"><span data-stu-id="3c2c5-236">The Sidebar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3c2c5-237">Klicken Sie auf das Symbol **erweitern** \ ( ![ Erweitern ][ImageExpandIcon] \) neben der Anzahl der Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-237">Click the **Expand** \(![Expand][ImageExpandIcon]\) icon next to the number of messages.</span></span>  <span data-ttu-id="3c2c5-238">In der folgenden Abbildung wird die Anzahl der Nachrichten als **13 Nachrichten**angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-238">In the following figure, the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="3c2c5-239">Die **Seitenleiste** zeigt eine Liste der URLs, die dazu geführt haben, dass Nachrichten protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-239">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="3c2c5-240">Beispielsweise `log.js` verursachte 11 Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-240">For example, `log.js` caused 11 messages.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Anzeigen der Quelle von Nachrichten in der Seitenleiste" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       <span data-ttu-id="3c2c5-242">Anzeigen der Quelle von Nachrichten in der Seitenleiste</span><span class="sxs-lookup"><span data-stu-id="3c2c5-242">Viewing the source of messages in the Sidebar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="3c2c5-243">Nach Benutzer Nachrichten filtern</span><span class="sxs-lookup"><span data-stu-id="3c2c5-243">Filter by user messages</span></span>   

<span data-ttu-id="3c2c5-244">Wenn Sie zuvor auf **Protokollinformationen**geklickt haben, wurde ein Skript aufgerufen, um `console.log('Hello, Console!')` die Nachricht in der Konsole zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-244">Earlier, when you clicked **Log Info**, a script called `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="3c2c5-245">Nachrichten, die von JavaScript wie diesem protokolliert werden, werden als **Benutzer Nachrichten**bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-245">Messages logged from JavaScript like this are called **user messages**.</span></span>  <span data-ttu-id="3c2c5-246">Wenn Sie hingegen auf **Ursache 404**geklickt haben, hat der Browser die Meldung auf eine Ebene protokolliert, `Error` die besagt, dass die angeforderte Ressource nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-246">In contrast, when you clicked **Cause 404**, the browser logged an `Error`-level message stating that the requested resource could not be found.</span></span>  <span data-ttu-id="3c2c5-247">Nachrichten wie diese werden als **Browser Nachrichten**angesehen.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-247">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="3c2c5-248">Verwenden Sie die **Seitenleiste** , um Browser Nachrichten zu filtern und nur Benutzer Nachrichten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-248">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="3c2c5-249">Klicken Sie auf **9 Benutzer Nachrichten**.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-249">Click **9 User Messages**.</span></span>  <span data-ttu-id="3c2c5-250">Die Browser Nachrichten werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-250">The browser messages are hidden.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Filtern von Browser Nachrichten" lightbox="../media/console-sidebar-user-messages.msft.png":::
       <span data-ttu-id="3c2c5-252">Filtern von Browser Nachrichten</span><span class="sxs-lookup"><span data-stu-id="3c2c5-252">Filtering out browser messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3c2c5-253">Klicken Sie auf **13 Nachrichten** , um alle Nachrichten erneut anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-253">Click **13 Messages** to show all messages again.</span></span>  

## <span data-ttu-id="3c2c5-254">Verwenden der Konsole neben einem anderen Panel</span><span class="sxs-lookup"><span data-stu-id="3c2c5-254">Use the Console alongside any other panel</span></span>   

<span data-ttu-id="3c2c5-255">Was passiert, wenn Sie Formatvorlagen bearbeiten, aber Sie müssen das Konsolenprotokoll schnell auf etwas überprüfen?</span><span class="sxs-lookup"><span data-stu-id="3c2c5-255">What if you are editing styles, but you need to quickly check the Console log for something?</span></span> <span data-ttu-id="3c2c5-256">Verwenden Sie die Schublade.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-256">Use the Drawer.</span></span>  

1.  <span data-ttu-id="3c2c5-257">Klicken Sie auf die Registerkarte **Elemente** .</span><span class="sxs-lookup"><span data-stu-id="3c2c5-257">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="3c2c5-258">Drücken Sie `Escape` .</span><span class="sxs-lookup"><span data-stu-id="3c2c5-258">Press `Escape`.</span></span>  <span data-ttu-id="3c2c5-259">Die Registerkarte "Konsole" des **Fachs** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-259">The Console tab of the **Drawer** opens.</span></span>  <span data-ttu-id="3c2c5-260">Es enthält alle Features des Konsolen Panels, die Sie in diesem Lernprogramm verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-260">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Die Registerkarte ' Konsole ' im Einzug" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         <span data-ttu-id="3c2c5-262">Die Registerkarte ' **Konsole** ' im **Einzug**</span><span class="sxs-lookup"><span data-stu-id="3c2c5-262">The **Console** tab in the **Drawer**</span></span>  
    :::image-end:::  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

<!--
 


-->  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge \ (Chrom \) Developer Tools | Microsoft docs"  
[DevToolsCommandMenu]: ../command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Ändern der Position von Microsoft Edge devtools | Microsoft docs"  
[DevToolsConsoleApi]: ./api.md "Konsolen-API-Referenz | Microsoft docs"  
[DevToolsConsoleReference]: ./reference.md "Konsolen Referenz | Microsoft docs"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Erste Schritte mit der Protokollierung von Nachrichten | Glitch"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Reguläre Ausdrücke | MDN"  

[RegExrMain]: https://regexr.com "Regexr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Stack-Trace – Wikipedia"  


> [!NOTE]
> <span data-ttu-id="3c2c5-272">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-272">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3c2c5-273">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/log) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="3c2c5-273">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="3c2c5-275">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3c2c5-275">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
