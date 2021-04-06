---
description: Das Außerkraftsetzungsfeature ist ein Feature innerhalb des Tools Sources von Microsoft Edge DevTools, mit dem Sie Webseitenressourcen auf Ihre Festplatte kopieren können.  Wenn Sie die Webseite aktualisieren, laden DevTools die Ressource nicht, sondern ersetzen sie durch Ihre lokale Kopie.
title: Überschreiben von Webseitenressourcen mit lokalen Kopien mithilfe von Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 7f273f89708e0948e68cd2c7ba79cefb6d7e167c
ms.sourcegitcommit: 2ddfd98d1e871be9c61380a8ca57da398d38bd54
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "11230964"
---
# <a name="override-webpage-resources-with-local-copies-using-microsoft-edge-devtools"></a><span data-ttu-id="f43d2-105">Überschreiben von Webseitenressourcen mit lokalen Kopien mithilfe von Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f43d2-105">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>  

<span data-ttu-id="f43d2-106">Manchmal müssen Sie ein Problem auf einer Webseite beheben, auf die Sie keinen Zugriff haben, oder Korrekturen beinhalten einen langsamen und komplexen Buildprozess.</span><span class="sxs-lookup"><span data-stu-id="f43d2-106">Sometimes you need to fix a problem on a webpage that you do not have access to or fixes involve a slow and complex build process.</span></span>  <span data-ttu-id="f43d2-107">Sie können alle Arten von Problemen in DevTools debuggen und beheben.</span><span class="sxs-lookup"><span data-stu-id="f43d2-107">You may debug and fix all kind of problems in DevTools.</span></span> <span data-ttu-id="f43d2-108">Das Problem ist jedoch, dass die Änderungen nicht beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="f43d2-108">But the problem is the changes do not persist.</span></span>  <span data-ttu-id="f43d2-109">Nachdem Sie die Datei aktualisiert haben, sind alle Ihre Arbeit weg.</span><span class="sxs-lookup"><span data-stu-id="f43d2-109">After you refresh the file, all your work is gone.</span></span>  

<span data-ttu-id="f43d2-110">Das Überschreibungsfeature im [Tool Quellen][DevToolsSourcesTool] hilft Ihnen bei der Lösung dieses Problems.</span><span class="sxs-lookup"><span data-stu-id="f43d2-110">The Overrides feature in the [Sources][DevToolsSourcesTool] tool helps you solve this problem.</span></span>  

<span data-ttu-id="f43d2-111">Sie können nun eine Ressource der aktuellen Webseite verwenden und lokal speichern.</span><span class="sxs-lookup"><span data-stu-id="f43d2-111">You may now take a resource of the current webpage and store it locally.</span></span>  <span data-ttu-id="f43d2-112">Wenn Sie die Webseite aktualisieren, wird die Ressource vom Browser nicht vom Server geladen.</span><span class="sxs-lookup"><span data-stu-id="f43d2-112">When you refresh the webpage, the browser does not load the resource from the server.</span></span>  <span data-ttu-id="f43d2-113">Stattdessen ersetzt der Browser sie durch Ihre lokale Kopie der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f43d2-113">Instead the browser replaces it with your local copy of the resource.</span></span>  

## <a name="setting-up-your-local-folder-to-store-overrides"></a><span data-ttu-id="f43d2-114">Einrichten des lokalen Ordners zum Speichern von Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="f43d2-114">Setting up your local folder to store Overrides</span></span>  

