---
title: Propriété canonique PidTagDetailsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1602d1753d9f7f6e6f407a85dab0a33255db7aae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585786"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="ebd15-103">Propriété canonique PidTagDetailsTable</span><span class="sxs-lookup"><span data-stu-id="ebd15-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="ebd15-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebd15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebd15-105">Contient un objet de la table affichage incorporé.</span><span class="sxs-lookup"><span data-stu-id="ebd15-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ebd15-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ebd15-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ebd15-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="ebd15-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="ebd15-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ebd15-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ebd15-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="ebd15-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="ebd15-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ebd15-110">Data type:</span></span>  <br/> |<span data-ttu-id="ebd15-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="ebd15-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="ebd15-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ebd15-112">Area:</span></span>  <br/> |<span data-ttu-id="ebd15-113">Conteneur MAPI</span><span class="sxs-lookup"><span data-stu-id="ebd15-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ebd15-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ebd15-114">Remarks</span></span>

<span data-ttu-id="ebd15-115">Transmission à la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour l’objet de cette propriété renvoie une interface [IMAPITable](imapitableiunknown.md) qui permet la création de la table d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ebd15-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="ebd15-116">MAPI utilise ce tableau pour afficher les feuilles de propriétés d’un objet de carnet d’adresses en réponse à un appel [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="ebd15-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ebd15-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ebd15-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ebd15-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ebd15-118">Header files</span></span>

<span data-ttu-id="ebd15-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ebd15-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="ebd15-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ebd15-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="ebd15-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ebd15-121">Mapitags.h</span></span>
  
> <span data-ttu-id="ebd15-122">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="ebd15-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ebd15-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebd15-123">See also</span></span>



[<span data-ttu-id="ebd15-124">Propriété canonique PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="ebd15-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="ebd15-125">Propriété canonique PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="ebd15-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="ebd15-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ebd15-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ebd15-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ebd15-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ebd15-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ebd15-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ebd15-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ebd15-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

