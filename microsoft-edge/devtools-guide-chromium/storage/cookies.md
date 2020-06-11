---
title: Anzeigen, bearbeiten und Löschen von Cookies mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 4bfd99a36a6a3f8fdf8dbd7787bd54cde87d79da
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "10708939"
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

# <span data-ttu-id="53d68-103">Anzeigen, bearbeiten und Löschen von Cookies mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="53d68-103">View, edit, and delete cookies with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="53d68-104">[Http-Cookies][MDNHTTPCookies] werden hauptsächlich verwendet, um Benutzersitzungen zu verwalten, Benutzer Personalisierungseinstellungen zu speichern und das Benutzerverhalten nachvollziehen zu können.</span><span class="sxs-lookup"><span data-stu-id="53d68-104">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="53d68-105">Cookies sind auch die Ursache für alle ärgerlichen Einwilligungsformulare "Diese Seite verwendet Cookies", die Sie im gesamten Web sehen.</span><span class="sxs-lookup"><span data-stu-id="53d68-105">Cookies are also the cause of all of the annoying "this page uses cookies" consent forms that you see across the web.</span></span>  <span data-ttu-id="53d68-106">Im folgenden Leitfaden erfahren Sie, wie Sie die HTTP-Cookies für eine Seite mit [Microsoft Edge devtools][MicrosoftEdgeDevTools]anzeigen, bearbeiten und löschen.</span><span class="sxs-lookup"><span data-stu-id="53d68-106">The following guide teaches you how to view, edit, and delete the HTTP cookies for a page with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="53d68-107">Öffnen des Bereichs "Cookies"</span><span class="sxs-lookup"><span data-stu-id="53d68-107">Open the Cookies pane</span></span>  

