---
title: Rapides interfaces boîte de dialogue remplissage (OneNote 2013)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: Cette rubrique décrit les interfaces que vous pouvez utiliser pour personnaliser par programme la boîte de dialogue classement rapide dans OneNote 2013.
ms.openlocfilehash: dd6b28ae6cb2acb007bae26ea661facaf1f8d4be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425336"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a><span data-ttu-id="53999-103">Rapides interfaces boîte de dialogue remplissage (OneNote 2013)</span><span class="sxs-lookup"><span data-stu-id="53999-103">Quick Filing dialog box interfaces (OneNote)</span></span>

<span data-ttu-id="53999-104">Cette rubrique décrit les interfaces que vous pouvez utiliser pour personnaliser par programme la boîte de dialogue classement rapide dans OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="53999-104">This topic describes the interfaces that you can use to programmatically customize the Quick Filing dialog box in OneNote 2013.</span></span>
  
## <a name="quick-filing-dialog-box"></a><span data-ttu-id="53999-105">Boîte de dialogue Classement rapide</span><span class="sxs-lookup"><span data-stu-id="53999-105">Quick Filing dialog box</span></span>

<span data-ttu-id="53999-p101">La boîte de dialogue classement rapide dans OneNote 2013 est une boîte de dialogue personnalisable qui permet aux utilisateurs de sélectionner un emplacement au sein de la structure de la hiérarchie OneNote. Emplacements sélectionnables incluent les ordinateurs portables, les groupes de sections, sections, pages et des sous-pages. La boîte de dialogue est utilisée au sein de l'application OneNote et par des applications externes par le biais de l'API OneNote 2013. La figure 1 montre la boîte de dialogue classement rapide dans son état par défaut.</span><span class="sxs-lookup"><span data-stu-id="53999-p101">The Quick Filing dialog box in OneNote 2013 is a customizable dialog box that allows users to select a location within the OneNote hierarchy structure. Selectable locations include notebooks, section groups, sections, pages, and subpages. The dialog box is used both within the OneNote application and by external applications through the OneNote 2013 API. Figure 1 shows the Quick Filing dialog box in its default state.</span></span>
  
<span data-ttu-id="53999-110">**La figure 1. Boîte de dialogue Remplissage rapide sans personnalisations**</span><span class="sxs-lookup"><span data-stu-id="53999-110">**Figure 1. Quick Filing dialog box without customizations**</span></span>

<span data-ttu-id="53999-111">![Boîte de dialogue Classement rapide sans boîte]de dialogue Classement rapide sans(media/ON15Con_quick_filing_dialog.jpg "personnalisations")</span><span class="sxs-lookup"><span data-stu-id="53999-111">![Quick Filing dialog box without customizations](media/ON15Con_quick_filing_dialog.jpg "Quick Filing dialog box without customizations")</span></span>
  
<span data-ttu-id="53999-p102">Dans la boîte de dialogue, les utilisateurs peuvent parcourir la hiérarchie de tous les ordinateurs portables pour rechercher les emplacements spécifiques ou rechercher dans la structure d'arborescence OneNote en tapant dans la zone de texte. Aspects de la boîte de dialogue qui peuvent être personnalisés incluent le titre, description, récente liste des résultats, texte de la case à cocher État, profondeur de l'arborescence, boutons et des types d'emplacements sélectionnable.</span><span class="sxs-lookup"><span data-stu-id="53999-p102">Within the dialog box, users can navigate the All Notebooks hierarchy to look for specific locations or search the OneNote tree structure by typing into the text box. Aspects of the dialog box that can be customized include the title, description, recent results list, check box text and state, tree depth, buttons, and selectable location types.</span></span>

<span data-ttu-id="53999-p103">Vous pouvez accéder à la fonctionnalité de boîte de dialogue classement rapide via deux interfaces OneNote 2013. L'interface **IQuickFilingDialog** permet aux utilisateurs d'instancier, configurer et exécuter la boîte de dialogue. L'interface **IQuickFilingDialogCallback** est appelé après la fermeture de la boîte de dialogue. La boîte de dialogue est exécutée dans le processus de OneNote, un mécanisme n'est nécessaire pour conserver un thread de la boîte de dialogue en cours d'exécution, puis pour capturer la sélection de l'utilisateur et l'état de la boîte de dialogue lors de sa fermeture.</span><span class="sxs-lookup"><span data-stu-id="53999-p103">You can access the Quick Filing dialog box functionality through two OneNote 2013 interfaces. The **IQuickFilingDialog** interface allows users to instantiate, set up, and run the dialog box. The **IQuickFilingDialogCallback** interface is called after the dialog box is closed. The dialog box is run in the OneNote process, so a mechanism is needed to keep the dialog box's thread running and then to capture the user's selection and the state of the dialog box when it is closed.</span></span> 
  
