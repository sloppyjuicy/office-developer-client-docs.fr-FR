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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 01d25614780f10f30d9e1314ea7f60ad3fbb4af0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785988"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a><span data-ttu-id="edeef-103">Propriété canonique PidTagExtendedRuleSizeLimit</span><span class="sxs-lookup"><span data-stu-id="edeef-103">PidTagExtendedRuleSizeLimit Canonical Property</span></span>

  
  
<span data-ttu-id="edeef-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="edeef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="edeef-105">Indique la taille maximale, en octets, l’utilisateur est autorisé à s’accumulent pour une seule règle « étendue ».</span><span class="sxs-lookup"><span data-stu-id="edeef-105">Contains the maximum size, in bytes, the user is allowed to accumulate for a single "extended" rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="edeef-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="edeef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="edeef-107">PR_EXTENDED_RULE_SIZE_LIMIT</span><span class="sxs-lookup"><span data-stu-id="edeef-107">PR_EXTENDED_RULE_SIZE_LIMIT</span></span>  <br/> |
|<span data-ttu-id="edeef-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="edeef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="edeef-109">0x0E9B</span><span class="sxs-lookup"><span data-stu-id="edeef-109">0x0E9B</span></span>  <br/> |
|<span data-ttu-id="edeef-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="edeef-110">Data type:</span></span>  <br/> |<span data-ttu-id="edeef-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="edeef-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="edeef-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="edeef-112">Area:</span></span>  <br/> |<span data-ttu-id="edeef-113">Règles</span><span class="sxs-lookup"><span data-stu-id="edeef-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edeef-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="edeef-114">Remarks</span></span>

<span data-ttu-id="edeef-115">Si cette propriété est définie sur l’objet d’ouverture de session, le client doit conserver la taille de la propriété **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) sous la valeur spécifiée par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="edeef-115">If this property is set on the logon object, the client should keep the size of the **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) property under the value specified by this property.</span></span> <span data-ttu-id="edeef-116">En revanche, le serveur doit renvoyer une erreur si le client tente de définir une propriété binaire est trop volumineux.</span><span class="sxs-lookup"><span data-stu-id="edeef-116">Conversely, the server should return an error if the client does attempt to set a binary property that is too large.</span></span>
  
<span data-ttu-id="edeef-117">Pour plus d’informations sur les règles d’étendue, voir [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="edeef-117">For information about extended rules, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="edeef-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="edeef-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="edeef-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="edeef-119">Protocol specifications</span></span>

<span data-ttu-id="edeef-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edeef-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edeef-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="edeef-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="edeef-122">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edeef-122">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edeef-123">Spécifie les opérations autorisées pour les objets de banque de messages principale.</span><span class="sxs-lookup"><span data-stu-id="edeef-123">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="edeef-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="edeef-124">Header files</span></span>

<span data-ttu-id="edeef-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="edeef-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="edeef-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="edeef-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="edeef-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="edeef-127">Mapitags.h</span></span>
  
> <span data-ttu-id="edeef-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="edeef-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="edeef-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edeef-129">See also</span></span>



[<span data-ttu-id="edeef-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="edeef-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="edeef-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="edeef-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="edeef-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="edeef-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="edeef-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="edeef-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