1.  <span data-ttu-id="f43d2-115">Suchen Sie **im Tool** Quellen auf der linken Seite nach mehreren Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="f43d2-115">In the **Sources** tool, find several sections on the left-hand side.</span></span>  <span data-ttu-id="f43d2-116">Wenn die **Option Außerkraftsetzungen** nicht angezeigt wird, wählen Sie die Option</span><span class="sxs-lookup"><span data-stu-id="f43d2-116">If the **Overrides** option is not displayed, choose the</span></span> <code>&#x0226B;</code><!--`≫`--> <span data-ttu-id="f43d2-117">icon to get there.</span><span class="sxs-lookup"><span data-stu-id="f43d2-117">icon to get there.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Quellentool mit nicht genügend Platz zum Anzeigen der Option Außerkraftsetzungen" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             <span data-ttu-id="f43d2-119">**Quellentool** mit nicht genügend Platz zum Anzeigen der Option "Außerkraftsetzungen"</span><span class="sxs-lookup"><span data-stu-id="f43d2-119">**Sources** tool with not enough space to show the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Auswählen der Option Außerkraftsetzungen" lightbox="../media/javascript-overrides-menu.msft.png":::
             <span data-ttu-id="f43d2-121">Auswählen der Option Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="f43d2-121">Choose the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="f43d2-122">Nachdem Sie die **Option Außerkraftsetzungen** ausgewählt haben, müssen Sie einen Ordner auf dem lokalen Computer auswählen, um die Ressourcendateien zu speichern, die Sie ersetzen möchten.</span><span class="sxs-lookup"><span data-stu-id="f43d2-122">After you choose the **Overrides** option, you must choose a folder on your local computer to store the resource files that you want to replace.</span></span>  <span data-ttu-id="f43d2-123">Wählen Sie den **Ordner + Auswählen für Außerkraftsetzungen aus,** um nach einem Ordner zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f43d2-123">Choose the **+ Select folder for overrides** to search for a folder.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Auswählen eines Ordners, der für Außerkraftsetzungen verwendet werden soll" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       <span data-ttu-id="f43d2-125">Auswählen eines Ordners, der für Außerkraftsetzungen verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="f43d2-125">Choose a folder to use for overrides</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f43d2-126">DevTools warnt Sie, dass Sie voll auf den Ordner zugreifen müssen und keine vertraulichen Informationen preis geben sollten.</span><span class="sxs-lookup"><span data-stu-id="f43d2-126">DevTools warns you that must have full access to the folder and that you should not reveal any sensitive information.</span></span>  <span data-ttu-id="f43d2-127">Wählen Sie auf der Warnleiste Die Option **Zugriff** gewähren zulassen aus.</span><span class="sxs-lookup"><span data-stu-id="f43d2-127">On the warning bar, choose **Allow** to grant access.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="Gewähren von DevTools-Zugriff auf Ordner" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       <span data-ttu-id="f43d2-129">Gewähren von DevTools-Zugriff auf Ordner</span><span class="sxs-lookup"><span data-stu-id="f43d2-129">Grant DevTools access to folder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f43d2-130">Im **Bereich Außerkraftsetzungen** sollte neben dem Ordner "Außerkraftsetzungen" ein `Enable Local Overrides` Kontrollkästchen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f43d2-130">In the **Overrides** pane, a checkbox should be displayed next to `Enable Local Overrides` and your overrides folder.</span></span>  <span data-ttu-id="f43d2-131">Neben dem Symbol wird ein Symbol angezeigt, mit dem Sie Ihre lokalen Außerkraftsetzungseinstellungen löschen können.</span><span class="sxs-lookup"><span data-stu-id="f43d2-131">An icon is displayed next to it that allows you to delete your local overrides settings.</span></span>  <span data-ttu-id="f43d2-132">Sie sind nun mit dem Einrichten Ihres Ordners fertig und können live-Ressourcen durch lokale ersetzen.</span><span class="sxs-lookup"><span data-stu-id="f43d2-132">You are now done setting up your folder and ready to replace live resources with local ones.</span></span>
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Erfolgreiches Einrichten eines Außerkraftsetzungsordners" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       <span data-ttu-id="f43d2-134">Erfolgreiches Einrichten eines Außerkraftsetzungsordners</span><span class="sxs-lookup"><span data-stu-id="f43d2-134">Successful set up of an overrides folder</span></span>  
    :::image-end:::  
    
## <a name="adding-files-to-your-overrides-folder"></a><span data-ttu-id="f43d2-135">Hinzufügen von Dateien zum Ordner Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="f43d2-135">Adding files to your Overrides folder</span></span>  
  
