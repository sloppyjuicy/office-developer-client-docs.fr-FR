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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 227ceb468c54cea98519057b2f837a4aee84820c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387215"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="d8dd8-103">Propriété canonique PidTagOriginatorNonDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="d8dd8-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="d8dd8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8dd8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8dd8-105">Contient la valeur TRUE si un expéditeur du message demande un rapport de non-remise pour un destinataire particulier.</span><span class="sxs-lookup"><span data-stu-id="d8dd8-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8dd8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d8dd8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d8dd8-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="d8dd8-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="d8dd8-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d8dd8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d8dd8-109">0x0C08</span><span class="sxs-lookup"><span data-stu-id="d8dd8-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="d8dd8-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d8dd8-110">Data type:</span></span>  <br/> |<span data-ttu-id="d8dd8-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d8dd8-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d8dd8-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d8dd8-112">Area:</span></span>  <br/> |<span data-ttu-id="d8dd8-113">MIME</span><span class="sxs-lookup"><span data-stu-id="d8dd8-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8dd8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d8dd8-114">Remarks</span></span>

<span data-ttu-id="d8dd8-115">Cette propriété est utilisée pour diriger le système de messagerie dans la gestion des messages non remis.</span><span class="sxs-lookup"><span data-stu-id="d8dd8-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="d8dd8-116">Dans ce cas, le message doit fournir également la propriété **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="d8dd8-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d8dd8-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d8dd8-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d8dd8-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="d8dd8-118">Protocol specifications</span></span>

<span data-ttu-id="d8dd8-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8dd8-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8dd8-120">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="d8dd8-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d8dd8-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d8dd8-121">Header files</span></span>

<span data-ttu-id="d8dd8-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d8dd8-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="d8dd8-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d8dd8-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="d8dd8-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="d8dd8-124">Mapitags.h</span></span>
  
> <span data-ttu-id="d8dd8-125">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="d8dd8-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d8dd8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8dd8-126">See also</span></span>



[<span data-ttu-id="d8dd8-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d8dd8-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d8dd8-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d8dd8-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d8dd8-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d8dd8-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d8dd8-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d8dd8-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

