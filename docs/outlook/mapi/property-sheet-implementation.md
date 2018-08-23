---
title: Implémentation d’une feuille de propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9a0fad8fa20b2d94077f9fbdf8a3c595c0ab219e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580865"
---
# <a name="property-sheet-implementation"></a><span data-ttu-id="64d60-103">Implémentation d’une feuille de propriétés</span><span class="sxs-lookup"><span data-stu-id="64d60-103">Property Sheet Implementation</span></span>

  
  
<span data-ttu-id="64d60-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64d60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64d60-105">Une feuille de propriétés est une boîte de dialogue pour afficher les propriétés d’un objet.</span><span class="sxs-lookup"><span data-stu-id="64d60-105">A property sheet is a dialog box for displaying the properties of an object.</span></span> <span data-ttu-id="64d60-106">Les propriétés peuvent être en lecture seule, l’activation de l’utilisateur uniquement pour les afficher, ou de lecture/écriture, permettant à l’utilisateur apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="64d60-106">The properties can be read-only, enabling the user only to view them, or read/write, enabling the user to make changes.</span></span> <span data-ttu-id="64d60-107">Une feuille de propriétés contient une ou plusieurs fenêtres enfants qui se chevauchent, appelés pages.</span><span class="sxs-lookup"><span data-stu-id="64d60-107">A property sheet contains one or more overlapping child windows called pages.</span></span> <span data-ttu-id="64d60-108">Chaque page contient un contrôle windows pour définir un groupe de propriétés connexes.</span><span class="sxs-lookup"><span data-stu-id="64d60-108">Each page contains control windows for setting a group of related properties.</span></span> <span data-ttu-id="64d60-109">Les utilisateurs naviguer d’une page en sélectionnant un onglet qui affiche la page correspondante au premier plan de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="64d60-109">Users navigate from page to page by selecting a tab that brings the corresponding page to the foreground of the property sheet.</span></span>
  
<span data-ttu-id="64d60-110">Fournisseurs de services doivent implémenter une feuille de propriétés qui affiche un jeu de propriétés relatives à la configuration dans le service message minimal.</span><span class="sxs-lookup"><span data-stu-id="64d60-110">Service providers must implement a property sheet that displays a minimal set of properties related to configuration in the message service.</span></span> <span data-ttu-id="64d60-111">Si vous autorisez ces propriétés de service de message à modifier, vous pouvez soit autoriser les utilisateurs du client applications, telles que le panneau, apportez les modifications ou appliquer les modifications apportées par programme.</span><span class="sxs-lookup"><span data-stu-id="64d60-111">If you allow these message service properties to be changed, you can either allow users of client applications, such as the Control Panel, to make the changes or implement the changes programmatically.</span></span> <span data-ttu-id="64d60-112">Feuilles de propriétés pour afficher et modifier d’autres types de propriétés est facultative.</span><span class="sxs-lookup"><span data-stu-id="64d60-112">Implementing property sheets to display and edit other types of properties is optional.</span></span> 
  
<span data-ttu-id="64d60-113">En règle générale, vous devrez afficher une feuille de propriétés dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="64d60-113">Typically, you will need to display a property sheet in the following situations:</span></span>
  
- <span data-ttu-id="64d60-114">Lorsqu’un client appelle la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) de l’objet de votre statut.</span><span class="sxs-lookup"><span data-stu-id="64d60-114">When a client calls your status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method.</span></span> 
    
- <span data-ttu-id="64d60-115">Lorsque MAPI appelle la méthode d’ouverture de session de l’objet de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="64d60-115">When MAPI calls your provider object's logon method.</span></span>
    
- <span data-ttu-id="64d60-116">Lorsque MAPI appelle la fonction de point d’entrée pour le service de message de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="64d60-116">When MAPI calls the entry point function for your provider's message service.</span></span>
    
