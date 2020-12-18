---
description: Anzeigen und Bearbeiten von localStorage mit dem lokalen Speicherbereich und der Konsole
title: Anzeigen und Bearbeiten des lokalen Speichers mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: c68f11b8ba2c10a0792f10acf5c5ededf2ad8e8d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231188"
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

# Anzeigen und Bearbeiten des lokalen Speichers mit Microsoft Edge devtools  

In diesem Leitfaden wird gezeigt, wie Sie [localStorage][MDNWindowsLocalStorage] -Schlüssel-Wert-Paare mithilfe von [Microsoft Edge devtools][MicrosoftEdgeDevTools] anzeigen, bearbeiten und löschen.  

## Anzeigen von localStorage-Schlüsseln und-Werten  

1.  Wählen Sie die Registerkarte **Anwendung** aus, um das **Anwendungs** Tool zu öffnen.  Standardmäßig wird der Bereich **Manifest** angezeigt.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest.msft.png":::
       Bereich ' **Manifest** '  
    :::image-end:::  
    
1.  Erweitern Sie das Menü **lokaler Speicher** .  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Das Menü "lokaler Speicher"" lightbox="../media/storage-application-local-storage.msft.png":::
       Das Menü " **lokaler Speicher** "  
    :::image-end:::  
    
1.  Wählen Sie eine Domäne aus, um die Schlüssel-Wert-Paare anzuzeigen.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Die localStorage-Schlüssel-Wert-Paare für die https://www.bing.com Domäne" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       Die `localStorage` Schlüssel-Wert-Paare für die `https://www.bing.com` Domäne  
    :::image-end:::  
    
1.  Wählen Sie eine Zeile der Tabelle aus, um den Wert im Viewer unter der Tabelle anzuzeigen.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Anzeigen des Werts des eventLogQueue_Online Schlüssels" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       Anzeigen des Werts des `eventLogQueue_Online` Schlüssels  
    :::image-end:::  
    
## Erstellen eines neuen localStorage-Schlüssel-Wert-Paars  

1.  [Anzeigen der localStorage-Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)  
1.  Doppelklicken Sie auf den leeren Teil der Tabelle.  DevTools erstellt eine neue Zeile und fokussiert den Cursor in der **Schlüssel** Spalte.  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Der leere Teil der Tabelle zum doppelklicken, um ein neues Schlüssel-Wert-Paar zu erstellen" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       Der leere Teil der Tabelle zum doppelklicken, um ein neues Schlüssel-Wert-Paar zu erstellen  
    :::image-end:::  
    
## Bearbeiten von localStorage-Schlüsseln oder-Werten  

1.  [Anzeigen der localStorage-Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)  
1.  Doppelklicken Sie auf eine Zelle in der Spalte **Schlüssel** oder **Wert** , um diesen Schlüssel oder Wert zu bearbeiten.  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Bearbeiten eines localStorage-Schlüssels" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       Bearbeiten eines `localStorage` Schlüssels  
    :::image-end:::  
    
## Löschen von localStorage-Schlüssel-Wert-Paaren  

1.  [Anzeigen der `localStorage` Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)  
1.  Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.  DevTools hebt das Blau hervor, um anzugeben, dass es markiert ist.  
1.  Wählen Sie den `Delete` Schlüssel aus, oder wählen Sie **Ausgewählte löschen** ( ![ Ausgewählte löschen ][ImageDeleteIcon] \) aus.  
    
## Löschen aller `localStorage` Schlüssel-Wert-Paare für eine Domäne  

1.  [Anzeigen der `localStorage` Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)  
1.  Wählen Sie **Alle löschen** \ ( ![ Alle löschen ][ImageClearIcon] \) aus.  
    
## Interagieren mit localStorage über die Konsole  

Da sie JavaScript in der **Konsole**ausführen können und die **Konsole** Zugriff auf die JavaScript-Kontexte der Seite hat, ist es möglich, mit `localStorage` der **Konsole**zu interagieren.  

1.  Verwenden Sie das **JavaScript** -Kontextmenü, um den JavaScript-Kontext der **Konsole** zu ändern, wenn Sie auf die `localStorage` Schlüssel-Wert-Paare einer anderen Domäne als auf die angezeigte Seite zugreifen möchten.  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Ändern des JavaScript-Kontexts der Konsole" lightbox="../media/storage-console-local-storage.msft.png":::
       Ändern des JavaScript-Kontexts der Konsole  
    :::image-end:::  
    
1.  Führen Sie Ihre `localStorage` Ausdrücke in der Konsole wie in Ihrem JavaScript aus.  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Interagieren mit localStorage über die Konsole" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       Interagieren mit `localStorage` der **Konsole**  
    :::image-end:::  
    
## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
