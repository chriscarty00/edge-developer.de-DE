---
description: Informieren Sie sich über die verschiedenen Entwurfsaspekte und das Benutzeroberflächenverhalten, die beim Erstellen von Microsoft Edge-Erweiterungen zu berücksichtigen sind.
title: Erweiterungen – Entwurf
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, JavaScript, Design, Symbole, Entwickler
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a32223f93baf44d2ca523e92cf9d7584ad9a8333
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234181"
---
# <span data-ttu-id="54ad2-104">Entwurfsrichtlinien für Microsoft Edge-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="54ad2-104">Design Guidelines For Microsoft Edge Extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="54ad2-105">Die folgende Seite enthält verschiedene Entwurfsaspekte und Benutzeroberflächenverhalten, die beim Erstellen von Microsoft Edge-Erweiterungen zu berücksichtigen sind.</span><span class="sxs-lookup"><span data-stu-id="54ad2-105">The following page contains various design aspects and UI behavior to consider when creating Microsoft Edge extensions.</span></span>  

## <span data-ttu-id="54ad2-106">Symbole</span><span class="sxs-lookup"><span data-stu-id="54ad2-106">Icons</span></span>  

<span data-ttu-id="54ad2-107">Sie sollten die Symbole ihrer Erweiterung mithilfe einer Vektorgrafik erstellen.</span><span class="sxs-lookup"><span data-stu-id="54ad2-107">You should make the icons of your extension using a vector graphic.</span></span>  <span data-ttu-id="54ad2-108">Sie müssen ein paar unterschiedliche Größen Ihres Symbols für Ihre Erweiterung und drei zusätzliche Größen erstellen, wenn Sie Ihre Erweiterung verpacken möchten.</span><span class="sxs-lookup"><span data-stu-id="54ad2-108">You must create a few different sizes of your icon for your extension, and three additional sizes if you want to package your extension.</span></span>  <span data-ttu-id="54ad2-109">Microsoft Edge-Erweiterungen unterstützen keine SVG-Symbole.</span><span class="sxs-lookup"><span data-stu-id="54ad2-109">Microsoft Edge extensions do not support .svg icons.</span></span>  

<span data-ttu-id="54ad2-110">Bevor Sie Ihre Erweiterungssymbole erstellen, sollten Sie den Leitfaden zur [Barrierefreiheit][ExtensionsGuidesAccessibility] überprüfen, um sicherzustellen, dass Ihre Symbole einen hohen Kontrast aufweisen und sowohl in hellen als auch in dunklen Designs von Microsoft Edge sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="54ad2-110">Before you create your extension icons, you should review the [accessibility][ExtensionsGuidesAccessibility] guide to ensure that your icons have high enough contrast and are visible in both the light and dark themes of Microsoft Edge.</span></span>  

<span data-ttu-id="54ad2-111">Während ein WebKit-Bildformat unterstützt wird, werden PNG-Symbole für die Transparenz Unterstützung empfohlen.</span><span class="sxs-lookup"><span data-stu-id="54ad2-111">While any webkit image format is supported, .png icons are recommended for transparency support.</span></span>  

### <span data-ttu-id="54ad2-112">Symbole für Ihre Erweiterung</span><span class="sxs-lookup"><span data-stu-id="54ad2-112">Icons for your extension</span></span>  

<span data-ttu-id="54ad2-113">Für Ihre Erweiterung müssen Sie eine Symbolgröße für die Browser Aktion oder Seiten Aktion und eine Symbolgröße für den Bereich " **Erweiterungen** " erstellen.</span><span class="sxs-lookup"><span data-stu-id="54ad2-113">For your extension, you must create one icon size for the browser action or page action, and one icon size for the **Extensions** pane.</span></span>  <span data-ttu-id="54ad2-114">Es können mehr als eine Größe für die einzelnen Größen zur Unterstützung von Displays mit höherer Auflösung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="54ad2-114">More than one size for each may be provided to support high resolution displays.</span></span>  

