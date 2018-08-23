---
title: Implémentation d’un tableau d’affichage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3e31dd7b25b3abf333505c8bde57f61be7a10901
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580606"
---
# <a name="display-table-implementation"></a><span data-ttu-id="96780-103">Implémentation d’un tableau d’affichage</span><span class="sxs-lookup"><span data-stu-id="96780-103">Display Table Implementation</span></span>

  
  
<span data-ttu-id="96780-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96780-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96780-105">Un tableau d’affichage est utilisé pour afficher une feuille de propriétés, une boîte de dialogue se compose d’une ou plusieurs pages de propriétés dédiée à afficher et de modifier éventuellement une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="96780-105">A display table is used to show a property sheet, a special dialog box that is composed of one or more tabbed property pages dedicated to displaying and possibly editing one or more properties.</span></span> <span data-ttu-id="96780-106">Associé à chaque table est un [IAttach : IMAPIProp](iattachimapiprop.md) implémentation de l’interface.</span><span class="sxs-lookup"><span data-stu-id="96780-106">Associated with every display table is an [IAttach : IMAPIProp](iattachimapiprop.md) interface implementation.</span></span> <span data-ttu-id="96780-107">L’implémentation [IMAPIProp](imapipropiunknown.md) gère les données de propriété qui sont présentées dans la feuille des propriétés.</span><span class="sxs-lookup"><span data-stu-id="96780-107">The [IMAPIProp](imapipropiunknown.md) implementation maintains the property data that is presented in the property sheet.</span></span> 
  
<span data-ttu-id="96780-108">Les lignes dans un affichage de tableau représentent les contrôles dans la feuille des propriétés.</span><span class="sxs-lookup"><span data-stu-id="96780-108">The rows in a display table represent the controls in the property sheet.</span></span> <span data-ttu-id="96780-109">La plupart des contrôles peut être associé à des propriétés gérées avec l’implémentation **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="96780-109">Most controls can be associated with properties maintained with the **IMAPIProp** implementation.</span></span> <span data-ttu-id="96780-110">Lorsqu’un utilisateur modifie la valeur d’un contrôle modifiable, la propriété correspondante est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="96780-110">When a user changes the value of a modifiable control, the corresponding property is updated.</span></span> 
  
<span data-ttu-id="96780-111">Les colonnes dans un affichage de tableau représentent les propriétés du contrôle, telles que sa position dans la feuille des propriétés, son type, structure associée et identificateur.</span><span class="sxs-lookup"><span data-stu-id="96780-111">The columns in a display table represent properties of the control, such as its position in the property sheet, its type, associated structure, and identifier.</span></span> <span data-ttu-id="96780-112">Pour obtenir une liste complète des colonnes de tableau d’affichage requis, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="96780-112">For a complete list of required display table columns, see [Display Tables](display-tables.md).</span></span>
  
<span data-ttu-id="96780-113">MAPI affiche une feuille de propriétés à l’utilisateur d’une application cliente en lisant les valeurs de propriété à partir de l’implémentation **IMAPIProp** associé à la table d’affichage ou de la table d’affichage directement.</span><span class="sxs-lookup"><span data-stu-id="96780-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span></span> <span data-ttu-id="96780-114">Lorsque l’utilisateur avec la feuille des propriétés, modification des valeurs dans les contrôles, appels MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) pour enregistrer un contrôle modifié si l’indicateur de DT_SET_IMMEDIATE du contrôle est défini.</span><span class="sxs-lookup"><span data-stu-id="96780-114">As the user works with the property sheet, changing values in the controls, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to save a changed control if the control's DT_SET_IMMEDIATE flag is set.</span></span> <span data-ttu-id="96780-115">Pour les contrôles sans l’indicateur DT_SET_IMMEDIATE est défini, les modifications apportées aux propriétés sont enregistrées lorsque l’utilisateur ferme la boîte de dialogue en cliquant sur le bouton **OK** ou **Appliquer** .</span><span class="sxs-lookup"><span data-stu-id="96780-115">For controls without the DT_SET_IMMEDIATE flag set, changes to properties are saved when the user dismisses the dialog box by clicking the **OK** or **Apply Now** button.</span></span> <span data-ttu-id="96780-116">Un clic sur un de ces boutons ou sur le bouton **Annuler** , MAPI supprime la feuille des propriétés d’affichage.</span><span class="sxs-lookup"><span data-stu-id="96780-116">When either of these buttons or the **Cancel** button is clicked, MAPI removes the property sheet from view.</span></span> 
  
<span data-ttu-id="96780-117">MAPI accède à la table d’affichage en appelant la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) dans l’implémentation **IMAPIProp** et demande la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) ou par héritage dans un appel que vous avez apportées à MAPI, tel que [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span><span class="sxs-lookup"><span data-stu-id="96780-117">MAPI gains access to your display table either by calling the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method in the **IMAPIProp** implementation and requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property or by inheriting it in a call that you have made to MAPI, such as [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span></span>
  
<span data-ttu-id="96780-118">La première technique d’accès est utilisée lorsque les fournisseurs de carnet d’adresses sont invités à afficher plus d’informations sur les utilisateurs ou les listes de distribution de messagerie.</span><span class="sxs-lookup"><span data-stu-id="96780-118">The first access technique is used when address book providers are asked to show details about messaging users or distribution lists.</span></span> <span data-ttu-id="96780-119">Le traitement suivant se produit :</span><span class="sxs-lookup"><span data-stu-id="96780-119">The following processing occurs:</span></span>
  
1. <span data-ttu-id="96780-120">Un client appelle la méthode [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="96780-120">A client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
    
2. <span data-ttu-id="96780-121">MAPI appelle la méthode de [IABLogon::OpenEntry](iablogon-openentry.md) du fournisseur de carnet d’adresses pour accéder à l’utilisateur de messagerie qui représente l’entrée sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="96780-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span></span> 
    
3. <span data-ttu-id="96780-122">MAPI appelle la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de l’utilisateur de messagerie pour récupérer la propriété **PR_DETAILS_TABLE** , la table d’affichage de la boîte de dialogue Détails.</span><span class="sxs-lookup"><span data-stu-id="96780-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span></span> 
    
4. <span data-ttu-id="96780-123">MAPI affiche la boîte de dialogue Gestion de l’interaction avec les informations de l’utilisateur et le supprime lorsque l’utilisateur est terminée.</span><span class="sxs-lookup"><span data-stu-id="96780-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="96780-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96780-124">See also</span></span>



[<span data-ttu-id="96780-125">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="96780-125">MAPI Service Providers</span></span>](mapi-service-providers.md)

