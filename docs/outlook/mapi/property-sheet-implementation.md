---
title: Implémentation de feuille de propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3f1c6497a182231645691f669d8900d33b495503
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430048"
---
# <a name="property-sheet-implementation"></a><span data-ttu-id="81526-103">Implémentation de feuille de propriétés</span><span class="sxs-lookup"><span data-stu-id="81526-103">Property Sheet Implementation</span></span>

  
  
<span data-ttu-id="81526-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81526-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81526-105">Une feuille de propriétés est une boîte de dialogue qui affiche les propriétés d’un objet.</span><span class="sxs-lookup"><span data-stu-id="81526-105">A property sheet is a dialog box for displaying the properties of an object.</span></span> <span data-ttu-id="81526-106">Les propriétés peuvent être en lecture seule, ce qui permet à l’utilisateur de les afficher uniquement, ou en lecture/écriture, ce qui lui permet d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="81526-106">The properties can be read-only, enabling the user only to view them, or read/write, enabling the user to make changes.</span></span> <span data-ttu-id="81526-107">Une feuille de propriétés contient une ou plusieurs fenêtres enfants superposées appelées pages.</span><span class="sxs-lookup"><span data-stu-id="81526-107">A property sheet contains one or more overlapping child windows called pages.</span></span> <span data-ttu-id="81526-108">Chaque page contient des fenêtres de contrôle pour définir un groupe de propriétés connexes.</span><span class="sxs-lookup"><span data-stu-id="81526-108">Each page contains control windows for setting a group of related properties.</span></span> <span data-ttu-id="81526-109">Les utilisateurs naviguent d’une page à l’autre en sélectionnant un onglet qui place la page correspondante au premier plan de la feuille des propriétés.</span><span class="sxs-lookup"><span data-stu-id="81526-109">Users navigate from page to page by selecting a tab that brings the corresponding page to the foreground of the property sheet.</span></span>
  
<span data-ttu-id="81526-110">Les fournisseurs de services doivent implémenter une feuille de propriétés qui affiche un ensemble minimal de propriétés liées à la configuration dans le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="81526-110">Service providers must implement a property sheet that displays a minimal set of properties related to configuration in the message service.</span></span> <span data-ttu-id="81526-111">Si vous autorisez la modification de ces propriétés de service de message, vous pouvez autoriser les utilisateurs d’applications clientes, telles que le Panneau de contrôle, à apporter les modifications ou à implémenter les modifications par programme.</span><span class="sxs-lookup"><span data-stu-id="81526-111">If you allow these message service properties to be changed, you can either allow users of client applications, such as the Control Panel, to make the changes or implement the changes programmatically.</span></span> <span data-ttu-id="81526-112">L’implémentation de feuilles de propriétés pour afficher et modifier d’autres types de propriétés est facultative.</span><span class="sxs-lookup"><span data-stu-id="81526-112">Implementing property sheets to display and edit other types of properties is optional.</span></span> 
  
<span data-ttu-id="81526-113">En règle générale, vous devez afficher une feuille de propriétés dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="81526-113">Typically, you will need to display a property sheet in the following situations:</span></span>
  
- <span data-ttu-id="81526-114">Lorsqu’un client appelle la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) de votre objet d’état.</span><span class="sxs-lookup"><span data-stu-id="81526-114">When a client calls your status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method.</span></span> 
    
- <span data-ttu-id="81526-115">Lorsque MAPI appelle la méthode d’accès de votre objet fournisseur.</span><span class="sxs-lookup"><span data-stu-id="81526-115">When MAPI calls your provider object's logon method.</span></span>
    
- <span data-ttu-id="81526-116">Lorsque MAPI appelle la fonction de point d’entrée pour le service de messagerie de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="81526-116">When MAPI calls the entry point function for your provider's message service.</span></span>
    
