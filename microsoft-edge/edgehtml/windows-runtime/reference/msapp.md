---
title: MSApp-API-Referenz
description: Stellt Hilfsfunktionen zur Verfügung, mit denen Sie Blob- und MSStream-Objekte erstellen können.  MSApp-Objekte und -Member werden für Windows-Apps mithilfe von JavaScript unterstützt.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, Dateiupload, Blog, MSStream, Windows 10-Apps, UWP, Edge
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0607929971b1dd2956571304230f69f756497e32
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439724"
---
# <a name="msapp"></a><span data-ttu-id="e2e63-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="e2e63-105">MSApp</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="e2e63-106">Das MSApp-Objekt und seine Member werden nur für Windows-Apps unterstützt, die JavaScript \(einschließlich PWAs, die auf Windows-API-Features zugreifen\).</span><span class="sxs-lookup"><span data-stu-id="e2e63-106">The MSApp object and its members are supported only for Windows apps using JavaScript \(including PWAs accessing Windows API features\).</span></span>  <span data-ttu-id="e2e63-107">Das #A0 ist nur im lokalen Kontext eines #A1 in einer #A1 vorhanden, die über das ms-appx-URI-Schema geladen wird. Andernfalls ist das Objekt nicht vorhanden (und folglich sind keine seiner Methoden und Eigenschaften verfügbar).</span><span class="sxs-lookup"><span data-stu-id="e2e63-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>  

