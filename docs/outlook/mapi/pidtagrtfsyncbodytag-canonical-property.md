---
title: Propriété canonique PidTagRtfSyncBodyTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyTag
api_type:
- COM
ms.assetid: 2dab5018-4214-4162-93bc-e5565f3ac24c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bad754d21652d3f5278a6dad3ec06f4a0b533036
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786647"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a><span data-ttu-id="ee82a-103">Propriété canonique PidTagRtfSyncBodyTag</span><span class="sxs-lookup"><span data-stu-id="ee82a-103">PidTagRtfSyncBodyTag Canonical Property</span></span>

  
  
<span data-ttu-id="ee82a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ee82a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ee82a-105">Contient des caractères significatifs qui s’affichent au début du texte du message.</span><span class="sxs-lookup"><span data-stu-id="ee82a-105">Contains significant characters that appear at the beginning of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee82a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ee82a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee82a-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span><span class="sxs-lookup"><span data-stu-id="ee82a-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span></span>  <br/> |
|<span data-ttu-id="ee82a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ee82a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ee82a-109">0 x 1008</span><span class="sxs-lookup"><span data-stu-id="ee82a-109">0x1008</span></span>  <br/> |
|<span data-ttu-id="ee82a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ee82a-110">Data type:</span></span>  <br/> |<span data-ttu-id="ee82a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ee82a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ee82a-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="ee82a-112">Area:</span></span>  <br/> |<span data-ttu-id="ee82a-113">Message MAPI</span><span class="sxs-lookup"><span data-stu-id="ee82a-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee82a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ee82a-114">Remarks</span></span>

<span data-ttu-id="ee82a-115">La fonction [RTFSync](rtfsync.md) utilise la balise de texte pour indiquer le début du texte du message.</span><span class="sxs-lookup"><span data-stu-id="ee82a-115">The [RTFSync](rtfsync.md) function uses the text tag to indicate the beginning of the message text.</span></span> <span data-ttu-id="ee82a-116">Lorsque le texte est modifié, la balise est utilisée pour trouver le début du texte précédent.</span><span class="sxs-lookup"><span data-stu-id="ee82a-116">When the text is modified, the tag is used to find the beginning of the previous text.</span></span> 
  
<span data-ttu-id="ee82a-117">Ces propriétés sont des propriétés auxiliaires au Format RTF.</span><span class="sxs-lookup"><span data-stu-id="ee82a-117">These properties are Rich Text Format auxiliary properties.</span></span> <span data-ttu-id="ee82a-118">Ils sont utilisés par la fonction **RTFSync** et ne sont pas destinés à être directement utilisé par les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="ee82a-118">They are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ee82a-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ee82a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ee82a-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ee82a-120">Protocol specifications</span></span>

<span data-ttu-id="ee82a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee82a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee82a-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="ee82a-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ee82a-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee82a-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee82a-124">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="ee82a-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ee82a-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ee82a-125">Header files</span></span>

<span data-ttu-id="ee82a-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ee82a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee82a-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ee82a-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="ee82a-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ee82a-128">Mapitags.h</span></span>
  
> <span data-ttu-id="ee82a-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="ee82a-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee82a-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee82a-130">See also</span></span>



[<span data-ttu-id="ee82a-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ee82a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee82a-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ee82a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee82a-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ee82a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee82a-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ee82a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

