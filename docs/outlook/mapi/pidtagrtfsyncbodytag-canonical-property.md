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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 24ef1d4e3e936426aea8216119e8ada9f6122e95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331177"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a><span data-ttu-id="c04f7-103">Propriété canonique PidTagRtfSyncBodyTag</span><span class="sxs-lookup"><span data-stu-id="c04f7-103">PidTagRtfSyncBodyTag Canonical Property</span></span>

  
  
<span data-ttu-id="c04f7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c04f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c04f7-105">Contient des caractères significatifs qui apparaissent au début du texte du message.</span><span class="sxs-lookup"><span data-stu-id="c04f7-105">Contains significant characters that appear at the beginning of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c04f7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c04f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c04f7-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span><span class="sxs-lookup"><span data-stu-id="c04f7-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span></span>  <br/> |
|<span data-ttu-id="c04f7-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c04f7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c04f7-109">0x1008</span><span class="sxs-lookup"><span data-stu-id="c04f7-109">0x1008</span></span>  <br/> |
|<span data-ttu-id="c04f7-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c04f7-110">Data type:</span></span>  <br/> |<span data-ttu-id="c04f7-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c04f7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c04f7-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c04f7-112">Area:</span></span>  <br/> |<span data-ttu-id="c04f7-113">Message MAPI</span><span class="sxs-lookup"><span data-stu-id="c04f7-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c04f7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c04f7-114">Remarks</span></span>

<span data-ttu-id="c04f7-115">La [fonction RTFSync](rtfsync.md) utilise la balise de texte pour indiquer le début du texte du message.</span><span class="sxs-lookup"><span data-stu-id="c04f7-115">The [RTFSync](rtfsync.md) function uses the text tag to indicate the beginning of the message text.</span></span> <span data-ttu-id="c04f7-116">Lorsque le texte est modifié, la balise est utilisée pour trouver le début du texte précédent.</span><span class="sxs-lookup"><span data-stu-id="c04f7-116">When the text is modified, the tag is used to find the beginning of the previous text.</span></span> 
  
<span data-ttu-id="c04f7-117">Ces propriétés sont des propriétés auxiliaires du format texte enrichi.</span><span class="sxs-lookup"><span data-stu-id="c04f7-117">These properties are Rich Text Format auxiliary properties.</span></span> <span data-ttu-id="c04f7-118">Elles sont utilisées par la **fonction RTFSync** et ne sont pas destinées à être utilisées directement par les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="c04f7-118">They are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c04f7-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c04f7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c04f7-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="c04f7-120">Protocol specifications</span></span>

<span data-ttu-id="c04f7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c04f7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c04f7-122">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="c04f7-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c04f7-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c04f7-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c04f7-124">Encode et décode les objets de message et de pièce jointe dans une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="c04f7-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c04f7-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c04f7-125">Header files</span></span>

<span data-ttu-id="c04f7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c04f7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c04f7-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c04f7-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="c04f7-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c04f7-128">Mapitags.h</span></span>
  
> <span data-ttu-id="c04f7-129">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="c04f7-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c04f7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c04f7-130">See also</span></span>



[<span data-ttu-id="c04f7-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c04f7-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c04f7-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c04f7-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c04f7-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c04f7-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c04f7-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c04f7-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

