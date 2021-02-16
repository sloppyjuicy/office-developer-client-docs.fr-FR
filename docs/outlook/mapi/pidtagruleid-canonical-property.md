---
title: Propriété canonique PidTagRuleId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleId
api_type:
- COM
ms.assetid: 341e8db0-52b7-4ba7-aaa6-eedf2783b4e8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8d88838893836c550136be9556299258b44e3e49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359492"
---
# <a name="pidtagruleid-canonical-property"></a><span data-ttu-id="aff89-103">Propriété canonique PidTagRuleId</span><span class="sxs-lookup"><span data-stu-id="aff89-103">PidTagRuleId Canonical Property</span></span>

  
  
<span data-ttu-id="aff89-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aff89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aff89-105">Spécifie un identificateur unique que le serveur de messagerie génère pour chaque règle lors de sa première création.</span><span class="sxs-lookup"><span data-stu-id="aff89-105">Specifies a unique identifier the messaging server generates for each rule when the rule is first created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aff89-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="aff89-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aff89-107">PR_RULE_ID</span><span class="sxs-lookup"><span data-stu-id="aff89-107">PR_RULE_ID</span></span>  <br/> |
|<span data-ttu-id="aff89-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="aff89-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aff89-109">0x6674</span><span class="sxs-lookup"><span data-stu-id="aff89-109">0x6674</span></span>  <br/> |
|<span data-ttu-id="aff89-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="aff89-110">Data type:</span></span>  <br/> |<span data-ttu-id="aff89-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="aff89-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="aff89-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="aff89-112">Area:</span></span>  <br/> |<span data-ttu-id="aff89-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="aff89-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aff89-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="aff89-114">Remarks</span></span>

<span data-ttu-id="aff89-115">Le client ne doit pas spécifier cette propriété lors de la création d’une règle, mais il doit la spécifier lors de la modification ou de la suppression d’une règle.</span><span class="sxs-lookup"><span data-stu-id="aff89-115">The client must not specify this property when creating a new rule but must specify it when modifying or deleting a rule.</span></span>
  
<span data-ttu-id="aff89-116">Lors de la suppression d’une règle, la seule propriété que le client doit transmettre **est PR_RULE_ID** et ne doit pas transmettre d’autre propriété.</span><span class="sxs-lookup"><span data-stu-id="aff89-116">When deleting a rule, the only property the client must pass is **PR_RULE_ID** and should not pass in any other property.</span></span> <span data-ttu-id="aff89-117">Le serveur doit ignorer les propriétés autres que cette propriété.</span><span class="sxs-lookup"><span data-stu-id="aff89-117">The server must ignore properties other than this property.</span></span> <span data-ttu-id="aff89-118">Lors de l’ajout d’une règle, le client ne doit pas transmettre **PR_RULE_ID**, il doit passer les propriétés **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) et **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aff89-118">When adding a rule, the client must not pass in **PR_RULE_ID**, it must pass in the **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) and **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) properties.</span></span> <span data-ttu-id="aff89-119">Lors de la modification d’une règle, le client doit transmettre **PR_RULE_ID** et transmettre le reste des propriétés qui doivent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="aff89-119">When modifying a rule, the client must pass in **PR_RULE_ID** and should pass in the rest of the properties that need to be modified.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="aff89-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="aff89-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aff89-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="aff89-121">Protocol specifications</span></span>

<span data-ttu-id="aff89-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aff89-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aff89-123">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="aff89-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aff89-124">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aff89-124">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aff89-125">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="aff89-125">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aff89-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="aff89-126">Header files</span></span>

<span data-ttu-id="aff89-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aff89-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="aff89-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="aff89-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="aff89-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aff89-129">Mapitags.h</span></span>
  
> <span data-ttu-id="aff89-130">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="aff89-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aff89-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aff89-131">See also</span></span>



[<span data-ttu-id="aff89-132">Propriété canonique PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="aff89-132">PidTagRuleCondition Canonical Property</span></span>](pidtagrulecondition-canonical-property.md)
  
[<span data-ttu-id="aff89-133">Propriété canonique PidTagRuleActions</span><span class="sxs-lookup"><span data-stu-id="aff89-133">PidTagRuleActions Canonical Property</span></span>](pidtagruleactions-canonical-property.md)
  
[<span data-ttu-id="aff89-134">Propriété canonique PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="aff89-134">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="aff89-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="aff89-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aff89-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="aff89-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aff89-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="aff89-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aff89-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="aff89-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

