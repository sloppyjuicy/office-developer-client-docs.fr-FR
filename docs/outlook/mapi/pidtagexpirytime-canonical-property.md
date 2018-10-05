---
title: Propriété canonique PidTagExpiryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryTime
api_type:
- HeaderDef
ms.assetid: 6e4d4ee9-c6b1-4987-b02e-684c2af3d21c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8d6fa58e61dde30292487c95fb8a74d568a3bbeb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388468"
---
# <a name="pidtagexpirytime-canonical-property"></a><span data-ttu-id="c89ae-103">Propriété canonique PidTagExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c89ae-103">PidTagExpiryTime Canonical Property</span></span>

  
  
<span data-ttu-id="c89ae-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c89ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c89ae-105">Contient la date et l’heure lorsque le système de messagerie peut invalider le contenu d’un message.</span><span class="sxs-lookup"><span data-stu-id="c89ae-105">Contains the date and time when the messaging system can invalidate the content of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c89ae-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c89ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c89ae-107">PR_EXPIRY_TIME</span><span class="sxs-lookup"><span data-stu-id="c89ae-107">PR_EXPIRY_TIME</span></span>  <br/> |
|<span data-ttu-id="c89ae-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c89ae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c89ae-109">0x0015</span><span class="sxs-lookup"><span data-stu-id="c89ae-109">0x0015</span></span>  <br/> |
|<span data-ttu-id="c89ae-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c89ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="c89ae-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c89ae-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c89ae-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c89ae-112">Area:</span></span>  <br/> |<span data-ttu-id="c89ae-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="c89ae-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c89ae-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c89ae-114">Remarks</span></span>

<span data-ttu-id="c89ae-115">Cette propriété est utilisée pour diriger que le système de messagerie dans la gestion des remises de messages.</span><span class="sxs-lookup"><span data-stu-id="c89ae-115">This property is used to direct the messaging system in handling delivered interpersonal messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c89ae-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c89ae-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c89ae-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="c89ae-117">Protocol specifications</span></span>

<span data-ttu-id="c89ae-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c89ae-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c89ae-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="c89ae-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c89ae-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c89ae-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c89ae-121">Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="c89ae-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c89ae-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c89ae-122">Header files</span></span>

<span data-ttu-id="c89ae-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c89ae-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c89ae-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c89ae-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c89ae-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="c89ae-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c89ae-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="c89ae-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c89ae-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c89ae-127">See also</span></span>



[<span data-ttu-id="c89ae-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c89ae-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c89ae-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c89ae-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c89ae-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c89ae-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c89ae-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c89ae-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

