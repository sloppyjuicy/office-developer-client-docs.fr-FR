---
title: Propriété canonique PidTagScheduleInfoFreeBusyAway
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyAway
api_type:
- COM
ms.assetid: 7b5d013a-15ac-469a-98c8-3ed1e80f6faf
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7520c473ee9373f8c23c4f5b4bb020291e2be007
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338506"
---
# <a name="pidtagscheduleinfofreebusyaway-canonical-property"></a><span data-ttu-id="033b7-103">Propriété canonique PidTagScheduleInfoFreeBusyAway</span><span class="sxs-lookup"><span data-stu-id="033b7-103">PidTagScheduleInfoFreeBusyAway Canonical Property</span></span>

  
  
<span data-ttu-id="033b7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="033b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="033b7-105">Contient les heures pour lesquelles l'état de disponibilité est défini sur OOF.</span><span class="sxs-lookup"><span data-stu-id="033b7-105">Contains the times for which the free/busy status is set to OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="033b7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="033b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="033b7-107">PR_SCHDINFO_FREEBUSY_OOF</span><span class="sxs-lookup"><span data-stu-id="033b7-107">PR_SCHDINFO_FREEBUSY_OOF</span></span>  <br/> |
|<span data-ttu-id="033b7-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="033b7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="033b7-109">0x6856</span><span class="sxs-lookup"><span data-stu-id="033b7-109">0x6856</span></span>  <br/> |
|<span data-ttu-id="033b7-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="033b7-110">Data type:</span></span>  <br/> |<span data-ttu-id="033b7-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="033b7-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="033b7-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="033b7-112">Area:</span></span>  <br/> |<span data-ttu-id="033b7-113">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="033b7-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="033b7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="033b7-114">Remarks</span></span>

<span data-ttu-id="033b7-115">Le format, le calcul et les contraintes de cette propriété sont les mêmes que ceux de **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), mais font référence à des rendez-vous marqués comme OOF sur le calendrier associé.</span><span class="sxs-lookup"><span data-stu-id="033b7-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="033b7-116">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="033b7-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="033b7-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="033b7-117">Protocol specifications</span></span>

<span data-ttu-id="033b7-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="033b7-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="033b7-119">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="033b7-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="033b7-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="033b7-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="033b7-121">Publie la disponibilité d'un utilisateur ou d'une ressource.</span><span class="sxs-lookup"><span data-stu-id="033b7-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="033b7-122">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="033b7-122">Header files</span></span>

<span data-ttu-id="033b7-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="033b7-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="033b7-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="033b7-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="033b7-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="033b7-125">Mapitags.h</span></span>
  
> <span data-ttu-id="033b7-126">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="033b7-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="033b7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="033b7-127">See also</span></span>



[<span data-ttu-id="033b7-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="033b7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="033b7-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="033b7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="033b7-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="033b7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="033b7-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="033b7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

