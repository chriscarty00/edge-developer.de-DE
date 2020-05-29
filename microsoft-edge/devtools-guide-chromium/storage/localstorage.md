---
title: Anzeigen und Bearbeiten des lokalen Speichers mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: f7e187662aec8231f2cc4e99baab1b4b8e2048ad
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612011"
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



In diesem Leitfaden wird gezeigt, wie Sie mit [Microsoft Edge devtools][MicrosoftEdgeDevTools] [`localStorage`][MDNWindowsLocalStorage] Schlüssel-Wert-Paare anzeigen, bearbeiten und löschen können.  

## Anzeigen von localStorage-Schlüsseln und-Werten   

1.  Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.  Standardmäßig wird der Bereich **Manifest** angezeigt.  
    
    > ##### Abbildung1  
    > Bereich ' Manifest '  
    > ![Bereich ' Manifest '][ImageManifest]  

1.  Erweitern Sie das Menü **lokaler Speicher** .  
    
    > ##### Abbildung2  
    > Das Menü " **lokaler Speicher** " zeigt zwei Domänen an: `https://business.bing.com` und `https://www.bing.com`  
    > ![Das Menü "lokaler Speicher"][ImageLocalStorageMenu]  

1.  Wählen Sie eine Domäne aus, um die Schlüssel-Wert-Paare anzuzeigen.  
    
    > ##### Abbildung 3  
    > Die `localStorage` Schlüssel-Wert-Paare für die `https://www.bing.com` Domäne  
    > ![Die localStorage-Schlüssel-Wert-Paare für die https://www.bing.com Domäne][ImageLocalStorage]  

1.  Wählen Sie eine Zeile der Tabelle aus, um den Wert im Viewer unter der Tabelle anzuzeigen.  
    
    > ##### Abbildung4  
    > Anzeigen des Werts des `eventLogQueue_Online` Schlüssels  
    > ![Anzeigen des Werts des eventLogQueue_Online Schlüssels][ImageLocalStorageViewer]  

## Erstellen eines neuen `localStorage` Schlüssel-Wert-Paars   

1.  [Anzeigen der `localStorage` Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)  
1.  Doppelklicken Sie auf den leeren Teil der Tabelle.  DevTools erstellt eine neue Zeile und fokussiert den Cursor in der **Schlüssel** Spalte.  
    
    > ##### Abbildung5  
    > Der leere Teil der Tabelle zum doppelklicken, um ein neues Schlüssel-Wert-Paar zu erstellen  
    > ![Der leere Teil der Tabelle zum doppelklicken, um ein neues Schlüssel-Wert-Paar zu erstellen][ImageLocalStorageCreate]  

## Bearbeiten von `localStorage` Schlüsseln oder Werten   

1.  [Anzeigen der `localStorage` Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)  
1.  Doppelklicken Sie auf eine Zelle in der Spalte **Schlüssel** oder **Wert** , um diesen Schlüssel oder Wert zu bearbeiten.  
    
    > ##### Abbildung6  
    > Bearbeiten eines `localStorage` Schlüssels  
    > ![Bearbeiten eines localStorage-Schlüssels][ImageLocalStorageEdit]  

## Löschen von `localStorage` Schlüssel-Wert-Paaren   

1.  [Anzeigen der `localStorage` Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)  
1.  Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.  DevTools hebt das Blau hervor, um anzugeben, dass es markiert ist.  

1.  Drücken Sie die Eingabe `Delete` Taste, oder klicken Sie auf **Ausgewählte löschen Löschen** ![ ][ImageDeleteIcon] .  

## Löschen aller `localStorage` Schlüssel-Wert-Paare für eine Domäne   

1.  [Anzeigen der `localStorage` Schlüssel-Wert-Paare einer Domäne](#view-localstorage-keys-and-values)  

1.  Wählen Sie **alle** löschen aus ![ ][ImageClearIcon] .  

## Interagieren mit `localStorage` der Konsole   

Da sie JavaScript in der **Konsole**ausführen können und die **Konsole** Zugriff auf die JavaScript-Kontexte der Seite hat, ist es möglich, mit `localStorage` der **Konsole**zu interagieren.  

1.  Verwenden Sie das **JavaScript** -Kontextmenü, um den JavaScript-Kontext der **Konsole** zu ändern, wenn Sie auf die `localStorage` Schlüssel-Wert-Paare einer anderen Domäne als auf die angezeigte Seite zugreifen möchten.  
    
    > ##### Abbildung7  
    > Ändern des JavaScript-Kontexts der **Konsole**  
    > ![Ändern des JavaScript-Kontexts der Konsole][ImageJSContext]  

1.  Führen Sie Ihre `localStorage` Ausdrücke in der Konsole wie in Ihrem JavaScript aus.  
    
    > ##### Abbildung8  
    > Interagieren mit `localStorage` der **Konsole**  
    > ![Interagieren mit localStorage über die Konsole][ImageLocalStorageConsole]  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Abbildung 1: der Bereich "Manifest""  
[ImageLocalStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage.msft.png "Abbildung 2: lokales Speicher-Menü"  
[ImageLocalStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value.msft.png "Abbildung 3: die localStorage-Schlüssel-Wert-Paare für die https://www.bing.com Domäne"  
[ImageLocalStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value-selected.msft.png "Abbildung 4: Anzeigen des Werts des eventLogQueue_Online Schlüssels"  
[ImageLocalStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-new-key-value.msft.png "Abbildung 5: der leere Teil der Tabelle, doppelklicken Sie, um ein neues Schlüssel-Wert-Paar zu erstellen"  
[ImageLocalStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-edit-key-value.msft.png "Abbildung 6: Bearbeiten eines localStorage-Schlüssels"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage.msft.png "Abbildung 7: Ändern des JavaScript-Kontexts der Konsole"  
[ImageLocalStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage-interaction.msft.png "Abbildung 8: interagieren mit localStorage über die Konsole"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
