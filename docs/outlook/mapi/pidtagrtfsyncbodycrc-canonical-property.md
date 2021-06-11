---
title: Propriété canonique PidTagRtfSyncBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCrc
api_type:
- COM
ms.assetid: 95db4837-400f-476f-b313-60e8baa1c6d1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 85ac61d968243283e5ad9283730941adcd87cd5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357868"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a><span data-ttu-id="efa16-103">Propriété canonique PidTagRtfSyncBodyCrc</span><span class="sxs-lookup"><span data-stu-id="efa16-103">PidTagRtfSyncBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="efa16-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efa16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efa16-105">Contient la vérification de redondance cyclique (CRC) calculée pour le texte du message.</span><span class="sxs-lookup"><span data-stu-id="efa16-105">Contains the cyclical redundancy check (CRC) computed for the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="efa16-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="efa16-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="efa16-107">PR_RTF_SYNC_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="efa16-107">PR_RTF_SYNC_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="efa16-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="efa16-108">Identifier:</span></span>  <br/> |<span data-ttu-id="efa16-109">0x1006</span><span class="sxs-lookup"><span data-stu-id="efa16-109">0x1006</span></span>  <br/> |
|<span data-ttu-id="efa16-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="efa16-110">Data type:</span></span>  <br/> |<span data-ttu-id="efa16-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="efa16-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="efa16-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="efa16-112">Area:</span></span>  <br/> |<span data-ttu-id="efa16-113">Message MAPI</span><span class="sxs-lookup"><span data-stu-id="efa16-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efa16-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="efa16-114">Remarks</span></span>

<span data-ttu-id="efa16-115">La [fonction RTFSync](rtfsync.md) calcule la CRC en utilisant uniquement les caractères qu’elle considère comme significatifs pour le message.</span><span class="sxs-lookup"><span data-stu-id="efa16-115">The [RTFSync](rtfsync.md) function computes the CRC by using only the characters that it considers to be significant to the message.</span></span> <span data-ttu-id="efa16-116">Par exemple, certains espaces et autres caractères ignoreables sont omis de la CRC.</span><span class="sxs-lookup"><span data-stu-id="efa16-116">For example, some white space and other ignorable characters are omitted from the CRC.</span></span> 
  
<span data-ttu-id="efa16-117">Cette propriété est une propriété auxiliaire rtf (Rich Text Format).</span><span class="sxs-lookup"><span data-stu-id="efa16-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="efa16-118">Ces propriétés sont utilisées par **la fonction RTFSync** et ne sont pas destinées à être utilisées directement par les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="efa16-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="efa16-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="efa16-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="efa16-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="efa16-120">Protocol specifications</span></span>

<span data-ttu-id="efa16-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="efa16-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="efa16-122">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="efa16-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="efa16-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="efa16-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="efa16-124">Encode et décode les objets de message et de pièce jointe dans une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="efa16-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="efa16-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="efa16-125">Header files</span></span>

<span data-ttu-id="efa16-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="efa16-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="efa16-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="efa16-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="efa16-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="efa16-128">Mapitags.h</span></span>
  
> <span data-ttu-id="efa16-129">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="efa16-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="efa16-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efa16-130">See also</span></span>



[<span data-ttu-id="efa16-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="efa16-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="efa16-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="efa16-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="efa16-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="efa16-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="efa16-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="efa16-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