## <a name="iquickfilingdialog-interface"></a><span data-ttu-id="53999-118">Interface IQuickFilingDialog</span><span class="sxs-lookup"><span data-stu-id="53999-118">IQuickFilingDialog interface</span></span>
<span data-ttu-id="53999-119"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="53999-119"><a name="odc_IQuickFilingDialog"> </a></span></span>

<span data-ttu-id="53999-p104">Cette interface autorise l'utilisateur à personnaliser et exécuter la boîte de dialogue. L'utilisateur peut instancier une boîte de dialogue par le biais de la classe **Application** à l'aide de la méthode **Application.QuickFilingDialog**. La méthode retourne une instance de la boîte de dialogue. Une fois que les propriétés de la boîte de dialogue sont définies, la méthode **IQuickFilingDialog.Run** est utilisée pour exécuter la boîte de dialogue. Cette méthode exécute la boîte de dialogue sur un nouveau thread.</span><span class="sxs-lookup"><span data-stu-id="53999-p104">This interface allows the user to customize and run the dialog box. The user can instantiate a dialog box through the **Application** class by using the **Application.QuickFilingDialog** method. The method returns an instance of the dialog box. Once the properties of the dialog box are set, the **IQuickFilingDialog.Run** method is used to run the dialog box. This method runs the dialog box on a new thread.</span></span> 
  
<span data-ttu-id="53999-125">**Propriétés**</span><span class="sxs-lookup"><span data-stu-id="53999-125">**Properties**</span></span>

