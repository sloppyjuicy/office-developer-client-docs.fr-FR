---
title: Propriété canonique PidTagScheduleInfoMonthsAway
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsAway
api_type:
- COM
ms.assetid: 282a8ba1-b786-4d17-b6c5-17e935e59a6b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 90df272a70fd4133a780f205c93b42f26ed1ae96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303408"
---
# <a name="pidtagscheduleinfomonthsaway-canonical-property"></a><span data-ttu-id="87e47-103">Propriété canonique PidTagScheduleInfoMonthsAway</span><span class="sxs-lookup"><span data-stu-id="87e47-103">PidTagScheduleInfoMonthsAway Canonical Property</span></span>

  
  
<span data-ttu-id="87e47-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87e47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87e47-105">Contient une liste des mois pendant lesquels des données de type absence du bureau (OOF) sont présentes dans le message de libre/occupé.</span><span class="sxs-lookup"><span data-stu-id="87e47-105">Contains a list of the months for which free/busy data of type out of office (OOF) is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87e47-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="87e47-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87e47-107">PR_SCHDINFO_MONTHS_OOF</span><span class="sxs-lookup"><span data-stu-id="87e47-107">PR_SCHDINFO_MONTHS_OOF</span></span>  <br/> |
|<span data-ttu-id="87e47-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="87e47-108">Identifier:</span></span>  <br/> |<span data-ttu-id="87e47-109">0x6855</span><span class="sxs-lookup"><span data-stu-id="87e47-109">0x6855</span></span>  <br/> |
|<span data-ttu-id="87e47-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="87e47-110">Data type:</span></span>  <br/> |<span data-ttu-id="87e47-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="87e47-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="87e47-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="87e47-112">Area:</span></span>  <br/> |<span data-ttu-id="87e47-113">Libre/Occupé</span><span class="sxs-lookup"><span data-stu-id="87e47-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87e47-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="87e47-114">Remarks</span></span>

<span data-ttu-id="87e47-115">Le format, le calcul et les contraintes de cette propriété sont identiques à ceux de **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), mais font référence aux rendez-vous qui sont marqués comme absence du bureau (OOF) sur l’objet calendrier associé.</span><span class="sxs-lookup"><span data-stu-id="87e47-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked out of office (OOF) on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="87e47-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="87e47-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87e47-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="87e47-117">Protocol specifications</span></span>

<span data-ttu-id="87e47-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87e47-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87e47-119">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="87e47-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="87e47-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87e47-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87e47-121">Publie la disponibilité d’un utilisateur ou d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="87e47-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87e47-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="87e47-122">Header files</span></span>

<span data-ttu-id="87e47-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87e47-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="87e47-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="87e47-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="87e47-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="87e47-125">Mapitags.h</span></span>
  
> <span data-ttu-id="87e47-126">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="87e47-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87e47-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87e47-127">See also</span></span>



[<span data-ttu-id="87e47-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="87e47-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87e47-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="87e47-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87e47-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="87e47-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87e47-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="87e47-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

