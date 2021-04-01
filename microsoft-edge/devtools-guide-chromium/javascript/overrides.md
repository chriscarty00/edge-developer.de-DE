---
description: Das Feature "Außerkraftsetzungen" ist ein Feature im Quellen Tool von Microsoft Edge devtools, mit dem Sie Webseiten Ressourcen auf Ihre Festplatte kopieren können.  Wenn Sie die Webseite aktualisieren, wird die Ressource von devtools nicht geladen, sondern stattdessen durch Ihre lokale Kopie ersetzt.
title: Überschreiben von Webseiten Ressourcen mit lokalen Kopien mithilfe von Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 7f273f89708e0948e68cd2c7ba79cefb6d7e167c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230964"
---
# <span data-ttu-id="83ab4-105">Überschreiben von Webseiten Ressourcen mit lokalen Kopien mithilfe von Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="83ab4-105">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>  

<span data-ttu-id="83ab4-106">Manchmal müssen Sie ein Problem auf einer Webseite beheben, auf die Sie keinen Zugriff haben, oder Fehlerbehebungen beinhalten einen langsamen und komplexen Buildprozess.</span><span class="sxs-lookup"><span data-stu-id="83ab4-106">Sometimes you need to fix a problem on a webpage that you do not have access to or fixes involve a slow and complex build process.</span></span>  <span data-ttu-id="83ab4-107">Sie können alle Arten von Problemen in devtools Debuggen und beheben.</span><span class="sxs-lookup"><span data-stu-id="83ab4-107">You may debug and fix all kind of problems in DevTools.</span></span> <span data-ttu-id="83ab4-108">Das Problem besteht aber darin, dass die Änderungen nicht fortbestehen.</span><span class="sxs-lookup"><span data-stu-id="83ab4-108">But the problem is the changes do not persist.</span></span>  <span data-ttu-id="83ab4-109">Nachdem Sie die Datei aktualisiert haben, ist Ihre Arbeit nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="83ab4-109">After you refresh the file, all your work is gone.</span></span>  

<span data-ttu-id="83ab4-110">Das Feature "Außerkraftsetzungen" im [Quellen][DevToolsSourcesTool] Tool hilft Ihnen bei der Lösung dieses Problems.</span><span class="sxs-lookup"><span data-stu-id="83ab4-110">The Overrides feature in the [Sources][DevToolsSourcesTool] tool helps you solve this problem.</span></span>  

<span data-ttu-id="83ab4-111">Sie können nun eine Ressource der aktuellen Webseite aufnehmen und lokal speichern.</span><span class="sxs-lookup"><span data-stu-id="83ab4-111">You may now take a resource of the current webpage and store it locally.</span></span>  <span data-ttu-id="83ab4-112">Wenn Sie die Webseite aktualisieren, lädt der Browser die Ressource nicht vom Server.</span><span class="sxs-lookup"><span data-stu-id="83ab4-112">When you refresh the webpage, the browser does not load the resource from the server.</span></span>  <span data-ttu-id="83ab4-113">Stattdessen ersetzt der Browser ihn durch Ihre lokale Kopie der Ressource.</span><span class="sxs-lookup"><span data-stu-id="83ab4-113">Instead the browser replaces it with your local copy of the resource.</span></span>  

## <span data-ttu-id="83ab4-114">Einrichten Ihres lokalen Ordners zum Speichern von Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="83ab4-114">Setting up your local folder to store Overrides</span></span>  

