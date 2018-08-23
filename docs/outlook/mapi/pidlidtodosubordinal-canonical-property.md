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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 98dfdab24d2c4170609d9db1c3104a3f17436736
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578065"
---
# <a name="pidlidtodosubordinal-canonical-property"></a><span data-ttu-id="f7291-103">Propriété canonique PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="f7291-103">PidLidToDoSubOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="f7291-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7291-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7291-105">Agit comme un séparateur de jonction lorsque la propriété **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) trie les objets et le résultat dans un lien.</span><span class="sxs-lookup"><span data-stu-id="f7291-105">Acts as a tie breaker when the **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) property sorts objects and the result in a tie.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7291-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f7291-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7291-107">dispidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="f7291-107">dispidToDoSubOrdinal</span></span>  <br/> |
|<span data-ttu-id="f7291-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="f7291-108">Property set:</span></span>  <br/> |<span data-ttu-id="f7291-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f7291-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f7291-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="f7291-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f7291-111">0x000085A1</span><span class="sxs-lookup"><span data-stu-id="f7291-111">0x000085A1</span></span>  <br/> |
|<span data-ttu-id="f7291-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f7291-112">Data type:</span></span>  <br/> |<span data-ttu-id="f7291-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f7291-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f7291-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f7291-114">Area:</span></span>  <br/> |<span data-ttu-id="f7291-115">Task</span><span class="sxs-lookup"><span data-stu-id="f7291-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7291-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f7291-116">Remarks</span></span>

<span data-ttu-id="f7291-117">En cas d’utilisation, cette propriété doit être triée lexicographiquement.</span><span class="sxs-lookup"><span data-stu-id="f7291-117">If used, this property must be sorted lexicographically.</span></span> <span data-ttu-id="f7291-118">Les caractères d’un composant de la chaîne doivent contenir uniquement les chiffres zéro à neuf.</span><span class="sxs-lookup"><span data-stu-id="f7291-118">The component characters of the string must consist of only the numerals zero through nine.</span></span> <span data-ttu-id="f7291-119">Cette propriété doit être définie à l’origine pour « 5555555 ».</span><span class="sxs-lookup"><span data-stu-id="f7291-119">This property should be initially set to "5555555".</span></span> <span data-ttu-id="f7291-120">La longueur de cette propriété ne doit pas dépasser 254 caractères (à l’exception du caractère de fin NULL).</span><span class="sxs-lookup"><span data-stu-id="f7291-120">The length of this property must not exceed 254 characters (excluding the terminating NULL character).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f7291-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f7291-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7291-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f7291-122">Protocol specifications</span></span>

<span data-ttu-id="f7291-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7291-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7291-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="f7291-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f7291-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7291-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7291-126">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="f7291-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7291-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f7291-127">Header files</span></span>

<span data-ttu-id="f7291-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7291-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7291-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f7291-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7291-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7291-130">See also</span></span>



[<span data-ttu-id="f7291-131">Propriété canonique PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="f7291-131">PidLidToDoOrdinalDate Canonical Property</span></span>](pidlidtodoordinaldate-canonical-property.md)


[<span data-ttu-id="f7291-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f7291-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7291-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f7291-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7291-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f7291-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7291-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f7291-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