<span data-ttu-id="81526-117">Les fournisseurs de transport implémentent également des feuilles de propriétés pour afficher les propriétés liées aux options de message, et les fournisseurs de carnets d’adresses implémentent des feuilles de propriétés pour afficher et modifier des informations détaillées sur les utilisateurs de messagerie et les listes de distribution, les critères de recherche avancés et les modèles permettant d’entrer de nouveaux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="81526-117">Transport providers also implement property sheets to display properties related to message options, and address book providers implement property sheets to view and edit detailed information about messaging users and distribution lists, advanced search criteria, and templates for entering new users.</span></span>
  
<span data-ttu-id="81526-118">Vous pouvez utiliser l’une des trois techniques suivantes pour créer une feuille de propriétés :</span><span class="sxs-lookup"><span data-stu-id="81526-118">You can use one of the following three techniques to create a property sheet:</span></span>
  
- <span data-ttu-id="81526-119">Manuellement, comme vous le feriez pour n’importe quelle boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="81526-119">Manually, as you would any dialog box.</span></span>
    
- <span data-ttu-id="81526-120">À l’aide du contrôle commun de feuille de propriétés fourni dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="81526-120">By using the property sheet common control provided in the Windows SDK.</span></span>
    
- <span data-ttu-id="81526-121">À l’aide d’un tableau d’affichage MAPI.</span><span class="sxs-lookup"><span data-stu-id="81526-121">By using a MAPI display table.</span></span>
    
<span data-ttu-id="81526-122">Les fournisseurs doivent choisir la dernière option (créer une feuille de propriétés à l’aide d’un tableau d’affichage).</span><span class="sxs-lookup"><span data-stu-id="81526-122">Providers should choose the last option (create a property sheet by using a display table).</span></span> <span data-ttu-id="81526-123">Il s’agit de l’option la plus simple, car elle élimine la nécessité d’utiliser l’interface utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="81526-123">This is the simplest option because it eliminates the need to work with the Windows user interface.</span></span> 
  
<span data-ttu-id="81526-124">Pour implémenter une feuille de propriétés construite à partir d’un tableau d’affichage pour les propriétés de votre service de message, utilisez la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="81526-124">To implement a property sheet built from a display table for your message service properties, use the following procedure:</span></span>
  
1. <span data-ttu-id="81526-125">Appelez [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) pour ouvrir une section dans le profil actuel.</span><span class="sxs-lookup"><span data-stu-id="81526-125">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) to open a section in the current profile.</span></span> <span data-ttu-id="81526-126">Passez votre [MAPIUID](mapiuid.md) ou NULL pour ouvrir la section de profil de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="81526-126">Pass your [MAPIUID](mapiuid.md) or NULL to open your provider's profile section.</span></span> 
    
2. <span data-ttu-id="81526-127">Appelez [CreateIProp pour](createiprop.md) créer un objet de données de propriété.</span><span class="sxs-lookup"><span data-stu-id="81526-127">Call [CreateIProp](createiprop.md) to create a property data object.</span></span> 
    
3. <span data-ttu-id="81526-128">Appelez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) de la section de profil pour copier toutes les propriétés de la section dans l’objet de données de propriété.</span><span class="sxs-lookup"><span data-stu-id="81526-128">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy all of the section's properties to the property data object.</span></span> 
    
4. <span data-ttu-id="81526-129">Créez un tableau d’affichage en construisant une ou plusieurs structures [DTPAGE](dtpage.md) qui décrivent les contrôles à afficher dans la feuille des propriétés et en appelant la [fonction BuildDisplayTable,](builddisplaytable.md) ou en implémentant du code personnalisé.</span><span class="sxs-lookup"><span data-stu-id="81526-129">Create a display table either by building one or more [DTPAGE](dtpage.md) structures that describe the controls to appear on the property sheet and calling the [BuildDisplayTable](builddisplaytable.md) function, or by implementing custom code.</span></span> 
    
