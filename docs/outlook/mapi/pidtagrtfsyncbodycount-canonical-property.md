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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6f6e687412dfce1e5fcee6b4a4d64f3e5106455f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398800"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a><span data-ttu-id="279f7-103">Propriété canonique PidTagRtfSyncBodyCount</span><span class="sxs-lookup"><span data-stu-id="279f7-103">PidTagRtfSyncBodyCount Canonical Property</span></span>

  
  
<span data-ttu-id="279f7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="279f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="279f7-105">Affiche le nombre de caractères significatives du texte du message.</span><span class="sxs-lookup"><span data-stu-id="279f7-105">Contains a count of the significant characters of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="279f7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="279f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="279f7-107">PR_RTF_SYNC_BODY_COUNT</span><span class="sxs-lookup"><span data-stu-id="279f7-107">PR_RTF_SYNC_BODY_COUNT</span></span>  <br/> |
|<span data-ttu-id="279f7-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="279f7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="279f7-109">0 x 1007</span><span class="sxs-lookup"><span data-stu-id="279f7-109">0x1007</span></span>  <br/> |
|<span data-ttu-id="279f7-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="279f7-110">Data type:</span></span>  <br/> |<span data-ttu-id="279f7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="279f7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="279f7-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="279f7-112">Area:</span></span>  <br/> |<span data-ttu-id="279f7-113">Message MAPI</span><span class="sxs-lookup"><span data-stu-id="279f7-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="279f7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="279f7-114">Remarks</span></span>

<span data-ttu-id="279f7-115">La fonction [RTFSync](rtfsync.md) calcule le nombre de caractères du texte à l’aide uniquement à ceux qui lui significatifs au message.</span><span class="sxs-lookup"><span data-stu-id="279f7-115">The [RTFSync](rtfsync.md) function computes the count of characters in the text using only those that it considers to be significant to the message.</span></span> <span data-ttu-id="279f7-116">Par exemple, certains espaces blancs et autres caractères pouvant être ignorés sont tous deux omis du nombre.</span><span class="sxs-lookup"><span data-stu-id="279f7-116">For example, some white space and other ignorable characters are omitted from the count.</span></span> 
  
<span data-ttu-id="279f7-117">Cette propriété est une propriété auxiliaire RTF (RICH Text Format).</span><span class="sxs-lookup"><span data-stu-id="279f7-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="279f7-118">Ces propriétés sont utilisées par la fonction **RTFSync** et ne sont pas destinées à être directement utilisé par les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="279f7-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="279f7-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="279f7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="279f7-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="279f7-120">Protocol specifications</span></span>

<span data-ttu-id="279f7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="279f7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="279f7-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="279f7-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="279f7-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="279f7-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="279f7-124">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="279f7-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="279f7-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="279f7-125">Header files</span></span>

<span data-ttu-id="279f7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="279f7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="279f7-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="279f7-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="279f7-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="279f7-128">Mapitags.h</span></span>
  
> <span data-ttu-id="279f7-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="279f7-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="279f7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="279f7-130">See also</span></span>



[<span data-ttu-id="279f7-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="279f7-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="279f7-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="279f7-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="279f7-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="279f7-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="279f7-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="279f7-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