|<span data-ttu-id="53999-126">**Name**</span><span class="sxs-lookup"><span data-stu-id="53999-126">**Name**</span></span>|<span data-ttu-id="53999-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="53999-127">**Type**</span></span>|<span data-ttu-id="53999-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="53999-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="53999-129">**Title**</span><span class="sxs-lookup"><span data-stu-id="53999-129">**Title**</span></span> <br/> |<span data-ttu-id="53999-130">string</span><span class="sxs-lookup"><span data-stu-id="53999-130">string</span></span>  <br/> |<span data-ttu-id="53999-131">Obtient ou définit le texte du titre qui s'affiche dans la barre de titre de la fenêtre de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="53999-131">Gets or sets the title text that appears in the title bar of the dialog box window.</span></span>  <br/> |
|<span data-ttu-id="53999-132">**Description**</span><span class="sxs-lookup"><span data-stu-id="53999-132">**Description**</span></span> <br/> |<span data-ttu-id="53999-133">string</span><span class="sxs-lookup"><span data-stu-id="53999-133">string</span></span>  <br/> |<span data-ttu-id="53999-p105">Obtient ou définit la description de texte pour indiquer à l'utilisateur sur les éléments à sélectionner. Cette valeur peut être texte multiligne.</span><span class="sxs-lookup"><span data-stu-id="53999-p105">Gets or sets the text description to instruct the user about what to select. This value can be multiple-line text.</span></span>  <br/> |
|<span data-ttu-id="53999-136">**CheckboxText**</span><span class="sxs-lookup"><span data-stu-id="53999-136">**CheckboxText**</span></span> <br/> |<span data-ttu-id="53999-137">string</span><span class="sxs-lookup"><span data-stu-id="53999-137">string</span></span>  <br/> |<span data-ttu-id="53999-p106">Obtient ou définit le texte qui suit la case à cocher. Si cette valeur est définie sur une chaîne non vide, une case à cocher apparaît dans la boîte de dialogue. Si la valeur est une chaîne vide, aucune case à cocher s'affiche.</span><span class="sxs-lookup"><span data-stu-id="53999-p106">Gets or sets the text that follows the check box. If this value is set to a non-empty string, a check box appears in the dialog box. If the value is an empty string, no check box appears.</span></span>  <br/> |
|<span data-ttu-id="53999-141">**CheckboxState**</span><span class="sxs-lookup"><span data-stu-id="53999-141">**CheckboxState**</span></span> <br/> |<span data-ttu-id="53999-142">bool</span><span class="sxs-lookup"><span data-stu-id="53999-142">bool</span></span>  <br/> |<span data-ttu-id="53999-p107">Obtient ou définit l'état de la case à cocher. Si la valeur est définie sur **false**, la case à cocher est désactivée au démarrage de la boîte de dialogue. Si la valeur est définie sur **true**, la case à cocher est activée lorsque la boîte de dialogue est démarrée en tant que **CheckboxText** est une chaîne vide.  </span><span class="sxs-lookup"><span data-stu-id="53999-p107">Gets or sets the state of the check box. If value is set to **false**, the check box is cleared when the dialog box is started. If the value is set to **true**, the check box is selected when the dialog box is started as long as **CheckboxText** is a non-empty string.  </span></span><br/> |
|<span data-ttu-id="53999-146">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="53999-146">**WindowHandle**</span></span> <br/> |<span data-ttu-id="53999-147">ulong</span><span class="sxs-lookup"><span data-stu-id="53999-147">ulong</span></span>  <br/> |<span data-ttu-id="53999-148">Obtient l'ID de handle de la fenêtre de boîte de dialogue classement rapide.</span><span class="sxs-lookup"><span data-stu-id="53999-148">Gets the handle ID of the Quick Filing dialog box window.</span></span>  <br/> |
|<span data-ttu-id="53999-149">**TreeDepth**</span><span class="sxs-lookup"><span data-stu-id="53999-149">**TreeDepth**</span></span> <br/> |<span data-ttu-id="53999-150">**HierarchyElement**</span><span class="sxs-lookup"><span data-stu-id="53999-150">**HierarchyElement**</span></span> <br/> |<span data-ttu-id="53999-p108">Obtient ou définit la profondeur l'arborescence OneNote doit être affiché dans la section tous les ordinateurs portables. Par défaut, l'arborescence est affichée aux sections. Cette propriété n'affecte pas le type d'éléments peut être sélectionné. </span><span class="sxs-lookup"><span data-stu-id="53999-p108">Gets or sets how deep the OneNote tree should be displayed in the All Notebooks section. By default, the tree is displayed up to the sections. This property does not affect what type of elements can be selected.  </span></span><br/> <span data-ttu-id="53999-p109">Si **TreeDepth** est défini sur un élément plus bas dans la hiérarchie OneNote que peuvent être sélectionnés par un des boutons, la profondeur de l'arborescence affichée sera l'élément sélectionnable possible la plus faible. En d'autres termes, si la profondeur de l'arborescence est définie à afficher aux pages, mais l'élément sélectionnable le plus bas est une section, l'arborescence est affichée aux sections.  </span><span class="sxs-lookup"><span data-stu-id="53999-p109">If **TreeDepth** is set to an element lower in the OneNote hierarchy than can be selected by any of the buttons, the displayed tree depth will be the lowest possible selectable element. That is, if tree depth is set to display down to pages, but the lowest selectable element is a section, the tree is displayed down to sections.  </span></span><br/> |
|<span data-ttu-id="53999-156">**ParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="53999-156">**ParentWindowHandle**</span></span> <br/> |<span data-ttu-id="53999-157">ulong</span><span class="sxs-lookup"><span data-stu-id="53999-157">ulong</span></span>  <br/> |<span data-ttu-id="53999-p110">Obtient ou définit l'ID du handle de la fenêtre parente de la boîte de dialogue. Si cette propriété est définie, la boîte de dialogue classement rapide sera modale par rapport à la fenêtre parent affecté lorsque la boîte de dialogue s'ouvre. En d'autres termes, un utilisateur ne sera pas en mesure d'accéder à la fenêtre parent jusqu'à la fermeture de la boîte de dialogue classement rapide.</span><span class="sxs-lookup"><span data-stu-id="53999-p110">Gets or sets the handle ID of the parent window of the dialog box. If this property is set, the Quick Filing dialog box will be modal to the assigned parent window when the dialog box opens. That is, a user will not be able to access the parent window until the Quick Filing dialog box is closed.</span></span>  <br/> |
|<span data-ttu-id="53999-161">**Position**</span><span class="sxs-lookup"><span data-stu-id="53999-161">**Position**</span></span> <br/> |<span data-ttu-id="53999-162">tagPOINT</span><span class="sxs-lookup"><span data-stu-id="53999-162">tagPOINT</span></span>  <br/> |<span data-ttu-id="53999-p111">Obtient ou définit la position de la fenêtre par rapport à l'écran. Par défaut, la boîte de dialogue s'affiche au milieu de la fenêtre parent ou le bureau.</span><span class="sxs-lookup"><span data-stu-id="53999-p111">Gets or sets the position of the window in relation to the screen. By default, the dialog box appears in the middle of the parent window or the desktop.</span></span>  <br/> |
|<span data-ttu-id="53999-165">**SelectedItem**</span><span class="sxs-lookup"><span data-stu-id="53999-165">**SelectedItem**</span></span> <br/> |<span data-ttu-id="53999-166">string</span><span class="sxs-lookup"><span data-stu-id="53999-166">string</span></span>  <br/> |<span data-ttu-id="53999-p112">Obtient l'ID d'objet de l'emplacement de OneNote sélectionnée par l'utilisateur lors de la fermeture de la boîte de dialogue. Si l'utilisateur clique sur le bouton **Annuler**, l'objet est définie sur null. </span><span class="sxs-lookup"><span data-stu-id="53999-p112">Gets the object ID of the OneNote location selected by the user when the dialog box is closed. If the user clicks the **Cancel** button, the object is set to null.  </span></span><br/> |
|<span data-ttu-id="53999-169">**PressedButton**</span><span class="sxs-lookup"><span data-stu-id="53999-169">**PressedButton**</span></span> <br/> |<span data-ttu-id="53999-170">ulong</span><span class="sxs-lookup"><span data-stu-id="53999-170">ulong</span></span>  <br/> |<span data-ttu-id="53999-p113">Obtient quel bouton a été utilisé lors de la fermeture de la boîte de dialogue. Si l'utilisateur a cliqué sur le bouton **Annuler**, cette propriété renvoie la valeur -1. Tous les autres boutons sont affectées des valeurs entières à partir de 0, est incrémentée de 1 pour chaque bouton ajouté à la boîte de dialogue. La valeur entière du bouton **OK** par défaut est 0.  </span><span class="sxs-lookup"><span data-stu-id="53999-p113">Gets which button was clicked when the dialog box was closed. If the **Cancel** button was clicked, this property returns a value of -1. All other buttons are assigned integer values from 0, incremented by 1 for each button added to the dialog box. The integer value of the default **OK** button is 0.  </span></span><br/> |
   