<span data-ttu-id="64d60-117">Fournisseurs de transport implémentent également les feuilles de propriétés pour afficher les propriétés liées aux options de message et fournisseurs de carnet d’adresses implémentent des feuilles de propriétés pour afficher et modifier des informations détaillées sur les utilisateurs et les listes de distribution, recherche avancée de la messagerie critères et modèles pour la saisie de nouveaux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="64d60-117">Transport providers also implement property sheets to display properties related to message options, and address book providers implement property sheets to view and edit detailed information about messaging users and distribution lists, advanced search criteria, and templates for entering new users.</span></span>
  
<span data-ttu-id="64d60-118">Vous pouvez utiliser une des trois méthodes suivantes pour créer une feuille de propriétés :</span><span class="sxs-lookup"><span data-stu-id="64d60-118">You can use one of the following three techniques to create a property sheet:</span></span>
  
- <span data-ttu-id="64d60-119">Manuellement, comme vous le feriez pour toute boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="64d60-119">Manually, as you would any dialog box.</span></span>
    
- <span data-ttu-id="64d60-120">À l’aide de la propriété contrôle de la feuille fourni dans le SDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="64d60-120">By using the property sheet common control provided in the Windows SDK.</span></span>
    
- <span data-ttu-id="64d60-121">Afficher le tableau à l’aide d’une MAPI.</span><span class="sxs-lookup"><span data-stu-id="64d60-121">By using a MAPI display table.</span></span>
    
<span data-ttu-id="64d60-122">Fournisseurs doivent choisir la dernière option (créer une feuille de propriétés à l’aide d’un tableau d’affichage).</span><span class="sxs-lookup"><span data-stu-id="64d60-122">Providers should choose the last option (create a property sheet by using a display table).</span></span> <span data-ttu-id="64d60-123">Il s’agit de l’option la plus simple car elle élimine la nécessité de travailler avec l’interface utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="64d60-123">This is the simplest option because it eliminates the need to work with the Windows user interface.</span></span> 
  
<span data-ttu-id="64d60-124">Pour implémenter une feuille de propriétés créée à partir d’un tableau d’affichage pour des propriétés de service de message, utilisez la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="64d60-124">To implement a property sheet built from a display table for your message service properties, use the following procedure:</span></span>
  
1. <span data-ttu-id="64d60-125">Appelez [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) pour ouvrir une section dans le profil actif.</span><span class="sxs-lookup"><span data-stu-id="64d60-125">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) to open a section in the current profile.</span></span> <span data-ttu-id="64d60-126">Passez vos [MAPIUID](mapiuid.md) ou la valeur NULL pour ouvrir la section de profil de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="64d60-126">Pass your [MAPIUID](mapiuid.md) or NULL to open your provider's profile section.</span></span> 
    
2. <span data-ttu-id="64d60-127">Appelez [CreateIProp](createiprop.md) pour créer un objet de données de propriété.</span><span class="sxs-lookup"><span data-stu-id="64d60-127">Call [CreateIProp](createiprop.md) to create a property data object.</span></span> 
    
3. <span data-ttu-id="64d60-128">Appeler la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) de la section profil pour copier toutes les propriétés de la section à l’objet de données de propriété.</span><span class="sxs-lookup"><span data-stu-id="64d60-128">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy all of the section's properties to the property data object.</span></span> 
    
4. <span data-ttu-id="64d60-129">Créer un tableau d’affichage en créant une ou plusieurs structures [DTPAGE](dtpage.md) qui décrivent les contrôles qui doit apparaître sur la feuille des propriétés et appeler la fonction [BuildDisplayTable](builddisplaytable.md) , ou en implémentant un code personnalisé.</span><span class="sxs-lookup"><span data-stu-id="64d60-129">Create a display table either by building one or more [DTPAGE](dtpage.md) structures that describe the controls to appear on the property sheet and calling the [BuildDisplayTable](builddisplaytable.md) function, or by implementing custom code.</span></span> 
    
