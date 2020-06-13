---
title: Anzeigen, bearbeiten und Löschen von Cookies mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: ecd8df7058bca4535d1f7da15ce1d500ef85aefe
ms.sourcegitcommit: a34858dd3260967ba9699842fa839c7a94775fe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/12/2020
ms.locfileid: "10710371"
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

# Anzeigen, bearbeiten und Löschen von Cookies mit Microsoft Edge devtools  

[Http-Cookies][MDNHTTPCookies] werden hauptsächlich verwendet, um Benutzersitzungen zu verwalten, Benutzer Personalisierungseinstellungen zu speichern und das Benutzerverhalten nachvollziehen zu können.  Cookies sind auch die Ursache für alle ärgerlichen Einwilligungsformulare "Diese Seite verwendet Cookies", die Sie im gesamten Web sehen.  Im folgenden Leitfaden erfahren Sie, wie Sie die HTTP-Cookies für eine Seite mit [Microsoft Edge devtools][MicrosoftEdgeDevTools]anzeigen, bearbeiten und löschen.  

## Öffnen des Bereichs "Cookies"  

1.  [Öffnen Sie devtools][DevToolsOpen].  
1.  Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.  Der Bereich **Manifest** sollte geöffnet sein.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Abbildung 1: der Bereich "Manifest"  
    :::image-end:::  

1.  Erweitern Sie unter **Speicher** den Eintrag **Cookies**, und wählen Sie dann einen Ursprung aus.  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="Der Bereich "Cookies"" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       Abbildung 2: der Bereich "Cookies"  
    :::image-end:::  

## Felder  

Die Tabelle " **Cookies** " enthält die folgenden Felder.  

*   **Name**  Der Name des Cookies.  
*   **Value**aus.  Der Wert des Cookies.  
*   **Domäne**aus.  Die Hosts, die das Cookie empfangen dürfen.  Siehe [Bereich der Cookies][MDNHTTPCookiesScope].  
*   **Path**aus.  Die URL, die in der angeforderten URL vorhanden sein muss, um die Kopfzeile zu senden `Cookie` .  Siehe [Bereich der Cookies][MDNHTTPCookiesScope].  
*   **Läuft ab/max-Alter**.  Das Ablaufdatum oder das maximale Alter des Cookies.  Weitere Informationen finden Sie unter [permanente Cookies][MDNHTTPCookiesPermanent].  Für [Sitzungscookies][MDNHTTPCookiesSession] ist dieser Wert immer `Session` .  
*   **Größe**aus.  Die Größe des Cookies in Bytes.  
*   **Http**.  Ist "true", gibt dieses Feld an, dass das Cookie nur über HTTP verwendet und JavaScript-Änderungen nicht zulässig sind.  Siehe [HttpOnly-Cookies][MDNHTTPCookiesSecure].  
*   **Sicher**.  Ist "true", gibt dieses Feld an, dass das Cookie nur über eine sichere HTTPS-Verbindung an den Server gesendet werden muss.  Siehe [sichere Cookies][MDNHTTPCookiesSecure].  
*   **SameSite**.  Enthält `strict` oder `lax` Wenn das Cookie das experimentelle [SameSite][MDNHTTPCookiesSamesite] -Attribut verwendet.  
*   **Priorität**.  Contains `low` , `medium` \ (Standard \) oder `high` Wenn das Cookie das veraltete [Cookie Priority][ChromiumIssue232693] -Attribut verwendet.

## Filtern von Cookies  

Verwenden Sie das Textfeld " **Filter** ", um Cookies nach **Name** oder **Wert**zu filtern.  Das Filtern nach anderen Feldern wird nicht unterstützt.  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Filtern von Cookies, die nicht die Text-ID enthalten" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   Abbildung 3: Filtern von Cookies, die keinen Text enthalten `ID`  
:::image-end:::  

## Bearbeiten eines Cookies  

Die Felder **Name**, **value**, **Domain**, **path**und **Expires/max-age** können bearbeitet werden.  
Doppelklicken Sie auf ein Feld, um es zu bearbeiten.  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Festlegen des Namens eines Cookies auf DEVTOOLS!" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   Abbildung 4: Festlegen des Namens eines Cookies auf `DEVTOOLS!`  
:::image-end:::  

## Löschen von Cookies  

Wählen Sie ein Cookie aus, **und wählen Sie ausgewählte** löschen ausgewählt löschen aus ![ ][ImageDeleteIcon] , um das bestimmte Cookie zu löschen.  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Löschen eines bestimmten Cookies" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   Abbildung 5: Löschen eines bestimmten Cookies  
:::image-end:::  

Wählen **Sie alle löschen** ![ aus ][ImageClearIcon] , um alle Cookies zu löschen.  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Löschen aller Cookies" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   Abbildung 6: Löschen aller Cookies  
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
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
