---
title: Propriété canonique PidTagRuleCondition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleCondition
api_type:
- COM
ms.assetid: 8a11e846-c62f-4c06-876f-94623d50cc3b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5b513bc5ff6b95b26a96e36a4d04a49737cf6216
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359506"
---
# <a name="pidtagrulecondition-canonical-property"></a><span data-ttu-id="4c763-103">Propriété canonique PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="4c763-103">PidTagRuleCondition Canonical Property</span></span>

  
  
<span data-ttu-id="4c763-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c763-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c763-105">Condition utilisée lorsque vous évaluez la règle.</span><span class="sxs-lookup"><span data-stu-id="4c763-105">The condition used when you evaluate the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4c763-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4c763-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c763-107">PR_RULE_CONDITION</span><span class="sxs-lookup"><span data-stu-id="4c763-107">PR_RULE_CONDITION</span></span>  <br/> |
|<span data-ttu-id="4c763-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4c763-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4c763-109">0x6679</span><span class="sxs-lookup"><span data-stu-id="4c763-109">0x6679</span></span>  <br/> |
|<span data-ttu-id="4c763-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4c763-110">Data type:</span></span>  <br/> |<span data-ttu-id="4c763-111">PT_SRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="4c763-111">PT_SRESTRICTION</span></span>  <br/> |
|<span data-ttu-id="4c763-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4c763-112">Area:</span></span>  <br/> |<span data-ttu-id="4c763-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="4c763-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c763-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4c763-114">Remarks</span></span>

<span data-ttu-id="4c763-115">La condition est exprimée sous la forme d’une **restriction** et la mémoire tampon **PropertyValue** contient la structure **restriction** empaqueté comme spécifié dans [[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4c763-115">The condition is expressed as a **Restriction** and the **PropertyValue** buffer contains the **Restriction** structure packaged as specified in [[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4c763-116">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4c763-116">MFCMAPI reference</span></span>

<span data-ttu-id="4c763-117">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4c763-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4c763-118">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="4c763-118">**File**</span></span>|<span data-ttu-id="4c763-119">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="4c763-119">**Function**</span></span>|<span data-ttu-id="4c763-120">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="4c763-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4c763-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="4c763-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="4c763-122">PropCopyMore, HrCopyRestriction</span><span class="sxs-lookup"><span data-stu-id="4c763-122">PropCopyMore, HrCopyRestriction</span></span>  <br/> |<span data-ttu-id="4c763-123">Ces fonctions montrent comment PT_SRESTRICTION **une** propriété à des fins de copie dans une autre propriété.</span><span class="sxs-lookup"><span data-stu-id="4c763-123">These functions demonstrate how to parse a **PT_SRESTRICTION** property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4c763-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4c763-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4c763-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="4c763-125">Protocol specifications</span></span>

<span data-ttu-id="4c763-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c763-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c763-127">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="4c763-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4c763-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c763-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c763-129">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="4c763-129">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="4c763-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c763-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c763-131">Définit les structures de données de base utilisées dans les opérations distantes.</span><span class="sxs-lookup"><span data-stu-id="4c763-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4c763-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4c763-132">Header files</span></span>

<span data-ttu-id="4c763-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c763-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c763-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4c763-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="4c763-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4c763-135">Mapitags.h</span></span>
  
> <span data-ttu-id="4c763-136">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="4c763-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c763-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c763-137">See also</span></span>



[<span data-ttu-id="4c763-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4c763-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c763-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4c763-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c763-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4c763-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c763-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4c763-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

