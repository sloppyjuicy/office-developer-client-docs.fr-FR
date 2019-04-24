---
title: Propriété canonique PidTagRuleActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleActions
api_type:
- COM
ms.assetid: 3ec4259a-8fe9-46c3-82b8-42c6907b8515
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ab246414f7caaf76f462d9b80e762fe614c77c21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278899"
---
# <a name="pidtagruleactions-canonical-property"></a><span data-ttu-id="e1df4-103">Propriété canonique PidTagRuleActions</span><span class="sxs-lookup"><span data-stu-id="e1df4-103">PidTagRuleActions Canonical Property</span></span>

  
  
<span data-ttu-id="e1df4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1df4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1df4-105">Contient l'ensemble des actions associées à la règle.</span><span class="sxs-lookup"><span data-stu-id="e1df4-105">Contains the set of actions associated with the rule.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1df4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e1df4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1df4-107">PR_RULE_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="e1df4-107">PR_RULE_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="e1df4-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e1df4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e1df4-109">0x6680</span><span class="sxs-lookup"><span data-stu-id="e1df4-109">0x6680</span></span>  <br/> |
|<span data-ttu-id="e1df4-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e1df4-110">Data type:</span></span>  <br/> |<span data-ttu-id="e1df4-111">PT_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="e1df4-111">PT_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="e1df4-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e1df4-112">Area:</span></span>  <br/> |<span data-ttu-id="e1df4-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="e1df4-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1df4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e1df4-114">Remarks</span></span>

<span data-ttu-id="e1df4-115">Les actions sont exprimées sous la forme d'une action de règle et la mémoire tampon de valeur de la propriété contient la structure de mémoire tampon des données de l'action de règle empaquetées comme spécifié dans [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e1df4-115">The actions are expressed as a rule action and the property value buffer contains the rule action data buffer structure packaged as specified in [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e1df4-116">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e1df4-116">MFCMAPI reference</span></span>

<span data-ttu-id="e1df4-117">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e1df4-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e1df4-118">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="e1df4-118">**File**</span></span>|<span data-ttu-id="e1df4-119">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="e1df4-119">**Function**</span></span>|<span data-ttu-id="e1df4-120">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="e1df4-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e1df4-121">ImportProcs. cpp</span><span class="sxs-lookup"><span data-stu-id="e1df4-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="e1df4-122">PropCopyMore, HrCopyActions</span><span class="sxs-lookup"><span data-stu-id="e1df4-122">PropCopyMore, HrCopyActions</span></span>  <br/> |<span data-ttu-id="e1df4-123">Ces fonctions montrent comment analyser une propriété PT_ACTIONS à des fins de copie vers une autre propriété.</span><span class="sxs-lookup"><span data-stu-id="e1df4-123">These functions demonstrate how to parse a PT_ACTIONS property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e1df4-124">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="e1df4-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1df4-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="e1df4-125">Protocol specifications</span></span>

<span data-ttu-id="e1df4-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1df4-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1df4-127">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="e1df4-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1df4-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1df4-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1df4-129">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="e1df4-129">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1df4-130">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="e1df4-130">Header files</span></span>

<span data-ttu-id="e1df4-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e1df4-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1df4-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e1df4-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1df4-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e1df4-133">Mapitags.h</span></span>
  
> <span data-ttu-id="e1df4-134">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="e1df4-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1df4-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1df4-135">See also</span></span>



[<span data-ttu-id="e1df4-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e1df4-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1df4-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e1df4-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1df4-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e1df4-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1df4-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e1df4-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

