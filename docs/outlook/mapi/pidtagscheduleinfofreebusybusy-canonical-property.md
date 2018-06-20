---
title: Propriété canonique PidTagScheduleInfoFreeBusyBusy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyBusy
api_type:
- COM
ms.assetid: 84d9c5b5-e734-4c07-b4cc-1d7b13c1ed19
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e0c59b569f4f01584fd65a7c3e13d6daac69d8a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786717"
---
# <a name="pidtagscheduleinfofreebusybusy-canonical-property"></a><span data-ttu-id="4ac8d-103">Propriété canonique PidTagScheduleInfoFreeBusyBusy</span><span class="sxs-lookup"><span data-stu-id="4ac8d-103">PidTagScheduleInfoFreeBusyBusy Canonical Property</span></span>

  
  
<span data-ttu-id="4ac8d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4ac8d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4ac8d-105">Contient les blocs de temps dont le statut est occupé (e).</span><span class="sxs-lookup"><span data-stu-id="4ac8d-105">Contains the blocks of time for which the status is busy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ac8d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4ac8d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4ac8d-107">PR_SCHDINFO_FREEBUSY_BUSY</span><span class="sxs-lookup"><span data-stu-id="4ac8d-107">PR_SCHDINFO_FREEBUSY_BUSY</span></span>  <br/> |
|<span data-ttu-id="4ac8d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4ac8d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4ac8d-109">0x6854</span><span class="sxs-lookup"><span data-stu-id="4ac8d-109">0x6854</span></span>  <br/> |
|<span data-ttu-id="4ac8d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4ac8d-110">Data type:</span></span>  <br/> |<span data-ttu-id="4ac8d-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="4ac8d-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="4ac8d-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="4ac8d-112">Area:</span></span>  <br/> |<span data-ttu-id="4ac8d-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="4ac8d-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ac8d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4ac8d-114">Remarks</span></span>

<span data-ttu-id="4ac8d-115">Format, calcul les contraintes de cette propriété sont les mêmes que ceux du **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) mais faire référence à des rendez-vous sont marquées comme occupé (e) sur l’objet calendar associé.</span><span class="sxs-lookup"><span data-stu-id="4ac8d-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4ac8d-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4ac8d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4ac8d-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="4ac8d-117">Protocol specifications</span></span>

<span data-ttu-id="4ac8d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ac8d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ac8d-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="4ac8d-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4ac8d-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ac8d-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ac8d-121">Publie la disponibilité d’un utilisateur ou une ressource.</span><span class="sxs-lookup"><span data-stu-id="4ac8d-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4ac8d-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4ac8d-122">Header files</span></span>

<span data-ttu-id="4ac8d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4ac8d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="4ac8d-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4ac8d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="4ac8d-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="4ac8d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="4ac8d-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="4ac8d-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ac8d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ac8d-127">See also</span></span>



[<span data-ttu-id="4ac8d-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4ac8d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4ac8d-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4ac8d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4ac8d-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4ac8d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4ac8d-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="4ac8d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

