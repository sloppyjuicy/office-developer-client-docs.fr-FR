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
ms.openlocfilehash: 5dd0d4c19f30e189218b1aeddd333df58e42102a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316288"
---
# <a name="pidtagflagcompletetime-canonical-property"></a><span data-ttu-id="6f6cd-103">Propriété canonique PidTagFlagCompleteTime</span><span class="sxs-lookup"><span data-stu-id="6f6cd-103">PidTagFlagCompleteTime Canonical Property</span></span>

  
  
<span data-ttu-id="6f6cd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f6cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f6cd-105">Spécifie la date et l'heure au format UTC (Coordinated Universal Time) auxquelles l'objet message a été marqué comme étant terminé.</span><span class="sxs-lookup"><span data-stu-id="6f6cd-105">Specifies the date and time in Coordinated Universal Time (UTC) that the message object was flagged as completed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f6cd-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6f6cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f6cd-107">PR_FLAG_COMPLETE_TIME</span><span class="sxs-lookup"><span data-stu-id="6f6cd-107">PR_FLAG_COMPLETE_TIME</span></span>  <br/> |
|<span data-ttu-id="6f6cd-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6f6cd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f6cd-109">0x1091</span><span class="sxs-lookup"><span data-stu-id="6f6cd-109">0x1091</span></span>  <br/> |
|<span data-ttu-id="6f6cd-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6f6cd-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f6cd-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="6f6cd-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="6f6cd-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6f6cd-112">Area:</span></span>  <br/> |<span data-ttu-id="6f6cd-113">Divers</span><span class="sxs-lookup"><span data-stu-id="6f6cd-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f6cd-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6f6cd-114">Remarks</span></span>

<span data-ttu-id="6f6cd-115">Cette propriété est supprimée si l'objet message n'est pas marqué comme terminé.</span><span class="sxs-lookup"><span data-stu-id="6f6cd-115">This property is deleted if the message object is not flagged complete.</span></span> <span data-ttu-id="6f6cd-116">La plus petite résolution du temps doit être de minutes (la valeur doit être un multiple de 600 millions).</span><span class="sxs-lookup"><span data-stu-id="6f6cd-116">The time's smallest resolution must be minutes (the value must be a multiple of 600,000,000).</span></span> <span data-ttu-id="6f6cd-117">Cette propriété ne doit pas exister si l'objet est un objet lié à la réunion et qu'il ne doit pas exister sur un objet Task.</span><span class="sxs-lookup"><span data-stu-id="6f6cd-117">This property must not exist if the object is a meeting-related object, and it should not exist on a task object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6f6cd-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="6f6cd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6f6cd-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="6f6cd-119">Protocol specifications</span></span>

<span data-ttu-id="6f6cd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f6cd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f6cd-121">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="6f6cd-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6f6cd-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f6cd-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f6cd-123">Spécifie les propriétés et les opérations relatives au marquage.</span><span class="sxs-lookup"><span data-stu-id="6f6cd-123">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6f6cd-124">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="6f6cd-124">Header files</span></span>

<span data-ttu-id="6f6cd-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6f6cd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f6cd-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6f6cd-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f6cd-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="6f6cd-127">Mapitags.h</span></span>
  
> <span data-ttu-id="6f6cd-128">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="6f6cd-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f6cd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f6cd-129">See also</span></span>



[<span data-ttu-id="6f6cd-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6f6cd-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f6cd-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6f6cd-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f6cd-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6f6cd-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f6cd-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6f6cd-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

