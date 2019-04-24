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
ms.openlocfilehash: bca8fccaa43bb3157b3d4e2af7d6aafa64972b41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316295"
---
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="7f767-103">Propriété canonique PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="7f767-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="7f767-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f767-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f767-105">Spécifie l'état de l'indicateur de l'objet message.</span><span class="sxs-lookup"><span data-stu-id="7f767-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f767-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7f767-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f767-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="7f767-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="7f767-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="7f767-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f767-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="7f767-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="7f767-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7f767-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f767-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7f767-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7f767-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="7f767-112">Area:</span></span>  <br/> |<span data-ttu-id="7f767-113">Divers</span><span class="sxs-lookup"><span data-stu-id="7f767-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f767-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f767-114">Remarks</span></span>

<span data-ttu-id="7f767-115">Cette propriété ne doit pas exister sur un objet lié à une réunion et elle ne doit pas exister sur un objet Task.</span><span class="sxs-lookup"><span data-stu-id="7f767-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="7f767-116">Lorsqu'elle est définie sur d'autres objets message, la valeur de cette propriété doit être l'une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="7f767-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="7f767-117">**Valeur numérique**</span><span class="sxs-lookup"><span data-stu-id="7f767-117">**Numeric value**</span></span>|<span data-ttu-id="7f767-118">**Nom**</span><span class="sxs-lookup"><span data-stu-id="7f767-118">**Name**</span></span>|<span data-ttu-id="7f767-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="7f767-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7f767-120">Non présent</span><span class="sxs-lookup"><span data-stu-id="7f767-120">Not present</span></span>  <br/> |<span data-ttu-id="7f767-121">S/O</span><span class="sxs-lookup"><span data-stu-id="7f767-121">N/A</span></span>  <br/> |<span data-ttu-id="7f767-122">Unindicateur</span><span class="sxs-lookup"><span data-stu-id="7f767-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="7f767-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7f767-123">0x00000001</span></span>  <br/> |<span data-ttu-id="7f767-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="7f767-124">followupComplete</span></span>  <br/> |<span data-ttu-id="7f767-125">Indicateur complet</span><span class="sxs-lookup"><span data-stu-id="7f767-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="7f767-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7f767-126">0x00000002</span></span>  <br/> |<span data-ttu-id="7f767-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="7f767-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="7f767-128">Marqué d’un indicateur</span><span class="sxs-lookup"><span data-stu-id="7f767-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7f767-129">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="7f767-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7f767-130">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="7f767-130">Protocol specifications</span></span>

<span data-ttu-id="7f767-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f767-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f767-132">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="7f767-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7f767-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f767-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f767-134">Spécifie les propriétés et les opérations relatives au marquage.</span><span class="sxs-lookup"><span data-stu-id="7f767-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7f767-135">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="7f767-135">Header files</span></span>

<span data-ttu-id="7f767-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7f767-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f767-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7f767-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f767-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7f767-138">Mapitags.h</span></span>
  
> <span data-ttu-id="7f767-139">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="7f767-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f767-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f767-140">See also</span></span>



[<span data-ttu-id="7f767-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7f767-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f767-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7f767-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f767-143">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7f767-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f767-144">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="7f767-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

