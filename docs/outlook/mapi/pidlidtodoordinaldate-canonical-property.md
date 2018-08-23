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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b19f36337459753e153a96021b1d70308b374bed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577757"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a><span data-ttu-id="0415f-103">Propriété canonique PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="0415f-103">PidLidToDoOrdinalDate Canonical Property</span></span>

  
  
<span data-ttu-id="0415f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0415f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0415f-105">Détermine l’ordre de tri des objets dans une liste de tâches consolidée.</span><span class="sxs-lookup"><span data-stu-id="0415f-105">Determines the sort order of objects in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0415f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0415f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0415f-107">dispidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="0415f-107">dispidToDoOrdinalDate</span></span>  <br/> |
|<span data-ttu-id="0415f-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="0415f-108">Property set:</span></span>  <br/> |<span data-ttu-id="0415f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="0415f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="0415f-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="0415f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0415f-111">0x000085A0</span><span class="sxs-lookup"><span data-stu-id="0415f-111">0x000085A0</span></span>  <br/> |
|<span data-ttu-id="0415f-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0415f-112">Data type:</span></span>  <br/> |<span data-ttu-id="0415f-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="0415f-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="0415f-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0415f-114">Area:</span></span>  <br/> |<span data-ttu-id="0415f-115">Task</span><span class="sxs-lookup"><span data-stu-id="0415f-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0415f-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="0415f-116">Remarks</span></span>

<span data-ttu-id="0415f-117">Lorsqu’un objet est marqué, cette propriété doit être définie à l’heure actuelle en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="0415f-117">When an object is flagged, this property should be set to the current time in Coordinated Universal Time (UTC).</span></span> 
  
<span data-ttu-id="0415f-118">Si le client permet à un utilisateur réorganiser les tâches dans la liste des tâches consolidée par le biais de déplacement ou d’autres mécanismes, ils peuvent utiliser n’importe quel algorithme approprié pour déterminer la nouvelle valeur de cette propriété afin que la tâche s’affiche dans l’emplacement correct lorsque cette propriété est utilisée comme un trier champ Ting.</span><span class="sxs-lookup"><span data-stu-id="0415f-118">If the client allows a user to reorder tasks within the consolidated task list via dragging or other mechanisms, they can use any suitable algorithm to determine the new value of this property so that the task appears in the correct place when this property is used as a sorting field.</span></span>
  
<span data-ttu-id="0415f-119">Lorsque cette propriété est utilisée pour trier les objets et les tri des résultats d’égalité, la propriété **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) est utilisée comme un séparateur de jonction.</span><span class="sxs-lookup"><span data-stu-id="0415f-119">When this property is used to sort objects and the sort results in a tie, the **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) property is used as a tie breaker.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0415f-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0415f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0415f-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="0415f-121">Protocol specifications</span></span>

<span data-ttu-id="0415f-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0415f-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0415f-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="0415f-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0415f-124">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0415f-124">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0415f-125">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="0415f-125">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0415f-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0415f-126">Header files</span></span>

<span data-ttu-id="0415f-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0415f-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0415f-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0415f-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0415f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0415f-129">See also</span></span>



[<span data-ttu-id="0415f-130">Propriété canonique PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="0415f-130">PidLidToDoSubOrdinal Canonical Property</span></span>](pidlidtodosubordinal-canonical-property.md)


[<span data-ttu-id="0415f-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0415f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0415f-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0415f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0415f-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0415f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0415f-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0415f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

