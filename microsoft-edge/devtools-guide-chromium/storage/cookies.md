---
description: Erfahren Sie, wie Sie die HTTP-Cookies für eine Seite mithilfe von devTools Microsoft Edge anzeigen, bearbeiten und löschen.
title: Anzeigen, Bearbeiten und Löschen von Cookies mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: c208ca628fe91ed5922bc36566be2b9bdd20ec0b
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439682"
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

# <a name="view-edit-and-delete-cookies-with-microsoft-edge-devtools"></a>Anzeigen, Bearbeiten und Löschen von Cookies mit Microsoft Edge DevTools  

[HTTP-Cookies][MDNHTTPCookies] werden hauptsächlich verwendet, um Benutzersitzungen zu verwalten, Benutzerpersonalisierungseinstellungen zu speichern und das Benutzerverhalten nachverfolgt zu werden.  Cookies sind auch die Ursache für alle lästigen, die diese **Seite verwendet** Cookies Zustimmungsformulare, die im Web gefunden werden.  Im folgenden Handbuch erfahren Sie, wie Sie die HTTP-Cookies für eine Webseite mit devTools Microsoft Edge [anzeigen, bearbeiten und löschen.][MicrosoftEdgeDevTools]  

## <a name="open-the-cookies-pane"></a>Öffnen des Bereichs "Cookies"  

1.  [Öffnen Sie DevTools][DevToolsOpen].  
1.  Wählen Sie die **Registerkarte Anwendung** aus, um den Bereich **Anwendung zu** öffnen.  Der **Manifestbereich** sollte geöffnet werden.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Abbildung 1: Der Manifestbereich  
    :::image-end:::  

1.  Wählen **Storage** **sie Cookies**aus, und wählen Sie dann einen Ursprung aus.  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="Der Bereich Cookies" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       Abbildung 2: Der Bereich "Cookies"  
    :::image-end:::  

## <a name="fields"></a>Felder  

Die **Tabelle Cookies** enthält die folgenden Felder.  

*   **Name**  Der Name des Cookies.  
*   **Wert**.  Der Wert des Cookies.  
*   **Domäne**.  Die Hosts, die das Cookie empfangen dürfen.  Navigieren Sie zu [Bereich der Cookies][MDNHTTPCookiesScope].  
*   **Pfad**.  Die URL, die in der angeforderten URL vorhanden sein muss, um den Header zu `Cookie` senden.  Navigieren Sie zu [Bereich der Cookies][MDNHTTPCookiesScope].  
*   **Läuft ab / Max-Age**.  Das Ablaufdatum oder das maximale Alter des Cookies.  Navigieren Sie zu [Dauerhafte Cookies][MDNHTTPCookiesPermanent].  Für [Sitzungscookies][MDNHTTPCookiesSession] ist dieser Wert immer `Session` .  
*   **Größe**.  Die Größe des Cookies in Bytes.  
*   **HTTP**.  Wenn true, gibt dieses Feld an, dass das Cookie nur über HTTP verwendet werden soll, und die JavaScript-Änderung ist nicht zulässig.  Navigieren Sie zu [HttpOnly Cookies][MDNHTTPCookiesSecure].  
*   **Secure**.  Wenn true, gibt dieses Feld an, dass das Cookie nur über eine sichere HTTPS-Verbindung an den Server gesendet werden darf.  Navigieren Sie zu [Sichere Cookies][MDNHTTPCookiesSecure].  
*   **SameSite**.  Enthält `strict` oder wenn das Cookie das experimentelle `lax` [Samesite-Attribut][MDNHTTPCookiesSamesite] verwendet.  
*   **Priorität**.  Enthält `low` , \(default\), oder wenn das Cookie das veraltete `medium` Cookie `high` [Priority-Attribut][ChromiumIssue232693] verwendet.

## <a name="filter-cookies"></a>Filtern von Cookies  

Verwenden Sie das **Textfeld Filter,** um Cookies nach **Name oder Value** zu **filtern.**  Das Filtern nach anderen Feldern wird nicht unterstützt.  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Filtern von Cookies, die die Text-ID nicht enthalten" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   Abbildung 3: Filtern von Cookies, die den Text nicht enthalten `ID`  
:::image-end:::  

## <a name="edit-a-cookie"></a>Bearbeiten eines Cookies  

Die **Felder Name**, **Value**, **Domain**, **Path**und **Expires / Max-Age** können bearbeitet werden.  
Doppelklicken Sie auf ein Feld, um es zu bearbeiten.  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Festlegen des Namens eines Cookies auf DEVTOOLS!" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   Abbildung 4: Festlegen des Namens eines Cookies auf `DEVTOOLS!`  
:::image-end:::  

## <a name="delete-cookies"></a>Löschen von Cookies  

Wählen Sie ein Cookie aus, und wählen Sie **Ausgewähltes** Löschen \( Ausgewähltes Löschen \) aus, ![ um das spezifische Cookie zu ](../media/delete-icon.msft.png) löschen.  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Löschen eines bestimmten Cookies" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   Abbildung 5: Löschen eines bestimmten Cookies  
:::image-end:::  

Wählen **Sie Alle** löschen \( Alle löschen ![ ](../media/clear-icon.msft.png) \), um alle Cookies zu löschen.  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Löschen aller Cookies" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   Abbildung 6: Löschen aller Cookies  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chromium) Developer Tools"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Öffnen Microsoft Edge DevTools"  

[ChromiumIssue232693]: https://bugs.chromium.org/p/chromium/issues/detail?id=232693 "Chromium Problem 232693: Implementieren des Prioritätsfelds für Cookies | Chromium Bugs"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "HTTP-Cookies | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "HTTP-Cookies – permanente | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "HTTP-Cookies – SameSite-Cookies | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "HTTP-Cookies – Umfang der | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "HTTP-Cookies – Secure and HttpOnly cookies | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "HTTP-Cookies – Sitzungscookies | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
