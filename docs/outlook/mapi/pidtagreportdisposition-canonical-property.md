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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 62d5b04086e45b6b3d2cfa960472010827d60d6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786590"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="eb492-103">Propriété canonique PidTagReportDisposition</span><span class="sxs-lookup"><span data-stu-id="eb492-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="eb492-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb492-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eb492-105">Indique l’état de l’accusé de réception pour les messages reçus de demande.</span><span class="sxs-lookup"><span data-stu-id="eb492-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb492-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="eb492-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb492-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="eb492-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="eb492-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="eb492-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eb492-109">0 x 0080</span><span class="sxs-lookup"><span data-stu-id="eb492-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="eb492-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="eb492-110">Data type:</span></span>  <br/> |<span data-ttu-id="eb492-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eb492-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="eb492-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="eb492-112">Area:</span></span>  <br/> |<span data-ttu-id="eb492-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="eb492-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb492-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="eb492-114">Remarks</span></span>

<span data-ttu-id="eb492-115">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="eb492-115">The following are valid values:</span></span>
  
- <span data-ttu-id="eb492-116">« supprimer »</span><span class="sxs-lookup"><span data-stu-id="eb492-116">"deleted"</span></span>
    
- <span data-ttu-id="eb492-117">« traitement »</span><span class="sxs-lookup"><span data-stu-id="eb492-117">"processed"</span></span>
    
- <span data-ttu-id="eb492-118">« distribué »</span><span class="sxs-lookup"><span data-stu-id="eb492-118">"dispatched"</span></span>
    
- <span data-ttu-id="eb492-119">« refusé »</span><span class="sxs-lookup"><span data-stu-id="eb492-119">"denied"</span></span>
    
- <span data-ttu-id="eb492-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="eb492-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="eb492-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="eb492-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eb492-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="eb492-122">Protocol specifications</span></span>

<span data-ttu-id="eb492-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="eb492-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="eb492-124">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="eb492-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eb492-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="eb492-125">Header files</span></span>

<span data-ttu-id="eb492-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb492-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb492-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="eb492-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="eb492-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="eb492-128">Mapitags.h</span></span>
  
> <span data-ttu-id="eb492-129">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="eb492-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb492-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb492-130">See also</span></span>



[<span data-ttu-id="eb492-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="eb492-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb492-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="eb492-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb492-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="eb492-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb492-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="eb492-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

