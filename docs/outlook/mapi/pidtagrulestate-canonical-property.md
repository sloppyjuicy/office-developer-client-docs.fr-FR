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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a0e15462cd3dc14c93155e34e47b7caac2c04087
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338611"
---
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="c043e-103">Propriété canonique PidTagRuleState</span><span class="sxs-lookup"><span data-stu-id="c043e-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="c043e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c043e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c043e-105">Valeur interprétée comme une combinaison de masques binaires d'indicateurs qui spécifient l'état de la règle.</span><span class="sxs-lookup"><span data-stu-id="c043e-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c043e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c043e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c043e-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="c043e-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="c043e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c043e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c043e-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="c043e-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="c043e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c043e-110">Data type:</span></span>  <br/> |<span data-ttu-id="c043e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c043e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c043e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c043e-112">Area:</span></span>  <br/> |<span data-ttu-id="c043e-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="c043e-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c043e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c043e-114">Remarks</span></span>

<span data-ttu-id="c043e-115">Le tableau suivant définit les valeurs possibles de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c043e-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="c043e-116">En (ST_ENABLED, masque de masque 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="c043e-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="c043e-117">La règle est activée pour l'exécution.</span><span class="sxs-lookup"><span data-stu-id="c043e-117">The rule is enabled for execution.</span></span> <span data-ttu-id="c043e-118">Si cet indicateur n'est pas défini, le serveur doit ignorer cette règle lors de l'évaluation des règles.</span><span class="sxs-lookup"><span data-stu-id="c043e-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="c043e-119">ER (ST_ERROR, masque binaire 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="c043e-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="c043e-120">Le serveur a rencontré une erreur lors du traitement de la règle.</span><span class="sxs-lookup"><span data-stu-id="c043e-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="c043e-121">DE (ST_ONLY_WHEN_OOF, masque de binaire 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="c043e-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="c043e-122">La règle est exécutée uniquement lorsque l'utilisateur définit l'état de l'absence du bureau dans la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="c043e-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="c043e-123">Cet indicateur ne doit pas être défini dans une règle de dossiers publics.</span><span class="sxs-lookup"><span data-stu-id="c043e-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="c043e-124">Bonjour (ST_KEEP_OOF_HIST, masque de masque)</span><span class="sxs-lookup"><span data-stu-id="c043e-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="c043e-125">Cet indicateur ne doit pas être défini dans une règle de dossiers publics.</span><span class="sxs-lookup"><span data-stu-id="c043e-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="c043e-126">EL (ST_EXIT_LEVEL, masque de binaire 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="c043e-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="c043e-127">L'évaluation de la règle se terminera après l'exécution de cette règle, sauf pour l'évaluation des règles d'absence du bureau.</span><span class="sxs-lookup"><span data-stu-id="c043e-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="c043e-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, masque de binaire 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="c043e-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="c043e-129">L'évaluation de cette règle peut être ignorée.</span><span class="sxs-lookup"><span data-stu-id="c043e-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="c043e-130">PE (ST_RULE_PARSE_ERROR, masque de binaire 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="c043e-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="c043e-131">Le serveur a rencontré une erreur lors de l'analyse des données de règle fournies par le client.</span><span class="sxs-lookup"><span data-stu-id="c043e-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="c043e-132">X</span><span class="sxs-lookup"><span data-stu-id="c043e-132">X</span></span>
  
> <span data-ttu-id="c043e-133">Non utilisé par ce protocole.</span><span class="sxs-lookup"><span data-stu-id="c043e-133">Unused by this protocol.</span></span> <span data-ttu-id="c043e-134">Ce bit ne doit pas être modifié par le client.</span><span class="sxs-lookup"><span data-stu-id="c043e-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="c043e-135">Remarque sur l'interaction entre ST_ONLY_WHEN_OOF et ST_EXIT_LEVEL Flags:</span><span class="sxs-lookup"><span data-stu-id="c043e-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="c043e-136">Lorsque l'État «absent (e) du Bureau» est défini sur la boîte aux lettres et qu'une condition de règle donne la valeur TRUE,</span><span class="sxs-lookup"><span data-stu-id="c043e-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="c043e-137">LES</span><span class="sxs-lookup"><span data-stu-id="c043e-137">AND:</span></span>
  
- <span data-ttu-id="c043e-138">L'indicateur ST_EXIT_LEVEL est défini pour la règle et l'indicateur ST_ONLY_WHEN_OOF n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="c043e-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="c043e-139">Ensuite, le serveur ne doit pas évaluer les règles suivantes qui n'ont pas d'indicateur ST_ONLY_WHEN_OOF défini, et doit évaluer les règles suivantes qui ont un indicateur ST_ONLY_WHEN_OOF défini.</span><span class="sxs-lookup"><span data-stu-id="c043e-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="c043e-140">DES</span><span class="sxs-lookup"><span data-stu-id="c043e-140">OR:</span></span>
  
- <span data-ttu-id="c043e-141">Les indicateurs ST_EXIT_LEVEL et ST_ONLY_WHEN_OOF sont définis pour la règle.</span><span class="sxs-lookup"><span data-stu-id="c043e-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="c043e-142">Ensuite, le serveur ne doit pas évaluer les règles suivantes.</span><span class="sxs-lookup"><span data-stu-id="c043e-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="c043e-143">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="c043e-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c043e-144">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="c043e-144">Protocol specifications</span></span>

<span data-ttu-id="c043e-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c043e-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c043e-146">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="c043e-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c043e-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c043e-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c043e-148">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="c043e-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c043e-149">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="c043e-149">Header files</span></span>

<span data-ttu-id="c043e-150">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c043e-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="c043e-151">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c043e-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="c043e-152">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c043e-152">Mapitags.h</span></span>
  
> <span data-ttu-id="c043e-153">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="c043e-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c043e-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c043e-154">See also</span></span>



[<span data-ttu-id="c043e-155">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c043e-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c043e-156">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c043e-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c043e-157">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c043e-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c043e-158">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c043e-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

