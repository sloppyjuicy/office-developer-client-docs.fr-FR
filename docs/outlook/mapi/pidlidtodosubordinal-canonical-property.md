---
title: Propriété canonique PidLidToDoSubOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoSubOrdinal
api_type:
- COM
ms.assetid: e3bc15ef-155e-49fd-88e5-64713df9b939
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9965ed059ba4596232111f5fbd86b9d177e3c3dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785497"
---
# <a name="pidlidtodosubordinal-canonical-property"></a><span data-ttu-id="5739d-103">Propriété canonique PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="5739d-103">PidLidToDoSubOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="5739d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5739d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5739d-105">Agit comme un séparateur de jonction lorsque la propriété **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) trie les objets et le résultat dans un lien.</span><span class="sxs-lookup"><span data-stu-id="5739d-105">Acts as a tie breaker when the **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) property sorts objects and the result in a tie.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5739d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5739d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5739d-107">dispidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="5739d-107">dispidToDoSubOrdinal</span></span>  <br/> |
|<span data-ttu-id="5739d-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="5739d-108">Property set:</span></span>  <br/> |<span data-ttu-id="5739d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5739d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5739d-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="5739d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5739d-111">0x000085A1</span><span class="sxs-lookup"><span data-stu-id="5739d-111">0x000085A1</span></span>  <br/> |
|<span data-ttu-id="5739d-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5739d-112">Data type:</span></span>  <br/> |<span data-ttu-id="5739d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5739d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5739d-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="5739d-114">Area:</span></span>  <br/> |<span data-ttu-id="5739d-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="5739d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5739d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="5739d-116">Remarks</span></span>

<span data-ttu-id="5739d-117">En cas d’utilisation, cette propriété doit être triée lexicographiquement.</span><span class="sxs-lookup"><span data-stu-id="5739d-117">If used, this property must be sorted lexicographically.</span></span> <span data-ttu-id="5739d-118">Les caractères d’un composant de la chaîne doivent contenir uniquement les chiffres zéro à neuf.</span><span class="sxs-lookup"><span data-stu-id="5739d-118">The component characters of the string must consist of only the numerals zero through nine.</span></span> <span data-ttu-id="5739d-119">Cette propriété doit être définie à l’origine pour « 5555555 ».</span><span class="sxs-lookup"><span data-stu-id="5739d-119">This property should be initially set to "5555555".</span></span> <span data-ttu-id="5739d-120">La longueur de cette propriété ne doit pas dépasser 254 caractères (à l’exception du caractère de fin NULL).</span><span class="sxs-lookup"><span data-stu-id="5739d-120">The length of this property must not exceed 254 characters (excluding the terminating NULL character).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5739d-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5739d-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5739d-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="5739d-122">Protocol specifications</span></span>

<span data-ttu-id="5739d-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5739d-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5739d-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="5739d-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5739d-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5739d-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5739d-126">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="5739d-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5739d-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5739d-127">Header files</span></span>

<span data-ttu-id="5739d-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5739d-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="5739d-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5739d-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5739d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5739d-130">See also</span></span>



[<span data-ttu-id="5739d-131">Propriété canonique PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="5739d-131">PidLidToDoOrdinalDate Canonical Property</span></span>](pidlidtodoordinaldate-canonical-property.md)


[<span data-ttu-id="5739d-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5739d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5739d-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5739d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5739d-134">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5739d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5739d-135">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="5739d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