<span data-ttu-id="f43d2-136">Öffnen Sie das Elementtool, und überprüfen Sie die Webseite, um Dem Ordner "Außerkraftsetzungen" Dateien hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f43d2-136">To add files to your overrides folder, open the **Elements** tool and inspect the webpage.</span></span>  <span data-ttu-id="f43d2-137">Wählen Sie zum Bearbeiten den Namen der CSS-Datei im **Formatvorlageninspektor** aus.</span><span class="sxs-lookup"><span data-stu-id="f43d2-137">To edit, choose the name of the CSS file in the **Styles** inspector.</span></span>  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Auswählen einer Datei im Formatvorlageninspektor" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   <span data-ttu-id="f43d2-139">Auswählen einer Datei im **Formatvorlageninspektor**</span><span class="sxs-lookup"><span data-stu-id="f43d2-139">Choose a file in the **Styles** inspector</span></span>  
:::image-end:::  

<span data-ttu-id="f43d2-140">Zeigen Sie **im Editor** Quellen auf den Dateinamen der ausgewählten Datei, öffnen Sie das Kontextmenü \(rechtsklicken\), und wählen Sie Speichern für **Außerkraftsetzungen aus.**</span><span class="sxs-lookup"><span data-stu-id="f43d2-140">On the **Sources** editor, hover on the file name of your chosen file, open the contextual menu \(right-click\), and choose **Save for overrides**.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="Fügen Sie im Quellen-Editor den Namen der Datei zu Außerkraftsetzungen hinzu." lightbox="../media/javascript-overrides-file-name.msft.png":::
   <span data-ttu-id="f43d2-142">Fügen Sie **im Quellen-Editor** den Namen der Datei zu Außerkraftsetzungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="f43d2-142">In the **Sources** editor, add the name of the file to overrides</span></span>  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="Wählen Sie im Kontextmenü Speichern für Außerkraftsetzungen aus." lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   <span data-ttu-id="f43d2-144">Wählen Sie im Kontextmenü Speichern **für Außerkraftsetzungen aus.**</span><span class="sxs-lookup"><span data-stu-id="f43d2-144">On the context menu, choose **Save for overrides**</span></span>  
:::image-end:::  

<span data-ttu-id="f43d2-145">Die Datei wird in Ihrem Überschreibungsordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f43d2-145">The file is stored in your overrides folder.</span></span>  <span data-ttu-id="f43d2-146">Stellen Sie sicher, dass DevTools einen Ordner mit dem Namen mithilfe der URL der Datei mit der richtigen Verzeichnisstruktur erstellt.</span><span class="sxs-lookup"><span data-stu-id="f43d2-146">Verify that DevTools create a folder that is named using the URL of the file with the correct directory structure.</span></span>  <span data-ttu-id="f43d2-147">Die Datei wird darin gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f43d2-147">The file is stored inside.</span></span>  <span data-ttu-id="f43d2-148">Der Dateiname im Editor zeigt nun auch einen lila Punkt an, der angibt, dass die Datei lokal und nicht live ist.</span><span class="sxs-lookup"><span data-stu-id="f43d2-148">The file name in the editor now also shows a purple dot that indicates that the file is local and not a live one.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Die Datei wurde erfolgreich im Ordner Außerkraftsetzungen gespeichert." lightbox="../media/javascript-overrides-file-stored.msft.png":::
   <span data-ttu-id="f43d2-150">Die Datei wurde erfolgreich im Ordner "Außerkraftsetzungen" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f43d2-150">Successfully stored the file in your overrides folder</span></span>  
