---
title: Anzeigen, bearbeiten und Löschen von Cookies mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 084c4116cd4c9c5e70b2fe341257fa68ba2c8ae7
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612068"
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





# <span data-ttu-id="cbd4c-103">Anzeigen, bearbeiten und Löschen von Cookies mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="cbd4c-103">View, Edit, And Delete Cookies With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="cbd4c-104">[Http-Cookies][MDNHTTPCookies] werden hauptsächlich verwendet, um Benutzersitzungen zu verwalten, Benutzer Personalisierungseinstellungen zu speichern und das Benutzerverhalten nachvollziehen zu können.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-104">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="cbd4c-105">Sie sind auch die Ursache für alle diese lästigen Einwilligungsformulare "Diese Seite verwendet Cookies", die Sie im gesamten Web sehen.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-105">They are also the cause of all of those annoying "this page uses cookies" consent forms that you see across the web.</span></span>  <span data-ttu-id="cbd4c-106">In diesem Leitfaden lernen Sie, wie Sie die HTTP-Cookies für eine Seite mit [Microsoft Edge devtools][MicrosoftEdgeDevTools]anzeigen, bearbeiten und löschen.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-106">This guide teaches you how to view, edit, and delete the HTTP cookies for a page with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="cbd4c-107">Öffnen des Bereichs "Cookies"</span><span class="sxs-lookup"><span data-stu-id="cbd4c-107">Open the Cookies pane</span></span>   

