---
description: Hier erfahren Sie, wie Sie Erweiterungen hinzufügen und entfernen sowie die Schaltfläche einer Erweiterung neben der Adressleiste verschieben.
title: Hinzufügen und Entfernen von Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterung
ms.custom: seodec18
localization_priority: Priority
ms.openlocfilehash: fdc6950962e7ce7e0a720d0bafa7e2c63ebd7098
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567431"
---
# <span data-ttu-id="facc8-104">Hinzufügen, verschieben und Entfernen von Erweiterungen für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="facc8-104">Adding, moving, and removing extensions for Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="facc8-105">Microsoft Edge-Unterstützung für Erweiterungen wurde im **Windows 10 Anniversary Update**eingeführt.</span><span class="sxs-lookup"><span data-stu-id="facc8-105">Microsoft Edge support for extensions was introduced in the **Windows 10 Anniversary Update**.</span></span> <span data-ttu-id="facc8-106">Wenn Sie eine Microsoft Edge-Erweiterung entwickeln und Sie laden möchten, oder wenn Sie Sie bereits haben und jetzt entfernen möchten, lesen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="facc8-106">If you're developing a Microsoft Edge extension and want to load it up, or if you already have and now want to remove it, check out the steps below.</span></span>
<span data-ttu-id="facc8-107">Darüber hinaus finden Sie Informationen dazu, wie Sie die Position Ihres Erweiterungssymbols im Browser ändern können.</span><span class="sxs-lookup"><span data-stu-id="facc8-107">Also included are details on how to change your extension icon's location in the browser.</span></span>

## <span data-ttu-id="facc8-108">Hinzufügen einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="facc8-108">Adding an extension</span></span>

1. <span data-ttu-id="facc8-109">Öffnen Sie Microsoft Edge, und geben Sie "about: Flags" in die Adressleiste ein.</span><span class="sxs-lookup"><span data-stu-id="facc8-109">Open Microsoft Edge and type 'about:flags' into the address bar.</span></span>

2. <span data-ttu-id="facc8-110">Aktivieren Sie das Kontrollkästchen **Erweiterungsentwickler Features aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="facc8-110">Select the **Enable extension developer features** checkbox.</span></span>

   ![Info: Flags aktivieren von Entwicklerfeatures](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > <span data-ttu-id="facc8-112">Wenn Sie nicht über das Windows 10 Anniversary Update oder höher verfügen, ist diese Option nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="facc8-112">If you don't have the Windows 10 Anniversary Update or later, this option will not be available.</span></span>

3. <span data-ttu-id="facc8-113">Wählen Sie **mehr (.** ..) aus, um das Menü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="facc8-113">Select **More (...)** to open the menu.</span></span>

   ![Schaltfläche "Weitere"](./../media/morebutton.png)  

4. <span data-ttu-id="facc8-115">Wählen Sie im Menü **Erweiterungen** aus.</span><span class="sxs-lookup"><span data-stu-id="facc8-115">Select **Extensions** from the menu.</span></span>

5. <span data-ttu-id="facc8-116">Wählen Sie die Schaltfläche **Erweiterung laden** aus.</span><span class="sxs-lookup"><span data-stu-id="facc8-116">Select the **Load extension** button.</span></span>

   ![Auswählen der Lade Erweiterung](./../media/sideload-load-extension.png)

6. <span data-ttu-id="facc8-118">Navigieren Sie zum Ordner Ihrer Erweiterung, und wählen Sie die Schaltfläche **Ordner auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="facc8-118">Navigate to your extension's folder and select the  **Select folder** button.</span></span>
   ![Auswählen des zu ladenden Erweiterungs Ordners](./../media/sideload-select-extension.png)
   > [!NOTE]
   > <span data-ttu-id="facc8-120">Wenn beim Laden der Erweiterung eine Fehlermeldung angezeigt wird, lesen Sie auf der Seite zur [Problembehandlung](./../troubleshooting.md) nach Anleitungen.</span><span class="sxs-lookup"><span data-stu-id="facc8-120">If you encounter an error message when loading your extension, refer to the [troubleshooting](./../troubleshooting.md) page for guidance.</span></span>


**<span data-ttu-id="facc8-121">Sie haben es geschafft!</span><span class="sxs-lookup"><span data-stu-id="facc8-121">You're all set!</span></span> <span data-ttu-id="facc8-122">Die im Erweiterungsbereich von Microsoft Edge aufgelistete Erweiterung wird nun angezeigt.</span><span class="sxs-lookup"><span data-stu-id="facc8-122">You should now see the extension listed in Microsoft Edge's extension pane.</span></span>**

![Erweiterung im Erweiterungsbereich](./../media/sideload-extension-installed.png)

> [!NOTE]
> <span data-ttu-id="facc8-124">Nicht signierte Erweiterungen werden bei nachfolgenden Starts von Microsoft Edge automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="facc8-124">Unsigned extensions are automatically turned off on subsequent launches of Microsoft Edge.</span></span> <span data-ttu-id="facc8-125">Wenn der Browser in einen Ruhezustand wechselt (nach ungefähr 10 Sekunden Inaktivität), wird unten im Fenster die folgende Benachrichtigung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="facc8-125">When the browser enters an idle state (after approximately 10 seconds of inactivity) you will see the following notification at the bottom of the window.</span></span> ![<span data-ttu-id="facc8-126">riskante Benachrichtigung wenn ](./../media/riskynotification.png) Sie die nicht signierten Erweiterungen aktivieren möchten, klicken Sie auf "trotzdem einschalten".</span><span class="sxs-lookup"><span data-stu-id="facc8-126">risky notification](./../media/riskynotification.png) To turn on the unsigned extensions, click "Turn on anyway".</span></span>



