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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 205b6ddc2b65297d69a2223aab7b745b223ee553
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316281"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="d4663-103">Propriété canonique PidTagFollowupIcon</span><span class="sxs-lookup"><span data-stu-id="d4663-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="d4663-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4663-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4663-105">Spécifie la couleur d’indicateur de l’objet message.</span><span class="sxs-lookup"><span data-stu-id="d4663-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d4663-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d4663-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4663-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="d4663-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="d4663-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d4663-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d4663-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="d4663-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="d4663-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d4663-110">Data type:</span></span>  <br/> |<span data-ttu-id="d4663-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d4663-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d4663-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d4663-112">Area:</span></span>  <br/> |<span data-ttu-id="d4663-113">Renommer le dossier des messages</span><span class="sxs-lookup"><span data-stu-id="d4663-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4663-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d4663-114">Remarks</span></span>

<span data-ttu-id="d4663-115">Cette propriété ne doit pas exister, sauf si la valeur de la propriété **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) est définie sur « followupFlagged » ou si l’objet message est un objet lié à la réunion.</span><span class="sxs-lookup"><span data-stu-id="d4663-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="d4663-116">Cette propriété ne doit pas exister sur un objet de tâche.</span><span class="sxs-lookup"><span data-stu-id="d4663-116">This property should not exist on a task object.</span></span> <span data-ttu-id="d4663-117">Lorsqu’elle est définie sur d’autres objets de message, cette propriété doit être définie sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d4663-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="d4663-118">**Valeur numérique**</span><span class="sxs-lookup"><span data-stu-id="d4663-118">**Numeric value**</span></span>|<span data-ttu-id="d4663-119">**Name**</span><span class="sxs-lookup"><span data-stu-id="d4663-119">**Name**</span></span>|<span data-ttu-id="d4663-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="d4663-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d4663-121">Non présent</span><span class="sxs-lookup"><span data-stu-id="d4663-121">Not present</span></span>  <br/> |<span data-ttu-id="d4663-122">S/O</span><span class="sxs-lookup"><span data-stu-id="d4663-122">N/A</span></span>  <br/> |<span data-ttu-id="d4663-123">Aucune couleur</span><span class="sxs-lookup"><span data-stu-id="d4663-123">No color</span></span>  <br/> |
|<span data-ttu-id="d4663-124">1</span><span class="sxs-lookup"><span data-stu-id="d4663-124">1</span></span>  <br/> |<span data-ttu-id="d4663-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="d4663-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="d4663-126">Indicateur violet</span><span class="sxs-lookup"><span data-stu-id="d4663-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="d4663-127">2</span><span class="sxs-lookup"><span data-stu-id="d4663-127">2</span></span>  <br/> |<span data-ttu-id="d4663-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="d4663-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="d4663-129">Indicateur orange</span><span class="sxs-lookup"><span data-stu-id="d4663-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="d4663-130">3</span><span class="sxs-lookup"><span data-stu-id="d4663-130">3</span></span>  <br/> |<span data-ttu-id="d4663-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="d4663-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="d4663-132">Indicateur vert</span><span class="sxs-lookup"><span data-stu-id="d4663-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="d4663-133">4 </span><span class="sxs-lookup"><span data-stu-id="d4663-133">4</span></span>  <br/> |<span data-ttu-id="d4663-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="d4663-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="d4663-135">Indicateur jaune</span><span class="sxs-lookup"><span data-stu-id="d4663-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="d4663-136">5 </span><span class="sxs-lookup"><span data-stu-id="d4663-136">5</span></span>  <br/> |<span data-ttu-id="d4663-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="d4663-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="d4663-138">Indicateur bleu</span><span class="sxs-lookup"><span data-stu-id="d4663-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="d4663-139">6 </span><span class="sxs-lookup"><span data-stu-id="d4663-139">6</span></span>  <br/> |<span data-ttu-id="d4663-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="d4663-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="d4663-141">Indicateur rouge</span><span class="sxs-lookup"><span data-stu-id="d4663-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d4663-142">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d4663-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d4663-143">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="d4663-143">Protocol specifications</span></span>

<span data-ttu-id="d4663-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4663-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4663-145">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="d4663-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d4663-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4663-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4663-147">Spécifie les propriétés et les opérations liées au marquage.</span><span class="sxs-lookup"><span data-stu-id="d4663-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d4663-148">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d4663-148">Header files</span></span>

<span data-ttu-id="d4663-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d4663-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4663-150">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d4663-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="d4663-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d4663-151">Mapitags.h</span></span>
  
> <span data-ttu-id="d4663-152">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="d4663-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4663-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4663-153">See also</span></span>



[<span data-ttu-id="d4663-154">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d4663-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4663-155">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d4663-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4663-156">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d4663-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4663-157">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d4663-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

