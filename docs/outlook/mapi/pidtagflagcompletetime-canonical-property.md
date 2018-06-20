---
title: Propriété canonique PidTagFlagCompleteTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagCompleteTime
api_type:
- HeaderDef
ms.assetid: effc738a-30f4-4a5e-b21d-04b50dad1f45
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: efaa8cf84204234697431a190a5cb6745b55ecae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785983"
---
# <a name="pidtagflagcompletetime-canonical-property"></a><span data-ttu-id="72030-103">Propriété canonique PidTagFlagCompleteTime</span><span class="sxs-lookup"><span data-stu-id="72030-103">PidTagFlagCompleteTime Canonical Property</span></span>

  
  
<span data-ttu-id="72030-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72030-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72030-105">Spécifie la date et l’heure en temps universel coordonné (UTC) que l’objet du message a été marqué comme étant achevée.</span><span class="sxs-lookup"><span data-stu-id="72030-105">Specifies the date and time in Coordinated Universal Time (UTC) that the message object was flagged as completed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72030-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="72030-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72030-107">PR_FLAG_COMPLETE_TIME</span><span class="sxs-lookup"><span data-stu-id="72030-107">PR_FLAG_COMPLETE_TIME</span></span>  <br/> |
|<span data-ttu-id="72030-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="72030-108">Identifier:</span></span>  <br/> |<span data-ttu-id="72030-109">0x1091</span><span class="sxs-lookup"><span data-stu-id="72030-109">0x1091</span></span>  <br/> |
|<span data-ttu-id="72030-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="72030-110">Data type:</span></span>  <br/> |<span data-ttu-id="72030-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="72030-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="72030-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="72030-112">Area:</span></span>  <br/> |<span data-ttu-id="72030-113">Divers</span><span class="sxs-lookup"><span data-stu-id="72030-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72030-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="72030-114">Remarks</span></span>

<span data-ttu-id="72030-115">Cette propriété est supprimée si l’objet du message n’est pas marqué comme terminé.</span><span class="sxs-lookup"><span data-stu-id="72030-115">This property is deleted if the message object is not flagged complete.</span></span> <span data-ttu-id="72030-116">Résolution la plus faible de l’heure doit être minutes (la valeur doit être un multiple de 600,000,000).</span><span class="sxs-lookup"><span data-stu-id="72030-116">The time's smallest resolution must be minutes (the value must be a multiple of 600,000,000).</span></span> <span data-ttu-id="72030-117">Cette propriété ne doit pas exister si l’objet est un objet liées à la réunion, et il ne doit pas exister sur un objet task.</span><span class="sxs-lookup"><span data-stu-id="72030-117">This property must not exist if the object is a meeting-related object, and it should not exist on a task object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="72030-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="72030-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="72030-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="72030-119">Protocol specifications</span></span>

<span data-ttu-id="72030-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72030-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72030-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="72030-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="72030-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72030-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72030-123">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="72030-123">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="72030-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="72030-124">Header files</span></span>

<span data-ttu-id="72030-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72030-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="72030-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="72030-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="72030-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="72030-127">Mapitags.h</span></span>
  
> <span data-ttu-id="72030-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="72030-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72030-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72030-129">See also</span></span>



[<span data-ttu-id="72030-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="72030-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72030-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="72030-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72030-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="72030-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72030-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="72030-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

