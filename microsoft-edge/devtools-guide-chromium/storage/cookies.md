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





# Anzeigen, bearbeiten und Löschen von Cookies mit Microsoft Edge devtools   

  

[Http-Cookies][MDNHTTPCookies] werden hauptsächlich verwendet, um Benutzersitzungen zu verwalten, Benutzer Personalisierungseinstellungen zu speichern und das Benutzerverhalten nachvollziehen zu können.  Sie sind auch die Ursache für alle diese lästigen Einwilligungsformulare "Diese Seite verwendet Cookies", die Sie im gesamten Web sehen.  In diesem Leitfaden lernen Sie, wie Sie die HTTP-Cookies für eine Seite mit [Microsoft Edge devtools][MicrosoftEdgeDevTools]anzeigen, bearbeiten und löschen.  

## Öffnen des Bereichs "Cookies"   

1.  [Öffnen Sie devtools][DevToolsOpen].  
1.  Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.  Der Bereich **Manifest** sollte geöffnet sein.  
    
    > ##### Abbildung1  
    > Bereich ' Manifest '  
    > ![Bereich ' Manifest '][ImageManifest]  

1.  Erweitern Sie unter **Speicher** den Eintrag **Cookies**, und wählen Sie dann einen Ursprung aus.  
    
    > ##### Abbildung2  
    > Der Bereich "Cookies"  
    > ![Der Bereich "Cookies"][ImageCookies]  

## Felder   

Die Tabelle **Cookies** enthält die folgenden Felder:  

*   **Name**  Der Name des Cookies.  
*   **Value**aus.  Der Wert des Cookies.  
*   **Domäne**aus.  Die Hosts, die das Cookie empfangen dürfen.  Siehe [Bereich der Cookies][MDNHTTPCookiesScope].  
*   **Path**aus.  Die URL, die in der angeforderten URL vorhanden sein muss, um die Kopfzeile zu senden `Cookie` .  Siehe [Bereich der Cookies][MDNHTTPCookiesScope].  
*   **Läuft ab/max-Alter**.  Das Ablaufdatum oder das maximale Alter des Cookies.  Weitere Informationen finden Sie unter [permanente Cookies][MDNHTTPCookiesPermanent].  Für [Sitzungscookies][MDNHTTPCookiesSession] ist dieser Wert immer `Session` .  
*   **Größe**aus.  Die Größe des Cookies in Bytes.  
*   **Http**.  Ist "true", gibt dieses Feld an, dass das Cookie nur über HTTP verwendet und JavaScript-Änderungen nicht zulässig sind.  Siehe [HttpOnly-Cookies][MDNHTTPCookiesSecure].  
*   **Sicher**.  Ist "true", gibt dieses Feld an, dass das Cookie nur über eine sichere HTTPS-Verbindung an den Server gesendet werden muss.  Siehe [sichere Cookies][MDNHTTPCookiesSecure].  
*   **SameSite**.  Enthält `strict` oder `lax` Wenn das Cookie das experimentelle [SameSite][MDNHTTPCookiesSamesite] -Attribut verwendet.  

## Filtern von Cookies   

Verwenden Sie das Textfeld " **Filter** ", um Cookies nach **Name** oder **Wert**zu filtern.  Das Filtern nach anderen Feldern wird nicht unterstützt.  

> ##### Abbildung 3  
> Filtern von Cookies, die keinen Text enthalten `ID`  
> ![Filtern von Cookies, die nicht die Text-ID enthalten][ImageCookiesFilter]  

## Bearbeiten eines Cookies   

Die Felder **Name**, **value**, **Domain**, **path**und **Expires/max-age** können bearbeitet werden.  
Doppelklicken Sie auf ein Feld, um es zu bearbeiten.  

> ##### Abbildung4  
> Festlegen des Namens eines Cookies auf `DEVTOOLS!`  
> ![Festlegen des Namens eines Cookies auf DEVTOOLS!][ImageEditCookie]  

## Löschen von Cookies   

Wählen Sie ein Cookie aus, und klicken Sie dann auf **ausgewählte** ![ Löschen ausgewählt löschen ][ImageDeleteIcon] , um das eine Cookie zu löschen.  

> ##### Abbildung5  
> Löschen eines bestimmten Cookies  
> ![Löschen eines bestimmten Cookies][ImageDeleteCookie]  

Wählen **Sie alle löschen** ![ aus ][ImageClearIcon] , um alle Cookies zu löschen.  

> ##### Abbildung6  
> Löschen aller Cookies  
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
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
