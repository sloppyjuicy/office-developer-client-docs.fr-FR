---
title: Propriété canonique PidTagRtfSyncPrefixCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncPrefixCount
api_type:
- COM
ms.assetid: c2b15ac5-9e89-4ee2-812d-102d0b2ac56e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 61683534504b7451f126591af149d11306cff1bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357861"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a><span data-ttu-id="b8443-103">Propriété canonique PidTagRtfSyncPrefixCount</span><span class="sxs-lookup"><span data-stu-id="b8443-103">PidTagRtfSyncPrefixCount Canonical Property</span></span>

  
  
<span data-ttu-id="b8443-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8443-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8443-105">Contient le nombre de caractères ignorés qui apparaissent avant les caractères significatifs du message.</span><span class="sxs-lookup"><span data-stu-id="b8443-105">Contains a count of the ignorable characters that appear before the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b8443-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b8443-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b8443-107">PR_RTF_SYNC_PREFIX_COUNT</span><span class="sxs-lookup"><span data-stu-id="b8443-107">PR_RTF_SYNC_PREFIX_COUNT</span></span>  <br/> |
|<span data-ttu-id="b8443-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b8443-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b8443-109">0x1010</span><span class="sxs-lookup"><span data-stu-id="b8443-109">0x1010</span></span>  <br/> |
|<span data-ttu-id="b8443-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b8443-110">Data type:</span></span>  <br/> |<span data-ttu-id="b8443-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b8443-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b8443-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b8443-112">Area:</span></span>  <br/> |<span data-ttu-id="b8443-113">Message MAPI</span><span class="sxs-lookup"><span data-stu-id="b8443-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8443-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b8443-114">Remarks</span></span>

<span data-ttu-id="b8443-115">Le nombre de caractères de préfixe n’inclut pas d’espace blanc.</span><span class="sxs-lookup"><span data-stu-id="b8443-115">The count of prefix characters does not include white space.</span></span>
  
<span data-ttu-id="b8443-116">Cette propriété est une propriété auxiliaire rtf (Rich Text Format).</span><span class="sxs-lookup"><span data-stu-id="b8443-116">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="b8443-117">Les propriétés auxiliaires RTF sont utilisées par la [fonction RTFSync](rtfsync.md) et ne sont pas destinées à être utilisées directement par les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="b8443-117">RTF auxiliary properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b8443-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b8443-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b8443-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="b8443-119">Protocol specifications</span></span>

<span data-ttu-id="b8443-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8443-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8443-121">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="b8443-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b8443-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8443-122">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8443-123">Code et décode les objets de message et de pièce jointe dans une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="b8443-123">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b8443-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b8443-124">Header files</span></span>

<span data-ttu-id="b8443-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b8443-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b8443-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b8443-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="b8443-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b8443-127">Mapitags.h</span></span>
  
> <span data-ttu-id="b8443-128">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="b8443-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b8443-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8443-129">See also</span></span>



[<span data-ttu-id="b8443-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b8443-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b8443-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b8443-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b8443-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b8443-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b8443-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b8443-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

