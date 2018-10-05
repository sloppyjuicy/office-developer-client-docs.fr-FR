---
title: Propriété canonique PidLidMeetingType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d2b00c67984d090274a17028ee74e46bee482e2b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399633"
---
# <a name="pidlidmeetingtype-canonical-property"></a><span data-ttu-id="0c687-103">Propriété canonique PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="0c687-103">PidLidMeetingType Canonical Property</span></span>

  
  
<span data-ttu-id="0c687-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c687-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c687-105">Indique le type de demande de réunion ou de mise à jour de la réunion.</span><span class="sxs-lookup"><span data-stu-id="0c687-105">Indicates the type of meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c687-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0c687-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c687-107">dispidMeetingType</span><span class="sxs-lookup"><span data-stu-id="0c687-107">dispidMeetingType</span></span>  <br/> |
|<span data-ttu-id="0c687-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="0c687-108">Property set:</span></span>  <br/> |<span data-ttu-id="0c687-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="0c687-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="0c687-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="0c687-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0c687-111">0x00000026</span><span class="sxs-lookup"><span data-stu-id="0c687-111">0x00000026</span></span>  <br/> |
|<span data-ttu-id="0c687-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0c687-112">Data type:</span></span>  <br/> |<span data-ttu-id="0c687-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0c687-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0c687-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0c687-114">Area:</span></span>  <br/> |<span data-ttu-id="0c687-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="0c687-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c687-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c687-116">Remarks</span></span>

<span data-ttu-id="0c687-117">La valeur de cette propriété doit avoir une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="0c687-117">The value of this property must be set to one of the following:</span></span>
  
|<span data-ttu-id="0c687-118">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="0c687-118">**Property**</span></span>|<span data-ttu-id="0c687-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="0c687-119">**Value**</span></span>|<span data-ttu-id="0c687-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="0c687-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0c687-121">mtgEmpty</span><span class="sxs-lookup"><span data-stu-id="0c687-121">mtgEmpty</span></span>  <br/> |<span data-ttu-id="0c687-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c687-122">0x00000000</span></span>  <br/> |<span data-ttu-id="0c687-123">Non spécifié.</span><span class="sxs-lookup"><span data-stu-id="0c687-123">Unspecified.</span></span>  <br/> |
|<span data-ttu-id="0c687-124">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="0c687-124">mtgRequest</span></span>  <br/> |<span data-ttu-id="0c687-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0c687-125">0x00000001</span></span>  <br/> |<span data-ttu-id="0c687-126">Demande de réunion initiale.</span><span class="sxs-lookup"><span data-stu-id="0c687-126">Initial meeting request.</span></span>  <br/> |
|<span data-ttu-id="0c687-127">mtgFull</span><span class="sxs-lookup"><span data-stu-id="0c687-127">mtgFull</span></span>  <br/> |<span data-ttu-id="0c687-128">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="0c687-128">0x00010000</span></span>  <br/> |<span data-ttu-id="0c687-129">Mise à jour intégrale.</span><span class="sxs-lookup"><span data-stu-id="0c687-129">Full update.</span></span>  <br/> |
|<span data-ttu-id="0c687-130">mtgInfo</span><span class="sxs-lookup"><span data-stu-id="0c687-130">mtgInfo</span></span>  <br/> |<span data-ttu-id="0c687-131">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="0c687-131">0x00020000</span></span>  <br/> |<span data-ttu-id="0c687-132">Mise à jour d’information.</span><span class="sxs-lookup"><span data-stu-id="0c687-132">Informational update.</span></span>  <br/> |
|<span data-ttu-id="0c687-133">mtgOutOfDate</span><span class="sxs-lookup"><span data-stu-id="0c687-133">mtgOutOfDate</span></span>  <br/> |<span data-ttu-id="0c687-134">0 x 00080000</span><span class="sxs-lookup"><span data-stu-id="0c687-134">0x00080000</span></span>  <br/> |<span data-ttu-id="0c687-135">Une nouvelle demande de réunion ou une mise à jour de la réunion a été reçu après celle-ci.</span><span class="sxs-lookup"><span data-stu-id="0c687-135">A newer meeting request or meeting update was received after this one.</span></span>  <br/> |
|<span data-ttu-id="0c687-136">mtgDelegatorCopy</span><span class="sxs-lookup"><span data-stu-id="0c687-136">mtgDelegatorCopy</span></span>  <br/> |<span data-ttu-id="0c687-137">0 x 00100000</span><span class="sxs-lookup"><span data-stu-id="0c687-137">0x00100000</span></span>  <br/> |<span data-ttu-id="0c687-138">Elle est définie sur la copie de la personne qui a délégué lorsqu’un délégué poignées réunion les objets liés.</span><span class="sxs-lookup"><span data-stu-id="0c687-138">This is set on the delegator's copy when a delegate handles meeting-related objects.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0c687-139">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0c687-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0c687-140">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="0c687-140">Protocol specifications</span></span>

<span data-ttu-id="0c687-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c687-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c687-142">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="0c687-142">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0c687-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c687-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c687-144">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="0c687-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0c687-145">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0c687-145">Header files</span></span>

<span data-ttu-id="0c687-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c687-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c687-147">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0c687-147">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c687-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c687-148">See also</span></span>



[<span data-ttu-id="0c687-149">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0c687-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c687-150">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0c687-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c687-151">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0c687-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c687-152">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0c687-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