### <a name="methods"></a><span data-ttu-id="53999-175">Méthodes</span><span class="sxs-lookup"><span data-stu-id="53999-175">Methods</span></span>

<span data-ttu-id="53999-176">**SetRecentResults**</span><span class="sxs-lookup"><span data-stu-id="53999-176">**SetRecentResults**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53999-177">**Description**</span><span class="sxs-lookup"><span data-stu-id="53999-177">**Description**</span></span> <br/> |<span data-ttu-id="53999-p114">Définit quelle liste résultats récents s'affichera dans la boîte de dialogue classement rapide et indique s'il faut inclure certains emplacements spéciaux classement dans la liste. Les utilisateurs peuvent sélectionner une liste de résultats récents à partir de l'énumération [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) . Les utilisateurs peuvent également choisir d'ajouter les options suivantes à la liste : Section en cours, Page en cours ou Notes non classées. Si **RecentResultType.rrtNone** est sélectionné, aucune liste de résultats récents n'est indiqué.  </span><span class="sxs-lookup"><span data-stu-id="53999-p114">Sets what recent result list will be displayed in the Quick Filing dialog box, and indicates whether to include some special filing locations in the list. Users can select a recent result list from the [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) enumeration. Users can also choose to add the following options to the list: Current Section, Current Page, or Unfiled Notes. If **RecentResultType.rrtNone** is selected, no recent result list is shown.  </span></span><br/> |
|<span data-ttu-id="53999-182">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="53999-182">**Syntax**</span></span> <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|<span data-ttu-id="53999-183">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="53999-183">**Parameters**</span></span> <br/> | <span data-ttu-id="53999-184">_recentResults_ &ndash; Objet de type **RecentResultType** qui indique la liste des résultats récents, le cas caser, qui doit apparaître.</span><span class="sxs-lookup"><span data-stu-id="53999-184">_recentResults_ &ndash; An object of type **RecentResultType** that indicates which recent result list, if any, should appear.</span></span> <span data-ttu-id="53999-185">Si **rrtNone** est sélectionné, aucune liste de résultats récents n'apparaît dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="53999-185">If **rrtNone** is selected, no recent result list appears in the dialog box.</span></span><br/><br/>  <span data-ttu-id="53999-186">_fShowCurrentSection_ &ndash; Valeur Boolean qui indique si la section actuelle doit être incluse dans la liste des résultats récents.</span><span class="sxs-lookup"><span data-stu-id="53999-186">_fShowCurrentSection_ &ndash; A Boolean value that indicates whether the current section should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="53999-187">_fShowCurrentPage_ &ndash; Valeur Boolean qui indique si la page actuelle doit être incluse dans la liste des résultats récents.</span><span class="sxs-lookup"><span data-stu-id="53999-187">_fShowCurrentPage_ &ndash; A Boolean value that indicates whether the current page should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="53999-188">_fShowUnfiledNotes_ &ndash; Valeur Boolean qui indique si la section Notes non filtrées doit être incluse dans la liste des résultats récents.</span><span class="sxs-lookup"><span data-stu-id="53999-188">_fShowUnfiledNotes_ &ndash; A Boolean value that indicates whether the Unfiled Notes section should be included in the recent result list.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="53999-p116">[!REMARQUE] Si un emplacement de la classification spéciaux ne peuvent pas être sélectionné à l'aide d'un des boutons dans la boîte de dialogue, il n'est pas affiché dans la liste. Si aucun élément sélectionnable dans la liste des résultats récents n'est trouvée, aucune liste de résultats récents ne s'affiche.</span><span class="sxs-lookup"><span data-stu-id="53999-p116">If a special filing location cannot be selected by using any of the buttons in the dialog box, it is not shown in the list. If no selectable item in the recent results list is found, no recent result list is displayed.</span></span> 
  
