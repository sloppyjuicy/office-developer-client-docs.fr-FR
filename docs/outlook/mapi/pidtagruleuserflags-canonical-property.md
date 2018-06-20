---
title: Propriété canonique PidTagRuleUserFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleUserFlags
api_type:
- COM
ms.assetid: c5dfb21f-b35e-4521-bf2b-e3d03d98d75d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8a44c88cbc971d9d5358fc6b24093e56e9565eb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786682"
---
# <a name="pidtagruleuserflags-canonical-property"></a><span data-ttu-id="4446a-103">Propriété canonique PidTagRuleUserFlags</span><span class="sxs-lookup"><span data-stu-id="4446a-103">PidTagRuleUserFlags Canonical Property</span></span>

  
  
<span data-ttu-id="4446a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4446a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4446a-105">Cette propriété est définie par le client à l’usage exclusif du client.</span><span class="sxs-lookup"><span data-stu-id="4446a-105">This property is set by the client for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4446a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4446a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4446a-107">PR_RULE_USER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="4446a-107">PR_RULE_USER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="4446a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4446a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4446a-109">0x6678</span><span class="sxs-lookup"><span data-stu-id="4446a-109">0x6678</span></span>  <br/> |
|<span data-ttu-id="4446a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4446a-110">Data type:</span></span>  <br/> |<span data-ttu-id="4446a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4446a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4446a-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="4446a-112">Area:</span></span>  <br/> |<span data-ttu-id="4446a-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="4446a-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4446a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4446a-114">Remarks</span></span>

<span data-ttu-id="4446a-115">Le serveur doit conserver la valeur de cette propriété si elle a été définie par le client.</span><span class="sxs-lookup"><span data-stu-id="4446a-115">The server must preserve the value of this property if it was set by the client.</span></span> <span data-ttu-id="4446a-116">Le serveur doit ignorer pendant le traitement et l’évaluation de la règle.</span><span class="sxs-lookup"><span data-stu-id="4446a-116">The server must ignore it during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4446a-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4446a-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4446a-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="4446a-118">Protocol specifications</span></span>

<span data-ttu-id="4446a-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4446a-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4446a-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="4446a-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4446a-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4446a-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4446a-122">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="4446a-122">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4446a-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4446a-123">Header files</span></span>

<span data-ttu-id="4446a-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4446a-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4446a-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4446a-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4446a-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="4446a-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4446a-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="4446a-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4446a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4446a-128">See also</span></span>



[<span data-ttu-id="4446a-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4446a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4446a-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4446a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4446a-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4446a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4446a-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="4446a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