<span data-ttu-id="54ad2-115">Eine Erweiterung sollte über eine Browser Aktion oder ein Symbol für eine Seiten Aktion verfügen.</span><span class="sxs-lookup"><span data-stu-id="54ad2-115">An extension should have a browser action or page action icon.</span></span>  <span data-ttu-id="54ad2-116">Die Browser Aktion-und Seiten Aktionssymbole können zur Laufzeit mithilfe der [BrowserAction. SetIcon][MSDApiBrowseractionSeticon] -Methode oder der [PageAction. SetIcon][MDNApiPageactionSeticon] -Methode geändert werden.</span><span class="sxs-lookup"><span data-stu-id="54ad2-116">The browser action and page action icons may be changed at runtime using the [browserAction.setIcon][MSDApiBrowseractionSeticon] method or [pageAction.setIcon][MDNApiPageactionSeticon] method.</span></span>  

#### <span data-ttu-id="54ad2-117">Browser Aktion</span><span class="sxs-lookup"><span data-stu-id="54ad2-117">Browser action</span></span>  

<span data-ttu-id="54ad2-118">Die bevorzugten Größen für Browser Aktion und Seiten Aktionssymbole sind `20px` , `25px` , `30px` und `40px` .</span><span class="sxs-lookup"><span data-stu-id="54ad2-118">The preferred sizes for browser action and page action icons are `20px`, `25px`, `30px`, and `40px`.</span></span>  <span data-ttu-id="54ad2-119">Zu den anderen unterstützten Größen gehören `19px` , `35px` und `38px` .</span><span class="sxs-lookup"><span data-stu-id="54ad2-119">Other supported sizes include `19px`, `35px`, and `38px`.</span></span>  

<span data-ttu-id="54ad2-120">Die folgende [manifest.jsim][ExtensionsApisupportManifestkeys] Datei-Snippet zeigt ein Standard-und HD-Browser-Aktionssymbol, das mit dem [browser_action][MDNManifestjsonBrowserAction] -Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="54ad2-120">The following [manifest.json][ExtensionsApisupportManifestkeys] file snippet shows a standard and high definition browser action icon being specified using the [browser_action][MDNManifestjsonBrowserAction] key.</span></span>  <span data-ttu-id="54ad2-121">Für den [page_action][MDNManifestjsonPageAction] -Schlüssel gilt dieselbe Syntax.</span><span class="sxs-lookup"><span data-stu-id="54ad2-121">The same syntax applies for the [page_action][MDNManifestjsonPageAction] key.</span></span>  

```json
"browser_action": {
    "default_icon": {
        "20": "images/icon_20.png",
        "40": "images/icon_40.png"
    },
    "default_title": "Fetch page info",
    "default_popup": "popup.html"
}
```  

<span data-ttu-id="54ad2-122">Wenn die Browser Aktion durch die Erweiterung eingestellt wurde, wird Sie entweder im Menü Aktionen nach dem Auswählen von **mehr (...)** oder rechts neben der Adressleiste angezeigt, wenn der Benutzer die **Schaltfläche "anzeigen" neben der Adressleiste** aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="54ad2-122">If the browser action has been set by the extension, it appears either in the Actions menu after selecting **More(...)**,  or to the right of the address bar if **Show button next to the address bar** has been toggled on by the user.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/actionmenu-browseraction.png" alt-text="Browser Aktion im Menü ' Aktion '":::
         <span data-ttu-id="54ad2-124">Browser Aktion im Menü ' Aktion '</span><span class="sxs-lookup"><span data-stu-id="54ad2-124">Browser action in action menu</span></span> :::image-end:::
      
      <!--![browser action in action menu][ImageActionmenuBrowseraction]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/browseractionicon.png" alt-text="Browser Aktion":::
         <span data-ttu-id="54ad2-126">Browser Aktion</span><span class="sxs-lookup"><span data-stu-id="54ad2-126">Browser action</span></span> :::image-end:::
      
      <!--![browser action][ImageBrowserActionIcon]  -->  
   :::column-end:::
