---
title: Propriété canonique PidTagRuleProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProvider
api_type:
- COM
ms.assetid: 64f80a03-9ba4-495a-9666-b3a909335cb6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5456e0abffd1ac25983809d32fde88644eaa01cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786668"
---
# <a name="pidtagruleprovider-canonical-property"></a><span data-ttu-id="43230-103">Propriété canonique PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="43230-103">PidTagRuleProvider Canonical Property</span></span>

  
  
<span data-ttu-id="43230-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="43230-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="43230-105">Contient le nom de l’application qui définit une règle.</span><span class="sxs-lookup"><span data-stu-id="43230-105">Contains the name of the application that sets a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43230-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="43230-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43230-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A, PR_RULE_PROVIDER_W</span><span class="sxs-lookup"><span data-stu-id="43230-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span></span>  <br/> |
|<span data-ttu-id="43230-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="43230-108">Identifier:</span></span>  <br/> |<span data-ttu-id="43230-109">0x6681</span><span class="sxs-lookup"><span data-stu-id="43230-109">0x6681</span></span>  <br/> |
|<span data-ttu-id="43230-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="43230-110">Data type:</span></span>  <br/> |<span data-ttu-id="43230-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="43230-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="43230-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="43230-112">Area:</span></span>  <br/> |<span data-ttu-id="43230-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="43230-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43230-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="43230-114">Remarks</span></span>

<span data-ttu-id="43230-115">Différé actions besoin de ces propriétés pour identifier le code qui doivent interpréter et exécuter l’action de règle.</span><span class="sxs-lookup"><span data-stu-id="43230-115">Deferred actions need these properties to identify the code that must interpret and execute the rule action.</span></span>
  
<span data-ttu-id="43230-116">Règles stockées sur les boîtes aux lettres et des dossiers sont associés à l’application qui leur propriétaire par une chaîne de fournisseur de règle.</span><span class="sxs-lookup"><span data-stu-id="43230-116">Rules stored on mailboxes and folders are associated with the application that owns them by a rule provider string.</span></span> <span data-ttu-id="43230-117">Un fournisseur de règles définit et gère les règles dans une table de règles.</span><span class="sxs-lookup"><span data-stu-id="43230-117">A rule provider sets and handles rules in a rule table.</span></span> <span data-ttu-id="43230-118">Il fournit également un moyen de gérer les actions différées si ces règles sont définies.</span><span class="sxs-lookup"><span data-stu-id="43230-118">It also provides a means of handling any deferred actions if such rules are set.</span></span> <span data-ttu-id="43230-119">Actions différées sont créées implicitement par la banque d’informations.</span><span class="sxs-lookup"><span data-stu-id="43230-119">Deferred actions are created implicitly by the information store.</span></span> <span data-ttu-id="43230-120">Pour les opérations de copie ou de déplacement vers une autre banque, si un fournisseur définit une règle d’action différée, il doit fournir un gestionnaire pour exécuter l’action lorsque la règle est déclenchée et une action différée est créée.</span><span class="sxs-lookup"><span data-stu-id="43230-120">For move or copy operations to a different store, if a provider sets a deferred action rule, it must provide a handler to perform the action when the rule is fired and a deferred action is created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="43230-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="43230-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="43230-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="43230-122">Protocol specifications</span></span>

<span data-ttu-id="43230-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43230-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43230-124">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="43230-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="43230-125">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43230-125">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43230-126">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="43230-126">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="43230-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="43230-127">Header files</span></span>

<span data-ttu-id="43230-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43230-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="43230-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="43230-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="43230-130">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="43230-130">Mapitags.h</span></span>
  
> <span data-ttu-id="43230-131">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="43230-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43230-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43230-132">See also</span></span>



[<span data-ttu-id="43230-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="43230-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43230-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="43230-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43230-135">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="43230-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43230-136">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="43230-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