<span data-ttu-id="53999-191">L'exemple suivant utilise la méthode **SetRecentResults** pour afficher la section en cours, page en cours et la section Notes non classées dans la liste de résultats récents.</span><span class="sxs-lookup"><span data-stu-id="53999-191">The following example uses the **SetRecentResults** method to display the current section, current page, and the Unfiled Notes section in the recent result list.</span></span> 
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            ...
        }

```

<span data-ttu-id="53999-192">**AddButton**</span><span class="sxs-lookup"><span data-stu-id="53999-192">**AddButton**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53999-193">**Description**</span><span class="sxs-lookup"><span data-stu-id="53999-193">**Description**</span></span> <br/> |<span data-ttu-id="53999-p117">Permet aux utilisateurs d'ajouter et personnaliser des boutons dans la boîte de dialogue. Les utilisateurs peuvent spécifier le texte sur les boutons et les éléments de la hiérarchie de OneNote peuvent être sélectionnés par chaque bouton.</span><span class="sxs-lookup"><span data-stu-id="53999-p117">Allows users to add and customize buttons in the dialog box. Users can specify the text on the buttons and what elements of the OneNote hierarchy can be selected by each button.</span></span>  <br/> |
|<span data-ttu-id="53999-196">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="53999-196">**Syntax**</span></span> <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|<span data-ttu-id="53999-197">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="53999-197">**Parameters**</span></span> <br/> | <span data-ttu-id="53999-198">_bstrText_ &ndash; Chaîne qui spécifie le texte à apparaître sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="53999-198">_bstrText_ &ndash; A string that specifies the text to appear on the button.</span></span> <span data-ttu-id="53999-199">Pour personnaliser le bouton **OK** par défaut, passez une valeur null en tant que **bstrText**.</span><span class="sxs-lookup"><span data-stu-id="53999-199">To customize the default **OK** button, pass in a null value as **bstrText**.</span></span>  <br/><br/><span data-ttu-id="53999-200">_allowedElements_ &ndash; Élément **HierarchyElement** qui indique les éléments de hiérarchie en lecture OneNote qu’un utilisateur est autorisé à sélectionner à l’aide du bouton.</span><span class="sxs-lookup"><span data-stu-id="53999-200">_allowedElements_ &ndash; A **HierarchyElement** that indicates what non-read-only OneNote hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="53999-201">Pour sélectionner plusieurs éléments, l'utilisateur doit passer l'opérateur **OR** pour toutes les valeurs d'équivalente uint des types **HierarchyElement** autorisés comme un **HierarchyElement**.</span><span class="sxs-lookup"><span data-stu-id="53999-201">For selecting multiple items, the user should pass in the **OR** operator for all the uint equivalent values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="53999-202">_allowedReadOnlyElements_ &ndash; Élément **HierarchyElement** qui indique les éléments OneNote hiérarchie en lecture seule qu’un utilisateur est autorisé à sélectionner à l’aide du bouton.</span><span class="sxs-lookup"><span data-stu-id="53999-202">_allowedReadOnlyElements_ &ndash; A **HierarchyElement** that indicates what OneNote read-only hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="53999-203">Pour sélectionner plusieurs éléments, l'utilisateur doit passer l'opérateur **OR** pour toutes les valeurs d'équivalents **uint** des types **HierarchyElement** autorisés comme un **HierarchyElement**.</span><span class="sxs-lookup"><span data-stu-id="53999-203">For selecting multiple items, the user should pass in the **OR** operator for all the **uint** equivalents values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="53999-204">_fDefault_ &ndash; Valeur boolé américaine qui spécifie si ce bouton doit être le bouton par défaut.</span><span class="sxs-lookup"><span data-stu-id="53999-204">_fDefault_ &ndash; A Boolean value that specifies whether this button should be the default button.</span></span> <span data-ttu-id="53999-205">Si plusieurs boutons sont définis en tant que valeur par défaut, le bouton dernier spécifié devienne le bouton par défaut.</span><span class="sxs-lookup"><span data-stu-id="53999-205">If multiple buttons are set as default, the last specified button becomes the default button.</span></span>  <br/> |
   
<span data-ttu-id="53999-p122">L'exemple suivant ajoute trois boutons à la boîte de dialogue classement rapide. La première condition, **ensemble**, peut être sélectionnée par tous les éléments dans l'arborescence de la hiérarchie OneNote. Les autres, **les ordinateurs portables** et les **Pages**, peuvent être sélectionnés uniquement si leurs éléments correspondants, les ordinateurs portables et les Pages, sont sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="53999-p122">The following example adds three buttons to the Quick Filing dialog box. The first one, **All**, can be selected by all elements in the OneNote hierarchy tree. The others, **Notebooks** and **Pages**, can be selected only if their corresponding elements, Notebooks and Pages, are selected.</span></span>
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            ... 
        }

```

