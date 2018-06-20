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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f4eae388d51b0428d508a675681fa4cd1d94e46f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786651"
---
# <a name="pidtagrulecondition-canonical-property"></a><span data-ttu-id="96fa0-103">Propriété canonique PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="96fa0-103">PidTagRuleCondition Canonical Property</span></span>

  
  
<span data-ttu-id="96fa0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="96fa0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="96fa0-105">La condition utilisée lors de l’évaluation de la règle.</span><span class="sxs-lookup"><span data-stu-id="96fa0-105">The condition used when you evaluate the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96fa0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="96fa0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96fa0-107">PR_RULE_CONDITION</span><span class="sxs-lookup"><span data-stu-id="96fa0-107">PR_RULE_CONDITION</span></span>  <br/> |
|<span data-ttu-id="96fa0-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="96fa0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="96fa0-109">0x6679</span><span class="sxs-lookup"><span data-stu-id="96fa0-109">0x6679</span></span>  <br/> |
|<span data-ttu-id="96fa0-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="96fa0-110">Data type:</span></span>  <br/> |<span data-ttu-id="96fa0-111">PT_SRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="96fa0-111">PT_SRESTRICTION</span></span>  <br/> |
|<span data-ttu-id="96fa0-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="96fa0-112">Area:</span></span>  <br/> |<span data-ttu-id="96fa0-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="96fa0-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96fa0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="96fa0-114">Remarks</span></span>

<span data-ttu-id="96fa0-115">La condition est exprimée sous la forme d’une **Restriction** et la mémoire tampon **PropertyValue** contient la structure de **Restriction** empaquetée tel que spécifié dans [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="96fa0-115">The condition is expressed as a **Restriction** and the **PropertyValue** buffer contains the **Restriction** structure packaged as specified in [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="96fa0-116">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="96fa0-116">MFCMAPI reference</span></span>

<span data-ttu-id="96fa0-117">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="96fa0-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="96fa0-118">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="96fa0-118">**File**</span></span>|<span data-ttu-id="96fa0-119">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="96fa0-119">**Function**</span></span>|<span data-ttu-id="96fa0-120">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="96fa0-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="96fa0-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="96fa0-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="96fa0-122">PropCopyMore, HrCopyRestriction</span><span class="sxs-lookup"><span data-stu-id="96fa0-122">PropCopyMore, HrCopyRestriction</span></span>  <br/> |<span data-ttu-id="96fa0-123">Ces fonctions vous montrer comment analyser une propriété **PT_SRESTRICTION** à des fins de copie vers une autre propriété.</span><span class="sxs-lookup"><span data-stu-id="96fa0-123">These functions demonstrate how to parse a **PT_SRESTRICTION** property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="96fa0-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="96fa0-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="96fa0-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="96fa0-125">Protocol specifications</span></span>

<span data-ttu-id="96fa0-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96fa0-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96fa0-127">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="96fa0-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="96fa0-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96fa0-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96fa0-129">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="96fa0-129">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="96fa0-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96fa0-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96fa0-131">Définit les structures de base de données qui sont utilisés dans les opérations à distance.</span><span class="sxs-lookup"><span data-stu-id="96fa0-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="96fa0-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="96fa0-132">Header files</span></span>

<span data-ttu-id="96fa0-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96fa0-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="96fa0-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="96fa0-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="96fa0-135">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="96fa0-135">Mapitags.h</span></span>
  
> <span data-ttu-id="96fa0-136">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="96fa0-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96fa0-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96fa0-137">See also</span></span>



[<span data-ttu-id="96fa0-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="96fa0-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96fa0-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="96fa0-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96fa0-140">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="96fa0-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96fa0-141">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="96fa0-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

