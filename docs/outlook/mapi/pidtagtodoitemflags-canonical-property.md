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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284482"
---
# <a name="pidtagtodoitemflags-canonical-property"></a><span data-ttu-id="ac0ef-103">Propriété canonique PidTagToDoItemFlags</span><span class="sxs-lookup"><span data-stu-id="ac0ef-103">PidTagToDoItemFlags Canonical Property</span></span>

  
  
<span data-ttu-id="ac0ef-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac0ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac0ef-105">Représente la condition To-Do d’un élément.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-105">Represents a To-Do item's flagged condition.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac0ef-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ac0ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac0ef-107">PR_TODO_ITEM_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac0ef-107">PR_TODO_ITEM_FLAGS</span></span>  <br/> |
|<span data-ttu-id="ac0ef-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ac0ef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac0ef-109">0x0E2B</span><span class="sxs-lookup"><span data-stu-id="ac0ef-109">0x0E2B</span></span>  <br/> |
|<span data-ttu-id="ac0ef-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ac0ef-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac0ef-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ac0ef-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ac0ef-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ac0ef-112">Area:</span></span>  <br/> |<span data-ttu-id="ac0ef-113">MAPI non transmetteable</span><span class="sxs-lookup"><span data-stu-id="ac0ef-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac0ef-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ac0ef-114">Remarks</span></span>

<span data-ttu-id="ac0ef-115">Cette propriété est un champ de bits dans lequel chaque bit doit être définie sur 1 si la condition associée dans le tableau suivant s’applique, sinon 0.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-115">This property is a bit field in which each bit should be set to 1 if the associated condition in the following table applies, otherwise 0.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="ac0ef-116">Valeur numérique</span><span class="sxs-lookup"><span data-stu-id="ac0ef-116">Numeric value</span></span>  <br/> |<span data-ttu-id="ac0ef-117">Nom</span><span class="sxs-lookup"><span data-stu-id="ac0ef-117">Name</span></span>  <br/> |<span data-ttu-id="ac0ef-118">Description</span><span class="sxs-lookup"><span data-stu-id="ac0ef-118">Description</span></span>  <br/> |
|<span data-ttu-id="ac0ef-119">Non présent</span><span class="sxs-lookup"><span data-stu-id="ac0ef-119">Not present</span></span>  <br/> |<span data-ttu-id="ac0ef-120">S/O</span><span class="sxs-lookup"><span data-stu-id="ac0ef-120">N/A</span></span>  <br/> |<span data-ttu-id="ac0ef-121">Non survolé</span><span class="sxs-lookup"><span data-stu-id="ac0ef-121">Unflagged</span></span>  <br/> |
|<span data-ttu-id="ac0ef-122">1</span><span class="sxs-lookup"><span data-stu-id="ac0ef-122">1</span></span>  <br/> |<span data-ttu-id="ac0ef-123">todoTimeFlagged</span><span class="sxs-lookup"><span data-stu-id="ac0ef-123">todoTimeFlagged</span></span>  <br/> |<span data-ttu-id="ac0ef-124">L’objet est marqué au moment de l’heure</span><span class="sxs-lookup"><span data-stu-id="ac0ef-124">Object is time flagged</span></span>  <br/> |
|<span data-ttu-id="ac0ef-125">8 </span><span class="sxs-lookup"><span data-stu-id="ac0ef-125">8</span></span>  <br/> |<span data-ttu-id="ac0ef-126">todoRecipientFlagged</span><span class="sxs-lookup"><span data-stu-id="ac0ef-126">todoRecipientFlagged</span></span>  <br/> |<span data-ttu-id="ac0ef-127">Ne doit être définie que sur un objet de brouillon de message, ce qui signifie que l’objet est marqué pour les destinataires.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-127">Should only be set on a draft message object, and it means that the object is flagged for recipients.</span></span>  <br/> |
   
<span data-ttu-id="ac0ef-128">Tous les bits qui ne sont pas spécifiés dans le tableau sont réservés.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-128">All bits that are not specified in the table are reserved.</span></span> <span data-ttu-id="ac0ef-129">Elles doivent être ignorées, mais doivent être conservées si elles sont définies.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-129">They must be ignored, but should be preserved if they are set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ac0ef-130">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ac0ef-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ac0ef-131">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="ac0ef-131">Protocol specifications</span></span>

<span data-ttu-id="ac0ef-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac0ef-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac0ef-133">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ac0ef-134">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac0ef-134">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac0ef-135">Spécifie les propriétés et les opérations liées au marquage.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-135">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ac0ef-136">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ac0ef-136">Header files</span></span>

<span data-ttu-id="ac0ef-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac0ef-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac0ef-138">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac0ef-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ac0ef-139">Mapitags.h</span></span>
  
> <span data-ttu-id="ac0ef-140">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac0ef-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac0ef-141">See also</span></span>



[<span data-ttu-id="ac0ef-142">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ac0ef-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac0ef-143">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ac0ef-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac0ef-144">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ac0ef-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac0ef-145">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ac0ef-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

