---
title: Propriété canonique PidTagRtfSyncTrailingCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncTrailingCount
api_type:
- COM
ms.assetid: 3f0e5b24-767e-46f5-bb3d-e9cb82cb935b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 67093cf456db9df5f9e939bdda9d2e44f248dadc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397918"
---
# <a name="pidtagrtfsynctrailingcount-canonical-property"></a><span data-ttu-id="1e7b9-103">Propriété canonique PidTagRtfSyncTrailingCount</span><span class="sxs-lookup"><span data-stu-id="1e7b9-103">PidTagRtfSyncTrailingCount Canonical Property</span></span>

  
  
<span data-ttu-id="1e7b9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e7b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e7b9-105">Affiche le nombre de caractères qui s’affiche après les caractères significatives du message peut être ignorés.</span><span class="sxs-lookup"><span data-stu-id="1e7b9-105">Contains a count of the ignorable characters that appear after the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e7b9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1e7b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e7b9-107">PR_RTF_SYNC_TRAILING_COUNT</span><span class="sxs-lookup"><span data-stu-id="1e7b9-107">PR_RTF_SYNC_TRAILING_COUNT</span></span>  <br/> |
|<span data-ttu-id="1e7b9-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1e7b9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e7b9-109">0x1011</span><span class="sxs-lookup"><span data-stu-id="1e7b9-109">0x1011</span></span>  <br/> |
|<span data-ttu-id="1e7b9-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1e7b9-110">Data type:</span></span>  <br/> |<span data-ttu-id="1e7b9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1e7b9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1e7b9-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1e7b9-112">Area:</span></span>  <br/> |<span data-ttu-id="1e7b9-113">Message MAPI</span><span class="sxs-lookup"><span data-stu-id="1e7b9-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e7b9-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1e7b9-114">Remarks</span></span>

<span data-ttu-id="1e7b9-115">Cette propriété est une propriété auxiliaire enrichi texte Format correspondante.</span><span class="sxs-lookup"><span data-stu-id="1e7b9-115">This property is a Rich Text Format (RFT) auxiliary property.</span></span> <span data-ttu-id="1e7b9-116">Ces propriétés sont utilisées par la fonction [RTFSync](rtfsync.md) et ne sont pas destinées à être directement utilisé par les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="1e7b9-116">These properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1e7b9-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1e7b9-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1e7b9-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="1e7b9-118">Protocol specifications</span></span>

<span data-ttu-id="1e7b9-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e7b9-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e7b9-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="1e7b9-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1e7b9-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e7b9-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e7b9-122">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="1e7b9-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1e7b9-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1e7b9-123">Header files</span></span>

<span data-ttu-id="1e7b9-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e7b9-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e7b9-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1e7b9-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e7b9-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="1e7b9-126">Mapitags.h</span></span>
  
> <span data-ttu-id="1e7b9-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="1e7b9-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e7b9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e7b9-128">See also</span></span>



[<span data-ttu-id="1e7b9-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1e7b9-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e7b9-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1e7b9-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e7b9-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1e7b9-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e7b9-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1e7b9-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