5. <span data-ttu-id="81526-130">Appelez [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) pour afficher une feuille de propriétés qui possède les propriétés copiées.</span><span class="sxs-lookup"><span data-stu-id="81526-130">Call [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) to display a property sheet that has the copied properties.</span></span> <span data-ttu-id="81526-131">Passez un pointeur vers l’objet de données de propriété en tant que paramètre _lpConfigData_ et un pointeur vers le tableau d’affichage en tant que paramètre _lpDisplayTable._</span><span class="sxs-lookup"><span data-stu-id="81526-131">Pass a pointer to the property data object as the  _lpConfigData_ parameter and a pointer to the display table as the  _lpDisplayTable_ parameter.</span></span> <span data-ttu-id="81526-132">Si vous souhaitez remplacer le mode d’accès par défaut pour cette feuille de propriétés, ne définissez pas l’indicateur DT_EDITABLE pour chaque contrôle du tableau d’affichage qui représente une propriété en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="81526-132">If you want to override the default access mode for this property sheet, do not set the DT_EDITABLE flag for each control in the display table that represents a read-only property.</span></span> 
    
6. <span data-ttu-id="81526-133">Lorsque toutes les modifications ont été apportées dans la feuille des propriétés, appelez la méthode **IMAPIProp::CopyTo** de l’objet de données de propriété pour copier les propriétés modifiées dans la section de profil.</span><span class="sxs-lookup"><span data-stu-id="81526-133">When all of the changes have been made in the property sheet, call the property data object's **IMAPIProp::CopyTo** method to copy the changed properties back to the profile section.</span></span> 
    
<span data-ttu-id="81526-134">Pour obtenir une vue d’ensemble des tableaux d’affichage, voir [Tableaux d’affichage.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="81526-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> 
  
<span data-ttu-id="81526-135">Pour plus d’informations sur les tableaux d’affichage, voir [Display Table Implementation](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="81526-135">For detailed information about display tables, see [Display Table Implementation](display-table-implementation.md).</span></span> 
  
<span data-ttu-id="81526-136">Pour plus d’informations sur l’implémentation d’un contrôle, voir [Control Object Implementation](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="81526-136">For information about implementing a control, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
<span data-ttu-id="81526-137">Pour récupérer l’index d’un contrôle qu’un utilisateur sélectionne dans une zone de liste de tableau d’affichage, attendez que l’utilisateur clique sur **OK** ou **Applique.**</span><span class="sxs-lookup"><span data-stu-id="81526-137">To retrieve the index of a control that a user selects in a display table list box, wait until the user clicks **OK** or **Apply**.</span></span> <span data-ttu-id="81526-138">À ce stade, l’identificateur d’entrée de l’élément sélectionné est écrit dans l’interface [IMAPIProp : IUnknown](imapipropiunknown.md) en tant que valeur de la propriété spécifiée par le membre **ulPRSetProperty** dans la structure [DTBLLBX.](dtbllbx.md)</span><span class="sxs-lookup"><span data-stu-id="81526-138">At this point, the entry identifier of the selected item is written back to the [IMAPIProp : IUnknown](imapipropiunknown.md) interface as the value of the property specified by the **ulPRSetProperty** member in the [DTBLLBX](dtbllbx.md) structure.</span></span> 
  
<span data-ttu-id="81526-139">Si vous devez pouvoir ajouter ou supprimer des éléments de votre zone de liste, l’utilisation d’un tableau d’affichage et de la méthode [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="81526-139">If you need to be able to add or remove items from your list box, using a display table and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method will not work.</span></span> <span data-ttu-id="81526-140">Envisagez plutôt d’implémenter une feuille de propriétés avec l’API de feuille de propriétés Win32 contenue dans comdlg32.dll fichier.</span><span class="sxs-lookup"><span data-stu-id="81526-140">Instead, consider implementing a property sheet with the Win32 property sheet API contained in the comdlg32.dll file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="81526-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81526-141">See also</span></span>



[<span data-ttu-id="81526-142">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="81526-142">MAPI Service Providers</span></span>](mapi-service-providers.md)

