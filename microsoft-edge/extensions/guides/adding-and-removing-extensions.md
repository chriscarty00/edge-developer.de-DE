---
description: Erfahren Sie, wie Sie Erweiterungen hinzufügen und entfernen sowie die Schaltfläche einer Erweiterung neben die Adressleiste verschieben können.
title: Hinzufügen und Entfernen von Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, HTML, CSS, JavaScript, Entwickler, Erweiterung
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: aeebc0f18d6b4a743c790571b8287a209233e73f
ms.sourcegitcommit: 1e33cd41e5afb2e6dbdc19353011ff6c2b019f9c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2020
ms.locfileid: "10866078"
---
# <span data-ttu-id="f2249-104">Hinzufügen, Verschieben und Entfernen von Erweiterungen für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f2249-104">Adding, moving, and removing extensions for Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="f2249-105">Die Microsoft Edge-Unterstützung für Erweiterungen wurde im **Windows 10 Anniversary Update** eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f2249-105">Microsoft Edge support for extensions was introduced in the **Windows 10 Anniversary Update**.</span></span> <span data-ttu-id="f2249-106">Wenn Sie eine Microsoft Edge-Erweiterung entwickeln und sie laden möchten oder wenn Sie sie bereits verwenden und jetzt entfernen möchten, lesen Sie die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="f2249-106">If you're developing a Microsoft Edge extension and want to load it up, or if you already have and now want to remove it, check out the steps below.</span></span>
<span data-ttu-id="f2249-107">Außerdem finden Sie hier Einzelheiten dazu, wie Sie die Position Ihres Erweiterungssymbols im Browser ändern können.</span><span class="sxs-lookup"><span data-stu-id="f2249-107">Also included are details on how to change your extension icon's location in the browser.</span></span>

## <span data-ttu-id="f2249-108">Hinzufügen einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="f2249-108">Adding an extension</span></span>

1. <span data-ttu-id="f2249-109">Öffnen Sie Microsoft Edge, und geben Sie "about:flags" in die Adressleiste ein.</span><span class="sxs-lookup"><span data-stu-id="f2249-109">Open Microsoft Edge and type 'about:flags' into the address bar.</span></span>

