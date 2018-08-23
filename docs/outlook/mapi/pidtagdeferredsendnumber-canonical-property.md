---
title: Propriété canonique PidTagDeferredSendNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendNumber
api_type:
- HeaderDef
ms.assetid: 8ada5c9b-bec5-42d8-bc58-f0411ec4e88b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 30ee7c1a7eb86fd4cdfe90fb6711bd1b295fd5e6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591085"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a><span data-ttu-id="de113-103">Propriété canonique PidTagDeferredSendNumber</span><span class="sxs-lookup"><span data-stu-id="de113-103">PidTagDeferredSendNumber Canonical Property</span></span>

  
  
<span data-ttu-id="de113-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de113-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de113-105">Contient un nombre qui peut être utilisé pour calculer l’ajournement d’envoyer un message.</span><span class="sxs-lookup"><span data-stu-id="de113-105">Contains a number that can be used to compute the deferment of sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de113-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="de113-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de113-107">PR_DEFERRED_SEND_NUMBER</span><span class="sxs-lookup"><span data-stu-id="de113-107">PR_DEFERRED_SEND_NUMBER</span></span>  <br/> |
|<span data-ttu-id="de113-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="de113-108">Identifier:</span></span>  <br/> |<span data-ttu-id="de113-109">0x3FEB</span><span class="sxs-lookup"><span data-stu-id="de113-109">0x3FEB</span></span>  <br/> |
|<span data-ttu-id="de113-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="de113-110">Data type:</span></span>  <br/> |<span data-ttu-id="de113-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="de113-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="de113-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="de113-112">Area:</span></span>  <br/> |<span data-ttu-id="de113-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="de113-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de113-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="de113-114">Remarks</span></span>

<span data-ttu-id="de113-115">Cette propriété est utilisée pour le calcul de la propriété **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) lorsqu’il n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="de113-115">This property is used for computing the **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) property when it is not present.</span></span> <span data-ttu-id="de113-116">Lors de l’envoi d’un message est différé, la propriété **PR_DEFERRED_SEND_NUMBER** doit être définie avec la propriété **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)), si la propriété **PR_DEFERRED_SEND_TIME** est absente.</span><span class="sxs-lookup"><span data-stu-id="de113-116">When sending a message is deferred, the **PR_DEFERRED_SEND_NUMBER** property should be set along with the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) property, if the **PR_DEFERRED_SEND_TIME** property is absent.</span></span> 
  
<span data-ttu-id="de113-117">La valeur **PR_DEFERRED_SEND_NUMBER** doit être définie entre 0 et 999.</span><span class="sxs-lookup"><span data-stu-id="de113-117">The **PR_DEFERRED_SEND_NUMBER** value must be set between 0 and 999.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="de113-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="de113-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="de113-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="de113-119">Protocol specifications</span></span>

<span data-ttu-id="de113-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de113-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de113-121">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="de113-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="de113-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="de113-122">Header files</span></span>

<span data-ttu-id="de113-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de113-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="de113-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="de113-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="de113-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="de113-125">Mapitags.h</span></span>
  
> <span data-ttu-id="de113-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="de113-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de113-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de113-127">See also</span></span>



[<span data-ttu-id="de113-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="de113-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de113-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="de113-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de113-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="de113-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de113-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="de113-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

