---
title: Propriété canonique PidTagRuleState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleState
api_type:
- COM
ms.assetid: f62f3055-b855-4203-aa5c-6ba28b58c6f7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a0e15462cd3dc14c93155e34e47b7caac2c04087
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338611"
---
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="a5d10-103">Propriété canonique PidTagRuleState</span><span class="sxs-lookup"><span data-stu-id="a5d10-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="a5d10-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5d10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5d10-105">Valeur interprétée comme une combinaison de masque de bits d’indicateurs spécifiant l’état de la règle.</span><span class="sxs-lookup"><span data-stu-id="a5d10-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5d10-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a5d10-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5d10-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="a5d10-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="a5d10-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a5d10-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a5d10-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="a5d10-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="a5d10-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a5d10-110">Data type:</span></span>  <br/> |<span data-ttu-id="a5d10-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a5d10-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a5d10-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a5d10-112">Area:</span></span>  <br/> |<span data-ttu-id="a5d10-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="a5d10-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5d10-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a5d10-114">Remarks</span></span>

<span data-ttu-id="a5d10-115">Le tableau suivant définit les valeurs possibles de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="a5d10-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="a5d10-116">EN (ST_ENABLED, masque de bits 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="a5d10-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="a5d10-117">La règle est activée pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="a5d10-117">The rule is enabled for execution.</span></span> <span data-ttu-id="a5d10-118">Si cet indicateur n’est pas définie, le serveur doit ignorer cette règle lors de l’évaluation des règles.</span><span class="sxs-lookup"><span data-stu-id="a5d10-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="a5d10-119">ER (ST_ERROR, masque de bits 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="a5d10-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="a5d10-120">Le serveur a rencontré une erreur de traitement de la règle.</span><span class="sxs-lookup"><span data-stu-id="a5d10-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="a5d10-121">OF (ST_ONLY_WHEN_OOF, masque de bits 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="a5d10-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="a5d10-122">La règle est exécutée uniquement lorsque l’utilisateur définit l’état d’absence du bureau sur la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a5d10-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="a5d10-123">Cet indicateur ne doit pas être définie dans une règle de dossier public.</span><span class="sxs-lookup"><span data-stu-id="a5d10-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="a5d10-124">HI (ST_KEEP_OOF_HIST, masque de bits 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="a5d10-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="a5d10-125">Cet indicateur ne doit pas être définie dans une règle de dossier public.</span><span class="sxs-lookup"><span data-stu-id="a5d10-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="a5d10-126">EL (ST_EXIT_LEVEL, masque de bits 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="a5d10-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="a5d10-127">L’évaluation de la règle se termine après l’exécution de cette règle, à l’exception de l’évaluation des règles d’int office.</span><span class="sxs-lookup"><span data-stu-id="a5d10-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="a5d10-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, masque de bits 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="a5d10-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="a5d10-129">L’évaluation de cette règle peut être ignorée.</span><span class="sxs-lookup"><span data-stu-id="a5d10-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="a5d10-130">PE (ST_RULE_PARSE_ERROR, masque de bits 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="a5d10-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="a5d10-131">Le serveur a rencontré une erreur lors de l’analyse des données de règle fournies par le client.</span><span class="sxs-lookup"><span data-stu-id="a5d10-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="a5d10-132">X</span><span class="sxs-lookup"><span data-stu-id="a5d10-132">X</span></span>
  
> <span data-ttu-id="a5d10-133">Inutilisé par ce protocole.</span><span class="sxs-lookup"><span data-stu-id="a5d10-133">Unused by this protocol.</span></span> <span data-ttu-id="a5d10-134">Ce bit ne doit pas être modifié par le client.</span><span class="sxs-lookup"><span data-stu-id="a5d10-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="a5d10-135">Notez l’interaction entre ST_ONLY_WHEN_OOF et ST_EXIT_LEVEL indicateurs :</span><span class="sxs-lookup"><span data-stu-id="a5d10-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="a5d10-136">Lorsque l’état « Out of Office » est définie sur la boîte aux lettres et qu’une condition de règle est évaluée à TRUE,</span><span class="sxs-lookup"><span data-stu-id="a5d10-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="a5d10-137">ET :</span><span class="sxs-lookup"><span data-stu-id="a5d10-137">AND:</span></span>
  
- <span data-ttu-id="a5d10-138">La règle possède l’indicateur ST_EXIT_LEVEL et n’a pas d’indicateur ST_ONLY_WHEN_OOF définie.</span><span class="sxs-lookup"><span data-stu-id="a5d10-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="a5d10-139">Ensuite, le serveur ne doit pas évaluer les règles suivantes qui n’ont pas d’indicateur ST_ONLY_WHEN_OOF, et doit évaluer les règles suivantes qui ont ST_ONLY_WHEN_OOF d’indicateur.</span><span class="sxs-lookup"><span data-stu-id="a5d10-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="a5d10-140">OU :</span><span class="sxs-lookup"><span data-stu-id="a5d10-140">OR:</span></span>
  
- <span data-ttu-id="a5d10-141">Les indicateurs ST_EXIT_LEVEL et ST_ONLY_WHEN_OOF règle sont tous deux définies.</span><span class="sxs-lookup"><span data-stu-id="a5d10-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="a5d10-142">Ensuite, le serveur ne doit pas évaluer les règles suivantes.</span><span class="sxs-lookup"><span data-stu-id="a5d10-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a5d10-143">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a5d10-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5d10-144">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="a5d10-144">Protocol specifications</span></span>

<span data-ttu-id="a5d10-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5d10-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5d10-146">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="a5d10-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5d10-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5d10-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5d10-148">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="a5d10-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5d10-149">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a5d10-149">Header files</span></span>

<span data-ttu-id="a5d10-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5d10-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5d10-151">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a5d10-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="a5d10-152">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a5d10-152">Mapitags.h</span></span>
  
> <span data-ttu-id="a5d10-153">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="a5d10-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5d10-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5d10-154">See also</span></span>



[<span data-ttu-id="a5d10-155">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a5d10-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5d10-156">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a5d10-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5d10-157">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a5d10-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5d10-158">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a5d10-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