:::row-end:::

#### <span data-ttu-id="54ad2-127">Seiten Aktion</span><span class="sxs-lookup"><span data-stu-id="54ad2-127">Page action</span></span>  

<span data-ttu-id="54ad2-128">Der [page_action][MDNManifestjsonPageAction] -Schlüssel hat dieselbe JSON-Manifest-Syntax wie der [browser_action][MDNManifestjsonBrowserAction] -Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="54ad2-128">The [page_action][MDNManifestjsonPageAction] key has the same JSON manifest syntax as the [browser_action][MDNManifestjsonBrowserAction] key.</span></span>  <span data-ttu-id="54ad2-129">Die Seiten Aktion weist auch die gleichen Symbolgrößen Anforderungen wie Browser Aktion auf.</span><span class="sxs-lookup"><span data-stu-id="54ad2-129">Page action also has the same icon size requirements as browser action.</span></span>  

<span data-ttu-id="54ad2-130">Wenn die Seiten Aktion in der Datei " [manifest.js][ExtensionsApisupportManifestkeys] " angegeben ist, wird Sie in der Adressleiste angezeigt, wenn die [PageAction. Show][MDNApiPageactionShow] -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="54ad2-130">If page action is specified in the [manifest.json][ExtensionsApisupportManifestkeys] file, it appears within the address bar whenever the [pageAction.show][MDNApiPageactionShow] method is used.</span></span>  

:::image type="complex" source="../media/pageaction.png" alt-text="Seiten Aktion":::
   <span data-ttu-id="54ad2-132">Seiten Aktion</span><span class="sxs-lookup"><span data-stu-id="54ad2-132">Page action</span></span>
:::image-end:::

<!--![page action][ImagePageaction]  -->  

##### <span data-ttu-id="54ad2-133">Verwaltungsoberfläche</span><span class="sxs-lookup"><span data-stu-id="54ad2-133">Management UI</span></span>  

<span data-ttu-id="54ad2-134">Wenn Benutzer zum Bereich "Erweiterungen" navigieren, indem Sie im Menü **mehr (.** ..) und dann auf **Erweiterungen**klicken, wird neben dem Namen der Erweiterung ein Symbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="54ad2-134">When users navigate to the extensions pane by going to the **More(...)** menu and selecting **Extensions**, an icon is displayed next to the name of the extension.</span></span>  

<span data-ttu-id="54ad2-135">Sie sollten die folgenden Symbolgrößen angeben.</span><span class="sxs-lookup"><span data-stu-id="54ad2-135">You should specify the following icon sizes.</span></span>  

| <span data-ttu-id="54ad2-136">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="54ad2-136">Key</span></span> | <span data-ttu-id="54ad2-137">Details</span><span class="sxs-lookup"><span data-stu-id="54ad2-137">Details</span></span> |  
|:--- |:--- |  
| `48px` | <span data-ttu-id="54ad2-138">Das Symbol für die Standardauflösung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="54ad2-138">Icon for standard resolution displays.</span></span> |  
| `128px` | <span data-ttu-id="54ad2-139">Symbol für Displays mit höherer Auflösung.</span><span class="sxs-lookup"><span data-stu-id="54ad2-139">Icon for high resolution displays.</span></span> |  
| `176px` | <span data-ttu-id="54ad2-140">Das Symbol für eine noch höhere Auflösung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="54ad2-140">Icon for even higher resolution displays.</span></span> |  


```json
"icons": {
    "48": "images/icon_48.png",
    "128": "images/icon_128.png",
    "176": "images/icon_176.png"
},
```  

:::image type="complex" source="../media/management-ui.png" alt-text="Verwaltungsoberfläche":::
   <span data-ttu-id="54ad2-142">Verwaltungsoberfläche</span><span class="sxs-lookup"><span data-stu-id="54ad2-142">Management UI</span></span>
