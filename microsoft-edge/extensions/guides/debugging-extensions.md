---
description: In den F12-Entwickler Tools erfahren Sie, wie Sie das Hintergrundskript einer Erweiterung, Inhalts Skripts und Erweiterungsseiten Debuggen.
title: Erweiterungen – Debuggen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, JavaScript, Entwickler, Debuggen, Debuggen
ms.custom: seodec18
ms.openlocfilehash: 34488870cb4e4a92a9d57859509ce7d1176cf284
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567435"
---
# <span data-ttu-id="58a66-104">Debuggen von Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="58a66-104">Debugging extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="58a66-105">Sie können Ihre Erweiterungen in Microsoft Edge mithilfe der F12-Entwickler Tools debuggen.</span><span class="sxs-lookup"><span data-stu-id="58a66-105">You can debug your extensions in Microsoft Edge by using F12 Developer Tools.</span></span>

<span data-ttu-id="58a66-106">Das folgende Video durchläuft eine fehlerhafte Microsoft-Edge-Erweiterung, wobei jedes Debugging-Szenario durchlaufen und auf dem Weg repariert werden kann.</span><span class="sxs-lookup"><span data-stu-id="58a66-106">The following video goes through a buggy Microsoft Edge extension, walking though each debugging scenario and fixing it up along the way.</span></span> <span data-ttu-id="58a66-107">Weitere Informationen finden Sie in den folgenden schrittweisen Anleitungen.</span><span class="sxs-lookup"><span data-stu-id="58a66-107">See the step-by-step instructions below for more info.</span></span>

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]


> [!NOTE]
> <span data-ttu-id="58a66-108">Um das Erweiterungs Debuggen mit F12 zu nutzen, müssen Sie zuerst die Entwicklerfeatures in about: Flags aktivieren.</span><span class="sxs-lookup"><span data-stu-id="58a66-108">In order to take advantage of extension debugging with F12, you must first turn on developer features in about:flags.</span></span> <span data-ttu-id="58a66-109">Weitere Informationen hierzu finden Sie unter [Hinzufügen und Entfernen von Erweiterungen](./adding-and-removing-extensions.md) .</span><span class="sxs-lookup"><span data-stu-id="58a66-109">See [Adding and removing extensions](./adding-and-removing-extensions.md) for details on how to do this.</span></span>


## <span data-ttu-id="58a66-110">Debuggen von Hintergrund Skripten</span><span class="sxs-lookup"><span data-stu-id="58a66-110">Background script debugging</span></span>
<span data-ttu-id="58a66-111">So beginnen Sie mit dem Debuggen des hintergrundskripts ihrer Erweiterung:</span><span class="sxs-lookup"><span data-stu-id="58a66-111">To start debugging the background script of your extension:</span></span>

1. <span data-ttu-id="58a66-112">Klicken Sie auf **mehr (...)** gefolgt von **Erweiterungen** , um in den Erweiterungsbereich zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="58a66-112">Click on **More (...)** followed by **Extensions** to go into the extension pane.</span></span>  
 ![Schaltfläche "Weitere"](./../media/morebutton.png)
2. <span data-ttu-id="58a66-114">Klicken Sie auf die Erweiterung, die Sie debuggen möchten.</span><span class="sxs-lookup"><span data-stu-id="58a66-114">Click on the extension that you want to debug.</span></span>
3. <span data-ttu-id="58a66-115">Klicken Sie auf den Link " **Hintergrundseite** ", um F12 für den Hintergrundprozess aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="58a66-115">Click on the **Background page** link to bring up F12 for the background process.</span></span>  
 ![ausgewählte Erweiterungs Ansicht der Optionen mit dem Link "überprüfen"](./../media/debug-inspect.png)
4. <span data-ttu-id="58a66-117">Wählen Sie die Registerkarte **Debugger** in F12 aus.</span><span class="sxs-lookup"><span data-stu-id="58a66-117">Select the **Debugger** tab in F12.</span></span>
5. <span data-ttu-id="58a66-118">Navigieren Sie zu dem Hintergrundskript ihrer Erweiterung, und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="58a66-118">Navigate to and select your extension's background script.</span></span>
6. <span data-ttu-id="58a66-119">Platzieren Sie Haltepunkte für das Debuggen, indem Sie links neben der Quellcodezeile klicken.</span><span class="sxs-lookup"><span data-stu-id="58a66-119">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
 ![F12-Konsole mit Hintergrundskript mit Unterbrechungspunkten](./../media/debug-f12-background.png)
7. <span data-ttu-id="58a66-121">Wählen Sie die Registerkarte **Konsole** aus, und führen Sie den Befehl " `location.reload()` " aus.</span><span class="sxs-lookup"><span data-stu-id="58a66-121">Select the **Console** tab and execute the command "`location.reload()`".</span></span> <span data-ttu-id="58a66-122">Dadurch wird das Hintergrundskript erneut ausgeführt, sodass Sie den Code schrittweise durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="58a66-122">This will re-execute the background script, allowing you to step through your code.</span></span>  
 ![Konsole mit dem Eintrag "Location. Reload"](./../media/debug-f12-background-console.png)


## <span data-ttu-id="58a66-124">Debuggen von Inhalts Skripts</span><span class="sxs-lookup"><span data-stu-id="58a66-124">Content script debugging</span></span>
<span data-ttu-id="58a66-125">So beginnen Sie mit dem Debuggen des Inhalts Skripts ihrer Erweiterung:</span><span class="sxs-lookup"><span data-stu-id="58a66-125">To start debugging the content script of your extension:</span></span>