:::image-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="f43d2-151">Im folgenden Beispiel können Sie nun die Formatvorlagen der Webseite ändern.</span><span class="sxs-lookup"><span data-stu-id="f43d2-151">In the following example, you may now change the styles of the webpage.</span></span>  <span data-ttu-id="f43d2-152">Wenn Sie einen roten Rahmen um die Datei hinzufügen möchten, kopieren Sie im Formatvorlagen-Editor die folgende Formatvorlage, und fügen Sie sie dem body-Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="f43d2-152">To add a red border around the file, on the **Styles** editor, copy the following style, and add it to the body element.</span></span>  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f43d2-153">Die Datei wird automatisch auf Ihrem Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f43d2-153">The file is automatically saved on your computer.</span></span>  <span data-ttu-id="f43d2-154">Wenn Sie die Datei aktualisieren, wird der Rahmen angezeigt, und ihre Arbeit geht nicht verloren.</span><span class="sxs-lookup"><span data-stu-id="f43d2-154">If you refresh the file, the border is displayed and none of your work is lost.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Webseitenformatvorlagen dauerhaft ändern, indem Sie eine Datei im Ordner Außerkraftsetzungen bearbeiten" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         <span data-ttu-id="f43d2-156">Webseitenformatvorlagen dauerhaft ändern, indem Sie eine Datei im Ordner "Außerkraftsetzungen" bearbeiten</span><span class="sxs-lookup"><span data-stu-id="f43d2-156">Change webpage styles persistently by editing a file in your overrides folder</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="f43d2-157">Zeigen Sie **im Tool** Quellen im Abschnitt **Seite** auf eine beliebige Datei, öffnen Sie das Kontextmenü \(mit der rechten Maustaste auf\), und fügen Sie es außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="f43d2-157">On the **Sources** tool, in the **Page** section, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="f43d2-158">Auch hier haben Dateien, die sich bereits im Ordner "Außerkraftsetzungen" befinden, einen lila Punkt auf dem Symbol.</span><span class="sxs-lookup"><span data-stu-id="f43d2-158">Again, files that are already in your overrides folder have a purple dot on the icon.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Auswählen einer Datei aus dem Tool Quellen für Außerkraftsetzungen" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         <span data-ttu-id="f43d2-160">Auswählen einer Datei aus dem **Tool "Quellen"** für Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="f43d2-160">Choose a file from the **Sources** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f43d2-161">Alternativ zeigen Sie im **Netzwerktool** auf eine beliebige Datei, öffnen Sie das Kontextmenü \(rechtsklicken\), und fügen Sie es außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="f43d2-161">Alternatively, on the **Network** tool, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="f43d2-162">Wenn Außerkraftsetzungen wirksam sind, dateien, die sich auf Ihrem Computer befinden und nicht von der Livewebseite.</span><span class="sxs-lookup"><span data-stu-id="f43d2-162">When overrides are in effect, files that are located on your computer and not from the live webpage.</span></span>  <span data-ttu-id="f43d2-163">Wenn Außerkraftsetzungen wirksam sind, suchen Sie im **Netzwerktool** ein Warnsymbol neben dem Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="f43d2-163">When overrides are in effect, on the **Network** tool, locate a warning icon next to the file name.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Auswählen einer Datei aus dem Netzwerktool für Außerkraftsetzungen" lightbox="../media/javascript-overrides-network.msft.png":::
         <span data-ttu-id="f43d2-165">Auswählen einer Datei aus dem **Netzwerktool** für Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="f43d2-165">Choose a file from the **Network** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="two-way-interaction-of-overrides"></a><span data-ttu-id="f43d2-166">Zwei-Wege-Interaktion von Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="f43d2-166">Two-way interaction of overrides</span></span>  

<span data-ttu-id="f43d2-167">Verwenden Sie den Editor, der mit dem **Sources-Tool** von DevTools oder einem beliebigen Editor bereitgestellt wird, den Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="f43d2-167">Use the editor provided with the **Sources** tool of DevTools or any editor you want to change the files.</span></span>  <span data-ttu-id="f43d2-168">Änderungen werden für alle Produkte synchronisiert, die auf die Dateien im Ordner "Außerkraftsetzungen" zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f43d2-168">Changes are synced across all the products that access the files in the overrides folder.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f43d2-169">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="f43d2-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Übersicht über das | Microsoft Docs"  