<span data-ttu-id="53999-209">**Run**</span><span class="sxs-lookup"><span data-stu-id="53999-209">**Run**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53999-210">**Description**</span><span class="sxs-lookup"><span data-stu-id="53999-210">**Description**</span></span> <br/> |<span data-ttu-id="53999-p123">Affiche la boîte de dialogue classement rapide à partir d'un thread. Elle accepte une référence à l'interface **IQuickFilingDialogCallback**, dont la méthode **OnDialogClosed** sera appelée une fois que la boîte de dialogue se ferme.  </span><span class="sxs-lookup"><span data-stu-id="53999-p123">Displays the Quick Filing dialog box from a new thread. It takes a reference to the **IQuickFilingDialogCallback** interface, whose **OnDialogClosed** method will be called once the dialog box closes.  </span></span><br/> |
|<span data-ttu-id="53999-213">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="53999-213">**Syntax**</span></span> <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|<span data-ttu-id="53999-214">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="53999-214">**Parameters**</span></span> <br/> | <span data-ttu-id="53999-215">_piCallback_ &ndash; Référence à l’interface **IQuickFilingDialogCallback** qui sera ins instantiée une fois la boîte de dialogue refermée.</span><span class="sxs-lookup"><span data-stu-id="53999-215">_piCallback_ &ndash; A reference to the **IQuickFilingDialogCallback** interface that will be instantiated once the dialog box closes.</span></span>  <br/> |
   
<span data-ttu-id="53999-216">L'exemple suivant utilise la méthode **Run** pour afficher la boîte de dialogue classement rapide à partir d'un thread.</span><span class="sxs-lookup"><span data-stu-id="53999-216">The following example uses the **Run** method to display the Quick Filing dialog box from a new thread.</span></span> 
  
```cs
    class OpenQuickFilingDialog
    {
            ... 
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            ... 
        }
    }

```

<span data-ttu-id="53999-217">**TreeCollapsedState**</span><span class="sxs-lookup"><span data-stu-id="53999-217">**TreeCollapsedState**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53999-218">**Description**</span><span class="sxs-lookup"><span data-stu-id="53999-218">**Description**</span></span> <br/> |<span data-ttu-id="53999-219">Indique si l'arborescence de la hiérarchie doit être développé ou réduit.</span><span class="sxs-lookup"><span data-stu-id="53999-219">Indicates whether the hierarchy tree should be expanded or collapsed.</span></span>  <br/> |
|<span data-ttu-id="53999-220">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="53999-220">**Syntax**</span></span> <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|<span data-ttu-id="53999-221">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="53999-221">**Parameters**</span></span> <br/> | <span data-ttu-id="53999-222">_tcs_ - Spécifie si l'arborescence est développée ou réduite.</span><span class="sxs-lookup"><span data-stu-id="53999-222">_tcs_ - Specifies whether the tree is expanded or collapsed.</span></span>  <br/> |
   
<span data-ttu-id="53999-223">**NotebookFilterOut**</span><span class="sxs-lookup"><span data-stu-id="53999-223">**NotebookFilterOut**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53999-224">**Description**</span><span class="sxs-lookup"><span data-stu-id="53999-224">**Description**</span></span> <br/> |<span data-ttu-id="53999-225">Filtre la liste des ordinateurs portables indiqué par type.</span><span class="sxs-lookup"><span data-stu-id="53999-225">Filters the list of notebooks shown by type.</span></span>  <br/> |
|<span data-ttu-id="53999-226">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="53999-226">**Syntax**</span></span> <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|<span data-ttu-id="53999-227">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="53999-227">**Parameters**</span></span> <br/> | <span data-ttu-id="53999-228">_nfo_ - Spécifie l'ensemble des ordinateurs portables qui doivent être filtrées en dehors de la liste</span><span class="sxs-lookup"><span data-stu-id="53999-228">_nfo_ - Specifies the set of notebooks that are to be filtered out of the list</span></span>  <br/> |
   
<span data-ttu-id="53999-229">**ShowCreateNewNotebook**</span><span class="sxs-lookup"><span data-stu-id="53999-229">**ShowCreateNewNotebook**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53999-230">**Description**</span><span class="sxs-lookup"><span data-stu-id="53999-230">**Description**</span></span> <br/> |<span data-ttu-id="53999-231">Affiche l'option créer un nouveau bloc-notes dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="53999-231">Displays the create new notebook option in the dialog.</span></span>  <br/> |
|<span data-ttu-id="53999-232">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="53999-232">**Syntax**</span></span> <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|<span data-ttu-id="53999-233">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="53999-233">**Parameters**</span></span> <br/> |<span data-ttu-id="53999-234">Aucune</span><span class="sxs-lookup"><span data-stu-id="53999-234">None</span></span>  <br/> |
   
