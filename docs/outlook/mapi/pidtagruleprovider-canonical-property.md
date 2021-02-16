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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 19889a1f48a6088f0d5ad224f7e9189b112622fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280604"
---
# <a name="pidtagruleprovider-canonical-property"></a><span data-ttu-id="c8802-103">Propriété canonique PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="c8802-103">PidTagRuleProvider Canonical Property</span></span>

  
  
<span data-ttu-id="c8802-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8802-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8802-105">Contient le nom de l’application qui définit une règle.</span><span class="sxs-lookup"><span data-stu-id="c8802-105">Contains the name of the application that sets a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8802-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c8802-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8802-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A, PR_RULE_PROVIDER_W</span><span class="sxs-lookup"><span data-stu-id="c8802-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span></span>  <br/> |
|<span data-ttu-id="c8802-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c8802-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c8802-109">0x6681</span><span class="sxs-lookup"><span data-stu-id="c8802-109">0x6681</span></span>  <br/> |
|<span data-ttu-id="c8802-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c8802-110">Data type:</span></span>  <br/> |<span data-ttu-id="c8802-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c8802-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c8802-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c8802-112">Area:</span></span>  <br/> |<span data-ttu-id="c8802-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="c8802-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8802-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c8802-114">Remarks</span></span>

<span data-ttu-id="c8802-115">Les actions différées ont besoin de ces propriétés pour identifier le code qui doit interpréter et exécuter l’action de règle.</span><span class="sxs-lookup"><span data-stu-id="c8802-115">Deferred actions need these properties to identify the code that must interpret and execute the rule action.</span></span>
  
<span data-ttu-id="c8802-116">Les règles stockées dans les boîtes aux lettres et les dossiers sont associées à l’application qui les possède par une chaîne de fournisseur de règles.</span><span class="sxs-lookup"><span data-stu-id="c8802-116">Rules stored on mailboxes and folders are associated with the application that owns them by a rule provider string.</span></span> <span data-ttu-id="c8802-117">Un fournisseur de règles définit et gère les règles dans une table de règles.</span><span class="sxs-lookup"><span data-stu-id="c8802-117">A rule provider sets and handles rules in a rule table.</span></span> <span data-ttu-id="c8802-118">Il fournit également un moyen de gérer les actions différées si de telles règles sont définies.</span><span class="sxs-lookup"><span data-stu-id="c8802-118">It also provides a means of handling any deferred actions if such rules are set.</span></span> <span data-ttu-id="c8802-119">Les actions différées sont créées implicitement par la boutique d’informations.</span><span class="sxs-lookup"><span data-stu-id="c8802-119">Deferred actions are created implicitly by the information store.</span></span> <span data-ttu-id="c8802-120">Pour les opérations de déplacement ou de copie dans un autre magasin, si un fournisseur définit une règle d’action différée, il doit fournir un responsable pour effectuer l’action lorsque la règle est déclenché et qu’une action différée est créée.</span><span class="sxs-lookup"><span data-stu-id="c8802-120">For move or copy operations to a different store, if a provider sets a deferred action rule, it must provide a handler to perform the action when the rule is fired and a deferred action is created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c8802-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c8802-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c8802-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="c8802-122">Protocol specifications</span></span>

<span data-ttu-id="c8802-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8802-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8802-124">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="c8802-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c8802-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c8802-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c8802-126">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="c8802-126">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c8802-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c8802-127">Header files</span></span>

<span data-ttu-id="c8802-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8802-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8802-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c8802-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="c8802-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c8802-130">Mapitags.h</span></span>
  
> <span data-ttu-id="c8802-131">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="c8802-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8802-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8802-132">See also</span></span>



[<span data-ttu-id="c8802-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c8802-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8802-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c8802-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8802-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c8802-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8802-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c8802-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

