---
description: Erfahren Sie mit den F12 Developer Tools, wie Sie das Hintergrundskript, Inhaltsskripts und Erweiterungsseiten einer Erweiterung debuggen.
title: Debuggen | Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, javascript, developer, debug, debugging
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a23c7558080cca7671cdfc9790705a8d8c9ed705
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399365"
---
# <a name="debugging-extensions"></a><span data-ttu-id="ada97-104">Debugging von Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="ada97-104">Debugging extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="ada97-105">Sie können Ihre Erweiterungen in Microsoft Edge mithilfe von F12 Developer Tools debuggen.</span><span class="sxs-lookup"><span data-stu-id="ada97-105">You can debug your extensions in Microsoft Edge by using F12 Developer Tools.</span></span>  

<span data-ttu-id="ada97-106">Im folgenden Video wird eine fehlerhafte Microsoft Edge-Erweiterung durch die einzelnen Debuggingszenarien gestreamt und auf dem Weg nach oben gefixt.</span><span class="sxs-lookup"><span data-stu-id="ada97-106">The following video goes through a buggy Microsoft Edge extension, walking though each debugging scenario and fixing it up along the way.</span></span>  <span data-ttu-id="ada97-107">Weitere Informationen finden Sie in den schrittweisen Anweisungen unten.</span><span class="sxs-lookup"><span data-stu-id="ada97-107">See the step-by-step instructions below for more info.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]  

> [!NOTE]
> <span data-ttu-id="ada97-108">Um das Erweiterungsdebuggen mit F12 nutzen zu können, müssen Sie zuerst Entwicklerfeatures in "about:flags" aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ada97-108">In order to take advantage of extension debugging with F12, you must first turn on developer features in about:flags.</span></span>  <span data-ttu-id="ada97-109">Weitere [Informationen dazu finden Sie unter](./adding-and-removing-extensions.md) Hinzufügen und Entfernen von Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="ada97-109">See [Adding and removing extensions](./adding-and-removing-extensions.md) for details on how to do this.</span></span>  

## <a name="background-script-debugging"></a><span data-ttu-id="ada97-110">Debuggen von Hintergrundskripts</span><span class="sxs-lookup"><span data-stu-id="ada97-110">Background script debugging</span></span>  

<span data-ttu-id="ada97-111">So starten Sie das Debuggen des Hintergrundskripts Ihrer Erweiterung:</span><span class="sxs-lookup"><span data-stu-id="ada97-111">To start debugging the background script of your extension:</span></span>  

1.  <span data-ttu-id="ada97-112">Klicken Sie auf **Weitere (...)** gefolgt von **Erweiterungen,** um in den Erweiterungsbereich zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="ada97-112">Click on **More (...)** followed by **Extensions** to go into the extension pane.</span></span>  
    
    ![Schaltfläche "Mehr"](../media/morebutton.png)  
    
1.  <span data-ttu-id="ada97-114">Klicken Sie auf die Erweiterung, die Sie debuggen möchten.</span><span class="sxs-lookup"><span data-stu-id="ada97-114">Click on the extension that you want to debug.</span></span>  
1.  <span data-ttu-id="ada97-115">Klicken Sie auf den **Link Hintergrundseite,** um F12 für den Hintergrundprozess zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ada97-115">Click on the **Background page** link to bring up F12 for the background process.</span></span>  
    
    ![Ausgewählte Erweiterungsansicht von Optionen mit Link "Überprüfen"](../media/debug-inspect.png)  
    
1.  <span data-ttu-id="ada97-117">Wählen Sie **die Registerkarte Debugger** in F12 aus.</span><span class="sxs-lookup"><span data-stu-id="ada97-117">Select the **Debugger** tab in F12.</span></span>  
1.  <span data-ttu-id="ada97-118">Navigieren Sie zum Hintergrundskript Ihrer Erweiterung, und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="ada97-118">Navigate to and select your extension's background script.</span></span>  
1.  <span data-ttu-id="ada97-119">Platzieren Sie Haltepunkte für das Debuggen, indem Sie links von der Quellcodezeile klicken.</span><span class="sxs-lookup"><span data-stu-id="ada97-119">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
    
    ![f12-Konsole mit Hintergrundskript mit Unterbrechungspunkten](../media/debug-f12-background.png)  
    
1.  <span data-ttu-id="ada97-121">Wählen Sie die **Registerkarte Konsole** aus, und führen Sie den Befehl `location.reload()` aus.</span><span class="sxs-lookup"><span data-stu-id="ada97-121">Select the **Console** tab and execute the `location.reload()` command.</span></span>  <span data-ttu-id="ada97-122">Dadurch wird das Hintergrundskript erneut ausgeführt, sodass Sie ihren Code schrittweise ausführen können.</span><span class="sxs-lookup"><span data-stu-id="ada97-122">This will re-execute the background script, allowing you to step through your code.</span></span>  
    
    ![Konsole mit eingegebener location.reload](../media/debug-f12-background-console.png)  
    
## <a name="content-script-debugging"></a><span data-ttu-id="ada97-124">Debuggen von Inhaltsskripts</span><span class="sxs-lookup"><span data-stu-id="ada97-124">Content script debugging</span></span>  

<span data-ttu-id="ada97-125">So starten Sie das Debuggen des Inhaltsskripts Ihrer Erweiterung:</span><span class="sxs-lookup"><span data-stu-id="ada97-125">To start debugging the content script of your extension:</span></span>  