<span data-ttu-id="53999-235">**AddInitialEditor**</span><span class="sxs-lookup"><span data-stu-id="53999-235">**AddInitialEditor**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53999-236">**Description**</span><span class="sxs-lookup"><span data-stu-id="53999-236">**Description**</span></span> <br/> |<span data-ttu-id="53999-237">Ajoute un utilisateur comme un éditeur initial dans un bloc-notes dans la boîte de dialogue classement rapide.</span><span class="sxs-lookup"><span data-stu-id="53999-237">Adds a user as an initial editor to a notebook in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="53999-238">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="53999-238">**Syntax**</span></span> <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|<span data-ttu-id="53999-239">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="53999-239">**Parameters**</span></span> <br/> | <span data-ttu-id="53999-p124">_initialEditor_ - adresse de messagerie de l'utilisateur que vous souhaitez ajouter en tant qu'éditeur dans le bloc-notes. Lorsque l'ordinateur portable est créé par le biais de la boîte de dialogue classement rapide, il est automatiquement partagé avec tous les éditeurs initiale.  </span><span class="sxs-lookup"><span data-stu-id="53999-p124">_initialEditor_ - The email address of the user you wish to add as an editor to the notebook. When the notebook is created via the Quick Filing dialog box, it is automatically shared with all Initial Editors.  </span></span><br/> |
   
<span data-ttu-id="53999-242">**ClearInitialEditors**</span><span class="sxs-lookup"><span data-stu-id="53999-242">**ClearInitialEditors**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53999-243">**Description**</span><span class="sxs-lookup"><span data-stu-id="53999-243">**Description**</span></span> <br/> |<span data-ttu-id="53999-244">Supprime tous les éditeurs initiales de la boîte de dialogue classement rapide.</span><span class="sxs-lookup"><span data-stu-id="53999-244">Removes all initial editors from the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="53999-245">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="53999-245">**Syntax**</span></span> <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|<span data-ttu-id="53999-246">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="53999-246">**Parameters**</span></span> <br/> |<span data-ttu-id="53999-247">Aucun</span><span class="sxs-lookup"><span data-stu-id="53999-247">None</span></span>  <br/> |
   
<span data-ttu-id="53999-248">**ShowSharingHyperlink**</span><span class="sxs-lookup"><span data-stu-id="53999-248">**ShowSharingHyperlink**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53999-249">**Description**</span><span class="sxs-lookup"><span data-stu-id="53999-249">**Description**</span></span> <br/> |<span data-ttu-id="53999-250">Afficher le lien hypertexte dans l'aide de partage dans la boîte de dialogue classement rapide.</span><span class="sxs-lookup"><span data-stu-id="53999-250">Displays the Sharing Help Topic Hyperlink in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="53999-251">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="53999-251">**Syntax**</span></span> <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|<span data-ttu-id="53999-252">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="53999-252">**Parameters**</span></span> <br/> |<span data-ttu-id="53999-253">Aucun</span><span class="sxs-lookup"><span data-stu-id="53999-253">None</span></span>  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a><span data-ttu-id="53999-254">Interface IQuickFilingDialogCallback</span><span class="sxs-lookup"><span data-stu-id="53999-254">IQuickFilingDialogCallback interface</span></span>
<span data-ttu-id="53999-255"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="53999-255"><a name="odc_IQuickFilingDialog"> </a></span></span>

<span data-ttu-id="53999-p125">Cette interface autorise l'utilisateur à accéder à la boîte de dialogue Propriétés après la fermeture de la boîte de dialogue. Une fois que la boîte de dialogue se ferme, OneNote 2013 appelle la méthode **IQuickFilingDialogCallback.OnDialogClose** dans cette interface.</span><span class="sxs-lookup"><span data-stu-id="53999-p125">This interface allows the user to access the dialog box properties after the dialog box closes. Once the dialog box closes, OneNote 2013 calls the **IQuickFilingDialogCallback.OnDialogClose** method in this interface.</span></span> 
  
<span data-ttu-id="53999-258">Une classe qui hérite de cette interface doit être défini.</span><span class="sxs-lookup"><span data-stu-id="53999-258">A class that inherits this interface has to be defined.</span></span>
  
### <a name="methods"></a><span data-ttu-id="53999-259">Méthodes</span><span class="sxs-lookup"><span data-stu-id="53999-259">Methods</span></span>

<span data-ttu-id="53999-260">La section suivante décrit les méthodes associées aux interfaces détaillées précédemment.</span><span class="sxs-lookup"><span data-stu-id="53999-260">The following section describes the methods associated with the interfaces detailed previously.</span></span>
  
