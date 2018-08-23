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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1f068ce2e8d98caa7d8733a182c051a820848333
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579808"
---
# <a name="pidtagscheduleinfofreebusybusy-canonical-property"></a><span data-ttu-id="3bddc-103">Propriété canonique PidTagScheduleInfoFreeBusyBusy</span><span class="sxs-lookup"><span data-stu-id="3bddc-103">PidTagScheduleInfoFreeBusyBusy Canonical Property</span></span>

  
  
<span data-ttu-id="3bddc-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bddc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bddc-105">Contient les blocs de temps dont le statut est occupé (e).</span><span class="sxs-lookup"><span data-stu-id="3bddc-105">Contains the blocks of time for which the status is busy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3bddc-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3bddc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3bddc-107">PR_SCHDINFO_FREEBUSY_BUSY</span><span class="sxs-lookup"><span data-stu-id="3bddc-107">PR_SCHDINFO_FREEBUSY_BUSY</span></span>  <br/> |
|<span data-ttu-id="3bddc-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3bddc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3bddc-109">0x6854</span><span class="sxs-lookup"><span data-stu-id="3bddc-109">0x6854</span></span>  <br/> |
|<span data-ttu-id="3bddc-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3bddc-110">Data type:</span></span>  <br/> |<span data-ttu-id="3bddc-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="3bddc-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="3bddc-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3bddc-112">Area:</span></span>  <br/> |<span data-ttu-id="3bddc-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="3bddc-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3bddc-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3bddc-114">Remarks</span></span>

<span data-ttu-id="3bddc-115">Format, calcul les contraintes de cette propriété sont les mêmes que ceux du **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) mais faire référence à des rendez-vous sont marquées comme occupé (e) sur l’objet calendar associé.</span><span class="sxs-lookup"><span data-stu-id="3bddc-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3bddc-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3bddc-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3bddc-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="3bddc-117">Protocol specifications</span></span>

<span data-ttu-id="3bddc-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3bddc-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3bddc-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="3bddc-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3bddc-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3bddc-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3bddc-121">Publie la disponibilité d’un utilisateur ou une ressource.</span><span class="sxs-lookup"><span data-stu-id="3bddc-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3bddc-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3bddc-122">Header files</span></span>

<span data-ttu-id="3bddc-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3bddc-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3bddc-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3bddc-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="3bddc-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="3bddc-125">Mapitags.h</span></span>
  
> <span data-ttu-id="3bddc-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="3bddc-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3bddc-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bddc-127">See also</span></span>



[<span data-ttu-id="3bddc-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3bddc-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3bddc-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3bddc-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3bddc-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3bddc-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3bddc-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3bddc-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

