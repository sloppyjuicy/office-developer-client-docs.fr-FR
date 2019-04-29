---
title: Propriété canonique PidTagReportDisposition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 56b9e7bd-eece-4264-8ee5-a1bcbec4f35c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dae31959cddad7ad61ea32f2372ea34bdbff658e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423705"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="be915-103">Propriété canonique PidTagReportDisposition</span><span class="sxs-lookup"><span data-stu-id="be915-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="be915-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be915-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be915-105">Indique l'état de réception des messages qui demandent des accusés de réception.</span><span class="sxs-lookup"><span data-stu-id="be915-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be915-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="be915-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be915-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="be915-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="be915-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="be915-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be915-109">0x0080</span><span class="sxs-lookup"><span data-stu-id="be915-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="be915-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="be915-110">Data type:</span></span>  <br/> |<span data-ttu-id="be915-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="be915-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="be915-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="be915-112">Area:</span></span>  <br/> |<span data-ttu-id="be915-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="be915-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be915-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="be915-114">Remarks</span></span>

<span data-ttu-id="be915-115">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="be915-115">The following are valid values:</span></span>
  
- <span data-ttu-id="be915-116">supprimés</span><span class="sxs-lookup"><span data-stu-id="be915-116">"deleted"</span></span>
    
- <span data-ttu-id="be915-117">traiter</span><span class="sxs-lookup"><span data-stu-id="be915-117">"processed"</span></span>
    
- <span data-ttu-id="be915-118">distribuées</span><span class="sxs-lookup"><span data-stu-id="be915-118">"dispatched"</span></span>
    
- <span data-ttu-id="be915-119">Verr</span><span class="sxs-lookup"><span data-stu-id="be915-119">"denied"</span></span>
    
- <span data-ttu-id="be915-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="be915-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="be915-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="be915-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="be915-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="be915-122">Protocol specifications</span></span>

<span data-ttu-id="be915-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="be915-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="be915-124">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="be915-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="be915-125">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="be915-125">Header files</span></span>

<span data-ttu-id="be915-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="be915-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="be915-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="be915-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="be915-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="be915-128">Mapitags.h</span></span>
  
> <span data-ttu-id="be915-129">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="be915-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be915-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be915-130">See also</span></span>



[<span data-ttu-id="be915-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="be915-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be915-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="be915-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be915-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="be915-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be915-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="be915-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

