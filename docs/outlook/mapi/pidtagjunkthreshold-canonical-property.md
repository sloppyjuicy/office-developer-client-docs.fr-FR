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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 078dfcc7c24870cf95a2a4b2385c34fbeb64fac0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387110"
---
# <a name="pidtagjunkthreshold-canonical-property"></a><span data-ttu-id="a5e2a-103">Propriété canonique PidTagJunkThreshold</span><span class="sxs-lookup"><span data-stu-id="a5e2a-103">PidTagJunkThreshold Canonical Property</span></span>

  
  
<span data-ttu-id="a5e2a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5e2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5e2a-105">Indique le degré le courrier entrant doit être envoyé vers le dossier courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a5e2a-105">Indicates how aggressively incoming mail should be sent to the Junk Email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5e2a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a5e2a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5e2a-107">PR_JUNK_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="a5e2a-107">PR_JUNK_THRESHOLD</span></span>  <br/> |
|<span data-ttu-id="a5e2a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a5e2a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a5e2a-109">0x6101</span><span class="sxs-lookup"><span data-stu-id="a5e2a-109">0x6101</span></span>  <br/> |
|<span data-ttu-id="a5e2a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a5e2a-110">Data type:</span></span>  <br/> |<span data-ttu-id="a5e2a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a5e2a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a5e2a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a5e2a-112">Area:</span></span>  <br/> |<span data-ttu-id="a5e2a-113">Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="a5e2a-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5e2a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a5e2a-114">Remarks</span></span>

<span data-ttu-id="a5e2a-115">Cette propriété correspond à la haute / basse / aucun paramètre de filtre.</span><span class="sxs-lookup"><span data-stu-id="a5e2a-115">This property corresponds to the high / low / none filter setting.</span></span> <span data-ttu-id="a5e2a-116">Une valeur de « 0xFFFFFFFF » indique que le filtrage du courrier indésirable ne doit pas être appliqué, mais listes rouges doivent toujours être appliquées.</span><span class="sxs-lookup"><span data-stu-id="a5e2a-116">A value of "0xFFFFFFFF" indicates that spam filtering should not be applied, however block lists must still be applied.</span></span> <span data-ttu-id="a5e2a-117">La valeur « 0 x 80000000 » indique que tous les messages est le courrier indésirable à l’exception de ces messages des expéditeurs de la liste des expéditeurs approuvés ou envoyé aux destinataires dans la liste des destinataires approuvés.</span><span class="sxs-lookup"><span data-stu-id="a5e2a-117">A value of "0x80000000" indicates that all mail is spam except those messages from senders on the trusted senders list or sent to recipients on the trusted recipients list.</span></span> <span data-ttu-id="a5e2a-118">Valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5e2a-118">Values for this are as follows:</span></span>
  
|<span data-ttu-id="a5e2a-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="a5e2a-119">**Value**</span></span>|<span data-ttu-id="a5e2a-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="a5e2a-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a5e2a-121">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="a5e2a-121">0xFFFFFFFF</span></span>  <br/> |<span data-ttu-id="a5e2a-122">Aucun filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="a5e2a-122">No spam filtering</span></span>  <br/> |
|<span data-ttu-id="a5e2a-123">0 x 00000006</span><span class="sxs-lookup"><span data-stu-id="a5e2a-123">0x00000006</span></span>  <br/> |<span data-ttu-id="a5e2a-124">Filtrage du courrier indésirable faible</span><span class="sxs-lookup"><span data-stu-id="a5e2a-124">Low spam filtering</span></span>  <br/> |
|<span data-ttu-id="a5e2a-125">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="a5e2a-125">0x00000003</span></span>  <br/> |<span data-ttu-id="a5e2a-126">Filtrage du courrier indésirable élevé</span><span class="sxs-lookup"><span data-stu-id="a5e2a-126">High spam filtering</span></span>  <br/> |
|<span data-ttu-id="a5e2a-127">0 x 80000000</span><span class="sxs-lookup"><span data-stu-id="a5e2a-127">0x80000000</span></span>  <br/> |<span data-ttu-id="a5e2a-128">Listes approuvées uniquement</span><span class="sxs-lookup"><span data-stu-id="a5e2a-128">Trusted Lists Only</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a5e2a-129">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a5e2a-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5e2a-130">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="a5e2a-130">Protocol specifications</span></span>

<span data-ttu-id="a5e2a-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5e2a-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5e2a-132">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="a5e2a-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5e2a-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5e2a-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5e2a-134">Permet la gestion des listes autoriser/bloquer et la détermination des messages de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a5e2a-134">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5e2a-135">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a5e2a-135">Header files</span></span>

<span data-ttu-id="a5e2a-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5e2a-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5e2a-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a5e2a-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="a5e2a-138">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="a5e2a-138">Mapitags.h</span></span>
  
> <span data-ttu-id="a5e2a-139">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="a5e2a-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5e2a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5e2a-140">See also</span></span>



[<span data-ttu-id="a5e2a-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a5e2a-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5e2a-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a5e2a-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5e2a-143">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a5e2a-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5e2a-144">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a5e2a-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