2. <span data-ttu-id="f2249-110">Aktivieren Sie das Kontrollkästchen **Entwicklerfunktionen für Erweiterungen aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="f2249-110">Select the **Enable extension developer features** checkbox.</span></span>

   !["about:flags" aktivieren Entwicklerfeatures](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > <span data-ttu-id="f2249-112">Wenn Sie nicht über das Windows 10 Anniversary Update oder höher verfügen, steht diese Option nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f2249-112">If you don't have the Windows 10 Anniversary Update or later, this option will not be available.</span></span>

3. <span data-ttu-id="f2249-113">Wählen Sie **Mehr (...)** aus, um das Menü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f2249-113">Select **More (...)** to open the menu.</span></span>

   ![Schaltfläche "Mehr"](./../media/morebutton.png)  

4. <span data-ttu-id="f2249-115">Wählen Sie **Erweiterungen** aus dem Menü aus.</span><span class="sxs-lookup"><span data-stu-id="f2249-115">Select **Extensions** from the menu.</span></span>

5. <span data-ttu-id="f2249-116">Klicken Sie auf die Schaltfläche **Erweiterung laden**.</span><span class="sxs-lookup"><span data-stu-id="f2249-116">Select the **Load extension** button.</span></span>

   !["Erweiterung laden" auswählen](./../media/sideload-load-extension.png)

6. <span data-ttu-id="f2249-118">Navigieren Sie zum Ordner Ihrer Erweiterung, und wählen Sie die Schaltfläche **Ordner auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="f2249-118">Navigate to your extension's folder and select the  **Select folder** button.</span></span>
   ![Zu ladenden Erweiterungsordner auswählen](./../media/sideload-select-extension.png)
   > [!NOTE]
   > <span data-ttu-id="f2249-120">Wird beim Laden der Erweiterung eine Fehlermeldung angezeigt, finden Sie weitere Anleitungen auf der Seite [Problembehandlung](./../troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="f2249-120">If you encounter an error message when loading your extension, refer to the [troubleshooting](./../troubleshooting.md) page for guidance.</span></span>


**<span data-ttu-id="f2249-121">Sie sind fertig!</span><span class="sxs-lookup"><span data-stu-id="f2249-121">You're all set!</span></span> <span data-ttu-id="f2249-122">Die Erweiterung sollte nun im Erweiterungsbereich von Microsoft Edge aufgelistet sein.</span><span class="sxs-lookup"><span data-stu-id="f2249-122">You should now see the extension listed in Microsoft Edge's extension pane.</span></span>**

![Erweiterung im Erweiterungsbereich](./../media/sideload-extension-installed.png)

> [!NOTE]
> <span data-ttu-id="f2249-124">Bei nachfolgenden Starts von Microsoft Edge werden nicht signierte Erweiterungen automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f2249-124">Unsigned extensions are automatically turned off on subsequent launches of Microsoft Edge.</span></span> <span data-ttu-id="f2249-125">Wenn der Browser in einen Ruhezustand übergeht (nach etwa 10 Sekunden Inaktivität), wird unten im Fenster die folgende Benachrichtigung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f2249-125">When the browser enters an idle state (after approximately 10 seconds of inactivity) you will see the following notification at the bottom of the window.</span></span> ![<span data-ttu-id="f2249-126">Riskikobenachrichtigung](./../media/riskynotification.png) Um die unsignierten Erweiterungen zu aktivieren, klicken Sie auf "Trotzdem aktivieren".</span><span class="sxs-lookup"><span data-stu-id="f2249-126">risky notification](./../media/riskynotification.png) To turn on the unsigned extensions, click "Turn on anyway".</span></span>



## <span data-ttu-id="f2249-127">Verschieben der Schaltfläche "Erweiterung"</span><span class="sxs-lookup"><span data-stu-id="f2249-127">Moving the extension button</span></span>
<span data-ttu-id="f2249-128">Je nach den Einstellungen ihrer Erweiterung kann Sie im Menü **Mehr (...)** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f2249-128">Depending on your extension's settings, it could appear in the **More (...)** menu.</span></span>

   ![Aktionsbereich](./../media/browseraction.png)  


<span data-ttu-id="f2249-130">Wenn Sie die Schaltfläche für einen einfacheren Zugriff aus diesem Menü heraus verschieben möchten:</span><span class="sxs-lookup"><span data-stu-id="f2249-130">If you want to move the button out of this menu for easier access:</span></span>

1. <span data-ttu-id="f2249-131">Klicken Sie mit der rechten Maustaste auf die Schaltfläche "Erweiterung".</span><span class="sxs-lookup"><span data-stu-id="f2249-131">Right-click the extension button.</span></span>

2. <span data-ttu-id="f2249-132">Wählen Sie **Schaltfläche neben Adressleiste anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="f2249-132">Select **Show button next to address bar**.</span></span>

   ![Aktionsbereich](./../media/browseraction_contextmenu.png)  

<span data-ttu-id="f2249-134">Alternativ können Sie dies über die Seite mit den Erweiterungsdetails tun:</span><span class="sxs-lookup"><span data-stu-id="f2249-134">Alternatively, you may do this from the extensions details page:</span></span>

1. <span data-ttu-id="f2249-135">Klicken Sie auf die Schaltfläche "Erweiterung".</span><span class="sxs-lookup"><span data-stu-id="f2249-135">Click on the extension button.</span></span>
2. <span data-ttu-id="f2249-136">Aktivieren Sie **Schaltfläche neben Adressleiste anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="f2249-136">Toggle **Show button next to address bar** to on.</span></span>

   ![Aktivierte Umschaltfläche zum Anzeigen der Schaltfläche](./../media/show-button-toggle.png)

> [!NOTE]
> <span data-ttu-id="f2249-138">Sie können die Schaltfläche jederzeit zurück zum Menü **Mehr (...)** bewegen, indem Sie mit der rechten Maustaste darauf klicken und die Option **Neben der Adressleiste anzeigen** deaktivieren oder die Option **Schaltfläche neben Adressleiste anzeigen** auf der Seite mit den Erweiterungsdetails deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="f2249-138">You can always move the button back to the **More (...)** menu by right-clicking it and unselecting **Show next to address bar** or by going to the extension details page and toggling **Show button next to address bar** to off.</span></span>


## <span data-ttu-id="f2249-139">Entfernen einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="f2249-139">Removing an extension</span></span>

1. <span data-ttu-id="f2249-140">Öffnen Sie Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f2249-140">Open Microsoft Edge.</span></span>

2. <span data-ttu-id="f2249-141">Wählen Sie **Mehr (...)** aus, um das Menü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f2249-141">Select **More (...)** to open the menu.</span></span>

3. <span data-ttu-id="f2249-142">Wählen Sie **Erweiterungen** aus dem Menü aus.</span><span class="sxs-lookup"><span data-stu-id="f2249-142">Select **Extensions** from the menu.</span></span>

4. <span data-ttu-id="f2249-143">Klicken Sie mit der rechten Maustaste auf die zu entfernende Erweiterung, und wählen Sie **Entfernen** aus, oder wählen Sie die Erweiterung aus, und klicken Sie auf die Schaltfläche **Entfernen**.</span><span class="sxs-lookup"><span data-stu-id="f2249-143">Right-click the extension you want to remove and select **Remove**, or select the extension and click the **Remove** button.</span></span>

   ![Aktionsbereich](./../media/remove.png)  

**<span data-ttu-id="f2249-145">Die Erweiterung sollte nun nicht mehr in der Liste in Microsoft Edge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f2249-145">The extension should disappear from the list in Microsoft Edge.</span></span>**
