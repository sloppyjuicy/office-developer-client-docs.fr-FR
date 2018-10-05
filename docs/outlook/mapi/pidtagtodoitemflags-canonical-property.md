---
title: Propriété canonique PidTagToDoItemFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6ddc7231afef0a224b92be7fe86216e56200ab70
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400281"
---
# <a name="pidtagtodoitemflags-canonical-property"></a><span data-ttu-id="6e4b8-103">Propriété canonique PidTagToDoItemFlags</span><span class="sxs-lookup"><span data-stu-id="6e4b8-103">PidTagToDoItemFlags Canonical Property</span></span>

  
  
<span data-ttu-id="6e4b8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e4b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e4b8-105">Représente la condition avec indicateur d’un élément action.</span><span class="sxs-lookup"><span data-stu-id="6e4b8-105">Represents a To-Do item's flagged condition.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e4b8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6e4b8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e4b8-107">PR_TODO_ITEM_FLAGS</span><span class="sxs-lookup"><span data-stu-id="6e4b8-107">PR_TODO_ITEM_FLAGS</span></span>  <br/> |
|<span data-ttu-id="6e4b8-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6e4b8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6e4b8-109">0x0E2B</span><span class="sxs-lookup"><span data-stu-id="6e4b8-109">0x0E2B</span></span>  <br/> |
|<span data-ttu-id="6e4b8-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6e4b8-110">Data type:</span></span>  <br/> |<span data-ttu-id="6e4b8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6e4b8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6e4b8-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6e4b8-112">Area:</span></span>  <br/> |<span data-ttu-id="6e4b8-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="6e4b8-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e4b8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6e4b8-114">Remarks</span></span>

<span data-ttu-id="6e4b8-115">Cette propriété est un champ de bits dans lequel chaque bit doit être défini sur 1 si la condition associée dans le tableau suivant s’applique, 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6e4b8-115">This property is a bit field in which each bit should be set to 1 if the associated condition in the following table applies, otherwise 0.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="6e4b8-116">Valeur numérique</span><span class="sxs-lookup"><span data-stu-id="6e4b8-116">Numeric value</span></span>  <br/> |<span data-ttu-id="6e4b8-117">Nom</span><span class="sxs-lookup"><span data-stu-id="6e4b8-117">Name</span></span>  <br/> |<span data-ttu-id="6e4b8-118">Description</span><span class="sxs-lookup"><span data-stu-id="6e4b8-118">Description</span></span>  <br/> |
|<span data-ttu-id="6e4b8-119">Absent</span><span class="sxs-lookup"><span data-stu-id="6e4b8-119">Not present</span></span>  <br/> |<span data-ttu-id="6e4b8-120">S/O</span><span class="sxs-lookup"><span data-stu-id="6e4b8-120">N/A</span></span>  <br/> |<span data-ttu-id="6e4b8-121">Sans indicateur</span><span class="sxs-lookup"><span data-stu-id="6e4b8-121">Unflagged</span></span>  <br/> |
|<span data-ttu-id="6e4b8-122">1</span><span class="sxs-lookup"><span data-stu-id="6e4b8-122">1</span></span>  <br/> |<span data-ttu-id="6e4b8-123">todoTimeFlagged</span><span class="sxs-lookup"><span data-stu-id="6e4b8-123">todoTimeFlagged</span></span>  <br/> |<span data-ttu-id="6e4b8-124">Objet est marqué de temps</span><span class="sxs-lookup"><span data-stu-id="6e4b8-124">Object is time flagged</span></span>  <br/> |
|<span data-ttu-id="6e4b8-125">8</span><span class="sxs-lookup"><span data-stu-id="6e4b8-125">8</span></span>  <br/> |<span data-ttu-id="6e4b8-126">todoRecipientFlagged</span><span class="sxs-lookup"><span data-stu-id="6e4b8-126">todoRecipientFlagged</span></span>  <br/> |<span data-ttu-id="6e4b8-127">Ne doit être défini sur un objet de message provisoire, et cela signifie que l’objet est marqué pour les destinataires.</span><span class="sxs-lookup"><span data-stu-id="6e4b8-127">Should only be set on a draft message object, and it means that the object is flagged for recipients.</span></span>  <br/> |
   
<span data-ttu-id="6e4b8-128">Tous les bits qui ne sont pas spécifiés dans le tableau sont réservés.</span><span class="sxs-lookup"><span data-stu-id="6e4b8-128">All bits that are not specified in the table are reserved.</span></span> <span data-ttu-id="6e4b8-129">Ils doivent être ignorés, mais doivent être préservées si elles sont définies.</span><span class="sxs-lookup"><span data-stu-id="6e4b8-129">They must be ignored, but should be preserved if they are set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6e4b8-130">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6e4b8-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e4b8-131">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="6e4b8-131">Protocol specifications</span></span>

<span data-ttu-id="6e4b8-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e4b8-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e4b8-133">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="6e4b8-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e4b8-134">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e4b8-134">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e4b8-135">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="6e4b8-135">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e4b8-136">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6e4b8-136">Header files</span></span>

<span data-ttu-id="6e4b8-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e4b8-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e4b8-138">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6e4b8-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="6e4b8-139">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6e4b8-139">Mapitags.h</span></span>
  
> <span data-ttu-id="6e4b8-140">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="6e4b8-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e4b8-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e4b8-141">See also</span></span>



[<span data-ttu-id="6e4b8-142">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6e4b8-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e4b8-143">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6e4b8-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e4b8-144">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6e4b8-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e4b8-145">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6e4b8-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