1.  <span data-ttu-id="ada97-126">Starten Sie F12, indem Sie entweder zur Schaltfläche **Mehr (...)** navigieren und **F12 Developer Tools** auswählen oder die Tastatur `F12` drücken.</span><span class="sxs-lookup"><span data-stu-id="ada97-126">Launch F12 by either navigating to the **More (...)** button and selecting **F12 Developer Tools** or by pressing `F12` on your keyboard.</span></span>  
1.  <span data-ttu-id="ada97-127">Navigieren Sie zum Inhaltsskript Ihrer Erweiterung, und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="ada97-127">Navigate to and select your extension's content script.</span></span>  <span data-ttu-id="ada97-128">Inhaltsskripts für derzeit ausgeführte Erweiterungen werden von einem anderen Ordner für jede Erweiterung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ada97-128">Content scripts for extensions currently running will be depicted by a different folder for each extension.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="ada97-129">Es werden nur ausgeführte Inhaltsskripts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ada97-129">Only running content scripts will appear.</span></span>  
    
1.  <span data-ttu-id="ada97-130">Platzieren Sie Haltepunkte für das Debuggen, indem Sie links von der Quellcodezeile klicken.</span><span class="sxs-lookup"><span data-stu-id="ada97-130">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
    
    ![f12 mit Debuggen des Inhaltsskripts](../media/debug-content-f12.png)  
    
1.  <span data-ttu-id="ada97-132">Aktualisieren Sie die Browserregisterkarte, um mit dem Schritt durch den Code zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="ada97-132">Refresh the browser tab to begin stepping though your code.</span></span>  
    
## <a name="extension-page-debugging"></a><span data-ttu-id="ada97-133">Debuggen von Erweiterungsseiten</span><span class="sxs-lookup"><span data-stu-id="ada97-133">Extension page debugging</span></span>  

<span data-ttu-id="ada97-134">Es gibt zwei Methoden, die für den Zugriff auf den Quellcode Ihrer Erweiterungsseite zum Debuggen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ada97-134">There are two methods that can be used for accessing the source code of your extension page for debugging.</span></span>  <span data-ttu-id="ada97-135">Eine Methode gilt für eine Vielzahl von Seiten, die andere nur für Popupseiten.</span><span class="sxs-lookup"><span data-stu-id="ada97-135">One method applies to a variety of pages while the other only works for popup pages.</span></span>  

### <a name="debugging-any-extension-page"></a><span data-ttu-id="ada97-136">Debuggen einer beliebigen Erweiterungsseite</span><span class="sxs-lookup"><span data-stu-id="ada97-136">Debugging any extension page</span></span>  

<span data-ttu-id="ada97-137">Die folgende Methode funktioniert für alle Erweiterungsseiten wie die Optionsseite und Popups:</span><span class="sxs-lookup"><span data-stu-id="ada97-137">The following method works for all extension pages like the options page and popups:</span></span>  

1.  <span data-ttu-id="ada97-138">Klicken Sie mit der rechten Maustaste auf den Hintergrund Ihrer Seite.</span><span class="sxs-lookup"><span data-stu-id="ada97-138">Right-click on the background of your page.</span></span>  
1.  <span data-ttu-id="ada97-139">Wählen **Sie Quelle anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="ada97-139">Select **View source**.</span></span>  
    
    ![Öffnen des Popupdebu debuggings mit f12](../media/debug-popup-select.png)  
    
1.  <span data-ttu-id="ada97-141">Nachdem F12 geöffnet wurde, platzieren Sie Haltepunkte in der Datei, die Sie debuggen möchten.</span><span class="sxs-lookup"><span data-stu-id="ada97-141">Once F12 opens, place breakpoints within the file you want to debug.</span></span>  
    
    ![Popupdebu debugging mit f12](../media/debug-popup-f12.png)  
    
1.  <span data-ttu-id="ada97-143">Wählen Sie die **Registerkarte Konsole** aus, und führen Sie den Befehl `location.reload()` aus.</span><span class="sxs-lookup"><span data-stu-id="ada97-143">Select the **Console** tab and execute the command `location.reload()`.</span></span>  <span data-ttu-id="ada97-144">Dadurch wird das Seitenskript erneut ausgeführt, sodass Sie ihren Code schrittweise ausführen können.</span><span class="sxs-lookup"><span data-stu-id="ada97-144">This will re-execute the page script, allowing you to step through your code.</span></span>  
    
    ![Konsole mit eingegebener location.reload](../media/debug-f12-background-console.png)  
    
### <a name="debugging-a-popup-extension-page"></a><span data-ttu-id="ada97-146">Debuggen einer Popuperweiterungsseite</span><span class="sxs-lookup"><span data-stu-id="ada97-146">Debugging a popup extension page</span></span>  

<span data-ttu-id="ada97-147">Die Methode zum Debuggen von Erweiterungsseiten gilt zwar auch für Popuperweiterungsseiten, die folgenden Schritte beschreiben jedoch eine weitere Möglichkeit zum Debuggen Ihres Popups:</span><span class="sxs-lookup"><span data-stu-id="ada97-147">While the method for debugging extension pages also applies to popup extension pages, the following steps outline another way to debug your popup:</span></span>  

1.  <span data-ttu-id="ada97-148">Klicken Sie mit der rechten Maustaste auf das Symbol Ihrer Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="ada97-148">Right-click your extension's icon.</span></span>  
1.  <span data-ttu-id="ada97-149">Wählen **Sie Popup überprüfen aus.**</span><span class="sxs-lookup"><span data-stu-id="ada97-149">Select **Inspect popup**.</span></span>  
    
    ![Überprüfen des Popupdebuggers](../media/debug-popup-inspect.png)  
    
1.  <span data-ttu-id="ada97-151">Führen Sie die Schritte 3 und 4 oben aus, um Haltepunkte zu platzieren und das Popup neu zu laden.</span><span class="sxs-lookup"><span data-stu-id="ada97-151">Follow steps 3 and 4 above for placing breakpoints and reloading the popup.</span></span>  
    