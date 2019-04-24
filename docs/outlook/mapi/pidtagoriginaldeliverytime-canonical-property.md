---
title: Propriété canonique PidTagOriginalDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDeliveryTime
api_type:
- COM
ms.assetid: 700ccfc9-493a-483b-aca0-aa2d7f6bb229
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bbe277092b450a4254e02d00d2cf54e35ec6be44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355656"
---
# <a name="pidtagoriginaldeliverytime-canonical-property"></a><span data-ttu-id="11c93-103">Propriété canonique PidTagOriginalDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="11c93-103">PidTagOriginalDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="11c93-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11c93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11c93-105">Contient une copie de la date et de l'heure de remise du message d'origine dans un thread.</span><span class="sxs-lookup"><span data-stu-id="11c93-105">Contains a copy of the original message's delivery date and time in a thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11c93-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="11c93-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11c93-107">PR_ORIGINAL_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="11c93-107">PR_ORIGINAL_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="11c93-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="11c93-108">Identifier:</span></span>  <br/> |<span data-ttu-id="11c93-109">0x0055</span><span class="sxs-lookup"><span data-stu-id="11c93-109">0x0055</span></span>  <br/> |
|<span data-ttu-id="11c93-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="11c93-110">Data type:</span></span>  <br/> |<span data-ttu-id="11c93-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="11c93-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="11c93-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="11c93-112">Area:</span></span>  <br/> |<span data-ttu-id="11c93-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="11c93-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11c93-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="11c93-114">Remarks</span></span>

<span data-ttu-id="11c93-115">Cette propriété est copiée à partir de la propriété **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) d'origine dans les opérations de réponse ou de transfert ultérieures et utilisée dans les rapports lus et non lus.</span><span class="sxs-lookup"><span data-stu-id="11c93-115">This property is copied from the original **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property in subsequent reply or forward operations and used in read and nonread reports.</span></span> <span data-ttu-id="11c93-116">Les rapports de remise utilisent la propriété **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) à la place.</span><span class="sxs-lookup"><span data-stu-id="11c93-116">Delivery reports use the **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) property instead.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="11c93-117">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="11c93-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="11c93-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="11c93-118">Protocol specifications</span></span>

<span data-ttu-id="11c93-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11c93-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11c93-120">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="11c93-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="11c93-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11c93-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11c93-122">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="11c93-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="11c93-123">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="11c93-123">Header files</span></span>

<span data-ttu-id="11c93-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="11c93-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="11c93-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="11c93-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="11c93-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="11c93-126">Mapitags.h</span></span>
  
> <span data-ttu-id="11c93-127">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="11c93-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11c93-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11c93-128">See also</span></span>



[<span data-ttu-id="11c93-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="11c93-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11c93-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="11c93-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11c93-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="11c93-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11c93-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="11c93-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