1.  <span data-ttu-id="cbd4c-108">[Öffnen Sie devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="cbd4c-108">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="cbd4c-109">Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="cbd4c-110">Der Bereich **Manifest** sollte geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-110">The **Manifest** pane should open.</span></span>  
    
    > ##### <span data-ttu-id="cbd4c-111">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="cbd4c-111">Figure 1</span></span>  
    > <span data-ttu-id="cbd4c-112">Bereich ' Manifest '</span><span class="sxs-lookup"><span data-stu-id="cbd4c-112">The Manifest pane</span></span>  
    > ![Bereich ' Manifest '][ImageManifest]  

1.  <span data-ttu-id="cbd4c-114">Erweitern Sie unter **Speicher** den Eintrag **Cookies**, und wählen Sie dann einen Ursprung aus.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-114">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    > ##### <span data-ttu-id="cbd4c-115">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="cbd4c-115">Figure 2</span></span>  
    > <span data-ttu-id="cbd4c-116">Der Bereich "Cookies"</span><span class="sxs-lookup"><span data-stu-id="cbd4c-116">The Cookies pane</span></span>  
    > ![Der Bereich "Cookies"][ImageCookies]  

## <span data-ttu-id="cbd4c-118">Felder</span><span class="sxs-lookup"><span data-stu-id="cbd4c-118">Fields</span></span>   

<span data-ttu-id="cbd4c-119">Die Tabelle **Cookies** enthält die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="cbd4c-119">The **Cookies** table contains the following fields:</span></span>  

*   <span data-ttu-id="cbd4c-120">**Name**</span><span class="sxs-lookup"><span data-stu-id="cbd4c-120">**Name**.</span></span>  <span data-ttu-id="cbd4c-121">Der Name des Cookies.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-121">The name of the cookie.</span></span>  
*   <span data-ttu-id="cbd4c-122">**Value**aus.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-122">**Value**.</span></span>  <span data-ttu-id="cbd4c-123">Der Wert des Cookies.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-123">The value of the cookie.</span></span>  
*   <span data-ttu-id="cbd4c-124">**Domäne**aus.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-124">**Domain**.</span></span>  <span data-ttu-id="cbd4c-125">Die Hosts, die das Cookie empfangen dürfen.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-125">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="cbd4c-126">Siehe [Bereich der Cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="cbd4c-126">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="cbd4c-127">**Path**aus.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-127">**Path**.</span></span>  <span data-ttu-id="cbd4c-128">Die URL, die in der angeforderten URL vorhanden sein muss, um die Kopfzeile zu senden `Cookie` .</span><span class="sxs-lookup"><span data-stu-id="cbd4c-128">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="cbd4c-129">Siehe [Bereich der Cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="cbd4c-129">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="cbd4c-130">**Läuft ab/max-Alter**.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-130">**Expires / Max-Age**.</span></span>  <span data-ttu-id="cbd4c-131">Das Ablaufdatum oder das maximale Alter des Cookies.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-131">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="cbd4c-132">Weitere Informationen finden Sie unter [permanente Cookies][MDNHTTPCookiesPermanent].</span><span class="sxs-lookup"><span data-stu-id="cbd4c-132">See [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="cbd4c-133">Für [Sitzungscookies][MDNHTTPCookiesSession] ist dieser Wert immer `Session` .</span><span class="sxs-lookup"><span data-stu-id="cbd4c-133">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="cbd4c-134">**Größe**aus.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-134">**Size**.</span></span>  <span data-ttu-id="cbd4c-135">Die Größe des Cookies in Bytes.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-135">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="cbd4c-136">**Http**.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-136">**HTTP**.</span></span>  <span data-ttu-id="cbd4c-137">Ist "true", gibt dieses Feld an, dass das Cookie nur über HTTP verwendet und JavaScript-Änderungen nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-137">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="cbd4c-138">Siehe [HttpOnly-Cookies][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="cbd4c-138">See [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="cbd4c-139">**Sicher**.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-139">**Secure**.</span></span>  <span data-ttu-id="cbd4c-140">Ist "true", gibt dieses Feld an, dass das Cookie nur über eine sichere HTTPS-Verbindung an den Server gesendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-140">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="cbd4c-141">Siehe [sichere Cookies][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="cbd4c-141">See [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="cbd4c-142">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-142">**SameSite**.</span></span>  <span data-ttu-id="cbd4c-143">Enthält `strict` oder `lax` Wenn das Cookie das experimentelle [SameSite][MDNHTTPCookiesSamesite] -Attribut verwendet.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-143">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  

## <span data-ttu-id="cbd4c-144">Filtern von Cookies</span><span class="sxs-lookup"><span data-stu-id="cbd4c-144">Filter cookies</span></span>   

<span data-ttu-id="cbd4c-145">Verwenden Sie das Textfeld " **Filter** ", um Cookies nach **Name** oder **Wert**zu filtern.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-145">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="cbd4c-146">Das Filtern nach anderen Feldern wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-146">Filtering by other fields is not supported.</span></span>  

> ##### <span data-ttu-id="cbd4c-147">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="cbd4c-147">Figure 3</span></span>  
> <span data-ttu-id="cbd4c-148">Filtern von Cookies, die keinen Text enthalten</span><span class="sxs-lookup"><span data-stu-id="cbd4c-148">Filtering out any cookies that do not contain the text</span></span> `ID`  
> ![Filtern von Cookies, die nicht die Text-ID enthalten][ImageCookiesFilter]  

## <span data-ttu-id="cbd4c-150">Bearbeiten eines Cookies</span><span class="sxs-lookup"><span data-stu-id="cbd4c-150">Edit a cookie</span></span>   

<span data-ttu-id="cbd4c-151">Die Felder **Name**, **value**, **Domain**, **path**und **Expires/max-age** können bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-151">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="cbd4c-152">Doppelklicken Sie auf ein Feld, um es zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-152">Double-click a field to edit it.</span></span>  

> ##### <span data-ttu-id="cbd4c-153">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="cbd4c-153">Figure 4</span></span>  
> <span data-ttu-id="cbd4c-154">Festlegen des Namens eines Cookies auf</span><span class="sxs-lookup"><span data-stu-id="cbd4c-154">Setting the name of a cookie to</span></span> `DEVTOOLS!`  
> ![Festlegen des Namens eines Cookies auf DEVTOOLS!][ImageEditCookie]  

## <span data-ttu-id="cbd4c-156">Löschen von Cookies</span><span class="sxs-lookup"><span data-stu-id="cbd4c-156">Delete cookies</span></span>   

<span data-ttu-id="cbd4c-157">Wählen Sie ein Cookie aus, und klicken Sie dann auf **ausgewählte** ![ Löschen ausgewählt löschen ][ImageDeleteIcon] , um das eine Cookie zu löschen.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-157">Select a cookie and then click **Delete Selected** ![Delete Selected][ImageDeleteIcon]  to delete that one cookie.</span></span>  

> ##### <span data-ttu-id="cbd4c-158">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="cbd4c-158">Figure 5</span></span>  
> <span data-ttu-id="cbd4c-159">Löschen eines bestimmten Cookies</span><span class="sxs-lookup"><span data-stu-id="cbd4c-159">Deleting a specific cookie</span></span>  
> ![Löschen eines bestimmten Cookies][ImageDeleteCookie]  

<span data-ttu-id="cbd4c-161">Wählen **Sie alle löschen** ![ aus ][ImageClearIcon] , um alle Cookies zu löschen.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-161">Select **Clear All** ![Clear All][ImageClearIcon]  to delete all cookies.</span></span>  

> ##### <span data-ttu-id="cbd4c-162">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="cbd4c-162">Figure 6</span></span>  
> <span data-ttu-id="cbd4c-163">Löschen aller Cookies</span><span class="sxs-lookup"><span data-stu-id="cbd4c-163">Clearing all cookies</span></span>  
> ![Löschen aller Cookies][ImageClearAllCookies]  

<!--    -->  

  

<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest-empty.msft.png "Abbildung 1: der Bereich "Manifest""  
[ImageCookies]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-selected.msft.png "Abbildung 2: der Bereich "Cookies""  
[ImageCookiesFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-filter-id.msft.png "Abbildung 3: Filtern von Cookies, die nicht die Text-ID enthalten"  
[ImageEditCookie]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-rename.msft.png "Abbildung 4: Festlegen des Namens eines Cookies auf DEVTOOLS!"  
[ImageDeleteCookie]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-delete-selected.msft.png "Abbildung 5: Löschen eines bestimmten Cookies"  
[ImageClearAllCookies]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-clear-all.msft.png "Abbildung 6: Löschen aller Cookies"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Öffnen von Microsoft Edge devtools"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "HTTP-Cookies | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "HTTP-Cookies – permanente Cookies | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "HTTP-Cookies-SameSite Cookies | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "HTTP-Cookies – Bereich von Cookies | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "HTTP-Cookies – sichere und HttpOnly Cookies | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "HTTP-Cookies – Sitzungscookies | MDN"  

> [!NOTE]
> <span data-ttu-id="cbd4c-179">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-179">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cbd4c-180">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="cbd4c-180">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="cbd4c-182">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cbd4c-182">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
