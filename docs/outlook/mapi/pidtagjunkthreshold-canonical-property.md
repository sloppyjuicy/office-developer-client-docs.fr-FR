---
title: Propriété canonique PidTagJunkThreshold
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 078dfcc7c24870cf95a2a4b2385c34fbeb64fac0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326851"
---
# <a name="pidtagjunkthreshold-canonical-property"></a><span data-ttu-id="68fa6-103">Propriété canonique PidTagJunkThreshold</span><span class="sxs-lookup"><span data-stu-id="68fa6-103">PidTagJunkThreshold Canonical Property</span></span>

  
  
<span data-ttu-id="68fa6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68fa6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68fa6-105">Indique la façon dont le courrier entrant dynamique doit être envoyé vers le dossier courrier inDésirable.</span><span class="sxs-lookup"><span data-stu-id="68fa6-105">Indicates how aggressively incoming mail should be sent to the Junk Email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68fa6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="68fa6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="68fa6-107">PR_JUNK_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="68fa6-107">PR_JUNK_THRESHOLD</span></span>  <br/> |
|<span data-ttu-id="68fa6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="68fa6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="68fa6-109">0x6101</span><span class="sxs-lookup"><span data-stu-id="68fa6-109">0x6101</span></span>  <br/> |
|<span data-ttu-id="68fa6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="68fa6-110">Data type:</span></span>  <br/> |<span data-ttu-id="68fa6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="68fa6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="68fa6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="68fa6-112">Area:</span></span>  <br/> |<span data-ttu-id="68fa6-113">Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="68fa6-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68fa6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="68fa6-114">Remarks</span></span>

<span data-ttu-id="68fa6-115">Cette propriété correspond au paramètre de filtre haut/bas/aucun.</span><span class="sxs-lookup"><span data-stu-id="68fa6-115">This property corresponds to the high / low / none filter setting.</span></span> <span data-ttu-id="68fa6-116">Une valeur de «0xFFFFFFFF» indique que le filtrage du courrier indésirable ne doit pas être appliqué, mais les listes bloquées doivent néanmoins être appliquées.</span><span class="sxs-lookup"><span data-stu-id="68fa6-116">A value of "0xFFFFFFFF" indicates that spam filtering should not be applied, however block lists must still be applied.</span></span> <span data-ttu-id="68fa6-117">La valeur «0x80000000» indique que tous les messages sont du courrier indésirable, à l'exception des messages provenant d'expéditeurs figurant dans la liste des expéditeurs approuvés ou envoyés à des destinataires figurant dans la liste des destinataires approuvés.</span><span class="sxs-lookup"><span data-stu-id="68fa6-117">A value of "0x80000000" indicates that all mail is spam except those messages from senders on the trusted senders list or sent to recipients on the trusted recipients list.</span></span> <span data-ttu-id="68fa6-118">Les valeurs de cette valeur sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="68fa6-118">Values for this are as follows:</span></span>
  
|<span data-ttu-id="68fa6-119">**Value**</span><span class="sxs-lookup"><span data-stu-id="68fa6-119">**Value**</span></span>|<span data-ttu-id="68fa6-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="68fa6-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="68fa6-121">Égale</span><span class="sxs-lookup"><span data-stu-id="68fa6-121">0xFFFFFFFF</span></span>  <br/> |<span data-ttu-id="68fa6-122">Aucun filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="68fa6-122">No spam filtering</span></span>  <br/> |
|<span data-ttu-id="68fa6-123">0x00000006</span><span class="sxs-lookup"><span data-stu-id="68fa6-123">0x00000006</span></span>  <br/> |<span data-ttu-id="68fa6-124">Faible filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="68fa6-124">Low spam filtering</span></span>  <br/> |
|<span data-ttu-id="68fa6-125">0x00000003</span><span class="sxs-lookup"><span data-stu-id="68fa6-125">0x00000003</span></span>  <br/> |<span data-ttu-id="68fa6-126">Filtrage du courrier indésirable élevé</span><span class="sxs-lookup"><span data-stu-id="68fa6-126">High spam filtering</span></span>  <br/> |
|<span data-ttu-id="68fa6-127">0x80000000</span><span class="sxs-lookup"><span data-stu-id="68fa6-127">0x80000000</span></span>  <br/> |<span data-ttu-id="68fa6-128">Listes approuvées uniquement</span><span class="sxs-lookup"><span data-stu-id="68fa6-128">Trusted Lists Only</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="68fa6-129">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="68fa6-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="68fa6-130">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="68fa6-130">Protocol specifications</span></span>

<span data-ttu-id="68fa6-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68fa6-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68fa6-132">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="68fa6-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="68fa6-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68fa6-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68fa6-134">Active la gestion des listes d'autorisation/de blocage et la détermination des messages électroniques indésirables.</span><span class="sxs-lookup"><span data-stu-id="68fa6-134">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="68fa6-135">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="68fa6-135">Header files</span></span>

<span data-ttu-id="68fa6-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="68fa6-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="68fa6-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="68fa6-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="68fa6-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="68fa6-138">Mapitags.h</span></span>
  
> <span data-ttu-id="68fa6-139">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="68fa6-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68fa6-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68fa6-140">See also</span></span>



[<span data-ttu-id="68fa6-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="68fa6-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="68fa6-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="68fa6-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="68fa6-143">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="68fa6-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="68fa6-144">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="68fa6-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

