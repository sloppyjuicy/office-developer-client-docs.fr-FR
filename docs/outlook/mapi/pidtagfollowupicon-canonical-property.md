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
ms.openlocfilehash: 205b6ddc2b65297d69a2223aab7b745b223ee553
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316281"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="b4be3-103">Propriété canonique PidTagFollowupIcon</span><span class="sxs-lookup"><span data-stu-id="b4be3-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="b4be3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4be3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4be3-105">Spécifie la couleur de l'indicateur de l'objet message.</span><span class="sxs-lookup"><span data-stu-id="b4be3-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4be3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b4be3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4be3-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="b4be3-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="b4be3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b4be3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4be3-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="b4be3-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="b4be3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b4be3-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4be3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b4be3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b4be3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b4be3-112">Area:</span></span>  <br/> |<span data-ttu-id="b4be3-113">Renommer le dossier de messages</span><span class="sxs-lookup"><span data-stu-id="b4be3-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4be3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b4be3-114">Remarks</span></span>

<span data-ttu-id="b4be3-115">Cette propriété ne doit exister que si la valeur de la propriété **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) est définie sur «followupFlagged», ou l'objet message est un objet lié à la réunion.</span><span class="sxs-lookup"><span data-stu-id="b4be3-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="b4be3-116">Cette propriété ne doit pas exister sur un objet Task.</span><span class="sxs-lookup"><span data-stu-id="b4be3-116">This property should not exist on a task object.</span></span> <span data-ttu-id="b4be3-117">Lorsqu'elle est définie sur d'autres objets message, la valeur de cette propriété doit être l'une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4be3-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="b4be3-118">**Valeur numérique**</span><span class="sxs-lookup"><span data-stu-id="b4be3-118">**Numeric value**</span></span>|<span data-ttu-id="b4be3-119">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b4be3-119">**Name**</span></span>|<span data-ttu-id="b4be3-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="b4be3-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b4be3-121">Non présent</span><span class="sxs-lookup"><span data-stu-id="b4be3-121">Not present</span></span>  <br/> |<span data-ttu-id="b4be3-122">S/O</span><span class="sxs-lookup"><span data-stu-id="b4be3-122">N/A</span></span>  <br/> |<span data-ttu-id="b4be3-123">Aucune couleur</span><span class="sxs-lookup"><span data-stu-id="b4be3-123">No color</span></span>  <br/> |
|<span data-ttu-id="b4be3-124">0,1</span><span class="sxs-lookup"><span data-stu-id="b4be3-124">1</span></span>  <br/> |<span data-ttu-id="b4be3-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="b4be3-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="b4be3-126">Drapeau violet</span><span class="sxs-lookup"><span data-stu-id="b4be3-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="b4be3-127">n°2</span><span class="sxs-lookup"><span data-stu-id="b4be3-127">2</span></span>  <br/> |<span data-ttu-id="b4be3-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="b4be3-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="b4be3-129">Drapeau Orange</span><span class="sxs-lookup"><span data-stu-id="b4be3-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="b4be3-130">3</span><span class="sxs-lookup"><span data-stu-id="b4be3-130">3</span></span>  <br/> |<span data-ttu-id="b4be3-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="b4be3-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="b4be3-132">Drapeau vert</span><span class="sxs-lookup"><span data-stu-id="b4be3-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="b4be3-133">4</span><span class="sxs-lookup"><span data-stu-id="b4be3-133">4</span></span>  <br/> |<span data-ttu-id="b4be3-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="b4be3-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="b4be3-135">Drapeau jaune</span><span class="sxs-lookup"><span data-stu-id="b4be3-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="b4be3-136">disque</span><span class="sxs-lookup"><span data-stu-id="b4be3-136">5</span></span>  <br/> |<span data-ttu-id="b4be3-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="b4be3-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="b4be3-138">Drapeau bleu</span><span class="sxs-lookup"><span data-stu-id="b4be3-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="b4be3-139">6.x</span><span class="sxs-lookup"><span data-stu-id="b4be3-139">6</span></span>  <br/> |<span data-ttu-id="b4be3-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="b4be3-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="b4be3-141">Drapeau rouge</span><span class="sxs-lookup"><span data-stu-id="b4be3-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b4be3-142">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="b4be3-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b4be3-143">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="b4be3-143">Protocol specifications</span></span>

<span data-ttu-id="b4be3-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4be3-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4be3-145">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="b4be3-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b4be3-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4be3-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4be3-147">Spécifie les propriétés et les opérations relatives au marquage.</span><span class="sxs-lookup"><span data-stu-id="b4be3-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b4be3-148">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="b4be3-148">Header files</span></span>

<span data-ttu-id="b4be3-149">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b4be3-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4be3-150">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b4be3-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4be3-151">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b4be3-151">Mapitags.h</span></span>
  
> <span data-ttu-id="b4be3-152">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="b4be3-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4be3-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4be3-153">See also</span></span>



[<span data-ttu-id="b4be3-154">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b4be3-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4be3-155">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b4be3-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4be3-156">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b4be3-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4be3-157">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b4be3-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

