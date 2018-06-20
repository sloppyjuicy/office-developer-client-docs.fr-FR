---
title: Propriété canonique PidTagFollowupIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFollowupIcon
api_type:
- HeaderDef
ms.assetid: 374cef41-141a-491b-8dd1-eaf1a2044204
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 39840f27d67daca625daea08555ab89d5a362e63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786012"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="cec7d-103">Propriété canonique PidTagFollowupIcon</span><span class="sxs-lookup"><span data-stu-id="cec7d-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="cec7d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cec7d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cec7d-105">Spécifie la couleur de l’objet du message.</span><span class="sxs-lookup"><span data-stu-id="cec7d-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cec7d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="cec7d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cec7d-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="cec7d-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="cec7d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="cec7d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cec7d-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="cec7d-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="cec7d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="cec7d-110">Data type:</span></span>  <br/> |<span data-ttu-id="cec7d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cec7d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cec7d-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="cec7d-112">Area:</span></span>  <br/> |<span data-ttu-id="cec7d-113">Renommer le dossier de message</span><span class="sxs-lookup"><span data-stu-id="cec7d-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cec7d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="cec7d-114">Remarks</span></span>

<span data-ttu-id="cec7d-115">Cette propriété ne doit pas exister, sauf si la valeur de la propriété **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) est définie sur « followupFlagged » ou l’objet du message est un objet liées à la réunion.</span><span class="sxs-lookup"><span data-stu-id="cec7d-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="cec7d-116">Cette propriété ne doit pas exister sur un objet task.</span><span class="sxs-lookup"><span data-stu-id="cec7d-116">This property should not exist on a task object.</span></span> <span data-ttu-id="cec7d-117">Lorsque la valeur sur d’autres objets de message, cette propriété doit avoir une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="cec7d-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="cec7d-118">**Valeur numérique**</span><span class="sxs-lookup"><span data-stu-id="cec7d-118">**Numeric value**</span></span>|<span data-ttu-id="cec7d-119">**Nom**</span><span class="sxs-lookup"><span data-stu-id="cec7d-119">**Name**</span></span>|<span data-ttu-id="cec7d-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="cec7d-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cec7d-121">Absent</span><span class="sxs-lookup"><span data-stu-id="cec7d-121">Not present</span></span>  <br/> |<span data-ttu-id="cec7d-122">S/O</span><span class="sxs-lookup"><span data-stu-id="cec7d-122">N/A</span></span>  <br/> |<span data-ttu-id="cec7d-123">Aucune couleur</span><span class="sxs-lookup"><span data-stu-id="cec7d-123">No color</span></span>  <br/> |
|<span data-ttu-id="cec7d-124">1</span><span class="sxs-lookup"><span data-stu-id="cec7d-124">1</span></span>  <br/> |<span data-ttu-id="cec7d-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="cec7d-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="cec7d-126">Indicateur violet</span><span class="sxs-lookup"><span data-stu-id="cec7d-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="cec7d-127">2</span><span class="sxs-lookup"><span data-stu-id="cec7d-127">2</span></span>  <br/> |<span data-ttu-id="cec7d-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="cec7d-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="cec7d-129">Indicateur orange</span><span class="sxs-lookup"><span data-stu-id="cec7d-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="cec7d-130">3</span><span class="sxs-lookup"><span data-stu-id="cec7d-130">3</span></span>  <br/> |<span data-ttu-id="cec7d-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="cec7d-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="cec7d-132">Indicateur vert</span><span class="sxs-lookup"><span data-stu-id="cec7d-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="cec7d-133">4</span><span class="sxs-lookup"><span data-stu-id="cec7d-133">4</span></span>  <br/> |<span data-ttu-id="cec7d-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="cec7d-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="cec7d-135">Indicateur jaune</span><span class="sxs-lookup"><span data-stu-id="cec7d-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="cec7d-136">5</span><span class="sxs-lookup"><span data-stu-id="cec7d-136">5</span></span>  <br/> |<span data-ttu-id="cec7d-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="cec7d-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="cec7d-138">Indicateur bleu</span><span class="sxs-lookup"><span data-stu-id="cec7d-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="cec7d-139">6</span><span class="sxs-lookup"><span data-stu-id="cec7d-139">6</span></span>  <br/> |<span data-ttu-id="cec7d-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="cec7d-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="cec7d-141">Indicateur rouge</span><span class="sxs-lookup"><span data-stu-id="cec7d-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="cec7d-142">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="cec7d-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cec7d-143">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="cec7d-143">Protocol specifications</span></span>

<span data-ttu-id="cec7d-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cec7d-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cec7d-145">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="cec7d-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cec7d-146">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cec7d-146">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cec7d-147">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="cec7d-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cec7d-148">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="cec7d-148">Header files</span></span>

<span data-ttu-id="cec7d-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cec7d-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="cec7d-150">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="cec7d-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="cec7d-151">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="cec7d-151">Mapitags.h</span></span>
  
> <span data-ttu-id="cec7d-152">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="cec7d-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cec7d-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cec7d-153">See also</span></span>



[<span data-ttu-id="cec7d-154">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="cec7d-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cec7d-155">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="cec7d-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cec7d-156">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="cec7d-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cec7d-157">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="cec7d-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