1. <span data-ttu-id="58a66-126">Starten Sie F12, indem Sie entweder zur Schaltfläche **mehr (.** ..) navigieren und **"F12-Entwickler Tools"** auswählen oder auf der Tastatur F12 drücken.</span><span class="sxs-lookup"><span data-stu-id="58a66-126">Launch F12 by either navigating to the **More (...)** button and selecting **"F12 Developer Tools"** or by pressing F12 on your keyboard.</span></span>
2. <span data-ttu-id="58a66-127">Navigieren Sie zu dem Inhalts Skript ihrer Erweiterung, und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="58a66-127">Navigate to and select your extension's content script.</span></span> <span data-ttu-id="58a66-128">Inhalts Skripts für zurzeit ausgeführte Erweiterungen werden für jede Erweiterung in einem anderen Ordner dargestellt.</span><span class="sxs-lookup"><span data-stu-id="58a66-128">Content scripts for extensions currently running will be depicted by a different folder for each extension.</span></span>

    > [!NOTE]
    > <span data-ttu-id="58a66-129">Es werden nur ausgeführte Inhalts Skripts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="58a66-129">Only running content scripts will appear.</span></span>

3. <span data-ttu-id="58a66-130">Platzieren Sie Haltepunkte für das Debuggen, indem Sie links neben der Quellcodezeile klicken.</span><span class="sxs-lookup"><span data-stu-id="58a66-130">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
 ![F12, wenn das Inhalts Skript gedebuggt wird](./../media/debug-content-f12.png)
4. <span data-ttu-id="58a66-132">Aktualisieren Sie die Registerkarte Browser, um mit der schrittweisen Ausführung des Codes zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="58a66-132">Refresh the browser tab to begin stepping though your code.</span></span>




## <span data-ttu-id="58a66-133">Debuggen von Erweiterungsseiten</span><span class="sxs-lookup"><span data-stu-id="58a66-133">Extension page debugging</span></span>

<span data-ttu-id="58a66-134">Es gibt zwei Methoden, die für den Zugriff auf den Quellcode der Erweiterungsseite zum Debuggen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="58a66-134">There are two methods that can be used for accessing the source code of your extension page for debugging.</span></span> <span data-ttu-id="58a66-135">Eine Methode gilt für eine Vielzahl von Seiten, während die andere nur für Popup Seiten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="58a66-135">One method applies to a variety of pages while the other only works for popup pages.</span></span>

### <span data-ttu-id="58a66-136">Debuggen einer beliebigen Erweiterungsseite</span><span class="sxs-lookup"><span data-stu-id="58a66-136">Debugging any extension page</span></span>
<span data-ttu-id="58a66-137">Die folgende Methode funktioniert für alle Erweiterungsseiten wie die Seite "Optionen" und Popups:</span><span class="sxs-lookup"><span data-stu-id="58a66-137">The following method works for all extension pages like the options page and popups:</span></span>


1. <span data-ttu-id="58a66-138">Klicken Sie mit der rechten Maustaste auf den Hintergrund der Seite.</span><span class="sxs-lookup"><span data-stu-id="58a66-138">Right-click on the background of your page.</span></span>
2. <span data-ttu-id="58a66-139">Wählen Sie **"Quelle anzeigen"** aus.</span><span class="sxs-lookup"><span data-stu-id="58a66-139">Select **"View source"**.</span></span>

   ![Popup Debuggen mit F12](./../media/debug-popup-select.png)

3. <span data-ttu-id="58a66-141">Sobald F12 geöffnet wird, platzieren Sie Haltepunkte in der Datei, die Sie debuggen möchten.</span><span class="sxs-lookup"><span data-stu-id="58a66-141">Once F12 opens, place breakpoints within the file you want to debug.</span></span>

   ![Popup Debuggen mit F12](./../media/debug-popup-f12.png)
4. <span data-ttu-id="58a66-143">Wählen Sie die Registerkarte **Konsole** aus, und führen Sie den Befehl aus `location.reload()` .</span><span class="sxs-lookup"><span data-stu-id="58a66-143">Select the **Console** tab and execute the command `location.reload()`.</span></span> <span data-ttu-id="58a66-144">Dadurch wird das Seitenskript erneut ausgeführt, sodass Sie den Code schrittweise durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="58a66-144">This will re-execute the page script, allowing you to step through your code.</span></span>  

   ![Konsole mit dem Eintrag "Location. Reload"](./../media/debug-f12-background-console.png)

### <span data-ttu-id="58a66-146">Debuggen einer Popup Erweiterungsseite</span><span class="sxs-lookup"><span data-stu-id="58a66-146">Debugging a popup extension page</span></span>
<span data-ttu-id="58a66-147">Die Methode zum Debuggen von Erweiterungsseiten gilt zwar auch für Popup Erweiterungsseiten, doch mit den folgenden Schritten wird eine weitere Möglichkeit zum Debuggen des Popups skizziert:</span><span class="sxs-lookup"><span data-stu-id="58a66-147">While the method for debugging extension pages also applies to popup extension pages, the following steps outline another way to debug your popup:</span></span>

1. <span data-ttu-id="58a66-148">Klicken Sie mit der rechten Maustaste auf das Symbol der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="58a66-148">Right-click your extension's icon.</span></span>
2. <span data-ttu-id="58a66-149">Wählen Sie **"Popup inspizieren"** aus.</span><span class="sxs-lookup"><span data-stu-id="58a66-149">Select **"Inspect popup"**.</span></span>

   ![Popup-Debug-Prüfung](./../media/debug-popup-inspect.png)
3. <span data-ttu-id="58a66-151">Führen Sie die Schritte 3 und 4 für die Platzierung von Haltepunkten und das erneute Laden des Popups aus.</span><span class="sxs-lookup"><span data-stu-id="58a66-151">Follow steps 3 and 4 above for placing breakpoints and reloading the popup.</span></span>