1.  <span data-ttu-id="83ab4-115">Suchen Sie im **Quellen** Tool auf der linken Seite mehrere Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="83ab4-115">In the **Sources** tool, find several sections on the left-hand side.</span></span>  <span data-ttu-id="83ab4-116">Wenn die Option " **Außerkraftsetzungen** " nicht angezeigt wird, wählen Sie die</span><span class="sxs-lookup"><span data-stu-id="83ab4-116">If the **Overrides** option is not displayed, choose the</span></span> <code>&#x0226B;</code><!--`≫`--> <span data-ttu-id="83ab4-117">Symbol, um dorthin zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="83ab4-117">icon to get there.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Quellen Tool mit nicht genügend Speicherplatz, um die Option Außerkraftsetzungen anzuzeigen" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             <span data-ttu-id="83ab4-119">**Quellen** Tool mit nicht genügend Speicherplatz, um die Option "Außerkraftsetzungen" anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="83ab4-119">**Sources** tool with not enough space to show the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Auswählen der Option Außerkraftsetzungen" lightbox="../media/javascript-overrides-menu.msft.png":::
             <span data-ttu-id="83ab4-121">Auswählen der Option "Außerkraftsetzungen"</span><span class="sxs-lookup"><span data-stu-id="83ab4-121">Choose the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="83ab4-122">Nachdem Sie die Option **Overrides** ausgewählt haben, müssen Sie einen Ordner auf dem lokalen Computer auswählen, um die Ressourcendateien zu speichern, die Sie ersetzen möchten.</span><span class="sxs-lookup"><span data-stu-id="83ab4-122">After you choose the **Overrides** option, you must choose a folder on your local computer to store the resource files that you want to replace.</span></span>  <span data-ttu-id="83ab4-123">Wählen Sie den **Ordner + SELECT für Außerkraftsetzungen** aus, um nach einem Ordner zu suchen.</span><span class="sxs-lookup"><span data-stu-id="83ab4-123">Choose the **+ Select folder for overrides** to search for a folder.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Auswählen eines Ordners, der für Außerkraftsetzungen verwendet werden soll" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       <span data-ttu-id="83ab4-125">Auswählen eines Ordners, der für Außerkraftsetzungen verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="83ab4-125">Choose a folder to use for overrides</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="83ab4-126">DevTools warnt Sie, dass der Vollzugriff auf den Ordner vorhanden sein muss und dass Sie keine vertraulichen Informationen offen legen sollten.</span><span class="sxs-lookup"><span data-stu-id="83ab4-126">DevTools warns you that must have full access to the folder and that you should not reveal any sensitive information.</span></span>  <span data-ttu-id="83ab4-127">Wählen Sie auf der warnungsleiste **zulassen** aus, um Zugriff zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="83ab4-127">On the warning bar, choose **Allow** to grant access.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="Gewähren von devtools Zugriff auf Ordner" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       <span data-ttu-id="83ab4-129">Gewähren von devtools Zugriff auf Ordner</span><span class="sxs-lookup"><span data-stu-id="83ab4-129">Grant DevTools access to folder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="83ab4-130">Im Bereich " **Außerkraftsetzungen** " sollte ein Kontrollkästchen neben `Enable Local Overrides` dem Ordner "Überschreibungen" angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="83ab4-130">In the **Overrides** pane, a checkbox should be displayed next to `Enable Local Overrides` and your overrides folder.</span></span>  <span data-ttu-id="83ab4-131">Daneben wird ein Symbol angezeigt, in dem Sie Ihre lokalen Außerkraftsetzungseinstellungen löschen können.</span><span class="sxs-lookup"><span data-stu-id="83ab4-131">An icon is displayed next to it that allows you to delete your local overrides settings.</span></span>  <span data-ttu-id="83ab4-132">Sie haben nun die Einrichtung Ihres Ordners abgeschlossen und sind bereit, Live-Ressourcen durch lokale zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="83ab4-132">You are now done setting up your folder and ready to replace live resources with local ones.</span></span>
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Erfolgreiche Einrichtung eines Overrides-Ordners" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       <span data-ttu-id="83ab4-134">Erfolgreiche Einrichtung eines Overrides-Ordners</span><span class="sxs-lookup"><span data-stu-id="83ab4-134">Successful set up of an overrides folder</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="83ab4-135">Hinzufügen von Dateien zu Ihrem Overrides-Ordner</span><span class="sxs-lookup"><span data-stu-id="83ab4-135">Adding files to your Overrides folder</span></span>  
  
