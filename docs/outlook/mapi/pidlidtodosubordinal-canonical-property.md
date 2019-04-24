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
ms.openlocfilehash: c4ea125a5bde89e0885be4c04e3f106f202b1e18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344918"
---
# <a name="pidlidtodosubordinal-canonical-property"></a><span data-ttu-id="a92eb-103">Propriété canonique PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="a92eb-103">PidLidToDoSubOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="a92eb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a92eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a92eb-105">Agit comme un disjoncteur de liaison lorsque la propriété **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) trie les objets et le résultat en un lien.</span><span class="sxs-lookup"><span data-stu-id="a92eb-105">Acts as a tie breaker when the **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) property sorts objects and the result in a tie.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a92eb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a92eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a92eb-107">dispidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="a92eb-107">dispidToDoSubOrdinal</span></span>  <br/> |
|<span data-ttu-id="a92eb-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="a92eb-108">Property set:</span></span>  <br/> |<span data-ttu-id="a92eb-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a92eb-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a92eb-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="a92eb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a92eb-111">0x000085A1</span><span class="sxs-lookup"><span data-stu-id="a92eb-111">0x000085A1</span></span>  <br/> |
|<span data-ttu-id="a92eb-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a92eb-112">Data type:</span></span>  <br/> |<span data-ttu-id="a92eb-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a92eb-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a92eb-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a92eb-114">Area:</span></span>  <br/> |<span data-ttu-id="a92eb-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="a92eb-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a92eb-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="a92eb-116">Remarks</span></span>

<span data-ttu-id="a92eb-117">Si elle est utilisée, cette propriété doit être triée lexicographically.</span><span class="sxs-lookup"><span data-stu-id="a92eb-117">If used, this property must be sorted lexicographically.</span></span> <span data-ttu-id="a92eb-118">Les caractères des composants de la chaîne doivent être constitués uniquement des chiffres 0 à 9.</span><span class="sxs-lookup"><span data-stu-id="a92eb-118">The component characters of the string must consist of only the numerals zero through nine.</span></span> <span data-ttu-id="a92eb-119">Cette propriété doit être définie initialement sur «5555555».</span><span class="sxs-lookup"><span data-stu-id="a92eb-119">This property should be initially set to "5555555".</span></span> <span data-ttu-id="a92eb-120">La longueur de cette propriété ne doit pas dépasser 254 caractères (à l'exception du caractère NULL de fin).</span><span class="sxs-lookup"><span data-stu-id="a92eb-120">The length of this property must not exceed 254 characters (excluding the terminating NULL character).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a92eb-121">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="a92eb-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a92eb-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="a92eb-122">Protocol specifications</span></span>

<span data-ttu-id="a92eb-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a92eb-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a92eb-124">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="a92eb-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a92eb-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a92eb-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a92eb-126">Spécifie les propriétés et les opérations relatives au marquage.</span><span class="sxs-lookup"><span data-stu-id="a92eb-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a92eb-127">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="a92eb-127">Header files</span></span>

<span data-ttu-id="a92eb-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a92eb-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="a92eb-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a92eb-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a92eb-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a92eb-130">See also</span></span>



[<span data-ttu-id="a92eb-131">Propriété canonique PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="a92eb-131">PidLidToDoOrdinalDate Canonical Property</span></span>](pidlidtodoordinaldate-canonical-property.md)


[<span data-ttu-id="a92eb-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a92eb-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a92eb-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a92eb-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a92eb-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a92eb-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a92eb-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a92eb-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

