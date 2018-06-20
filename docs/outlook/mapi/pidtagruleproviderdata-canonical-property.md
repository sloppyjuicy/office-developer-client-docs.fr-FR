---
title: Propriété canonique PidTagRuleProviderData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProviderData
api_type:
- COM
ms.assetid: b04a277c-b483-4f54-b360-311034b9a7ee
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 054299e6bdf685163bc23678a2070f5d702a4529
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786669"
---
# <a name="pidtagruleproviderdata-canonical-property"></a><span data-ttu-id="82ea4-103">Propriété canonique PidTagRuleProviderData</span><span class="sxs-lookup"><span data-stu-id="82ea4-103">PidTagRuleProviderData Canonical Property</span></span>

  
  
<span data-ttu-id="82ea4-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="82ea4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="82ea4-105">Une propriété opaque qui définit par le client à l’usage exclusif du client.</span><span class="sxs-lookup"><span data-stu-id="82ea4-105">An opaque property that the client sets for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="82ea4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="82ea4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82ea4-107">PR_RULE_PROVIDER_DATA</span><span class="sxs-lookup"><span data-stu-id="82ea4-107">PR_RULE_PROVIDER_DATA</span></span>  <br/> |
|<span data-ttu-id="82ea4-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="82ea4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="82ea4-109">0x6684</span><span class="sxs-lookup"><span data-stu-id="82ea4-109">0x6684</span></span>  <br/> |
|<span data-ttu-id="82ea4-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="82ea4-110">Data type:</span></span>  <br/> |<span data-ttu-id="82ea4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="82ea4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="82ea4-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="82ea4-112">Area:</span></span>  <br/> |<span data-ttu-id="82ea4-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="82ea4-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82ea4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="82ea4-114">Remarks</span></span>

<span data-ttu-id="82ea4-115">Le serveur doit conserver la valeur de cette propriété si elle a été définie par le client, mais doit ignorer son contenu au cours de traitement et d’évaluation de la règle.</span><span class="sxs-lookup"><span data-stu-id="82ea4-115">The server must preserve the value of this property if it was set by the client but must ignore its contents during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="82ea4-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="82ea4-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="82ea4-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="82ea4-117">Protocol specifications</span></span>

<span data-ttu-id="82ea4-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82ea4-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82ea4-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="82ea4-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="82ea4-120">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82ea4-120">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82ea4-121">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="82ea4-121">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="82ea4-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="82ea4-122">Header files</span></span>

<span data-ttu-id="82ea4-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82ea4-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="82ea4-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="82ea4-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="82ea4-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="82ea4-125">Mapitags.h</span></span>
  
> <span data-ttu-id="82ea4-126">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="82ea4-126">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="82ea4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82ea4-127">See also</span></span>



[<span data-ttu-id="82ea4-128">Propriété canonique PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="82ea4-128">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="82ea4-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="82ea4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82ea4-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="82ea4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82ea4-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="82ea4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82ea4-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="82ea4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