5. <span data-ttu-id="64d60-130">Appelez [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) pour afficher une feuille de propriétés qui possède les propriétés copiées.</span><span class="sxs-lookup"><span data-stu-id="64d60-130">Call [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) to display a property sheet that has the copied properties.</span></span> <span data-ttu-id="64d60-131">Passer un pointeur vers l’objet de données de propriété en tant que le paramètre _lpConfigData_ et un pointeur vers le tableau de l’affichage en tant que paramètre _lpDisplayTable_ .</span><span class="sxs-lookup"><span data-stu-id="64d60-131">Pass a pointer to the property data object as the  _lpConfigData_ parameter and a pointer to the display table as the  _lpDisplayTable_ parameter.</span></span> <span data-ttu-id="64d60-132">Si vous souhaitez remplacer le mode d’accès par défaut pour cette feuille de propriétés, ne définissez pas l’indicateur DT_EDITABLE pour chaque contrôle dans le tableau d’affichage qui représente une propriété en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="64d60-132">If you want to override the default access mode for this property sheet, do not set the DT_EDITABLE flag for each control in the display table that represents a read-only property.</span></span> 
    
6. <span data-ttu-id="64d60-133">Lorsque toutes les modifications ont été apportées dans la feuille des propriétés, appelez la méthode de **IMAPIProp::CopyTo** de l’objet de données de propriété pour copier les propriétés modifiées à la section de profil.</span><span class="sxs-lookup"><span data-stu-id="64d60-133">When all of the changes have been made in the property sheet, call the property data object's **IMAPIProp::CopyTo** method to copy the changed properties back to the profile section.</span></span> 
    
<span data-ttu-id="64d60-134">Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="64d60-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> 
  
<span data-ttu-id="64d60-135">Pour plus d’informations sur les tables d’affichage, voir [Implémentation de Table afficher](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="64d60-135">For detailed information about display tables, see [Display Table Implementation](display-table-implementation.md).</span></span> 
  
<span data-ttu-id="64d60-136">Pour plus d’informations sur l’implémentation d’un contrôle, voir [Implémentation d’objet de contrôle](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="64d60-136">For information about implementing a control, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
<span data-ttu-id="64d60-137">Pour récupérer l’index d’un contrôle sélectionné par un utilisateur dans une zone de liste affichage tableau, attendez que l’utilisateur clique sur **OK** ou sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="64d60-137">To retrieve the index of a control that a user selects in a display table list box, wait until the user clicks **OK** or **Apply**.</span></span> <span data-ttu-id="64d60-138">À ce stade, l’identificateur d’entrée de l’élément sélectionné est réécrit dans la [IMAPIProp : IUnknown](imapipropiunknown.md) interface comme valeur de la propriété spécifiée par le membre **ulPRSetProperty** de la structure [DTBLLBX](dtbllbx.md) .</span><span class="sxs-lookup"><span data-stu-id="64d60-138">At this point, the entry identifier of the selected item is written back to the [IMAPIProp : IUnknown](imapipropiunknown.md) interface as the value of the property specified by the **ulPRSetProperty** member in the [DTBLLBX](dtbllbx.md) structure.</span></span> 
  
<span data-ttu-id="64d60-139">Si vous devez être en mesure d’ajouter ou supprimer des éléments de votre zone de liste, l’à l’aide d’un tableau d’affichage et la méthode [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="64d60-139">If you need to be able to add or remove items from your list box, using a display table and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method will not work.</span></span> <span data-ttu-id="64d60-140">Au lieu de cela, envisagez d’implémenter une feuille de propriétés avec l’API de feuille de propriétés Win32 contenue dans le fichier comdlg32.dll.</span><span class="sxs-lookup"><span data-stu-id="64d60-140">Instead, consider implementing a property sheet with the Win32 property sheet API contained in the comdlg32.dll file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64d60-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64d60-141">See also</span></span>



[<span data-ttu-id="64d60-142">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="64d60-142">MAPI Service Providers</span></span>](mapi-service-providers.md)