<span data-ttu-id="e2e63-108">Es bietet Hilfsfunktionen, mit denen Sie [Blob-](https://developer.mozilla.org/docs/Web/API/Blob) und [MSStream-Objekte erstellen](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) können.</span><span class="sxs-lookup"><span data-stu-id="e2e63-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="e2e63-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="e2e63-109">Methods</span></span>](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e2e63-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span><span class="sxs-lookup"><span data-stu-id="e2e63-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="e2e63-111">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e2e63-111">Constants</span></span>](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e2e63-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span><span class="sxs-lookup"><span data-stu-id="e2e63-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="e2e63-113">MSAppAsyncOperation-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e2e63-113">MSAppAsyncOperation interface</span></span>](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [<span data-ttu-id="e2e63-114">start</span><span class="sxs-lookup"><span data-stu-id="e2e63-114">start</span></span>](#start)  
   :::column-end:::
:::row-end:::  

## <a name="msapp-methods"></a><span data-ttu-id="e2e63-115">MSApp-Methoden</span><span class="sxs-lookup"><span data-stu-id="e2e63-115">MSApp methods</span></span>  

### <a name="cleartemporarywebdataasync"></a><span data-ttu-id="e2e63-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="e2e63-116">clearTemporaryWebDataAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-117">Entfernt Cache- und indexierteDB-Daten für die App oder [WebView](../../hosting/webview/index.md).</span><span class="sxs-lookup"><span data-stu-id="e2e63-117">Clears cache and indexedDB data for the app or [WebView](../../hosting/webview/index.md).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-118">Parameters</span></span>**  
      
      <span data-ttu-id="e2e63-119">Diese Methode verfügt über keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e2e63-119">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-120">Return value</span></span>**  
      
      <span data-ttu-id="e2e63-121">Typ: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="e2e63-121">Type: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span></span>  
      
      <span data-ttu-id="e2e63-122">Stellt eine asynchrone Aktion dar.</span><span class="sxs-lookup"><span data-stu-id="e2e63-122">Represents an asynchronous action.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-123">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="e2e63-123">Exceptions</span></span>**  
      
      <span data-ttu-id="e2e63-124">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-124">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e63-125">Remarks</span></span>**  
      
      <span data-ttu-id="e2e63-126">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-126">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2e63-127">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createblobfromrandomaccessstream"></a><span data-ttu-id="e2e63-128">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="e2e63-128">createBlobFromRandomAccessStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-129">Erstellt ein [Blob](https://developer.mozilla.org/docs/Web/API/Blob) aus einem [IRandomAccessStream-Objekt.](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)</span><span class="sxs-lookup"><span data-stu-id="e2e63-129">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span>  <span data-ttu-id="e2e63-130">Diese Methode sollte beim Umgang mit Objekten in Apps verwendet werden, um ein W3C-basiertes Objekt aus `IRandomAccessStream` dem Datenstrom zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e2e63-130">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span>  <span data-ttu-id="e2e63-131">Nachdem das Blob erstellt wurde, kann es mit [den FileReader-,](https://developer.mozilla.org/docs/Web/API/FileReader) [URL-APIs](https://developer.mozilla.org/docs/Web/API/URL)und [XMLHttpRequest verwendet werden.](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest)</span><span class="sxs-lookup"><span data-stu-id="e2e63-131">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-132">Parameters</span></span>**  
      
      `type` <span data-ttu-id="e2e63-133">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-133">[in]</span></span>  
      
      | <span data-ttu-id="e2e63-134">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-134">Type</span></span> | <span data-ttu-id="e2e63-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-135">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e2e63-136">String</span></span> | <span data-ttu-id="e2e63-137">Inhaltstyp der Daten.</span><span class="sxs-lookup"><span data-stu-id="e2e63-137">Content type of the data.</span></span>  <span data-ttu-id="e2e63-138">Diese Zeichenfolge sollte das im Medientyptoken in Abschnitt 3.7 von RFC 2616 definierte Format haben.</span><span class="sxs-lookup"><span data-stu-id="e2e63-138">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  |  
      
      `stream` <span data-ttu-id="e2e63-139">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-139">[in]</span></span>  
      
      | <span data-ttu-id="e2e63-140">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-140">Type</span></span> | <span data-ttu-id="e2e63-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-141">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-142">Any</span><span class="sxs-lookup"><span data-stu-id="e2e63-142">Any</span></span> | <span data-ttu-id="e2e63-143">[IRandomAccessStream,](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) das im Blob gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2e63-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-144">Return value</span></span>**  
      
      | <span data-ttu-id="e2e63-145">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-145">Type</span></span> | <span data-ttu-id="e2e63-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-146">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-147">Blob</span><span class="sxs-lookup"><span data-stu-id="e2e63-147">Blob</span></span> | <span data-ttu-id="e2e63-148">Neues Blob-Objekt, das den Datenstrom enthält.</span><span class="sxs-lookup"><span data-stu-id="e2e63-148">New blob object that contains the stream.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-149">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="e2e63-149">Exceptions</span></span>**  
      
      | <span data-ttu-id="e2e63-150">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="e2e63-150">Exception</span></span> | <span data-ttu-id="e2e63-151">Bedingung</span><span class="sxs-lookup"><span data-stu-id="e2e63-151">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-152">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="e2e63-152">TypeMismatchError</span></span> | <span data-ttu-id="e2e63-153">Der Knotentyp ist mit dem erwarteten Parametertyp nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e2e63-153">The node type is incompatible with the expected parameter type.</span></span>  <span data-ttu-id="e2e63-154">Für Versionen vor Internet Explorer 10 wird TYPE_MISMATCH_ERR zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2e63-154">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-155">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e63-155">Remarks</span></span>**  
      
      <span data-ttu-id="e2e63-156">Erstellt einen Blob aus Windows-Runtime-Typen über den MSApp-Namespace im Window-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e2e63-156">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span>  <span data-ttu-id="e2e63-157">Mit dieser Methode wird ein Blob erstellt, das im Wesentlichen ein leichter Wrapper über das [bereitgestellte RandomAccessStream-Objekt](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) ist.</span><span class="sxs-lookup"><span data-stu-id="e2e63-157">This method will create a blob that is essentially a light wrapper over the [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span>  <span data-ttu-id="e2e63-158">Das Blob besitzt die Lebensdauer dieses Datenstroms, und der Datenstrom wird geschlossen, wenn das Blob zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="e2e63-158">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-159">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2e63-159">Example</span></span>**  
      
      ```javascript
      var randomAccessStream = dataPackage.GetData("image/bmp");
      var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
      var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});
      
      document.getElementById("imagetag").src = url; 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createdatapackage"></a><span data-ttu-id="e2e63-160">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="e2e63-160">createDataPackage</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-161">Konvertiert den angegebenen Bereich des Benutzers oder der Anwendung in ein HTML-Fragment, das freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="e2e63-161">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-162">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-162">Parameters</span></span>**  
      
      `object` <span data-ttu-id="e2e63-163">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-163">[in]</span></span>  
      
      | <span data-ttu-id="e2e63-164">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-164">Type</span></span> | <span data-ttu-id="e2e63-165">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-165">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-166">Any</span><span class="sxs-lookup"><span data-stu-id="e2e63-166">Any</span></span> | <span data-ttu-id="e2e63-167">Dieser Bereich kann entweder aus einem Auswahlobjekt erstellt werden, z. B.: `window.selection.getRangeAt(0)` oder manuell.</span><span class="sxs-lookup"><span data-stu-id="e2e63-167">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-168">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-168">Return value</span></span>**  
      
      | <span data-ttu-id="e2e63-169">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-169">Type</span></span> | <span data-ttu-id="e2e63-170">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-170">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-171">Any</span><span class="sxs-lookup"><span data-stu-id="e2e63-171">Any</span></span> | <span data-ttu-id="e2e63-172">Enthält das HTML-Markup für den angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="e2e63-172">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-173">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="e2e63-173">Exceptions</span></span>**  
      
      <span data-ttu-id="e2e63-174">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-174">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-175">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e63-175">Remarks</span></span>**  
      
      <span data-ttu-id="e2e63-176">Diese Methode unterstützt nur [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), nicht [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span><span class="sxs-lookup"><span data-stu-id="e2e63-176">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span>  <span data-ttu-id="e2e63-177">Das zurückgegebene Datenpaket für den angegebenen Bereich enthält HTML-Markup im Zwischenablageformat.</span><span class="sxs-lookup"><span data-stu-id="e2e63-177">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>  
      
      <span data-ttu-id="e2e63-178">Für das zurückgegebene Datenpaket sind keine Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e2e63-178">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-179">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2e63-179">Example</span></span>**  
      
      <span data-ttu-id="e2e63-180">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-180">None.</span></span>  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createdatapackagefromselection"></a><span data-ttu-id="e2e63-181">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="e2e63-181">createDataPackageFromSelection</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-182">Konvertiert die Auswahl des Benutzers oder der Anwendung in ein HTML-Fragment, das freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="e2e63-182">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-183">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-183">Parameters</span></span>**  
      
      <span data-ttu-id="e2e63-184">Diese Methode verfügt über keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e2e63-184">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-185">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-185">Return value</span></span>**  
      
      | <span data-ttu-id="e2e63-186">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-186">Type</span></span> | <span data-ttu-id="e2e63-187">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-187">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-188">Any</span><span class="sxs-lookup"><span data-stu-id="e2e63-188">Any</span></span> | <span data-ttu-id="e2e63-189">Enthält das HTML-Markup für den angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="e2e63-189">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-190">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="e2e63-190">Exceptions</span></span>**  
      
      <span data-ttu-id="e2e63-191">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-191">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-192">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e63-192">Remarks</span></span>**  
      
      <span data-ttu-id="e2e63-193">Das zurückgegebene Datenpaket für die Auswahl enthält HTML-Markup im Zwischenablageformat.</span><span class="sxs-lookup"><span data-stu-id="e2e63-193">The returned data package for the selection contains HTML markup in clipboard format.</span></span>  <span data-ttu-id="e2e63-194">Wenn innerhalb der Benutzeroberfläche der Anwendung keine Benutzerauswahl vorkommt, gibt der `createDataPackageFromSelection` `null` zurück.</span><span class="sxs-lookup"><span data-stu-id="e2e63-194">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns `null`.</span></span>  
      
      <span data-ttu-id="e2e63-195">Für das zurückgegebene Datenpaket sind keine Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e2e63-195">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-196">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2e63-196">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### <a name="createfilefromstoragefile"></a><span data-ttu-id="e2e63-197">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="e2e63-197">createFileFromStorageFile</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-198">Konvertiert ein [WinRT](/uwp/api/) [StorageFile-Objekt](/uwp/api/windows.storage.storagefile) in ein standard W3C [File-Objekt.](https://developer.mozilla.org/docs/Web/API/File)</span><span class="sxs-lookup"><span data-stu-id="e2e63-198">Converts a [WinRT](/uwp/api/) [StorageFile](/uwp/api/windows.storage.storagefile) to a standard W3C [File](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-199">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-199">Parameters</span></span>**  
      
      `storageFile` <span data-ttu-id="e2e63-200">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-200">[in]</span></span>
      
      | <span data-ttu-id="e2e63-201">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-201">Type</span></span> | <span data-ttu-id="e2e63-202">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-202">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-203">Any</span><span class="sxs-lookup"><span data-stu-id="e2e63-203">Any</span></span> | <span data-ttu-id="e2e63-204">Enthält die Speicherdatei.</span><span class="sxs-lookup"><span data-stu-id="e2e63-204">Contains the storage file.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-205">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-205">Return value</span></span>**
      
      <span data-ttu-id="e2e63-206">Keiner</span><span class="sxs-lookup"><span data-stu-id="e2e63-206">None</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-207">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="e2e63-207">Exceptions</span></span>**  
      
      | <span data-ttu-id="e2e63-208">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="e2e63-208">Exception</span></span> | <span data-ttu-id="e2e63-209">Bedingung</span><span class="sxs-lookup"><span data-stu-id="e2e63-209">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-210">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="e2e63-210">TypeMismatchError</span></span> | <span data-ttu-id="e2e63-211">Der angegebene W3C-Dateiverweis ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e2e63-211">The specified W3C file reference is invalid.</span></span>  <span data-ttu-id="e2e63-212">Für Versionen vor Internet Explorer 10 wird `TYPE_MISMATCH_ERR` zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2e63-212">For versions earlier than Internet Explorer 10, `TYPE_MISMATCH_ERR` is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-213">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e63-213">Remarks</span></span>**  
      
      <span data-ttu-id="e2e63-214">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-214">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-215">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2e63-215">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createstreamfrominputstream"></a><span data-ttu-id="e2e63-216">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="e2e63-216">createStreamFromInputStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-217">Erstellt einen [MSStream aus](https://msdn.microsoft.com/library/hh772328) einem [InputStream -Objekt.](https://msdn.microsoft.com/library/hh772327)</span><span class="sxs-lookup"><span data-stu-id="e2e63-217">Creates an [MSStream](https://msdn.microsoft.com/library/hh772328) from an [InputStream](https://msdn.microsoft.com/library/hh772327).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-218">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-218">Parameters</span></span>**  
      
      `type` <span data-ttu-id="e2e63-219">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-219">[in]</span></span>
      
      | <span data-ttu-id="e2e63-220">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-220">Type</span></span> | <span data-ttu-id="e2e63-221">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-221">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-222">DOMString</span><span class="sxs-lookup"><span data-stu-id="e2e63-222">DOMString</span></span> | <span data-ttu-id="e2e63-223">Inhaltstyp der Daten.</span><span class="sxs-lookup"><span data-stu-id="e2e63-223">Content type of the data.</span></span>  <span data-ttu-id="e2e63-224">Diese Zeichenfolge sollte das im Medientyptoken in Abschnitt 3.7 von RFC 2616 definierte Format haben.</span><span class="sxs-lookup"><span data-stu-id="e2e63-224">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  <span data-ttu-id="e2e63-225">\([Siehe MIME-Typen,]( https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) z. B. `text/plain` , , , , , , , , `text/html` und so `image/jpeg` `image/png` `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` weiter\).</span><span class="sxs-lookup"><span data-stu-id="e2e63-225">\([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) such as `text/plain`, `text/html`, `image/jpeg`, `image/png`, `audio/mpeg`, `audio/ogg`, `audio/*`, `video/mp4`, and so on\).</span></span>  
      
      `inputStream` <span data-ttu-id="e2e63-226">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-226">[in]</span></span>
      
      | <span data-ttu-id="e2e63-227">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-227">Type</span></span> | <span data-ttu-id="e2e63-228">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-228">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-229">Any</span><span class="sxs-lookup"><span data-stu-id="e2e63-229">Any</span></span> | <span data-ttu-id="e2e63-230">Der [IInputStream,](/uwp/api/Windows.Storage.Streams.IInputStream) der in gespeichert werden `MSStream` soll.</span><span class="sxs-lookup"><span data-stu-id="e2e63-230">The [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-231">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-231">Return value</span></span>**
      
      <span data-ttu-id="e2e63-232">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-232">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-233">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="e2e63-233">Exceptions</span></span>**  
      
      <span data-ttu-id="e2e63-234">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-234">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-235">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e63-235">Remarks</span></span>**  
      
      <span data-ttu-id="e2e63-236">Diese Methode verwendet einen Inhaltstyp und den `IInputStream` Verweis.</span><span class="sxs-lookup"><span data-stu-id="e2e63-236">This method takes a content-type, and the `IInputStream` reference.</span></span>  <span data-ttu-id="e2e63-237">Die Methode überprüft dann, ob der übergebene Streamverweis eine Instanz des Typs ist und, falls `IInputStream` nicht, ausgelöst `DOMException TYPE_MISMATCH_ERR` wird.</span><span class="sxs-lookup"><span data-stu-id="e2e63-237">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span>  <span data-ttu-id="e2e63-238">Wenn kein Fehler auftritt, `createStreamFromInputStream` wird `MSStream` ein \(aus den Eingaben\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="e2e63-238">If no error occurs, `createStreamFromInputStream` creates an `MSStream` \(from its inputs\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-239">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2e63-239">Example</span></span>**  
      
      <span data-ttu-id="e2e63-240">Ein `IInputStream` kann zum Erstellen eines verwendet `MSStream` werden.</span><span class="sxs-lookup"><span data-stu-id="e2e63-240">An `IInputStream` can be used to create an `MSStream`.</span></span>  <span data-ttu-id="e2e63-241">Wie bei Objekten mit einmaler Verwendung werden alle von erstellten URLs beim ersten Auflösen durch das `MSStreams` `URL.createObjectURL` Image-Element widerrufen.</span><span class="sxs-lookup"><span data-stu-id="e2e63-241">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span>  <span data-ttu-id="e2e63-242">Darüber hinaus werden Anforderungen für eine zweite URL für dieses Objekt nach der Verwendung des Datenstroms fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="e2e63-242">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>  
      
      ```javascript
      var inputStream = myInputStream; //get InputStream from socket API, and so on
      var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
      document.getElementById("imagetag").src = URL.createObjectURL(stream); 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="execasyncatpriority"></a><span data-ttu-id="e2e63-243">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="e2e63-243">execAsyncAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-244">Plant einen Rückruf, der zu einem späteren Zeitpunkt gemäß der angegebenen Priorität ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2e63-244">Schedules a callback to be executed at a later time according to the given priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-245">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-245">Parameters</span></span>**  
      
      `asynchronousCallback` <span data-ttu-id="e2e63-246">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-246">[in]</span></span>
      
      | <span data-ttu-id="e2e63-247">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-247">Type</span></span> | <span data-ttu-id="e2e63-248">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-248">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-249">Funktion</span><span class="sxs-lookup"><span data-stu-id="e2e63-249">Function</span></span> | <span data-ttu-id="e2e63-250">Die Rückruffunktion, die asynchron ausgeführt werden soll, wird mit der angegebenen Prioritätspriorität ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="e2e63-250">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>  |  
      
      `priority` <span data-ttu-id="e2e63-251">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-251">[in]</span></span>
      
      | <span data-ttu-id="e2e63-252">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-252">Type</span></span> | <span data-ttu-id="e2e63-253">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-253">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-254">DOMString</span><span class="sxs-lookup"><span data-stu-id="e2e63-254">DOMString</span></span> | <span data-ttu-id="e2e63-255">Der Kontextprioritätswert, mit dem der asynchroneCallback-Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2e63-255">The contextual priority value at which the asynchronousCallback callback is run.</span></span>  <span data-ttu-id="e2e63-256">Weitere Informationen finden Sie unter [MSApp Constants](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="e2e63-256">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="e2e63-257">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-257">[in]</span></span>
      
      | <span data-ttu-id="e2e63-258">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-258">Type</span></span> | <span data-ttu-id="e2e63-259">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-259">Description</span></span> |  
      |:---- |:--- |   
      | <span data-ttu-id="e2e63-260">Any</span><span class="sxs-lookup"><span data-stu-id="e2e63-260">Any</span></span> | <span data-ttu-id="e2e63-261">Eine optionale Reihe von Argumenten, die an die synchroneCallback-Rückruffunktion \(als Parameter 1 und so weiter\) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e2e63-261">An optional series of arguments that are passed to the synchronousCallback callback function \(as parameters 1 and so on\).</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-262">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-262">Return value</span></span>**  
      
      <span data-ttu-id="e2e63-263">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e2e63-263">This method does not return a value.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-264">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="e2e63-264">Exceptions</span></span>**  
      
      <span data-ttu-id="e2e63-265">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-265">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-266">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e63-266">Remarks</span></span>**  
      
      <span data-ttu-id="e2e63-267">Die `asynchronousCallback` bereitgestellte Rückruffunktion wird später asynchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e2e63-267">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span>  `asynchronousCallback` <span data-ttu-id="e2e63-268">wird entsprechend der angegebenen Priorität versendet.</span><span class="sxs-lookup"><span data-stu-id="e2e63-268">will be dispatched according to the provided priority.</span></span>  <span data-ttu-id="e2e63-269">Die normale Priorität entspricht der vorhandenen [setImmediate-Methode.](https://developer.mozilla.org/docs/Web/API/Window/setImmediate)</span><span class="sxs-lookup"><span data-stu-id="e2e63-269">Normal priority is equivalent to the existing [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span>  <span data-ttu-id="e2e63-270">Wenn der Rückruf ausgeführt wird, wird die aktuelle Kontextpriorität für die Dauer der Ausführung des Rückrufs auf den angegebenen Prioritätsparameterwert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e2e63-270">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>  
      
      <span data-ttu-id="e2e63-271">Der `asynchronousCallback` Callbackparameter kann eine beliebige Funktion sein.</span><span class="sxs-lookup"><span data-stu-id="e2e63-271">The `asynchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="e2e63-272">Wenn Argumente nach dem Parameter angegeben werden, werden sie `priority` alle an die Rückruffunktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="e2e63-272">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>  
      
      <span data-ttu-id="e2e63-273">Im Gegensatz zu wird jedes von der Rückruffunktion zurückgegebene Objekt `execAtPriority` `asynchronousCallback` ignoriert \(und nicht über `execAsyncAtPriority` \zurückgegeben).</span><span class="sxs-lookup"><span data-stu-id="e2e63-273">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored \(and not returned via `execAsyncAtPriority`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-274">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2e63-274">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="execatpriority"></a><span data-ttu-id="e2e63-275">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="e2e63-275">execAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-276">Führt die angegebene Rückruffunktion mit der angegebenen Kontextpriorität aus.</span><span class="sxs-lookup"><span data-stu-id="e2e63-276">Runs the specified callback function at the given contextual priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-277">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-277">Parameters</span></span>**  
      
      `synchronousCallback` <span data-ttu-id="e2e63-278">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-278">[in]</span></span>  
      
      | <span data-ttu-id="e2e63-279">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-279">Type</span></span> | <span data-ttu-id="e2e63-280">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-280">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-281">Funktion</span><span class="sxs-lookup"><span data-stu-id="e2e63-281">Function</span></span> | <span data-ttu-id="e2e63-282">Die Rückruffunktion, die synchron mit der angegebenen Kontextpriorität der Priorität ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2e63-282">The callback function to run synchronously at the given priority contextual priority.</span></span>  |  
      
      `priority` <span data-ttu-id="e2e63-283">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-283">[in]</span></span>  
      
      | <span data-ttu-id="e2e63-284">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-284">Type</span></span> | <span data-ttu-id="e2e63-285">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-285">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-286">DOMString</span><span class="sxs-lookup"><span data-stu-id="e2e63-286">DOMString</span></span> | <span data-ttu-id="e2e63-287">Der angegebene Prioritätswert, auf den der aktuelle Kontextprioritätswert festgelegt wird, wenn die `synchronousCallback` Rückruffunktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2e63-287">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span>  <span data-ttu-id="e2e63-288">Weitere Informationen finden Sie unter [MSApp Constants](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="e2e63-288">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="e2e63-289">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-289">[in]</span></span>  
      
      | <span data-ttu-id="e2e63-290">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-290">Type</span></span> | <span data-ttu-id="e2e63-291">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-291">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-292">Any</span><span class="sxs-lookup"><span data-stu-id="e2e63-292">Any</span></span> | <span data-ttu-id="e2e63-293">Eine optionale Reihe von Argumenten, die an die `synchronousCallback` Rückruffunktion \(als Parameter 1 und so weiter\) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e2e63-293">An optional series of arguments that are passed to the `synchronousCallback` callback function \(as parameters 1 and so on\).</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-294">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-294">Return value</span></span>**  
      
      | <span data-ttu-id="e2e63-295">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-295">Type</span></span> | <span data-ttu-id="e2e63-296">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-296">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-297">Any</span><span class="sxs-lookup"><span data-stu-id="e2e63-297">Any</span></span> | <span data-ttu-id="e2e63-298">Gibt den Rückgabewert des `synchronousCallback` Rückrufs \(wie zutreffend\) zurück.</span><span class="sxs-lookup"><span data-stu-id="e2e63-298">Returns the return value of the `synchronousCallback` callback \(as applicable\).</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-299">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="e2e63-299">Exceptions</span></span>**  
      
      <span data-ttu-id="e2e63-300">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-300">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-301">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e63-301">Remarks</span></span>**  
      
      <span data-ttu-id="e2e63-302">Die `synchronousCallback` bereitgestellte Rückrufmethode wird synchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e2e63-302">The provided `synchronousCallback` callback method is execute synchronously.</span></span>  <span data-ttu-id="e2e63-303">Die aktuelle Kontextpriorität wird für die Dauer der bereitgestellten Rückruffunktion in den angegebenen Prioritätswert (angegeben durch das Prioritätsargument) geändert.</span><span class="sxs-lookup"><span data-stu-id="e2e63-303">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span>  <span data-ttu-id="e2e63-304">Sobald die Ausführung der Rückruffunktion abgeschlossen ist, wird die Priorität auf den vorherigen Wert vor dem Aufruf `execAtPriority` zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2e63-304">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span>  <span data-ttu-id="e2e63-305">Der Rückgabewert von `execAtPriority` ist der Rückgabewert der Rückrufmethode \(wie angegeben\).</span><span class="sxs-lookup"><span data-stu-id="e2e63-305">The return value from `execAtPriority` is the return value of the callback method \(as provided\).</span></span>  
      
      <span data-ttu-id="e2e63-306">Der `synchronousCallback` Callbackparameter kann eine beliebige Funktion sein.</span><span class="sxs-lookup"><span data-stu-id="e2e63-306">The `synchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="e2e63-307">Wenn Argumente nach dem Priority-Parameter angegeben werden, werden sie an die bereitgestellte Rückrufmethode übergeben.</span><span class="sxs-lookup"><span data-stu-id="e2e63-307">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span>  <span data-ttu-id="e2e63-308">Wenn der Rückrufparameter einen Wert zurückgibt, wird dieser Wert auch zum `execAtPriority` Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="e2e63-308">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-309">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2e63-309">Example</span></span>**  
      
      ```javascript
      var user = Windows.System.UserProfile.UserInformation;
      
      MSApp.execAtPriority(function () { // This callback executes synchronously.
        user.getFirstNameAsync().then(function () { // Dispatches at high priority.
          return user.getLastNameAsync();
        }).done(function () { // Dispatches at high priority.
          // USEFUL CODE HERE
        });
      }, MSApp.HIGH); // The second argument of the execAtPriority method.
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="getcurrentpriority"></a><span data-ttu-id="e2e63-310">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="e2e63-310">getCurrentPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-311">Gibt die aktuelle Kontextpriorität zurück.</span><span class="sxs-lookup"><span data-stu-id="e2e63-311">Returns the current contextual priority.</span></span>  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-312">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-312">Parameters</span></span>**  
      
      <span data-ttu-id="e2e63-313">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-313">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-314">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-314">Return value</span></span>**  
      
      | <span data-ttu-id="e2e63-315">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-315">Type</span></span> | <span data-ttu-id="e2e63-316">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-316">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-317">DOMString</span><span class="sxs-lookup"><span data-stu-id="e2e63-317">DOMString</span></span> | <span data-ttu-id="e2e63-318">Der Rückgabewert ist eine der Zeichenfolgen `MSApp.HIGH` , `MSApp.NORMAL` oder `MSApp.IDLE` .</span><span class="sxs-lookup"><span data-stu-id="e2e63-318">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-319">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="e2e63-319">Exceptions</span></span>**  
      
      <span data-ttu-id="e2e63-320">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-320">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-321">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e63-321">Remarks</span></span>**  
      
      <span data-ttu-id="e2e63-322">Diese Methode gibt die aktuelle Kontextpriorität \(siehe [MSApp-Konstanten](#msapp-constants)\) zurück, die über und geändert werden `execAtPriority` `execAsyncAtPriority` kann.</span><span class="sxs-lookup"><span data-stu-id="e2e63-322">This method returns the current contextual priority \(see [MSApp Constants](#msapp-constants)\), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-323">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2e63-323">Example</span></span>**  
      
      ```javascript
      if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
          // YOUR CODE HERE
      }
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="gethtmlprintdocumentsource"></a><span data-ttu-id="e2e63-324">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="e2e63-324">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="e2e63-325">Synchrone API, die veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="e2e63-325">Synchronous API that has been deprecated.</span></span>  <span data-ttu-id="e2e63-326">Informationen zu Windows 10 finden Sie unter `getHtmlPrintDocumentSourceAsync` .</span><span class="sxs-lookup"><span data-stu-id="e2e63-326">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span>  <span data-ttu-id="e2e63-327">Informationen Windows 8 und 8.1-Apps finden Sie im MSDN-Eintrag für [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span><span class="sxs-lookup"><span data-stu-id="e2e63-327">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <a name="gethtmlprintdocumentsourceasync"></a><span data-ttu-id="e2e63-328">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="e2e63-328">getHtmlPrintDocumentSourceAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-329">Gibt den Quellinhalt zurück, der gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2e63-329">Returns the source content that is to be printed.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-330">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-330">Parameters</span></span>**  
      
      `htmlDoc` <span data-ttu-id="e2e63-331">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-331">[in]</span></span>  
      
      | <span data-ttu-id="e2e63-332">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-332">Type</span></span> | <span data-ttu-id="e2e63-333">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-333">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-334">Dokument</span><span class="sxs-lookup"><span data-stu-id="e2e63-334">Document</span></span> | <span data-ttu-id="e2e63-335">Das zu druckde HTML-Dokument.</span><span class="sxs-lookup"><span data-stu-id="e2e63-335">The HTML document to be printed.</span></span>  <span data-ttu-id="e2e63-336">Dies kann das Stammdokument, das Dokument in einem iframe, ein Dokumentfragment oder ein SVG-Dokument sein.</span><span class="sxs-lookup"><span data-stu-id="e2e63-336">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span>  <span data-ttu-id="e2e63-337">Beachten Sie, dass htmlDoc ein Dokument und kein Element sein muss.</span><span class="sxs-lookup"><span data-stu-id="e2e63-337">Be aware that htmlDoc must be a document, not an element.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-338">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-338">Return value</span></span>**
      
      <span data-ttu-id="e2e63-339">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-339">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-340">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="e2e63-340">Exceptions</span></span>**  
      
      <span data-ttu-id="e2e63-341">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-341">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-342">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e63-342">Remarks</span></span>**  
      
      <span data-ttu-id="e2e63-343">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-343">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-344">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e2e63-344">Example 1</span></span>**  
      
      ```javascript
      var printTask = event.request.createPrintTask(title, function (args) {
              var deferral = args.getDeferral();
              var getPrintDocumentSourceAsync;
              if (MSApp.getHtmlPrintDocumentSourceAsync) { // Windows 10
                  getPrintDocumentSourceAsync = MSApp.getHtmlPrintDocumentSourceAsync(document);
              } else {
                  getPrintDocumentSourceAsync = WinJS.Promise.as(MSApp.getHtmlPrintDocumentSource(document));
              }
              getPrintDocumentSourceAsync.then(function (source) {
                  args.setSource(source);
                  deferral.complete();
              }, function (error) {
                  console.error(error);
                  deferral.complete();
              });
      });
      ```  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-345">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e2e63-345">Example 2</span></span>**  
      
      ```javascript
      function registerForPrintContract() {
              var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
              printManager.onprinttaskrequested = onPrintTaskRequested;
              console.log("Print Contract registered.  Use the Print button to print.", "sample", "status");
      }
      
      // Variable to hold the document source to print
      var gHtmlPrintDocumentSource = null;
      
      // Print event handler for printing via the PrintManager API.
      function onPrintTaskRequested(printEvent) {
          var printTask = printEvent.request.createPrintTask("Print Sample", function (args) {
              args.setSource(gHtmlPrintDocumentSource);
      
              // Register the handler for print task completion event
              printTask.oncompleted = onPrintTaskCompleted;
          });
      }
      
      // Print Task event handler is invoked when the print job is completed.
      function onPrintTaskCompleted(printTaskCompletionEvent) {
          // Notify the user about the failure
          if (printTaskCompletionEvent.completion === Windows.Graphics.Printing.PrintTaskCompletion.failed) {
              console.log("Failed to print.", "sample", "error");
          }
      }
      
      // Executed just before printing.
      var beforePrint = function () {
          // Replace with code to be executed just before printing the current document:
      };
      
      // Executed immediately after printing.
      var afterPrint = function () {
          // Replace with code to be executed immediately after printing the current document:
      };
      
      function printButtonHandler() {
          // Optionally, functions to be executed immediately before and after printing can be configured as following:
          window.document.body.onbeforeprint = beforePrint;
          window.document.body.onafterprint = afterPrint;
          
          // Get document source to print
          MSApp.getHtmlPrintDocumentSourceAsync(document).then(function (htmlPrintDocumentSource) {
              gHtmlPrintDocumentSource = htmlPrintDocumentSource;
      
              // If the print contract is registered, the print experience is invoked.
              Windows.Graphics.Printing.PrintManager.showPrintUIAsync();
          });
      }
      ```  
   :::column-end:::
:::row-end:::  

### <a name="getviewid"></a><span data-ttu-id="e2e63-346">getViewId</span><span class="sxs-lookup"><span data-stu-id="e2e63-346">getViewId</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-347">Unterstützung für mehrere Fenster.</span><span class="sxs-lookup"><span data-stu-id="e2e63-347">Support for multiple windows.</span></span>  
      
      > [!NOTE] 
      > <span data-ttu-id="e2e63-348">In Win8.1 unterstützten JavaScript-UWP-Apps mehrere Fenster mithilfe von MSApp-DOM-APIs, die nun enteignet sind.</span><span class="sxs-lookup"><span data-stu-id="e2e63-348">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span>  <span data-ttu-id="e2e63-349">Verwenden Sie für Windows 10 `window.open` , und das neue `window` `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="e2e63-349">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>  
      
      | <span data-ttu-id="e2e63-350">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-350">Description</span></span> |<span data-ttu-id="e2e63-351">Windows 10</span><span class="sxs-lookup"><span data-stu-id="e2e63-351">Windows 10</span></span> | <span data-ttu-id="e2e63-352">Windows8.1</span><span class="sxs-lookup"><span data-stu-id="e2e63-352">Windows 8.1</span></span> |  
      |:---- |:---- |:--- |  
      | <span data-ttu-id="e2e63-353">Erstellen eines neuen Fensters</span><span class="sxs-lookup"><span data-stu-id="e2e63-353">Create new window</span></span> | [<span data-ttu-id="e2e63-354">window.open</span><span class="sxs-lookup"><span data-stu-id="e2e63-354">window.open</span></span>](https://developer.mozilla.org/docs/Web/API/Window/open) | [<span data-ttu-id="e2e63-355">MSApp.createNewView</span><span class="sxs-lookup"><span data-stu-id="e2e63-355">MSApp.createNewView</span></span>](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |<span data-ttu-id="e2e63-356">Neues Window-Objekt</span><span class="sxs-lookup"><span data-stu-id="e2e63-356">New window object</span></span> | [<span data-ttu-id="e2e63-357">Fenster</span><span class="sxs-lookup"><span data-stu-id="e2e63-357">window</span></span>](https://developer.mozilla.org/docs/Web/API/Window) |[<span data-ttu-id="e2e63-358">MSAppView</span><span class="sxs-lookup"><span data-stu-id="e2e63-358">MSAppView</span></span>](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-359">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-359">Parameters</span></span>**  
      
      `window`
      
      | <span data-ttu-id="e2e63-360">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-360">Type</span></span> | <span data-ttu-id="e2e63-361">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-361">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-362">DOMString</span><span class="sxs-lookup"><span data-stu-id="e2e63-362">DOMString</span></span> | <span data-ttu-id="e2e63-363">Ein Objekt, das ein Fenster mit einem DOM-Dokument darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2e63-363">An object representing a window containing a DOM document.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-364">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-364">Return value</span></span>**  
      
      `viewId`
      
      | <span data-ttu-id="e2e63-365">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-365">Type</span></span> | <span data-ttu-id="e2e63-366">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-366">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-367">Zahl</span><span class="sxs-lookup"><span data-stu-id="e2e63-367">Number</span></span> | <span data-ttu-id="e2e63-368">Kann mit den verschiedenen [Windows.UI.ViewManagement.ApplicationViewSwitcher-APIs verwendet](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) werden.</span><span class="sxs-lookup"><span data-stu-id="e2e63-368">Can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-369">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="e2e63-369">Exceptions</span></span>**  
      
      <span data-ttu-id="e2e63-370">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-370">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-371">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e63-371">Remarks</span></span>**  
      
      <span data-ttu-id="e2e63-372">Verwenden [Sie window.open](https://developer.mozilla.org/docs/Web/API/Window/open) und [window](https://developer.mozilla.org/docs/Web/API/Window) zum Erstellen neuer Fenster, fügen Sie dann jedoch die API hinzu, um mit WinRT-APIs zu `MSApp.getViewId` interagieren.</span><span class="sxs-lookup"><span data-stu-id="e2e63-372">Use [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) and [window](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span>  <span data-ttu-id="e2e63-373">Es verwendet ein Objekt als Parameter und gibt eine Zahl zurück, die mit den verschiedenen `window` `viewId` [Windows.UI.ViewManagement.ApplicationViewSwitcher-APIs verwendet werden](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) kann.</span><span class="sxs-lookup"><span data-stu-id="e2e63-373">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  
      
      *   <span data-ttu-id="e2e63-374">Verzögern der Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="e2e63-374">Delaying Visibility</span></span>  
          
          <span data-ttu-id="e2e63-375">Ansichten in WinRT beginnen normalerweise ausgeblendet, und der Endentwickler verwendet so etwas wie zum Anzeigen der `TryShowAsStandaloneAsync` Ansicht, sobald sie vollständig vorbereitet ist.</span><span class="sxs-lookup"><span data-stu-id="e2e63-375">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span>  <span data-ttu-id="e2e63-376">Zeigt in der Webwelt sofort ein Fenster an, und der Endbenutzer kann beobachten, wie Inhalte `window.open` geladen und gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="e2e63-376">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span>  <span data-ttu-id="e2e63-377">Damit Ihre neuen Fenster wie Ansichten in WinRT agieren und nicht sofort angezeigt werden, haben wir eine Option `window.open` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e2e63-377">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span>  <span data-ttu-id="e2e63-378">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e2e63-378">For example:</span></span>  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   <span data-ttu-id="e2e63-379">Primäre Fensterunterschiede</span><span class="sxs-lookup"><span data-stu-id="e2e63-379">Primary Window Differences</span></span>  
          
          <span data-ttu-id="e2e63-380">Das primäre Fenster, das zunächst vom Betriebssystem geöffnet wird, verhält sich anders als die sekundären Fenster, die geöffnet werden:</span><span class="sxs-lookup"><span data-stu-id="e2e63-380">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span>  
          
          | <span data-ttu-id="e2e63-381">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-381">Description</span></span> | <span data-ttu-id="e2e63-382">Primär</span><span class="sxs-lookup"><span data-stu-id="e2e63-382">Primary</span></span> | <span data-ttu-id="e2e63-383">Sekundärer</span><span class="sxs-lookup"><span data-stu-id="e2e63-383">Secondary</span></span> |  
          |:---- |:--- |:--- |  
          | <span data-ttu-id="e2e63-384">window.open</span><span class="sxs-lookup"><span data-stu-id="e2e63-384">window.open</span></span> | <span data-ttu-id="e2e63-385">Zugelassen</span><span class="sxs-lookup"><span data-stu-id="e2e63-385">Allowed</span></span> | <span data-ttu-id="e2e63-386">Disallowed</span><span class="sxs-lookup"><span data-stu-id="e2e63-386">Disallowed</span></span> |  
          | <span data-ttu-id="e2e63-387">window.close</span><span class="sxs-lookup"><span data-stu-id="e2e63-387">window.close</span></span> | <span data-ttu-id="e2e63-388">Schließen der App</span><span class="sxs-lookup"><span data-stu-id="e2e63-388">Close app</span></span> | <span data-ttu-id="e2e63-389">Fenster schließen</span><span class="sxs-lookup"><span data-stu-id="e2e63-389">Close window</span></span> |  
          | <span data-ttu-id="e2e63-390">Navigationseinschränkungen</span><span class="sxs-lookup"><span data-stu-id="e2e63-390">Navigation restrictions</span></span> | <span data-ttu-id="e2e63-391">Nur ACUR</span><span class="sxs-lookup"><span data-stu-id="e2e63-391">ACUR only</span></span> | <span data-ttu-id="e2e63-392">Keine Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="e2e63-392">No restrictions</span></span> |  
          
         <!-- The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).  -->  
      
      *   <span data-ttu-id="e2e63-393">Kommunikationseinschränkungen für den gleichen Ursprung</span><span class="sxs-lookup"><span data-stu-id="e2e63-393">Same Origin Communication Restrictions</span></span>  
          
          <span data-ttu-id="e2e63-394">Es gibt ein schwieriges technisches Problem, das die ordnungsgemäße Unterstützung synchroner, identischer, fensterübergreifender Skriptaufrufe verhindert.</span><span class="sxs-lookup"><span data-stu-id="e2e63-394">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span>  <span data-ttu-id="e2e63-395">Wenn Sie ein Fenster mit demselben Ursprung öffnen, kann skript in einem Fenster direkt Funktionen im anderen Fenster aufrufen, und einige dieser Aufrufe werden fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="e2e63-395">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span>  `postMessage` <span data-ttu-id="e2e63-396">Anrufe funktionieren einfach gut, und es wird empfohlen, dies nach Möglichkeit zu tun.</span><span class="sxs-lookup"><span data-stu-id="e2e63-396">calls work just fine and is the recommended way to do things if possible.</span></span>  <span data-ttu-id="e2e63-397">Es werden Arbeiten zur Verbesserung dieses Problems ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e2e63-397">Work to improve this issue is in progress.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-398">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2e63-398">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### <a name="istaskscheduledatpriorityorhigher"></a><span data-ttu-id="e2e63-399">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="e2e63-399">isTaskScheduledAtPriorityOrHigher</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-400">Gibt einen booleschen Wert zurück, der angibt, ob ausstehende Arbeit auf der angegebenen Prioritätsebene oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="e2e63-400">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-401">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-401">Parameters</span></span>**  
      
      `priority` <span data-ttu-id="e2e63-402">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-402">[in]</span></span>
      
      | <span data-ttu-id="e2e63-403">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-403">Type</span></span> | <span data-ttu-id="e2e63-404">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-404">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-405">DOMString</span><span class="sxs-lookup"><span data-stu-id="e2e63-405">DOMString</span></span> | <span data-ttu-id="e2e63-406">Ein Prioritätswert \(siehe [MSApp-Konstanten](#msapp-constants)\), der die Prioritätsstufe und höher an gibt, um nach ausstehenden Arbeiten in der Warteschlange zu fragen.</span><span class="sxs-lookup"><span data-stu-id="e2e63-406">A priority value \(see [MSApp Constants](#msapp-constants)\) specifying the priority level and above to query for any outstanding queued work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-407">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-407">Return value</span></span>**  
      
      | <span data-ttu-id="e2e63-408">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-408">Type</span></span> | <span data-ttu-id="e2e63-409">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-409">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-410">Boolesch</span><span class="sxs-lookup"><span data-stu-id="e2e63-410">Boolean</span></span> | <span data-ttu-id="e2e63-411">Gibt zurück, wenn Arbeit in der Warteschlange auf der angegebenen Prioritätsebene oder höher `true` liegt, `false` andernfalls.</span><span class="sxs-lookup"><span data-stu-id="e2e63-411">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-412">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="e2e63-412">Exceptions</span></span>**  
      
      <span data-ttu-id="e2e63-413">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-413">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-414">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e63-414">Remarks</span></span>**  
      
      <span data-ttu-id="e2e63-415">Die -Methode bietet eine Möglichkeit für JavaScript-Code, um zu bestimmen, ob ausstehende Arbeit auf den verschiedenen Prioritätsebenen \(oder höher\) mit der Absicht, dass der aufrufende JavaScript-Code dann entscheiden kann, arbeit mit höherer Priorität zu `isTaskScheduledAtPriorityOrHigher` ergeben.</span><span class="sxs-lookup"><span data-stu-id="e2e63-415">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels \(or above\) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-416">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2e63-416">Example</span></span>**  
      
      ```javascript
      function performIdleWork(array_in) {
          var idx = 0;
          
          function performIdleWorkHelper() {
              for (; idx < array_in.length; ++idx) {
                  
                  // USEFUL CODE HERE 
                  
                  if (MSApp.isTaskScheduledAtPriorityOrHigher(MSApp.NORMAL)) {
                      MSApp.execAsyncAtPriority(performIdleWorkHelper, msPriority.IDLE);
                      break;
                  } // if
              } // for
          } // performIdleWorkHelper
          
          performIdleWorkHelper();
      } // performIdleWork
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="pagehandlesallapplicationactivations"></a><span data-ttu-id="e2e63-417">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="e2e63-417">pageHandlesAllApplicationActivations</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-418">Wird verwendet, um eine Aktualisierung des Startpfads (Seitenladen) vor jedem Aktivierungsereignis \(z. B. klicken auf eine Benachrichtigung oder eine angeheftet Kachel\) zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="e2e63-418">Used to avoid a refresh of the start path (page reload) before every activate event \(such as clicking a notification or a pinned tile\).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-419">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-419">Parameters</span></span>**  
      
      | <span data-ttu-id="e2e63-420">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-420">Type</span></span> | <span data-ttu-id="e2e63-421">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-421">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-422">Boolesch</span><span class="sxs-lookup"><span data-stu-id="e2e63-422">Boolean</span></span> | <span data-ttu-id="e2e63-423">Verwenden Sie diese Option, um das Aktualisieren des Startpfads (Seitenladen) immer zu überspringen und stattdessen direkt zum Starten `MSApp.pageHandlesAllApplicationActivations(true)` des `WebUIApplication` aktivierten Ereignisses zu springen.</span><span class="sxs-lookup"><span data-stu-id="e2e63-423">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span>  <span data-ttu-id="e2e63-424">Erfordert, dass alle Seiten Aktivierungsereignisse separat behandeln.</span><span class="sxs-lookup"><span data-stu-id="e2e63-424">Requires that all pages handle activation events separately.</span></span>  <span data-ttu-id="e2e63-425">Wenn Sie diese Methode als definieren, löst das Klicken auf ein aktiviertes Ereignis \(wie eine Benachrichtigung\) das Erneute laden nicht aus, was für Apps mit einer einzelnen Seite unerlässlich ist, die Seiten neu laden `true` möchten.</span><span class="sxs-lookup"><span data-stu-id="e2e63-425">By defining this method as `true`, clicking an activated event \(like a notification\) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-426">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-426">Return value</span></span>**
      
      <span data-ttu-id="e2e63-427">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-427">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-428">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="e2e63-428">Exceptions</span></span>**  
      
      <span data-ttu-id="e2e63-429">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-429">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-430">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e63-430">Remarks</span></span>**  
      
      <span data-ttu-id="e2e63-431">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-431">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-432">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2e63-432">Example</span></span>**  
      
      ```javascript
      // Without this, the app will first refresh to the start path before every activate event
      window.MSApp.pageHandlesAllApplicationActivations(true); 
      
      // This must not be deffered so that it can receive the initial `activated` event in time
      window.Windows.UI.WebUI.WebUIApplication.addEventListener(
          `activated`,
          e =>
              microsoftInterface.handleActivatedEvent(e);
          }),
          false
      );
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="suppresssubdownloadcredentialprompts"></a><span data-ttu-id="e2e63-433">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="e2e63-433">suppressSubdownloadCredentialPrompts</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-434">Steuert, ob eine App mögliche Authentifizierungsaufforderungen während des Downloads von Ressourcen unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="e2e63-434">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-435">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-435">Parameters</span></span>**  
     
      `suppress` <span data-ttu-id="e2e63-436">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-436">[in]</span></span>
      
      | <span data-ttu-id="e2e63-437">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-437">Type</span></span> | <span data-ttu-id="e2e63-438">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-438">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-439">Boolesch</span><span class="sxs-lookup"><span data-stu-id="e2e63-439">Boolean</span></span> | <span data-ttu-id="e2e63-440">Der Wert true unterdrückt potenzielle Authentifizierungsaufforderungen.</span><span class="sxs-lookup"><span data-stu-id="e2e63-440">A value of true suppresses potential authentication prompts.</span></span>  <span data-ttu-id="e2e63-441">Der Wert false unterdrückt keine potenziellen Authentifizierungsaufforderungen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="e2e63-441">A value of false does not suppress any potential authentication prompts from the user.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-442">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-442">Return value</span></span>**  
      
      <span data-ttu-id="e2e63-443">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-443">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-444">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="e2e63-444">Exceptions</span></span>**  
      
      <span data-ttu-id="e2e63-445">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-445">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-446">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e63-446">Remarks</span></span>**  
      
      <span data-ttu-id="e2e63-447">Die `suppressSubdownloadCredentialPrompts` Methode steuert, ob eine App potenzielle Authentifizierungsaufforderungen während des Downloads von Ressourcen unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="e2e63-447">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span>  <span data-ttu-id="e2e63-448">Das Standardverhalten besteht im Nicht unterdrücken von Anmeldeinformationsaufforderungen.</span><span class="sxs-lookup"><span data-stu-id="e2e63-448">The default behavior is to not suppress credential prompts.</span></span>  
      
      `suppressSubdownloadCredentialPrompts` <span data-ttu-id="e2e63-449">ist für die Verwendung durch Apps vorgesehen, die eine übermäßig große Anzahl von Ressourcen laden können, die eine Authentifizierung erfordern, z. B. eine E-Mail-App \(die einen Newsletter enthalten kann, der eine Reihe von Bildern enthält, für die für jedes Bild eine Authentifizierung erforderlich ist\).</span><span class="sxs-lookup"><span data-stu-id="e2e63-449">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app \(which could contain a newsletter containing a number of images where each image requires authentication\).</span></span>  
      
      <span data-ttu-id="e2e63-450">Beim Unterdrücken von Anmeldeinformationen werden beim Zugriff auf Ressourcen, die eine Authentifizierung erfordern, keine Dialogfelder für die Authentifizierung auf Servern angezeigt, und die Ressource wird nicht heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="e2e63-450">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span>  <span data-ttu-id="e2e63-451">Beachten Sie, dass sich dies weder auf andere mögliche Aufforderungen wie Proxyauthentifizierung oder Clientzertifizierungsanforderungsdialogfelder noch auf `suppressSubdownloadCredentialPrompts` XHR auswirken kann.</span><span class="sxs-lookup"><span data-stu-id="e2e63-451">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>  
      
      <span data-ttu-id="e2e63-452">Beachten Sie, `suppressSubdownloadCredentialPrompts` dass sich dies auf alle Inhalte in der Anwendung aus wirkt, einschließlich der inhalte, die im Element gehostet `webview` werden.</span><span class="sxs-lookup"><span data-stu-id="e2e63-452">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>  
      
      > [!IMPORTANT]
      > <span data-ttu-id="e2e63-453">Entscheidungen zur Eingabeaufforderung von Anmeldeinformationen werden zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="e2e63-453">Credential prompt decisions are cached.</span></span>  <span data-ttu-id="e2e63-454">Daher wird das Unterdrücken von Anmeldeinformationsaufforderungen sofort wirksam, wenn Anmeldeinformationsaufforderungen nach dem Unterdrücken der Eingabeaufforderungen jedoch möglicherweise ein erneutes Laden des Dokuments wirksam werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e2e63-454">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-455">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2e63-455">Example</span></span>**  
      
      ```javascript
      // Set to true to suppress potential credential prompts:
      MSApp.suppressSubdownloadCredentialPrompts(true);
      // Now one can load content or navigate iframe/webview to some other site.
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="terminateapp"></a><span data-ttu-id="e2e63-456">terminateApp</span><span class="sxs-lookup"><span data-stu-id="e2e63-456">terminateApp</span></span>  


:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-457">Beendet die aktuelle Anwendung und generiert einen Fehlerbericht.</span><span class="sxs-lookup"><span data-stu-id="e2e63-457">Terminates the current application and generates a failure report.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-458">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-458">Parameters</span></span>**  
      
      `error` <span data-ttu-id="e2e63-459">[in]</span><span class="sxs-lookup"><span data-stu-id="e2e63-459">[in]</span></span>
      
      | <span data-ttu-id="e2e63-460">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-460">Type</span></span> | <span data-ttu-id="e2e63-461">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-461">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-462">Fehler</span><span class="sxs-lookup"><span data-stu-id="e2e63-462">Error</span></span> | <span data-ttu-id="e2e63-463">Ein Objekt, mit dem Sie den Fehler `Error` beschreiben können, der die Beendigung ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="e2e63-463">An `Error` object that you can use to describe the error that triggered the termination.</span></span>  <span data-ttu-id="e2e63-464">Das Objekt muss die Zahlen-, Beschreibungs- und Stapeleigenschaften enthalten. Ein Fehlerbericht wird nicht generiert, wenn das Objekt diese Eigenschaften `Error` nicht enthält.</span><span class="sxs-lookup"><span data-stu-id="e2e63-464">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-465">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-465">Return value</span></span>**
      
      <span data-ttu-id="e2e63-466">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-466">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-467">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="e2e63-467">Exceptions</span></span>**  
      
      <span data-ttu-id="e2e63-468">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-468">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-469">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e63-469">Remarks</span></span>**  
      
      <span data-ttu-id="e2e63-470">Wenn das von gemeldete Problem zu einem der 5 obersten Probleme Ihrer App wird, wird es auf der Seite `terminateApp` Qualität der App angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e2e63-470">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-471">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2e63-471">Example</span></span>**  
      
      <span data-ttu-id="e2e63-472">Dieses Beispiel ruft `terminateApp` auf, wenn eine Ausnahme auftritt.</span><span class="sxs-lookup"><span data-stu-id="e2e63-472">This example calls `terminateApp` when an exception is encountered.</span></span>  <span data-ttu-id="e2e63-473">Es verwendet das `Error` bereitgestellte Objekt, wenn Sie eine Ausnahme abfangen.</span><span class="sxs-lookup"><span data-stu-id="e2e63-473">It uses the `Error` object provided when you catch an exception.</span></span>  
      
      ```javascript
      try {  
          var obj2 = null;  
          obj2.val = 5;  
      }  
      catch(e) {  
          window.MSApp.terminateApp(e);  
      }  
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="msapp-constants"></a><span data-ttu-id="e2e63-474">MSApp-Konstanten</span><span class="sxs-lookup"><span data-stu-id="e2e63-474">MSApp Constants</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-475">Zulässige Prioritätswerte, die `execAsyncAtPriority` mit , , und verknüpft `execAtPriority` `getCurrentPriority` `isTaskScheduldAtPriorityOrHigher` sind.</span><span class="sxs-lookup"><span data-stu-id="e2e63-475">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>  
   :::column-end:::
   :::column span="":::
      #### <a name="current"></a><span data-ttu-id="e2e63-476">Aktuell</span><span class="sxs-lookup"><span data-stu-id="e2e63-476">Current</span></span>  
      
      `current`  
      
      | <span data-ttu-id="e2e63-477">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-477">Type</span></span> | <span data-ttu-id="e2e63-478">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-478">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-479">DOMString</span><span class="sxs-lookup"><span data-stu-id="e2e63-479">DOMString</span></span> | <span data-ttu-id="e2e63-480">Wenn die Methode mit der entsprechenden Methode \(Siehe auch Abschnitt\) verwendet wird, verwendet die Methode beim Ausführen des angeforderten Vorgangs die aktuelle `current` Kontextpriorität.</span><span class="sxs-lookup"><span data-stu-id="e2e63-480">When `current` is used with the appropriate method \(See also section\), the method will use the current contextual priority when executing the requested operation.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="high"></a><span data-ttu-id="e2e63-481">Hoch </span><span class="sxs-lookup"><span data-stu-id="e2e63-481">High</span></span>  
      
      `high`  
      
      | <span data-ttu-id="e2e63-482">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-482">Type</span></span> | <span data-ttu-id="e2e63-483">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-483">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-484">DOMString</span><span class="sxs-lookup"><span data-stu-id="e2e63-484">DOMString</span></span> | <span data-ttu-id="e2e63-485">Wenn die Methode mit der entsprechenden Methode \(Siehe auch Abschnitt\) verwendet wird, verwendet die Methode beim Ausführen des angeforderten Vorgangs eine höhere Priorität als die normale Priorität und löst den Vorgang vor jeder vorhandenen normalen `high` Prioritätsarbeit aus.</span><span class="sxs-lookup"><span data-stu-id="e2e63-485">When `high` is used with the appropriate method \(See also section\), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      #### <a name="idle"></a><span data-ttu-id="e2e63-486">Leerlauf</span><span class="sxs-lookup"><span data-stu-id="e2e63-486">Idle</span></span>  
      
      `idle`  
      
      | <span data-ttu-id="e2e63-487">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-487">Type</span></span> | <span data-ttu-id="e2e63-488">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-488">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-489">DOMString</span><span class="sxs-lookup"><span data-stu-id="e2e63-489">DOMString</span></span> | <span data-ttu-id="e2e63-490">Wenn die Methode mit der entsprechenden Methode \(Siehe auch Abschnitt\) verwendet wird, verwendet die Methode beim Ausführen des angeforderten Vorgangs eine niedrigere Priorität als die normale Priorität, und der Vorgang wird nach jeder vorhandenen normalen `ideal` Prioritätsarbeit ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="e2e63-490">When `ideal` is used with the appropriate method \(See also section\), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="normal"></a><span data-ttu-id="e2e63-491">Normal</span><span class="sxs-lookup"><span data-stu-id="e2e63-491">Normal</span></span>  
      
      `normal`  
      
      | <span data-ttu-id="e2e63-492">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-492">Type</span></span> | <span data-ttu-id="e2e63-493">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-493">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-494">DOMString</span><span class="sxs-lookup"><span data-stu-id="e2e63-494">DOMString</span></span> | <span data-ttu-id="e2e63-495">Wenn die Methode mit der entsprechenden Methode verwendet wird (siehe auch Abschnitt), verwendet die Methode beim Ausführen des angeforderten Vorgangs die normale vorhandene `normal` Priorität.</span><span class="sxs-lookup"><span data-stu-id="e2e63-495">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-496">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2e63-496">Example</span></span>**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-497">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2e63-497">Requirements</span></span>**  
      
      | <span data-ttu-id="e2e63-498">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-498">Type</span></span> | <span data-ttu-id="e2e63-499">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-499">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-500">IDL</span><span class="sxs-lookup"><span data-stu-id="e2e63-500">IDL</span></span> | <span data-ttu-id="e2e63-501">Mshtml.idl</span><span class="sxs-lookup"><span data-stu-id="e2e63-501">Mshtml.idl</span></span> |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## <a name="msappasyncoperation"></a><span data-ttu-id="e2e63-502">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="e2e63-502">MSAppAsyncOperation</span></span>  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <a name="start"></a><span data-ttu-id="e2e63-503">start</span><span class="sxs-lookup"><span data-stu-id="e2e63-503">start</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2e63-504">Startet die `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="e2e63-504">Starts the `MSAppAsyncOperation`.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="e2e63-505">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e63-505">Parameters</span></span>**  
      
      <span data-ttu-id="e2e63-506">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-506">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="e2e63-507">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e63-507">Return value</span></span>**
      
      <span data-ttu-id="e2e63-508">Keine</span><span class="sxs-lookup"><span data-stu-id="e2e63-508">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **<span data-ttu-id="e2e63-509">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2e63-509">Properties</span></span>**  
      
      `error` <span data-ttu-id="e2e63-510">property</span><span class="sxs-lookup"><span data-stu-id="e2e63-510">property</span></span>  
      
      | <span data-ttu-id="e2e63-511">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-511">Type</span></span> | <span data-ttu-id="e2e63-512">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-512">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-513">DOMError</span><span class="sxs-lookup"><span data-stu-id="e2e63-513">DOMError</span></span> | <span data-ttu-id="e2e63-514">Stellt einen Fehler in `MSAppAsyncOperation` dar.</span><span class="sxs-lookup"><span data-stu-id="e2e63-514">Represents an error in `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` <span data-ttu-id="e2e63-515">property</span><span class="sxs-lookup"><span data-stu-id="e2e63-515">property</span></span>  
      
      | <span data-ttu-id="e2e63-516">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-516">Type</span></span> | <span data-ttu-id="e2e63-517">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-517">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-518">EventHandler</span><span class="sxs-lookup"><span data-stu-id="e2e63-518">EventHandler</span></span> | <span data-ttu-id="e2e63-519">Eigenschaft zum Festlegen eines Ereignishandlers nach Abschluss von `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="e2e63-519">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` <span data-ttu-id="e2e63-520">property</span><span class="sxs-lookup"><span data-stu-id="e2e63-520">property</span></span>  
      
      | <span data-ttu-id="e2e63-521">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-521">Type</span></span> | <span data-ttu-id="e2e63-522">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-522">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-523">EventHandler</span><span class="sxs-lookup"><span data-stu-id="e2e63-523">EventHandler</span></span> | <span data-ttu-id="e2e63-524">Eigenschaft zum Festlegen eines Ereignishandlers auf einen Fehler während `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="e2e63-524">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` <span data-ttu-id="e2e63-525">property</span><span class="sxs-lookup"><span data-stu-id="e2e63-525">property</span></span>  
      
      | <span data-ttu-id="e2e63-526">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-526">Type</span></span> | <span data-ttu-id="e2e63-527">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-527">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-528">Zahl</span><span class="sxs-lookup"><span data-stu-id="e2e63-528">Number</span></span> | <span data-ttu-id="e2e63-529">Stellt den Status des asynchronen Vorgangs in der Windows-App mithilfe von JavaScript dar.</span><span class="sxs-lookup"><span data-stu-id="e2e63-529">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span>  <span data-ttu-id="e2e63-530">Werte sind: `Started[0]` , `Completed[1]` , `Error[2]` .</span><span class="sxs-lookup"><span data-stu-id="e2e63-530">Values include: `Started[0]`, `Completed[1]`, `Error[2]`.</span></span>  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` <span data-ttu-id="e2e63-531">property</span><span class="sxs-lookup"><span data-stu-id="e2e63-531">property</span></span>  
      
      | <span data-ttu-id="e2e63-532">Typ</span><span class="sxs-lookup"><span data-stu-id="e2e63-532">Type</span></span> | <span data-ttu-id="e2e63-533">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2e63-533">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="e2e63-534">Any</span><span class="sxs-lookup"><span data-stu-id="e2e63-534">Any</span></span> |<span data-ttu-id="e2e63-535">Stellt das Ergebnis von `MSAppAsyncOperation` dar.</span><span class="sxs-lookup"><span data-stu-id="e2e63-535">Represents the result of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
