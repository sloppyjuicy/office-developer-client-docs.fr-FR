---
title: Propriété canonique PidTagLatestDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLatestDeliveryTime
api_type:
- HeaderDef
ms.assetid: 6c2e64bc-786e-4867-a504-46f4d1214337
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3640ec4471b72dea81d56cc2c462ef145095480f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590924"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="11b8d-103">Propriété canonique PidTagLatestDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="11b8d-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="11b8d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11b8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11b8d-105">Contient la date et l’heure quand un message transfert agent de doit remettre un message le plus récent.</span><span class="sxs-lookup"><span data-stu-id="11b8d-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11b8d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="11b8d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11b8d-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="11b8d-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="11b8d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="11b8d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="11b8d-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="11b8d-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="11b8d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="11b8d-110">Data type:</span></span>  <br/> |<span data-ttu-id="11b8d-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="11b8d-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="11b8d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="11b8d-112">Area:</span></span>  <br/> |<span data-ttu-id="11b8d-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="11b8d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11b8d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="11b8d-114">Remarks</span></span>

<span data-ttu-id="11b8d-115">Si un agent MTA ne peut pas remettre un message au moment où que cette propriété spécifie, il annule le message sans remise.</span><span class="sxs-lookup"><span data-stu-id="11b8d-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="11b8d-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="11b8d-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="11b8d-117">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="11b8d-117">Header files</span></span>

<span data-ttu-id="11b8d-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11b8d-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="11b8d-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="11b8d-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="11b8d-120">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="11b8d-120">Mapitags.h</span></span>
  
> <span data-ttu-id="11b8d-121">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="11b8d-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11b8d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11b8d-122">See also</span></span>



[<span data-ttu-id="11b8d-123">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="11b8d-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11b8d-124">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="11b8d-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11b8d-125">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="11b8d-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11b8d-126">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="11b8d-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

