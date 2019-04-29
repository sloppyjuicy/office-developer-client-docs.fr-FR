---
title: Propriété canonique PidTagOwnStoreEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnStoreEntryId
api_type:
- COM
ms.assetid: 6a82ee90-10a1-49e0-8f3a-a2cd9f490f99
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 16a23c4e711bf9f7b670dff8b3e8f65371aa6bda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427373"
---
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="42eb5-103">Propriété canonique PidTagOwnStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="42eb5-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="42eb5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42eb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42eb5-105">Contient l'identificateur d'entrée d'une banque de messages étroitement couplée d'un transport.</span><span class="sxs-lookup"><span data-stu-id="42eb5-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42eb5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="42eb5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="42eb5-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="42eb5-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="42eb5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="42eb5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="42eb5-109">0x3E06</span><span class="sxs-lookup"><span data-stu-id="42eb5-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="42eb5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="42eb5-110">Data type:</span></span>  <br/> |<span data-ttu-id="42eb5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="42eb5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="42eb5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="42eb5-112">Area:</span></span>  <br/> |<span data-ttu-id="42eb5-113">Propriétés de la Banque de messages</span><span class="sxs-lookup"><span data-stu-id="42eb5-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42eb5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="42eb5-114">Remarks</span></span>

<span data-ttu-id="42eb5-115">Cette propriété spécifie l'identificateur d'entrée pour le magasin étroitement couplé, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="42eb5-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="42eb5-116">Par exemple, un fournisseur de transport peut spécifier l'identificateur de l'entrée de la Banque de dossiers privés afin que le spouleur MAPI puisse connecter le fournisseur de transport au magasin.</span><span class="sxs-lookup"><span data-stu-id="42eb5-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="42eb5-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="42eb5-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="42eb5-118">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="42eb5-118">Header files</span></span>

<span data-ttu-id="42eb5-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="42eb5-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="42eb5-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="42eb5-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="42eb5-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="42eb5-121">Mapitags.h</span></span>
  
> <span data-ttu-id="42eb5-122">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="42eb5-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="42eb5-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42eb5-123">See also</span></span>



[<span data-ttu-id="42eb5-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="42eb5-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="42eb5-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="42eb5-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="42eb5-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="42eb5-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="42eb5-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="42eb5-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

