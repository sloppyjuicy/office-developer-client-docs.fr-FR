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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 9d1adb6dd1fc151c9a599ea44391c2ca5b2fe2aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580564"
---
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="86e87-103">Propriété canonique PidTagRuleState</span><span class="sxs-lookup"><span data-stu-id="86e87-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="86e87-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86e87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86e87-105">Une valeur est interprétée comme une combinaison de masque de bits d’indicateurs qui spécifient l’état de la règle.</span><span class="sxs-lookup"><span data-stu-id="86e87-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86e87-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="86e87-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="86e87-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="86e87-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="86e87-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="86e87-108">Identifier:</span></span>  <br/> |<span data-ttu-id="86e87-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="86e87-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="86e87-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="86e87-110">Data type:</span></span>  <br/> |<span data-ttu-id="86e87-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="86e87-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="86e87-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="86e87-112">Area:</span></span>  <br/> |<span data-ttu-id="86e87-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="86e87-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86e87-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="86e87-114">Remarks</span></span>

<span data-ttu-id="86e87-115">Le tableau suivant définit les valeurs possibles de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="86e87-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="86e87-116">Fr-fr (ST_ENABLED, masque de bits 0 x 00000001)</span><span class="sxs-lookup"><span data-stu-id="86e87-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="86e87-117">La règle est activée pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="86e87-117">The rule is enabled for execution.</span></span> <span data-ttu-id="86e87-118">Si cet indicateur n’est pas défini, le serveur doit ignorer cette règle lors de l’évaluation des règles.</span><span class="sxs-lookup"><span data-stu-id="86e87-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="86e87-119">Restauration d’urgence (ST_ERROR, masque de bits 0 x 00000002)</span><span class="sxs-lookup"><span data-stu-id="86e87-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="86e87-120">Le serveur a rencontré une erreur de traitement de la règle.</span><span class="sxs-lookup"><span data-stu-id="86e87-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="86e87-121">DE (ST_ONLY_WHEN_OOF, masque de bits 0 x 00000004)</span><span class="sxs-lookup"><span data-stu-id="86e87-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="86e87-122">La règle est exécutée uniquement lorsque l’utilisateur définit l’état d’absence du bureau (OOF) dans la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="86e87-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="86e87-123">Cet indicateur ne doit pas être défini dans une règle de dossier public.</span><span class="sxs-lookup"><span data-stu-id="86e87-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="86e87-124">HI (ST_KEEP_OOF_HIST, masque de bits 0 x 00000008)</span><span class="sxs-lookup"><span data-stu-id="86e87-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="86e87-125">Cet indicateur ne doit pas être défini dans une règle de dossier public.</span><span class="sxs-lookup"><span data-stu-id="86e87-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="86e87-126">EL (ST_EXIT_LEVEL, masque de bits 0 x 00000010)</span><span class="sxs-lookup"><span data-stu-id="86e87-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="86e87-127">Évaluation de la règle se termine après l’exécution de cette règle, à l’exception d’évaluation des règles d’absence du bureau.</span><span class="sxs-lookup"><span data-stu-id="86e87-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="86e87-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, masque de bits 0 x 00000020)</span><span class="sxs-lookup"><span data-stu-id="86e87-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="86e87-129">Évaluation de cette règle peut être ignorée.</span><span class="sxs-lookup"><span data-stu-id="86e87-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="86e87-130">PE (ST_RULE_PARSE_ERROR, masque de bits 0 x 00000040)</span><span class="sxs-lookup"><span data-stu-id="86e87-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="86e87-131">Le serveur a rencontré une erreur de l’analyse des données règle fournies par le client.</span><span class="sxs-lookup"><span data-stu-id="86e87-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="86e87-132">X </span><span class="sxs-lookup"><span data-stu-id="86e87-132">X</span></span>
  
> <span data-ttu-id="86e87-133">N’est pas utilisé par ce protocole.</span><span class="sxs-lookup"><span data-stu-id="86e87-133">Unused by this protocol.</span></span> <span data-ttu-id="86e87-134">Ce bit ne doit pas être modifié par le client.</span><span class="sxs-lookup"><span data-stu-id="86e87-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="86e87-135">Indicateurs de note sur l’interaction entre ST_ONLY_WHEN_OOF et ST_EXIT_LEVEL :</span><span class="sxs-lookup"><span data-stu-id="86e87-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="86e87-136">Lorsque l’état « d’absence du bureau » est définie sur la boîte aux lettres, et une condition a la valeur TRUE,</span><span class="sxs-lookup"><span data-stu-id="86e87-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="86e87-137">ET :</span><span class="sxs-lookup"><span data-stu-id="86e87-137">AND:</span></span>
  
- <span data-ttu-id="86e87-138">La règle a l’indicateur ST_EXIT_LEVEL défini et l’indicateur ST_ONLY_WHEN_OOF n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="86e87-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="86e87-139">Puis, le serveur ne doit pas évaluer les règles suivantes qui n’ont pas ST_ONLY_WHEN_OOF l’indicateur est défini et doit prendre les règles suivantes qui indicateur ST_ONLY_WHEN_OOF ont été défini.</span><span class="sxs-lookup"><span data-stu-id="86e87-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="86e87-140">OR :</span><span class="sxs-lookup"><span data-stu-id="86e87-140">OR:</span></span>
  
- <span data-ttu-id="86e87-141">La règle possède à la fois les ST_EXIT_LEVEL ST_ONLY_WHEN_OOF indicateurs et définir.</span><span class="sxs-lookup"><span data-stu-id="86e87-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="86e87-142">Puis, le serveur ne doit pas évaluer toutes les règles suivantes.</span><span class="sxs-lookup"><span data-stu-id="86e87-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="86e87-143">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="86e87-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="86e87-144">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="86e87-144">Protocol specifications</span></span>

<span data-ttu-id="86e87-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e87-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86e87-146">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="86e87-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="86e87-147">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e87-147">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86e87-148">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="86e87-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="86e87-149">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="86e87-149">Header files</span></span>

<span data-ttu-id="86e87-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86e87-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="86e87-151">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="86e87-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="86e87-152">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="86e87-152">Mapitags.h</span></span>
  
> <span data-ttu-id="86e87-153">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="86e87-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="86e87-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86e87-154">See also</span></span>



[<span data-ttu-id="86e87-155">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="86e87-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="86e87-156">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="86e87-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="86e87-157">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="86e87-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="86e87-158">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="86e87-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