:::image-end:::

<!--![management UI][ImageManagementUi]  -->  

### <span data-ttu-id="54ad2-143">Symbole für Verpackungen</span><span class="sxs-lookup"><span data-stu-id="54ad2-143">Icons for packaging</span></span>  

<span data-ttu-id="54ad2-144">Sobald Ihre Erweiterung für die Verpackung bereit ist, müssen Sie drei weitere Symbolgrößen bereithalten.</span><span class="sxs-lookup"><span data-stu-id="54ad2-144">Once your extension is ready for packaging, you must have three additional icon sizes ready.</span></span>  

| <span data-ttu-id="54ad2-145">Size</span><span class="sxs-lookup"><span data-stu-id="54ad2-145">Size</span></span> | <span data-ttu-id="54ad2-146">Details</span><span class="sxs-lookup"><span data-stu-id="54ad2-146">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="54ad2-147">44px</span><span class="sxs-lookup"><span data-stu-id="54ad2-147">44px</span></span> | <span data-ttu-id="54ad2-148">Wird in der Windows-Benutzeroberfläche verwendet \(**App-Liste**, **Einstellungen**  \>  **System**-  \>  **apps & Funktionen**\).</span><span class="sxs-lookup"><span data-stu-id="54ad2-148">Used in the Windows UI \(**App List**, **Settings** \> **System** \> **Apps & features**\).</span></span> |  
| <span data-ttu-id="54ad2-149">50px</span><span class="sxs-lookup"><span data-stu-id="54ad2-149">50px</span></span> | <span data-ttu-id="54ad2-150">Verpackungsanforderung \(nirgendwo sichtbar \).</span><span class="sxs-lookup"><span data-stu-id="54ad2-150">Packaging requirement \(not visible anywhere\).</span></span> |  
| <span data-ttu-id="54ad2-151">150px</span><span class="sxs-lookup"><span data-stu-id="54ad2-151">150px</span></span> | <span data-ttu-id="54ad2-152">Wird als Symbol für den Microsoft Store verwendet.</span><span class="sxs-lookup"><span data-stu-id="54ad2-152">Used as the icon for the Microsoft Store.</span></span> |  


<span data-ttu-id="54ad2-153">Sehen Sie sich entweder den Leitfaden für [Manuelle Verpackungen][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] oder das [ManifoldJS-verpackungshandbuch][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] an, um festzustellen, wo diese Symbole plaziert sind.</span><span class="sxs-lookup"><span data-stu-id="54ad2-153">See either the [manual packaging guide][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] or the [ManifoldJS packaging guide][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] to determine where these icons is placed.</span></span>  <span data-ttu-id="54ad2-154">Dies hängt davon ab, welche Verpackungsmethode Sie auswählen.</span><span class="sxs-lookup"><span data-stu-id="54ad2-154">This depends upon which packaging method you choose.</span></span>  

#### <span data-ttu-id="54ad2-155">Symbol für Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="54ad2-155">Microsoft Store icon</span></span>  

<span data-ttu-id="54ad2-156">Wenn das 150px-Symbol für den Microsoft Store über einen transparenten Hintergrund verfügt, wird die Akzentfarbe des Geräts des Benutzers als Hintergrundfarbe des Symbols angezeigt.</span><span class="sxs-lookup"><span data-stu-id="54ad2-156">If the 150px icon for the Microsoft Store has a transparent background, the accent color of the user's device appears as the background color of the icon.</span></span>  

<span data-ttu-id="54ad2-157">Wenn ein Benutzer beispielsweise Rosa als Akzentfarbe ausgewählt hat, wird der transparente Hintergrund des Store-Symbols als Rosa angezeigt.</span><span class="sxs-lookup"><span data-stu-id="54ad2-157">For example, if a user has selected pink as the accent color, the transparent background of your store icon is displayed as pink.</span></span>  

