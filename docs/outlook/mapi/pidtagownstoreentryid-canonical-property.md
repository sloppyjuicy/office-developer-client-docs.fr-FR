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
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="cceca-103">Propriété canonique PidTagOwnStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="cceca-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="cceca-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cceca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cceca-105">Contient l’identificateur d’entrée de la magasin de messages fortement couplé d’un transport.</span><span class="sxs-lookup"><span data-stu-id="cceca-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cceca-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="cceca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cceca-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cceca-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="cceca-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="cceca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cceca-109">0x3E06</span><span class="sxs-lookup"><span data-stu-id="cceca-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="cceca-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="cceca-110">Data type:</span></span>  <br/> |<span data-ttu-id="cceca-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cceca-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cceca-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="cceca-112">Area:</span></span>  <br/> |<span data-ttu-id="cceca-113">Propriétés de la boutique de messages</span><span class="sxs-lookup"><span data-stu-id="cceca-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cceca-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="cceca-114">Remarks</span></span>

<span data-ttu-id="cceca-115">Cette propriété spécifie l’identificateur d’entrée pour le magasin étroitement couplé, s’il en existe un.</span><span class="sxs-lookup"><span data-stu-id="cceca-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="cceca-116">Par exemple, un fournisseur de transport peut spécifier l’identificateur d’entrée du magasin de dossiers privés afin que lepooler MAPI puisse connecter le fournisseur de transport à la banque.</span><span class="sxs-lookup"><span data-stu-id="cceca-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cceca-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="cceca-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cceca-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="cceca-118">Header files</span></span>

<span data-ttu-id="cceca-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cceca-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="cceca-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="cceca-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="cceca-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cceca-121">Mapitags.h</span></span>
  
> <span data-ttu-id="cceca-122">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="cceca-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cceca-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cceca-123">See also</span></span>



[<span data-ttu-id="cceca-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="cceca-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cceca-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="cceca-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cceca-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="cceca-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cceca-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="cceca-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

