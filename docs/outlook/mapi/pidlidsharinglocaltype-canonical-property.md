---
title: Propriété canonique PidLidSharingLocalType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingLocalType
api_type:
- COM
ms.assetid: 6ac438a1-d36f-424f-b4b4-d6f2d26fd350
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f24486270f5f20596e76781c7ddf4cbc90e17a11
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583952"
---
# <a name="pidlidsharinglocaltype-canonical-property"></a><span data-ttu-id="64744-103">Propriété canonique PidLidSharingLocalType</span><span class="sxs-lookup"><span data-stu-id="64744-103">PidLidSharingLocalType Canonical Property</span></span>

  
  
<span data-ttu-id="64744-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64744-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64744-105">Spécifie la valeur de la propriété **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) du dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="64744-105">Specifies the value of the **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of the folder that is being shared.</span></span> <span data-ttu-id="64744-106">Il s’agit d’une propriété d’un message de partage.</span><span class="sxs-lookup"><span data-stu-id="64744-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64744-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="64744-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="64744-108">dispidSharingLocalType</span><span class="sxs-lookup"><span data-stu-id="64744-108">dispidSharingLocalType</span></span>  <br/> |
|<span data-ttu-id="64744-109">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="64744-109">Property set:</span></span>  <br/> |<span data-ttu-id="64744-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="64744-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="64744-111">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="64744-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="64744-112">0x00008A14</span><span class="sxs-lookup"><span data-stu-id="64744-112">0x00008A14</span></span>  <br/> |
|<span data-ttu-id="64744-113">Type de données :</span><span class="sxs-lookup"><span data-stu-id="64744-113">Data type:</span></span>  <br/> |<span data-ttu-id="64744-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="64744-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="64744-115">Domaine :</span><span class="sxs-lookup"><span data-stu-id="64744-115">Area:</span></span>  <br/> |<span data-ttu-id="64744-116">Partage</span><span class="sxs-lookup"><span data-stu-id="64744-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64744-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="64744-117">Remarks</span></span>

<span data-ttu-id="64744-118">La valeur de cette propriété doit être une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="64744-118">The value of this property must be one of the following:</span></span>
  
- <span data-ttu-id="64744-119">« ERREUR. Rendez-vous »</span><span class="sxs-lookup"><span data-stu-id="64744-119">"IPF.Appointment"</span></span>
    
- <span data-ttu-id="64744-120">« ERREUR. Contact »</span><span class="sxs-lookup"><span data-stu-id="64744-120">"IPF.Contact"</span></span>
    
- <span data-ttu-id="64744-121">« ERREUR. Tâche »</span><span class="sxs-lookup"><span data-stu-id="64744-121">"IPF.Task"</span></span>
    
- <span data-ttu-id="64744-122">« ERREUR. StickyNote »</span><span class="sxs-lookup"><span data-stu-id="64744-122">"IPF.StickyNote"</span></span>
    
- <span data-ttu-id="64744-123">« ERREUR. Journal »</span><span class="sxs-lookup"><span data-stu-id="64744-123">"IPF.Journal"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="64744-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="64744-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64744-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="64744-125">Protocol specifications</span></span>

<span data-ttu-id="64744-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64744-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64744-127">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="64744-127">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="64744-128">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64744-128">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64744-129">Partage des dossiers de boîte aux lettres entre des clients.</span><span class="sxs-lookup"><span data-stu-id="64744-129">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64744-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="64744-130">Header files</span></span>

<span data-ttu-id="64744-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64744-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="64744-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="64744-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64744-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64744-133">See also</span></span>



[<span data-ttu-id="64744-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="64744-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64744-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="64744-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64744-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="64744-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64744-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="64744-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