<span data-ttu-id="53999-261">**OnDialogClosed**</span><span class="sxs-lookup"><span data-stu-id="53999-261">**OnDialogClosed**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53999-262">**Description**</span><span class="sxs-lookup"><span data-stu-id="53999-262">**Description**</span></span> <br/> |<span data-ttu-id="53999-p126">Permet aux utilisateurs d'ajouter des fonctionnalités permettant de capturer et utiliser la sélection de l'utilisateur à partir de la boîte de dialogue. Cette méthode est appelée après la fermeture de la boîte de dialogue classement rapide. Cette méthode est une fonction dont les interfaces **IQuickFilingDialogCallback** à définir.  </span><span class="sxs-lookup"><span data-stu-id="53999-p126">Enables users to add functionality to capture and use the user selection from the dialog box. This method is called after the Quick Filing dialog box is closed. This method is a function that **IQuickFilingDialogCallback** interfaces have to define.  </span></span><br/> |
|<span data-ttu-id="53999-266">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="53999-266">**Syntax**</span></span> <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|<span data-ttu-id="53999-267">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="53999-267">**Parameters**</span></span> <br/> | <span data-ttu-id="53999-268">_boîte de dialogue_ &ndash; Objet **IQuickFilingDialog** qui a appelé **la méthode OnDialogClose.**</span><span class="sxs-lookup"><span data-stu-id="53999-268">_dialog_ &ndash; The **IQuickFilingDialog** object that called the **OnDialogClose** method.</span></span>  <br/> |
   
<span data-ttu-id="53999-p127">L'exemple suivant est un exemple d'interface **IQuickFilingDialogCallback**. La méthode **OnDialogClose** imprime la sélection de l'utilisateur à partir de la boîte de dialogue classement rapide sur la console.</span><span class="sxs-lookup"><span data-stu-id="53999-p127">The following example is a sample **IQuickFilingDialogCallback** interface. The **OnDialogClose** method prints the user's selection from the Quick Filing dialog box to the console.</span></span> 
  
```cs
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }

```

## <a name="example"></a><span data-ttu-id="53999-271">Exemple</span><span class="sxs-lookup"><span data-stu-id="53999-271">Example</span></span>
<span data-ttu-id="53999-272"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="53999-272"><a name="odc_IQuickFilingDialog"> </a></span></span>

<span data-ttu-id="53999-p128">L'exemple de code suivant ouvre une boîte de dialogue classement rapide qui a un titre personnalisé, description, liste des derniers résultats, profondeur de l'arborescence, case à cocher et les boutons. L'utilisateur de l'élément, vous appuyez sur le bouton sélectionné et état de la case à cocher s'affiche dans une fenêtre de console lorsque la boîte de dialogue est fermée. Pour afficher le bouton de page activé, l'utilisateur aura rechercher une page et sélectionnez-le, car la profondeur de l'arborescence est fixée aux sections. La boîte de dialogue n'est pas un enfant de n'importe quelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="53999-p128">The following code example opens a Quick Filing dialog box that has a customized title, description, recent result list, tree depth, check box, and buttons. The user's selected item, pressed button, and check-box state will be displayed in a console window when the dialog box is closed. To see the page button enabled, the user will have to search for a page and select it, because the tree depth is set down to sections. The dialog box is not a child of any window.</span></span>
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using Microsoft.Office.Interop.OneNote;
namespace SampleQFD
{
    class OpenQuickFilingDialog
    {
        private static EventWaitHandle wh = new AutoResetEvent(false);
        private static IQuickFilingDialog qfDialog;
        private static String strTitle = "Sample Title";
        private static String strDescription = "Sample Description";
        private static String strCheckboxText = "Sample Checkbox";
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            // Instantiate Quick Filing UI
            qfDialog = app.QuickFiling();
            #region//SET API PARAMETERS
            // TITLE
            qfDialog.Title = strTitle;
            // DESCRIPTION
            qfDialog.Description = strDescription;
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            // TREE DEPTH
            qfDialog.TreeDepth = HierarchyElement.heSections;
            // CHECKBOX
            qfDialog.CheckboxText = strCheckboxText;
            qfDialog.CheckboxState = false;
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            // PARENTWINDOW
            #endregion
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            // Clean up and Wait so console window does not close
            qfDialog = null;
            wh.WaitOne();
        }
    }
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }
}

```

## <a name="see-also"></a><span data-ttu-id="53999-277">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53999-277">See also</span></span>

- [<span data-ttu-id="53999-278">Référence du développeur OneNote</span><span class="sxs-lookup"><span data-stu-id="53999-278">OneNote developer reference</span></span>](onenote-developer-reference.md)

