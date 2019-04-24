---
title: Propriété canonique PidTagRuleProviderData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProviderData
api_type:
- COM
ms.assetid: b04a277c-b483-4f54-b360-311034b9a7ee
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e4d209c4f185ff253476beb04913e6a64884f9b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335419"
---
# <a name="pidtagruleproviderdata-canonical-property"></a><span data-ttu-id="07f22-103">Propriété canonique PidTagRuleProviderData</span><span class="sxs-lookup"><span data-stu-id="07f22-103">PidTagRuleProviderData Canonical Property</span></span>

  
  
<span data-ttu-id="07f22-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07f22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07f22-105">Propriété opaque définie par le client pour l'utilisation exclusive du client.</span><span class="sxs-lookup"><span data-stu-id="07f22-105">An opaque property that the client sets for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07f22-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="07f22-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="07f22-107">PR_RULE_PROVIDER_DATA</span><span class="sxs-lookup"><span data-stu-id="07f22-107">PR_RULE_PROVIDER_DATA</span></span>  <br/> |
|<span data-ttu-id="07f22-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="07f22-108">Identifier:</span></span>  <br/> |<span data-ttu-id="07f22-109">0x6684</span><span class="sxs-lookup"><span data-stu-id="07f22-109">0x6684</span></span>  <br/> |
|<span data-ttu-id="07f22-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="07f22-110">Data type:</span></span>  <br/> |<span data-ttu-id="07f22-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="07f22-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="07f22-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="07f22-112">Area:</span></span>  <br/> |<span data-ttu-id="07f22-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="07f22-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07f22-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="07f22-114">Remarks</span></span>

<span data-ttu-id="07f22-115">Le serveur doit conserver la valeur de cette propriété si elle a été définie par le client mais doit ignorer son contenu pendant l'évaluation et le traitement de la règle.</span><span class="sxs-lookup"><span data-stu-id="07f22-115">The server must preserve the value of this property if it was set by the client but must ignore its contents during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="07f22-116">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="07f22-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="07f22-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="07f22-117">Protocol specifications</span></span>

<span data-ttu-id="07f22-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07f22-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07f22-119">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="07f22-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="07f22-120">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07f22-120">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07f22-121">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="07f22-121">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="07f22-122">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="07f22-122">Header files</span></span>

<span data-ttu-id="07f22-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="07f22-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="07f22-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="07f22-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="07f22-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="07f22-125">Mapitags.h</span></span>
  
> <span data-ttu-id="07f22-126">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="07f22-126">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="07f22-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07f22-127">See also</span></span>



[<span data-ttu-id="07f22-128">Propriété canonique PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="07f22-128">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="07f22-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="07f22-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07f22-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="07f22-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07f22-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="07f22-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07f22-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="07f22-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