:::row:::
   :::column span="1":::
       :::image type="complex" source="../media/windows-accent-color.png" alt-text="Windows-Akzentfarbe":::
          <span data-ttu-id="54ad2-159">Windows-Akzentfarbe</span><span class="sxs-lookup"><span data-stu-id="54ad2-159">Windows accent color</span></span> :::image-end:::
       
       <!--![Windows accent color][ImageWindowsAccentColor]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/store-icon-with-transparent-background.png" alt-text="Automatisch ausgewählte Hintergrundfarbe":::
         <span data-ttu-id="54ad2-161">Automatisch ausgewählte Hintergrundfarbe</span><span class="sxs-lookup"><span data-stu-id="54ad2-161">Background color auto selected</span></span> :::image-end:::
      
      <!--![Background color auto selected][ImageStoreIconTransparencyBackground]  -->  
   :::column-end:::
:::row-end:::

<span data-ttu-id="54ad2-162">Wenn Sie Ihre eigene Hintergrundfarbe für Ihren Microsoft Store aussuchen möchten, müssen Sie den Hintergrund undurchsichtig machen.</span><span class="sxs-lookup"><span data-stu-id="54ad2-162">If you want to pick your own background color for your Microsoft Store, you must make the background opaque.</span></span>  

> [!NOTE]
> <span data-ttu-id="54ad2-163">Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion.</span><span class="sxs-lookup"><span data-stu-id="54ad2-163">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="54ad2-164">[Kontaktieren Sie uns][AkaExtensionRequest] mit Ihren Anforderungen für den Microsoft Store, und Ihre Anfrage wird für ein zukünftiges Update in Betracht gezogen.</span><span class="sxs-lookup"><span data-stu-id="54ad2-164">[Contact us][AkaExtensionRequest] with your requests for the Microsoft Store, and your request is considered for a future update.</span></span>  

<!-- image links -->  

<!--[ImageActionmenuBrowseraction]: ../media/actionmenu-browseraction.png "browser action in action menu"  -->  
<!--[ImageBrowserActionIcon]: ../media/browseractionicon.png "browser action"  -->  
<!--[ImagePageaction]: ../media/pageaction.png "page action"  -->  
<!--[ImageManagementUi]: ../media/management-ui.png "management UI"  -->  
<!--[ImageWindowsAccentColor]: ../media/windows-accent-color.png "Windows accent color"  -->  
<!--[ImageStoreIconTransparencyBackground]: ../media/store-icon-with-transparent-background.png "Background color auto selected"  -->  

<!-- links -->  

[ExtensionsGuidesAccessibility]: ./accessibility.md "Barrierefreiheit | Microsoft docs"  
[ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder]: ./packaging/creating-and-testing-extension-packages.md#assets-folder "Ordner "Objekte" – erstellen und Testen eines Microsoft Edge Extension AppX-Pakets | Microsoft docs"  
[ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs]: ./packaging/using-manifoldjs-to-package-extensions.md#packaging-with-manifoldjs "Verpacken mit ManifoldJS – Verwenden von ManifoldJS zum Erstellen von Erweiterungs AppX-Paketen | Microsoft docs"  

[ExtensionsApisupportManifestkeys]: ../API-support/supported-manifest-keys.md "Unterstützte manifestschlüssel | Microsoft docs"  

[AkaExtensionRequest]: https://aka.ms/extension-request "Erreichen Sie uns"  

[MSDApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "BrowserControl. SetIcon ()-API | MDN"  
[MDNApiPageactionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/pageAction/setIcon "pagestyle. SetIcon ()-API | MDN"  
[MDNApiPageactionShow]: https://developer.mozilla.org/Add-ons/WebExtensions/API/pageAction/show "pagestyle. Show ()-API | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/browser_action "browser_action-manifest.js| MDN"  
[MDNManifestjsonPageAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action "page_action-manifest.js| MDN"  
