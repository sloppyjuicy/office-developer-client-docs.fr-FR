---
title: Propriété canonique PidTagContactAddressBookMultipleAddressFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 34f61f3ef64e5751f9be3df534c4379583447799
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592695"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="20eba-103">Propriété canonique PidTagContactAddressBookMultipleAddressFlag</span><span class="sxs-lookup"><span data-stu-id="20eba-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="20eba-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20eba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20eba-105">Contient un indicateur qui a la valeur TRUE si le fournisseur prend en charge plusieurs adresses de messagerie par élément de contact.</span><span class="sxs-lookup"><span data-stu-id="20eba-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20eba-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="20eba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="20eba-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="20eba-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="20eba-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="20eba-108">Identifier:</span></span>  <br/> |<span data-ttu-id="20eba-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="20eba-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="20eba-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="20eba-110">Data type:</span></span>  <br/> |<span data-ttu-id="20eba-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="20eba-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="20eba-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="20eba-112">Area:</span></span>  <br/> |<span data-ttu-id="20eba-113">Carnet d’adresses de contacts</span><span class="sxs-lookup"><span data-stu-id="20eba-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20eba-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="20eba-114">Remarks</span></span>

<span data-ttu-id="20eba-115">Si cette propriété a la valeur TRUE, le fournisseur n’autorise pas les contacts sans les adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="20eba-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="20eba-116">Si la valeur est FALSE, le fournisseur affiche tous les contacts ou non une adresse de messagerie principale.</span><span class="sxs-lookup"><span data-stu-id="20eba-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="20eba-117">Uniquement l’adresse de messagerie principale sera respectée.</span><span class="sxs-lookup"><span data-stu-id="20eba-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="20eba-118">Il s’agit d’une propriété sur un conteneur de carnet d’adresses de contacts et une colonne dans la table des conteneurs du carnet d’adresses de contacts.</span><span class="sxs-lookup"><span data-stu-id="20eba-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="20eba-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="20eba-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="20eba-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="20eba-120">Header files</span></span>

<span data-ttu-id="20eba-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20eba-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="20eba-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="20eba-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="20eba-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="20eba-123">Mapitags.h</span></span>
  
> <span data-ttu-id="20eba-124">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="20eba-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20eba-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20eba-125">See also</span></span>



[<span data-ttu-id="20eba-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="20eba-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="20eba-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="20eba-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="20eba-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="20eba-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="20eba-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="20eba-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

