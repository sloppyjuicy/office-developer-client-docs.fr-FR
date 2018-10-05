---
title: Propriété canonique PidTagExtendedRuleMessageCondition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageCondition
api_type:
- HeaderDef
ms.assetid: 891851e1-e4a4-4c20-a26c-7223bcca35f7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7c444485c3a443694e2902343a02da5605bde39f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401656"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a><span data-ttu-id="f66a8-103">Propriété canonique PidTagExtendedRuleMessageCondition</span><span class="sxs-lookup"><span data-stu-id="f66a8-103">PidTagExtendedRuleMessageCondition Canonical Property</span></span>

  
  
<span data-ttu-id="f66a8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f66a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f66a8-105">Contient des informations sur les propriétés nommées qui sont contenus dans des conditions de règle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="f66a8-105">Contains information about any named properties that are contained inside of extended rule conditions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f66a8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f66a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f66a8-107">PR_EXTENDED_RULE_MSG_CONDITION</span><span class="sxs-lookup"><span data-stu-id="f66a8-107">PR_EXTENDED_RULE_MSG_CONDITION</span></span>  <br/> |
|<span data-ttu-id="f66a8-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f66a8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f66a8-109">0x0E9A</span><span class="sxs-lookup"><span data-stu-id="f66a8-109">0x0E9A</span></span>  <br/> |
|<span data-ttu-id="f66a8-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f66a8-110">Data type:</span></span>  <br/> |<span data-ttu-id="f66a8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f66a8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f66a8-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f66a8-112">Area:</span></span>  <br/> |<span data-ttu-id="f66a8-113">Rules</span><span class="sxs-lookup"><span data-stu-id="f66a8-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f66a8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f66a8-114">Remarks</span></span>

<span data-ttu-id="f66a8-115">Cette propriété doit être définie sur un message FAI.</span><span class="sxs-lookup"><span data-stu-id="f66a8-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="f66a8-116">Il remplit la même fonction que **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), mais il contient des informations supplémentaires sur les propriétés nommées utilisé.</span><span class="sxs-lookup"><span data-stu-id="f66a8-116">It serves the same purpose as **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), but contains additional information about the named properties used.</span></span> <span data-ttu-id="f66a8-117">Toutes les valeurs de chaîne contenues dans n’importe quelle partie de cette valeur de la propriété condition doivent être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="f66a8-117">All string values contained in any part of this condition property value must be in Unicode format.</span></span>
  
<span data-ttu-id="f66a8-118">Pour plus d’informations sur le format de cette propriété binaire, voir [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f66a8-118">For information about the format of this binary property, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f66a8-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f66a8-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f66a8-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f66a8-120">Protocol specifications</span></span>

<span data-ttu-id="f66a8-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f66a8-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f66a8-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="f66a8-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f66a8-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f66a8-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f66a8-124">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="f66a8-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f66a8-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f66a8-125">Header files</span></span>

<span data-ttu-id="f66a8-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f66a8-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f66a8-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f66a8-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="f66a8-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f66a8-128">Mapitags.h</span></span>
  
> <span data-ttu-id="f66a8-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="f66a8-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f66a8-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f66a8-130">See also</span></span>



[<span data-ttu-id="f66a8-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f66a8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f66a8-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f66a8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f66a8-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f66a8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f66a8-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f66a8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

