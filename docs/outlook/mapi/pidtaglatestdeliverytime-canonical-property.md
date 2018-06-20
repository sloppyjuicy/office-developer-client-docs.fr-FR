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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0cf25dc5a1182d019ea183f2c0714925f220aeb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786179"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="ea2fc-103">Propriété canonique PidTagLatestDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="ea2fc-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="ea2fc-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ea2fc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ea2fc-105">Contient la date et l’heure quand un message transfert agent de doit remettre un message le plus récent.</span><span class="sxs-lookup"><span data-stu-id="ea2fc-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ea2fc-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ea2fc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ea2fc-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="ea2fc-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="ea2fc-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ea2fc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ea2fc-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="ea2fc-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="ea2fc-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ea2fc-110">Data type:</span></span>  <br/> |<span data-ttu-id="ea2fc-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ea2fc-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ea2fc-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="ea2fc-112">Area:</span></span>  <br/> |<span data-ttu-id="ea2fc-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="ea2fc-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea2fc-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ea2fc-114">Remarks</span></span>

<span data-ttu-id="ea2fc-115">Si un agent MTA ne peut pas remettre un message au moment où que cette propriété spécifie, il annule le message sans remise.</span><span class="sxs-lookup"><span data-stu-id="ea2fc-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ea2fc-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ea2fc-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ea2fc-117">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ea2fc-117">Header files</span></span>

<span data-ttu-id="ea2fc-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ea2fc-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="ea2fc-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ea2fc-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="ea2fc-120">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ea2fc-120">Mapitags.h</span></span>
  
> <span data-ttu-id="ea2fc-121">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="ea2fc-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea2fc-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea2fc-122">See also</span></span>



[<span data-ttu-id="ea2fc-123">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ea2fc-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ea2fc-124">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ea2fc-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ea2fc-125">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ea2fc-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ea2fc-126">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ea2fc-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

