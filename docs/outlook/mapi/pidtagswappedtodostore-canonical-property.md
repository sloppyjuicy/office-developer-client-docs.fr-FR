---
title: Propriété canonique PidTagSwappedToDoStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoStore
api_type:
- COM
ms.assetid: 1edae9ac-fc9a-4bfe-b053-99de848c5144
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 41aa97a52176cf68775d6fd507d3d042888092cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358904"
---
# <a name="pidtagswappedtodostore-canonical-property"></a><span data-ttu-id="706aa-103">Propriété canonique PidTagSwappedToDoStore</span><span class="sxs-lookup"><span data-stu-id="706aa-103">PidTagSwappedToDoStore Canonical Property</span></span>

  
  
<span data-ttu-id="706aa-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="706aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="706aa-105">Détermine la nécessité de post-transmission du traitement d’un e-mail.</span><span class="sxs-lookup"><span data-stu-id="706aa-105">Determines the need for post-transmit processing of an email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="706aa-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="706aa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="706aa-107">PR_SWAPPED_TODO_STORE</span><span class="sxs-lookup"><span data-stu-id="706aa-107">PR_SWAPPED_TODO_STORE</span></span>  <br/> |
|<span data-ttu-id="706aa-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="706aa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="706aa-109">0x0E2C</span><span class="sxs-lookup"><span data-stu-id="706aa-109">0x0E2C</span></span>  <br/> |
|<span data-ttu-id="706aa-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="706aa-110">Data type:</span></span>  <br/> |<span data-ttu-id="706aa-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="706aa-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="706aa-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="706aa-112">Area:</span></span>  <br/> |<span data-ttu-id="706aa-113">MAPI non transmetteable</span><span class="sxs-lookup"><span data-stu-id="706aa-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="706aa-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="706aa-114">Remarks</span></span>

<span data-ttu-id="706aa-115">Si cette propriété est définie sur un brouillon de message, sa valeur doit être définie sur la valeur de la propriété **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) du message.</span><span class="sxs-lookup"><span data-stu-id="706aa-115">If this property is set on a draft message, then its value must be set to the value of **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property of the message.</span></span>
  
<span data-ttu-id="706aa-116">Pour plus d’informations, voir la section [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) « Post-Transmit Processing of a Flagged Message ».</span><span class="sxs-lookup"><span data-stu-id="706aa-116">For more information, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) section "Post-Transmit Processing of a Flagged Message."</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="706aa-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="706aa-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="706aa-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="706aa-118">Protocol specifications</span></span>

<span data-ttu-id="706aa-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="706aa-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="706aa-120">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="706aa-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="706aa-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="706aa-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="706aa-122">Spécifie les propriétés et les opérations liées au marquage.</span><span class="sxs-lookup"><span data-stu-id="706aa-122">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="706aa-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="706aa-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="706aa-124">Spécifie les propriétés et le modèle d’interaction pour les messages électroniques et autres rappels d’objets.</span><span class="sxs-lookup"><span data-stu-id="706aa-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="706aa-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="706aa-125">Header files</span></span>

<span data-ttu-id="706aa-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="706aa-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="706aa-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="706aa-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="706aa-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="706aa-128">Mapitags.h</span></span>
  
> <span data-ttu-id="706aa-129">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="706aa-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="706aa-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="706aa-130">See also</span></span>



[<span data-ttu-id="706aa-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="706aa-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="706aa-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="706aa-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="706aa-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="706aa-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="706aa-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="706aa-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

