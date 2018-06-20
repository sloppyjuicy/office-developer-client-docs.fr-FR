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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c1096df0eff4b43239978620f4ccf2e9d221095a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786731"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a><span data-ttu-id="52792-103">Propriété canonique PidTagScheduleInfoMonthsMerged</span><span class="sxs-lookup"><span data-stu-id="52792-103">PidTagScheduleInfoMonthsMerged Canonical Property</span></span>

  
  
<span data-ttu-id="52792-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52792-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52792-105">Contient une liste des mois pour les données et de disponibilité de type occupé (e) ou une absence du bureau (OOF) message est présente dans le message et de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="52792-105">Contains a list of the months for which free/busy data of type busy or an out of office (OOF) message is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52792-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="52792-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52792-107">PR_SCHDINFO_MONTHS_MERGED</span><span class="sxs-lookup"><span data-stu-id="52792-107">PR_SCHDINFO_MONTHS_MERGED</span></span>  <br/> |
|<span data-ttu-id="52792-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="52792-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52792-109">0x684F</span><span class="sxs-lookup"><span data-stu-id="52792-109">0x684F</span></span>  <br/> |
|<span data-ttu-id="52792-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="52792-110">Data type:</span></span>  <br/> |<span data-ttu-id="52792-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="52792-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="52792-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="52792-112">Area:</span></span>  <br/> |<span data-ttu-id="52792-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="52792-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52792-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="52792-114">Remarks</span></span>

<span data-ttu-id="52792-115">Événements de type disponible/occupé provisoire ne sont pas inclus dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="52792-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="52792-116">La syntaxe/format et les contraintes de cette propriété sont les mêmes que ceux du **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) mais faire référence à un rendez-vous qui sont marqués absent du bureau ou occupé (e) sur l’objet calendar associé.</span><span class="sxs-lookup"><span data-stu-id="52792-116">The syntax/format and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked OOF or Busy on the associated calendar object.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="52792-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="52792-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52792-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="52792-118">Protocol specifications</span></span>

<span data-ttu-id="52792-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52792-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52792-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="52792-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="52792-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52792-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52792-122">Publie la disponibilité d’un utilisateur ou une ressource.</span><span class="sxs-lookup"><span data-stu-id="52792-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="52792-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="52792-123">Header files</span></span>

<span data-ttu-id="52792-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52792-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="52792-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="52792-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="52792-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="52792-126">Mapitags.h</span></span>
  
> <span data-ttu-id="52792-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="52792-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52792-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52792-128">See also</span></span>



[<span data-ttu-id="52792-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="52792-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52792-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="52792-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52792-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="52792-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52792-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="52792-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

