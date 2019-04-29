---
title: Implémentation des tables d'affichage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6990e32445083c3465693df2c1a3d40b980853c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435263"
---
# <a name="display-table-implementation"></a><span data-ttu-id="c35c3-103">Implémentation des tables d'affichage</span><span class="sxs-lookup"><span data-stu-id="c35c3-103">Display Table Implementation</span></span>

  
  
<span data-ttu-id="c35c3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c35c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c35c3-105">Une table d'affichage est utilisée pour afficher une feuille de propriétés, une boîte de dialogue spéciale constituée d'une ou de plusieurs pages de propriétés à onglets dédiées à l'affichage et éventuellement la modification d'une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="c35c3-105">A display table is used to show a property sheet, a special dialog box that is composed of one or more tabbed property pages dedicated to displaying and possibly editing one or more properties.</span></span> <span data-ttu-id="c35c3-106">L'implémentation de l'interface [IAttach: IMAPIProp](iattachimapiprop.md) est associée à chaque table d'affichage.</span><span class="sxs-lookup"><span data-stu-id="c35c3-106">Associated with every display table is an [IAttach : IMAPIProp](iattachimapiprop.md) interface implementation.</span></span> <span data-ttu-id="c35c3-107">L'implémentation de [IMAPIProp](imapipropiunknown.md) gère les données de propriété présentées dans la feuille des propriétés.</span><span class="sxs-lookup"><span data-stu-id="c35c3-107">The [IMAPIProp](imapipropiunknown.md) implementation maintains the property data that is presented in the property sheet.</span></span> 
  
<span data-ttu-id="c35c3-108">Les lignes d'une table d'affichage représentent les contrôles de la feuille des propriétés.</span><span class="sxs-lookup"><span data-stu-id="c35c3-108">The rows in a display table represent the controls in the property sheet.</span></span> <span data-ttu-id="c35c3-109">La plupart des contrôles peuvent être associés à des propriétés gérées à l'aide de l'implémentation **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="c35c3-109">Most controls can be associated with properties maintained with the **IMAPIProp** implementation.</span></span> <span data-ttu-id="c35c3-110">Lorsqu'un utilisateur modifie la valeur d'un contrôle modifiable, la propriété correspondante est mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c35c3-110">When a user changes the value of a modifiable control, the corresponding property is updated.</span></span> 
  
<span data-ttu-id="c35c3-111">Les colonnes d'une table d'affichage représentent les propriétés du contrôle, telles que sa position dans la feuille des propriétés, son type, sa structure associée et son identificateur.</span><span class="sxs-lookup"><span data-stu-id="c35c3-111">The columns in a display table represent properties of the control, such as its position in the property sheet, its type, associated structure, and identifier.</span></span> <span data-ttu-id="c35c3-112">Pour obtenir la liste complète des colonnes de tableau d'affichage requises, consultez la rubrique [Display tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c35c3-112">For a complete list of required display table columns, see [Display Tables](display-tables.md).</span></span>
  
<span data-ttu-id="c35c3-113">MAPI affiche une feuille de propriétés à l'utilisateur d'une application cliente en lisant les valeurs des propriétés de l'implémentation **IMAPIProp** associée à la table d'affichage ou à partir de la table d'affichage directement.</span><span class="sxs-lookup"><span data-stu-id="c35c3-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span></span> <span data-ttu-id="c35c3-114">Lorsque l'utilisateur travaille sur la feuille des propriétés, en modifiant les valeurs dans les contrôles, MAPI appelle [IMAPIProp:: SetProps](imapiprop-setprops.md) pour enregistrer un contrôle modifié si l'indicateur DT_SET_IMMEDIATE du contrôle est défini.</span><span class="sxs-lookup"><span data-stu-id="c35c3-114">As the user works with the property sheet, changing values in the controls, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to save a changed control if the control's DT_SET_IMMEDIATE flag is set.</span></span> <span data-ttu-id="c35c3-115">Pour les contrôles sans l'indicateur DT_SET_IMMEDIATE, les modifications apportées aux propriétés sont enregistrées lorsque l'utilisateur fait disparaître la boîte de dialogue en cliquant sur le bouton **OK** ou **appliquer maintenant** .</span><span class="sxs-lookup"><span data-stu-id="c35c3-115">For controls without the DT_SET_IMMEDIATE flag set, changes to properties are saved when the user dismisses the dialog box by clicking the **OK** or **Apply Now** button.</span></span> <span data-ttu-id="c35c3-116">Lorsque l'utilisateur clique sur l'un ou l'autre de ces boutons ou sur le bouton **Annuler** , MAPI supprime la feuille de propriétés de l'affichage.</span><span class="sxs-lookup"><span data-stu-id="c35c3-116">When either of these buttons or the **Cancel** button is clicked, MAPI removes the property sheet from view.</span></span> 
  
<span data-ttu-id="c35c3-117">MAPI accède à votre table d'affichage en appelant la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) dans l'implémentation **IMAPIProp** et en demandant la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) ou en l'héritant d'un appel que vous avez effectué vers MAPI, tel que [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md).</span><span class="sxs-lookup"><span data-stu-id="c35c3-117">MAPI gains access to your display table either by calling the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method in the **IMAPIProp** implementation and requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property or by inheriting it in a call that you have made to MAPI, such as [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span></span>
  
<span data-ttu-id="c35c3-118">La première technique d'accès est utilisée lorsque des fournisseurs de carnet d'adresses sont invités à afficher des détails sur les utilisateurs de messagerie ou les listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="c35c3-118">The first access technique is used when address book providers are asked to show details about messaging users or distribution lists.</span></span> <span data-ttu-id="c35c3-119">Le traitement suivant se produit:</span><span class="sxs-lookup"><span data-stu-id="c35c3-119">The following processing occurs:</span></span>
  
1. <span data-ttu-id="c35c3-120">Un client appelle la méthode [IAddrBook::D etails](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="c35c3-120">A client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
    
2. <span data-ttu-id="c35c3-121">MAPI appelle la méthode [IABLogon:: OpenEntry](iablogon-openentry.md) du fournisseur de carnet d'adresses pour accéder à l'utilisateur de messagerie qui représente l'entrée sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="c35c3-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span></span> 
    
3. <span data-ttu-id="c35c3-122">MAPI appelle la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) de l'utilisateur de messagerie pour récupérer la propriété **PR_DETAILS_TABLE** , la table d'affichage de la boîte de dialogue détails.</span><span class="sxs-lookup"><span data-stu-id="c35c3-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span></span> 
    
4. <span data-ttu-id="c35c3-123">MAPI affiche la boîte de dialogue, qui gère l'interaction de l'utilisateur avec les informations, et la supprime lorsque l'utilisateur a terminé.</span><span class="sxs-lookup"><span data-stu-id="c35c3-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c35c3-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c35c3-124">See also</span></span>



[<span data-ttu-id="c35c3-125">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="c35c3-125">MAPI Service Providers</span></span>](mapi-service-providers.md)

