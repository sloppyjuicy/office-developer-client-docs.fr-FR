---
title: Propriété canonique PidTagStoreState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreState
api_type:
- COM
ms.assetid: 36e49cf5-1411-42c5-9112-09958243996d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8f00addf7abdd765d97c54350e46979f788f06ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399010"
---
# <a name="pidtagstorestate-canonical-property"></a><span data-ttu-id="54673-103">Propriété canonique PidTagStoreState</span><span class="sxs-lookup"><span data-stu-id="54673-103">PidTagStoreState Canonical Property</span></span>

  
  
<span data-ttu-id="54673-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54673-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54673-105">Contient un indicateur qui décrit l’état de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="54673-105">Contains a flag that describes the state of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54673-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="54673-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="54673-107">PR_STORE_STATE</span><span class="sxs-lookup"><span data-stu-id="54673-107">PR_STORE_STATE</span></span>  <br/> |
|<span data-ttu-id="54673-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="54673-108">Identifier:</span></span>  <br/> |<span data-ttu-id="54673-109">0x340E</span><span class="sxs-lookup"><span data-stu-id="54673-109">0x340E</span></span>  <br/> |
|<span data-ttu-id="54673-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="54673-110">Data type:</span></span>  <br/> |<span data-ttu-id="54673-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="54673-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="54673-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="54673-112">Area:</span></span>  <br/> |<span data-ttu-id="54673-113">Banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="54673-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54673-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="54673-114">Remarks</span></span>

<span data-ttu-id="54673-115">Cette propriété est dynamique et peut changer en fonction des actions de l’utilisateur, contrairement à la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="54673-115">This property is dynamic and can change based on user actions, unlike the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="54673-116">Peut avoir la valeur suivante :</span><span class="sxs-lookup"><span data-stu-id="54673-116">The following value can be set:</span></span>
  
<span data-ttu-id="54673-117">STORE_HAS_SEARCHES</span><span class="sxs-lookup"><span data-stu-id="54673-117">STORE_HAS_SEARCHES</span></span> 
  
> <span data-ttu-id="54673-118">L’utilisateur a créé un ou plusieurs recherches actives dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="54673-118">The user has created one or more active searches in the store.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="54673-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="54673-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="54673-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="54673-120">Protocol specifications</span></span>

<span data-ttu-id="54673-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54673-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54673-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="54673-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="54673-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54673-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54673-124">Spécifie les opérations autorisées pour les objets de banque de messages principale.</span><span class="sxs-lookup"><span data-stu-id="54673-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="54673-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="54673-125">Header files</span></span>

<span data-ttu-id="54673-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54673-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="54673-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="54673-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="54673-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="54673-128">Mapitags.h</span></span>
  
> <span data-ttu-id="54673-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="54673-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54673-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54673-130">See also</span></span>



[<span data-ttu-id="54673-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="54673-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54673-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="54673-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54673-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="54673-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54673-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="54673-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

