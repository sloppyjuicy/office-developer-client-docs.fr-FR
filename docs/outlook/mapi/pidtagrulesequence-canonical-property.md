---
title: Propriété canonique PidTagRuleSequence
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleSequence
api_type:
- COM
ms.assetid: c42f2539-f7d6-464a-a82c-f0ac51823168
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7f36562ba189cd8f547056b93c0f0373ee9a3360
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563491"
---
# <a name="pidtagrulesequence-canonical-property"></a><span data-ttu-id="bab00-103">Propriété canonique PidTagRuleSequence</span><span class="sxs-lookup"><span data-stu-id="bab00-103">PidTagRuleSequence Canonical Property</span></span>

  
  
<span data-ttu-id="bab00-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bab00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bab00-105">Une valeur utilisée pour déterminer l’ordre dans lequel les règles sont évaluées et exécutées.</span><span class="sxs-lookup"><span data-stu-id="bab00-105">A value used to determine the order in which rules are evaluated and executed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bab00-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bab00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bab00-107">PR_RULE_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="bab00-107">PR_RULE_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="bab00-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="bab00-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bab00-109">0x6676</span><span class="sxs-lookup"><span data-stu-id="bab00-109">0x6676</span></span>  <br/> |
|<span data-ttu-id="bab00-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="bab00-110">Data type:</span></span>  <br/> |<span data-ttu-id="bab00-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bab00-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bab00-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="bab00-112">Area:</span></span>  <br/> |<span data-ttu-id="bab00-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="bab00-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bab00-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="bab00-114">Remarks</span></span>

<span data-ttu-id="bab00-115">Les règles sont évaluées dans l’ordre en fonction de l’ordre croissant de cette valeur.</span><span class="sxs-lookup"><span data-stu-id="bab00-115">Rules are evaluated in sequence according to the increasing order of this value.</span></span> <span data-ttu-id="bab00-116">L’ordre d’évaluation pour les règles qui ont la même valeur dans cette propriété n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="bab00-116">The evaluation order for rules that have the same value in this property is undefined.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bab00-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="bab00-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bab00-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="bab00-118">Protocol specifications</span></span>

<span data-ttu-id="bab00-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bab00-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bab00-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="bab00-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bab00-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bab00-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bab00-122">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="bab00-122">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="bab00-123">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bab00-123">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bab00-124">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les éléments de calendrier et de message lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bab00-124">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="bab00-125">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bab00-125">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bab00-126">Inclut les opérations autorisées pour les objets de la table principale.</span><span class="sxs-lookup"><span data-stu-id="bab00-126">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="bab00-127">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bab00-127">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bab00-128">Spécifie les opérations autorisées pour les objets de banque de messages principale.</span><span class="sxs-lookup"><span data-stu-id="bab00-128">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bab00-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="bab00-129">Header files</span></span>

<span data-ttu-id="bab00-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bab00-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="bab00-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bab00-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="bab00-132">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="bab00-132">Mapitags.h</span></span>
  
> <span data-ttu-id="bab00-133">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="bab00-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bab00-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bab00-134">See also</span></span>



[<span data-ttu-id="bab00-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bab00-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bab00-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="bab00-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bab00-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="bab00-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bab00-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="bab00-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

