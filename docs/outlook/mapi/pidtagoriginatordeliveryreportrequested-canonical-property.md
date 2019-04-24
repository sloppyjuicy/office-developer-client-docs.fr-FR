---
title: Propriété canonique PidTagOriginatorDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a92ee13e571032c050f69677d9daba8dad7aea3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356300"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a><span data-ttu-id="c381e-103">Propriété canonique PidTagOriginatorDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="c381e-103">PidTagOriginatorDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="c381e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c381e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c381e-105">Contient la valeur TRUE si l'expéditeur d'un message demande un rapport de remise pour un destinataire particulier du système de messagerie avant que le message ne soit placé dans la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="c381e-105">Contains TRUE if a message sender requests a delivery report for a particular recipient from the messaging system before the message is placed in the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c381e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c381e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c381e-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="c381e-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="c381e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c381e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c381e-109">0x0023</span><span class="sxs-lookup"><span data-stu-id="c381e-109">0x0023</span></span>  <br/> |
|<span data-ttu-id="c381e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c381e-110">Data type:</span></span>  <br/> |<span data-ttu-id="c381e-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c381e-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c381e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c381e-112">Area:</span></span>  <br/> |<span data-ttu-id="c381e-113">MIME</span><span class="sxs-lookup"><span data-stu-id="c381e-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c381e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c381e-114">Remarks</span></span>

<span data-ttu-id="c381e-115">Cette propriété est utilisée pour diriger le système de messagerie dans la gestion des messages remis.</span><span class="sxs-lookup"><span data-stu-id="c381e-115">This property is used to direct the messaging system in handling delivered messages.</span></span> <span data-ttu-id="c381e-116">Dans ce cas, le message doit également fournir la propriété **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) définie sur false.</span><span class="sxs-lookup"><span data-stu-id="c381e-116">In this case, the message must also furnish the **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
<span data-ttu-id="c381e-117">La définition de la propriété **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** sur un message est un moyen de demander des rapports d'état de remise à tous les destinataires.</span><span class="sxs-lookup"><span data-stu-id="c381e-117">Setting the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** property on a message is a way to request delivery status reports for all recipients.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c381e-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="c381e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c381e-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="c381e-119">Protocol specifications</span></span>

<span data-ttu-id="c381e-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c381e-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c381e-121">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="c381e-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c381e-122">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="c381e-122">Header files</span></span>

<span data-ttu-id="c381e-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c381e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c381e-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c381e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c381e-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c381e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c381e-126">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="c381e-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c381e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c381e-127">See also</span></span>



[<span data-ttu-id="c381e-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c381e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c381e-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c381e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c381e-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c381e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c381e-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c381e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

