---
title: Propriété canonique PidTagFlagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 38df67757082bd12e008e56632ec7e6961ba9d42
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785993"
---
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="a7052-103">Propriété canonique PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="a7052-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="a7052-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7052-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7052-105">Spécifie l’état de l’indicateur de l’objet du message.</span><span class="sxs-lookup"><span data-stu-id="a7052-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7052-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a7052-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7052-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="a7052-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="a7052-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a7052-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7052-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="a7052-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="a7052-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a7052-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7052-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a7052-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a7052-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="a7052-112">Area:</span></span>  <br/> |<span data-ttu-id="a7052-113">Divers</span><span class="sxs-lookup"><span data-stu-id="a7052-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7052-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7052-114">Remarks</span></span>

<span data-ttu-id="a7052-115">Cette propriété ne doit pas exister sur un objet liées à la réunion, et il ne doit pas exister sur un objet task.</span><span class="sxs-lookup"><span data-stu-id="a7052-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="a7052-116">Lorsque la valeur sur d’autres objets de message, vous devez définir cette propriété sur une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a7052-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="a7052-117">**Valeur numérique**</span><span class="sxs-lookup"><span data-stu-id="a7052-117">**Numeric value**</span></span>|<span data-ttu-id="a7052-118">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a7052-118">**Name**</span></span>|<span data-ttu-id="a7052-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="a7052-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a7052-120">Absent</span><span class="sxs-lookup"><span data-stu-id="a7052-120">Not present</span></span>  <br/> |<span data-ttu-id="a7052-121">S/O</span><span class="sxs-lookup"><span data-stu-id="a7052-121">N/A</span></span>  <br/> |<span data-ttu-id="a7052-122">Sans indicateur</span><span class="sxs-lookup"><span data-stu-id="a7052-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="a7052-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a7052-123">0x00000001</span></span>  <br/> |<span data-ttu-id="a7052-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="a7052-124">followupComplete</span></span>  <br/> |<span data-ttu-id="a7052-125">Marqué comme terminé</span><span class="sxs-lookup"><span data-stu-id="a7052-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="a7052-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a7052-126">0x00000002</span></span>  <br/> |<span data-ttu-id="a7052-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="a7052-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="a7052-128">Marqué d’un indicateur</span><span class="sxs-lookup"><span data-stu-id="a7052-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a7052-129">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a7052-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7052-130">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="a7052-130">Protocol specifications</span></span>

<span data-ttu-id="a7052-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7052-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7052-132">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="a7052-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a7052-133">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7052-133">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7052-134">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="a7052-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7052-135">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a7052-135">Header files</span></span>

<span data-ttu-id="a7052-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7052-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7052-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a7052-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7052-138">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="a7052-138">Mapitags.h</span></span>
  
> <span data-ttu-id="a7052-139">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="a7052-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7052-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7052-140">See also</span></span>



[<span data-ttu-id="a7052-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a7052-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7052-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a7052-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7052-143">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a7052-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7052-144">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="a7052-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

