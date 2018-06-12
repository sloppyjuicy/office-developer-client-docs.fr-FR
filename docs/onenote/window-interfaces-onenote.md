---
title: Interfaces de fenêtre (OneNote 2013)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: Les interfaces Window et Windows sont que des objets OneNote 2013 API qui permet aux utilisateurs de travailler avec les fenêtres OneNote. Ces objets permettent aux utilisateurs d'énumérer l'ensemble des fenêtres OneNote et de modifier certaines propriétés de la fenêtre.
ms.openlocfilehash: 83a3742419a4c8faf11c22c4766744d675151c1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782548"
---
# <a name="window-interfaces-onenote"></a><span data-ttu-id="a632e-104">Interfaces de fenêtre (OneNote 2013)</span><span class="sxs-lookup"><span data-stu-id="a632e-104">Window interfaces (OneNote)</span></span>

<span data-ttu-id="a632e-p102">Les interfaces **Window** et **Windows** sont que des objets OneNote 2013 API qui permet aux utilisateurs de travailler avec les fenêtres OneNote. Ces objets permettent aux utilisateurs d'énumérer l'ensemble des fenêtres OneNote et de modifier certaines propriétés de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a632e-p102">The **Window** and **Windows** interfaces are OneNote 2013 API objects that enables users to work with OneNote windows. These objects allow users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
  
## <a name="onenote-window-views"></a><span data-ttu-id="a632e-107">Affichages de fenêtre OneNote</span><span class="sxs-lookup"><span data-stu-id="a632e-107">OneNote window views</span></span>

<span data-ttu-id="a632e-108">La liste suivante indique les modes de quatre affichage que vous pouvez utiliser pour les fenêtres OneNote :</span><span class="sxs-lookup"><span data-stu-id="a632e-108">The following list shows the four view modes that you can use for OneNote windows:</span></span> 
  
- <span data-ttu-id="a632e-109">Mode normal  affiche la fenêtre de OneNote par défaut dans lequel les volets de navigation Bloc-notes et de Page sont visibles.</span><span class="sxs-lookup"><span data-stu-id="a632e-109">Normal view—Displays the default OneNote window in which the Notebook and Page navigation panes are visible.</span></span>
    
- <span data-ttu-id="a632e-110">Page vue d'ensemble  affiche une minimale-interface utilisateur (IU) de vue dans laquelle les volets bloc-notes et de Page ne sont pas affichées.</span><span class="sxs-lookup"><span data-stu-id="a632e-110">Full Page view—Displays a minimal user-interface (UI) view in which the Notebook and Page panes are not displayed.</span></span>
    
- <span data-ttu-id="a632e-p103">Note rapide  affiche une fenêtre de petite taille qui permet aux utilisateurs de prendre des notes courtes. Vous accédez généralement notes rapides par le biais de l'icône de OneNote dans la zone de notification de Windows, mais vous pouvez également accéder par le biais de l'onglet **affichage** dans OneNote.</span><span class="sxs-lookup"><span data-stu-id="a632e-p103">Quick note—Displays a small window that allows users to take short notes. You would usually access quick notes through the OneNote icon in the Windows notification area, but you can also access them through the **View** tab in OneNote.</span></span> 
    
- <span data-ttu-id="a632e-p104">Ancrer sur le bureau  affiche une fenêtre OneNote que vous pouvez ancrer à n'importe quel côté du bureau (similaire à la barre des tâches). Cet affichage réduit la taille du bureau pour s'adapter à la fenêtre. Vous pouvez ancrer qu'une seule fenêtre à tout moment, et la fenêtre est toujours visible sans le blocage du bureau.</span><span class="sxs-lookup"><span data-stu-id="a632e-p104">Dock to Desktop—Displays a OneNote window that you can dock to any side of the desktop (similar to the taskbar). This view reduces the size of the desktop to fit the window. You can dock only one window at any time, and the window is always visible without blocking the desktop.</span></span> 
    
<span data-ttu-id="a632e-116">La figure suivante illustre le l’affichage de la Page entière, station d’accueil pour l’affichage du bureau, et notes rapides se présenter comme sur votre bureau.</span><span class="sxs-lookup"><span data-stu-id="a632e-116">The following figure shows what the Full Page view, Dock to Desktop view, and quick notes look like on your desktop.</span></span>
  
<span data-ttu-id="a632e-117">**Affichages OneNote**</span><span class="sxs-lookup"><span data-stu-id="a632e-117">**OneNote views**</span></span>

