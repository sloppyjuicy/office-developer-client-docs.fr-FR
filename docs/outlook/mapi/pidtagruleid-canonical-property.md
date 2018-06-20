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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 52a6132dcd6aa2c3a2951f3d1a6458808364dccb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786649"
---
# <a name="pidtagruleid-canonical-property"></a><span data-ttu-id="27128-103">Propriété canonique PidTagRuleId</span><span class="sxs-lookup"><span data-stu-id="27128-103">PidTagRuleId Canonical Property</span></span>

  
  
<span data-ttu-id="27128-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27128-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27128-105">Spécifie un identificateur unique du serveur de messagerie génère pour chaque règle lors de la création de la règle.</span><span class="sxs-lookup"><span data-stu-id="27128-105">Specifies a unique identifier the messaging server generates for each rule when the rule is first created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27128-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="27128-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27128-107">PR_RULE_ID</span><span class="sxs-lookup"><span data-stu-id="27128-107">PR_RULE_ID</span></span>  <br/> |
|<span data-ttu-id="27128-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="27128-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27128-109">0x6674</span><span class="sxs-lookup"><span data-stu-id="27128-109">0x6674</span></span>  <br/> |
|<span data-ttu-id="27128-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="27128-110">Data type:</span></span>  <br/> |<span data-ttu-id="27128-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="27128-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="27128-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="27128-112">Area:</span></span>  <br/> |<span data-ttu-id="27128-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="27128-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27128-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="27128-114">Remarks</span></span>

<span data-ttu-id="27128-115">Le client ne doit pas spécifier de cette propriété lorsque vous créez une nouvelle règle mais doit spécifier lors de la modification ou suppression d’une règle.</span><span class="sxs-lookup"><span data-stu-id="27128-115">The client must not specify this property when creating a new rule but must specify it when modifying or deleting a rule.</span></span>
  
<span data-ttu-id="27128-116">Lorsque vous supprimez une règle, la seule propriété que le client doit transmettre est **PR_RULE_ID** et ne doit pas passer dans n’importe quelle autre propriété.</span><span class="sxs-lookup"><span data-stu-id="27128-116">When deleting a rule, the only property the client must pass is **PR_RULE_ID** and should not pass in any other property.</span></span> <span data-ttu-id="27128-117">Le serveur doit ignorer les propriétés de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="27128-117">The server must ignore properties other than this property.</span></span> <span data-ttu-id="27128-118">Lorsque vous ajoutez une règle, le client ne doit pas passer dans **PR_RULE_ID**, il doit passer **PR_RULE_PROVIDER** ([ , **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) et **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)) PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) Propriétés.</span><span class="sxs-lookup"><span data-stu-id="27128-118">When adding a rule, the client must not pass in **PR_RULE_ID**, it must pass in the **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) and **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) properties.</span></span> <span data-ttu-id="27128-119">Lorsque vous modifiez une règle, le client doit passer **PR_RULE_ID** et doit transmettre le reste des propriétés qui doivent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="27128-119">When modifying a rule, the client must pass in **PR_RULE_ID** and should pass in the rest of the properties that need to be modified.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="27128-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="27128-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27128-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="27128-121">Protocol specifications</span></span>

<span data-ttu-id="27128-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27128-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27128-123">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="27128-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="27128-124">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27128-124">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27128-125">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="27128-125">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27128-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="27128-126">Header files</span></span>

<span data-ttu-id="27128-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27128-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="27128-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="27128-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="27128-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="27128-129">Mapitags.h</span></span>
  
> <span data-ttu-id="27128-130">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="27128-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27128-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27128-131">See also</span></span>



[<span data-ttu-id="27128-132">Propriété canonique PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="27128-132">PidTagRuleCondition Canonical Property</span></span>](pidtagrulecondition-canonical-property.md)
  
[<span data-ttu-id="27128-133">Propriété canonique PidTagRuleActions</span><span class="sxs-lookup"><span data-stu-id="27128-133">PidTagRuleActions Canonical Property</span></span>](pidtagruleactions-canonical-property.md)
  
[<span data-ttu-id="27128-134">Propriété canonique PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="27128-134">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="27128-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="27128-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27128-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="27128-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27128-137">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="27128-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27128-138">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="27128-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

