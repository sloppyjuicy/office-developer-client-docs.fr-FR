---
title: Propriété canonique PidTagScheduleInfoMonthsMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsMerged
api_type:
- COM
ms.assetid: b13b5d7b-413e-4405-8a35-0422477a9e86
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 53bc27b4ddd05b4a52328c605a6d4f673c91afd2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383820"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a><span data-ttu-id="25864-103">Propriété canonique PidTagScheduleInfoMonthsMerged</span><span class="sxs-lookup"><span data-stu-id="25864-103">PidTagScheduleInfoMonthsMerged Canonical Property</span></span>

  
  
<span data-ttu-id="25864-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25864-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25864-105">Contient une liste des mois pour les données et de disponibilité de type occupé (e) ou une absence du bureau (OOF) message est présente dans le message et de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="25864-105">Contains a list of the months for which free/busy data of type busy or an out of office (OOF) message is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25864-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="25864-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25864-107">PR_SCHDINFO_MONTHS_MERGED</span><span class="sxs-lookup"><span data-stu-id="25864-107">PR_SCHDINFO_MONTHS_MERGED</span></span>  <br/> |
|<span data-ttu-id="25864-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="25864-108">Identifier:</span></span>  <br/> |<span data-ttu-id="25864-109">0x684F</span><span class="sxs-lookup"><span data-stu-id="25864-109">0x684F</span></span>  <br/> |
|<span data-ttu-id="25864-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="25864-110">Data type:</span></span>  <br/> |<span data-ttu-id="25864-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="25864-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="25864-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="25864-112">Area:</span></span>  <br/> |<span data-ttu-id="25864-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="25864-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25864-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="25864-114">Remarks</span></span>

<span data-ttu-id="25864-115">Événements de type disponible/occupé provisoire ne sont pas inclus dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="25864-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="25864-116">La syntaxe/format et les contraintes de cette propriété sont les mêmes que ceux du **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) mais faire référence à un rendez-vous qui sont marqués absent du bureau ou occupé (e) sur l’objet calendar associé.</span><span class="sxs-lookup"><span data-stu-id="25864-116">The syntax/format and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked OOF or Busy on the associated calendar object.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="25864-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="25864-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25864-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="25864-118">Protocol specifications</span></span>

<span data-ttu-id="25864-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25864-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25864-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="25864-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="25864-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25864-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25864-122">Publie la disponibilité d’un utilisateur ou une ressource.</span><span class="sxs-lookup"><span data-stu-id="25864-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25864-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="25864-123">Header files</span></span>

<span data-ttu-id="25864-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25864-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="25864-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="25864-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="25864-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="25864-126">Mapitags.h</span></span>
  
> <span data-ttu-id="25864-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="25864-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25864-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25864-128">See also</span></span>



[<span data-ttu-id="25864-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="25864-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25864-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="25864-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25864-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="25864-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25864-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="25864-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