<span data-ttu-id="a632e-118">![Affichages de fenêtre OneNote] (media/ON15Con_views.jpg "Affichages de fenêtre OneNote")</span><span class="sxs-lookup"><span data-stu-id="a632e-118">![OneNote window views](media/ON15Con_views.jpg "OneNote window views")</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="a632e-119">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a632e-119">Interfaces</span></span>

<span data-ttu-id="a632e-120">Cette section répertorie les interfaces et les membres que vous pouvez utiliser pour modifier par programme les fenêtres OneNote.</span><span class="sxs-lookup"><span data-stu-id="a632e-120">This section lists the interfaces and members that you can use to modify OneNote windows programmatically.</span></span>
  
### <a name="windows-interface"></a><span data-ttu-id="a632e-121">Interface de Windows</span><span class="sxs-lookup"><span data-stu-id="a632e-121">Windows interface</span></span>

<span data-ttu-id="a632e-p105">L'interface **Windows** permet à l'utilisateur d'accéder à l'ensemble des fenêtres ouvertes de OneNote. Il s'agit d'une propriété de la classe **Application** OneNote, accédée via **Application.Windows**. Ce qui retourne l'ensemble énuméré des fenêtres OneNote.</span><span class="sxs-lookup"><span data-stu-id="a632e-p105">The **Windows** interface allows the user to access the set of opened OneNote windows. It is a property of the OneNote **Application** class, accessed through **Application.Windows**. This returns the enumerated set of OneNote windows.</span></span> 
  
<span data-ttu-id="a632e-125">**Propriétés**</span><span class="sxs-lookup"><span data-stu-id="a632e-125">**Properties**</span></span>

|<span data-ttu-id="a632e-126">**Name**</span><span class="sxs-lookup"><span data-stu-id="a632e-126">**Name**</span></span>|<span data-ttu-id="a632e-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="a632e-127">**Type**</span></span>|<span data-ttu-id="a632e-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="a632e-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a632e-129">**Count**</span><span class="sxs-lookup"><span data-stu-id="a632e-129">**Count**</span></span> <br/> |<span data-ttu-id="a632e-130">ulong</span><span class="sxs-lookup"><span data-stu-id="a632e-130">ulong</span></span>  <br/> |<span data-ttu-id="a632e-131">Obtient le nombre d'objets de **Window** dans le jeu de **Windows**.</span><span class="sxs-lookup"><span data-stu-id="a632e-131">Gets the number of **Window** objects in the **Windows** set.</span></span>  <br/> |
|<span data-ttu-id="a632e-132">**CurrentWindow**</span><span class="sxs-lookup"><span data-stu-id="a632e-132">**CurrentWindow**</span></span> <br/> |<span data-ttu-id="a632e-133">**Window**</span><span class="sxs-lookup"><span data-stu-id="a632e-133">**Window**</span></span> <br/> |<span data-ttu-id="a632e-134">Obtient l'objet **Window** de la fenêtre OneNote active.</span><span class="sxs-lookup"><span data-stu-id="a632e-134">Gets the **Window** object of the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="a632e-135">**Items**</span><span class="sxs-lookup"><span data-stu-id="a632e-135">**Items**</span></span> <br/> |<span data-ttu-id="a632e-136">**Window**</span><span class="sxs-lookup"><span data-stu-id="a632e-136">**Window**</span></span> <br/> |<span data-ttu-id="a632e-p106">Renvoie l'objet **Window** qui correspond à la valeur d'index transmise. Cette propriété n'est pas accessible directement. Pour renvoyer un objet **Window**, utilisez **Windows [(uint) index]**. </span><span class="sxs-lookup"><span data-stu-id="a632e-p106">Returns the **Window** object that corresponds to the index value passed. This property cannot be accessed directly. To return a **Window** object, use **Windows [(uint) index]**.  </span></span><br/> |
   
### <a name="window-interface"></a><span data-ttu-id="a632e-140">Interface de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="a632e-140">Window interface</span></span>

<span data-ttu-id="a632e-p107">L'interface **Window** permet à l'utilisateur d'accéder à certaines propriétés de chaque fenêtre. Chaque fenêtre OneNote est accessible par l'énumération par le biais de la propriété **Windows** de la classe **Application**.</span><span class="sxs-lookup"><span data-stu-id="a632e-p107">The **Window** interface allows the user to access certain properties of each window. Each OneNote window can be accessed by enumerating through the **Windows** property of the **Application** class.</span></span> 
  
<span data-ttu-id="a632e-143">**Propriétés**</span><span class="sxs-lookup"><span data-stu-id="a632e-143">**Properties**</span></span>