## <span data-ttu-id="facc8-127">Verschieben der Erweiterungsschaltfläche</span><span class="sxs-lookup"><span data-stu-id="facc8-127">Moving the extension button</span></span>
<span data-ttu-id="facc8-128">Je nach den Einstellungen ihrer Erweiterung kann Sie im Menü **mehr (.** ..) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="facc8-128">Depending on your extension's settings, it could appear in the **More (...)** menu.</span></span>

   ![Menü ' Aktionen '](./../media/browseraction.png)  


<span data-ttu-id="facc8-130">Wenn Sie die Schaltfläche für einen einfacheren Zugriff aus diesem Menü verschieben möchten, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="facc8-130">If you want to move the button out of this menu for easier access:</span></span>

1. <span data-ttu-id="facc8-131">Klicken Sie mit der rechten Maustaste auf die Erweiterungsschaltfläche.</span><span class="sxs-lookup"><span data-stu-id="facc8-131">Right-click the extension button.</span></span>

2. <span data-ttu-id="facc8-132">Wählen Sie **neben der Adressleiste die Schaltfläche anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="facc8-132">Select **Show button next to address bar**.</span></span>

   ![Menü ' Aktionen '](./../media/browseraction_contextmenu.png)  

<span data-ttu-id="facc8-134">Sie können dies auch über die Seite mit den Erweiterungs Details tun:</span><span class="sxs-lookup"><span data-stu-id="facc8-134">Alternatively, you may do this from the extensions details page:</span></span>

1. <span data-ttu-id="facc8-135">Klicken Sie auf die Erweiterungsschaltfläche.</span><span class="sxs-lookup"><span data-stu-id="facc8-135">Click on the extension button.</span></span>
2. <span data-ttu-id="facc8-136">**Schaltfläche "anzeigen" neben Adressleiste** auf ein umschalten.</span><span class="sxs-lookup"><span data-stu-id="facc8-136">Toggle **Show button next to address bar** to on.</span></span>

   ![Schaltfläche "Schalter anzeigen" aktiviert](./../media/show-button-toggle.png)

> [!NOTE]
> <span data-ttu-id="facc8-138">Sie können die Schaltfläche immer wieder in das Menü **mehr (...)** verschieben, indem Sie mit der rechten Maustaste darauf klicken und die Option **neben der Adressleiste anzeigen** oder auf der Seite Erweiterungs Details auf die **Schaltfläche "anzeigen" neben "Adressleiste"** und dann auf "aus" klicken.</span><span class="sxs-lookup"><span data-stu-id="facc8-138">You can always move the button back to the **More (...)** menu by right-clicking it and unselecting **Show next to address bar** or by going to the extension details page and toggling **Show button next to address bar** to off.</span></span>


## <span data-ttu-id="facc8-139">Entfernen einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="facc8-139">Removing an extension</span></span>

1. <span data-ttu-id="facc8-140">Öffnen Sie Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="facc8-140">Open Microsoft Edge.</span></span>

2. <span data-ttu-id="facc8-141">Wählen Sie **mehr (.** ..) aus, um das Menü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="facc8-141">Select **More (...)** to open the menu.</span></span>

3. <span data-ttu-id="facc8-142">Wählen Sie im Menü **Erweiterungen** aus.</span><span class="sxs-lookup"><span data-stu-id="facc8-142">Select **Extensions** from the menu.</span></span>

4. <span data-ttu-id="facc8-143">Klicken Sie mit der rechten Maustaste auf die zu entfernende Erweiterung, wählen Sie **Entfernen**aus, oder wählen Sie die Erweiterung aus, und klicken Sie auf die Schaltfläche **Entfernen** .</span><span class="sxs-lookup"><span data-stu-id="facc8-143">Right-click the extension you want to remove and select **Remove**, or select the extension and click the **Remove** button.</span></span>

   ![Menü ' Aktionen '](./../media/remove.png)  

**<span data-ttu-id="facc8-145">Die Erweiterung sollte aus der Liste in Microsoft Edge verschwinden.</span><span class="sxs-lookup"><span data-stu-id="facc8-145">The extension should disappear from the list in Microsoft Edge.</span></span>**