<span data-ttu-id="83ab4-136">Zum Hinzufügen von Dateien zu Ihrem Überschreibungen-Ordner öffnen Sie das **Element** Tool, und überprüfen Sie die Webseite.</span><span class="sxs-lookup"><span data-stu-id="83ab4-136">To add files to your overrides folder, open the **Elements** tool and inspect the webpage.</span></span>  <span data-ttu-id="83ab4-137">Wählen Sie zum Bearbeiten im **Formatvorlagen** -Inspektor den Namen der CSS-Datei aus.</span><span class="sxs-lookup"><span data-stu-id="83ab4-137">To edit, choose the name of the CSS file in the **Styles** inspector.</span></span>  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Auswählen einer Datei im Formatvorlagen-Inspektor" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   <span data-ttu-id="83ab4-139">Auswählen einer Datei im **Formatvorlagen** -Inspektor</span><span class="sxs-lookup"><span data-stu-id="83ab4-139">Choose a file in the **Styles** inspector</span></span>  
:::image-end:::  

<span data-ttu-id="83ab4-140">Zeigen Sie im **Quellen** -Editor auf den Dateinamen der ausgewählten Datei, öffnen Sie das Kontextmenü \(Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **für Außerkraftsetzungen speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="83ab4-140">On the **Sources** editor, hover on the file name of your chosen file, open the contextual menu \(right-click\), and choose **Save for overrides**.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="Fügen Sie im Quellen-Editor den Namen der Datei hinzu, die überschrieben werden soll." lightbox="../media/javascript-overrides-file-name.msft.png":::
   <span data-ttu-id="83ab4-142">Fügen Sie im **Quellen** -Editor den Namen der Datei hinzu, die überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="83ab4-142">In the **Sources** editor, add the name of the file to overrides</span></span>  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="Wählen Sie im Kontextmenü die Option für Außerkraftsetzungen speichern aus." lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   <span data-ttu-id="83ab4-144">Wählen Sie im Kontextmenü die Option **für Außerkraftsetzungen speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="83ab4-144">On the context menu, choose **Save for overrides**</span></span>  
:::image-end:::  

<span data-ttu-id="83ab4-145">Die Datei wird im Ordner Overrides gespeichert.</span><span class="sxs-lookup"><span data-stu-id="83ab4-145">The file is stored in your overrides folder.</span></span>  <span data-ttu-id="83ab4-146">Überprüfen Sie, ob devtools einen Ordner mit dem Namen der URL der Datei mit der richtigen Verzeichnisstruktur erstellt.</span><span class="sxs-lookup"><span data-stu-id="83ab4-146">Verify that DevTools create a folder that is named using the URL of the file with the correct directory structure.</span></span>  <span data-ttu-id="83ab4-147">Die Datei wird in gespeichert.</span><span class="sxs-lookup"><span data-stu-id="83ab4-147">The file is stored inside.</span></span>  <span data-ttu-id="83ab4-148">Der Dateiname im Editor zeigt nun auch einen lila Punkt an, der angibt, dass die Datei lokal und nicht Live ist.</span><span class="sxs-lookup"><span data-stu-id="83ab4-148">The file name in the editor now also shows a purple dot that indicates that the file is local and not a live one.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Die Datei wurde erfolgreich im Ordner Overrides gespeichert" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   <span data-ttu-id="83ab4-150">Die Datei wurde erfolgreich im Ordner "Overrides" gespeichert</span><span class="sxs-lookup"><span data-stu-id="83ab4-150">Successfully stored the file in your overrides folder</span></span>  
:::image-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="83ab4-151">Im folgenden Beispiel können Sie nun die Formatvorlagen der Webseite ändern.</span><span class="sxs-lookup"><span data-stu-id="83ab4-151">In the following example, you may now change the styles of the webpage.</span></span>  <span data-ttu-id="83ab4-152">Wenn Sie einen roten Rahmen um die Datei hinzufügen möchten, kopieren Sie den folgenden Stil im **Formatvorlagen** -Editor, und fügen Sie ihn dem Body-Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="83ab4-152">To add a red border around the file, on the **Styles** editor, copy the following style, and add it to the body element.</span></span>  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="83ab4-153">Die Datei wird automatisch auf Ihrem Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="83ab4-153">The file is automatically saved on your computer.</span></span>  <span data-ttu-id="83ab4-154">Wenn Sie die Datei aktualisieren, wird der Rahmen angezeigt, und keine ihrer Arbeit geht verloren.</span><span class="sxs-lookup"><span data-stu-id="83ab4-154">If you refresh the file, the border is displayed and none of your work is lost.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Dauerhaftes ändern von Webseitenformat Vorlagen durch Bearbeiten einer Datei im Ordner Außerkraftsetzungen" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         <span data-ttu-id="83ab4-156">Dauerhaftes ändern von Webseitenformat Vorlagen durch Bearbeiten einer Datei im Ordner "Außerkraftsetzungen"</span><span class="sxs-lookup"><span data-stu-id="83ab4-156">Change webpage styles persistently by editing a file in your overrides folder</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="83ab4-157">Zeigen Sie im Bereich " **Quellen** " im Abschnitt " **Seite** " auf eine beliebige Datei, öffnen Sie das Kontextmenü \(Klicken Sie mit der rechten Maustaste auf \), und fügen Sie es zu Außerkraftsetzungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="83ab4-157">On the **Sources** tool, in the **Page** section, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="83ab4-158">Auch die Dateien, die sich bereits im Ordner "Außerkraftsetzungen" befinden, haben einen lila Punkt auf dem Symbol.</span><span class="sxs-lookup"><span data-stu-id="83ab4-158">Again, files that are already in your overrides folder have a purple dot on the icon.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Auswählen einer Datei aus dem Quellen Tool für Außerkraftsetzungen" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         <span data-ttu-id="83ab4-160">Auswählen einer Datei aus dem **Quellen** Tool für Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="83ab4-160">Choose a file from the **Sources** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="83ab4-161">Sie können aber auch im **Netzwerk** Tool auf eine beliebige Datei zeigen, das Kontextmenü öffnen \(mit der rechten Maustaste auf \) klicken und es zu Außerkraftsetzungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="83ab4-161">Alternatively, on the **Network** tool, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="83ab4-162">Wenn Außerkraftsetzungen aktiviert sind, finden Sie Dateien, die sich auf Ihrem Computer und nicht auf der Live-Webseite befinden.</span><span class="sxs-lookup"><span data-stu-id="83ab4-162">When overrides are in effect, files that are located on your computer and not from the live webpage.</span></span>  <span data-ttu-id="83ab4-163">Wenn Außerkraftsetzungen aktiviert sind, suchen Sie im Tool **Netzwerk** nach einem Warnungssymbol neben dem Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="83ab4-163">When overrides are in effect, on the **Network** tool, locate a warning icon next to the file name.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Auswählen einer Datei aus dem Netzwerktool für Außerkraftsetzungen" lightbox="../media/javascript-overrides-network.msft.png":::
         <span data-ttu-id="83ab4-165">Auswählen einer Datei aus dem **Netzwerk** Tool für Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="83ab4-165">Choose a file from the **Network** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="83ab4-166">Bidirektionale Interaktion von Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="83ab4-166">Two-way interaction of overrides</span></span>  

<span data-ttu-id="83ab4-167">Verwenden Sie den mit dem **Sources** -Tool von devtools bereitgestellten Editor oder einen beliebigen Editor, in dem Sie die Dateien ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="83ab4-167">Use the editor provided with the **Sources** tool of DevTools or any editor you want to change the files.</span></span>  <span data-ttu-id="83ab4-168">Änderungen werden über alle Produkte synchronisiert, die auf die Dateien im Ordner "Außerkraftsetzungen" zugreifen.</span><span class="sxs-lookup"><span data-stu-id="83ab4-168">Changes are synced across all the products that access the files in the overrides folder.</span></span>  

## <span data-ttu-id="83ab4-169">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="83ab4-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Übersicht über das Quellen Tool | Microsoft docs"  