1.  <span data-ttu-id="53d68-108">[Öffnen Sie devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="53d68-108">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="53d68-109">Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="53d68-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="53d68-110">Der Bereich **Manifest** sollte geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="53d68-110">The **Manifest** pane should open.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="53d68-112">Abbildung 1: der Bereich "Manifest"</span><span class="sxs-lookup"><span data-stu-id="53d68-112">Figure 1:  The Manifest pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="53d68-113">Erweitern Sie unter **Speicher** den Eintrag **Cookies**, und wählen Sie dann einen Ursprung aus.</span><span class="sxs-lookup"><span data-stu-id="53d68-113">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="Der Bereich "Cookies"" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       <span data-ttu-id="53d68-115">Abbildung 2: der Bereich "Cookies"</span><span class="sxs-lookup"><span data-stu-id="53d68-115">Figure 2:  The Cookies pane</span></span>  
    :::image-end:::  

## <span data-ttu-id="53d68-116">Felder</span><span class="sxs-lookup"><span data-stu-id="53d68-116">Fields</span></span>  

<span data-ttu-id="53d68-117">Die Tabelle " **Cookies** " enthält die folgenden Felder.</span><span class="sxs-lookup"><span data-stu-id="53d68-117">The **Cookies** table contains the following fields.</span></span>  

*   <span data-ttu-id="53d68-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="53d68-118">**Name**.</span></span>  <span data-ttu-id="53d68-119">Der Name des Cookies.</span><span class="sxs-lookup"><span data-stu-id="53d68-119">The name of the cookie.</span></span>  
*   <span data-ttu-id="53d68-120">**Value**aus.</span><span class="sxs-lookup"><span data-stu-id="53d68-120">**Value**.</span></span>  <span data-ttu-id="53d68-121">Der Wert des Cookies.</span><span class="sxs-lookup"><span data-stu-id="53d68-121">The value of the cookie.</span></span>  
*   <span data-ttu-id="53d68-122">**Domäne**aus.</span><span class="sxs-lookup"><span data-stu-id="53d68-122">**Domain**.</span></span>  <span data-ttu-id="53d68-123">Die Hosts, die das Cookie empfangen dürfen.</span><span class="sxs-lookup"><span data-stu-id="53d68-123">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="53d68-124">Siehe [Bereich der Cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="53d68-124">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="53d68-125">**Path**aus.</span><span class="sxs-lookup"><span data-stu-id="53d68-125">**Path**.</span></span>  <span data-ttu-id="53d68-126">Die URL, die in der angeforderten URL vorhanden sein muss, um die Kopfzeile zu senden `Cookie` .</span><span class="sxs-lookup"><span data-stu-id="53d68-126">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="53d68-127">Siehe [Bereich der Cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="53d68-127">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="53d68-128">**Läuft ab/max-Alter**.</span><span class="sxs-lookup"><span data-stu-id="53d68-128">**Expires / Max-Age**.</span></span>  <span data-ttu-id="53d68-129">Das Ablaufdatum oder das maximale Alter des Cookies.</span><span class="sxs-lookup"><span data-stu-id="53d68-129">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="53d68-130">Weitere Informationen finden Sie unter [permanente Cookies][MDNHTTPCookiesPermanent].</span><span class="sxs-lookup"><span data-stu-id="53d68-130">See [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="53d68-131">Für [Sitzungscookies][MDNHTTPCookiesSession] ist dieser Wert immer `Session` .</span><span class="sxs-lookup"><span data-stu-id="53d68-131">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="53d68-132">**Größe**aus.</span><span class="sxs-lookup"><span data-stu-id="53d68-132">**Size**.</span></span>  <span data-ttu-id="53d68-133">Die Größe des Cookies in Bytes.</span><span class="sxs-lookup"><span data-stu-id="53d68-133">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="53d68-134">**Http**.</span><span class="sxs-lookup"><span data-stu-id="53d68-134">**HTTP**.</span></span>  <span data-ttu-id="53d68-135">Ist "true", gibt dieses Feld an, dass das Cookie nur über HTTP verwendet und JavaScript-Änderungen nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="53d68-135">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="53d68-136">Siehe [HttpOnly-Cookies][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="53d68-136">See [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="53d68-137">**Sicher**.</span><span class="sxs-lookup"><span data-stu-id="53d68-137">**Secure**.</span></span>  <span data-ttu-id="53d68-138">Ist "true", gibt dieses Feld an, dass das Cookie nur über eine sichere HTTPS-Verbindung an den Server gesendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="53d68-138">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="53d68-139">Siehe [sichere Cookies][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="53d68-139">See [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="53d68-140">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="53d68-140">**SameSite**.</span></span>  <span data-ttu-id="53d68-141">Enthält `strict` oder `lax` Wenn das Cookie das experimentelle [SameSite][MDNHTTPCookiesSamesite] -Attribut verwendet.</span><span class="sxs-lookup"><span data-stu-id="53d68-141">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  
*   <span data-ttu-id="53d68-142">**Priorität**.</span><span class="sxs-lookup"><span data-stu-id="53d68-142">**Priority**.</span></span>  <span data-ttu-id="53d68-143">Contains `low` , `medium` \ (Standard \) oder `high` Wenn das Cookie das Attribut "abgewertete [Cookies][ChromiumIssue232693] " verwendet.</span><span class="sxs-lookup"><span data-stu-id="53d68-143">Contains `low`, `medium` \(default\), or `high` if the cookie is using the depreciated [cookie Priority][ChromiumIssue232693] attribute.</span></span>

## <span data-ttu-id="53d68-144">Filtern von Cookies</span><span class="sxs-lookup"><span data-stu-id="53d68-144">Filter cookies</span></span>  

<span data-ttu-id="53d68-145">Verwenden Sie das Textfeld " **Filter** ", um Cookies nach **Name** oder **Wert**zu filtern.</span><span class="sxs-lookup"><span data-stu-id="53d68-145">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="53d68-146">Das Filtern nach anderen Feldern wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="53d68-146">Filtering by other fields is not supported.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Filtern von Cookies, die nicht die Text-ID enthalten" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   <span data-ttu-id="53d68-148">Abbildung 3: Filtern von Cookies, die keinen Text enthalten</span><span class="sxs-lookup"><span data-stu-id="53d68-148">Figure 3:  Filtering out any cookies that do not contain the text</span></span> `ID`  
:::image-end:::  

## <span data-ttu-id="53d68-149">Bearbeiten eines Cookies</span><span class="sxs-lookup"><span data-stu-id="53d68-149">Edit a cookie</span></span>  

<span data-ttu-id="53d68-150">Die Felder **Name**, **value**, **Domain**, **path**und **Expires/max-age** können bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="53d68-150">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="53d68-151">Doppelklicken Sie auf ein Feld, um es zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="53d68-151">Double-click a field to edit it.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Festlegen des Namens eines Cookies auf DEVTOOLS!" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   <span data-ttu-id="53d68-153">Abbildung 4: Festlegen des Namens eines Cookies auf</span><span class="sxs-lookup"><span data-stu-id="53d68-153">Figure 4:  Setting the name of a cookie to</span></span> `DEVTOOLS!`  
:::image-end:::  

## <span data-ttu-id="53d68-154">Löschen von Cookies</span><span class="sxs-lookup"><span data-stu-id="53d68-154">Delete cookies</span></span>  

<span data-ttu-id="53d68-155">Wählen Sie ein Cookie aus, **und wählen Sie ausgewählte** löschen ausgewählt löschen aus ![ ][ImageDeleteIcon] , um das bestimmte Cookie zu löschen.</span><span class="sxs-lookup"><span data-stu-id="53d68-155">Select a cookie and select **Delete Selected** ![Delete Selected][ImageDeleteIcon]  to delete the specific cookie.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Löschen eines bestimmten Cookies" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   <span data-ttu-id="53d68-157">Abbildung 5: Löschen eines bestimmten Cookies</span><span class="sxs-lookup"><span data-stu-id="53d68-157">Figure 5:  Deleting a specific cookie</span></span>  
:::image-end:::  

<span data-ttu-id="53d68-158">Wählen **Sie alle löschen** ![ aus ][ImageClearIcon] , um alle Cookies zu löschen.</span><span class="sxs-lookup"><span data-stu-id="53d68-158">Select **Clear All** ![Clear All][ImageClearIcon]  to delete all cookies.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Löschen aller Cookies" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   <span data-ttu-id="53d68-160">Abbildung 6: Löschen aller Cookies</span><span class="sxs-lookup"><span data-stu-id="53d68-160">Figure 6:  Clearing all cookies</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Öffnen von Microsoft Edge devtools"  

[ChromiumIssue232693]: https://bugs.chromium.org/p/chromium/issues/detail?id=232693 "Chrom Problem 232693: Implementieren des Prioritäts Felds für Cookies | Chrom Fehler"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "HTTP-Cookies | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "HTTP-Cookies – permanente Cookies | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "HTTP-Cookies-SameSite Cookies | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "HTTP-Cookies – Bereich von Cookies | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "HTTP-Cookies – sichere und HttpOnly Cookies | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "HTTP-Cookies – Sitzungscookies | MDN"  

> [!NOTE]
> <span data-ttu-id="53d68-170">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53d68-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="53d68-171">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="53d68-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="53d68-173">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="53d68-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
