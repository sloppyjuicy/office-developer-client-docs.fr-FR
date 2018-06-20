---
title: Propriété canonique PidTagOriginatorNonDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorNonDeliveryReportRequested
api_type:
- COM
ms.assetid: 0a19ba44-abb0-4868-9d7d-75184058d4c0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 841d2b14efc781d89727b0c7ed677f527526a4ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786357"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="5daac-103">Propriété canonique PidTagOriginatorNonDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="5daac-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="5daac-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5daac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5daac-105">Contient la valeur TRUE si un expéditeur du message demande un rapport de non-remise pour un destinataire particulier.</span><span class="sxs-lookup"><span data-stu-id="5daac-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5daac-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5daac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5daac-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="5daac-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="5daac-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5daac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5daac-109">0x0C08</span><span class="sxs-lookup"><span data-stu-id="5daac-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="5daac-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5daac-110">Data type:</span></span>  <br/> |<span data-ttu-id="5daac-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5daac-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5daac-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="5daac-112">Area:</span></span>  <br/> |<span data-ttu-id="5daac-113">MIME</span><span class="sxs-lookup"><span data-stu-id="5daac-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5daac-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5daac-114">Remarks</span></span>

<span data-ttu-id="5daac-115">Cette propriété est utilisée pour diriger le système de messagerie dans la gestion des messages non remis.</span><span class="sxs-lookup"><span data-stu-id="5daac-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="5daac-116">Dans ce cas, le message doit fournir également la propriété **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="5daac-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5daac-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5daac-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5daac-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="5daac-118">Protocol specifications</span></span>

<span data-ttu-id="5daac-119">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5daac-119">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5daac-120">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="5daac-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5daac-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5daac-121">Header files</span></span>

<span data-ttu-id="5daac-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5daac-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="5daac-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5daac-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="5daac-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="5daac-124">Mapitags.h</span></span>
  
> <span data-ttu-id="5daac-125">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="5daac-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5daac-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5daac-126">See also</span></span>



[<span data-ttu-id="5daac-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5daac-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5daac-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5daac-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5daac-129">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5daac-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5daac-130">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="5daac-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