|<span data-ttu-id="a632e-144">**Name**</span><span class="sxs-lookup"><span data-stu-id="a632e-144">**Name**</span></span>|<span data-ttu-id="a632e-145">**Type**</span><span class="sxs-lookup"><span data-stu-id="a632e-145">**Type**</span></span>|<span data-ttu-id="a632e-146">**Description**</span><span class="sxs-lookup"><span data-stu-id="a632e-146">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a632e-147">**Active**</span><span class="sxs-lookup"><span data-stu-id="a632e-147">**Active**</span></span> <br/> |<span data-ttu-id="a632e-148">bool</span><span class="sxs-lookup"><span data-stu-id="a632e-148">bool</span></span>  <br/> |<span data-ttu-id="a632e-149">Obtient ou définit une valeur qui indique si la fenêtre est la fenêtre active de OneNote.</span><span class="sxs-lookup"><span data-stu-id="a632e-149">Gets or sets a value that indicates whether the window is the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="a632e-150">**Application**</span><span class="sxs-lookup"><span data-stu-id="a632e-150">**Application**</span></span> <br/> |<span data-ttu-id="a632e-151">**Application**</span><span class="sxs-lookup"><span data-stu-id="a632e-151">**Application**</span></span> <br/> |<span data-ttu-id="a632e-152">Obtient l'objet **Application** OneNote qui est associé à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a632e-152">Gets the OneNote **Application** object that is associated with the window.</span></span>  <br/> |
|<span data-ttu-id="a632e-153">**CurrentPageId**</span><span class="sxs-lookup"><span data-stu-id="a632e-153">**CurrentPageId**</span></span> <br/> |<span data-ttu-id="a632e-154">string</span><span class="sxs-lookup"><span data-stu-id="a632e-154">string</span></span>  <br/> |<span data-ttu-id="a632e-155">Obtient l'ID d'objet de la page OneNote active de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a632e-155">Gets the object ID of the active OneNote page of the window.</span></span>  <br/> |
|<span data-ttu-id="a632e-156">**CurrentSectionId**</span><span class="sxs-lookup"><span data-stu-id="a632e-156">**CurrentSectionId**</span></span> <br/> |<span data-ttu-id="a632e-157">string</span><span class="sxs-lookup"><span data-stu-id="a632e-157">string</span></span>  <br/> |<span data-ttu-id="a632e-158">Obtient l'ID d'objet de la section OneNote active de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a632e-158">Gets the object ID of the active OneNote section of the window.</span></span>  <br/> |
|<span data-ttu-id="a632e-159">**CurrentSectionGroupId**</span><span class="sxs-lookup"><span data-stu-id="a632e-159">**CurrentSectionGroupId**</span></span> <br/> |<span data-ttu-id="a632e-160">string</span><span class="sxs-lookup"><span data-stu-id="a632e-160">string</span></span>  <br/> |<span data-ttu-id="a632e-161">Obtient l'ID d'objet du groupe de section OneNote active de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a632e-161">Gets the object ID of the active OneNote section group of the window.</span></span>  <br/> |
|<span data-ttu-id="a632e-162">**CurrentNotebookId**</span><span class="sxs-lookup"><span data-stu-id="a632e-162">**CurrentNotebookId**</span></span> <br/> |<span data-ttu-id="a632e-163">string</span><span class="sxs-lookup"><span data-stu-id="a632e-163">string</span></span>  <br/> |<span data-ttu-id="a632e-164">Obtient l'ID d'objet du bloc-notes OneNote actif de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a632e-164">Gets the object ID of the active OneNote notebook of the window.</span></span>  <br/> |
|<span data-ttu-id="a632e-165">**DockedLocation**</span><span class="sxs-lookup"><span data-stu-id="a632e-165">**DockedLocation**</span></span> <br/> |<span data-ttu-id="a632e-166">**DockedLocation**</span><span class="sxs-lookup"><span data-stu-id="a632e-166">**DockedLocation**</span></span> <br/> |<span data-ttu-id="a632e-167">Obtient ou définit l'emplacement d'ancrage de la fenêtre OneNote.</span><span class="sxs-lookup"><span data-stu-id="a632e-167">Gets or sets the docked location of the OneNote window.</span></span>  <br/> |
|<span data-ttu-id="a632e-168">**FullPageView**</span><span class="sxs-lookup"><span data-stu-id="a632e-168">**FullPageView**</span></span> <br/> |<span data-ttu-id="a632e-169">bool</span><span class="sxs-lookup"><span data-stu-id="a632e-169">bool</span></span>  <br/> |<span data-ttu-id="a632e-170">Obtient ou définit une valeur qui indique si la fenêtre est en mode Page entière (affichage de l'interface utilisateur minimale).</span><span class="sxs-lookup"><span data-stu-id="a632e-170">Gets or sets a value that indicates whether the window is in Full Page view (minimal UI view).</span></span>  <br/> |
|<span data-ttu-id="a632e-171">**SideNote**</span><span class="sxs-lookup"><span data-stu-id="a632e-171">**SideNote**</span></span> <br/> |<span data-ttu-id="a632e-172">bool</span><span class="sxs-lookup"><span data-stu-id="a632e-172">bool</span></span>  <br/> |<span data-ttu-id="a632e-173">Obtient ou définit une valeur qui indique si la fenêtre est une fenêtre de note rapide.</span><span class="sxs-lookup"><span data-stu-id="a632e-173">Gets or sets a value that indicates whether the window is a quick note window.</span></span>  <br/> |
|<span data-ttu-id="a632e-174">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="a632e-174">**WindowHandle**</span></span> <br/> |<span data-ttu-id="a632e-175">ulong</span><span class="sxs-lookup"><span data-stu-id="a632e-175">ulong</span></span>  <br/> |<span data-ttu-id="a632e-176">Obtient l'ID de handle de la fenêtre OneNote.</span><span class="sxs-lookup"><span data-stu-id="a632e-176">Gets the handle ID of the OneNote window.</span></span>  <br/> |
   
<span data-ttu-id="a632e-177">**Méthodes**</span><span class="sxs-lookup"><span data-stu-id="a632e-177">**Methods**</span></span>
  
<span data-ttu-id="a632e-178">Vous pouvez utiliser les méthodes suivantes de l'interface **Window** pour naviguer vers les objets spécifiés dans la fenêtre OneNote ou à l'URL spécifiées.</span><span class="sxs-lookup"><span data-stu-id="a632e-178">You can use the following methods of the **Window** interface to navigate to specified objects in the OneNote window or to specified URLs.</span></span> 
  
<span data-ttu-id="a632e-179">**NavigateTo**</span><span class="sxs-lookup"><span data-stu-id="a632e-179">**NavigateTo**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a632e-180">**Description**</span><span class="sxs-lookup"><span data-stu-id="a632e-180">**Description**</span></span> <br/> |<span data-ttu-id="a632e-p108">Accède à l'objet spécifié dans la fenêtre OneNote. Par exemple, vous pouvez naviguer vers des sections, des pages et des éléments du plan au sein de pages.</span><span class="sxs-lookup"><span data-stu-id="a632e-p108">Navigates to the specified object in the OneNote window. For example, you can navigate to sections, pages, and outline elements within pages.</span></span>  <br/> |
|<span data-ttu-id="a632e-183">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="a632e-183">**Syntax**</span></span> <br/> | <span data-ttu-id="a632e-184">`HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); `</span><span class="sxs-lookup"><span data-stu-id="a632e-184"></span></span> <br/> |
|<span data-ttu-id="a632e-185">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="a632e-185">**Parameters**</span></span> <br/> | <span data-ttu-id="a632e-p109">_bstrHierarchyObjectID_ la hiérarchie OneNote des ID de l'objet que vous voulez atteindre. L'ID d'objet peut faire référence à un bloc-notes OneNote, section, le groupe de section ou page. </span><span class="sxs-lookup"><span data-stu-id="a632e-p109">_bstrHierarchyObjectID_—The hierarchy OneNote ID of the object you want to navigate to. The object ID can reference a OneNote notebook, section, section group, or page.  </span></span><br/>  <span data-ttu-id="a632e-p110">_bstrObjectID_ l'ID de OneNote de l'objet spécifique à accéder à l'intérieur d'une page OneNote. Si l'utilisateur ne souhaite pas d'accéder à un objet spécifique dans une page, ce paramètre est défini sur null. </span><span class="sxs-lookup"><span data-stu-id="a632e-p110">_bstrObjectID_—The OneNote ID of the specific object to navigate to within a OneNote page. If the user does not want to navigate to a specific object on a page, this parameter is set to null.  </span></span><br/> |
   
<span data-ttu-id="a632e-190">**NavigateToUrl**</span><span class="sxs-lookup"><span data-stu-id="a632e-190">**NavigateToUrl**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a632e-191">**Description**</span><span class="sxs-lookup"><span data-stu-id="a632e-191">**Description**</span></span> <br/> |<span data-ttu-id="a632e-p111">Si passé un lien OneNote (onenote: / /), ouvre la fenêtre OneNote à l'emplacement correspondant dans OneNote. Toutefois, si le lien est un lien externe, tel que http:// ou file://, une boîte de dialogue de sécurité s'affiche. Après le renvoi, OneNote essaie d'ouvrir la liaison et une erreur HResult.hrObjectDoesNotExist est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="a632e-p111">If passed a OneNote link (onenote://), opens the OneNote window to the corresponding location in OneNote. However, if the link is an external link, such as http:// or file://, a security dialog box will appear. Upon dismissal, OneNote attempts to open up the link and an HResult.hrObjectDoesNotExist error is returned.</span></span>  <br/> |
|<span data-ttu-id="a632e-195">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="a632e-195">**Syntax**</span></span> <br/> | <span data-ttu-id="a632e-196">`HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); `</span><span class="sxs-lookup"><span data-stu-id="a632e-196"></span></span> <br/> |
|<span data-ttu-id="a632e-197">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="a632e-197">**Parameters**</span></span> <br/> | <span data-ttu-id="a632e-198">_bstrUrl_ l'URL à atteindre.</span><span class="sxs-lookup"><span data-stu-id="a632e-198">_bstrUrl_—The URL to navigate to.</span></span>  <br/> |
   
<span data-ttu-id="a632e-199">**SetDockedLocation**</span><span class="sxs-lookup"><span data-stu-id="a632e-199">**SetDockedLocation**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a632e-200">**Description**</span><span class="sxs-lookup"><span data-stu-id="a632e-200">**Description**</span></span> <br/> |<span data-ttu-id="a632e-201">Ancre la fenêtre à l'emplacement spécifié par **dockLocation** et le moniteur au **ptMonitor**.</span><span class="sxs-lookup"><span data-stu-id="a632e-201">Docks the window to the location specified by **dockLocation** and the monitor at **ptMonitor**.</span></span>  <br/> |
|<span data-ttu-id="a632e-202">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="a632e-202">**Syntax**</span></span> <br/> | <span data-ttu-id="a632e-203">`HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);`</span><span class="sxs-lookup"><span data-stu-id="a632e-203"></span></span> <br/> |
|<span data-ttu-id="a632e-204">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="a632e-204">**Parameters**</span></span> <br/> | <span data-ttu-id="a632e-205">_dockLocation_ - indique l'emplacement d'ancrage d'une fenêtre OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="a632e-205">_dockLocation_ - Indicates the docked location of a OneNote 2013 window.</span></span>  <br/>  <span data-ttu-id="a632e-206">_ptMonitor_ - indique (facultatif) dans x, y coordonnées dont la fenêtre de surveillance doit être ancré dans.</span><span class="sxs-lookup"><span data-stu-id="a632e-206">_ptMonitor_ - (Optional) Indicates in x,y co-ordinates which monitor the window should be docked to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="a632e-207">Exemple</span><span class="sxs-lookup"><span data-stu-id="a632e-207">Example</span></span>

<span data-ttu-id="a632e-p112">Le code suivant effectue une itération dans les fenêtres OneNote pour rechercher une fenêtre fixe. Si aucune fenêtre ancrée n'existe, l'exemple ancre la fenêtre active. Si aucune fenêtre active n'existe, le code crée une nouvelle fenêtre ancrée.</span><span class="sxs-lookup"><span data-stu-id="a632e-p112">The following code iterates through the OneNote windows to find a docked window. If no docked window exists, the example docks the active window. If no active window exists, the code creates a new docked window.</span></span>
  
```cs
using System;
using System.Diagnostics;
using Microsoft.Office.Interop.OneNote;
namespace SampleWND
{
    class DockOneNoteWindow
    {
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = new Microsoft.Office.Interop.OneNote.Application();
            // Search through all OneNote windows for a docked window and activate it.
            bool foundDockedWND = false;
            for (int i = 0; i < app.Windows.Count; i++)
            {
                if (app.Windows[(uint) i].DockedLocation != DockLocation.dlNone)
                {
                    foundDockedWND = true;
                    app.Windows[(uint) i].Active = true;
                }
            }
            
            // If no docked window exists, dock the active window.
            if (!foundDockedWND && (app.Windows.Count > 0))
                app.Windows.CurrentWindow.DockedLocation = DockLocation.dlDefault;
            // If no active window exists, create a new docked window.
            if (app.Windows.Count < 1)
            {
                Process oneProc = new Process();
                oneProc.StartInfo.FileName = "onenote.exe";
                oneProc.StartInfo.Arguments = "/docked";
                oneProc.Start();
            }
        }
    }
}

```

## <a name="see-also"></a><span data-ttu-id="a632e-211">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a632e-211">See also</span></span>

- [<span data-ttu-id="a632e-212">Référence du développeur OneNote</span><span class="sxs-lookup"><span data-stu-id="a632e-212">OneNote developer reference</span></span>](onenote-developer-reference.md)

