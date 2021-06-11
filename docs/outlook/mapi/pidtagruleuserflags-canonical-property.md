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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 235efce341e1870f0c33917f1c6d42b021727308
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321342"
---
# <a name="pidtagruleuserflags-canonical-property"></a><span data-ttu-id="92ed6-103">Propriété canonique PidTagRuleUserFlags</span><span class="sxs-lookup"><span data-stu-id="92ed6-103">PidTagRuleUserFlags Canonical Property</span></span>

  
  
<span data-ttu-id="92ed6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92ed6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92ed6-105">Cette propriété est définie par le client pour l’utilisation exclusive du client.</span><span class="sxs-lookup"><span data-stu-id="92ed6-105">This property is set by the client for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92ed6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="92ed6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92ed6-107">PR_RULE_USER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="92ed6-107">PR_RULE_USER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="92ed6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="92ed6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="92ed6-109">0x6678</span><span class="sxs-lookup"><span data-stu-id="92ed6-109">0x6678</span></span>  <br/> |
|<span data-ttu-id="92ed6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="92ed6-110">Data type:</span></span>  <br/> |<span data-ttu-id="92ed6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="92ed6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="92ed6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="92ed6-112">Area:</span></span>  <br/> |<span data-ttu-id="92ed6-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="92ed6-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92ed6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="92ed6-114">Remarks</span></span>

<span data-ttu-id="92ed6-115">Le serveur doit conserver la valeur de cette propriété si elle a été définie par le client.</span><span class="sxs-lookup"><span data-stu-id="92ed6-115">The server must preserve the value of this property if it was set by the client.</span></span> <span data-ttu-id="92ed6-116">Le serveur doit l’ignorer pendant l’évaluation et le traitement de la règle.</span><span class="sxs-lookup"><span data-stu-id="92ed6-116">The server must ignore it during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="92ed6-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="92ed6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="92ed6-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="92ed6-118">Protocol specifications</span></span>

<span data-ttu-id="92ed6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92ed6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92ed6-120">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="92ed6-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="92ed6-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92ed6-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92ed6-122">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="92ed6-122">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="92ed6-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="92ed6-123">Header files</span></span>

<span data-ttu-id="92ed6-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92ed6-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="92ed6-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="92ed6-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="92ed6-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="92ed6-126">Mapitags.h</span></span>
  
> <span data-ttu-id="92ed6-127">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="92ed6-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92ed6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92ed6-128">See also</span></span>



[<span data-ttu-id="92ed6-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="92ed6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92ed6-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="92ed6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92ed6-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="92ed6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92ed6-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="92ed6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

