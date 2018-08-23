---
title: Propriété canonique PidTagRtfSyncBodyCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCount
api_type:
- COM
ms.assetid: b7267be4-8d5c-4dc7-86b2-651e03e84f9b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b88c036b3bc9b29962204ea0b90bd460ee1cf90f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585170"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a><span data-ttu-id="9317d-103">Propriété canonique PidTagRtfSyncBodyCount</span><span class="sxs-lookup"><span data-stu-id="9317d-103">PidTagRtfSyncBodyCount Canonical Property</span></span>

  
  
<span data-ttu-id="9317d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9317d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9317d-105">Affiche le nombre de caractères significatives du texte du message.</span><span class="sxs-lookup"><span data-stu-id="9317d-105">Contains a count of the significant characters of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9317d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9317d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9317d-107">PR_RTF_SYNC_BODY_COUNT</span><span class="sxs-lookup"><span data-stu-id="9317d-107">PR_RTF_SYNC_BODY_COUNT</span></span>  <br/> |
|<span data-ttu-id="9317d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9317d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9317d-109">0 x 1007</span><span class="sxs-lookup"><span data-stu-id="9317d-109">0x1007</span></span>  <br/> |
|<span data-ttu-id="9317d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9317d-110">Data type:</span></span>  <br/> |<span data-ttu-id="9317d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9317d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9317d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9317d-112">Area:</span></span>  <br/> |<span data-ttu-id="9317d-113">Message MAPI</span><span class="sxs-lookup"><span data-stu-id="9317d-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9317d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9317d-114">Remarks</span></span>

<span data-ttu-id="9317d-115">La fonction [RTFSync](rtfsync.md) calcule le nombre de caractères du texte à l’aide uniquement à ceux qui lui significatifs au message.</span><span class="sxs-lookup"><span data-stu-id="9317d-115">The [RTFSync](rtfsync.md) function computes the count of characters in the text using only those that it considers to be significant to the message.</span></span> <span data-ttu-id="9317d-116">Par exemple, certains espaces blancs et autres caractères pouvant être ignorés sont tous deux omis du nombre.</span><span class="sxs-lookup"><span data-stu-id="9317d-116">For example, some white space and other ignorable characters are omitted from the count.</span></span> 
  
<span data-ttu-id="9317d-117">Cette propriété est une propriété auxiliaire RTF (RICH Text Format).</span><span class="sxs-lookup"><span data-stu-id="9317d-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="9317d-118">Ces propriétés sont utilisées par la fonction **RTFSync** et ne sont pas destinées à être directement utilisé par les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="9317d-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9317d-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9317d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9317d-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="9317d-120">Protocol specifications</span></span>

<span data-ttu-id="9317d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9317d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9317d-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="9317d-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9317d-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9317d-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9317d-124">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="9317d-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9317d-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9317d-125">Header files</span></span>

<span data-ttu-id="9317d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9317d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9317d-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9317d-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="9317d-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="9317d-128">Mapitags.h</span></span>
  
> <span data-ttu-id="9317d-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="9317d-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9317d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9317d-130">See also</span></span>



[<span data-ttu-id="9317d-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9317d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9317d-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9317d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9317d-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9317d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9317d-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9317d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

