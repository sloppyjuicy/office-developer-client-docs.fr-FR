---
title: Propriété canonique PidTagExtendedRuleSizeLimit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleSizeLimit
api_type:
- HeaderDef
ms.assetid: 87186764-fb58-4cdf-804d-bb13c5a8cb65
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 336f2b4bd6a4251548284eae91a51ad7018949c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582125"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a><span data-ttu-id="e8f22-103">Propriété canonique PidTagExtendedRuleSizeLimit</span><span class="sxs-lookup"><span data-stu-id="e8f22-103">PidTagExtendedRuleSizeLimit Canonical Property</span></span>

  
  
<span data-ttu-id="e8f22-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8f22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8f22-105">Indique la taille maximale, en octets, l’utilisateur est autorisé à s’accumulent pour une seule règle « étendue ».</span><span class="sxs-lookup"><span data-stu-id="e8f22-105">Contains the maximum size, in bytes, the user is allowed to accumulate for a single "extended" rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e8f22-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e8f22-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e8f22-107">PR_EXTENDED_RULE_SIZE_LIMIT</span><span class="sxs-lookup"><span data-stu-id="e8f22-107">PR_EXTENDED_RULE_SIZE_LIMIT</span></span>  <br/> |
|<span data-ttu-id="e8f22-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e8f22-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e8f22-109">0x0E9B</span><span class="sxs-lookup"><span data-stu-id="e8f22-109">0x0E9B</span></span>  <br/> |
|<span data-ttu-id="e8f22-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e8f22-110">Data type:</span></span>  <br/> |<span data-ttu-id="e8f22-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e8f22-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e8f22-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e8f22-112">Area:</span></span>  <br/> |<span data-ttu-id="e8f22-113">Rules</span><span class="sxs-lookup"><span data-stu-id="e8f22-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8f22-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e8f22-114">Remarks</span></span>

<span data-ttu-id="e8f22-115">Si cette propriété est définie sur l’objet d’ouverture de session, le client doit conserver la taille de la propriété **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) sous la valeur spécifiée par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e8f22-115">If this property is set on the logon object, the client should keep the size of the **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) property under the value specified by this property.</span></span> <span data-ttu-id="e8f22-116">En revanche, le serveur doit renvoyer une erreur si le client tente de définir une propriété binaire est trop volumineux.</span><span class="sxs-lookup"><span data-stu-id="e8f22-116">Conversely, the server should return an error if the client does attempt to set a binary property that is too large.</span></span>
  
<span data-ttu-id="e8f22-117">Pour plus d’informations sur les règles d’étendue, voir [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e8f22-117">For information about extended rules, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e8f22-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e8f22-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e8f22-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="e8f22-119">Protocol specifications</span></span>

<span data-ttu-id="e8f22-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8f22-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8f22-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="e8f22-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e8f22-122">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8f22-122">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8f22-123">Spécifie les opérations autorisées pour les objets de banque de messages principale.</span><span class="sxs-lookup"><span data-stu-id="e8f22-123">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e8f22-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e8f22-124">Header files</span></span>

<span data-ttu-id="e8f22-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e8f22-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e8f22-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e8f22-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e8f22-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="e8f22-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e8f22-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="e8f22-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8f22-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8f22-129">See also</span></span>



[<span data-ttu-id="e8f22-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e8f22-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e8f22-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e8f22-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e8f22-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e8f22-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e8f22-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e8f22-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

