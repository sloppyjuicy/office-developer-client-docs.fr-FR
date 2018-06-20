---
title: Propriété canonique PidLidToDoOrdinalDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoOrdinalDate
api_type:
- COM
ms.assetid: b6a500fc-07f4-4788-ae46-d179a96a48e2
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d708424ccb15be15746fe8a33eea73a8e0f99323
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785499"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a><span data-ttu-id="bf8b2-103">Propriété canonique PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="bf8b2-103">PidLidToDoOrdinalDate Canonical Property</span></span>

  
  
<span data-ttu-id="bf8b2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf8b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf8b2-105">Détermine l’ordre de tri des objets dans une liste de tâches consolidée.</span><span class="sxs-lookup"><span data-stu-id="bf8b2-105">Determines the sort order of objects in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf8b2-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bf8b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf8b2-107">dispidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="bf8b2-107">dispidToDoOrdinalDate</span></span>  <br/> |
|<span data-ttu-id="bf8b2-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="bf8b2-108">Property set:</span></span>  <br/> |<span data-ttu-id="bf8b2-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="bf8b2-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="bf8b2-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="bf8b2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bf8b2-111">0x000085A0</span><span class="sxs-lookup"><span data-stu-id="bf8b2-111">0x000085A0</span></span>  <br/> |
|<span data-ttu-id="bf8b2-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="bf8b2-112">Data type:</span></span>  <br/> |<span data-ttu-id="bf8b2-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="bf8b2-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="bf8b2-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="bf8b2-114">Area:</span></span>  <br/> |<span data-ttu-id="bf8b2-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="bf8b2-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf8b2-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="bf8b2-116">Remarks</span></span>

<span data-ttu-id="bf8b2-117">Lorsqu’un objet est marqué, cette propriété doit être définie à l’heure actuelle en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="bf8b2-117">When an object is flagged, this property should be set to the current time in Coordinated Universal Time (UTC).</span></span> 
  
<span data-ttu-id="bf8b2-118">Si le client permet à un utilisateur réorganiser les tâches dans la liste des tâches consolidée par le biais de déplacement ou d’autres mécanismes, ils peuvent utiliser n’importe quel algorithme approprié pour déterminer la nouvelle valeur de cette propriété afin que la tâche s’affiche dans l’emplacement correct lorsque cette propriété est utilisée comme un trier champ Ting.</span><span class="sxs-lookup"><span data-stu-id="bf8b2-118">If the client allows a user to reorder tasks within the consolidated task list via dragging or other mechanisms, they can use any suitable algorithm to determine the new value of this property so that the task appears in the correct place when this property is used as a sorting field.</span></span>
  
<span data-ttu-id="bf8b2-119">Lorsque cette propriété est utilisée pour trier les objets et les tri des résultats d’égalité, la propriété **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) est utilisée comme un séparateur de jonction.</span><span class="sxs-lookup"><span data-stu-id="bf8b2-119">When this property is used to sort objects and the sort results in a tie, the **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) property is used as a tie breaker.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bf8b2-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="bf8b2-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bf8b2-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="bf8b2-121">Protocol specifications</span></span>

<span data-ttu-id="bf8b2-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf8b2-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf8b2-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="bf8b2-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bf8b2-124">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf8b2-124">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf8b2-125">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="bf8b2-125">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bf8b2-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="bf8b2-126">Header files</span></span>

<span data-ttu-id="bf8b2-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf8b2-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf8b2-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bf8b2-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf8b2-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf8b2-129">See also</span></span>



[<span data-ttu-id="bf8b2-130">Propriété canonique PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="bf8b2-130">PidLidToDoSubOrdinal Canonical Property</span></span>](pidlidtodosubordinal-canonical-property.md)


[<span data-ttu-id="bf8b2-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bf8b2-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf8b2-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="bf8b2-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf8b2-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="bf8b2-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf8b2-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="bf8b2-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

