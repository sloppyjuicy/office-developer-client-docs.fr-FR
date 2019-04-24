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
ms.openlocfilehash: 227ceb468c54cea98519057b2f837a4aee84820c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341957"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="f3d7a-103">Propriété canonique PidTagOriginatorNonDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="f3d7a-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="f3d7a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3d7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3d7a-105">Contient la valeur TRUE si un expéditeur de message demande un rapport de livraison pour un destinataire particulier.</span><span class="sxs-lookup"><span data-stu-id="f3d7a-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f3d7a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f3d7a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3d7a-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="f3d7a-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="f3d7a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f3d7a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f3d7a-109">0x0C08</span><span class="sxs-lookup"><span data-stu-id="f3d7a-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="f3d7a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f3d7a-110">Data type:</span></span>  <br/> |<span data-ttu-id="f3d7a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f3d7a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f3d7a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f3d7a-112">Area:</span></span>  <br/> |<span data-ttu-id="f3d7a-113">MIME</span><span class="sxs-lookup"><span data-stu-id="f3d7a-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3d7a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f3d7a-114">Remarks</span></span>

<span data-ttu-id="f3d7a-115">Cette propriété est utilisée pour diriger le système de messagerie dans la gestion des messages non remis.</span><span class="sxs-lookup"><span data-stu-id="f3d7a-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="f3d7a-116">Dans ce cas, le message doit également fournir la propriété **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) définie sur false.</span><span class="sxs-lookup"><span data-stu-id="f3d7a-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f3d7a-117">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="f3d7a-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f3d7a-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="f3d7a-118">Protocol specifications</span></span>

<span data-ttu-id="f3d7a-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3d7a-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3d7a-120">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="f3d7a-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f3d7a-121">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="f3d7a-121">Header files</span></span>

<span data-ttu-id="f3d7a-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f3d7a-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3d7a-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f3d7a-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="f3d7a-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f3d7a-124">Mapitags.h</span></span>
  
> <span data-ttu-id="f3d7a-125">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="f3d7a-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3d7a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3d7a-126">See also</span></span>



[<span data-ttu-id="f3d7a-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f3d7a-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3d7a-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f3d7a-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3d7a-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f3d7a-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3d7a-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f3d7a-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

